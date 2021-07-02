---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: default
title: Parson's Problems Java Variables and Expression
---
# Parsons Practice

## Variable and Expression Review
The following has the correct code to ‘swap’ the values in x and y (so that x ends up with y’s initial value and y ends up with x’s initial value), but the code is mixed up. Drag the needed blocks from the left into the correct order on the right. Check your solution by clicking on the Check button. You will be told if any of the blocks are in the wrong order or if you need to remove one or more blocks. 

<div id="Var-sortableTrash" class="sortable-code"></div> 
<div id="Var-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="Var-feedbackLink" value="Get Feedback" type="button" /> 
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
    "exec_limit": 2500,
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
