# WUI1708-12.7
$padding:15px;
@mixin xunhuan($type,$num){
  @for $i from 1 through $num{
    .col-#{$type}-#{$i}{
      width:1/$num*100%*$i;
      padding:$padding;
    }
  }
}
@media screen and (min-width:1200px) {
  .container{
    width: 1200px;
  }
  @include xunhuan(lg,12);
}
@media screen and (max-width:1200px) and (min-width:992px){
  .container{
    width: 970px;
  }
  @include xunhuan(md,12);
}
@media screen and (max-width:992px) and (min-width:768px){
  .container{
    width: 768px;
  }
  @include xunhuan(sm,12);
}
@media screen and (max-width:768px){
  @include xunhuan(xs,12);
}
