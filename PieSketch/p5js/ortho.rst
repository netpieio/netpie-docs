.. raw:: html

	<script src="https://sketch.netpie.io/widget/p5-widget.js"></script>

ortho()
=======

ตั้งกล้อง ortho

.. Setup ortho camera

**รูปแบบการใช้งาน**

ortho ( left, right, bottom, top, near, far )

**พารามิเตอร์**

- ``left``  Number: กล้องด้านซ้ายของเครื่องบิน

- ``right``  Number: กล้อง frustum right plane

- ``bottom``  Number: กล้องด้านล่างเป็นวงโคจร

- ``top``  Number: กล้องบนเครื่องบินโครเมี่ยม

- ``near``  Number: กล้อง frustum ใกล้ระนาบ

- ``far``  Number: กล้องเครื่องบินไกล

.. ``left``  Number: camera frustum left plane
.. ``right``  Number: camera frustum right plane
.. ``bottom``  Number: camera frustum bottom plane
.. ``top``  Number: camera frustum top plane
.. ``near``  Number: camera frustum near plane
.. ``far``  Number: camera frustum far plane

**ค่าที่ส่งออกมา**

- p5: วัตถุ p5

.. p5: the p5 object

.. raw:: html

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	//drag mouse to toggle the world!
	//there's no vanish point
	function setup(){
	  createCanvas(100, 100, WEBGL);
	  ortho(-width/2, width/2, height/2, -height/2, 0, 500);
	}
	function draw(){
	 background(200);
	 orbitControl();
	 for(var i = -1; i < 2; i++){
	    for(var j = -2; j < 3; j++){
	      push();
	      translate(i*160, 0, j*160);
	      box(40, 40, 40);
	      pop();
	    }
	  }
	}

	</script>

	<br><br>

..  [#f1] This document was generated from p5.js whose source code is available on `github <https://github.com/processing/p5.js>`_.
