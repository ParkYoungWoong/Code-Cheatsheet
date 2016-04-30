#Google Maps Sample

#### HTML
~~~~
<div id="google_map"></div>
~~~~

#### CSS
~~~~
#google_map {
    width: 500px;
    height: 500px;
}
~~~~

#### JS
~~~~
$(function () {

    google.maps.event.addDomListener(window, 'load', initMap);
    function initMap() {
        var map = new google.maps.Map(document.getElementById('google_map'), {
            center: {lat: 37.510494, lng: 127.042179},
            zoom: 14,
            minZoom: 10
        });
        var marker = new google.maps.Marker({
            position: new google.maps.LatLng(37.510494, 127.042179),
            map: map,
            title: '디자인나스 강남점!'
        });
    }

});
~~~~
