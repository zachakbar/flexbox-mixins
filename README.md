# SCSS Flexbox Mixins
These mixins include the broswer specific fallbacks for flexbox.

<h3><a href="http://www.w3schools.com/cssref/css3_pr_flexbox.asp" target="_blank"><strong>Flexbox</strong></a></h3>
<em>Mixin:</em>
<pre>
// no value needed

@mixin flexbox() {
	display: -ms-flexbox;
	display: -webkit-flex;
	display: flex;
}
</pre>
<em>Usage:</em>
<pre>.example-class{ @include flexbox(); }</pre>
<h3><a href="http://www.w3schools.com/cssref/css3_pr_flex-wrap.asp" target="_blank"><strong>Flex Wrap</strong></a></h3>
<em>Mixin:</em>
<pre>
$value: nowrap|wrap|wrap-reverse|initial|inherit

@mixin flex-wrap($value){
	-ms-flex-wrap: $value;
	-webkit-flex-wrap: $value;
	flex-wrap: $value;
}
</pre>
<em>Usage:</em>
<pre>.example-class{ @include flex-wrap(wrap); }</pre>
<h3><a href="http://www.w3schools.com/cssref/css3_pr_flex.asp" target="_blank"><strong>Flex</strong></a></h3>
This is shorthand for flex-grow, flex-shrink and optionally flex-basis. Space separated, in that order.
<em>Mixin:</em>
<pre>
$values: flex-grow flex-shrink flex-basis |auto|initial|inherit

@mixin flex($values){
	-ms-flex:  $values;
	-webkit-flex:  $values;
	flex:  $values;
}
</pre>
<em>Usage:</em>
<pre>
.example-class-1{ @include flex(1); }
.example-class-2{ @include flex(0 0 auto); }
</pre>
<h3><a href="http://www.w3schools.com/cssref/css3_pr_justify-content.asp" target="_blank"><strong>Justify Content</strong></a></h3>
<em>Mixin:</em>
<pre>
$value: flex-start|flex-end|center|space-between|space-around|initial|inherit

@mixin flex-justify-content($value) {
	@if $value == 'flex-start'{
		-ms-flex-pack: start;
		-webkit-justify-content: $value;
		justify-content: $value;
	}@else if $value == 'flex-end'{
		-ms-flex-pack: end;
		-webkit-justify-content: $value;
		justify-content: $value;
	}@else if $value == 'space-between'{
		-ms-flex-pack: justify;
		-webkit-justify-content: $value;
		justify-content: $value;
	}@else if $value == 'space-around'{
		-ms-flex-pack: distribute;
		-webkit-justify-content: $value;
		justify-content: $value;
	}@else{
		-ms-flex-pack: $value;
		-webkit-justify-content: $value;
		justify-content: $value;
	}
}
</pre>
<em>Usage:</em>
<pre>.example-class{ @include align-content(flex-start); }</pre>
<h3><a href="http://www.w3schools.com/cssref/css3_pr_align-items.asp" target="_blank"><strong>Align Items</strong></a></h3>
<em>Mixin:</em>
<pre>
$value: stretch|center|flex-start|flex-end|space-between|space-around|initial|inherit

@mixin flex-align-items($value){
	@if $value == 'flex-start'{
		-ms-flex-align: start;
		-webkit-align-items: $value;
		align-items: $value;
	}@else if $value == 'flex-end'{
		-ms-flex-align: end;
		-webkit-align-items: $value;
		align-items: $value;
	}@else{
		-ms-flex-align: $value;
		-webkit-align-items: $value;
		align-items: $value;
	}
}
</pre>
<em>Usage:</em>
<pre>.example-class{ @include justify-content(flex-start); }</pre>
<h3><a href="http://www.w3schools.com/cssref/css3_pr_align-content.asp" target="_blank"><strong>Align Content</strong></a></h3>
<em>Mixin:</em>
<pre>
$value: stretch|center|flex-start|flex-end|space-between|space-around|initial|inherit

@mixin flex-align-content($value){
	@if $value == 'flex-start'{
		-ms-flex-line-pack: start;
		-webkit-align-content: $value;
		align-content: $value;
	}@else if $value == 'flex-end'{
		-ms-flex-line-pack: end;
		-webkit-align-content: $value;
		align-content: $value;
	}@else if $value == 'space-between'{
		-ms-flex-line-pack: justify;
		-webkit-align-content: $value;
		align-content: $value;
	}@else if $value == 'space-around'{
		-ms-flex-line-pack: distribute;
		-webkit-align-content: $value;
		align-content: $value;
	}@else{
		-ms-flex-line-pack: $value;
		-webkit-align-content: $value;
		align-content: $value;
	}
}
</pre>
<em>Usage:</em>
<pre>.example-class{ @include align-items(flex-start); }</pre>
<h3><a href="http://www.w3schools.com/cssref/css3_pr_align-self.asp" target="_blank"><strong>Align Self</strong></a></h3>
<em>Mixin:</em>
<pre>
$value: auto|stretch|center|flex-start|flex-end|baseline|initial|inherit
	
@mixin flex-align-self($value){
	@if $value == 'flex-start'{
		-ms-flex-item-align: start;
		-webkit-align-self: $value;
		align-self: $value;
	}@else if $value == 'flex-end'{
		-ms-flex-item-align: end;
		-webkit-align-self: $value;
		align-self: $value;
	}@else{
		-ms-flex-item-align: $value;
		-webkit-align-self: $value;
		align-self: $value;
	}
}
</pre>
<em>Usage:</em>
<pre>.example-class{ @include align-self(flex-start); }</pre>

Suggestions are welcome and appreciated.

Thanks,

~Z
