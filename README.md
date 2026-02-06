<style>
/* The Modal (background) */
.modal {
  display: none;
  position: fixed;
  z-index: 9999;
  padding-top: 50px;
  left: 0; top: 0;
  width: 100%; height: 100%;
  background-color: rgba(0,0,0,0.9);
  backdrop-filter: blur(5px);
}

/* Modal Content (Image) */
.modal-content {
  margin: auto;
  display: block;
  max-width: 85%;
  max-height: 80vh;
  border: 3px solid white;
}

/* Caption Text */
#caption {
  margin: auto;
  display: block;
  width: 80%;
  text-align: center;
  color: #ccc;
  padding: 10px 0;
  font-size: 20px;
}

/* The Close Button */
.close {
  position: absolute;
  top: 15px; right: 35px;
  color: #f1f1f1;
  font-size: 40px;
  font-weight: bold;
  cursor: pointer;
}

.gallery-container {
  display: flex;
  overflow-x: auto;
  gap: 15px;
  padding: 20px;
  background: #f4f4f4;
  border-radius: 8px;
}

.gallery-item {
  flex: 0 0 300px;
  cursor: pointer;
  transition: 0.3s;
}

.gallery-item:hover {opacity: 0.7;}
</style>
