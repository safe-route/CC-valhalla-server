# Docker Compose For Valhalla

[Using gisops valhalla docker image](https://github.com/gis-ops/docker-valhalla), a flexible blank state valhalla engine container. Use `docker-compose.yml` to build the valhalla image presetted to Jakarta (you need to change some environments parameter in order to cater to your own needs), `docker-compose.novolume.yml` is the version where we don't need to mount a volume to the container at the cost of flexibility (you need to download each map tile after setting up the container)

## Details

Using image 3.0.9 tag from https://hub.docker.com. pull the image with `docker pull` `gisops/valhalla:3.0.9` or `gisops/valhalla:latest`.

## Environemnt Variables

Refer to [gisops valhalla repository](https://github.com/gis-ops/docker-valhalla)

## Usage

```bash
curl http://35.187.197.248:8002/route --data '{"locations":[{"lat":-6.189626,"l
on":106.825811},{"lat":-6.148926,"lon":106.727605}],"costing":"auto","directions_o
ptions":{"units":"miles"}}' | jq '.'
```

should response with:

```bash
{
  "trip": {
    "language": "en-US",
    "status": 0,
    "units": "miles",
    "status_message": "Found route between points",
    "legs": [
      {
        "shape": "fhwxJ__dwjEt~Bw_CtEcFjJyMn@iBCiCSkA]}@aBiBoqA}@qR?kD?a@M}E?uf@}@gKMyX_@qr@iu@gCyCeCkAuD{@eBOiC]@dE?hCMpGKfNW`SM~HKvCEhCq@vCFxLQn^BfCObQWbRAz@QbQEhCIjKMbGQ|IWpRIfDUdPGbFChCXxBRxBCpGBdE?tE?dE?l@AxWC`\\W`SGlJEvXKtEGtDQhCGfDMtDSnIC|@QjKIvCe@nr@JjVN~Ih@bPb@zLhCdx@n@b[NnS?l@TrQ\\b[NfXBlJDnIHrPMxWA`HC`SCvMIvD]fDy@vCoAfCgCfDkCxCwC?eI?c\\L}IN_ENiEj@aD|@uEvCsNlKwPhLiCzAwBzAaCxBwDz@wAl@eA|@yAz@gCjAaB^_D\\kWnIc\\lJiOdEyPdFof@vMy_@jK{LfDyHzA{HzAoKjAeUfDq]tEc|@rPcF|@iQvCkc@`Hy`@`Hs~AxWog@|IcANge@~H}kApQqXtEcANyh@nH{Cl@sNjBq[tE]?cD\\uGl@qBLu[zAmCNpCdYpAxMlCfXRjBhHvv@l@tE\\zAb@fCbAxCnC~H~I~RnOjW|_@pp@xo@beAxNzUnd@`q@pAfCdBfD|ElKrXro@hT`g@t@zA|@hBfBfDzBtElE`HjAhBx\\pf@zFlJlCvDf@|@zBdD|KdPbd@|s@nAhCfAxAv@lAhAhBrM~SlCdEnIvMtHhM|L`SpJbP|IhM|LhXtElJx@hBIxB@ND\\bBbFjBtETl@lQtd@dFzKjQ|^zLr[zAvC~EzKdF`HtHlJpHpGdGhChEfDvOzKtT|Jl}@pq@dTtOjM|IrFvDlM|InMnIdMfNpFpG|DbG~ElJfElKt@xBt@xBnCnHvj@fvBjE~RhDzUfB|Tp@jLj@zj@`BplD`@jUlAhb@jG|s@f@fD|BdO`G|^hO~r@l`@`dBrvB~sHhQbp@tZpeAlIb[~Mfm@xKfn@pCnR|Hxv@pAdOf@vNvCro@zEviDjHlaG~Up_GvAp\\vMfhDdIplDrId_Ed@lTvEjsBj@jUrC||AlI~kF}@naFHb[`CtEZxBJhCf@li@AfM@z`@d@nIdDpR|Jtn@bBbPr@xWaBtYyFdy@eAlKE`HJlItArF`BvDnE`HrHbGlItDzKzAxHOdI{@~GwCxFuE|EaHnCcGdAqG^kLwA}JcDoH{FoI_GwD_HyBoO{@mTz@aSfDuUfDqOxBmG|@gG?}k@|Im~@bQqDl@euBb[sn@|JyqBr[{ZbFwdChb@g`BhWso@nIip@`GkhApH_tArF__@zAiZjAk~@xBex@hC}M\\k~BrFg[z@qq@hC_hBhMqRxByjAjL}sAnHupBvDkT\\_aANqdCkB}@|@}@l@cA?aB?_e@LoVm@i~D_IgI\\{MrGkSm@}M?uI?{J?eUNoGOyDOoC?qVNkA?iP?cd@Ni[LyM?wTNi`AuE{JyBsUwC}]yCm`@uDgI{A",
        "summary": {
          "has_time_restrictions": false,
          "max_lon": 106.830025,
          "max_lat": -6.148922,
          "time": 1545,
          "length": 11.921,
          "min_lat": -6.193448,
          "min_lon": 106.727104
        },
        "maneuvers": [
          {
            "travel_mode": "drive",
            "begin_shape_index": 0,
            "length": 0.236,
            "time": 37,
            "type": 2,
            "end_shape_index": 4,
            "instruction": "Drive southeast on Jalan Gereja Theresia.",
            "verbal_pre_transition_instruction": "Drive southeast on Jalan Gereja Theresia for 2 tenths of a mile.",
            "travel_type": "car",
            "street_names": [
              "Jalan Gereja Theresia"
            ]
          },
          {
            "travel_type": "car",
            "travel_mode": "drive",
            "verbal_pre_transition_instruction": "Turn left onto Jalan HOS Cokroaminoto.",
            "verbal_transition_alert_instruction": "Turn left onto Jalan HOS Cokroaminoto.",
            "length": 0.339,
            "instruction": "Turn left onto Jalan HOS Cokroaminoto.",
            "end_shape_index": 22,
            "type": 15,
            "time": 97,
            "verbal_post_transition_instruction": "Continue for 3 tenths of a mile.",
            "street_names": [
              "Jalan HOS Cokroaminoto"
            ],
            "begin_shape_index": 4
          },
          ...
```