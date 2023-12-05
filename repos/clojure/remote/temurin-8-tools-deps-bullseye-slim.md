## `clojure:temurin-8-tools-deps-bullseye-slim`

```console
$ docker pull clojure@sha256:1c8b5388dfda912a38553028a8e4842c08974794f6ae280d57725a36186fdb65
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:181e512cc7c6f8a3783f69f48ce622727bf9028e5c755f86603dfce1b91db851
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.7 MB (196723316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6d070386205ba07a27ae281e199aa321726cca86852a19369627822e4c8e015`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 10:09:58 GMT
COPY dir:a294625293e4e40913c98181a9aeff55bc5e737b728d424dfdc884f576bd8f8d in /opt/java/openjdk 
# Tue, 21 Nov 2023 10:09:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 18:23:50 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 05 Dec 2023 18:23:50 GMT
WORKDIR /tmp
# Tue, 05 Dec 2023 18:24:07 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 05 Dec 2023 18:24:07 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 05 Dec 2023 18:24:08 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e607a1b241277667349406a3ca3eff66cf7b380f86e562b7d5416eccee3f02`  
		Last Modified: Tue, 21 Nov 2023 10:29:36 GMT  
		Size: 103.6 MB (103598267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016f0b757e04280c9da58629393c0252cc98a4589c20fac7d171a37b649d43af`  
		Last Modified: Tue, 05 Dec 2023 18:36:56 GMT  
		Size: 61.7 MB (61706604 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc924bd883b29998d496e04d8a323b41c2a75b5a09b111c708965fb7487944b`  
		Last Modified: Tue, 05 Dec 2023 18:36:49 GMT  
		Size: 621.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:1d6316d3883c2904e891fc13f0404f67ac428d02f50232ab20b365abf1f97800
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.6 MB (194591746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0444730d031f7fe2d15b3205871d04f7d0e84b1ab100218e924edd98b04f961a`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:22:58 GMT
COPY dir:95966e8772805277b939f0a555f93ce7d7e01898449cdb0fb69c182fe80d4021 in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:23:00 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 19:40:38 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 05 Dec 2023 19:40:38 GMT
WORKDIR /tmp
# Tue, 05 Dec 2023 19:40:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 05 Dec 2023 19:40:53 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 05 Dec 2023 19:40:53 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bd2b923d8c4292133cf043f70ec351fc6a6ee467ca5e62b739d1be33ec0fa3d`  
		Last Modified: Tue, 21 Nov 2023 07:40:45 GMT  
		Size: 102.7 MB (102701531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:721790452f85ea5c1f190a61e2029f39fb2cfad62fa4fab2cc4798d9a11287a2`  
		Last Modified: Tue, 05 Dec 2023 19:51:30 GMT  
		Size: 61.8 MB (61825472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330792c5217c675d54945164ee4a42f7114a8d1d40b3d4b0f514883801896c61`  
		Last Modified: Tue, 05 Dec 2023 19:51:23 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
