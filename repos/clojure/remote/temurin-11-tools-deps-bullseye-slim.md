## `clojure:temurin-11-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:3b6e7b70925a7a7e981a0823e6c48b7dc67591ddecd1dca3e09127b223197878
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:5062cc2ec4777be22e6893a06a58b84916d5297f9998b79193f33e21be0b1bf8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.5 MB (291463949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02256a1fea64c8f5e77375c858f653f9e468a5eca3d322329ea904555d0505b2`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Jul 2023 01:20:23 GMT
ADD file:4a063d4e089ef10c6806d7042a0040078674ac2db61df02df8bbb8fa4894910a in / 
# Tue, 04 Jul 2023 01:20:23 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 04:00:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 11:19:30 GMT
COPY dir:3cd19417e6ca044e31be7ef3c49c7d24f962c0f648fd205b421373092856c87f in /opt/java/openjdk 
# Wed, 05 Jul 2023 11:19:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 11:22:58 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Wed, 05 Jul 2023 11:22:58 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 11:23:14 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Jul 2023 11:23:15 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Jul 2023 11:23:15 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:9d21b12d5fab9ab82969054d72411ce627c209257df64b6057016c981e163c30`  
		Last Modified: Tue, 04 Jul 2023 01:25:43 GMT  
		Size: 31.4 MB (31417388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099caecba99bf99b21cfbb7f1c23915fe48406202f54aa425cdb8d4341babebd`  
		Last Modified: Wed, 05 Jul 2023 11:32:56 GMT  
		Size: 198.5 MB (198549444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c4223016b254c070c6a3b6699faaa06eb04ff36b4f998fbc3d725dde8b2180c`  
		Last Modified: Wed, 05 Jul 2023 11:34:38 GMT  
		Size: 61.5 MB (61496501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5bf4d89c25551943f80fb1bd3c5aad31f2c1d9fb4bcc9d66a01652a565ee78c`  
		Last Modified: Wed, 05 Jul 2023 11:34:31 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8ce26ea04169ba13a4c7d1ef1ddb89e97a7131c76ea57f3639472e54329cd5a9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **287.0 MB (287002652 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc607d342dbf51cac53f9599e0a2a59b61606c27a1d8fb2543887c602ea456ce`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 04 Jul 2023 01:57:52 GMT
ADD file:83a81aad5cdb80c654a520d913c8bcafe2b8e1062d81c389d4577cde5ad68167 in / 
# Tue, 04 Jul 2023 01:57:52 GMT
CMD ["bash"]
# Tue, 04 Jul 2023 06:34:25 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Jul 2023 03:35:40 GMT
COPY dir:46f070668c95bcfc449ea3e3aa03838e4c3f9939658e6aebe91ca179e673aded in /opt/java/openjdk 
# Wed, 05 Jul 2023 03:35:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Jul 2023 03:38:38 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Wed, 05 Jul 2023 03:38:38 GMT
WORKDIR /tmp
# Wed, 05 Jul 2023 03:38:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Jul 2023 03:38:52 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Jul 2023 03:38:52 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:50eb042e2421869704212f3e076e9088033eb9a5254341fb1b3022e6e2784921`  
		Last Modified: Tue, 04 Jul 2023 02:02:00 GMT  
		Size: 30.1 MB (30062957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b90eb25a0fa4522274c461d519d4e554d5d39052358c321552f0848e5d55556`  
		Last Modified: Wed, 05 Jul 2023 03:46:58 GMT  
		Size: 195.3 MB (195324199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3d9051ed6338c7861fc778e1ad6012db7e5534edace41b954543c80400fc842`  
		Last Modified: Wed, 05 Jul 2023 03:48:37 GMT  
		Size: 61.6 MB (61614880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147140292da08689e9c40b9d8acc824f948640c340ba446d786a6cc9998fdf01`  
		Last Modified: Wed, 05 Jul 2023 03:48:31 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
