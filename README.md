# SOC Incident Report: Brute Force Attack Detection
**Analyst:** [Arivazhagan] | **Case ID:** CAS-020526-LM

---

## 1. Attack Analysis: Brute Force (SSH)
**Summary:** Identified 69 failed authentication events from IP `10.48.156.247`. Use the slider below to view the evidence. Click any image to enter **Focus Mode**.

<div style="display: flex; overflow-x: auto; gap: 20px; padding-bottom: 25px; border: 1px solid #ddd; padding: 20px; border-radius: 10px; background-color: #f9f9f9; scroll-behavior: smooth;">

  <div id="slide1" style="flex: 0 0 500px; text-align: center;">
    <p style="font-weight: bold; margin-bottom: 5px;">1. Dashboard Overview</p>
    <a href="#img1">
      <img src="BF_1.png" width="500" style="border-radius: 5px; border: 1px solid #ccc;">
    </a>
    <p><a href="#slide2">Next Slide ➔</a></p>
  </div>

  <div id="slide2" style="flex: 0 0 500px; text-align: center;">
    <p style="font-weight: bold; margin-bottom: 5px;">2. Alert Distribution</p>
    <a href="#img2">
      <img src="BF_2.png" width="500" style="border-radius: 5px; border: 1px solid #ccc;">
    </a>
    <p><a href="#slide1">⬅ Prev</a> | <a href="#slide3">Next ➔</a></p>
  </div>

  <div id="slide3" style="flex: 0 0 500px; text-align: center;">
    <p style="font-weight: bold; margin-bottom: 5px;">3. Event Detail List</p>
    <a href="#img3">
      <img src="BF_3.png" width="500" style="border-radius: 5px; border: 1px solid #ccc;">
    </a>
    <p><a href="#slide2">⬅ Prev</a> | <a href="#slide4">Next ➔</a></p>
  </div>

  <div id="slide4" style="flex: 0 0 500px; text-align: center;">
    <p style="font-weight: bold; margin-bottom: 5px;">4. Rule 5712 Stats</p>
    <a href="img5">
      <img src="BF_5.png" width="500" style="border-radius: 5px; border: 1px solid #ccc;">
    </a>
    <p><a href="#slide3">⬅ Prev</a> | <a href="#slide5">Next ➔</a></p>
  </div>

  <div id="slide5" style="flex: 0 0 500px; text-align: center;">
    <p style="font-weight: bold; margin-bottom: 5px;">5. Rule 5712 Pie Chart</p>
    <a href="#img6">
      <img src="BF_6.png" width="500" style="border-radius: 5px; border: 1px solid #ccc;">
    </a>
    <p><a href="#slide4">⬅ Prev</a> | <a href="#slide6">Next ➔</a></p>
  </div>

  <div id="slide6" style="flex: 0 0 500px; text-align: center;">
    <p style="font-weight: bold; margin-bottom: 5px;">6. Src/Dest Analysis</p>
    <a href="#img7">
      <img src="BF_7.png" width="500" style="border-radius: 5px; border: 1px solid #ccc;">
    </a>
    <p><a href="#slide5">⬅ Prev</a> | <a href="#slide7">Next ➔</a></p>
  </div>

  <div id="slide7" style="flex: 0 0 500px; text-align: center;">
    <p style="font-weight: bold; margin-bottom: 5px;">7. Attacker IP Filter</p>
    <a href="#img8">
      <img src="BF_8.png" width="500" style="border-radius: 5px; border: 1px solid #ccc;">
    </a>
    <p><a href="#slide6">⬅ Prev</a></p>
  </div>

</div>

---

## 2. Focus Mode (Full Resolution Gallery)
*Click the thumbnails in the slider above to jump to the full-size view below.*

<div id="img1" style="margin-top: 50px; text-align: center;">
  <h3>1. Dashboard Overview</h3>
  <img src="BF_1.png" style="width: 100%; max-width: 1000px;">
  <p><a href="#slide1">Back to Slider ↑</a> | <a href="#img2">Next Image ↓</a></p>
</div>

<div id="img2" style="margin-top: 100px; text-align: center;">
  <h3>2. Alert Distribution</h3>
  <img src="BF_2.png" style="width: 100%; max-width: 1000px;">
  <p><a href="#img1">↑ Previous</a> | <a href="#slide2">Back to Slider ↑</a> | <a href="#img3">Next Image ↓</a></p>
</div>

<div id="img3" style="margin-top: 100px; text-align: center;">
  <h3>3. Event Detail List</h3>
  <img src="BF_3.png" style="width: 100%; max-width: 1000px;">
  <p><a href="#img2">↑ Previous</a> | <a href="#slide3">Back to Slider ↑</a> | <a href="#img4">Next Image ↓</a></p>
</div>

<div id="img4" style="margin-top: 100px; text-align: center;">
  <h3>4. Rule 5712 Stats</h3>
  <img src="BF_5.png" style="width: 100%; max-width: 1000px;">
  <p><a href="#img3">↑ Previous</a> | <a href="#slide4">Back to Slider ↑</a> | <a href="#img5">Next Image ↓</a></p>
</div>

<div id="img5" style="margin-top: 100px; text-align: center;">
  <h3>5. Rule 5712 Pie Chart</h3>
  <img src="BF_6.png" style="width: 100%; max-width: 1000px;">
  <p><a href="#img4">↑ Previous</a> | <a href="#slide5">Back to Slider ↑</a> | <a href="#img6">Next Image ↓</a></p>
</div>

<div id="img6" style="margin-top: 100px; text-align: center;">
  <h3>6. Src/Dest Analysis</h3>
  <img src="BF_7.png" style="width: 100%; max-width: 1000px;">
  <p><a href="#img5">↑ Previous</a> | <a href="#slide6">Back to Slider ↑</a> | <a href="#img7">Next Image ↓</a></p>
</div>

<div id="img7" style="margin-top: 100px; text-align: center;">
  <h3>7. Attacker IP Filter</h3>
  <img src="BF_8.png" style="width: 100%; max-width: 1000px;">
  <p><a href="#img6">↑ Previous</a> | <a href="#slide7">Back to Slider ↑</a></p>
</div>
