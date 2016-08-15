# SCSS Flexbox Mixins
These mixins include the broswer specific fallbacks for flexbox.

<h3><strong>Flexbox</strong></h3>
<em>Mixin:</em>
<pre>
// no value needed

@mixin flexbox() {
	display: -webkit-box;
	display: -moz-box;
	display: -ms-flexbox;
	display: -webkit-flex;
	display: flex;
}
</pre>
<em>Usage:</em>
<pre>.flexbox-class{ @include flexbox(); }</pre>
<h3><strong>Flex Wrap</strong></h3>
<em>Mixin:</em>
<pre>
$value: nowrap | wrap | wrap-reverse

@mixin flex-wrap($value){
	-webkit-box-flex-wrap: $value;
	-moz-box-flex-wrap: $value;
	-webkit-flex-wrap: $value;
	-ms-flex-wrap: $value;
	flex-wrap: $value;
}
</pre>
<em>Usage:</em>
<pre>.flex-wrap{ @include flex-wrap(wrap); }</pre>
<h3><strong>Flex</strong></h3>
<em>Mixin:</em>
<pre>
// Shorthand for flex-grow, flex-shrink and optionally flex-basis. Space separated, in that order.

@mixin flex($values){
	-webkit-box-flex: $values;
	-moz-box-flex:  $values;
	-webkit-flex:  $values;
	-ms-flex:  $values;
	flex:  $values;
}
</pre>
<em>Usage:</em>
<pre>.flex{ @include flex(0 0 auto); }</pre>
<h3><strong>Justify Content</strong></h3>
<em>Mixin:</em>
<pre>
$value: flex-start | flex-end | center | space-between | space-around

@mixin justify-content($value) {
	@if $value == 'flex-start'{
		-webkit-box-pack: start;
		-moz-box-pack: start;
		-webkit-justify-content: $value;
		-ms-flex-pack: start;
		justify-content: $value;
	}@else if $value == 'flex-end'{
		-webkit-box-pack: end;
		-moz-box-pack: end;
		-webkit-justify-content: $value;
		-ms-flex-pack: end;
		justify-content: $value;
	}@else if $value == 'space-between'{
		-webkit-box-pack: justify;
		-moz-box-pack: justify;
		-webkit-justify-content: $value;
		-ms-flex-pack: justify;
		justify-content: $value;
	}@else if $value == 'space-around'{
		-webkit-box-pack: justify;
		-moz-box-pack: justify;
		-webkit-justify-content: $value;
		-ms-flex-pack: distribute;
		justify-content: $value;
	}@else{
		-webkit-box-pack: $value;
		-moz-box-pack: $value;
		-webkit-justify-content: $value;
		-ms-flex-pack: $value;
		justify-content: $value;
	}
}
</pre>
<em>Usage:</em>
<pre>.justify-content{ @include justify-content(flex-start); }</pre>
<h3><strong>Align Content</strong></h3>
<em>Mixin:</em>
<pre>
$value: flex-start | flex-end | center | space-between | space-around | stretch

@mixin align-content($value){
	@if $value == 'flex-start'{
		-webkit-align-content: $value;
		-ms-flex-line-pack: start;
		align-content: $value;
	}@else if $value == 'flex-end'{
		-webkit-align-content: $value;
		-ms-flex-line-pack: start;
		align-content: $value;
	}@else if $value == 'space-between'{
		-webkit-align-content: $value;
		-ms-flex-line-pack: justify;
		align-content: $value;
	}@else if $value == 'space-around'{
		-webkit-align-content: $value;
		-ms-flex-line-pack: distribute;
		align-content: $value;
	}@else{
		-webkit-align-content: $value;
		-ms-flex-line-pack: $value;
		align-content: $value;
	}
}
</pre>
<em>Usage:</em>
<pre>.align-content{ @include align-content(flex-start); }</pre>
<h3><strong>Align Items</strong></h3>
<em>Mixin:</em>
<pre>
$value: flex-start | flex-end | center | baseline | stretch

@mixin align-items($value){
	@if $value == 'flex-start'{
		-webkit-box-align: start;
		-moz-box-align: start;
		-webkit-align-items: $value;
		-ms-flex-align: start;
		align-items: $value;
	}@else if $value == 'flex-end'{
		-webkit-box-align: end;
		-moz-box-align: end;
		-webkit-align-items: $value;
		-ms-flex-align: end;
		align-items: $value;
	}@else{
		-webkit-box-align: $value;
		-moz-box-align: $value;
		-webkit-align-items: $value;
		-ms-flex-align: $value;
		align-items: $value;
	}
}
</pre>
<em>Usage:</em>
<pre>.align-items{ @include align-items(flex-start); }</pre>
<h3><strong>Align Self</strong></h3>
<em>Mixin:</em>
<pre>
$value: auto | flex-start | flex-end | center | baseline | stretch
	
@mixin align-self($value){
	@if $value == 'flex-start'{
		-webkit-align-self: $value;
		-ms-flex-item-align: start;
		align-self: $value;
	}@else if $value == 'flex-end'{
		-webkit-align-self: $value;
		-ms-flex-item-align: end;
		align-self: $value;
	}@else{
		-webkit-align-self: $value;
		-ms-flex-item-align: $value;
		align-self: $value;
	}
}
</pre>
<em>Usage:</em>
<pre>.align-self{ @include align-self(flex-start); }</pre>
