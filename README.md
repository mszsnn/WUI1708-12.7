# WUI1708-12.7
$overflow: hidden;
$box-sizing: border-box;
$padding:15px;


.container,.container-fluid{
  height: auto;
  overflow: $overflow;
  box-sizing: $box-sizing;
  margin: 0 auto;
  padding-left: $padding;
  padding-right: $padding;
}
.row{
  width: 100%;
  height: auto;
  overflow:$overflow ;
  padding-left: -$padding;
  padding-right:- $padding;
  box-sizing: $box-sizing;

}
.row:after,.row:before{
  content: "";
  display: block;
  width: 0;
  height: 0;
  line-height: 0;
  clear: both;
}

[class*="col-"]{
  float: left;
  box-sizing: $box-sizing;
}



//混合宏
@mixin xun($type,$count){
  @for $a from 1 through 12{
    .col-#{$type}-#{$a}{
      width:1/$count*100%*$a;
      padding:$padding;
    }
  }
}
//pc大屏 col-lg
@media screen and (min-width: 1200px) {
  .container{
    width: 1170px;
  }
  @include xun(lg,12);

}
//pc小屏 col-md
@media screen and (max-width: 1200px) and (min-width: 992px) {
  .container{
    width: 970px;
  }
  @include xun(md,12);

}
/* 平板端 col-sm*/
@media screen and (max-width: 992px) and (min-width: 768px) {
  .container{
    width: 750px;
  }
  @include xun(ms,12);
}
//手机屏 col-xs
@media screen and (max-width: 1200px) {
  @include xun(xs,12);

}





@charset "UTF-8";
.container, .container-fluid {
  height: auto;
  overflow: hidden;
  box-sizing: border-box;
  margin: 0 auto;
  padding-left: 15px;
  padding-right: 15px;
}

.row {
  width: 100%;
  height: auto;
  overflow: hidden;
  padding-left: -15px;
  padding-right: -15px;
  box-sizing: border-box;
}

.row:after, .row:before {
  content: "";
  display: block;
  width: 0;
  height: 0;
  line-height: 0;
  clear: both;
}

[class*="col-"] {
  float: left;
  box-sizing: border-box;
}

@media screen and (min-width: 1200px) {
  .container {
    width: 1170px;
  }
  .col-lg-1 {
    width: 8.33333%;
    padding: 15px;
  }
  .col-lg-2 {
    width: 16.66667%;
    padding: 15px;
  }
  .col-lg-3 {
    width: 25%;
    padding: 15px;
  }
  .col-lg-4 {
    width: 33.33333%;
    padding: 15px;
  }
  .col-lg-5 {
    width: 41.66667%;
    padding: 15px;
  }
  .col-lg-6 {
    width: 50%;
    padding: 15px;
  }
  .col-lg-7 {
    width: 58.33333%;
    padding: 15px;
  }
  .col-lg-8 {
    width: 66.66667%;
    padding: 15px;
  }
  .col-lg-9 {
    width: 75%;
    padding: 15px;
  }
  .col-lg-10 {
    width: 83.33333%;
    padding: 15px;
  }
  .col-lg-11 {
    width: 91.66667%;
    padding: 15px;
  }
  .col-lg-12 {
    width: 100%;
    padding: 15px;
  }
}

@media screen and (max-width: 1200px) and (min-width: 992px) {
  .container {
    width: 970px;
  }
  .col-md-1 {
    width: 8.33333%;
    padding: 15px;
  }
  .col-md-2 {
    width: 16.66667%;
    padding: 15px;
  }
  .col-md-3 {
    width: 25%;
    padding: 15px;
  }
  .col-md-4 {
    width: 33.33333%;
    padding: 15px;
  }
  .col-md-5 {
    width: 41.66667%;
    padding: 15px;
  }
  .col-md-6 {
    width: 50%;
    padding: 15px;
  }
  .col-md-7 {
    width: 58.33333%;
    padding: 15px;
  }
  .col-md-8 {
    width: 66.66667%;
    padding: 15px;
  }
  .col-md-9 {
    width: 75%;
    padding: 15px;
  }
  .col-md-10 {
    width: 83.33333%;
    padding: 15px;
  }
  .col-md-11 {
    width: 91.66667%;
    padding: 15px;
  }
  .col-md-12 {
    width: 100%;
    padding: 15px;
  }
}

/* 平板端 col-sm*/
@media screen and (max-width: 992px) and (min-width: 768px) {
  .container {
    width: 750px;
  }
  .col-ms-1 {
    width: 8.33333%;
    padding: 15px;
  }
  .col-ms-2 {
    width: 16.66667%;
    padding: 15px;
  }
  .col-ms-3 {
    width: 25%;
    padding: 15px;
  }
  .col-ms-4 {
    width: 33.33333%;
    padding: 15px;
  }
  .col-ms-5 {
    width: 41.66667%;
    padding: 15px;
  }
  .col-ms-6 {
    width: 50%;
    padding: 15px;
  }
  .col-ms-7 {
    width: 58.33333%;
    padding: 15px;
  }
  .col-ms-8 {
    width: 66.66667%;
    padding: 15px;
  }
  .col-ms-9 {
    width: 75%;
    padding: 15px;
  }
  .col-ms-10 {
    width: 83.33333%;
    padding: 15px;
  }
  .col-ms-11 {
    width: 91.66667%;
    padding: 15px;
  }
  .col-ms-12 {
    width: 100%;
    padding: 15px;
  }
}

@media screen and (max-width: 1200px) {
  .col-xs-1 {
    width: 8.33333%;
    padding: 15px;
  }
  .col-xs-2 {
    width: 16.66667%;
    padding: 15px;
  }
  .col-xs-3 {
    width: 25%;
    padding: 15px;
  }
  .col-xs-4 {
    width: 33.33333%;
    padding: 15px;
  }
  .col-xs-5 {
    width: 41.66667%;
    padding: 15px;
  }
  .col-xs-6 {
    width: 50%;
    padding: 15px;
  }
  .col-xs-7 {
    width: 58.33333%;
    padding: 15px;
  }
  .col-xs-8 {
    width: 66.66667%;
    padding: 15px;
  }
  .col-xs-9 {
    width: 75%;
    padding: 15px;
  }
  .col-xs-10 {
    width: 83.33333%;
    padding: 15px;
  }
  .col-xs-11 {
    width: 91.66667%;
    padding: 15px;
  }
  .col-xs-12 {
    width: 100%;
    padding: 15px;
  }
}
