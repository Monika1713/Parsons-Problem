---
layout: default
title: Page 2 Example (Variable Check Grader)
---

Construct a program that swaps the values of variables <code>x</code> and <code>y</code> using the helper variable <code>tmp</code>. You can change the names of the variables (<span class="jsparson-toggle"></span>) by clicking them.

<div id="p3-sortableTrash" class="sortable-code"></div> 
<div id="p3-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="p3-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="p3-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 

<script type="text/javascript"> 
(function(){
  var initial = "gehe 50 vorwärts\n" +
                "drehe links\n" +
                "gehe 3 vorwärts";
                
  var parsonsPuzzle = new ParsonsWidget({
    sortableId: "p3-sortable",
    max_wrong_lines: 10,
    grader: ParsonsWidget._graders.LineBasedGrader,
    exec_limit: 2500,
    can_indent: true,
    x_indent: 50,
    lang: "en",
    show_feedback: true,
    trashId: "p3-sortableTrash"
  });
  
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  
  $("#p3-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#p3-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>
[Next](./example2.html)
