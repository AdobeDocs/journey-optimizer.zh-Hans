---
solution: Journey Optimizer
product: journey optimizer
title: 在登陆页面中使用自定义JavaScript
description: 了解如何在Journey Optimizer中设计登陆页面的内容
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
exl-id: 2a7ebead-5f09-4ea5-8f00-8b5625963290
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '559'
ht-degree: 2%

---

# 在登陆页面中使用自定义JavaScript {#lp-custom-js}

您可以使用自定义JavaScript定义登陆页面内容。 例如，如果您需要执行高级样式，或者要向登陆页面添加自定义行为，则可以构建并在中执行您自己的控件 [!DNL Journey Optimizer].

## 将JavaScript代码插入登陆页面

要将自定义JavaScript插入登陆页面内容，您可以执行以下操作：

* 在开始创建内容时导入现有HTML内容，然后选择包含自定义JavaScript代码的文件。 了解如何导入内容 [在此部分中](../design/existing-content.md).

* 从头开始或从保存的模板开始设计登陆页面。 拖放 **[!UICONTROL HTML]** 内容组件添加到画布中，并显示源代码以将您的JavaSCript添加到组件中。 了解如何在中使用HTML组件 [此部分](../design/content-components.md#HTML). <!--You can also simply switch the whole landing page content to code view and enter or paste your JavaScript code.-->

   ![](assets/lp_designer-html-component.png)

* 直接在内容设计器中输入或粘贴JavaScript代码。 了解如何编码您自己的内容 [在此部分中](../design/code-content.md).

>[!NOTE]
>
>目前，您无法在 [预览登陆页面](create-lp.md#test-landing-page).

要正确显示登陆页面，请按照以下各节所述使用以下语法。

## 代码初始化

要初始化JavaScript代码，您必须使用 `lpRuntimeReady` 事件。 成功初始化库后，将触发此事件。 将使用 `lpRuntime` 对象以公开库方法和挂钩。

`LpRuntime` 表示“登陆页面运行时”。 此对象是主库标识符。 它将公开挂接、表单提交方法以及可在自定义JavaScript中使用的其他实用工具方法。

**示例：**

```
if(window.lpRuntime){
    init(window.lpRuntime);
}else{
    window.addEventListener('lpRuntimeReady',function(e){
        init(e.detail);
    });
}
 
function init(lpRuntime){
    // Enter custom JavaScript here using methods from lpRuntime.
}
```

## 挂钩

使用挂钩，您可以在表单提交的生命周期中附加方法。 例如，您可以在实际提交表单之前，使用挂接执行某些表单验证。

以下是您可以使用的挂钩：

| 名称 | 描述 |
|--- |--- |
| addBeforeSubmitHook | 在提交表单之前调用的自定义挂接。 返回true以继续提交，否则返回false以阻止提交。 |
| addOnFailureHook | 在表单提交失败时调用的自定义挂接。 |
| addOnSuccessHook | 在成功提交表单时调用的自定义挂接。 |

**示例：**

```
//LpRuntime hooks
lpRuntime.hooks.addBeforeSubmitHook(function(){
    // Add your validation logic here.
});
```

## 自定义表单提交

下面列出的方法用于执行自定义表单提交。

>[!NOTE]
>
>由于表单提交由自定义JavaScript处理，因此需要通过设置全局变量来明确禁用默认提交 `disableDefaultFormSubmission` to `true`.

| 名称 | 描述 |
|--- |--- |
| submitForm | 此方法将提交表单并处理帖子提交流程。 |
| submitFormPartial | 此方法也将提交表单，但将跳过帖子提交流程。 例如，如果您已配置重定向到成功页面后成功提交的页面，则在部分表单提交的情况下不会发生重定向。 |

**示例：**

```
//LpRuntime methods
window.disableDefaultFormSubmission = true        // Flag to disable the default submission flow.
 
lpRuntime.submitForm(formSubmissionData);         // This will trigger the default form submission handling like redirecting to error or success page.
  
lpRuntime.submitFormPartial(formSubmissionData,{   // This will not trigger the default submission handling.
    beforeSubmit : callback,
    onFailure : failureCallback,                   // Custom onFailureCallback - will be used in partial submission of form.
    onSuccess : successCallback                    // Custom onSuccessCallback - will be used in partial submission of form.
})
```

## 实用程序函数

| 名称 | 描述 |
|--- |--- |
| getFormData | 此方法可用于获取 `formData` 以JSON对象的形式显示。 此对象可以传递到 `submitForm` 表单提交。 |

**示例：**

```
let formData = lpRuntime.getFormData();                           // Method to generate formdata
 
lpRuntime.submitForm(formData);
```

## 用例

### 用例1:在表单提交之前添加验证

```
<html>
<body>
// Enter HTML body here.
  
<script>
        if(window.lpRuntime){
          console.log('got runtime',lpRuntime);
          init(window.lpRuntime);
        }else{
          window.addEventListener('lpRuntimeReady',function(e){
            init(window.lpRuntime);
          });
        }
        
  
      // Here validate the function is checking if the checkbox is selected. This method should return true if you want form submission.
      function validateForm(){
        return document.querySelector('.spectrum-Checkbox-input').checked;
      }    
  
      function init(lpRuntime){
          lpRuntime.hooks.addBeforeSubmitHook(function(){
              return validateForm(); // This method should return true if you want to proceed with submission.
          })
      }
  
</script>  
  
</body>
</html>
```

### 用例2:部分表单提交

例如，您的表单上有多个复选框。 选中任何复选框后，您希望此数据保存到后端，而无需等待用户单击提交按钮。

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <input type='checkbox' value="2" name="name2"/>
        <input type='checkbox' value="3" name="name3"/>
        <input type='checkbox' value="4" name="name4"/>
    </form>
  
<script>
      window.disableDefaultFormSubmission=true;
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
     function init(lpRuntime){
        window.getElementByTagName('input').addEventListener('change',function(e){
            let formData = lpRuntime.getFormData();
            lpRuntime.submitFormPartial(formData);
        })
      }
    </script>
  
</body>
</html>
```

### 用例3:自定义Analytics标记

使用JavaScript，您可以添加输入字段的侦听器并附加自定义分析调用触发器。

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <input type='checkbox' value="2" name="name2"/>
        <input type='checkbox' value="3" name="name3"/>
        <input type='checkbox' value="4" name="name4"/>
    </form>
  
<script>
      window.disableDefaultFormSubmission=false;  
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
     function init(lpRuntime){
         window.getElementByTagName('input').addEventListener('change',function(e){
            //trigger analytics events
        })
      }
        
    </script>
  
</body>
</html>
```

### 用例4:动态表单

```
<html>
<body>
    <form>
        <input type='checkbox' value="1" name="name1"/>
        <div class="hiddenInput hidden">
            <input type='text' name="name2"/>
        </div>
    </form>
  
<script>
      window.disableDefaultFormSubmission=false;     
 
      window.addEventListener('lpRuntimeReady',function(e){        
        init(e.detail)
      }
 
      function init(lpRuntime){
        window.getElementByTagName('input').addEventListener('change',function(e){
            document.querySelector('.hiddenInput').toggleClass('hidden');
        })
      }
        
    </script>
  
</body>
</html>
```
