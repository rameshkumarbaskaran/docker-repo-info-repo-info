## `clojure:temurin-20-tools-deps-alpine`

```console
$ docker pull clojure@sha256:40c0ead83a7da92916529cd3d0d223d159a2d1be93a8f33e30256a3fff200cfb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-20-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:381450d831087685550641289242244f2957bafd306c827fbd452927717df3c7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **192.6 MB (192597956 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f609bc67ea851b4a76e6ed6b4fc54cff6e25d314b2071a9a2759b5caa3071974`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Mon, 07 Aug 2023 19:20:20 GMT
ADD file:32ff5e7a78b890996ee4681cc0a26185d3e9acdb4eb1e2aaccb2411f922fed6b in / 
# Mon, 07 Aug 2023 19:20:20 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 19:19:44 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 08 Aug 2023 19:19:44 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Aug 2023 19:19:44 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Mon, 14 Aug 2023 18:09:08 GMT
RUN apk add --no-cache fontconfig java-cacerts bash libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Mon, 14 Aug 2023 18:11:21 GMT
ENV JAVA_VERSION=jdk-20.0.2+9
# Mon, 14 Aug 2023 18:11:32 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='b03aced4b7a1c49bc00297e35e45480fd03818862b93e17e1551a3b721e89306';          BINARY_URL='https://github.com/adoptium/temurin20-binaries/releases/download/jdk-20.0.2%2B9/OpenJDK20U-jdk_x64_alpine-linux_hotspot_20.0.2_9.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Mon, 14 Aug 2023 18:11:35 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Mon, 14 Aug 2023 18:11:35 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Mon, 14 Aug 2023 18:11:35 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Mon, 14 Aug 2023 18:11:35 GMT
CMD ["jshell"]
# Mon, 14 Aug 2023 20:12:37 GMT
ENV CLOJURE_VERSION=1.11.1.1347
# Mon, 14 Aug 2023 20:12:37 GMT
WORKDIR /tmp
# Mon, 14 Aug 2023 20:12:41 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "d9158bf3a1d92fbf8551656e47a86f42e93d10f1db9defa2124bfee206ce8c8f *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Mon, 14 Aug 2023 20:12:41 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 14 Aug 2023 20:12:41 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Mon, 14 Aug 2023 20:12:41 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 14 Aug 2023 20:12:42 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:7264a8db6415046d36d16ba98b79778e18accee6ffa71850405994cffa9be7de`  
		Last Modified: Mon, 07 Aug 2023 19:20:54 GMT  
		Size: 3.4 MB (3401613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:994e83f716a0db024fb37caf707eae5af27172a0fffb691c6e7b53bb7fc5b3ab`  
		Last Modified: Mon, 14 Aug 2023 18:13:07 GMT  
		Size: 9.3 MB (9276497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4f448552bb15ae7982f30b7bf23aac44717ed6365a7a879d53de4c79d78622d`  
		Last Modified: Mon, 14 Aug 2023 18:18:33 GMT  
		Size: 152.9 MB (152930841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bdfae8054477c91597828697217510a2f61d4c33e790ad929e88b8d9903e2a`  
		Last Modified: Mon, 14 Aug 2023 18:18:21 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed7f96622c1da1429f1ec4655cd421ba42bf1bfc9532f6eb6d5f12679b6eb955`  
		Last Modified: Mon, 14 Aug 2023 18:18:21 GMT  
		Size: 734.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c61c41c6d742c02f9846ada56a8aceb0ff5b67c17ee5979d61302812aa5b642`  
		Last Modified: Mon, 14 Aug 2023 20:22:22 GMT  
		Size: 27.0 MB (26987071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f77eb42b41da881f7b9b473a7c9cc3aac6e1a280936dbe3333cb6c0c05799bc`  
		Last Modified: Mon, 14 Aug 2023 20:22:19 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d5c24906ea77779d8c77caf4490fd6cb351f427e4322c2eeffef6538be8faf2`  
		Last Modified: Mon, 14 Aug 2023 20:22:19 GMT  
		Size: 404.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
