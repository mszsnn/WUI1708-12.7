# WUI1708-12.7



.container, .container-fluid {
  height: auto;
  overflow: hidden;
  margin: 0 auto !important;
  /* padding: 0 15px; */
  box-sizing: border-box;
}

.row {
  height: auto;
  width: 100%;
  overflow: hidden;
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

@mixin grid($val, $copies,$pl,$pr,$con) {
  @if ($con!=0) {
    .container {
      width: #{$con}px;
    }
  }

  @for $i from 1 to #{$copies} {
    .col-#{$val}-#{$i} {
      width: 1/$copies*100%*$i;
    }
  }

  [class*="col-#{$val}"] {
    float: left;
    padding: #{$pl}px #{$pr}px;
    box-sizing: border-box;
  }
}

/*手机端 col-xs*/
@media screen and (max-width: 768px) {
  @include grid(xs, 12, 0, 15, 0);
}

/* 平板端 col-sm*/
@media screen and (min-width: 768px) and (max-width: 992px) {
  @include grid(sm, 12, 0, 15, 750);
}

/* PC小屏 col-md*/
@media screen and (min-width: 992px) and (max-width: 1200px) {
  @include grid(md, 12, 0, 15, 970);
}

/* PC大屏 col-lg*/
@media screen and (min-width: 1200px) {
  @include grid(lg, 12, 0, 15, 1170);
}
