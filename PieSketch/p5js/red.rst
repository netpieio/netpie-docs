.. raw:: html

	<script src="https://sketch.netpie.io/widget/p5-widget.js"></script>

red()
=====

แยกค่าสีแดงจากอาร์เรย์สีหรือพิกเซล

.. Extracts the red value from a color or pixel array.

**รูปแบบการใช้งาน**

red ( color )

**พารามิเตอร์**

- ``color``  p5.Color,Array: p5.Color object หรือ pixel array

.. ``color``  p5.Color,Array: p5.Color object or pixel array

**ค่าที่ส่งออกมา**

- Number: ค่าสีแดง

.. Number: the red value

.. raw:: html

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	c = color(255, 204, 0);  // Define color 'c'
	fill(c);  // Use color variable 'c' as fill color
	rect(15, 20, 35, 60);  // Draw left rectangle
	
	redValue = red(c);  // Get red in 'c'
	print(redValue);  // Print "255.0"
	fill(redValue, 0, 0);  // Use 'redValue' in new fill
	rect(50, 20, 35, 60);  // Draw right rectangle

	</script>

	<br><br>

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	
	colorMode(RGB, 255);
	var c = color(127, 255, 0);
	colorMode(RGB, 1);
	var myColor = red(c);
	print(myColor);

	</script>

	<br><br>

..  [#f1] This document was generated from p5.js whose source code is available on `github <https://github.com/processing/p5.js>`_.
