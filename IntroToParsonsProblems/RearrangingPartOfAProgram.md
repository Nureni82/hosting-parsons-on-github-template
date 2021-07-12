---
title: Rearranging only part of a program
---

#### The goal is for you to get used to using the Parson's Problem tool itself in a way that gets around the problem of having to rearrange lots and lots of 'boilerplate' lines

<p>This is because Java has a lot of lines that are important for Java, but aren't so important for us humans studying today's topic</p>

## Directions:

<div style="text-align: justify"> 
    <p>Construct a working program by dragging & dropping lines from the left to the right. You'll need to change the order of the lines and you'll need to adjust the indentation correctly.</p>
</div>

<div id="sortableTrash" class="sortable-code"></div> 
<div id="sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="feedbackLink" value="Get Feedback" type="button" /> 
    <input id="newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "    System.out.println(\"Welcome \");    \n" +
    "    System.out.println(\"to \");\n" +
    "    System.out.println(\"BIT \");\n" +
    "    System.out.println(\"115\");";
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
