#This should include text from another page

<html> 
  <head> 
    <script src="jquery.js"></script> 
    <script> 
    $(function(){
      $("#includedContent").load("https://developer.mbed.org/handbook/Homepage"); 
    });
    </script> 
  </head> 

  <body> 
     <div id="includedContent"></div>
  </body> 
</html>
