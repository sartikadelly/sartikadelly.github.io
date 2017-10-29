---
layout: post
title: Adding Maya iOS Style Toggle Button on repo
---

Here's a class for making an iOS Style toggle button in Maya (2014 and beyond) using python.
It's fully customizeable too.

## Class
Inherited from *QtWidgets.QWidget*
```python
class ToggleButton(QtWidgets.QWidget)

class ToggleButton(parent=None,
                   width=None, height=None,
                   colorSwitch=WHITE,
                   colorActive=BLUE_LIGHT,
                   colorInactive=GRAY,
                   roundedCorner = True)
```                 

### Parameters
Type | Flag | Description
--- | --- | ---
QWidget | parent | Parent widget
int | width | Width, default to (height * 2) if not provided
int | height | Height, default to (width * 0.5) if not provided.<br>Default to 32 if both *width & height is not provided*.
QColor | colorSwitch | Switch color.
QColor | colorActive | Background color when Toggle Button is active.
QColor | colorInctive | Background color when Toggle Button is inactive.
bool | roundedCorner | Rounded / Square corner style.

### Properties
Type | Name | Description
--- | --- | ---
bool | state | Toggle button state

## Example Usage
```python
import toggle_button

# Default toggle button with 32 height, and blue color as the active color
widget = toggle_button.ToggleButton()
widget.show()
```
![](https://github.com/sartikadelly/ios-togglebutton-for-maya/blob/master/screenshots/toggle_example_01.png)

```python
import toggle_button
widget = toggle_button.ToggleButton(width=100, colorActive=toggle_button.RED)
widget.show()
```
![](https://github.com/sartikadelly/ios-togglebutton-for-maya/blob/master/screenshots/toggle_example_02.png)

```python
import toggle_button
widget = toggle_button.ToggleButton(height=20, colorActive=toggle_button.QtGui.QColor('#8BC34A'), 
                                    colorInactive=toggle_button.QtGui.QColor('#FF9800'))
widget.show()
```
<img src="https://github.com/sartikadelly/ios-togglebutton-for-maya/blob/master/screenshots/toggle_example_03.png">

```python
import toggle_button
# A Square Toggle Button with custom size & colors
widget = toggle_button.ToggleButton(width=100, height=40,
  colorActive=toggle_button.QtGui.QColor(149,117,205),
  colorInactive=toggle_button.QtGui.QColor(77,182,172),
  colorSwitch=toggle_button.QtGui.QColor(240,244,195),
  roundedCorner=False)
widget.show()
```
![alt text](https://github.com/sartikadelly/ios-togglebutton-for-maya/blob/master/screenshots/toggle_example_04.png "Toggle Button Example 04")



