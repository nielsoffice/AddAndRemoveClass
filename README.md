# AddAndRemoveClass
JS remove multiple Class that assigned on element

```JS
    const removeMutipleClass = function(cID, setClass) {
     
    // get target element 
    let _id = document.getElementById(cID);	
    // condition to assigned class
    let doResize = window.screen.availWidth;
    let rSize = 768;	
		
    // if meet is set a true?
    if ( doResize <= rSize ) 
    { jQuery('#' + cID).addClass(setClass); } // set do add class
		
    // check how many class are assigned 
    // IF CLASS is >= 3 [ console.log( _id.classList.length ) ]
    // then removeClass
    if( _id.classList.length  >= 3 ) 
    // retarget the emenet needs to remve class
    { jQuery('#' +cID).removeClass( _id.classList[1] ); } // remove class from classList the last one added removed!
	 
    }
  
```

```JS

    const AddClassThenRemove = function(cID, conID) {

     // addClass on it can be attribute if you wish!	
    let ifTrue = jQuery('#' + cID).parent().addClass('HP-disable-active');
		  	
    // Then check until condition get true!    
    if(ifTrue.hasClass('HP-disable-active')) {
	   
       // IF DO SO! DO some mgic here....
		
    }
		
    // After the maic happened remove the class so I can do it over and over again
    jQuery('#' + cID).parent().removeClass('HP-disable-active'); 
 
   }
   
```

```HTML
<!DOCTYPE html>
<!-- Created By CodingNepal -->
<html lang="en" dir="ltr">
  <head>
    <meta charset="utf-8">
    <title>Custom Range Slider | CodingNepal</title>
    <link rel="stylesheet" href="style.css">
    <script src="https://ajax.googleapis.com/ajax/libs/jquery/3.6.4/jquery.min.js"></script>
    <style>

    </style>
  </head>
  <body>
  <div class="range">

    <input type="checkbox" class="data-val active" id="data-1" name="data-1" value="200">
    <input type="checkbox" class="data-val" id="data-2" name="data-2" value="1000">
    <input type="checkbox" class="data-val" id="data-3" name="data-3" value="2000">
    <input type="checkbox" class="data-val" id="data-4" name="data-4" value="5000">
    <input type="checkbox" class="data-val" id="data-5" name="data-5" value="20000">
    <input type="checkbox" class="data-val" id="data-6" name="data-6" value="50000">

 </div>
<script>

$(document).ready(function() {
  
  let linkPrice = '.data-val';	
	
  jQuery(linkPrice).css('cursor','pointer');
   
  const unLoopActiveClass = function(cID, conID) {
 
   // addClass on it can be attribute if you wish!	
   let activeClass = jQuery(cID);
 
   // Then check until condition get true!    
   if(activeClass.hasClass('active')) { 
   
   activeClass.removeClass('active'); 
   jQuery('#' + conID).addClass('active');
     
   }
  }
   
  jQuery(linkPrice).bind('click', function() {
 
    let unloopNextID = jQuery(this)[0].id; 
    
    unLoopActiveClass(linkPrice, unloopNextID); 
     
  });
   

});
```
