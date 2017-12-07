$width:100px;
$height:100px;
$padding:15px;
$i:1;
$j:12;
.container,
.container-fluid {
	height: auto;
	overflow: hidden;
	margin-left: auto;
	margin-right: auto;
	padding-left: $padding;
	padding-right: $padding;
	box-sizing: border-box;
}
.row {
    height: auto;
	overflow: hidden;
    box-sizing: border-box;
    &::before,::after{
        content: "";
        display: block;
        width: $width*0;
        height: $height*0;
        line-height: 0;
        clear: both;
    }
}
[class*="col-"] {
	float: left;
	padding-left: 15px;
	padding-right: 15px;
	box-sizing: border-box;
}
@mixin xun ($type){
    @for $i from 1 through 12 {
    .col-#{$type}-#{$i}{
        width: 1/$j*100%*$i;
    }
 }
}
@media screen and (max-width: 768px){
    @include xun (xs)
}
@media screen and (min-width: 768px) and (max-width: 992px) {
    @include xun (sm)
}
@media screen and (min-width: 992px) and (max-width: 1200px) {
    @include xun (md)
}
@media screen and (min-width: 1200px) {
    @include xun (lg)
}
