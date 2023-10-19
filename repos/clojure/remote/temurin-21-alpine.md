## `clojure:temurin-21-alpine`

```console
$ docker pull clojure@sha256:b8309de1785ec59e30ca3a17072be56cc5fd483adf43c0e8176bf842319aa14a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `clojure:temurin-21-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:df9061b056300f3513407221ba4f5a60d330660563a6ecadcac62570a787bacd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **197.3 MB (197306519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31c1905dbc60f55b17aa53abf750bf6334b1751defb078b7b50298b9b16831b6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 19 Oct 2023 02:50:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 19 Oct 2023 02:50:15 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 19 Oct 2023 02:50:15 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 19 Oct 2023 02:50:17 GMT
RUN apk add --no-cache fontconfig java-cacerts bash libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Thu, 19 Oct 2023 02:53:10 GMT
ENV JAVA_VERSION=jdk-21+35
# Thu, 19 Oct 2023 02:53:22 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        aarch64|arm64)          ESUM='3f8e5b0447d2dd711f12edda611ed1cf9aab4ca53c8fe32fca8fb1e6fee41c12';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_aarch64_alpine-linux_hotspot_21_35.tar.gz';          ;;        amd64|x86_64)          ESUM='4fd74f93f0b1a94d8471e0ed801fe9d938f7471f6efe8791880c85e7716c943f';          BINARY_URL='https://github.com/adoptium/temurin21-binaries/releases/download/jdk-21%2B35/OpenJDK21U-jdk_x64_alpine-linux_hotspot_21_35.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm -f /tmp/openjdk.tar.gz ${JAVA_HOME}/lib/src.zip;
# Thu, 19 Oct 2023 02:53:24 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 19 Oct 2023 02:53:24 GMT
COPY file:8b8864b3e02a33a579dc216fd51b28a6047bc8eeaa03045b258980fe0cf7fcb3 in /__cacert_entrypoint.sh 
# Thu, 19 Oct 2023 02:53:24 GMT
ENTRYPOINT ["/__cacert_entrypoint.sh"]
# Thu, 19 Oct 2023 02:53:24 GMT
CMD ["jshell"]
# Thu, 19 Oct 2023 07:09:47 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 19 Oct 2023 07:09:47 GMT
WORKDIR /tmp
# Thu, 19 Oct 2023 07:09:52 GMT
RUN apk add --no-cache curl bash make git && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Thu, 19 Oct 2023 07:09:52 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 19 Oct 2023 07:09:52 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 19 Oct 2023 07:09:52 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 19 Oct 2023 07:09:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f42efc8ffaa989c4197765e315c7d229fc40528c139b6be6a50e459fab1b640e`  
		Last Modified: Thu, 19 Oct 2023 02:55:23 GMT  
		Size: 9.3 MB (9276490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf76d6f40cd7ca863a644a0ca98e4600f322786a73de7a9bf1c175d6d95785b2`  
		Last Modified: Thu, 19 Oct 2023 02:59:40 GMT  
		Size: 157.6 MB (157630052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c035f235584ff3c6cb322faae306b071925722bfb8f2748f8ce3aaa2919be110`  
		Last Modified: Thu, 19 Oct 2023 02:59:26 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd0f3b1ff9d2c30fd49b405bac85864ddd3cac27c25cd99c361aa77fb8a13466`  
		Last Modified: Thu, 19 Oct 2023 02:59:26 GMT  
		Size: 733.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a2e704ffb38630c1036946c5e67efb21aa4165a8aa2775ab279441e7ada932`  
		Last Modified: Thu, 19 Oct 2023 07:14:46 GMT  
		Size: 27.0 MB (26996071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80337f81cbf1de1757a82446220f28b57eddfac5233da044035237ad6ce318ed`  
		Last Modified: Thu, 19 Oct 2023 07:14:43 GMT  
		Size: 624.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8d74df72a8eb341f793f19b67079e2401aecb026bf2c52b35e810fb9445443a`  
		Last Modified: Thu, 19 Oct 2023 07:14:43 GMT  
		Size: 407.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
