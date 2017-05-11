Test Collapsible Text
======================

.. raw:: html

  <style>
  .left {
      float:left;
  }
  .hide {
      display:none
  }
  </style>
  <script>
  function toggle_messege(type) {
   document.getElementById("div_messege").style.display = type;
     document.getElementById("hreh_close").style.display = type;
  }
  </script>

  <a class="left" href="javascript:toggle_messege('inline')" id='href_about'> About </a>
  <br />
  <a class="left hide" href="javascript:toggle_messege('none')" id='hreh_close'> (Close)</a>
  
  <div id='div_messege' class='hide'>Hidden messege to show, Hidden messege to show Hidden messege to show Hidden messege to show</div>
