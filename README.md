# google-map-api live https://jibon87.github.io/google-map-api/

```
goole map api

1.  js--link ---> jquery.min.js


2.  html 
    {
    
        <!-- google map -->
    <div id="contact-map" style="height: 300px"></div>



    <!-- map api key -->
    <script src="https://maps.googleapis.com/maps/api/js?key=AIzaSyAVjRq4073-q8YByUcYWak3GxAyFMofc70"></script>

    }
    
3.  active js {

    function basicmap() {
        var mapOptions = {
            // How zoomed in you want the map to start at (always required)
            zoom: 11,
            scrollwheel: true,
            // The latitude and longitude to center the map (always required)
            center: new google.maps.LatLng(22.9423256, 90.8180521), // New York
            // This is where you would paste any style found on Snazzy Maps.
            styles: [
                { featureType: "all", elementType: "labels.text.fill", stylers: [{ saturation: 36 }, { color: "#000000" }, { lightness: 40 }] },
                { featureType: "all", elementType: "labels.text.stroke", stylers: [{ visibility: "on" }, { color: "#000000" }, { lightness: 16 }] },
                { featureType: "all", elementType: "labels.icon", stylers: [{ visibility: "off" }] },
                { featureType: "administrative", elementType: "geometry.fill", stylers: [{ color: "#000000" }, { lightness: 20 }] },
                { featureType: "administrative", elementType: "geometry.stroke", stylers: [{ color: "#000000" }, { lightness: 17 }, { weight: 1.2 }] },
                { featureType: "landscape", elementType: "geometry", stylers: [{ color: "#000000" }, { lightness: 20 }] },
                { featureType: "poi", elementType: "geometry", stylers: [{ color: "#000000" }, { lightness: 21 }] },
                { featureType: "road.highway", elementType: "geometry.fill", stylers: [{ color: "#000000" }, { lightness: 17 }] },
                { featureType: "road.highway", elementType: "geometry.stroke", stylers: [{ color: "#000000" }, { lightness: 29 }, { weight: 0.2 }] },
                { featureType: "road.arterial", elementType: "geometry", stylers: [{ color: "#000000" }, { lightness: 18 }] },
                { featureType: "road.local", elementType: "geometry", stylers: [{ color: "#000000" }, { lightness: 16 }] },
                { featureType: "transit", elementType: "geometry", stylers: [{ color: "#000000" }, { lightness: 19 }] },
                { featureType: "water", elementType: "geometry", stylers: [{ color: "#000000" }, { lightness: 17 }] },
            ],
        };
        // We are using a div with id="contact-map" seen below in the <body>
        var mapElement = document.getElementById("contact-map");

        // Create the Google Map using our element and options defined above
        var map = new google.maps.Map(mapElement, mapOptions);

        // Let's also add a marker while we're at it
        var marker = new google.maps.Marker({
            position: new google.maps.LatLng(22.9423256, 90.8180521),
            map: map,
            title: "Cryptox",
        });
    }

    if ($("#contact-map").length != 0) {
        google.maps.event.addDomListener(window, "load", basicmap);
    }
    
}
5.  note [ 
           set your place [ lat & lng ]
         ]
