
jQuery(document).ready(function($) {

	"use strict";	
	

textareaheight();
})
var textareaheight=function(){
	$('textarea').each(function () {

	debugger;
	//var data = document.getElementById("textarea").parentElement.style.display;
	var scrollheight = this.scrollHeight;
	var rows = document.querySelector('textarea').value.split("\n").length;
	
	var data= document.querySelector('textarea').parentElement.style.display;
	//alert(data)
	if(scrollheight=='35' && rows=='')
	{
		
	
		 //this.setAttribute('style', 'height:' + (this.scrollHeight-10) + 'px;overflow-y:hidden;');
		
	}
	
	else if (scrollheight=='0'){
	
		// this.setAttribute('style', 'height:' + (this.scrollHeight+25) + 'px;overflow-y:hidden;');
		
		 // "class", "democlass"
		  //this.setAttribute('class', 'md-textarea form-control textarea_hide');
	}
	
	else{
if(rows=='1' || rows=='0'){

	 this.setAttribute('style', 'height:30px;overflow-y:hidden;');
	  
}
else if(rows=='2'){
	
	 this.setAttribute('style', 'height:' + (this.scrollHeight-10) + 'px;overflow-y:hidden;');
	  
}

 this.setAttribute('style', 'height:' + (this.scrollHeight) + 'px;overflow-y:hidden;');
 if(this.scrollHeight <= 30){
	 this.style.height = '32px';
 }

	}
	  
	}).on('input', function (evnt) {
		debugger;  
		 var scrollheight = evnt.target.scrollHeight;
			 var rows =evnt.target.value.split("\n").length;
			 if(navigator.userAgent.indexOf("Firefox") != -1 ) {
			    if(this.scrollHeight==30 && rows=='1'||this.scrollHeight==32 && rows=='1'||this.scrollHeight==29 && rows=='1'||this.scrollHeight==28 && rows=='1') {	
			     this.style.height = 'hidden';
			     this.style.height = '32px';
			    }else if(evnt.target.value=="" && rows=='1') {
			    	 this.style.height = 'auto';
				     this.style.height = (this.scrollHeight-17) + 'px';
			    }    
			    else{
			    	this.style.height = 'auto';
				     this.style.height = (this.scrollHeight) + 'px';
				     
			    }
			  }else{
				  this.style.height = 'auto';
				     this.style.height = (this.scrollHeight) + 'px';
			  }
			})	
}
