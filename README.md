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
