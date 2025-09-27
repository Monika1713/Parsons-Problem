
## Die Schildkröte bewegt sich

Bringe die Befehle in die korrekte Reihenfolge.

<div id="p2-sortableTrash" class="sortable-code"></div> 
<div id="p2-sortable" class="sortable-code"></div> 
<div style="clear:both;"></div> 
<p> 
    <input id="p2-feedbackLink" value="Get Feedback" type="button" /> 
    <input id="p2-newInstanceLink" value="Reset Problem" type="button" /> 
</p> 

<script type="text/javascript"> 
(function(){
  var initial = "fwd 30\n" +
                "rt 90\n" +
                "fwd 60\n" +
                "lt 90";
                
  var parsonsPuzzle = new ParsonsWidget({
    sortableId: "p2-sortable",
    max_wrong_lines: 10,
    grader: ParsonsWidget._graders.LineBasedGrader,
    exec_limit: 2500,
    can_indent: true,
    x_indent: 50,
    lang: "en",
    show_feedback: true,
    trashId: "p2-sortableTrash"
  });
  
  parsonsPuzzle.init(initial);
  parsonsPuzzle.shuffleLines();
  
  $("#p2-newInstanceLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.shuffleLines(); 
  }); 
  
  $("#p2-feedbackLink").click(function(event){ 
      event.preventDefault(); 
      parsonsPuzzle.getFeedback(); 
  }); 
})(); 
</script>


[Next](./parsons/example1.html)
