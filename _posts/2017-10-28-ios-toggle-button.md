---
layout: post
title: Adding Maya iOS Style Toggle Button on repo
---

Link to repo:
<https://github.com/sartikadelly/ios-togglebutton-for-maya>

Here's a class for making iOS Style toggle button for Maya (2014 and beyond) using Python.
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
<table>
  <thead>
    <tr>
      <th>Type</th>
      <th>Flag</th>
      <th>Description</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>QWidget</td>
      <td>parent</td>
      <td>Parent widget</td>
    </tr>
    <tr>
      <td>int</td>
      <td>width</td>
      <td>Width, default to (height * 2) if not provided</td>
    </tr>
    <tr>
      <td>int</td>
      <td>height</td>
      <td>Height, default to (width * 0.5) if not provided.<br>Default to 32 if both *width & height is not provided*.</td>
    </tr>
    <tr>
      <td>QColor</td>
      <td>colorSwitch</td>
      <td>Switch color.</td>
    </tr>
    <tr>
      <td>QColor</td>
      <td>colorActive</td>
      <td>Background color when Toggle Button is active.</td>
    </tr>    
    <tr>
      <td>QColor</td>
      <td>colorInctive</td>
      <td>Background color when Toggle Button is inactive.</td>
    </tr>      
    <tr>
      <td>bool</td>
      <td>roundedCorner</td>
      <td>Rounded / Square corner style.</td>
    </tr>     
  </tbody>
</table>  

### Properties
<table>
  <thead>
    <tr>
      <th>Type</th>
      <th>Name</th>
      <th>Description</th>
    </tr>
  </thead>  
    <tr>
      <td>bool</td>
      <td>state</td>
      <td>Toggle button state</td>
    </tr>   
</table>  

## Example Usage
```python
import toggle_button

# Default toggle button with 32 height, and blue color as the active color
widget = toggle_button.ToggleButton()
widget.show()
```
![](https://raw.githubusercontent.com/sartikadelly/ios-togglebutton-for-maya/master/screenshots/toggle_example_01.png)

```python
import toggle_button
widget = toggle_button.ToggleButton(width=100, colorActive=toggle_button.RED)
widget.show()
```
![](https://raw.githubusercontent.com/sartikadelly/ios-togglebutton-for-maya/master/screenshots/toggle_example_02.png)

```python
import toggle_button
widget = toggle_button.ToggleButton(height=20, colorActive=toggle_button.QtGui.QColor('#8BC34A'),
  colorInactive=toggle_button.QtGui.QColor('#FF9800'))
widget.show()
```
<img src="https://raw.githubusercontent.com/sartikadelly/ios-togglebutton-for-maya/master/screenshots/toggle_example_03.png">

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
<img src="https://raw.githubusercontent.com/sartikadelly/ios-togglebutton-for-maya/master/screenshots/toggle_example_04.png">

Link to repo:
<https://github.com/sartikadelly/ios-togglebutton-for-maya>


