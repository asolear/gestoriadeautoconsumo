---
hide:
  - navigation
  - toc
---

 

<link rel="stylesheet" href="https://unpkg.com/leaflet@1.9.4/dist/leaflet.css"
    integrity="sha256-p4NxAoJBhIIN+hmNHrzRCf9tD/miZyoHS5obTRR9BMY=" crossorigin="" />
<script src="https://unpkg.com/leaflet@1.9.4/dist/leaflet.js"
    integrity="sha256-20nQCchB9co0qIjJZRGuk2/Z9VM+kNiyxNV1lvTlZBo=" crossorigin=""></script>



<label>Indique su Ubicación</label>
<div id="map" style="width: 100%; height: 200px;"></div>


<form action="mailto:info@wattbucket.com?subject=QR " method="post"enctype="text/plain">

<input type="hidden" name='latitud' class="form-control" id="lat" value="40.41630407781033">
    
    
<input type="hidden" name='longitud' class="form-control" id="lng" value="-3.703777670925774">                    
    
    


 <textarea id="Factura" name="factura" style="width: 100%; height: 4vh;" placeholder="Ultima Factura de luz (€)"></textarea>
 <br> 
 <textarea id="Nombre" name="nombre" style="width: 100%; height: 4vh;" placeholder="Nombre"></textarea>
 <br> 
 <textarea id="Telefono" name="telefono" style="width: 100%; height: 4vh;" placeholder="Telefono"></textarea>
 <br> 
<textarea id="Mensaje" name="mensaje" style="width: 100%; height: 10vh;"  placeholder="Mensaje"></textarea><br>

<input type="file" name="archivo">
<br><br><label><input type="checkbox" class="agree" required> Acepto la Política de  Privacidad
</label><br>
    <input type="submit" style="width:100%;height: 60px;background-color: #4CAF50"
    value="✉️ eMAIL"><br>
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


<style> 
body { 
  background-image: url('https://github.com/asolear/assets/blob/master/imgs/fondo3.jpg?raw=true'); 
  background-repeat: no-repeat; 
  background-attachment: fixed; /* background-size: cover; */ 
  background-size: 100% 100%;
   } 
</style>      