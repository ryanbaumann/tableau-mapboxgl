
<html>

<head>
    <meta charset='utf-8' />
    <title>Mapbox GL in a Tableau Dashboard</title>
    <meta name='viewport' content='width=device-width, initial-scale=1'>
    <link href='https://api.tiles.mapbox.com/mapbox-gl-js/v0.28.0/mapbox-gl.css' rel='stylesheet' />
    <link href='https://www.mapbox.com/base/latest/base.css' rel='stylesheet' />
    <script src="https://code.jquery.com/jquery-2.2.4.min.js" integrity="sha256-BbhdlvQf/xTY9gja0Dq3HiwQF8LaCRTXxZKRutelT44=" crossorigin="anonymous"></script>
</head>
<style>
body {
    margin: 0;
    padding: 0;
    background-color: black;
    overflow-x: hidden;
}

.left {
    float: left;
    width: 40%;
}

.middle {
    float: center;
    margin: 5px;
}

.right {
    float: left;
    width: 30%;
}

#map {
    position: relative;
    width: 100%;
    height: 307px;
    overflow-y: hidden;
}

#container {
    width: 100%;
    height: 100%;
}

#tableauViz1 {
    background-color: black;
    width: 100%;
    height: 325px;
    margin: auto;
    overflow-y: hidden;
}

#tableauViz2 {
    background-color: black;
    width: 100%;
    height: 325px;
    margin: auto;
    overflow-y: hidden;
}

#tableauViz3 {
    background-color: black;
    width: 100%;
    height: 325px;
    margin: auto;
    overflow-y: hidden;
}


/*  SECTIONS  */

.section {
    clear: both;
}


/*  COLUMN SETUP  */

.col {
    display: block;
    float: left;
}

.col:first-child {
    margin-left: 0;
}


/*  GROUPING  */

.group:before,
.group:after {
    content: '';
    display: table;
}

.group:after {
    clear: both;
}

.group {
    zoom: 1;
    /* For IE 6/7 */
}


/*  GRID OF THREE  */

.span_1_of_3 {
    width: 33.33%;
}

.span_2_of_3 {
    width: 50%;
}

.span_3_of_3 {
    width: 100%;
}


/*  GO FULL WIDTH BELOW 480 PIXELS */

@media only screen and (max-width: 520px) {
    .col {
        /*margin: 1% 0 1% 0%;*/
    }
    .span_3_of_3,
    .span_2_of_3,
    .span_1_of_3 {
        width: 100%;
    }
}

.navbar-inverse {
    position: relative;
}


/* Dark attribution */

.mapboxgl-ctrl.mapboxgl-ctrl-attrib {
    background: rgba(0, 0, 0, .8);
}

.mapboxgl-ctrl.mapboxgl-ctrl-attrib a {
    color: #fff;
}

.map-overlay {
    width: 165px;
    top: 5px;
    padding: 5px;
    z-index: 1;
}

.map-overlay .map-overlay-inner {
    background: rgba(0, 0, 0, .8);
    color: #fff;
    box-shadow: 0 1px 2px rgba(0, 0, 0, 0.10);
    border-radius: 3px;
    padding: 5px;
    margin-bottom: 10px;
    z-index: 1;
}

.map-overlay-inner fieldset {
    border: none;
    padding: 0;
    margin: 0 0 10px;
    z-index: 1;
}


/* Dark popup */

.mapboxgl-popup-content {
    background-color: #202020;
    color: #fff;
    margin-left: 2px;
    margin-top: 2px;
    margin-bottom: 2px;
    margin-right: 2px;
    z-index: 10000;
}

.mapboxgl-popup-anchor-bottom-left .mapboxgl-popup-tip,
.mapboxgl-popup-anchor-bottom-right .mapboxgl-popup-tip,
.mapboxgl-popup-anchor-bottom .mapboxgl-popup-tip {
    border-top-color: #202020;
}

.mapboxgl-popup-anchor-top-left .mapboxgl-popup-tip,
.mapboxgl-popup-anchor-top-right .mapboxgl-popup-tip,
.mapboxgl-popup-anchor-top .mapboxgl-popup-tip {
    border-bottom-color: #202020;
}

.mapboxgl-popup-anchor-right .mapboxgl-popup-tip {
    border-left-color: #202020;
}

.mapboxgl-popup-anchor-left .mapboxgl-popup-tip {
    border-right-color: #202020;
}

#popup-menu ul,
#menu li {
    margin: 0;
    padding: 0;
    z-index: 1000;
}

.mapboxgl-ctrl-group {
    -webkit-filter: invert(100%);
}

