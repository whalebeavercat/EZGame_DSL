# User Studies Check-in
## Study 1
### User Study Methodology
We conducted three user studies with users who wanted to learn to code video games but wanted a simple language to learn first.
These users matched the scope of our DSL as that is what we are setting out to create.
We started off our user studies by introducing our project purpose to receive opinions on our project scope.
The next part of the user study consisted of explaining the DSL syntax and language functionality to receive input on our language design.
This is followed up with code examples to test readability and simplicity.
We ended off our user studies by asking for any final questions or feedback.

### User Study Feedback
We received a lot of good feedback while conducting our user studies. Our users all believed that our DSL could help them learn how to code simple video games.
They appreciated that our language more closely resembled actual programming languages than other tools used to help young people learn CS do.
They all agree that our DSL is important and will be useful.

While explaining the syntax and functionality of our language, we got a lot of good feedback and questions. The feedback is as follows:

1. How will indentation work? How will you be able to tell what statements belong to what? We got feedback that someone might not think to indent lines that belong to a certain clause/loop/function.
2. We got feedback that we should write more advanced examples that show the capability of our language. We used a lot of simple examples in our user studies and we got feedback that showing a fleshed out example will help show capability more, while still keeping the intended audience in mind.
3. The cloning attribute is confusing. Our users were confused whether the entity would be cloned in place or cloned to a random position.
4. We got feedback that the double equals for conditionals (==) is confusing. They did not understand why == is needed and suggested to keep it simple by using words like "equals" instead, similar to what we do for "and" and "or".
5. We got the suggestion to change the end conditions to use conditional statements as well, instead of using "one of:" and "all of:". The users were confused on how our current design worked for win conditions.

### User Study Response
All the feedback we received was very useful and will be taken into account. The following is our responses for the feedback above:

1. We will make it more clear when we describe our language syntax how indentation should work. As well, we will include detailed error messages if indentation is off. Our ANTLR should be updated to be clear what indentation is needed too.
2. We are working on writing more advanced examples
3. We need to discuss how to best handle the cloning attribute. One idea is to directly specify where it clones to. Another idea is to move the cloning functionality to the behavior section.
4. We will change to using words instead of == to keep it easy to learn.
5. We will rework our end conditions to use conditionals. One idea is to have a "Win:" and "Lose:" sections that is followed by a conditional.

### User Study Reflection
Overall, we think our user studies went well. We gained a lot of valuable feedback. We think our general structure for the user study was good.
One improvement for our user study is to have more examples for our language and have a better plan for what specific areas we are looking for feedback in.
We can add those improvements to our final user studies.

# Study 2
### User Study Methodology
Similar to the first user study, we conducted three user studies with users who wanted to learn to code video games but wanted a simple language to learn first.
These users matched the scope of our DSL as that is what we are setting out to create.
We started off our user studies by introducing our project purpose to receive opinions on our project scope.
The next part of the user study consisted of explaining the DSL syntax and language functionality to receive input on our language design.
This is followed up with code examples to test readability and simplicity.
We then showed the prototype for our game at the point of the user study to get feedback on our development progress.
We ended off our user studies by asking for any final questions or feedback.

### User Study Feedback
This user study was very productive for polishing our DSL. Like the last user study, we received a lot of quality feedback.
Our users once again agreed that our DSL effectively implemented its use case.
They appreciated that our language more closely resembled actual programming languages than other tools used to help young people learn CS do.
They all agree that our DSL is important and will be useful.

While conducting the user studies, we got a lot of good feedback and questions. The feedback is as follows:

1. Users were confused when forever loops and unless statements ended and suggested we made that more clear.
2. At the time of our user studies, our prototype has the game layout as just colored rectangles. Users suggested making the resulting game look better.
3. Users were confused with variables in some cases. In function definitions, they were confused that parameters created variables. Similarly, they were confused about how to change the value of variables.
4. Similar to the variable setting issue, users were confused with function calls and would like it to be more clear.

### User Study Response
All the feedback we received was very useful and will be taken into account. The following is our responses for the feedback above:

1. To make our language more clear for which blocks of code belong together, we added braces to our language.
2. We further worked on the aesthetics of the final game and added different sprite designs to make the game look more appealing.
3. To make it more clear when you define a new variable for functions, we added "var" in front of the function name. Similarly, we added "set" when mutating a variable to make it more clear.
4. Similar to the change for variables, we added "call" in front of function calls to make it more clear that a function is being called.

### User Study Reflection
Both the first and second user studies were extremely helpful in good language design. We gained a lot of valuable feedback. We think our general structure for the user study was good again.