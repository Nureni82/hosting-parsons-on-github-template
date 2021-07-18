---
title: Printing Even or Odd Number
---

## Purpose:

 <p>The purpose of this exercise is to practice the program flow and the sequence of statement executions using the conditional statements. For testing</p>


## Directions :

<div style="text-align: justify">
    <p>Task: The following program should print out “x is even” if the remainder of x divided by 2 is 0 and “x is odd” otherwise, but the code is mixed up. Drag the blocks from the left and place them in the correct order on the right. Click on Get Feedback to see if you are right.</p>
 
 <div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "public class EvenOrOdd{\n" +
    "	public static void main(String[ ] args) {\n" +
    "    	int num = 51;\n" +
    "    	if(x % 2 == 0) {\n" +
    "        	System.out.println(“x is even”);\n" +
    "        }\n" +
    "        else {\n" +
    "        	System.out.println(“x is odd”);\n" +
    "        }\n" +
    "   }\n" +
    "}\n" +
    "        \n" +
    "        \n" +
    "        ";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
