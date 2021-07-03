---
title: Code Tracing Review
---

## Directions: 
<div style="text-align: justify"> 
The following has the correct code to ‘swap’ the values in x and y (so that x ends up with y’s initial value and y ends up with x’s initial value), but the code is mixed up and contains one extra block which is not needed in a correct solution. 
Drag the needed blocks from the top into the correct order at the bottom. 
Check your solution by clicking on the Check button. Your can click Reset Problem button to reshuffle the code blocks. 
You will be told if any of the blocks are in the wrong order. </div>



<div id="Var-sortableTrash" class="sortable-code"></div> 
<div id="Var-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Var-feedbackLink" value="Check" type="button" /> 
    <input id="Var-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "int x = 3;\n" +
    "int y = 5;\n" +
    "int temp = 0;\n" +
    "temp = x;\n" +
    "x = y;\n" +
    "y = temp;\n" +
    "x=y; #distractor";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "Var-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 3,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "Var-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#Var-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#Var-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

### Example Next Link
[Problem 2](./https://github.com/Nureni82/hosting-parsons-on-github-template/blob/master/index2.markdown)
