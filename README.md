# 朱乐凯
$_box-sazing:border-box;
$_width:15px;
.container,.container-fluid{
  height: auto;
  overflow: hidden;
  box-sizing: $_box-sazing;
  margin-right: auto!important;
  margin-left: auto!important;
  padding-left: $_width;
  padding-right: $_width;
}
.row{
  width: 100%;
  height: auto;
  overflow: hidden;
  padding-left: -$_width;
  padding-right: -$_width;
  box-sizing: $_box-sazing;
}
.row{
  &:after,&:before{
    content: "";
    display: block;
    width: 0;
    height: 0;
    line-height: 0;
    clear: both;
  }
}

@mixin xuan($style,$type){
  @for $i from 1 through $style{
    .col-#{$type}-#{$i}{
    width: 1/$style*100%*$i;
    float: left;

    }
  }
}

@media screen and (max-width: 768px){
  
  @include xuan(12,xs);
}
@media screen and (min-width: 768px) and (max-width: 992px){
  @include xuan(12,sm);
}
@media screen and (min-width: 992px) and (max-width:1200px){
  @include xuan(12,md);
}
@media screen and (min-width: 1200px){
  @include xuan(12,lg);
}
