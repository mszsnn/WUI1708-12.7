$padding:15px;
$size:0;
.container,.container-fluid{
  height: auto;
  overflow: hidden;
  margin:{
    left:auto;
    right:auto;
  };
  padding:{
    left:$padding;
    right:$padding;
  };
  box-sizing: border-box;
}
.row{
  height:auto;
  overflow: hidden;
  margin:{
    left:$padding;
    right:$padding;
  };
  box-sizing: border-box;
  &::before,&::after{
    content: '';
    display: block;
    width:$size;
    height: $size;
    line-height:$size;
    clear: both;
  }
}
[class*="col-"]{
  float: left;
  padding:{
    left: 15px;
    right:15px;
  };
  box-sizing: border-box;
}
/***************************************/
$i:1;
$num:12;

@mixin xun($type){
  @for $i from 1 through 12{
    .col-#{$type}-#{$i}{
      width:1/$num*100%*$i;
    }
  }
}

@media screen and (max-width: 768px){

  @include xun(sm)
}
@media screen and (max-width: 992px) and (min-width: 768px){
  .container{
    width: 750px;
  }
  @include xun(md)
}
@media screen and (max-width: 1200px) and (min-width: 992px){
  .container{
    width: 970px;
  }
  @include xun(lg)
}
@media screen and (min-width: 1200px){
  .container{
    width: 1170px;
  }
  @include xun(xs)
}








