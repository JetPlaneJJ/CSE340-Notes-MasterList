# AS4 - Color Picker Hints

## Application Model Management
1. You should update the text field with current color as text: 
	- update for starting color!!!!!!!! do not forget!!!!!
	- correct string format (color hexcode) --> we give a method to you for this
2. Remember to update the color square thingy for starting color too
	- you should invoke something... it's in the TODO comments

## App Resiliency
1. need to update background + text when restoring from bundle --> very important!
	- will dock points if you don't do this correctly
2. restore colorpicker view state from bundle after restart
	- remember to use setColor again when restoring the state

## Views
1. You MUST redraw everytime setColor is called, this is a huge hint for that one TODO comment
2. The user may touch anywhere INSIDE the rainbow ring and it would still be considered State.INSIDE





