#PEERS-0 &ndash; Character Placement

This standard covers the general syntax to be used, including indentation, new line
placement, spaghetti code, and delimiters. This standard briefly touches base on
child languages; however, any such information that conflicts with another standard
standard, that is paired with this standard is overwritten.

[Definitions]()

####Table of Contents
- [0.1 Indentation]()
- [0.2 Spaces and New Lines]()
- [0.3 Delimiters]()
- [0.4 Spaghetti Code]()

##0.1 Indentation

[See the full documentation for 0.1]()

In PHP blocks, all code MUST BE in tabs, except in the case of a Heredoc or a Nowdoc;
in which case the inentation SHOULD BE reset to zero and follow the indentation of
that child language, for the duration of the Heredoc/Nowdoc.

If the PHP block is embedded in another language, such as HTML, then the PHP block
should be initially indented to the current indentation level.

PHP open &amp; close tags MUST NOT count towards indentation. The PHP open tag MUST
BE immediately followed with a new line, except when the total length of the PHP
block is less than 50 characters. In this case the entire PHP block MAY BE put on
one line.

In any case where there is a opening curly bracket (`{`), it MUST BE immediately
followed with a new line and the indentation level increased by 1. In any case where
there is a closing curly bracket (`}`), it MUST BE prefixed with a new line and the
indentation level decreased by 1. The only exception is when the total length of
the control directive (such as `while`, `foreach`, and `if`), including curly braces
and spaces, is less than 80 characters; in this case, the entire control directive
MAY BE on one line.

####Example:

```PHP

<?php
if ($is_home) {
	do_something();
} else {
	do_something_else();
}
?><!DOCTYPE html>

...

<div class="some-class">
	<h3><?php the_title(); ?></h3>
	<?php
	the_content();
	
	if ($text) {
		do_some_stuff();
		$lorem = <<<str
Lorem ipsum dolor sit amet, consectetur adipisicing elit.
str;
		read_more();
	}
	
	?>
</div>

```
