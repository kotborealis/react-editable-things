# React Editable Things
An assortment of common HTML form elements, editable in-line the React way.

Try out [the demo](http://kotborealis.github.io/react-editable-things/) and see what it looks like.

# Installation
`yarn add react-editable-things`

# Usage
```javascript
import { RIEToggle, RIEInput, RIETextArea, RIENumber, RIETags, RIESelect } from 'react-editable-things'
```
See /demo/src/demo.js for examples.

## Common props

### Required
* **value**: initial prop value
* **propName**: name of the prop to return to the _change_ function
* **change**: function which will receive a plain object with a single key, provided in _propName_

### Optional
* **validate**: validator function, returning a boolean or promise which resolves a boolean. 
* **shouldBlockWhileLoading**: disables editing until a new value is confirmed by parent
* **classLoading**: CSS class name to use when loading
* **classEditing**: CSS class name to apply while in editing mode
* **classInvalid**: CSS class name to apply when _doValidatoon_ returned false
* **className**: CSS base class
* **editProps**: Additional props for the editing component. This allows you to, for example, specify a maxLength attribute to control the maximum number of characters in the textarea, or add `style`.
* **defaultProps**: Additional props for idle component.

### Component-specific props

#### RIENumber
* **format**: custom formatting function, returns formatted string

#### RIETextArea
* **rows**: rows property on textarea tag while editing
* **cols**: rows property on textarea tag while editing

#### RIESelect
* **options**: an array of objects containing values and text for [select options](http://www.w3schools.com/tags/tag_option.asp)
```javascript
<RIESelect ... options={[
  {id: "1", text: "one"},
  {id: "2", text: "two"},
  {id: "3", text: "three"}
]} />
```