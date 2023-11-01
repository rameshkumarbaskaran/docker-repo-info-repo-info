## `clojure:temurin-17-bullseye`

```console
$ docker pull clojure@sha256:6ac70de1738996a6d51480ef8d7dcd7555a6bea53b5eeb62bf4f2637e5429689
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:de8a2dea79c2910ef4626063b9ddbbb9b4370e163b12ebcecbfcf831dfc52f53
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.8 MB (271834128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14fc79fe777c4f0b0b8d0e5b89fbecceae983055eef68513583e27f788a8e944`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:59 GMT
ADD file:da3938f00f114fa8f5948fb7182da39c43e5ce57a334ba528681cb29aff0d2f6 in / 
# Wed, 01 Nov 2023 00:21:00 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:13:02 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:23:38 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:23:40 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:27:00 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 01 Nov 2023 01:27:00 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:27:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Nov 2023 01:27:17 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Nov 2023 01:27:17 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 01 Nov 2023 01:27:17 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Nov 2023 01:27:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:2f088d622efd8dbaa13d01eafd0aac8f9f33bb335edd3be897ae8059338c7bf7`  
		Last Modified: Wed, 01 Nov 2023 00:25:49 GMT  
		Size: 55.1 MB (55058052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcddd2ced9b19df156d3ed20c740fcd9fb5a05a9908fc224ced26758a55c9b92`  
		Last Modified: Wed, 01 Nov 2023 01:40:29 GMT  
		Size: 144.9 MB (144873903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d88846c00f5a79af6953005547c2cd73bb38bddd75226c1cfdfa401eea1b49f`  
		Last Modified: Wed, 01 Nov 2023 01:42:35 GMT  
		Size: 71.9 MB (71901155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc2655e1500bb6c85a13e1c6c5ac77e3a2e59621319bed2bdb8780dc927551cf`  
		Last Modified: Wed, 01 Nov 2023 01:42:28 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e43f152c1d9892a6753d7e9714dbdb81e74c0ee10cef7d9916d615bd9c3d9f24`  
		Last Modified: Wed, 01 Nov 2023 01:42:28 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:32f78ced4c56bd4321abc74f6c11d29129b8e02dff9773f196bed710ebc49391
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.4 MB (269407606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff833e86312330b6e4d88552035d51e07532c37a0935e71e48a76bd3cb418867`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:58 GMT
ADD file:e1a6c6c976e5e7c53eb2a7343a7a763b46e56828588535f4c79e63d6ec08198d in / 
# Wed, 11 Oct 2023 18:24:58 GMT
CMD ["bash"]
# Wed, 11 Oct 2023 18:45:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:06:01 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 31 Oct 2023 01:06:05 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 01:10:28 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Tue, 31 Oct 2023 01:10:29 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 01:10:43 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 31 Oct 2023 01:10:44 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 31 Oct 2023 01:10:44 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 31 Oct 2023 01:10:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 31 Oct 2023 01:10:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:dd0dc10f921f4b3b65b17f20d367374079e6cb4e26531624ee64caaaf4adcc28`  
		Last Modified: Wed, 11 Oct 2023 18:28:45 GMT  
		Size: 53.7 MB (53707810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90039ec2f4fe2b5cdd7b80a6438242b4a123b1c3880a1f5babfa9b9b475835ae`  
		Last Modified: Tue, 31 Oct 2023 01:22:59 GMT  
		Size: 143.7 MB (143681710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:306d1603e776ec776e692f6150eb41fb2e6fe0f5e11ad0484c0c49ffbb1ba8fa`  
		Last Modified: Tue, 31 Oct 2023 01:25:48 GMT  
		Size: 72.0 MB (72017073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d03ffe906bbe93bf60a3d857f801624400a5241a29b5acb73a48e094ff4c59`  
		Last Modified: Tue, 31 Oct 2023 01:25:40 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7ead4f9f246c02dff0cccf809899f8a58af98b58367330f0e8a1b2a775ac735`  
		Last Modified: Tue, 31 Oct 2023 01:25:40 GMT  
		Size: 397.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
