## `clojure:temurin-8-tools-deps-bookworm-slim`

```console
$ docker pull clojure@sha256:6b92df458747bd9d9d560039198294702bb77733102e545123302fd943b4b9fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:b9678771f9540bb237943848e1660446e1ef36cbac0d2774dc311642775567a7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **204.7 MB (204669040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3175efccfce06df6cefe897baa452fa01a15e25d142ee59df046268a3c1bafa`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:28:08 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:28:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:30:10 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 01:30:10 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:30:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 01:30:29 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 01:30:29 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4d25ccb95233478198757a427ee2f81fab3092542dec1b3fbcd1c703e7241ae`  
		Last Modified: Fri, 13 Oct 2023 01:44:37 GMT  
		Size: 103.6 MB (103585059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40f9571064c9cc5c9bf56874b4c550b1bbf803f6de9382fdfc2da97ae8bceae3`  
		Last Modified: Fri, 13 Oct 2023 01:45:49 GMT  
		Size: 71.9 MB (71933489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fe93980cdccb9e03a8bc944d731347780a6d069e60b32a1ad99860eb8a4af2a`  
		Last Modified: Fri, 13 Oct 2023 01:45:41 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7c0d6a96888b8bd75770039b20fc46aa0c0a5400ee56c2e3970a4045a908960f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.6 MB (203565207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78921bbfce0383eddb2925654b56d4a8a59be1e2fe813599e1e2c56b1169e1d5`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:59:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 00:59:52 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Fri, 13 Oct 2023 00:59:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:01:37 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 01:01:37 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:01:52 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 01:01:53 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 01:01:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a57b690f142bf71ee0e56d780ce627f1f5444df7e8057dfc8cd7d677acefac58`  
		Last Modified: Fri, 13 Oct 2023 01:13:33 GMT  
		Size: 102.7 MB (102690507 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3bf481c742bee00e6fa9dbe6a7c8876e77bc87f28e0c47f1094a2239da9479`  
		Last Modified: Fri, 13 Oct 2023 01:14:35 GMT  
		Size: 71.7 MB (71694799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eaf872741840b42413430647d73062c667ed76da8f74f6039a688f0c1399a2e`  
		Last Modified: Fri, 13 Oct 2023 01:14:29 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
