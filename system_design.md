# Spoken english to written english conversion system design

### This is a design document that provides a structure on how to implement the above mentioned conversion system

## Architecture:
The architecture consists of three main components. 
### 1. Rules
This contains all the rules for conversion. For eg. "single"--> "1". The rules are maintained using a simple dictionary format.
Hence, new rules can be incrementally added without affecting the previous rules.

### 2. Checks
This component performs all the checks. For eg. we can add a constrain check if the given spoken paragraph has commas, full stops at proper places.
Each check is implemented as a separate function. Hence, new checks can be added incrementally.

### 3. Conversion 
This component uses the other components(as imports) to make the actual conversion. This simply calls the rules(from dictionary to perform conversions for each words and it's surrounding words) and checks(each as a function).

Finally, the main file(main.py) creates an object by instantiating a class of Conversion to take the text as input and show the converted output.


Such as modular design allows for incremental improvements without affecting the previous functionalities.



