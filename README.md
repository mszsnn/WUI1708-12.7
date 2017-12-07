@mixin xun($type,$count,$padding){
  @for $i from 1 through $count{
    .col-#{$type}-#{$i}{
      width: 1/$count*100%*$i;
      float: left;
      padding-left: $padding;
      padding-right: $padding;
      box-sizing: border-box;
    }
  }
}
.container,.container-fluid{
  height: auto;
  overflow: hidden;
  box-sizing: border-box;
  margin-left: auto !important;
  margin-right: auto !important;
}
.row{
  width: 100%;
  height: auto;
  overflow: hidden;
  box-sizing: border-box;
}
.row:before,.row:after{
  content: "";
  display: block;
  width: 0;
  height: 0;
  line-height: 0;
  clear: both;
}
@media screen and (min-width:1200px){
  @include xun(lg,12,20px);
}
@media screen and (max-width:1200px) and (min-width: 992px){
  @include xun(md,12,20px);
}
@media screen and (max-width:992px) and (min-width: 768px){
  @include xun(sm,12,20px);
}
@media screen and (max-width:768px) {
  @include xun(xs,12,20px);
}
