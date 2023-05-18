
# Plates

> Named after the word *tem**plate***.

## Features

- Template instantiation
- Template data model classes
- Multiple pages in one file


**Templates**

```html
<!-- Template Definition -->
<div hidden data-template="example">
    ...
</div>

<!-- Template Instantiation -->
<div data-instance="example"></div>

<!-- Template Data Model "Brain" -->
<div hidden data-template="example" data-model="Example">
    <script>
        class Example extends Model {
            init(variables) {
                // Use `variables` to initialize inner HTML elements
            }
        }
    </script>
    ...
</div>

<!-- Template Using CSS Class (hidden takes no effect when used with class) -->
<div hidden data-template="example" class="some-css-class" style="display: none">
    <!-- Now the template acts exactly like a CSS class when instantiated -->
    ...
</div>

<!-- Template Using CSS Class With Data Model -->
<div hidden data-template="example" data-model="Example" class="some-css-class" style="display: none">
    <script>
        class Example extends Model {
            init(variables) {
                // Use `variables` to initialize inner HTML elements
            }
        }
    </script>
    ...
</div>
```

**Pages**

```html
<!-- `main` is the default page shown at page load -->
<div hidden data-page="main">
    ...
</div>
```

To switch pages at any time:

```javascript
switch_page("<page name (what is put in data-page)>")
```
