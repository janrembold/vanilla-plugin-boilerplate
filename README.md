# Vanilla Plugin Boilerplate
A plain UMD vanilla javascript plugin boilerplate with optional jQuery initialization for the sake of convenience.
This boilerplate is useful for small or fast scripts that don't necessarily need jQuery.

## Usage
Change `pluginName` variable to your desired plugin name and include the plugin.

Initialize the plugin to a single html element with plain vanilla javascript.

```javascript
var boilerplate = new Boilerplate(document.getElementById('demo'), {
    someDefaultOption: 'Plugin was loaded vanilla style!'
});

boilerplate.doSomething();
```

Or append the plugin to a collection of elements with a jQuery selector. 
The plugin object will be attached to each elements data attribute. 
The data attributes name is `plugin_` prefixed to the given `pluginName`.
 
```javascript
$('.demo').Boilerplate({
    someDefaultOption: 'Plugin was loaded jQuery style!'
});

$('.demo').data('plugin_Boilerplate').doSomething();
```

## License
* Author: Jan Rembold
* License: MIT