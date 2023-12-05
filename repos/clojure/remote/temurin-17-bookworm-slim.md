## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:75d1a2b3c0cf235c9db5aa309d7076a821cbf4ad5d00a8a61a3bf23bbcc78a85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:0b7a722cc2d1f0c663e29b8af690ac808c301b6b7af88d8388269d39fd3e01d7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **246.2 MB (246168791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc972f0a17b08c5859986dba40febd0707dd8eb4cd32f44ba025e16b7969943`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:37 GMT
ADD file:d261a6f6921593f1e0b3f472ab1b1822e2c6deb0b369200f0b3370556bfad017 in / 
# Tue, 21 Nov 2023 05:21:37 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:08:59 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 10:02:19 GMT
COPY dir:e13dbcd57950f4d4d23f4aba8428b6fbbf838d8f4801d32a25e344d37d33c37e in /opt/java/openjdk 
# Sat, 02 Dec 2023 10:02:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 18:29:21 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 05 Dec 2023 18:29:21 GMT
WORKDIR /tmp
# Tue, 05 Dec 2023 18:29:38 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 05 Dec 2023 18:29:39 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 05 Dec 2023 18:29:39 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 05 Dec 2023 18:29:39 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 05 Dec 2023 18:29:39 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1f7ce2fa46ab3942feabee654933948821303a5a821789dddab2d8c3df59e227`  
		Last Modified: Tue, 21 Nov 2023 05:25:58 GMT  
		Size: 29.1 MB (29149908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0885deee54f6adeddb534e83c7fede08982afb277d99e56cc4f45a0a4902c5d`  
		Last Modified: Sat, 02 Dec 2023 10:18:38 GMT  
		Size: 144.9 MB (144873901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a80db499f42aa49344ec688dcc644e36b0e56943631a1a6aa8fb7ebcc9df99`  
		Last Modified: Tue, 05 Dec 2023 18:40:57 GMT  
		Size: 72.1 MB (72143966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b38547c72cb109caa22207dc1db305037a7c48a4e28f9831debd7a18f021b61a`  
		Last Modified: Tue, 05 Dec 2023 18:40:49 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa0ee5073123f7d845744ccbc0d5df25a81bfe9c815e47064a32068419eccb52`  
		Last Modified: Tue, 05 Dec 2023 18:40:49 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5d46e74e63828440ea5dfd502d567c4ef2aec83e517bcacb42a5e51e8a256dee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.8 MB (244759582 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d87539e62257619e00b1f58e944c1a676adbc076f91966caf67d9e4df6905333`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:06 GMT
ADD file:869c7d0747a17c53715581a2e862992eb8516c7f45f167821dfa80966a4870d1 in / 
# Tue, 21 Nov 2023 06:27:06 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:01 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 08:53:31 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Sat, 02 Dec 2023 08:53:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 19:45:11 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 05 Dec 2023 19:45:11 GMT
WORKDIR /tmp
# Tue, 05 Dec 2023 19:45:27 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 05 Dec 2023 19:45:27 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 05 Dec 2023 19:45:28 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 05 Dec 2023 19:45:28 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 05 Dec 2023 19:45:28 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2c6d21737d8318aa15c4cc838475029a5efc36c0429e3d8da80d97d0b96d9aaf`  
		Last Modified: Tue, 21 Nov 2023 06:30:30 GMT  
		Size: 29.2 MB (29179277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5174505a545417ed296a7213ad24367c7222fd420ece7b5f7b0bd62c3811e57`  
		Last Modified: Sat, 02 Dec 2023 09:08:12 GMT  
		Size: 143.7 MB (143681757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:773042e8592c96fe75df3b4f3af14c6417a997c9c19a4d2a264c2f267a9692e3`  
		Last Modified: Tue, 05 Dec 2023 19:54:55 GMT  
		Size: 71.9 MB (71897531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79c27fea7c1b905a1364b178278173f369642b10b7c6f0fa38c3331ebc7a1924`  
		Last Modified: Tue, 05 Dec 2023 19:54:49 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef3b3332c306abcaa3c8488143ed0051f29dd830907315cc18c63ad4031518aa`  
		Last Modified: Tue, 05 Dec 2023 19:54:49 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
