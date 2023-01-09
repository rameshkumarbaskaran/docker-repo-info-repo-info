## `clojure:temurin-19-boot-2.8.3-alpine`

```console
$ docker pull clojure@sha256:9d0bc2c10f99ff84dcc6b10725aada1bc33b09f90b8cfefafc3aa5bc2df8ce48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-19-boot-2.8.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:f37d494a0abe8c3f16f3c6fd500c14af6c7473daef91ad8e72af231f049d6ce1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **275.4 MB (275411406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d762b7c3cdd02742186db596ccfb38e7742b55ce1d4bee7a1265eedb21b08388`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Mon, 09 Jan 2023 17:05:20 GMT
ADD file:e4d600fc4c9c293efe360be7b30ee96579925d1b4634c94332e2ec73f7d8eca1 in / 
# Mon, 09 Jan 2023 17:05:20 GMT
CMD ["/bin/sh"]
# Mon, 09 Jan 2023 17:40:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Mon, 09 Jan 2023 17:40:09 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Jan 2023 17:40:09 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 09 Jan 2023 17:40:11 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Mon, 09 Jan 2023 17:42:15 GMT
ENV JAVA_VERSION=jdk-19.0.1+10
# Mon, 09 Jan 2023 17:42:31 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='76cfcdf47cdf24331b51939fd2840fd387cf62471da99e4718e2e42b486a9270';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19.0.1%2B10/OpenJDK19U-jdk_x64_alpine-linux_hotspot_19.0.1_10.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Mon, 09 Jan 2023 17:42:33 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 09 Jan 2023 17:42:34 GMT
CMD ["jshell"]
# Mon, 09 Jan 2023 21:33:52 GMT
ENV BOOT_VERSION=2.8.3
# Mon, 09 Jan 2023 21:33:52 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Mon, 09 Jan 2023 21:33:52 GMT
WORKDIR /tmp
# Mon, 09 Jan 2023 21:33:53 GMT
RUN apk add --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && sha256sum boot.sh && echo "0ccd697f2027e7e1cd3be3d62721057cbc841585740d0aaa9fbb485d7b1f17c3 *boot.sh" | sha256sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Mon, 09 Jan 2023 21:33:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Mon, 09 Jan 2023 21:33:54 GMT
ENV BOOT_AS_ROOT=yes
# Mon, 09 Jan 2023 21:34:13 GMT
RUN boot
# Mon, 09 Jan 2023 21:34:13 GMT
COPY file:0282db266eb050a3ad3609149efe2188243cb9f95c0b3e48a312ddef6c6bea02 in /usr/local/bin/entrypoint 
# Mon, 09 Jan 2023 21:34:14 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 09 Jan 2023 21:34:14 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:8921db27df2831fa6eaa85321205a2470c669b855f3ec95d5a3c2b46de0442c9`  
		Last Modified: Mon, 09 Jan 2023 17:05:45 GMT  
		Size: 3.4 MB (3370628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:846e3b32ee5a149e3ccb99051cdb52e96e11488293cdf72ee88168c88dd335c7`  
		Last Modified: Mon, 09 Jan 2023 17:44:40 GMT  
		Size: 12.0 MB (12020134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcb54b61233d188d9549a28cc575b4c988ce931a6c929eb03c115729b9cc3283`  
		Last Modified: Mon, 09 Jan 2023 17:47:09 GMT  
		Size: 200.3 MB (200303543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3118c2d15b6fdd4aeca06cb15ca8215967f8040b0e3b051a582aac0ee1cff475`  
		Last Modified: Mon, 09 Jan 2023 17:46:54 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ba315aaaa27cf043a11f9bff60f0f385dd67e73346fa8e5b4eaf4dfbb67de2`  
		Last Modified: Mon, 09 Jan 2023 21:40:18 GMT  
		Size: 896.1 KB (896073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae9822f5839c8b46666e4a9fd93c7368dfec13452500015f141e1fd91f940ca5`  
		Last Modified: Mon, 09 Jan 2023 21:40:21 GMT  
		Size: 58.8 MB (58820453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:703f47d37a0eb7459e41e88c517144acb803200106658d4bea89816eb37a60a0`  
		Last Modified: Mon, 09 Jan 2023 21:40:18 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
