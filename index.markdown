
## Die Schildkröte bewegt sich

Bringe die Befehle in die korrekte Reihenfolge.

<div id="8-sortableTrash" class="sortable-code"></div> 
<div id="8-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="8-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="8-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "schritt 1
\n" +
    "Schritt 2
\n" +
    "Schritt 3";
  var parsonsPuzzle = new ParsonsWidget({
    "sortableId": "8-sortable",
    "max_wrong_lines": 10,
    "grader": ParsonsWidget._graders.LineBasedGrader,
    "exec_limit": 2500,
    "can_indent": true,
    "x_indent": 50,
    "lang": "en",
    "show_feedback": true,
    "trashId": "8-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#8-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#8-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


[Next](./parsons/example1.html)
