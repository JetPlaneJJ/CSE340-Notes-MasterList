# Common topic misassumptions of CSE 340 Students

1. Developer Role differences:
- Component Dev = makes cool new *small* things like LineView which is reusable by other devs
- Library Extender = makes (usually) *GROUPS of components and more complicated things* than comp. dev. Makes new input types, layouts, styling.
- Architecture Extender = uses *toolkit to create funky innovative new stuff* like custom animations

2. Drawing THAT circle:
- Quiz question that keeps annoying you: "Plz create new CircleView. Add the circle with center at (100,100) with a radius of 10. In onDraw(), you call canvas.drawCircle(...) what should you write for cx cy?"
	- (cx,cy) = (10,10). Why? When you're inside the CircleView class, you only know everything w/in bounding box of the view, not the whole canvas. cx cy represents the center of the circle. If the top left of bounding box = (0,0) then you should put the circle at (10,10) so it doesn't get cut off :L
- Another similar questions but be careful of wording! "Consider a circle at 100,100 (relative to PARENT now), radius = 10. What are x,y,width,height for bounding box in parent coordinates?
	- (100,100,20,20). Right now this question wants you to consider the circle RELATIVE TO PARENT!!! width and height are just the circle diameter (radius*2)

3. MV Controller
	- View (ex: digital doorbell)
	- Controller (ex: software/functionality that knows current state, like electrical circuit that is completed when you press bell)
	- Model (ex: representations of the bell, maybe like bellState = RINGRING!!!)

4. Picking 
	- PICKING = **Post-ORDER!!!!**
	- Capture = go through picked list. Is rarely used by comp devs. 
		- In charge of saying "HELLO VIEW, WILL YOU CONSUME THIS EVENT???"
	- Bubbling = reverse order, is the default order for devs
	- See MVC slides, also in: https://github.com/JetPlaneJJ/CSE340-Notes-MasterList/blob/master/Major%20Topics/Event%20Dispatch.pdf

5. Event Records
	- What (Event type --> Key PUSHED)
	- Where (Event target --> CircleView)
	- When (timestamp)
	- Value (which key, coordinates etc --> mouse at 10,10)
	- Context (MODIFIERS --> SHIFT, CTRL, ALT...etc)
	- See Event Records slides: https://github.com/JetPlaneJJ/CSE340-Notes-MasterList/blob/master/Major%20Topics/Model%20View%20Controllers-Events.pdf


