<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Google Maps - Dibujar Polígono</title>
    <style>
        #map, #map-validar {
            width: 48%;
            height: 500px;
            display: inline-block;
        }
        #controls {
            margin-top: 10px;
            display: flex;
            flex-direction: column;
            max-width: 400px;
        }
        #coordenadas {
            margin-top: 10px;
            padding: 10px;
            background: #f4f4f4;
            border: 1px solid #ccc;
            font-family: monospace;
            white-space: pre-wrap;
        }
    </style>
    <script src="https://unpkg.com/sweetalert/dist/sweetalert.min.js"></script>

    
    <script async defer src="https://maps.googleapis.com/maps/api/js?key=AIzaSyAAQSjDblw3qjzm_kUAsiUS5YEtU0BqE9o&libraries=drawing,geometry&callback=initMap"></script>
</head>
<body>
    <table border="0">
        <tr>
            <td style="width: 50%;">
                <h2>Dibujar un polígono y validar coordenadas</h2>
                <div id="map" style="width: 100%; height: 300px"></div>
            </td>
            <td style="width: 50%;">
                <h3>Mapa de validación (Haz clic en el mapa para validar coordenadas)</h3>
                <div id="map-validar" style="width: 100%; height: 300px"></div>
            </td>
        </tr>
    </table>

    <div id="controls">
        <p id="resultado"></p>
    </div>

    <h3>Coordenadas del Polígono:</h3>
    <div id="coordenadas">Aún no se ha dibujado un polígono.</div>

    <script>
        let map, mapValidar, drawingManager, poligono = null;

        window.initMap = function() {
            // Mapa principal
            map = new google.maps.Map(document.getElementById("map"), {
                center: { lat: -33.4489, lng: -70.6693 },
                zoom: 13,
            });

            // Mapa para validar coordenadas
            mapValidar = new google.maps.Map(document.getElementById("map-validar"), {
                center: { lat: -33.4489, lng: -70.6693 },
                zoom: 13,
            });

            drawingManager = new google.maps.drawing.DrawingManager({
                drawingMode: google.maps.drawing.OverlayType.POLYGON,
                drawingControl: true,
                drawingControlOptions: {
                    position: google.maps.ControlPosition.TOP_CENTER,
                    drawingModes: ["polygon"]
                },
                polygonOptions: {
                    strokeColor: "#FF0000",
                    strokeOpacity: 0.8,
                    strokeWeight: 2,
                    fillColor: "#FF0000",
                    fillOpacity: 0.35,
                }
            });

            drawingManager.setMap(map);

            // Evento para dibujar polígono
            google.maps.event.addListener(drawingManager, "overlaycomplete", function(event) {
                if (event.type === google.maps.drawing.OverlayType.POLYGON) {
                    if (poligono) {
                        poligono.setMap(null);
                    }
                    poligono = event.overlay;
                    mostrarCoordenadas(poligono);
                }
            });

            // Evento para obtener coordenadas al hacer clic en el mapa de validación
            google.maps.event.addListener(mapValidar, 'click', function(event) {
                const lat = event.latLng.lat();
                const lng = event.latLng.lng();
                validarCoordenada(lat, lng);
            });
        };

        // Mostrar las coordenadas del polígono
        function mostrarCoordenadas(poligono) {
            const path = poligono.getPath();
            const coordenadasArray = [];

            for (let i = 0; i < path.getLength(); i++) {
                const latLng = path.getAt(i);
                coordenadasArray.push({ lat: latLng.lat(), lng: latLng.lng() });
            }

            document.getElementById("coordenadas").textContent = JSON.stringify(coordenadasArray, null, 2);
        }

        // Validar coordenada seleccionada en el mapa de validación
        function validarCoordenada(lat, lng) {
            if (!poligono) {
                document.getElementById("resultado").innerText = "⚠️ Primero dibuja un polígono en el mapa.";
                return;
            }

            const punto = new google.maps.LatLng(lat, lng);
            const dentro = google.maps.geometry.poly.containsLocation(punto, poligono);

            if(dentro){
                swal("","La coordenada ESTÁ dentro del polígono","success");
            } else {
                swal("","La coordenada NO ESTÁ dentro del polígono","error");
            }

        }
    </script>
</body>
</html>
