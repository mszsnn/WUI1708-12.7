$height:auto;
$overflow:hidden;
$box-sizing:border-box;
$margin-right: auto !important;
$margin-left: auto !important;
$width:100%;
$content:"";
$display:block;
$line-height: 0;
$clear: both;
$float: left;
$padding-left: 15px;
$padding-right: 15px;
$box-sizing: border-box;
$i:1;
.container,.container-fluid{
  height:$height;
  overflow: $overflow;
  box-sizing:$box-sizing;
  margin-right: $margin-right;
  margin-left: $margin-left;
}
.row{
  width: $width;
  height: $height;
  overflow:$overflow;
  box-sizing:$box-sizing;
  &:before{
    content: $content;
    display:$display;
    width: 0;
    height: 0;
    line-height:$line-height;
    clear: $clear;
  }
  &:after{
    content: $content;
    display:$display;
    width: 0;
    height: 0;
    line-height:$line-height;
    clear: $clear;
  }

}
[class^="col-"]{
  float: $float;
  padding-left: $padding-left;
  padding-right:$padding-right;
  box-sizing: $box-sizing;
}
@mixin xun($type,$cont){
  @for $i from 1 to $cont{
    .col-#{$type}-#{$i}{
      width:1/12*100%*$i;
    }
  }
}
@media screen and(max-width:768px){
  @include xun(xs,13)
}
@media screen and(max-width:992px)and(min-width: 768px){
  .container{
    width: 750px;
  }
  @include xun(sm,13)
}
@media screen and(max-width:1200px)and(min-width: 992px){
  .container{
    width: 970px;
  }
  @include xun(md,13)
}
@media screen and(min-width:1200px){
  .container{
    width:1170px;
  }
  @include xun(lg,13)
}
