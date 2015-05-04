ui-select add-on
=================

This ui-select add-on uses as the name implies the ui-select plugin to provide a select dropdown interface. [ui-select](https://github.com/angular-ui/ui-select) is used.

Installation
------------
The editor is an add-on to the Bootstrap decorator. To use it, just include
`angular-schema-form-uiselect.min.js`.

You'll need to include a few additional libraries to use uiselect:

1. [angular-underscore](https://github.com/floydsoft/angular-underscore)
2. [ui.select](https://github.com/angular-ui/ui-select)
3. [angular-translate](https://github.com/angular-translate/angular-translate)
4. Make sure to load the above libraries in your module
```javascript
angular.module('yourModule', [..., 'angular-underscore', 'ui.select', 'pascalprecht.translate', ...]);
```

Easiest way is to install is with bower, this will also include dependencies:
```bash
$ bower install stephenbaidu/angular-schema-form-uiselect
```

Usage
-----
The add-on adds a new form type, `uiselect`, and a new default
mapping.

| Schema             |   Default Form type  |
|:-------------------|:------------:|
| "type": "string" and "format": "uiselect"   |   uiselect   |
| "type": "array" and "format": "uiselect"   |   uimultiselect   |

### Schema Definintion
```javascript
person_list: {
  title: 'Person List',
  type: 'string',
  format: 'uiselect',
  items: [
    { value: '1', label: 'Person 1' },
    { value: '2', label: 'Person 2' }
  ]
},
persons_list: {
  title: 'Persons List',
  type: 'array',
  format: 'uiselect',
  items: [
    { value: '1', label: 'Person 1' },
    { value: '2', label: 'Person 2' },
    { value: '3', label: 'Person 3' }
  ]
}
```

Options
-------
The add-on provides only one option to specify a class for select
```javascript
{
  key: 'person_list',
  placeholder: 'Some Place Holder', //default will translate placeholder.select
  options: {
    uiClass: 'short_select'
  }
}
```
