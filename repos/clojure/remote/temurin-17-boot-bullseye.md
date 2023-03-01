## `clojure:temurin-17-boot-bullseye`

```console
$ docker pull clojure@sha256:537931f480ec4e17e2a94c844b5dd638876f50b830373e1717a614d587de395d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:ac65a5672a18199eff906f6e3d5496b00aa8b78228e3789373b1ef8806efc966
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.7 MB (308667415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bfb665e56006367f10a6f6fb927fb17038964b2a5db0be0fb9f1b4963a1367b6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:05 GMT
ADD file:b03d13d345c29f69557f410c8504e748226756d1f48e5abdb63cd40179b2640c in / 
# Thu, 09 Feb 2023 03:20:05 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:22:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 09 Feb 2023 09:28:07 GMT
COPY dir:5cf52f938fe415b0022fbccb8cf978562c503c0b8313cc9dedf46c1c4edb35cf in /opt/java/openjdk 
# Thu, 09 Feb 2023 09:28:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 09:28:09 GMT
ENV BOOT_VERSION=2.8.3
# Thu, 09 Feb 2023 09:28:09 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Thu, 09 Feb 2023 09:28:10 GMT
WORKDIR /tmp
# Thu, 09 Feb 2023 09:28:15 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Thu, 09 Feb 2023 09:28:16 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Thu, 09 Feb 2023 09:28:16 GMT
ENV BOOT_AS_ROOT=yes
# Thu, 09 Feb 2023 09:28:32 GMT
RUN boot
# Thu, 09 Feb 2023 09:28:33 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Thu, 09 Feb 2023 09:28:33 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 09 Feb 2023 09:28:33 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:1e4aec178e0864db93a6f97a20bde3445871a4562c1801185eca1238d3a0e80d`  
		Last Modified: Thu, 09 Feb 2023 03:24:47 GMT  
		Size: 55.0 MB (55046771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f1f93ea764dcf05c1b60ac69868cb3e583d17322a93bc9f10b76202e4b5f41e`  
		Last Modified: Thu, 09 Feb 2023 09:40:17 GMT  
		Size: 192.4 MB (192438166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37a8558902508d4fae35ded92a8e32f7b9959c6e33056da0caf70930ad755eaa`  
		Last Modified: Thu, 09 Feb 2023 09:40:03 GMT  
		Size: 2.4 MB (2361758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97a5ea8e2a3a165cb7ccae28201238bc6c8ef8fd0f1ac319270805029e022f1e`  
		Last Modified: Thu, 09 Feb 2023 09:40:07 GMT  
		Size: 58.8 MB (58820317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b40f8fd55b9a7572326947ae8f9caa1023d3b08650ed13cedd7d412dd2965fa7`  
		Last Modified: Thu, 09 Feb 2023 09:40:03 GMT  
		Size: 403.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:ab3913a2c40a39a3e4c2cdf15a4cb114c548bf632110bdf40466149cee485bc4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **306.1 MB (306135447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68a71e4fc8335e45a0fdc4e2fd0bc252ec524ee1bff2104a7816ac6cd7cb794b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:30 GMT
ADD file:a6a1df499d0d5b07fb366d776a11c42ddee6261e2425a921041b38e868192770 in / 
# Wed, 01 Mar 2023 02:20:30 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 03:01:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Mar 2023 03:06:37 GMT
COPY dir:a1bd99c3d82513db94430c73467e1e5c69ea4624d0489571d594afe503e15dc5 in /opt/java/openjdk 
# Wed, 01 Mar 2023 03:06:41 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 03:06:41 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 01 Mar 2023 03:06:41 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 01 Mar 2023 03:06:41 GMT
WORKDIR /tmp
# Wed, 01 Mar 2023 03:06:46 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 01 Mar 2023 03:06:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 01 Mar 2023 03:06:46 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 01 Mar 2023 03:07:04 GMT
RUN boot
# Wed, 01 Mar 2023 03:07:04 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 01 Mar 2023 03:07:04 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Mar 2023 03:07:04 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0f5fe16b1836feccd4765ac5685fc7a7b9c73445cac94fc595d2ffbc3cb59a7a`  
		Last Modified: Wed, 01 Mar 2023 02:23:53 GMT  
		Size: 53.7 MB (53703215 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c097dd772364568afdeb11bfacd1919beea269a0a3d0b0f445e90ba4644f1775`  
		Last Modified: Wed, 01 Mar 2023 03:17:19 GMT  
		Size: 191.3 MB (191260437 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a24d4ed866cfd7225aa8154bdc517a3b758b9590daeffac17949f16375e98b7f`  
		Last Modified: Wed, 01 Mar 2023 03:17:08 GMT  
		Size: 2.4 MB (2350996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffc0f6210329b5e7f95e68a7da489bf1b132965e3c8a0f8c8d6b89a7f842eb21`  
		Last Modified: Wed, 01 Mar 2023 03:17:11 GMT  
		Size: 58.8 MB (58820399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bba8e3de6a82d421b96af37c4bbf29be56df24d73dec5abe8e95026e9205e46`  
		Last Modified: Wed, 01 Mar 2023 03:17:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
