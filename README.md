### Initialization
How to initialize Froala from a page on using TinyMCE.

#### Remove TinyMCE Script
To replace TinyMCE with Froala, you must first remove TinyMCE Script.

```html
<!-- TinyMCE Script -->
<script src='https://cloud.tinymce.com/stable/tinymce.min.js'></script>
```

#### Include Froala Script.
Include the script package needed to use Froala.
Add the css code inside the head.
```html
<!-- Include external CSS. -->
<link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.4.0/css/font-awesome.min.css" rel="stylesheet" type="text/css" />
<link href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.25.0/codemirror.min.css" rel="stylesheet" type="text/css">
 
<!-- Include Editor style. -->
<link href="https://cdn.jsdelivr.net/npm/froala-editor@2.9.1/css/froala_editor.pkgd.min.css" rel="stylesheet" type="text/css" />
<link href="https://cdn.jsdelivr.net/npm/froala-editor@2.9.1/css/froala_style.min.css" rel="stylesheet" type="text/css" />
```

Add the js code to the bottom of the body.
```html
<!-- Include external JS libs. -->
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/jquery/1.11.0/jquery.min.js"></script>
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.25.0/codemirror.min.js"></script>
<script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.25.0/mode/xml/xml.min.js"></script>

<!-- Include Editor JS files. -->
<script type="text/javascript" src="https://cdn.jsdelivr.net/npm/froala-editor@2.9.1/js/froala_editor.pkgd.min.js"></script>
```

#### Replace JS code with TinyMCE to Froala.
Remove the TinyMCE code.

```javascript
tinymce.init({
  selector: 'textarea',
  toolbar: ['undo redo | bold italic underline']
});
```

Add the Froala code.
```javascript
$('textarea').froalaEditor({
  toolbarButtons: ['undo', 'redo', '|', 'bold', 'italic', 'underline']
});
```

#### Basic Initialization example
Below is the initialization code changed from TinyMCE to Froala.

```html
<!DOCTYPE html>
<html>
  <head>
    <meta charset="utf-8">

    <!-- Include external CSS. -->
    <link href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/4.4.0/css/font-awesome.min.css" rel="stylesheet" type="text/css" />
    <link href="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.25.0/codemirror.min.css" rel="stylesheet" type="text/css">

    <!-- Include Editor style. -->
    <link href="https://cdn.jsdelivr.net/npm/froala-editor@2.9.1/css/froala_editor.pkgd.min.css" rel="stylesheet" type="text/css" />
    <link href="https://cdn.jsdelivr.net/npm/froala-editor@2.9.1/css/froala_style.min.css" rel="stylesheet" type="text/css" />
  </head>

  <body>
    <!-- Create a tag that we will use as the editable area. -->
    <!-- You can use a div tag as well. -->
    <textarea></textarea>

    <!-- Include external JS libs. -->
    <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/jquery/1.11.0/jquery.min.js"></script>
    <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.25.0/codemirror.min.js"></script>
    <script type="text/javascript" src="https://cdnjs.cloudflare.com/ajax/libs/codemirror/5.25.0/mode/xml/xml.min.js"></script>

    <!-- Include Editor JS files. -->
    <script type="text/javascript" src="https://cdn.jsdelivr.net/npm/froala-editor@2.9.1/js/froala_editor.pkgd.min.js"></script>

    <!-- Initialize the editor. -->
    <script>
      $(function(){
        $('textarea').froalaEditor();
      });
    </script>
  </body>
</html>
```

