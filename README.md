$p:15px;
@mixin xun($type,$num){
  @for $i from 1 through $num{
    -col-#{$type}-#{$num}{
      width: 1/$num*100%*$i;
      padding: $p;
    }
  }
}
@media screen and (max-width:768px){
  @include xun(xs,12);
}
@media screen and (min-width:768px) and (max-width:992px){
  .container{
    width: 750px;
  }
  @include xun(sm,12);
}
@media screen and (min-width:992px) and (max-width:1200px){
  .container{
    width: 970px;
  }
  @include xun(md,12);
}
@media screen and (min-width:1200px){
  .container{
    width: 1170px;
  }
  @include xun(lg,12);
}

