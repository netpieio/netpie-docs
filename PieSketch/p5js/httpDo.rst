.. raw:: html

	<script src="https://sketch.netpie.io/widget/p5-widget.js"></script>

httpDo()
========

วิธีการดำเนินการคำร้องขอ HTTP หากไม่มีการระบุชนิดข้อมูล p5 จะพยายามคาดเดาตาม URL ซึ่งเป็นค่าเริ่มต้นเป็นข้อความ 
สำหรับการใช้งานขั้นสูงคุณอาจผ่านในเส้นทางเป็นอาร์กิวเมนต์แรกและวัตถุเป็นอาร์กิวเมนต์ที่สองลายเซ็นต่อไปนี้ตามที่ระบุในข้อกำหนดของ Fetch API

.. Method for executing an HTTP request. If data type is not specified,
.. p5 will try to guess based on the URL, defaulting to text.
.. 
.. For more advanced use, you may also pass in the path as the first argument
.. and a object as the second argument, the signature follows the one specified
.. in the Fetch API specification.

**รูปแบบการใช้งาน**

httpDo ( path, [method], [datatype], [data], [callback], [errorCallback] )

**พารามิเตอร์**

- ``path``  String: ชื่อไฟล์หรือ URL ที่จะโหลด

- ``method``  String: &quot;GET&quot;, &quot;POST&quot; หรือ &quot;PUT&quot; ค่าเริ่มต้นคือ &quot;GET&quot;

- ``datatype``  String: &quot;json&quot;, &quot;jsonp&quot;, &quot;xml&quot; หรือ &quot;ข้อความ&quot;

- ``data``  Object: ข้อมูล param ที่ส่งมาพร้อมกับคำขอ

- ``callback``  function: ฟังก์ชันที่จะดำเนินการหลังจาก httpget () เสร็จสมบูรณ์แล้วข้อมูลจะถูกส่งผ่านเป็นอาร์กิวเมนต์แรก

- ``errorCallback``  function: ฟังก์ชันที่จะดำเนินการถ้ามีข้อผิดพลาดการตอบสนองจะถูกส่งผ่านเป็นอาร์กิวเมนต์แรก

.. ``path``  String: name of the file or url to load
.. ``method``  String: either "GET", "POST", or "PUT", defaults to "GET"
.. ``datatype``  String: "json", "jsonp", "xml", or "text"
.. ``data``  Object: param data passed sent with request
.. ``callback``  function: function to be executed after httpGet() completes, data is passed in as first argument
.. ``errorCallback``  function: function to be executed if there is an error, response is passed in as first argument

.. raw:: html

	<script type="text/p5" data-autoplay data-hide-sourcecode>
	// Examples use USGS Earthquake API:
	// https://earthquake.usgs.gov/fdsnws/event/1/#methods
	
	// displays an animation of all USGS earthquakes
	var earthquakes;
	var eqFeatureIndex = 0;
	
	function preload() {
	   var url = 'https://earthquake.usgs.gov/fdsnws/event/1/query?format=geojson';
	   httpDo(url,
	     {
	       method: 'GET',
	       // Other Request options, like special headers for apis
	       headers: { authorization: 'Bearer secretKey' }
	     },
	     function(res) {
	       earthquakes = res;
	     });
	}
	
	function draw() {
	   // wait until the data is loaded
	   if (!earthquakes || !earthquakes.features[eqFeatureIndex]) {
	     return;
	   }
	   clear();
	
	   var feature = earthquakes.features[eqFeatureIndex];
	   var mag = feature.properties.mag;
	   var rad = mag / 11 * ((width + height) / 2);
	   fill(255, 0, 0, 100);
	   ellipse(
	     width / 2 + random(-2, 2),
	     height / 2 + random(-2, 2),
	     rad, rad
	   );
	
	   if (eqFeatureIndex >= earthquakes.features.length) {
	     eqFeatureIndex = 0;
	   } else {
	     eqFeatureIndex += 1;
	   }
	}

	</script>

	<br><br>

..  [#f1] This document was generated from p5.js whose source code is available on `github <https://github.com/processing/p5.js>`_.