##### Screen shot
![example00](https://github.com/froala-labs/migrate-from-tinymce/blob/master/images/example00.gif)

### Feature matching from TinyMCE - Froala
We will change the demo introduced in TinyMCE to Froala.

#### Basic Example
This example contains the plugins needed for the most common use cases.

TinyMCE Example
[Live example](https://codepen.io/tinymce/pen/YydQrY)

Froala Example
[Live example (Codepen)](https://codepen.io/romanesque/pen/OaOjBL) [Live example (JSfiddle)](https://jsfiddle.net/romanesque_io/ebLowmk5)

##### Screen shot
![example01](https://github.com/froala-labs/migrate-from-tinymce/blob/master/images/example01.gif)

#### Distraction-free Editor
TinyMCE Distraction-free editor option can be used in Froala.

TinyMCE Example
[Live example](https://codepen.io/tinymce/pen/xzoELd)

Froala Example
[Live example (Codepen)](https://codepen.io/romanesque/pen/PxEQZY) [Live example (JSfiddle)](https://jsfiddle.net/romanesque_io/3zn0qgrm)

##### Screen shot
![example02](https://github.com/froala-labs/migrate-from-tinymce/blob/master/images/example02.gif)

#### Inline Editor
Same as TinyMCE You can use the inline editing function.

TinyMCE Example
[Live example](https://codepen.io/tinymce/pen/bKPBjg)

Froala Example
[Live example (Codepen)](https://codepen.io/romanesque/pen/Oazvbg) [Live example (JSfiddle)](https://jsfiddle.net/romanesque_io/6r32dxbf)

##### Screen shot
![example03](https://github.com/froala-labs/migrate-from-tinymce/blob/master/images/example03.gif)

#### Custom Formats
In Froala, you can use Custom Formats with three functions [Inline Classes](https://www.froala.com/wysiwyg-editor/examples/inline-classes), [Inline Styles](https://www.froala.com/wysiwyg-editor/examples/inline-styles), and [Paragraph Styles](https://www.froala.com/wysiwyg-editor/examples/paragraph-styles).

TinyMCE Example
[Live example](https://codepen.io/tinymce/pen/QjzgRW)

Froala Example
[Live example (Codepen)](https://codepen.io/romanesque/pen/PxaYXV) [Live example (JSfiddle)](https://jsfiddle.net/romanesque_io/L2ozb8qd)

##### Screen shot
![example04](https://github.com/froala-labs/migrate-from-tinymce/blob/master/images/example04.gif)

#### Custom Toolbar Button

TinyMCE Example
[Live example](https://codepen.io/tinymce/pen/wKReOb)

Froala Example
[Live example (Codepen)](https://codepen.io/romanesque/pen/OazZjr) [Live example (JSfiddle)](https://jsfiddle.net/romanesque_io/jq6u2vef)

##### Screen shot
![example05](https://github.com/froala-labs/migrate-from-tinymce/blob/master/images/example05.gif)

#### Custom Toolbar Listbox

TinyMCE Example
[Live example](https://codepen.io/tinymce/pen/JYwJVr)

Froala Example
[Live example (Codepen)](https://codepen.io/romanesque/pen/dQKbGW) [Live example (JSfiddle)](https://jsfiddle.net/romanesque_io/vjpfd31b)

##### Screen shot
![example06](https://github.com/froala-labs/migrate-from-tinymce/blob/master/images/example06.gif)

#### image Tools

Froala offers rich inline tools for image editing.

TinyMCE Example
[Live example](https://codepen.io/tinymce/pen/epbRwB)

Froala Example
[Live example (Codepen)](https://codepen.io/romanesque/pen/MzXWep) [Live example (JSfiddle)](https://jsfiddle.net/romanesque_io/9aLr7kcz)

##### Screen shot
![example07](https://github.com/froala-labs/migrate-from-tinymce/blob/master/images/example07.gif)

#### Local Upload
Froala provides an intuitive UI for uploading local images to the server.

TinyMCE Example
[Live example](https://codepen.io/tinymce/pen/xLPoeV)

Froala Example
[Live example (Codepen)](https://codepen.io/romanesque/pen/KredzM) [Live example (JSfiddle)](https://jsfiddle.net/romanesque_io/hxjpmsve)

##### Screen shot
![example08](https://github.com/froala-labs/migrate-from-tinymce/blob/master/images/example08.gif)

### Use Froala Editor options

How to use options compared to TinyMCE.

#### How to run the code

Froala is based on [jQuery](http://jquery.com). In Froala, you can select a target using the [jQuery selector](https://api.jquery.com/category/selectors).

TinyMCE Code Examples
```javascript
tinymce.init({
  selector: 'textarea'
});
```

Froala Code Examples
```javascript
$('textarea').froalaEditor();
```

#### Work With Plugins
Froala supports a variety of plugins.

TinyMCE Code Example
```javascript
tinymce.init({
  selector: 'textarea',
  plugins : 'image link'
});
```

Froala Code Example
```javascript
$('textarea').froalaEditor({
  pluginsEnabled: ['image', 'link']
});
```

**Note:** By default, all plugins are enabled without using the pluginsEnabled option. 
**Note:** Each plugin requires you to include the corresponding JS and CSS files. Here is the [complete list of plugins](https://www.froala.com/wysiwyg-editor/docs/plugins) and the files required by them.


#### Using the toolbar
Like TinyMCE, the toolbars in Froala are easy to use.

TinyMCE Code Example
```javascript
tinymce.init({
  selector: 'textarea',
  toolbar: [
    'undo redo | styleselect | bold italic | link image',
    'alignleft aligncenter alignright'
  ]
});
```

Froala Code Example
```javascript
$('textarea').froalaEditor({
  toolbarButtons: [
    'undo', 'redo', '|', 'bold', 'italic', '|', 'insertLink', 'insertImage', '-',
    'alignLeft', 'alignCenter', 'alignRight'
  ]
});
```

**Note:** `|` will insert a vertical separator line in the toolbar, and `-` a horizontal one. For more information, see [Toolbar Buttons](https://www.froala.com/wysiwyg-editor/examples/toolbar-buttons).
**Note:** The menubar option is not used by Froala.
**Note:** For more information, see [Options](https://www.froala.com/wysiwyg-editor/docs/options).

### Use Froala Editor methods
How to use methods compared to TinyMCE.

#### Control method with external button
HTML Code Example
```html
<textarea>
  <p>This example illustrates how to clear the text using a button external to the Froala WYSIWYG HTML Editor interface.</p>
</textarea>
<button id="clear-text">Clear</button>
```

TinyMCE Code Example
```javascript
tinymce.init({
  selector: 'textarea',
  init_instance_callback : function(editor) {
    var button = document.getElementById("clear-text");
    button.addEventListener("click", function () {
      editor.setContent('');
      editor.focus();
    });
  }
});
```

Froala Code Example
```javascript
$('textarea').on('froalaEditor.initialized', function (e, editor) {
  editor.events.$on($('body'), 'click', '#clear-text', function () {
    editor.html.set('');
    editor.events.focus();
  });
})
.froalaEditor();
```

#### Replace selection to specified content
HTML Code Example
```html
<textarea>
  <p>This example illustrates how to clear the text using a button external to the Froala WYSIWYG HTML Editor interface.</p>
</textarea>
```

TinyMCE Code Example
```javascript
tinymce.init({
  selector: 'textarea',
  menubar: false,
  plugins: 'code',
  toolbar: 'mybutton code',
  setup: function (editor) {
    editor.addButton('mybutton', {
      text: false,
      icon: 'nonbreaking',
      onclick: function () {
        var blocks = editor.selection.getNode();
        var string = editor.selection.getContent({format:'text'});
 
        if(blocks.nodeName == 'SPAN') {
          editor.insertContent(string);
        } else {
          editor.insertContent('<span style="color: red;">' + string + '</span>');
        }
      }
    });
  }
});
```

Froala Code Example
```javascript
$.FE.DefineIcon('mybutton', {NAME: 'plus'});
$.FE.RegisterCommand('mybutton', {
  title: 'mybutton',
  callback: function () {
    var blocks = this.selection.element();
    var string = this.selection.text();
 
    if(blocks.tagName == 'SPAN') {
      this.html.insert(string);
    } else {
      this.html.insert('<span style="color: red;">' + string + '</span>');
    }
  }
});
 
$('textarea').froalaEditor({
  toolbarButtons: ['mybutton', 'html']
});
```
**Note:** For more information, see [Methods](https://www.froala.com/wysiwyg-editor/docs/methods).

### Use Froala Editor events
How to use events compared to TinyMCE.

#### Click event
TinyMCE Code Example
```javascript
tinymce.init({
  selector: 'textarea',
  init_instance_callback: function (editor) {
    editor.on('click', function (e) {
      console.log('Element clicked:', e.target.nodeName);
    });
  }
});
```

Froala Code Example
```javascript
$('textarea').on('froalaEditor.click', function (e, editor, clickEvent) {
  console.log('Element clicked:', e.target.nodeName);
})
.froalaEditor();
```

#### Exec Command events
TinyMCE Code Example
```javascript
tinymce.init({
  selector: 'textarea',
  init_instance_callback: function (editor) {
    editor.on('ExecCommand', function (e) {
      if (e.command === 'mceToggleFormat' && e.value === 'H1') {
        console.log('mceToggleFormat was executed')
      }
    });
  }
});
```

TinyMCE Code Example
```javascript
$('textarea').on('froalaEditor.commands.after', function (e, editor, cmd, param1, param2) {
  if(cmd === 'paragraphFormat' && param1 === 'H1') {
    console.log('paragraphFormat was executed');
  }
})
.froalaEditor();
```
**Note:** Refer to Events for configurable [Events](https://www.froala.com/wysiwyg-editor/docs/events).


### Froala Editor theming

Froala theme function is the same as TinyMCE skin function. You can also create your own theme and customize the rich text editor's interface the way you want using the [customizer](https://www.froala.com/wysiwyg-editor/customize).

TinyMCE Code Example
```javascript
tinymce.init({
  selector: 'textarea'
  skin_url: '/tinymce/skins/lightgray',
  skin: 'lightgray'
});
```

Froala Code Example
```html
<link href="../css/themes/gray.min.css" rel="stylesheet" type="text/css" />
```
```javascript
$('textarea').froalaEditor({
  theme: 'gray' // Set gray theme name.
})
```
**Note:** You must include a CSS theme file for theme use.