# WUI1708-12.7

$i: 1;
$count: 3;
$padding: 0px;
@mixin xun($type,$count,$padding) {
  @for $i from 0 through $count {
    .col-#{$type}-#{$i} {
      width: 1/12*100%*$i;
      box-sizing: border-box;
      padding: $padding;
    }
  }
}

@media screen and (max-width: 768px) {

  @include xun(xs, 12, 10px)

}

@media screen and (max-width: 992px) and (min-width: 768px) {
  .container{width: 750px;}
  @include xun(sm, 12, 10px)
}

@media screen and (max-width: 1200px) and (min-width: 992px) {
  .container{width: 970px;}
  @include xun(md, 12, 10px)
}

@media screen and (min-width: 1200px) {
  .container{width: 1200px;}
  @include xun(lg, 12, 10px)
}

$auto: auto;
$hidden: hidden;
$border-box: border-box;
.container, .container-fluid {
  height: $auto;
  overflow: $hidden;
  box-sizing: $border-box;
  margin-left: $auto !important;
  margin-right: $auto !important;
}

.row {
  width: 100%;
  height: auto;
  overflow: hidden;
  box-sizing: border-box;
  &:after, &:before {
    content: '';
    display: block;
    width: 0;
    height: 0;
    line-height: 0;
    clear: both;
  }

}
$left15:15px;$right15:15px;
[class*="col-"] {
  float: left;
  padding-left: $left15;
  padding-right:$right15;
}

