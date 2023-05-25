---
solution: Journey Optimizer
product: journey optimizer
title: 在登陆页面中使用自定义JavaScript
description: 了解如何在Journey Optimizer中设计登陆页面的内容
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
keywords: 登录，登陆页面， javascript，代码
exl-id: 2a7ebead-5f09-4ea5-8f00-8b5625963290
source-git-commit: c0afa3e2bc6dbcb0f2f2357eebc04285de8c5773
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 2%

---

# 在登陆页面中使用自定义JavaScript {#lp-custom-js}

您可以使用自定义JavaScript定义登陆页面内容。 例如，如果您需要执行高级样式设置，或者希望将自定义行为添加到登陆页面，则可以构建自己的控件并在中执行这些控件 [!DNL Journey Optimizer].

## 将JavaScript代码插入登陆页面

要将自定义JavaScript插入到登陆页面内容中，您可以执行以下操作：

* 开始创建内容时导入现有HTML内容，然后选择包含自定义JavaScript代码的文件。 了解如何导入内容 [在此部分中](../email/existing-content.md).

* 从头开始或从保存的模板设计登陆页面。 拖放 **[!UICONTROL HTML]** 将内容组件添加到画布中并显示源代码以将JavaScript添加到组件中。 了解如何在中使用HTML组件 [本节](../email/content-components.md#HTML). <!--You can also simply switch the whole landing page content to code view and enter or paste your JavaScript code.-->

   ![](assets/lp_designer-html-component.png)

* 将JavaScript代码直接输入或粘贴到内容设计器中。 了解如何为自己的内容编码 [在此部分中](../email/code-content.md).

>[!NOTE]
>
>目前，在以下情况下，您无法显示JavaScript正在使用 [预览登陆页面](create-lp.md#test-landing-page).

要正确显示登陆页面，请使用以下语法，如下节所述。

## 代码初始化

要初始化JavaScript代码，您必须使用 `lpRuntimeReady` 事件。 成功初始化库后，将触发此事件。 回调将通过以下方式执行 `lpRuntime` 对象来公开库方法和挂接。

`LpRuntime` 表示“登陆页面运行时”。 此对象是主库标识符。 它会公开挂接、表单提交方法以及在自定义JavaScript中使用的其他实用程序方法。

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

通过使用挂接，您可以在表单提交的生命周期中附加方法。 例如，您可以使用挂接在实际提交表单之前执行某些表单验证。

以下是您可以使用的挂钩：

| 名称 | 描述 |
|--- |--- |
| addBeforeSubmitHook | 在提交表单之前调用的自定义挂接。 返回true可继续提交，返回false可阻止提交。 |
| addOnFailureHook | 在失败的表单提交时调用的自定义挂接。 |
| addOnSuccessHook | 在成功提交表单时要调用的自定义挂接。 |

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
>由于表单提交由自定义JavaScript处理，因此需要通过设置全局变量来显式禁用默认提交 `disableDefaultFormSubmission` 到 `true`.

| 名称 | 描述 |
|--- |--- |
| submitform | 此方法将提交表单，并处理后提交流程。 |
| submitFormPartial | 此方法还将提交表单，但将跳过后提交流程。 例如，如果已配置在提交成功后重定向到成功页面，则在提交部分表单时不会发生该重定向。 |

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
| getFormData | 此方法可用于获取 `formData` 以JSON对象的形式提供。 此对象可以传递到 `submitForm` 用于表单提交。 |

**示例：**

```
let formData = lpRuntime.getFormData();                           // Method to generate formdata
 
lpRuntime.submitForm(formData);
```

## 用例

### 用例1：在提交表单前添加验证

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

### 用例2：部分表单提交

例如，您有一个表单，该页面上有多个复选框。 选中任何复选框时，您希望将此数据保存到后端，而无需等待用户单击提交按钮。

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

### 用例3：自定义分析标记

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

### 用例4：动态表单

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
