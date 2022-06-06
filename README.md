# Docker Compose For Valhalla

[Using gisops valhalla docker image](https://github.com/gis-ops/docker-valhalla), a flexible blank state valhalla engine container. Use `docker-compose.yml` to build the valhalla image presetted to Jakarta (you need to change some environments parameter in order to cater to your own needs), `docker-compose.novolume.yml` is the version where we don't need to mount a volume to the container at the cost of flexibility (you need to download each map tile after setting up the container)

## Details

Using image 3.0.9 tag from https://hub.docker.com. pull the image with `docker pull` `gisops/valhalla:3.0.9` or `gisops/valhalla:latest`.

## Environemnt Variables

Refer to [gisops valhalla repository](https://github.com/gis-ops/docker-valhalla)
