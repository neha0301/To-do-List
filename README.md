# To-do-List
A To-do List app created with tml,css, and jQuery. The app consists additional styling icons added from font-awesome and uigradients.com.
$('ul').on("click","li",function(){
	$(this).toggleClass("done");	
})
$('ul').on("click","span",function(event){
	
	$(this).parent().fadeOut(1000,function(){
			$(this).remove();
	});
	event.stopPropagation();
})
$("input[type='text']").on("keypress",function(event){
	if(event.which===13)
	{
		var todoText=$(this).val();
		$(this).val("");
		$("ul").append("<li><span><i class='fa fa-trash'></i></span> " +todoText+ "</li>");
	}
})
$(".fa-pencil").on("click",function(){
	$("input").fadeToggle(1000);
})
