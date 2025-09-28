
## Die Schildkröte bewegt sich

Bringe die Befehle in die korrekte Reihenfolge.

<div id="p8-sortableTrash" class="sortable-code"></div> 
<div id="p8-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="p8-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="p8-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 
<script type="text/javascript"> 
(function(){
  var initial = "schritt 1
\n" +
    "Schritt 2
\n" +
    "Schritt 3";
  var parsonsPuzzle = new ParsonsWidget({
    sortableId: "p8-sortable",
    max_wrong_lines: 10,
    grader: ParsonsWidget._graders.LineBasedGrader,
    exec_limit: 2500,
    can_indent: true,
    x_indent: 50,
    lang: "en",
    show_feedbac": true,
    trashId: "p8-sortableTrash"
  });
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  $("#p8-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  $("#p8-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>

[Next](./parsons/example1.html)
