## `groovy:jdk11-alpine`

```console
$ docker pull groovy@sha256:6e00dde8de988fb82cfc0f6eee81a6ac46e36223ce693a5e1692f9faa68a5d14
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `groovy:jdk11-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:90334af271e8e182219927d5bd14175881cdc7306d136e5f26bc3a94cd95e4c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **252.6 MB (252587680 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b87b8cb733b415f3d97945f5753af506cf0c6db104ede03e8849f0f613143c6b`
-	Default Command: `["groovysh"]`

```dockerfile
# Tue, 09 Aug 2022 17:19:53 GMT
ADD file:2a949686d9886ac7c10582a6c29116fd29d3077d02755e87e111870d63607725 in / 
# Tue, 09 Aug 2022 17:19:53 GMT
CMD ["/bin/sh"]
# Thu, 11 Aug 2022 19:19:38 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 11 Aug 2022 19:19:38 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Aug 2022 19:19:38 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 11 Aug 2022 19:19:40 GMT
RUN apk add --no-cache fontconfig libretls musl-locales musl-locales-lang ttf-dejavu tzdata zlib     && rm -rf /var/cache/apk/*
# Wed, 24 Aug 2022 19:19:58 GMT
ENV JAVA_VERSION=jdk-11.0.16.1+1
# Wed, 24 Aug 2022 19:20:14 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='327b3bfd1c14e15bf6c7fb4d0c6c3f9406c1282a16e24b1424215d764f687cb6';          BINARY_URL='https://github.com/adoptium/temurin11-binaries/releases/download/jdk-11.0.16.1%2B1/OpenJDK11U-jdk_x64_alpine-linux_hotspot_11.0.16.1_1.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;
# Wed, 24 Aug 2022 19:20:17 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 24 Aug 2022 19:20:17 GMT
CMD ["jshell"]
# Wed, 24 Aug 2022 20:23:06 GMT
CMD ["groovysh"]
# Wed, 24 Aug 2022 20:23:07 GMT
ENV GROOVY_HOME=/opt/groovy
# Wed, 24 Aug 2022 20:23:07 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy
# Wed, 24 Aug 2022 20:23:07 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Wed, 24 Aug 2022 20:23:07 GMT
WORKDIR /home/groovy
# Mon, 19 Sep 2022 21:26:23 GMT
ENV GROOVY_VERSION=3.0.13
# Mon, 19 Sep 2022 21:26:35 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm -rf "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy"
# Mon, 19 Sep 2022 21:26:35 GMT
USER groovy
# Mon, 19 Sep 2022 21:26:36 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:213ec9aee27d8be045c6a92b7eac22c9a64b44558193775a1a7f626352392b49`  
		Last Modified: Tue, 09 Aug 2022 14:25:13 GMT  
		Size: 2.8 MB (2806054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:107abfa4a9656cc98051eebaf02de090526191f4d53ab3733605b34f84513224`  
		Last Modified: Thu, 11 Aug 2022 19:29:52 GMT  
		Size: 12.1 MB (12050073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29496409cb750e4cd34c0abc2a0af5d4a8c9983eb3a8de05281f672289d5fb1e`  
		Last Modified: Wed, 24 Aug 2022 19:25:48 GMT  
		Size: 193.5 MB (193457720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0469b5bbda2d25b40afdbe052d9452b8af0246a6fc7abcea846b5ff7512de5b8`  
		Last Modified: Wed, 24 Aug 2022 19:25:34 GMT  
		Size: 179.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:868478a838840a736f036ebe3cbc210c6f021e54cffbad0897ebe91154ed4a81`  
		Last Modified: Wed, 24 Aug 2022 20:26:55 GMT  
		Size: 1.4 KB (1357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668dc51791a8b0ae846fc9f825e9d6f943eda7c2fb42520e8db4e37e9fa52f2b`  
		Last Modified: Mon, 19 Sep 2022 21:29:27 GMT  
		Size: 44.3 MB (44272126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:376f5dd796d0bea0d8a4e23de466bcc33ef1471ae66a3cbe3156a54469491cd5`  
		Last Modified: Mon, 19 Sep 2022 21:29:24 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