.loader {
    height: 100px;
    width: 20%;
    top: 200px;
    left: 200px;
    position: absolute;
    margin: 0 auto 1em;
    z-index: 9999;
    text-align: center;
}

.left-map {
    position: relative;
    bottom: 25px;
    float: left;
}

.left-map-top {
    position: absolute;
    top: 50px;
    float: left;
}

svg path,
svg rect {
    fill: #FF6700;
}
</style>

<body>
    <div id='title' class="middle">
        <h2> <a href='https://data.cityofnewyork.us/Public-Safety/NYPD-Motor-Vehicle-Collisions/h9gi-nx95' target='_blank' class="color: white;">NYC Vehicle Collisions</a> </h2>
    </div>
    <div class='container'>
        <div class='section group' id='mycontainer'>
            <div class='col span_2_of_3'>
                <div id='map'></div>
                <div class='left-map-top map-overlay'>
                    <div class='map-overlay-inner'>
                        <fieldset>
                            <label>
                                <h3>Collision Type</h3>
                            </label>
                            <div id='parameter'>
                                <select id='metric'>
                                    <option value='CYC_INJ'>Cycling Injuries</option>
                                    <option value='CYC_KIL'>Cycling Fatalities</option>
                                    <option value='PED_INJ'>Pedestrian Injuries</option>
                                    <option value='PED_KIL'>Pedestrian Fatalities</option>
                                    <option value='PER_INJ'>All Injuries</option>
                                    <option value='PER_KIL'>All Fatalities</option>
                                </select>
                            </div>
                        </fieldset>
                    </div>
                </div>
                <div class='loader loader--style1' title='0' id='loader'>
                    <svg version='1.1' id='loader-1' xmlns='http://www.w3.org/2000/svg' xmlns:xlink='http://www.w3.org/1999/xlink' x='0px' y='0px' width='40px' height='40px' viewBox='0 0 40 40' enable-background='new 0 0 40 40' xml:space='preserve'>
                        <path opacity='0.2' fill='#000' d='M20.201,5.169c-8.254,0-14.946,6.692-14.946,14.946c0,8.255,6.692,14.946,14.946,14.946
    s14.946-6.691,14.946-14.946C35.146,11.861,28.455,5.169,20.201,5.169z M20.201,31.749c-6.425,0-11.634-5.208-11.634-11.634
    c0-6.425,5.209-11.634,11.634-11.634c6.425,0,11.633,5.209,11.633,11.634C31.834,26.541,26.626,31.749,20.201,31.749z' />
                        <path fill='#000' d='M26.013,10.047l1.654-2.866c-2.198-1.272-4.743-2.012-7.466-2.012h0v3.312h0
    C22.32,8.481,24.301,9.057,26.013,10.047z'></path>
                        <animateTransform attributeType='xml' attributeName='transform' type='rotate' from='0 20 20' to='360 20 20' dur='0.5s' repeatCount='indefinite' />
                    </svg>
                </div>
                <a class='left-map' target='_blank' style='left:10px;' href='https://www.mapbox.com/'>
                    <img src='data:image/svg+xml;base64,PHN2ZyB4bWxuczpzdmc9Imh0dHA6Ly93d3cudzMub3JnLzIwMDAvc3ZnIiB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZlcnNpb249IjEuMSIgeD0iMCIgeT0iMCIgd2lkdGg9IjU5LjEiIGhlaWdodD0iMTgiIHZpZXdCb3g9IjAgMCA1OS4xIDE4IiBlbmFibGUtYmFja2dyb3VuZD0ibmV3IDAgMCA1OS4xMTkgMTgiIHhtbDpzcGFjZT0icHJlc2VydmUiPjxwYXRoIGQ9Ik0xLjQgMEMwLjYgMC4xIDAgMC44IDAgMS41TDAgMTMuNEMwIDE0LjIgMC43IDE0LjggMS41IDE0LjhMMy4zIDE0LjhDNCAxNC44IDQuNyAxNC4yIDQuOCAxMy40TDQuOCA5LjEgNS41IDEwLjNDNiAxMS4yIDcuNSAxMS4yIDggMTAuM0w4LjggOS4xIDguOCAxMy40QzguOCAxNC4xIDkuNSAxNC44IDEwLjIgMTQuOEwxMiAxNC44QzEyLjggMTQuOCAxMy41IDE0LjIgMTMuNSAxMy40TDEzLjUgMTMuMkMxNC41IDE0LjMgMTUuOSAxNSAxNy42IDE1TDIxLjcgMTUgMjEuNyAxNi41QzIxLjcgMTcuMyAyMi4zIDE4IDIzLjEgMThMMjQuOSAxOEMyNS43IDE4IDI2LjQgMTcuMyAyNi40IDE2LjVMMjYuNCAxNUMyOC4xIDE1IDI5LjUgMTQuNCAzMC41IDEzLjNMMzAuNSAxMy41QzMwLjUgMTMuOSAzMC43IDE0LjMgMzEgMTQuNiAzMS4zIDE0LjkgMzEuNiAxNSAzMiAxNUwzNS4zIDE1QzM3LjQgMTUgMzkuMiAxNCA0MC4zIDEyLjMgNDEuMyAxMy45IDQzLjEgMTUgNDUuMSAxNSA0Ni4yIDE1IDQ3LjEgMTQuOCA0Ny45IDE0LjMgNDguMiAxNC42IDQ4LjcgMTQuOCA0OS4xIDE0LjhMNTEuMyAxNC44QzUxLjcgMTQuOCA1Mi4yIDE0LjYgNTIuNSAxNC4yTDUzLjQgMTIuOSA1NC4zIDE0LjJDNTQuNiAxNC42IDU1LjEgMTQuOCA1NS41IDE0LjhMNTcuNyAxNC44QzU4LjggMTQuOCA1OS41IDEzLjQgNTguOSAxMi41TDU2LjMgOC45IDU4LjcgNS41QzU5LjQgNC42IDU4LjYgMy4xIDU3LjUgMy4xTDU1LjMgMy4xQzU0LjkgMy4xIDU0LjQgMy40IDU0LjEgMy44TDUzLjQgNC44IDUyLjcgMy44QzUyLjQgMy40IDUxLjkgMy4xIDUxLjQgMy4xTDQ5LjMgMy4xQzQ4LjggMy4xIDQ4LjMgMy40IDQ4IDMuOCA0Ny4yIDMuMyA0Ni4yIDMgNDUuMSAzIDQzLjEgMyA0MS4zIDQuMSA0MC4yIDUuNyAzOS4yIDQgMzcuNCAzIDM1LjMgM0wzNS4zIDEuNUMzNS4zIDEuMSAzNS4xIDAuNyAzNC44IDAuNCAzNC42IDAuMiAzNC4yIDAgMzMuOCAwTDMyIDBDMzEuMyAwIDMwLjUgMC44IDMwLjUgMS41TDMwLjUgNC43QzI5LjUgMy42IDI4LjEgMyAyNi41IDNMMjMuMSAzQzIyLjQgMyAyMS43IDMuNyAyMS43IDQuNUwyMS43IDQuOEMyMC42IDMuNyAxOS4yIDMgMTcuNiAzIDE1LjkgMyAxNC41IDMuNyAxMy41IDQuOEwxMy41IDEuNUMxMy41IDAuNyAxMi44IDAgMTIgMEwxMC42IDBDOS42IDAgOC40IDAuNCA3LjggMS40TDYuOCAzLjEgNS44IDEuNEM1LjEgMC40IDMuOSAwIDIuOSAwTDEuNSAwIDEuNCAwek0xLjUgMS41TDIuOSAxLjVDMy42IDEuNSA0LjIgMS43IDQuNSAyLjJMNi44IDYuMSA5IDIuMkM5LjMgMS43IDkuOSAxLjUgMTAuNiAxLjVMMTIgMS41IDEyIDEzLjUgMTAuMiAxMy41IDEwLjIgMy42IDYuOCA5LjUgMy4zIDMuNiAzLjMgMTMuNSAxLjUgMTMuNSAxLjUgMS41ek0zMi4xIDEuNUwzMy44IDEuNSAzMy44IDQuNUMzNC40IDQuNSAzNC44IDQuNSAzNS4zIDQuNSAzNy44IDQuNSAzOS43IDYuNCAzOS43IDkgMzkuNyAxMS42IDM3LjggMTMuNSAzNS4zIDEzLjVMMzIuMSAxMy41IDMyLjEgMS41ek0xNy42IDQuNUMyMCA0LjUgMjEuOCA2LjQgMjEuOCA5TDIxLjggMTMuNSAxNy42IDEzLjVDMTUuMSAxMy41IDEzLjQgMTEuNiAxMy40IDkgMTMuNCA2LjQgMTUuMSA0LjUgMTcuNiA0LjV6TTQ1LjEgNC41QzQ3LjUgNC41IDQ5LjUgNi41IDQ5LjUgOSA0OS41IDExLjUgNDcuNSAxMy41IDQ1LjEgMTMuNSA0Mi43IDEzLjUgNDAuNyAxMS41IDQwLjcgOSA0MC43IDYuNSA0Mi43IDQuNSA0NS4xIDQuNXpNMjMuMSA0LjVMMjYuNSA0LjVDMjguOSA0LjUgMzAuOCA2LjQgMzAuOCA5IDMwLjggMTEuNiAyOC45IDEzLjUgMjYuNSAxMy41TDI0LjkgMTMuNSAyNC45IDE2LjUgMjMuMSAxNi41IDIzLjEgNC41ek00OS4zIDQuNUw1MS40IDQuNSA1My40IDcuMyA1NS4zIDQuNSA1Ny41IDQuNSA1NC41IDguOSA1Ny43IDEzLjUgNTUuNSAxMy41IDUzLjQgMTAuNCA1MS4yIDEzLjUgNDkuMSAxMy41IDUyLjMgOC45IDQ5LjMgNC41ek0xNy42IDYuMkMxNi4yIDYuMiAxNS4xIDcuNCAxNS4xIDkgMTUuMSAxMC42IDE2LjIgMTEuOCAxNy42IDExLjhMMjAgMTEuOCAyMCA5QzIwIDcuNCAxOSA2LjIgMTcuNiA2LjJ6TTQ1LjEgNi4yQzQzLjcgNi4yIDQyLjUgNy41IDQyLjUgOSA0Mi41IDEwLjUgNDMuNyAxMS44IDQ1LjEgMTEuOCA0Ni42IDExLjggNDcuNyAxMC41IDQ3LjcgOSA0Ny43IDcuNSA0Ni42IDYuMiA0NS4xIDYuMnpNMjQuOSA2LjNMMjQuOSAxMS44IDI2LjUgMTEuOEMyNy45IDExLjggMjkuMSAxMC41IDI5LjEgOSAyOS4xIDcuNSAyOC4xIDYuMyAyNi41IDYuM0wyNC45IDYuM3pNMzMuOCA2LjNMMzMuOCAxMS44IDM1LjMgMTEuOEMzNi45IDExLjggMzggMTAuNSAzOCA5IDM4IDcuNSAzNi44IDYuMyAzNS4zIDYuM0wzMy44IDYuM3pNMTcuNiA3LjdDMTguMSA3LjcgMTguNSA4LjEgMTguNSA5TDE4LjUgMTAuMyAxNy42IDEwLjNDMTcgMTAuMyAxNi42IDkuOSAxNi42IDkgMTYuNiA4LjEgMTcgNy43IDE3LjYgNy43ek0yNi40IDcuN0MyNy4yIDcuNyAyNy42IDguNCAyNy42IDkgMjcuNiA5LjkgMjYuOSAxMC4zIDI2LjQgMTAuM0wyNi40IDcuN3pNMzUuMSA3LjdDMzUuOCA3LjcgMzYuNSA4LjMgMzYuNSA5IDM2LjUgOS44IDM1LjkgMTAuMyAzNS4xIDEwLjNMMzUuMSA3Ljd6TTQ1LjEgNy43QzQ1LjcgNy43IDQ2LjIgOC4yIDQ2LjIgOSA0Ni4yIDkuOCA0NS43IDEwLjMgNDUuMSAxMC4zIDQ0LjUgMTAuMyA0NCA5LjggNDQgOSA0NCA4LjIgNDQuNSA3LjcgNDUuMSA3Ljd6IiBvcGFjaXR5PSIwLjMiLz48cGF0aCBkPSJtMS41IDEuNSAwIDEyIDEuOCAwIDAtOS45IDMuNSA1LjkgMy41LTUuOSAwIDkuOSAxLjggMCAwLTEyLTEuNCAwQzkuOSAxLjUgOS4zIDEuNyA5IDIuMkw2LjggNi4xIDQuNSAyLjJDNC4yIDEuNyAzLjYgMS41IDIuOSAxLjVMMS41IDEuNVptMzAuNiAwIDAgMTIgMy4zIDBjMi40IDAgNC40LTEuOSA0LjQtNC41IDAtMi42LTEuOS00LjUtNC40LTQuNS0wLjUgMC0wLjkgMC0xLjUgMGwwLTMtMS43IDB6TTE3LjYgNC41Yy0yLjQgMC00LjIgMS45LTQuMiA0LjUgMCAyLjYgMS44IDQuNSA0LjIgNC41bDQuMiAwTDIxLjggOWMwLTIuNi0xLjctNC41LTQuMi00LjV6bTI3LjYgMGMtMi40IDAtNC40IDItNC40IDQuNSAwIDIuNSAyIDQuNSA0LjQgNC41IDIuNCAwIDQuMy0yIDQuMy00LjUgMC0yLjUtMS45LTQuNS00LjMtNC41em0tMjIgMCAwIDEyIDEuOCAwIDAtMyAxLjYgMGMyLjQgMCA0LjMtMS45IDQuMy00LjUgMC0yLjYtMS45LTQuNS00LjMtNC41bC0zLjMgMHptMjYuMiAwIDMgNC40LTMuMiA0LjYgMi4xIDAgMi4yLTMuMSAyLjEgMy4xIDIuMiAwTDU0LjUgOC45IDU3LjUgNC41IDU1LjMgNC41IDUzLjQgNy4zIDUxLjQgNC41IDQ5LjMgNC41Wk0xNy42IDYuMkMxOSA2LjIgMjAgNy40IDIwIDlsMCAyLjgtMi40IDBjLTEuNCAwLTIuNC0xLjItMi40LTIuOCAwLTEuNiAxLTIuOCAyLjQtMi44em0yNy42IDBjMS40IDAgMi42IDEuMiAyLjYgMi44IDAgMS41LTEuMiAyLjgtMi42IDIuOEM0My43IDExLjggNDIuNSAxMC41IDQyLjUgOWMwLTEuNSAxLjItMi44IDIuNi0yLjh6bS0yMC4yIDAgMS42IDBjMS42IDAgMi42IDEuMyAyLjYgMi44IDAgMS41LTEuMSAyLjgtMi42IDIuOGwtMS42IDAgMC01LjV6bTkgMCAxLjUgMGMxLjUgMCAyLjYgMS4zIDIuNiAyLjggMCAxLjUtMSAyLjgtMi42IDIuOGwtMS41IDAgMC01LjV6IiBmaWxsPSIjZmZmIi8+PC9zdmc+' alt='Mapbox' />
                </a>
            </div>
            <div class='col span_2_of_3'>
                <div id='tableauViz1'></div>
            </div>
            <div class='col span_2_of_3'>
                <div id='tableauViz2'></div>
            </div>
            <div class='col span_2_of_3'>
                <div id='tableauViz3'></div>
            </div>
        </div>
    </div>
    <script>
    function init() {
        //global variables in browser
        var incd_filter = ['all', ['>=', document.getElementById('metric').value, 1]]
        var incd_filter_base = ['all', ['<', document.getElementById('metric').value, 1]]

        var borough_centers = {
            'STATEN ISLAND': [-74.16325437951, 40.5719632938],
            'BROOKLYN': [-73.96331487639, 40.6460149617],
            'QUEENS': [-73.81373050739, 40.71611720724],
            'BRONX': [-73.86803506380, 40.85977744281],
            'MANHATTAN': [-73.98207463224, 40.75906717458]
        }

        //Remove scroll zoom on embed

        //GET EACH DASHBOARD WORKBOOK AND INTITIALIZE AS A SEPARATE DIV ELEMENT

        var oneUrl = 'https://public.tableau.com/views/NYCSafetyDashboard/a2?:showVizHome=no&:display_spinner=yes&:jsdebug=n&:embed=y&:display_overlay=no&:display_static_image=no&:animate_transition=yes ';
        var twoUrl = 'https://public.tableau.com/views/NYCSafetyDashboard/b2?:showVizHome=no&:display_spinner=yes&:jsdebug=n&:embed=y&:display_overlay=no&:display_static_image=no&:animate_transition=yes ';
        var threeUrl = 'https://public.tableau.com/views/NYCSafetyDashboard/c2?:showVizHome=no&:display_spinner=yes&:jsdebug=n&:embed=y&:display_overlay=no&:display_static_image=no&:animate_transition=yes ';

        var vizOptionsOne = {
            width: '100%',
            height: '400px',
            hideTabs: true,
            hideToolbar: true,
            onFirstInteractive: function() {}
        };

        var vizOptionsTwo = {
            width: '100%',
            height: '390px',
            hideTabs: true,
            hideToolbar: true,
            onFirstInteractive: function() {}
        };

        onePh = document.getElementById('tableauViz1')
        twoPh = document.getElementById('tableauViz2')
        threePh = document.getElementById('tableauViz3')

        var viz1 = new tableauSoftware.Viz(onePh, oneUrl, vizOptionsOne);
        var viz2 = new tableauSoftware.Viz(twoPh, twoUrl, vizOptionsOne);
        var viz3 = new tableauSoftware.Viz(threePh, threeUrl, vizOptionsTwo);

        //INITIALIZE THE MAPBOX MAP
        mapboxgl.accessToken = 'pk.eyJ1IjoicnNiYXVtYW5uIiwiYSI6IjdiOWEzZGIyMGNkOGY3NWQ4ZTBhN2Y5ZGU2Mzg2NDY2In0.jycgv7qwF8MMIWt4cT0RaQ';
        var bounds = [
            [-75.04728500751165, 39.68392799015035],
            [-72.91058699000139, 41.87764500765852]
        ];
        var centerPoint = [-73.98, 40.7488]

        var map = new mapboxgl.Map({
            container: 'map',
            style: 'mapbox://styles/mapbox/dark-v9',
            center: centerPoint,
            zoom: 12,
            minZoom: 10,
            maxZoom: 22,
            pitch: 30,
            maxBounds: bounds
        });

        map.addControl(new mapboxgl.NavigationControl({
            position: 'bottom-right'
        }));

        function gen_popup(feature, property) {
            var e = document.getElementById('metric')
            var prop_disp = e.options[e.selectedIndex].text;
            //Generate the html for the popup
            return ('<h3>Collision Detail</h3>' +
                '<ul>' +
                '<li>Time: <b>' + feature.properties.TS + '</b></li>' +
                '<li>Bourough: <b>' + feature.properties.BOROUGH + '</b></li>' +
                '<li>' + prop_disp + ': <b>' + feature.properties[property] + '</b></li>' +
                '<li>Factor: <b>' + feature.properties.VEH_CONTRIB_1 + '</b></li>' +
                '</ul>')
        }

        map.once('load', function() {
            map.addSource('veh-incidents', {
                type: 'vector',
                url: 'mapbox://rsbaumann.4juqkxoc?optimize=true'
            });

            map.addSource('bouroughs', {
                type: 'vector',
                url: 'mapbox://rsbaumann.6n6xib60?optimize=true'
            });

            map.addLayer({
                'id': 'veh-incd-base',
                'type': 'circle',
                'source': 'veh-incidents',
                'source-layer': 'nyc_pedcyc_collisions_161004-d5u2nq',
                'paint': {
                    'circle-color': 'yellow',
                    'circle-radius': {
                        'stops': [
                            [10, 1],
                            [16, 12]
                        ],
                        'type': 'exponential'
                    },
                    'circle-opacity': 0.3,
                    'circle-blur': 1
                }
            }, 'waterway-label');

            map.addLayer({
                'id': 'veh-incd',
                'type': 'circle',
                'source': 'veh-incidents',
                'source-layer': 'nyc_pedcyc_collisions_161004-d5u2nq',
                'paint': {
                    'circle-color': {
                        'property': 'CYC_INJ',
                        'type': 'exponential',
                        'colorSpace': 'lab',
                        'stops': [
                            [1, 'orange'],
                            [2, 'red']
                        ]
                    },
                    'circle-radius': {
                        'property': 'CYC_INJ',
                        'base': 3,
                        'type': 'exponential',
                        'stops': [
                            [{
                                zoom: 10,
                                value: 1
                            }, 2],
                            [{
                                zoom: 12,
                                value: 1
                            }, 4],
                            [{
                                zoom: 14,
                                value: 1
                            }, 10],
                            [{
                                zoom: 16,
                                value: 1
                            }, 20],
                            [{
                                zoom: 10,
                                value: 3
                            }, 3],
                            [{
                                zoom: 12,
                                value: 3
                            }, 6],
                            [{
                                zoom: 14,
                                value: 3
                            }, 15],
                            [{
                                zoom: 16,
                                value: 3
                            }, 30],
                        ]
                    },
                    'circle-opacity': 0.8,
                    'circle-blur': 0.5
                }
            }, 'veh-incd-base');

            map.addLayer({
                'id': 'bouroughs-fill',
                'type': 'fill',
                'source-layer': 'nyc-bouroughs-8e9odb',
                'source': 'bouroughs',
                'paint': {
                    'fill-color': {
                        'type': 'categorical',
                        'property': 'BoroName',
                        'stops': [
                            ['Queens', 'red'],
                            ['Bronx', 'blue'],
                            ['Brooklyn', 'green'],
                            ['Manhattan', 'purple'],
                            ['Staten Island', 'teal']
                        ]
                    },
                    'fill-opacity': 0.15,
                    'fill-outline-color': 'black'
                }
            }, 'veh-incd-base');

            map.addLayer({
                'id': '3d-buildings',
                'source': 'composite',
                'source-layer': 'building',
                'filter': ['==', 'extrude', 'true'],
                'type': 'fill-extrusion',
                'minzoom': 15,
                'paint': {
                    'fill-extrusion-color': '#aaa',
                    'fill-extrusion-height': {
                        'type': 'identity',
                        'property': 'height'
                    },
                    'fill-extrusion-base': {
                        'type': 'identity',
                        'property': 'min_height'
                    },
                    'fill-extrusion-opacity': .6
                }
            }, 'bouroughs-fill');

            map.setFilter('veh-incd', incd_filter);
            map.setFilter('veh-incd-base', incd_filter_base);

            map.on('click', function(e) {
                var features = map.queryRenderedFeatures(e.point, {
                    layers: ['veh-incd']
                });
                if (!features.length) {
                    return;
                }
                var feature = features[0];
                var html_popup = gen_popup(feature, document.getElementById('metric').value)
                var popup = new mapboxgl.Popup()
                    .setLngLat(map.unproject(e.point))
                    .setHTML(html_popup)
                    .addTo(map);
            });

            //Hide loading bar once tiles from source are loaded

            map.on('data', function(e) {
                if (e.dataType === 'tile' && e.source.id === 'veh-incidents') {
                    document.getElementById('loader').style.visibility = 'hidden';
                    $('#parameter').change(updateParam);
                }
            })

            map.on('mousemove', function(e) {
                var features = map.queryRenderedFeatures(e.point, {
                    layers: ['veh-incd']
                });
                map.getCanvas().style.cursor = (features.length) ? 'pointer' : '';
            });

            if (window.location.search.indexOf('embed') !== -1) map.scrollZoom.disable();
        });

        viz1.addEventListener(tableau.TableauEventName.MARKS_SELECTION, onBoroughSelection);
        viz2.addEventListener(tableau.TableauEventName.MARKS_SELECTION, onFactorSelection);
        viz3.addEventListener(tableau.TableauEventName.MARKS_SELECTION, onTimeSelection);

        // INTEGRATE FILTERS AND PARAMETERS BETWEEN TABLEAU & MAPBOX

        function onBoroughSelection(marksEvent) {
            return marksEvent.getMarksAsync().then(reportBorough);
        }

        function onFactorSelection(marksEvent) {
            return marksEvent.getMarksAsync().then(reportFactors);
        }

        function onTimeSelection(marksEvent) {
            return marksEvent.getMarksAsync().then(reportTime);
        }

        function mutateFilter(filter, old_operator, old_key, new_filter, recalc) {
            // Remove a filter from a Mapbox GL stylespec filter array, 
            // and add a newFilter to the filter array.
            // Return the mutated filter array

            for (i = 1; i < filter.length; i++) {
                if ((filter[i][0] === old_operator) && (filter[i][1] === old_key)) {
                    filter.splice(i, 1); //remove existinng parameter filter
                }
            }
            if (recalc == true) {
                filter.push(new_filter);
            }
            return filter
        }

        function reportBorough(marks) {
            //sync filters on map and dashboard when interacting with boroughs dash
            try {
                if (marks.length > 0) {
                    pair = marks[0].getPairs()[0];
                    fieldName = pair.fieldName.toUpperCase().replace(/\s/g, '_');
                    fieldValue = pair.value;
                    newFilterOne = ['==', fieldName, fieldValue]
                    incd_filter = mutateFilter(incd_filter, '==', fieldName, newFilterOne, true)
                    incd_filter_base = mutateFilter(incd_filter_base, '==', fieldName, newFilterOne, true)
                    viz2.getWorkbook().getActiveSheet().getWorksheets()[0].applyFilterAsync(fieldName, fieldValue, tableau.FilterUpdateType.REPLACE);
                    viz3.getWorkbook().getActiveSheet().getWorksheets()[0].applyFilterAsync(fieldName, fieldValue, tableau.FilterUpdateType.REPLACE);
                    map.flyTo({
                        center: borough_centers[fieldValue]
                    });
                } else {
                    viz2.getWorkbook().getActiveSheet().getWorksheets()[0].clearFilterAsync(fieldName);
                    viz3.getWorkbook().getActiveSheet().getWorksheets()[0].clearFilterAsync(fieldName);
                    incd_filter = mutateFilter(incd_filter, '==', 'BOROUGH', [], false)
                    incd_filter_base = mutateFilter(incd_filter_base, '==', 'BOROUGH', [], false)
                    map.flyTo({
                        center: centerPoint
                    });
                }
                refreshMap(map)
            } catch (e) {
                console.log(e)
            }
        }

        function reportFactors(marks) {
            //sync filters on map and dashboard when interacting with factors dash
            try {
                if (marks.length > 0) {
                    pair = marks[0].getPairs()[0];
                    fieldName = 'VEH_CONTRIB_1'
                    fieldValue = pair.value;
                    newFilterOne = ['==', fieldName, fieldValue]
                    incd_filter = mutateFilter(incd_filter, '==', 'VEH_CONTRIB_1', newFilterOne, true)
                    incd_filter_base = mutateFilter(incd_filter_base, '==', 'VEH_CONTRIB_1', newFilterOne, true)
                    viz1.getWorkbook().getActiveSheet().getWorksheets()[0].applyFilterAsync('Veh Contrib 1', fieldValue, tableau.FilterUpdateType.REPLACE);
                    viz3.getWorkbook().getActiveSheet().getWorksheets()[0].applyFilterAsync('Veh Contrib 1', fieldValue, tableau.FilterUpdateType.REPLACE);
                } else {
                    viz1.getWorkbook().getActiveSheet().getWorksheets()[0].clearFilterAsync('Veh Contrib 1');
                    viz3.getWorkbook().getActiveSheet().getWorksheets()[0].clearFilterAsync('Veh Contrib 1');
                    incd_filter = mutateFilter(incd_filter, '==', 'VEH_CONTRIB_1', [], false)
                    incd_filter_base = mutateFilter(incd_filter_base, '==', 'VEH_CONTRIB_1', [], false)
                }
                refreshMap(map)
            } catch (e) {
                console.log(e)
            }
        }

        function reportTime(marks) {
            //sync filters on map and dashboard when interacting with timeseries dash
            try {
                if (marks.length > 0) {
                    pair = marks[0].getPairs()[1];
                    fieldName = 'MONTH'
                    fieldValue = pair.value;
                    newFilterOne = ['==', fieldName, fieldValue]
                    incd_filter = mutateFilter(incd_filter, '==', fieldName, newFilterOne, true)
                    incd_filter_base = mutateFilter(incd_filter_base, '==', fieldName, newFilterOne, true)
                    viz1.getWorkbook().getActiveSheet().getWorksheets()[0].applyFilterAsync('MONTH', fieldValue, tableau.FilterUpdateType.REPLACE);
                    viz2.getWorkbook().getActiveSheet().getWorksheets()[0].applyFilterAsync('MONTH', fieldValue, tableau.FilterUpdateType.REPLACE);
                } else {
                    viz1.getWorkbook().getActiveSheet().getWorksheets()[0].clearFilterAsync('MONTH');
                    viz2.getWorkbook().getActiveSheet().getWorksheets()[0].clearFilterAsync('MONTH');
                    incd_filter = mutateFilter(incd_filter, '==', 'MONTH', [], false)
                    incd_filter_base = mutateFilter(incd_filter_base, '==', 'MONTH', [], false)
                }
                refreshMap(map)
            } catch (e) {
                console.log(e)
            }
        }

        function refreshMap(map) {
            map.setFilter('veh-incd', incd_filter);
            map.setFilter('veh-incd-base', incd_filter_base);
        }

        function onMarksSelection(marksEvent) {
            return marksEvent.getMarksAsync().then(reportSelectedMarks);
        }

        function onParamChange(paramEvent) {
            return paramEvent.getParameterAsync().then(reportSelectedParams);
        }

        function updateParam() {
            var propValue = document.getElementById('metric').value
            incd_filter = ['all', ['>=', propValue, 1]]
            incd_filter_base = ['all', ['<', propValue, 1]]
            refreshMap(map);
            viz1.getWorkbook().changeParameterValueAsync('Metric', propValue);
            viz2.getWorkbook().changeParameterValueAsync('Metric', propValue);
            viz3.getWorkbook().changeParameterValueAsync('Metric', propValue);
        };

        //Mobile Screen orientation
        var isMobile = {
            Android: function() {
                return /Android/i.test(navigator.userAgent);
            },
            iOS: function() {
                return /iPhone|iPad|iPod/i.test(navigator.userAgent);
            }
        };

        if (isMobile.Android()) {
            var previousWidth = $(window).width();
            $(window).on({
                resize: function(e) {
                    var YourFunction = (function() {

                        var screenWidth = $(window).width();
                        if (previousWidth != screenWidth) {
                            previousWidth = screenWidth;
                            window.location.reload();
                        }

                    })();

                }
            });

        } else //mainly for ios
        {
            $(window).on({
                orientationchange: function(e) {
                    window.location.reload();
                }
            });
        }
    }

    $(document).ready(function() {
        init(); //run the app!
    });
    </script>
</body>
<script src="https://public.tableau.com/javascripts/api/tableau-2.min.js"></script>
<script src='https://api.tiles.mapbox.com/mapbox-gl-js/v0.28.0/mapbox-gl.js'></script>

</html>
