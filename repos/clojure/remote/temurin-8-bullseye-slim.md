## `clojure:temurin-8-bullseye-slim`

```console
$ docker pull clojure@sha256:c5b5b6033b98d348885fd557e36f641dcdc4cab3431fdaa4353805a8ad3ed2d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:971c5d3217e1c0af88fcd99ed91a988b17b7c8187b8acd1574667a3a17c8685c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **196.5 MB (196504541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9fe6fc1467b34b40e62727e83495e527cf5b0fd66d1d1583a3cfdd5736ae3c8`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 27 Jul 2023 23:25:07 GMT
ADD file:3d726bf0abbc08d6dda026cc406cdfb529deb60071641d164de28fcd62d1c1c0 in / 
# Thu, 27 Jul 2023 23:25:07 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 02:22:05 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 01 Aug 2023 22:05:00 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Tue, 01 Aug 2023 22:05:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 14 Aug 2023 23:21:06 GMT
ENV CLOJURE_VERSION=1.11.1.1386
# Mon, 14 Aug 2023 23:21:06 GMT
WORKDIR /tmp
# Mon, 14 Aug 2023 23:21:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3a09e2df4d3abd89b5b1286af0133a36a525ff3acfe1432f98b5c24b170940e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 14 Aug 2023 23:21:23 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 14 Aug 2023 23:21:23 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:1d5252f66ea9b661aceca1027b3d7ca259a50608261a25b51148119ecf086932`  
		Last Modified: Thu, 27 Jul 2023 23:30:08 GMT  
		Size: 31.4 MB (31417602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:567fa53d58445e9c2f0ed4e6f4625dceeac843a03cecf021904aa8458a56dbcc`  
		Last Modified: Tue, 01 Aug 2023 22:15:34 GMT  
		Size: 103.6 MB (103585037 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b58931c832a1959fe68325abd3c14f07945fe6d19ba3e6fb04ceebbcf3a05a`  
		Last Modified: Mon, 14 Aug 2023 23:29:33 GMT  
		Size: 61.5 MB (61501284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d81170cad2daaa25de9ce17c98f3f05cc1976f245ec29527a71f96f552b5208`  
		Last Modified: Mon, 14 Aug 2023 23:29:25 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:84df4a11bea4af6b1e297f1db962311f4fb48ce5efb0ad66365df78f87819800
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **194.4 MB (194370278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3bb925ec40667785ac65ee14005467fe4381929ae8ad63985f0e0ecf5e26901`
-	Default Command: `["clj"]`

```dockerfile
# Thu, 27 Jul 2023 23:43:15 GMT
ADD file:085ecd2f941de953afe5513a41a37412d72cbafd982de581ebd2309b3772b51e in / 
# Thu, 27 Jul 2023 23:43:15 GMT
CMD ["bash"]
# Fri, 28 Jul 2023 14:25:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 01 Aug 2023 22:11:02 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Tue, 01 Aug 2023 22:11:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 15 Aug 2023 00:30:27 GMT
ENV CLOJURE_VERSION=1.11.1.1386
# Tue, 15 Aug 2023 00:30:27 GMT
WORKDIR /tmp
# Tue, 15 Aug 2023 00:30:41 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "3a09e2df4d3abd89b5b1286af0133a36a525ff3acfe1432f98b5c24b170940e8 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 15 Aug 2023 00:30:42 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 15 Aug 2023 00:30:42 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:795b5d192ab1819e75375fead3f2f931bd86046e3308224944f16a5ec3b97424`  
		Last Modified: Thu, 27 Jul 2023 23:47:14 GMT  
		Size: 30.1 MB (30062831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbeec71f6c091e1e46dc0373eb0d5b1f4661ddef9abd0393e4f9896f82a717d1`  
		Last Modified: Tue, 01 Aug 2023 22:18:26 GMT  
		Size: 102.7 MB (102690458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a934ed270a816f8b2cc9b139f3c24a51af90d25fe578e491c501d96c43dc6c`  
		Last Modified: Tue, 15 Aug 2023 00:37:14 GMT  
		Size: 61.6 MB (61616370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:568516a4e23243ee7d952b7e2f2155310c1b7af1e78fbe114dbe0b9599759955`  
		Last Modified: Tue, 15 Aug 2023 00:37:08 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
