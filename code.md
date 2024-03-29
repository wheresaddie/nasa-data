# SOLAR FLARE

| Each NFT has its own class A, B, C, M, and X, and wavelength metadata | 
| from 1 to 8. When a solar flare, whose classification is the same as your NFT, occurs, it will be unlocked.

```
GET https://api.nasa.gov/DONKI/FLR?startDate=2023-11-01&endDate=2023-11-12&api_key=cT7U8404Iu3L9BCAkPEJ0BRWeXOM6ecLLqg8UJyY
```

Scientists classify solar flares according to their X-ray brightness, in the wavelength range 1 to 8 Angstroms. Flares classes have names: A, B, C, M, and X, with A being the tiniest and X being the largest. Each category has nine subdivisions ranging from, e.g., C1 to C9, M1 to M9, and X1 to X9. These are logarithmic scales, much like the seismic Richter scale. So an M flare is 10 times as strong as a C flare.https://solar-center.stanford.edu/SID/activities/flare.html

Flare calendar: https://www.spaceweatherlive.com/en/archive.html

RESULT EXAMPLE (shorten):

```
"flrID": "2023-11-03T04:40:00-FLR-001",
        "instruments": [
            {
                "displayName": "GOES-P: EXIS 1.0-8.0"
            }
        ],
        "beginTime": "2023-11-03T04:40Z",
        "peakTime": "2023-11-03T06:17Z",
        "endTime": "2023-11-03T07:00Z",
        "classType": "C3.2",
        "sourceLocation": "N30W30",
        "activeRegionNum": null,
        "linkedEvents": [
            {
                "activityID": "2023-11-03T05:48:00-CME-001"
            }
        ],
  "https://webtools.ccmc.gsfc.nasa.gov/DONKI/view/FLR/27572/-1"
```

# GEOMAGNETIC STORM

Référence: https://www.spaceweatherlive.com/en/help/the-kp-index.html

The solar magnetic field reverses every 11 years. Here is the frequency of events ranked by magnitude. Bellow is an average of the total number of geomagnetic storms and their intensity measured in Kp.

Capture d’écran, le 2023-12-13 à 16.58.58

So for ASIDE, smart-contract can say: « If a geomagnetic storm whose kpIndex is superior »

```
GET https://api.nasa.gov/DONKI/GST?startDate=2023-11-01&endDate=2023-11-12&api_key=cT7U8404Iu3L9BCAkPEJ0BRWeXOM6ecLLqg8UJyY
```

RESULT EXAMPLE (shorten):

```
"gstID": "2023-11-05T09:00:00-GST-001",
        "startTime": "2023-11-05T09:00Z",
        "allKpIndex": [
            {
                "observedTime": "2023-11-05T21:00Z",
                "kpIndex": 6.33,
                "source": "NOAA"
            },
            {
                "observedTime": "2023-11-06T06:00Z",
                "kpIndex": 5.67,
                "source": "NOAA"}
                ];
                
“https://webtools.ccmc.gsfc.nasa.gov/DONKI/view/GST/27600/-1”
```

# CORONAL MASS EJECTION

Typically, coronal mass ejections are classified into three main categories, denoted as C, M, and X, with numerical subcategories (e.g., C1, C2, M1, M2, X1, X2, etc.). These classifications are based on the energy released by the CME, measured in X-rays. C-class eruptions are usually of low intensity, followed by M and X classes indicating increasingly powerful eruptions.

```
GET https://api.nasa.gov/DONKI/CMEAnalysis?startDate=2023-11-01&endDate=2023-11-12&mostAccurateOnly=true&speed=500&speed=0&halfAngle=30&catalog=ALL&api_key=cT7U8404Iu3L9BCAkPEJ0BRWeXOM6ecLLqg8UJyY&default
```

RESULT EXAMPLE (shorten):

```
   {
        "time21_5": "2023-11-06T13:39Z",
        "latitude": -30.0,
        "longitude": 62.0,
        "halfAngle": 36.0,
        "speed": 595.0,
        "type": "C",
        "isMostAccurate": true,
        "associatedCMEID": "2023-11-06T07:36:00-CME-001",
        "note": "A very approximate analysis (especially the longitude) since the source is close/on the limb and is not seen in its entirety.",
        "catalog": "M2M_CATALOG",
        "link": "https://webtools.ccmc.gsfc.nasa.gov/DONKI/view/CMEAnalysis/27632/-1"
    },
    {
        "time21_5": "2023-11-08T11:39Z",
        "latitude": 12.0,
        "longitude": 88.0,
        "halfAngle": 34.0,
        "speed": 871.0,
        "type": "C",
        "isMostAccurate": true,
        "associatedCMEID": "2023-11-08T07:24:00-CME-001",
        "note": "Measurement of leading edge using SOHO LASCO C2/C3 in SWPC_CAT. Parameters obtained using source location coordinates.",
        "catalog": "M2M_CATALOG",
        "link": "https://webtools.ccmc.gsfc.nasa.gov/DONKI/view/CMEAnalysis/27644/-1"
    },
```
    
# EARTHQUAKE

https://earthquake.usgs.gov/earthquakes/eventpage/us7000l9h4/executive

API usage example:

For exemple if i want a list of EarthQuake from 2023-10-10 to 2023-11-10 here with a minimum magnitude of 7:

```
GET https://earthquake.usgs.gov/fdsnws/event/1/query?format=geojson&starttime=2023-10-10&endtime=2023-11-10&minmagnitude=7
```

So for ASIDE, smart-contract can say: « Each NFT has its own Richer scale integrated into its metadata. When an Earthquake whose classification is the same as your NFT, occurs, it will be unlocked. »

RESULT EXAMPLE:

```
{
    "type": "FeatureCollection",
    "metadata": {
        "generated": 1702483360000,
        "url": "https://earthquake.usgs.gov/fdsnws/event/1/query?format=geojson&starttime=2023-10-10&endtime=2023-11-10&minmagnitude=7",
        "title": "USGS Earthquakes",
        "status": 200,
        "api": "1.14.0",
        "count": 1
    },
    "features": [
        {
            "type": "Feature",
            "properties": {
                "mag": 7.1,
                "place": "Banda Sea",
                "time": 1699419230283,
                "updated": 1701919288870,
                "tz": null,
                "url": "https://earthquake.usgs.gov/earthquakes/eventpage/us7000l9h4",
                "detail": "https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=us7000l9h4&format=geojson",
                "felt": 5,
                "cdi": 7.4,
                "mmi": 6.062,
                "alert": "green",
                "status": "reviewed",
                "tsunami": 0,
                "sig": 779,
                "net": "us",
                "code": "7000l9h4",
                "ids": ",us7000l9h4,",
                "sources": ",us,",
                "types": ",dyfi,finite-fault,general-text,ground-failure,impact-text,losspager,moment-tensor,origin,phase-data,shakemap,",
                "nst": 142,
                "dmin
