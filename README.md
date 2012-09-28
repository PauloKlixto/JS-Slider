JS-Slider
=========

function avancarState() {
jQuery(".slider-engine").animate({
marginLeft:"-=1000px",
marginRight:"+=1000px"
});
}
function voltarState() {
jQuery(".slider-engine").animate({
marginLeft:"+=1000px",
marginRight:"-=1000px"
});
}
jQuery(document).ready(function(){
jQuery(".voltar:first").hide();
jQuery(".avancar:last").hide();
jQuery(".menu-produtos li:first-child").addClass("categoriaproduto");
jQuery("ul.menu:last").addClass( "menu-no-border" );

window.setInterval(function(){
if (((jQuery("#slider-content .slider-engine").length - 1) * 1000) >  parseInt(jQuery("#slider-content .slider-engine").css("margin-right"))) {
avancarState();
} else {
for (i=1; i<jQuery("#slider-content .slider-engine").length; i++) {
voltarState();
}
}

}, 8000);
});