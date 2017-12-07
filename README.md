$padding:15px;
.container,.container-fluid {
  height: auto;
  overflow: hidden;
  margin-left: auto;
  margin-right: auto;
  padding-left:$padding;
  padding-right: $padding;
  box-sizing: border-box;
};
.row{
  height: auto;
  overflow: hidden;
  box-sizing: border-box;
  &::before,&::after{
    content: "";
    display: block;
    width: 0;
    height: 0;
    line-height: 0;
    clear: both;
  }
};
[class*="col-"] {
  float: left;
  padding-left: $padding;
  padding-right: $padding;
  box-sizing: border-box;
};
/* 手机<768px
平板768-992
pc小屏992-1200
pc大屏>1200px */
@mixin xun($type){
  @for $i from 1 to 13{
    col-#{$type}-#{$i}{
    width: 1/12*100%*$i;
    }
  }
}
@media screen and (max-width:768px ){
  @include xun(xs);
};
@media screen and (min-width: 768px) and (max-width: 992px){
  .container{
    width: 750px;
  }
  @include xun(sm);
}
@media screen and (min-width:992px ) and (max-width:1200px){
  .container{
    width: 970px
  }
  @include xun(md);
}
@media screen and (min-width: 1200px) {
  .container {
    width: 1170px;
  }
  @include xun(lg);
}
