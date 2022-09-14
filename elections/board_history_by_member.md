---
title: OWASP Global Board History by Member
layout: col-sidebar
permalink: /board_history/bymember/
---

<div>
<label for='board-filter'>Filter List:</label>
<input type='text' id='board-filter'>&nbsp;&nbsp;<button id='reset'>Reset Filter</button>
</div>


{% assign board_members = site.data.board-history | sort: 'year' | map: 'members' | map: 'name' | uniq %}
{% assign all_members = '' | split: ',' %}
{% for member in board_members %}
{{ member }}
{% assign years = "" %}
{% for history in site.data.board-history %}
{% for hmember in history.members %}
{% if hmember.name == member %}
{% assign years = years | append: history.year | append: ", " %}
{% endif %}
{% endfor %}
{% endfor %}
{% assign tsize = years.size | minus: 1%}
{{ years | truncate: tsize, " " }}
{% endfor %}


<script type='text/javascript'>      
    $("#board-filter").keyup(function(e) {
        var code = e.keyCode ? e.keyCode : e.which;
        
        if (code == 13) {  // Enter keycode
            var filter = $('#board-filter').val();         
            skip_next = false;
            
            $("p").each(function() {
                if(filter == ""){
                    $(this).show();
                }else{
                    if(skip_next){
                        skip_next = false;
                    }else{
                        if($(this).text().indexOf(filter) >= 0){
                            skip_next = true;
                        }else{
                            $(this).hide();
                            skip_next = false;
                        }
                    }
                }
            });
        }
    $("#reset").click(function(e){
        $("p").each(function() {                
                $(this).show();                
            });
    });
   });
</script>