Multiple Range Input
===============

Multiple Range Input is a jQuery plugin (based on Garrett Grimm's [Multiple Range Interface](https://github.com/grimmdude/multiple-range-interface)) that creates an input that allows the user to set multiple range based values.  
It's useful for interacting with timeline based data like videos, slideshows, music, etc.

##Install
	bower install multiple-range-input


##Usage
HTML:
```html
<div id="multiple-range-input"></div>
```

JS:
```js
$('#multiple-range-input').multipleRangeInput({
	onChange: function() {
		// Do stuff when the input values change
	},
	onSectionClick: function() {
		// Do stuff when a section is clicked
	},
	onSectionAdded: function(item) {
		// Do stuff when a section is added
	},
});
```

##Methods
After the interface is initialized methods can be called on it like so:

```js
$('#multiple-range-input').multipleRangeInterface('methodName', parameters);
```
###addSection
Adds a new range section.
```js
$('#multiple-range-input').multipleRangeInterface('addSection', {color: '#DDDDDD'});
```

Adds a new range section with a task.
```js
$('#multiple-range-input').multipleRangeInterface('addSection', {type: 'task'});
```
###deleteSection
Deletes a range section by id.
```js
$('#multiple-range-input').multipleRangeInterface('deleteSection', id);
```
###getValues
Gets values for all range sections.
```js
$('#multiple-range-input').multipleRangeInterface('getValues');
```
###setValues
Sets values for given section id.  The `id` field must be present in the parameters object. You can set a `readOnly` optional parameter or a `title` for a task
```js
$('#multiple-range-input').multipleRangeInterface('setValues' {id: 1, start: 20, stop: 44, readOnly: true, title });
```
###selectSection
Selects a range section by id.
```js
$('#multiple-range-input').multipleRangeInterface('selectSection', 2);
```
###getSelectedSection
Returns the data for the currently selected section.
```js
$('#multiple-range-input').multipleRangeInterface('getSelectedSection');
```

##Browser Support
The following browsers are what I've tested:
* Chrome
* Firefox
* Opera

If you find the plugin works in other browsers please let me know and I'll add it to the list.  Likewise if it doesn't work in certain browsers please let me know.
