## `clojure:temurin-17-tools-deps-1.11.1.1429-bookworm`

```console
$ docker pull clojure@sha256:088e51f8c4c5efe97852c1bd0b4ddc3f9fa95e2f96f7fbbdc588aeb8d3ff1522
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1429-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:410fd2ec9d3775ddcbf2b2843de5c0f39bf3ef41e17a6f23143e61f6168278aa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.0 MB (278036797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ead2d81e20314e1c67f742c998a9285d87a6e9ec307249e58136cd8b2d3f5a4d`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:24 GMT
ADD file:39d17d28c5de0bd629e5b7c8190228e5a445d61d668e189b7523e90e68f78244 in / 
# Tue, 21 Nov 2023 05:21:25 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:07:35 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 10:01:45 GMT
COPY dir:e13dbcd57950f4d4d23f4aba8428b6fbbf838d8f4801d32a25e344d37d33c37e in /opt/java/openjdk 
# Sat, 02 Dec 2023 10:01:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 18:28:56 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 05 Dec 2023 18:28:56 GMT
WORKDIR /tmp
# Tue, 05 Dec 2023 18:29:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 05 Dec 2023 18:29:15 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 05 Dec 2023 18:29:16 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 05 Dec 2023 18:29:16 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 05 Dec 2023 18:29:16 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:90e5e7d8b87a34877f61c2b86d053db1c4f440b9054cf49573e3be5d6a674a47`  
		Last Modified: Tue, 21 Nov 2023 05:25:34 GMT  
		Size: 49.6 MB (49582225 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e495ee1fadcd2e4c2fada36131707a339a5b7d1cec776ac2808c8ca2eeb0b4e`  
		Last Modified: Sat, 02 Dec 2023 10:18:18 GMT  
		Size: 144.9 MB (144873896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4ce63ef6fa9be5f0f21cc9b5ad77bc48d36a1b7e42f9e5c41f25cce5a5e001`  
		Last Modified: Tue, 05 Dec 2023 18:40:38 GMT  
		Size: 83.6 MB (83579657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7198ed6958deb2cb40a9c444e340377a4b94cb10c8485cb5a33479f4b188c128`  
		Last Modified: Tue, 05 Dec 2023 18:40:29 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3977689540316e0ecde4ec3f5625bd31f3ecca65730c4433ca2612f7a2c6301c`  
		Last Modified: Tue, 05 Dec 2023 18:40:29 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1429-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7139003971331c9d6c1b2bcc03905182e654f50fa82588e80f7e3a1447b89ef3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.6 MB (276627085 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1746665e3ddd260f55df35aa5afa19351f3b1485673f0209b1e3c0a092b48a7e`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:20:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 08:52:59 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Sat, 02 Dec 2023 08:53:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 19:44:48 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 05 Dec 2023 19:44:48 GMT
WORKDIR /tmp
# Tue, 05 Dec 2023 19:45:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 05 Dec 2023 19:45:08 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 05 Dec 2023 19:45:08 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 05 Dec 2023 19:45:08 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 05 Dec 2023 19:45:08 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36f02d73e685ee8484944282e77adf6fe8d1c76564b2f529abde1e7d5f24493f`  
		Last Modified: Sat, 02 Dec 2023 09:07:54 GMT  
		Size: 143.7 MB (143681757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc74801225956d35bcf52bb5c65bddea80fa40f6e5cac640c1494abcd61ca62b`  
		Last Modified: Tue, 05 Dec 2023 19:54:37 GMT  
		Size: 83.3 MB (83331656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f76322495658cac9c103905d6cd71f96184b00a2991e9bf8312fd790e590be67`  
		Last Modified: Tue, 05 Dec 2023 19:54:30 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca01df16db74d8241b4d03b09742b9b4ad02831603a885a56748e008f6b171ce`  
		Last Modified: Tue, 05 Dec 2023 19:54:30 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
