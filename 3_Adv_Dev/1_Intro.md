#This should include text from another page

<html> 
  <head> 
    <script src="jquery.js"></script> 
    <script> 
    $(function(){
      $("#includedContent").load("http://docs.mbed.org/docs/ble-intros/en/latest/AdvSamples/Overview/"); 
    });
    </script> 
  </head> 

  <body> 
     <div id="includedContent"></div>
  </body> 
</html>
