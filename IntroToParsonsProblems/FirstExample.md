---
title: Introduction To Parson's Problems
---

#### The goal is for you to get used to using the Parson's Problem tool itself.

## Directions:

<div style="text-align: justify"> 
<p>Construct a working program by dragging & dropping lines from the left to the right. You'll need to change the order of the lines and you'll need to adjust the indentation correctly.</p>
<p>The code should print out the message "Welcome to BIT 115", inside of a correctly formed Java program.  It doesn't have to do anything other than that</p>
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
