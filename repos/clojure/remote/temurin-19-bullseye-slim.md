## `clojure:temurin-19-bullseye-slim`

```console
$ docker pull clojure@sha256:5af51255643f08f7ceb659d49f1f562225b6ed7171845c2660e2ead3d0c7a0a9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:9d814b2b1ed2ff80c06aaacd87f52278ac2a0c9860e09c2ea60533812c5d4725
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **293.7 MB (293734966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97e1d268f9fdf8067d8f5acc36594c14d981041136ba36a2a713d9746a745d8b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:40:49 GMT
COPY dir:49a4548ab030e4d26793e92b4d74537cf530961ce7b4083b8d383585c96415d5 in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:40:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:42:41 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 05 Oct 2022 01:42:42 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:42:59 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Oct 2022 01:42:59 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Oct 2022 01:42:59 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:43:00 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:43:00 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e7de30eb4e390cffd51e73ffc9a011f0684ec59cf871eeee7182269b9d6507`  
		Last Modified: Wed, 05 Oct 2022 01:52:11 GMT  
		Size: 200.8 MB (200843776 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6f8ac47c2794e80568a10a284ee491d4895440a65ab925f2f89e5d5e638d66`  
		Last Modified: Wed, 05 Oct 2022 01:53:12 GMT  
		Size: 61.5 MB (61470069 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2edace831af65f555fb8590c638d63ac697e9e22b21b444a6c2183ff3cfbd897`  
		Last Modified: Wed, 05 Oct 2022 01:53:04 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d7b49c455ba96353ff1bcddb4fff42d3d46657b01afdd13836851610967435`  
		Last Modified: Wed, 05 Oct 2022 01:53:05 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:a5f0db24fbac666e2407bb5137c66137e9ff92e08d05c37070f3709166c62f1d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291041079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a34e7f6d1baa32ee2b9cec462523bf18a7f4a6233b4786cf8678eb70e482cf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:05:12 GMT
COPY dir:58f6c37df253d3555e493197f96e3f21593e31d3faf1967e0a7b9d8f0ae9e30c in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:05:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:07:50 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 05 Oct 2022 01:07:50 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:08:08 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Oct 2022 01:08:09 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Oct 2022 01:08:10 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:08:10 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:08:11 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:451966db02aec3760efec5b561c0d414315fc69df240034894ad8f6005b785c0`  
		Last Modified: Wed, 05 Oct 2022 01:21:02 GMT  
		Size: 199.6 MB (199582873 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72cf6e09ac8c99308613bbf3c99a1ebf45d281d713b357afd36109c4b3edda85`  
		Last Modified: Wed, 05 Oct 2022 01:22:14 GMT  
		Size: 61.4 MB (61392795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d93f075f6138fbf20236b5e6f792fb4991b64642bb1a9d0d640171d18a6b899f`  
		Last Modified: Wed, 05 Oct 2022 01:22:06 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a082ac275ce363d35fda6fdfe3a43a940ce5dac26e49f8766c1e59df94fc59e1`  
		Last Modified: Wed, 05 Oct 2022 01:22:06 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
