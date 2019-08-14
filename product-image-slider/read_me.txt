Installation and configuration detail :
----------------------------------------------------------

>> Install this extension through magento connect key.

>> Now open media.phtml file
>> path : app/design/frontend/rwd/default/template/catalog/product/view/media.phtml
>> Replace lin no : 70 with this :
   <ul class="product-image-thumbs bxslider-media">
>> Also add below code at end of the file :
   
   <script type="text/javascript" src="<?php echo $this->getSkinUrl('js/jquery.bxslider.js', array('_secure'=>true));?>"></script>
  <script type="text/javascript" src="<?php echo $this->getSkinUrl('js/jquery.bxslider.min.js', array('_secure'=>true));?>"></script>
  <link rel="stylesheet" href="<?php echo $this->getSkinUrl(); ?>css/jquery.bxslider.css" type="text/css" />
  <?php if (count($this->getGalleryImages()) > 3): ?>
  <script>
    $j = jQuery.noConflict();
    $j(document).ready(function(){
    $j('.bxslider-media').bxSlider({
       infiniteLoop: false,
        minSlides: 3,
        maxSlides: 4,
        slideWidth: 79,
        slideMargin: 10
    });
    });
        
 </script> 
 
------------------------------------------------------------------
 Contact Detail     
------------------------------------------------------------------ 

Email : support@i-quall.com or iquallinfo@gmail.com