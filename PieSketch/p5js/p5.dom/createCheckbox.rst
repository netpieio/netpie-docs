.. raw:: html

	<script src="https://sketch.netpie.io/widget/p5-widget.js"></script>

createCheckbox()
================

สร้างอิลิเมนต์   ใน DOM การเรียกใช้. checked () บนเช็คบ็อกซ์จะส่งกลับถ้ามีการตรวจสอบหรือไม่

.. Creates a checkbox &lt;input&gt;&lt;/input&gt; element in the DOM.
.. Calling .checked() on a checkbox returns if it is checked or not

**รูปแบบการใช้งาน**

createCheckbox ( [label], [value] )

**พารามิเตอร์**

- ``label``  String: ป้ายกำกับที่แสดงหลังจากช่องทำเครื่องหมาย

- ``value``  boolean: ค่าของช่องทำเครื่องหมาย การตรวจสอบเป็นจริงไม่ได้เลือกเป็น false ไม่ถูกตรวจสอบหากไม่มีค่าที่ระบุ

.. ``label``  String: label displayed after checkbox
.. ``value``  boolean: value of the checkbox; checked is true, unchecked is false.Unchecked if no value given

**ค่าที่ส่งออกมา**

- Object,p5.Element: ชี้ไปที่ p5.Element ถือสร้างโหนด

.. Object,p5.Element: pointer to p5.Element holding created node

.. raw:: html

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	var checkbox;
	
	function setup() {
	  checkbox = createCheckbox('label', false);
	  checkbox.changed(myCheckedEvent);
	}
	
	function myCheckedEvent() {
	  if (this.checked()) {
	    console.log("Checking!");
	  } else {
	    console.log("Unchecking!");
	  }
	}

	</script>

	<br><br>

..  [#f1] This document was generated from p5.js whose source code is available on `github <https://github.com/processing/p5.js>`_.
