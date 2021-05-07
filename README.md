nextcloud port:443
webdav port:888


docker run -d \
--name=nextcloud \
-e USERNAME=webdav \
-e PASSWORD=webdav \
-e PUID=5000 \
-e PGID=101 \
-e TZ=Asia/Shanghai \
-p 443:443 \
-p 888:888 \
-v /path/config:/config \
-v /path/data_nextcloud:/data \
-v /path/data_webdav:/data_webdav \
--restart no \
dingmingglc/nextcloud:latest
