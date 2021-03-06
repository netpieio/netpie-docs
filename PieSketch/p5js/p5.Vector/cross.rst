.. raw:: html

	<script src="https://sketch.netpie.io/widget/p5-widget.js"></script>

cross()
=======

คำนวณและส่งกลับเวกเตอร์ประกอบด้วยผลิตภัณฑ์ข้ามระหว่างสองเวกเตอร์ ทั้งแบบคงที่และแบบไม่คงที่จะส่งกลับค่า p5.Vector ใหม่ ดูตัวอย่างสำหรับบริบทเพิ่มเติม

.. Calculates and returns a vector composed of the cross product between
.. two vectors. Both the static and non static methods return a new p5.Vector.
.. See the examples for more context.

**รูปแบบการใช้งาน**

cross ( v )

**พารามิเตอร์**

- ``v``  p5.Vector: p5.Vector จะข้าม

.. ``v``  p5.Vector: p5.Vector to be crossed

**ค่าที่ส่งออกมา**

- p5.Vector: p5.Vector ประกอบด้วยผลิตภัณฑ์ข้าม

.. p5.Vector: p5.Vector composed of cross product

.. raw:: html

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	var v1 = createVector(1, 2, 3);
	var v2 = createVector(1, 2, 3);
	
	v1.cross(v2); // v's components are [0, 0, 0]

	</script>

	<br><br>

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	
	// Static method
	var v1 = createVector(1, 0, 0);
	var v2 = createVector(0, 1, 0);
	
	var crossProduct = p5.Vector.cross(v1, v2);
	// crossProduct has components [0, 0, 1]

	</script>

	<br><br>

..  [#f1] This document was generated from p5.js whose source code is available on `github <https://github.com/processing/p5.js>`_.
