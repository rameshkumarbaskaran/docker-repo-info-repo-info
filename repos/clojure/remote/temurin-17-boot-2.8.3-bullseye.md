## `clojure:temurin-17-boot-2.8.3-bullseye`

```console
$ docker pull clojure@sha256:bdb36527d736f76338993de22c975895a135cee7afda1fed81327940274192ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:9b35826072a3553afc692ce4440e1d3aded4d2d782855e788d6e6f31174d30fa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **308.4 MB (308366854 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:81e8dbf915e9a335b1755da4018f57f5293324852b4a50544f720d56ed3715b3`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:42 GMT
ADD file:26702ba2c3e94cb21cdb3c550cf01cf848823d160f3417b559116d4c718e5df0 in / 
# Tue, 25 Oct 2022 01:43:42 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:32:27 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:14:51 GMT
COPY dir:58adc2a0817e042696a68e5783ea1d9db89b18bd838f66f2ddc3c99acbc84106 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:14:52 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:14:52 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 02 Nov 2022 20:14:53 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 02 Nov 2022 20:14:53 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:14:58 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 02 Nov 2022 20:14:59 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Nov 2022 20:14:59 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 02 Nov 2022 20:15:18 GMT
RUN boot
# Wed, 02 Nov 2022 20:15:18 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 02 Nov 2022 20:15:18 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Nov 2022 20:15:18 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:17c9e6141fdb3387e5a1c07d4f9b6a05ac1498e96029fa3ea55470d4504f7770`  
		Last Modified: Tue, 25 Oct 2022 01:47:28 GMT  
		Size: 55.0 MB (55046332 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a743048e6b028bb91e927d7a70b42b7aa572cabf53bf650a7aa0bc002e2463`  
		Last Modified: Wed, 02 Nov 2022 20:27:22 GMT  
		Size: 192.1 MB (192137487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ecbeb13d42d773e7d3a42494e47b57d9c1155f71d965f1709adccd89ab1c75`  
		Last Modified: Wed, 02 Nov 2022 20:27:08 GMT  
		Size: 2.4 MB (2362142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4168bc5e0d8a4ebcf3dd1fc13c43515114a62962d92d70f3b9b257668906180d`  
		Last Modified: Wed, 02 Nov 2022 20:27:12 GMT  
		Size: 58.8 MB (58820492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4ac8055adadab61a333160e9dbcd2ee308f360484c7d67b3a1a5b6edb39a089`  
		Last Modified: Wed, 02 Nov 2022 20:27:08 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-boot-2.8.3-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:85dd94931ba91510f690e0daf6faf75800f8739fb7999a937fee7ecb9a48f97e
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **305.8 MB (305779345 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6dabeddc145a9a7a6296e74d003d482a92e367d6dfe4de03eacbcb8044f3ae2`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Tue, 25 Oct 2022 05:45:55 GMT
ADD file:b16745ece8ef84c028d7e9ac4bf026ac64f885d4170bfcc9d435f237144a1b99 in / 
# Tue, 25 Oct 2022 05:45:56 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 23:53:17 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 20:50:08 GMT
COPY dir:527d7e3a362e3a52ce4ecffbf599fb9423f60f5fcdccc64d800fcfec8666f5b8 in /opt/java/openjdk 
# Wed, 02 Nov 2022 20:50:12 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 20:50:12 GMT
ENV BOOT_VERSION=2.8.3
# Wed, 02 Nov 2022 20:50:12 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Wed, 02 Nov 2022 20:50:12 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:50:17 GMT
RUN apt-get update && apt-get install -y make wget && rm -rf /var/lib/apt/lists/* && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apt-get purge -y --auto-remove wget
# Wed, 02 Nov 2022 20:50:17 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Nov 2022 20:50:17 GMT
ENV BOOT_AS_ROOT=yes
# Wed, 02 Nov 2022 20:50:34 GMT
RUN boot
# Wed, 02 Nov 2022 20:50:35 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Wed, 02 Nov 2022 20:50:35 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Nov 2022 20:50:35 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8e1d92e7d04d2a9a9880cb45dc3c32c2805912cd86abed96d0ada3ff28748205`  
		Last Modified: Tue, 25 Oct 2022 05:48:40 GMT  
		Size: 53.7 MB (53701966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4deacd3ca10c3fa2537fe32ec939ce8fdafac62c9fc22abfa01f8f33e869e008`  
		Last Modified: Wed, 02 Nov 2022 21:01:00 GMT  
		Size: 190.9 MB (190904092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3fbbe857722b3480d76c518fd24a0195953984876cac2733d9ecda620a798c`  
		Last Modified: Wed, 02 Nov 2022 21:01:14 GMT  
		Size: 2.4 MB (2352307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f55ccbc46c89cf39923ea4216512793e6bd2454d3c82202d76c1a99e9bbdc40`  
		Last Modified: Wed, 02 Nov 2022 21:00:51 GMT  
		Size: 58.8 MB (58820580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f06631cb62fe8cda266898d7364437541f09a89f2deab5b0ea356b49b13364f`  
		Last Modified: Wed, 02 Nov 2022 21:00:48 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
