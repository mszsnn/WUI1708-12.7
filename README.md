@mixin reactive($border,$pieces) {
  .container, .container-fluid {
    height: auto;
    overflow: hidden;
    box-sizing: border-box;
    margin-left: auto !important;
    margin-right: auto !important;
  }
  .row {
    width: 100%;
    height: auto;
    overflow: hidden;
    box-sizing: border-box;
    padding-left: 10px;
    padding-right: 10px;
  }
  .row:before, .row:after {
    content: "";
    display: block;
    width: 0;
    height: 0;
    line-height: 0;
    clear: both;
  }
  [class*="col-"] {
    float: left;
    border-bottom: $border solid #fff;
    border-right: $border solid #fff;
    box-sizing: border-box;
  }
  @media screen and (max-width: 768px) {
    @for $i from 1 through $pieces {
      .col-xs-#{$i} {
        width: 1/$pieces*100%*$i;
      }
    }
  }
  @media screen and (min-width: 768px) and (max-width: 992px) {
    .container {
      width: 750px;
    }
    @for $i from 1 through $pieces {
      .col-sm-#{$i} {
        width: 1/$pieces*100%*$i;
      }
    }
  }
  @media screen and (min-width: 992px) and (max-width: 1200px) {
    .container {
      width: 970px;
    }
    @for $i from 1 through $pieces {
      .col-md-#{$i} {
        width: 1/$pieces*100%*$i;
      }
    }
  }
  @media screen and (min-width: 1200px) {
    .container {
      width: 1170px;
    }
    @for $i from 1 through $pieces {
      .col-lg-#{$i} {
        width: 1/$pieces*100%*$i;
      }
    }
  }
}
@include reactive(15px,10);
