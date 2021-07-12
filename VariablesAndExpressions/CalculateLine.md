---
title: Using the Slope/Intercept Form Of A Line
---

## Purpose:

 <p>The goal is practice arranging the steps of a formula/function into the correct steps, which will help you practice both statement sequencing and Java expressions</p>

<p>Construct a working program by dragging & dropping lines from the left to the right. You'll need to change the order of the lines and you'll need to adjust the indentation correctly.</p>

## Directions :

<div style="text-align: justify">
    <p>Task: You must rearrange the given lines of the program so that the finished program compiles, runs, and produces the following output:</p>
<pre>
y = 0.6*x + 2.0
when x is 10, y is 8.0
</pre>
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
  var initial = "// Line 1: y = mx + b\n" +
    "// Line 2: Let's declare the variables in left-to-right order\n" +
    "class SlopeIntercept {\n" +
    "  public static void main(String[] args) {\n" +
    "      double y;\n" +
    "      double m = 3.0/5.0;\n" +
    "      double x = 10;\n" +
    "      double b = 2;\n" +
    "      double firstStep = m * x;\n" +
    "      y = firstStep + b;\n" +
    "      System.out.println(\"y = \" + m + \"*x + \" + b );\n" +
    "      System.out.println(\"when x is 10, y is \" + y);\n" +
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
