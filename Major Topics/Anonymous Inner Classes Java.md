# Anonymous Inner Classes
- In Java, Anonymous Inner Classes are inner classes (or a non-static class that’s nested inside another class)
- Anonymous classes don’t have a name and are often used to make an instance of an object that has slightly different methods of another class or interface. This way, you don’t have to actually make a subclass of a class.
- You’re going to see this type of class in some of our homework when implementing something called “listeners”

## Looks something like this:
```java
public class ExActivity extends AppCompatActivity {
	private View.OnClickListener mClickListener = new View.OnClickListener() {
		public void onClick(View v) {
			if (mButton!=v) {
				// some code here
				return;
			}
		}
	};
	
}
```
