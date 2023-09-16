---
hide:
  - navigation
  - toc
---
                
<style>
    body { 
    background-image: url('https://github.com/asolear/assets/blob/master/imgs/fondo3.jpg?raw=true'); 
    background-repeat: no-repeat; 
    background-attachment: fixed; /* background-size: cover; */ 
    background-size: 100% 100%;
    } 
    .container {
        max-width: 400px;
        margin: 0 auto;
        padding: 20px;
    }
    label {
        display: block;
        margin-bottom: 5px;
    }
    input[type="text"],
    input[type="email"],
    textarea {
        width: 100%;
        padding: 10px;
        margin-bottom: 10px;
        border: 1px solid #ccc;
        border-radius: 5px;
    }
    input[type="submit"] {
        background-color: #007bff;
        color: #fff;
        padding: 10px 20px;
        border: none;
        border-radius: 5px;
        cursor: pointer;
    }
    input[type="submit"]:hover {
        background-color: #0056b3;
    }
</style>

<script>

    var map = L.map('map').setView([40.41630407781033, -3.703777670925774], 13);

    var tiles = L.tileLayer('https://tile.openstreetmap.org/{z}/{x}/{y}.png', {
        attribution: '&copy; <a href="http://www.openstreetmap.org/copyright">OpenStreetMap</a>'
    }).addTo(map);
    var marker = L.marker([40.41630407781033, -3.703777670925774]).addTo(map).openPopup();
    map.on('click', function (e) {
        if (marker) {
            map.removeLayer(marker);
        }
        marker = new L.Marker(e.latlng).addTo(map).openPopup();
        document.getElementById('lat').value = e.latlng.lat;
        document.getElementById('lng').value = e.latlng.lng;
    });
</script>


<div class="container">
  <h1>FormSubmit Demo</h1>
  <form target="_blank" action="https://formsubmit.co/pacoromangamez@gmail.com" method="POST">
    <div class="form-group">
      <div class="form-row">
        <div class="col">
          <input type="text" name="name" class="form-control" placeholder="Full Name" required>
        </div>
        <div class="col">
          <input type="email" name="email" class="form-control" placeholder="Email Address" required>
        </div>
      </div>
    </div>
    <div class="form-group">
      <textarea placeholder="Your Message" class="form-control" name="message" rows="10" required></textarea>
    </div>
    <button type="submit" class="btn btn-lg btn-dark btn-block">Submit Form</button>
  </form>
</div>              

