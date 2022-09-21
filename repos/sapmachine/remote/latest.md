## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:32fd23b07587ee9dff8b455e9d5dede20232beec7ba206c87e05142fbc510729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:af1db5ca3c2f44950f23807ec6c144d679e3ab1dde697391da20b801a635bd59
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **242.7 MB (242655923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db9859c560a01e2113842c4b7120655be3105acc5fa1e1fa1f29c66957b96caf`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 01 Sep 2022 23:46:26 GMT
ADD file:ff6963f777661fb16cc12fb04a97c558bd94768a6e4ab5bd90e01f3086818853 in / 
# Thu, 01 Sep 2022 23:46:27 GMT
CMD ["bash"]
# Fri, 02 Sep 2022 05:18:06 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Sep 2022 18:43:43 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys CACB9FE09150307D1D22D82962754C3B3ABCFE23     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-19-jdk=19     && rm -rf /var/lib/apt/lists/*
# Wed, 21 Sep 2022 18:43:43 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-19
# Wed, 21 Sep 2022 18:43:44 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:675920708c8bf10fbd02693dc8f43ee7dbe0a99cdfd55e06e6f1a8b43fd08e3f`  
		Last Modified: Thu, 01 Sep 2022 03:03:40 GMT  
		Size: 28.6 MB (28572685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f22cfdca4ade1c37b330579696289f17d20a8c14e27055b76204bcb6ec482d72`  
		Last Modified: Fri, 02 Sep 2022 05:20:14 GMT  
		Size: 7.9 MB (7920278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55aa8aa90af5b45722c794fb57fa2bc9c3a496ddf55e356324dbef75f1c769bc`  
		Last Modified: Wed, 21 Sep 2022 18:44:18 GMT  
		Size: 206.2 MB (206162960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
