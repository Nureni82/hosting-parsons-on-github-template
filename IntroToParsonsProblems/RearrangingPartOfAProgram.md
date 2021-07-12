---
title: Rearranging only part of a program
---

#### The goal is for you to get used to using the Parson's Problem tool itself in a way that gets around the problem of having to rearrange lots and lots of 'boilerplate' lines

<p>This is because Java has a lot of lines that are important for Java, but aren't so important for us humans studying today's topic</p>

## Directions:

<div style="text-align: justify"> 
    <p>Construct a working program by dragging & dropping lines from the left to the right. You'll need to change the order of the lines and you'll need to adjust the indentation correctly.</p>
    <p>What's new for this exercise is that you will only fix PART of the program - namely, the lines marked "FIX THIS PART".</p>
    <p>Normally you'll be given something like this:</p>
    <hr/>   
    <p> </p>
    <pre>
class RearrangingPartsOfTheProgram {
  public static void main(String[] args) {
    // FIX THIS PART!!!
  }
}
</pre>
    <p>Task: You must rearrange the given lines of the program so that the finished program compiles, runs, and produces the following output:</p>
<pre>
Hello
 
world!
</pre>
    <p>You are given the following lines to (re)arrange:</p>
<pre>
    System.out.println("Hello");    
    System.out.println(" ");
    System.out.println("world!");
</pre>
    <p> </p>
    <hr/>
    <p>You will be expected to produce a program that looks like this:</p>
    <pre>
class RearrangingPartsOfTheProgram {
  public static void main(String[] args) {
    System.out.println("Hello");    
    System.out.println(" ");
    System.out.println("world!");
  }
}
</pre>
</div>

### Try it yourself:

<div>
<p>Given the following program 'outline':</p>
    <hr/>    
    <pre>
class RearrangingPartsOfTheProgram {
  public static void main(String[] args) {
    // FIX THIS PART!!!
  }
}
</pre>
    <p>Task: You must rearrange the given lines of the program so that the finished program compiles, runs, and produces the following output:</p>
<pre>
Welcome 
to 
BIT 
115
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
  var initial = "    System.out.println(&quot;Welcome &quot;);    \n" +
    "    System.out.println(&quot;to &quot;);\n" +
    "    System.out.println(&quot;BIT &quot;);\n" +
    "    System.out.println(&quot;115&quot;);";
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
