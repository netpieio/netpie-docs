.. raw:: html

	<script src="https://sketch.netpie.io/widget/p5-widget.js"></script>

minute()
========

p5.js สื่อสารกับนาฬิกาบนคอมพิวเตอร์ของคุณ ฟังก์ชัน minute () จะคืนค่านาทีปัจจุบันเป็นค่าตั้งแต่ 0 ถึง 59

.. p5.js communicates with the clock on your computer. The minute() function
.. returns the current minute as a value from 0 - 59.

**รูปแบบการใช้งาน**

minute ( )

**ค่าที่ส่งออกมา**

- Number: นาทีปัจจุบัน

.. Number: the current minute

.. raw:: html

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	var m = minute();
	text("Current minute: \n" + m, 5, 50);

	</script>

	<br><br>

..  [#f1] This document was generated from p5.js whose source code is available on `github <https://github.com/processing/p5.js>`_.
