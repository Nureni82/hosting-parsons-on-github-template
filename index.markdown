---
title: Code Tracing Review
---

## Directions: 
<div style="text-align: justify"> 
The following has the correct code to ‘swap’ the values in x and y (so that x ends up with y’s initial value and y ends up with x’s initial value), but the code is mixed up and contains one extra block which is not needed in a correct solution. 
Drag the needed blocks from the top into the correct order at the bottom. 
Check your solution by clicking on the Get Feedback button. Your can click Reset Problem button to reshuffle the code blocks. 
You will be told if any of the blocks are in the wrong order. </div>



<div id="1-sortableTrash" class="sortable-code"></div> 
<div id="1-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="1-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="1-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "public class CodeTracing{\n" +
    "    public static void main(String[] args){\n" +
    "        int x = 2;\n" +
    "        int y = 3;\n" +
    "        int temp = 0;\n" +
    "        temp = x;\n" +
    "        x = y;\n" +
    "        y = temp;\n" +
    "    }\n" +
    "}\n" +
    "y = x; #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "1-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "1-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#1-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#1-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
