.. raw:: html

	<script src="https://sketch.netpie.io/widget/p5-widget.js"></script>

createButton()
==============

สร้างอิลิเมนต์   ใน DOM ใช้ขนาด. () เพื่อกำหนดขนาดการแสดงผลของปุ่ม ใช้. mousePressed () เพื่อระบุพฤติกรรมในการกด ผนวกเข้ากับโหนดคอนเทนเนอร์หากมีการระบุไว้มิฉะนั้นจะต่อท้ายกับเนื้อหา

.. Creates a &lt;button&gt;&lt;/button&gt; element in the DOM.
.. Use .size() to set the display size of the button.
.. Use .mousePressed() to specify behavior on press.
.. Appends to the container node if one is specified, otherwise
.. appends to body.

**รูปแบบการใช้งาน**

createButton ( label, [value] )

**พารามิเตอร์**

- ``label``  String: ฉลากที่แสดงบนปุ่ม

- ``value``  String: ค่าของปุ่ม

.. ``label``  String: label displayed on the button
.. ``value``  String: value of the button

**ค่าที่ส่งออกมา**

- Object,p5.Element: ชี้ไปที่ p5.Element ถือสร้างโหนด

.. Object,p5.Element: pointer to p5.Element holding created node

.. raw:: html

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	var button;
	function setup() {
	  createCanvas(100, 100);
	  background(0);
	  button = createButton('click me');
	  button.position(19, 19);
	  button.mousePressed(changeBG);
	}
	
	function changeBG() {
	  var val = random(255);
	  background(val);
	}

	</script>

	<br><br>

..  [#f1] This document was generated from p5.js whose source code is available on `github <https://github.com/processing/p5.js>`_.
