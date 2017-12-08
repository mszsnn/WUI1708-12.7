# WUI1708-12.7
$p:15px;
$m:-15px;
.container{
  height: auto;
  overflow: hidden;
  margin-left: auto;
  margin-right: auto;
  padding-left: $p;
  padding-right: $p;
  box-sizing: border-box;
}
.container-fluid{
  height: auto;
  overflow: hidden;
  margin-left: auto;
  margin-right: auto;
  box-sizing: border-box;
}
.row{
  height: auto;
  overflow: hidden;
  margin-left: $m;
  margin-right: $m;
  box-sizing: border-box;
}
.row::before,.row::after{
  content: "";
  display: block;
  width: 0;
  height: 0;
  line-height: 0;
  clear: both;
}
[class*="col-"]{
  float: left;
  padding-left: $p;
  padding-right: $p;
  box-sizing: border-box;
}

@mixin xun($type,$num){
  @for $i from 1 to $num {
    .col-#{$type}-#{$i}{
      width: 1/12*100%*$i;
    }
  }
}

/* pc大屏 col-lg-*/
@media screen and (min-width:1200px) {
  .container{
    width: 1170px;
  }
  @include xun(lg,13);
}
/* pc小屏  col-md-*/
@media screen and (min-width: 992px) and (max-width: 1200px){
  .container{
    width: 970px;
  }
  @include xun(md,13);
}
/* 平板端 col-sm-*/
@media screen and (min-width: 768px) and (max-width: 992px){
  .container{
    width: 750px;
  }
  @include xun(sm,13);
}
/* 手机端<768 col-xs-*/
@media screen and (max-width: 768px){
  @include xun(xs,13);
}
