
## Ein farbiges 3-Eck

Bringe die Befehle in die korrekte Reihenfolge. Ziehe die Blöcke dazu von links nach rechts. 
Über den Knopf "Get Feeback" kannst du kontrollieren, ob du richtig liegst.

<div id="p8-sortableTrash" class="sortable-code"></div>
<div id="p8-sortable" class="sortable-code"></div>
<div style="clear:both;"></div>
<p>
  <input id="p8-feedbackLink" value="Get Feedback" type="button" />
  <input id="p8-newInstanceLink" value="Reset Problem" type="button" />
</p>

<script type="text/javascript">
(function(){
  var initial = "rt 90\n" +
                "setpc red fd 200\n" +
                "lt 90\n" +
                "setpc blue fd 200\n" +
                "lt 135\n" +
                "setpc green fd 300";
  
  var parsonsPuzzle = new ParsonsWidget({
    sortableId: "p8-sortable",
    max_wrong_lines: 10,
    grader: ParsonsWidget._graders.LineBasedGrader,
    exec_limit: 2500,
    can_indent: true,
    x_indent: 50,
    lang: "en",
    show_feedback: true,
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

