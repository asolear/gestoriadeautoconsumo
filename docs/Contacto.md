---
hide:
  - navigation
  - toc
---
<style>
    body {
        font-family: Arial, sans-serif;
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


<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"
    integrity="sha256-p4NxAoJBhIIN+hmNHrzRCf9tD/miZyoHS5obTRR9BMY=" crossorigin="" />
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"
    integrity="sha256-20nQCchB9co0qIjJZRGuk2/Z9VM+kNiyxNV1lvTlZBo=" crossorigin=""></script>



<label>Indique su Ubicación</label>
<div id="map" style="width: 100%; height: 200px;"></div>


<form action="mailto:info@wattbucket.com?subject=QR " method="post" enctype="text/plain">
    <input type="hidden" name='latitud' class="form-control" id="lat" value="40.41630407781033">
    <input type="hidden" name='longitud' class="form-control" id="lng" value="-3.703777670925774">
    <textarea id="Factura" name="factura" 
        placeholder="Ultima Factura de luz (€)"></textarea>
    <br>
    <textarea id="Nombre" name="nombre" placeholder="Nombre"></textarea>
    <br>
    <textarea id="Telefono" name="telefono" placeholder="Telefono"></textarea>
    <br>
    <textarea id="Mensaje" name="mensaje" placeholder="Mensaje"></textarea><br>
    <input type="file" name="archivo">
    <br><br><label><input type="checkbox" class="agree" required> Acepto la Política de Privacidad
    </label><br>
    <input type="submit" value="✉️ eMAIL"><br>
</form>

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


