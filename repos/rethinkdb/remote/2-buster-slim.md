## `rethinkdb:2-buster-slim`

```console
$ docker pull rethinkdb@sha256:b142027c773d80048656fe1bc6c71c61f08279dd6be6a201bdb87a95ec99a685
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `rethinkdb:2-buster-slim` - linux; amd64

```console
$ docker pull rethinkdb@sha256:bc780f06c27fac4c10ccd0bc0258509e5298c98ee7e110f5f1ba84e88798c58f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51754709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9748409ac29202b6becca6c24bc029fb43cfca53746d2d60c5adb657395f5bc`
-	Default Command: `["rethinkdb","--bind","all"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:45:48 GMT
RUN apt-get -qqy update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Fri, 14 Aug 2020 21:12:36 GMT
RUN apt-key adv --keyserver keys.gnupg.net --recv-keys "539A3A8C6692E6E3F69B3FE81D85E93F801BB43F"     && echo "deb https://download.rethinkdb.com/repository/debian-buster buster main" > /etc/apt/sources.list.d/rethinkdb.list
# Fri, 14 Aug 2020 21:12:37 GMT
ENV RETHINKDB_PACKAGE_VERSION=2.4.1~0buster
# Fri, 14 Aug 2020 21:12:50 GMT
RUN apt-get -qqy update 	&& apt-get install -y rethinkdb=$RETHINKDB_PACKAGE_VERSION 	&& rm -rf /var/lib/apt/lists/*
# Fri, 14 Aug 2020 21:12:50 GMT
VOLUME [/data]
# Fri, 14 Aug 2020 21:12:50 GMT
WORKDIR /data
# Fri, 14 Aug 2020 21:12:51 GMT
CMD ["rethinkdb" "--bind" "all"]
# Fri, 14 Aug 2020 21:12:51 GMT
EXPOSE 28015 29015 8080
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf7975e8c352cc79bcac0fb7b7d3433054ff8a40b21411d6e9a8cd0da6766776`  
		Last Modified: Mon, 10 Aug 2020 19:00:55 GMT  
		Size: 6.7 MB (6669184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f35ca7cb163021376fc027d28e1a9aa0f6df516597597bf7770164b3a67f6d5d`  
		Last Modified: Fri, 14 Aug 2020 21:13:59 GMT  
		Size: 2.6 KB (2612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e6eaa3382fc34b4261ac413cc750fff2b9813c7cc5daabb71cddb0d07e54946`  
		Last Modified: Fri, 14 Aug 2020 21:14:03 GMT  
		Size: 18.0 MB (17990699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24551774cb19720139020672b9dac074754221b9b4138cd1ae9047c9d510796f`  
		Last Modified: Fri, 14 Aug 2020 21:13:59 GMT  
		Size: 93.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
