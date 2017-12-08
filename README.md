@mixin xun($type,$count,$padding){
  @for $i from 1 to ($count)+1{
    .col-#{$type}-#{$i}{
      width: 1/($count)*100%*$i;
      padding: ($padding);
    }
  }
}
@media screen and (min-width:1200px){
  @include xun(lg,12,15px);
}
@media screen and (max-width:1200px)and(min-width: 992px){
  @include xun(md,12,15px);
}
@media screen and (max-width:992px)and(min-width: 768px){
  @include xun(sm,12,15px);
}
@media screen and (max-width:768px){
  @include xun(xs,12,15px);
}
$auto:auto;
.container,.container-fluild{
  height: $auto;
  overflow: hidden;
  margin-left: $auto!important;
  margin-right: $auto!important;
  box-sizing: border-box;
}

.row{
  width: 100%;
  height: $auto;
  overflow: hidden;
  box-sizing: border-box;
  &:before,&:after{
    content: "";
    display: block;
    width: 0;
    height: 0;
    line-height: 0;
    clear: both;
  }
}
[class*="col-"]{
  float: left;
  padding-left: 15px;
  padding-right: 15px;
  box-sizing: border-box;
}
