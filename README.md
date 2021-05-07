docker run -d \
--name=nextcloud \
-e USERNAME=webdav \
-e PASSWORD=webdav \
-e PUID=5000 \
-e PGID=101 \
-e TZ=Asia/Shanghai \
-p 443:443 \
-p 888:888 \
-v /****path/config:/config \
-v /****/data_nextcloud:/data \
-v /****/data_webdav:/data_webdav \
--restart no \
dingmingglc/nextcloud:latest
