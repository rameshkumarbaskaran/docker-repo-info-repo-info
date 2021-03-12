## `neurodebian:nd-non-free`

```console
$ docker pull neurodebian@sha256:5566b9b4850ac4f79eb8adba3d697eb20785838df62e3443e1d80bab4cc90a02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `neurodebian:nd-non-free` - linux; amd64

```console
$ docker pull neurodebian@sha256:3a2b07e4ef1b6357a47d36103d6dedcbab82c0fbb50b5597fe2fa46cd5b123a1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66446023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7902bc54d3756764327fe6b92eb9ccaa9793fbde839d353612b15579c13602a`
-	Default Command: `["bash"]`

```dockerfile
# Fri, 12 Mar 2021 02:21:52 GMT
ADD file:719f8702f6aa56e8ad69f574e924fdf062e8fdc72584f70aaac387be5e1d4a51 in / 
# Fri, 12 Mar 2021 02:21:53 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 11:50:20 GMT
RUN set -x 	&& apt-get update 	&& { 		which gpg 		|| apt-get install -y --no-install-recommends gnupg 	; } 	&& { 		gpg --version | grep -q '^gpg (GnuPG) 1\.' 		|| apt-get install -y --no-install-recommends dirmngr 	; } 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 11:50:21 GMT
RUN set -x 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys DD95CC430502E37EF840ACEEA5D32F012649A5A9 	&& gpg --batch --export DD95CC430502E37EF840ACEEA5D32F012649A5A9 > /etc/apt/trusted.gpg.d/neurodebian.gpg 	&& rm -rf "$GNUPGHOME" 	&& apt-key list | grep neurodebian
# Fri, 12 Mar 2021 11:50:23 GMT
RUN { 	echo 'deb http://neuro.debian.net/debian sid main'; 	echo 'deb http://neuro.debian.net/debian data main'; 	echo '#deb-src http://neuro.debian.net/debian-devel sid main'; } > /etc/apt/sources.list.d/neurodebian.sources.list
# Fri, 12 Mar 2021 11:50:30 GMT
RUN set -x 	&& apt-get update 	&& apt-get install -y --no-install-recommends neurodebian-freeze eatmydata 	&& ln -s /usr/bin/eatmydata /usr/local/bin/apt-get 	&& rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 11:50:37 GMT
RUN sed -i -e 's,main *$,main contrib non-free,g' /etc/apt/sources.list.d/neurodebian.sources.list /etc/apt/sources.list
```

-	Layers:
	-	`sha256:78c7a03f25ec710f7b6b9ccc0ee40eb1871016252eea6df272c68389f18d30a5`  
		Last Modified: Fri, 12 Mar 2021 02:28:37 GMT  
		Size: 54.8 MB (54840531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:762ff88c90ad458a4f9f50dddb5016f3085fe3ae585980b96d328db99b014ec3`  
		Last Modified: Fri, 12 Mar 2021 11:54:30 GMT  
		Size: 11.3 MB (11299313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ff2278f23798743fec34194a2b260cc25dfe0224c9f55866ec5cc60edc477d`  
		Last Modified: Fri, 12 Mar 2021 11:54:29 GMT  
		Size: 1.8 KB (1760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7155a4c9f5fa62c6d4a358a75e76f885f8325ad84a58cd7f5579abd5e4e06c22`  
		Last Modified: Fri, 12 Mar 2021 11:54:29 GMT  
		Size: 242.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:319f3300b50f2ae2a908993d8d9a0c35e420aef0247da4ab4d1d109a96615056`  
		Last Modified: Fri, 12 Mar 2021 11:54:29 GMT  
		Size: 303.9 KB (303859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f430cfeb30ac451bd47f9f11c0082b3c4621b4d562e202b90aba4639cb995307`  
		Last Modified: Fri, 12 Mar 2021 11:54:41 GMT  
		Size: 318.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
