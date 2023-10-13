## `clojure:tools-deps-1.11.1.1413-bookworm-slim`

```console
$ docker pull clojure@sha256:e22338ae6d457e67cc16461ba79beee9c95d032f05f0bbd5509e7cf9d5dd19a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:tools-deps-1.11.1.1413-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:4268b05b05e7464a942acce88930098c896623320414539512e29a2ef88ff0bb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259674562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f0bf1672aaf7fd741b148b72547f1584bfaed0c0a62199f095122802b20a380`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:37:30 GMT
COPY dir:beb55fdaac250289b56099cc1cfaeaa831b83d06c84fba6631b83f617b38e9e3 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:37:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:39:48 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 01:39:49 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:40:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 01:40:07 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 01:40:07 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:40:07 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:40:07 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbf5b61dfd183de50825dec7643ad1497c3b31cea76cc6371df03e0799742b5e`  
		Last Modified: Fri, 13 Oct 2023 01:50:50 GMT  
		Size: 158.6 MB (158590466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fce939c46c0b83b5ae0e68e12f03f8b3b3fe662c8380caf8894952def3357f88`  
		Last Modified: Fri, 13 Oct 2023 01:53:04 GMT  
		Size: 71.9 MB (71933206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14329d983a8a01f09a8cd776a131378e3893da67ee5ab078039f88d6c846d4b0`  
		Last Modified: Fri, 13 Oct 2023 01:52:55 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5436b4ea04b6afef88010aa7b562a5a12232ce443ec2cbb4cc1eaef1114c0c23`  
		Last Modified: Fri, 13 Oct 2023 01:52:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:tools-deps-1.11.1.1413-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:8362922522731d935ab88bbb5430edc4bbaf8d1fbc116318d5b81b848dcf469e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257717559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80f068f5b1a2581debf0ba955569d3c38e90587ef8808caf12114eb5a9e3439f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:59:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:07:34 GMT
COPY dir:dad71274c7bcfed298f99738003c621c42f9777a181dc5466113abef10d5813a in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:07:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:09:31 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 01:09:31 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:09:46 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 01:09:47 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 01:09:47 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:09:47 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:09:47 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa4870e05bb17c1acef9d3bc4bbd7fe1f561511aca70dea873243bd4aa799977`  
		Last Modified: Fri, 13 Oct 2023 01:19:07 GMT  
		Size: 156.8 MB (156842670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de0df66a67d3155af273806e4d616809229c8cec66efdecef7f807d852ee5906`  
		Last Modified: Fri, 13 Oct 2023 01:21:02 GMT  
		Size: 71.7 MB (71694592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fac2aeabfb53cf12cf517266577ed3b0025634249551a4bcc61b5cc26e433146`  
		Last Modified: Fri, 13 Oct 2023 01:20:55 GMT  
		Size: 615.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c4ad17ab01ec484010104dc01475cd593376954213add38bada7dcc5a1acda2`  
		Last Modified: Fri, 13 Oct 2023 01:20:55 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
