# Debugging

TheBankStatement

>Found a bug that was not allowing my Checking Account's print method to display.

>I corrected it by using the debugger to locate where the error was occuring. After narrowing it down to the method and class, I created a breakpoint to focus the dubber on specific variables expected to display. The expected variable did show in the correctly when hovered over, however, it did not print. This allowed attention to other syntax within the parenthesis, specifically the formatter used to manipulate variables. Ultimately, I discovered I had been using the formatter for decimals and not integers. Once corrected, the checking account's print method displayed and the bug was fixed.

Before:
// Print Method
			public String print() {
		    	 String str = super.print();
		    	 str += String.format("%8.2f", this.getChkNbr());
		    	 return str;
			}
After:
// Print Method
			public String print() {
		    	 String str = super.print();
		    	 str += String.format("%4d", this.getChkNbr());
		    	 return str;
			}
