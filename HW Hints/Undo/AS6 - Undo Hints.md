Undo Assignment general tips and corrections from Winter 2020 Spec

1. Color Picker: is always red at start of app. Thumb should always reflect current color.
	- DO NOT PASS COLORPICKER INSIDE TOGGLE MENU!!!
	- there is already an AbstractColorPickerView in the given files
	- color picker can be placed anywhere as long as the whole thing is inside the screen :)
	- color picker should CLOSE if user presses inside the wheel and releases anywhere
	- all visible buttons should be grayed out/not usable immediately after clicking color_fab (leave color fab enabled)
	- after clicking color_fab and your picker shows up, then user clicks totally outside wheel, it is ok to close the window or not close it, doesn't matter.
2. on[Something]Selected methods:
	- must call addCollapsableMenu(R.layout.whatever... this::on[Something]Selected) in order to be able to execute code inside the on[Something]Selected method
		- do this even for the color_fab even tho it's no longer a "collapsable menu", most important part is "this::on[Something]Selected"

3. Part 4 ideas: clearing whole screen, dashed/dotted lines when drawing, emoji drawn along path when drawing, fill entire canvas with color...etc
	- Suggestion: use the existing undo and redo classes 

4. Reflection:
- be sure to group your data based on "like" issues, not based on who sent them to you.
- include specific steps you would take to solve the issues you found with the default Undo app.
- can suggest new heuristics for the "how well do the heuristics fit"?


Hints from Lecture Winter 2020: 
- Undo-go to prev action
- RrvDrawActivity: Contains ALL buttons
- Rvdrawingact: Implements a class that allows you to undo the redo, allows u to commit actions, calls
- AbstractDrActvity: No history, adding menus
- DrawingView: Keeps track of stroke views, has onTouchEvent with Pps state machine
Possible to implement action: Emojis, dotted lines... THERE IS A WORKSHEET, SEE WEBSITE FOR PDF DOWNLOAD!!!

Hints from Lecture Spring 2020 (5/22):
- Review: all systems have at least 3 models (Design/what you thought the system should do, System Image: your implementation, User Model/How the user thinks the system works)
