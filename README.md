# Option for resize colorbox()

var cboxOptions = {
  width: '95%',
  height: '95%',
  maxWidth: '960px',
  maxHeight: '960px',
}

$('.cbox-link').colorbox(cboxOptions);

$(window).resize(function(){
    $.colorbox.resize({
      width: window.innerWidth > parseInt(cboxOptions.maxWidth) ? cboxOptions.maxWidth : cboxOptions.width,
      height: window.innerHeight > parseInt(cboxOptions.maxHeight) ? cboxOptions.maxHeight : cboxOptions.height
    });
});
