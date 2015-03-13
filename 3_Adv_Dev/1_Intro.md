#This should include text from another page

<html> 
  <head> 
    <script src="jquery.js"></script> 
    <script> 
    $(function(){
      $("#includedContent").load("http://ble-intros.readthedocs.org/en/latest/GettingStarted/DesignersIntro/#mbed"); 
    });
    </script> 
  </head> 

  <body> 
     <div id="includedContent"></div>
  </body> 
</html>
