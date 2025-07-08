## Project 1 Check-in 1

Our DSL focusses on simplifying language for 2D top-down video games and tilemap design. The DSL enables the user to create video game without precise knowledge of game design, while also providing freedom to customize their game. This involves map creations, designing player/enemy behaviour, and defining collision scripts. User should be able to define enemy, platform, and player type, as well as entity components such as health, size, and hitbox. We can also specify speed and damage from a simplified collision script. 
We will provide rich features that will simplify loops and procedures and make them specific for game design. As a result, there is no need to design systems. 

### Rich Features:
1. Forever loops which can be broken out of based on mutable variables.
      ``` forever_loop_instruction: 'forever' condition_statement? ':' loop_code+; ```
2. Complex functions which support recursion and parameters
      ``` function_defintion: 'define' 'function' function_name '(' (variable_name (',' variable_name)*)? ')' ':' function_code+; ```
3. Proper mutable variables
      ``` variable_definition: 'var' variable_name '=' value_statement;```

An example of the DSL is given here:
```
ARENA:
  size = 100

ELEMENTS:
  define player mario:
    start = 0,0
    health = 10
    size = 2
    direction = right
  define enemy goomba:
    start = 1,1
    health = 8
    size = 1
    damage = 2
    direction = up
  define obstacle box:
    start = 2,2
    size = 2
    direction = down
  define collectable coin:
    start = random
    size = 1
    clone = 10
    direction = left

BEHAVIOUR:
  define function move_left_right(yeehaw, entity):
    forever unless (yeehaw > 10):
      repeat 100 times:
        move yeehaw
      face left
      wait 1 sec
      repeat 10 sec:
        move 1
      turn right
      wait 1 sec
      unless ((on pos 1,1) and (not (on pos entity))):
       yeehaw = yeehaw + 2
  goomba:
    var yeehaw = move_left_right
    move_left_right(yeehaw, goomba)
  coin:
    forever:
      wait 5 sec
      move random

END CRITERIA:
  one of:
    mario health == 0
    coin amount == 10

```

## Notes from the TA meeting
* The TA gave us advice about the complexity of our rich features. He suggested that features should not be an simple such that it can not be unrolled as JSON. As well, he suggested that a DSL should be simplified such that users have a reason to use it rather than using another programming language.
* The TA suggested that we should also make the DSL more complex such that it isn't as dependent on the backend. Although, it shouldn't be as complex such that the DSL isn't domain specific.
* Following his advice, we adjusted the for-loops in our program such that it simplified the fundamental steps in game design. For example, the forever loop is extremely helpful in game design. Otherwise, we would need to create individual systems and use an update method/loop for behavior. Adding mutable variables is helpful in game programming to simplify code.


## Notes from the Check-in 2
* TA gave us the advice that we could trim down out one of our rich features. After discussion, our group agreed to cut out the recursion feature in favour of keeping functions.
* Our first goal will be to tackle the syntax of the AST tree. To do this, our group will first come together, develop, and agree upon the design for the syntax. Once this is complete, we split tasks based on everyone's strengths.
* As suggested by the TA, we will try to create some prototypes and diagrams for our DSL.
* As for possible design changes, the TA suggested to contact them via email first and then reflect changes in the proposal file.

## Notes from the Check-in 3
* Before the meeting, the TA looked over our proposal and approved our rich features. Mayant said our rich features are strong and our proposal shows many good examples for our DSL.
* The TA suggested that we should simplify the boolean operators "all of" and "one of" for the end condition, saying that our group could have the same results through regular "and" and "or" conditions. 
* Then, we discussed about the user study. He suggested that we ask 2 or more people, who are new programmers, to use our DSL and provide feedback. For example, the forever-loops using "unless" and "if" might cause confusion for the user. He also told us about the format of the user study, structuring it as a Q&A, then summarizing the feedback.
* Later, we talked about the timeline for the project and how to start. We suggested tackling the AST first and maybe a game prototype. It is imperative that we get the AST right, since it is neccessary for the parser and evaluator team to work concurrently and prevent big changes down the road. We plan to contact the TA for feedback on our AST once developed.

## Notes from the Check-in 4
* Status of Implementation:
  * The team has started implementation. We currently have set up a Jira project to track assigned work and progress.
  * From the last check-in we have added some starter files (tinyHTML) as a template. (This was approved via Piazza question 33)
  * We have also finalized the structure and details of our implementation
  * We have also created a mock-up of the game's GUI using Java Swing
  * We will begin testing as we continue developing the project.
* Plans for final user study:
  * We are looking to get feedback after considering the changes suggested during our first user study.
  * Specifically, we are considering changing from indentation to curly braces to describe encapsulation.
* Planned timeline for the remaining days:
  * In the next few days, we hope to continue implementing our project. We will create the AST data structure and finalize the Lexer and Parser ANTLR implementations.
  * We hope to also begin implementing parts of the Evaluator that are not affected by the development of other modules.

## Notes from the Check-in 5
* We went over our plans during the TA check-in. Our team has good progress on the lexer and parser, but we still need to refine it. We also designed our AST structure and started implementing it in Java. We will first give a head start to the lexer/parser and AST because we believe that there will be a lot of structural changes to the AST necessary when developing the Evaluator. The TA also agreed with our plan.
* Some of the syntax for our DSL has been changed for better clarity and from our feedback in the user study. For example, we decided to use curly braces instead of indentation.
* The Evaluator will be the most challenging task and will require all our members to work on it. We plan to coordinate and implement it during the reading break.
* Since we are still working on the lexer/parser, our team has not done our final user study. We plan to conduct this user study after having the first working version.
* Our team plans to make the final video before the deadline, once we have our final version.
* Our group plans to contact the TA over the reading break if we have further questions.