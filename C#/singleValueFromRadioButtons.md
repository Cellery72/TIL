# Obtaining Single Value From Multiple Radio Buttons

Assuming you have all your Radio Buttons on a single Panel or other similar Control, it's easy enough to use LINQ to obtain a single value (representing the checked button) from multiple Buttons.

A single line can be implemented as such to create a new `var` containing a reference to the Checked Button.
```C#
var checkedButton = container.Controls.OfType<RadioButton>().FirstOrDefault(r=>r.Checked);
```
**Note:** `container` is the name of the control that contains your buttons, i.e. Panel, GroupBox or whatever else.
