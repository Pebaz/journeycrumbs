
1. Templates must be named `template-`
2. Pages must be named `page-`
3. Everywhere a template should be instantiated should be: `<div name="instance-TEMPLATE-NAME"></div>`

To define a template with a custom data model with functions that act upon the
element at instantiation time:

```html
<!--
To instance this, do:
    <div name="instance-foo"></div>
-->
<div hidden id="template-foo" data-model="TemplateFoo">
    <script>
        class TemplateFoo {
            init(self) {
                console.log('init!');
                self.innerText = Math.random();
            }
        }
    </script>
    Contents of this template ...
</div>
```
