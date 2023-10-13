## `clojure:temurin-11-boot-bookworm`

```console
$ docker pull clojure@sha256:97b09ed8d41e5d9ca98eec7cf03cdbcc80d424383fc5fe8b2965a4d31458b8cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-boot-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:00598211bc067baa035f3f7b2983ac7c7dcddbe3ec3e32c5a1352b57ccb7a4f3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **258.8 MB (258761146 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:631f1b553238fe3e3d604ba974e7e019b0b590944595b47e104e415821611461`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:26:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:30:47 GMT
COPY dir:ac445271830068829c3bd23eb1c86ee02cd9bb1649e3c49d8839a5a364b933c2 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:30:48 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:30:48 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 01:30:48 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:30:48 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:30:55 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 01:30:55 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:30:55 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 01:31:13 GMT
RUN boot
# Fri, 13 Oct 2023 01:31:13 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aebae23ea933618b87b53119336b32efadee3d48ee7cd73f6509a2ede465084`  
		Last Modified: Fri, 13 Oct 2023 01:46:18 GMT  
		Size: 144.8 MB (144825980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9dd5fa20f7a3734692dd9d76a5d67a6873143e8ea5bd24ab19e168a37004c77`  
		Last Modified: Fri, 13 Oct 2023 01:46:08 GMT  
		Size: 5.5 MB (5532564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83d848d31e997098d200b59309992e6b148dcd41123a2d05372bfc60d237f0af`  
		Last Modified: Fri, 13 Oct 2023 01:46:11 GMT  
		Size: 58.8 MB (58820378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-boot-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:4ce5a92561193005804d61eadeb482061905ebb86426330a9de0038e4db4b923
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **255.4 MB (255359313 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc4ec69b8300ac009fc16d3c54d0593b5d27936b0c482ae894ac4912f6e91149`
-	Default Command: `["boot","repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:02:05 GMT
COPY dir:17ac9e9d4b4d03adb229076835643ca11e6db9d9c122779536bfc61364556722 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:02:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:02:08 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 13 Oct 2023 01:02:08 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 13 Oct 2023 01:02:08 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:02:14 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Fri, 13 Oct 2023 01:02:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 13 Oct 2023 01:02:14 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 13 Oct 2023 01:02:31 GMT
RUN boot
# Fri, 13 Oct 2023 01:02:31 GMT
CMD ["boot" "repl"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98472fc4a9307f34b7d88432e2590b0c37a40b019f0ab081812f6d3b2d7968be`  
		Last Modified: Fri, 13 Oct 2023 01:15:04 GMT  
		Size: 141.6 MB (141570720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a34f20d508c6c5a86c94fe44a5150f374e611574539092f2bb5359405b846c8`  
		Last Modified: Fri, 13 Oct 2023 01:14:54 GMT  
		Size: 5.4 MB (5355553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb36afa46f3d62f78d8eaef0c50b43571e49f677787827f196b5e393df77593`  
		Last Modified: Fri, 13 Oct 2023 01:14:57 GMT  
		Size: 58.8 MB (58820462 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
