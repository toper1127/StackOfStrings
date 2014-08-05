StackOfStrings
==============
class StackOfStrings {
	private final int SIZE_LIMIT= 10;
	private int counter = 0;
	private String[] names = new String[this.SIZE_LIMIT];

	public StackOfStrings() {
		System.out.println("Created a Stack Data Structure");
	}

	/**
	*Insert an item in the stack
	*/
	public void push(String name){
		if(this.isFull()) {
			System.out.println("The stack is already full.");
		} else {
		this.names[this.counter] = name;
		this.counter++;
		}
	}

	/**
	*Removes an item from the stack
	*/
	public String pop() {
		if (this.isEmpty()) {
			System.out.println("Empty Stack");
			return "EMPTY";
		} else {
			String name = this.names[this.counter - 1];
			this.names[this.counter - 1] = "";
			this.counter--;
			return name;
		}
	}
	private boolean isEmpty() {
		if (this.counter == 0) {
			return true;
		} else {
			return false;
		}
	}
	private boolean isFull() {
		if (this.SIZE_LIMIT == (counter + 1)) {
			return true;
		} else {
			return false;
		}
	}

	public void display() {
		System.out.println("Q(-_-Q)Q(-_-Q)Q(-_-Q)Q(-_-Q)");
		System.out.println("(*_*)(*_*)(*_*)(*_*)");
		for (int i = 0; i < this.counter; i++){
			System.out.println(this.names[0]);
		}	
		System.out.println("(^_^)(^_^)(^_^)(^_^)");
	}

	private  int size() {
		return this.counter;
	}
}
======================================================================================================================
class StackOfStringsArrayApp {
	public static void main(String[] args) {
		StackOfStrings stack = new StackOfStrings();
		stack.push("John");
		stack.push("Mike");
		stack.push("Peter");
		stack.push("Orange");
		stack.push("Apple");
		stack.push("English");
		stack.push("Science");
		stack.push("Mathematics");
		stack.push("T.L.E.");
		stack.push("P.E.");

		stack.display();
		System.out.println("Removed " + stack.pop());
		System.out.println("Removed " + stack.pop());
		System.out.println("Removed " + stack.pop());
		System.out.println("Removed " + stack.pop());
		System.out.println("Removed " + stack.pop());  
		stack.display();
	}
}
