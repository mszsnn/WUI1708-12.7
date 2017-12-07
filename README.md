# WUI1708-12.7
@mixin xun($style,$count,$padding,$con){
  @if($con){
    .container{
      width: $con;
    }
  }
  @for $i from 1 to $count+1{
    .con-#{$style}-#{$i}{
      width: 1/$count*100%*$i;
      padding: $padding;
    }
  }
}

@media screen and (min-width: 1200px){
  @include xun(lg,5,15px,1200px);
}
@media screen and (max-width: 1200px) and (min-width: 992px){
  @include xun(xs,6,15px,992px);
}
@media screen and (max-width: 992px) and (min-width: 768px){
  @include xun(sm,2,15px,768px);
}
@media screen and (max-width: 768px){
  @include xun(md,9,15px,768px);
}
