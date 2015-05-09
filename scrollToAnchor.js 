/*
binds to click events on a elements with href
poitning to an anchor and scrolls to the matching element

Andrew Goldis agoldis@gmail.com
*/
(function(jQuery) {
  var $ = jQuery;


  var getTarget = function(href) {
    var name = href.substr(1);
    var query = '[name="' + name + '"]';
    return $(query);
  };

  var bindScrolling = function() {
    var $root = $('html, body');
    $('a[href*=#]').on('click', function(e) {
      e.preventDefault();
      var target = getTarget($.attr(this,'href'));
      $root.animate({
        scrollTop: target.offset().top
      }, 500);
    });
  };

  $(document).ready(bindScrolling)
})(jQuery);
