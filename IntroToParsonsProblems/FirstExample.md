---
title: Code Tracing Review
---

## Directions:

<div style="text-align: justify"> 
The following has the correct code to ‘swap’ the values in x and y (so that x ends up with y’s initial value and y ends up with x’s initial value), but the code is mixed up and contains one extra block which is not needed in a correct solution. 
Drag the needed blocks from the top into the correct order at the bottom. 
Check your solution by clicking on the Get Feedback button. Your can click Reset Problem button to reshuffle the code blocks. 
You will be told if any of the blocks are in the wrong order. </div>

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "class Main {\n" +
    "  public static void main(String[] args) {\n" +
    "    System.out.println(&quot;Welcome To BIT 115&quot;);\n" +
    "  }\n" +
    "}";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "trashId": "sortableTrash"
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
