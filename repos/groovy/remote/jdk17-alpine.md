## `groovy:jdk17-alpine`

```console
$ docker pull groovy@sha256:886a96b1c4682ad5c7ce931dff9d1e9ff789290fd1bf4a626a8a175a1efe3b79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `groovy:jdk17-alpine` - linux; amd64

```console
$ docker pull groovy@sha256:ceb47bb25ad5698d8d78cfaaa070c67443f05d87e23c19df831d1e6536d63a9f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **239.4 MB (239361004 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c94c9925c37b5f4a125ae6ae4181b359f96d8d2f08fdc036a615d2a615cdf8e`
-	Default Command: `["groovysh"]`

```dockerfile
# Thu, 17 Mar 2022 04:01:58 GMT
ADD file:cf4b631a115c2bbfbd81cad2d3041bceb64a8136aac92ba8a63b6c51d60af764 in / 
# Thu, 17 Mar 2022 04:01:59 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 08:42:16 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Thu, 17 Mar 2022 08:42:17 GMT
RUN apk add --no-cache tzdata musl-locales musl-locales-lang     && rm -rf /var/cache/apk/*
# Thu, 17 Mar 2022 08:44:31 GMT
ENV JAVA_VERSION=jdk-17.0.2+8
# Thu, 17 Mar 2022 08:45:00 GMT
RUN set -eux;     ARCH="$(apk --print-arch)";     case "${ARCH}" in        amd64|x86_64)          ESUM='a07cc09db0e71d06ea388902f8fcea8151b2b9ba51a16f75f9c0a3ac9acbfb61';          BINARY_URL='https://github.com/adoptium/temurin17-binaries/releases/download/jdk-17.0.2%2B8/OpenJDK17U-jdk_x64_alpine-linux_hotspot_17.0.2_8.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p /opt/java/openjdk; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory /opt/java/openjdk 	      --strip-components 1 	      --no-same-owner 	  ;     rm -rf /tmp/openjdk.tar.gz;
# Thu, 17 Mar 2022 08:45:00 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 08:45:01 GMT
RUN echo Verifying install ...     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Thu, 17 Mar 2022 08:45:01 GMT
CMD ["jshell"]
# Fri, 18 Mar 2022 23:29:10 GMT
CMD ["groovysh"]
# Fri, 18 Mar 2022 23:29:10 GMT
ENV GROOVY_HOME=/opt/groovy
# Fri, 18 Mar 2022 23:29:10 GMT
RUN set -o errexit -o nounset     && echo "Adding groovy user and group"     && addgroup --system --gid 1000 groovy     && adduser --system --ingroup groovy --uid 1000 --shell /bin/ash groovy     && mkdir --parents /home/groovy/.groovy/grapes     && chown -R groovy:groovy /home/groovy     && chmod -R 1777 /home/groovy         && echo "Symlinking root .groovy to groovy .groovy"     && ln -s /home/groovy/.groovy /root/.groovy
# Fri, 18 Mar 2022 23:29:11 GMT
VOLUME [/home/groovy/.groovy/grapes]
# Fri, 18 Mar 2022 23:29:11 GMT
WORKDIR /home/groovy
# Fri, 18 Mar 2022 23:29:11 GMT
ENV GROOVY_VERSION=3.0.10
# Fri, 18 Mar 2022 23:29:23 GMT
RUN set -o errexit -o nounset     && echo "Installing build dependencies"     && apk add --no-cache --virtual .build-deps         gnupg         && echo "Downloading Groovy"     && wget --no-verbose --output-document=groovy.zip "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip"         && echo "Importing keys listed in http://www.apache.org/dist/groovy/KEYS from key server"     && export GNUPGHOME="$(mktemp -d)"     && gpg --batch --no-tty --keyserver keyserver.ubuntu.com --recv-keys         7FAA0F2206DE228F0DB01AD741321490758AAD6F         331224E1D7BE883D16E8A685825C06C827AF6B66         34441E504A937F43EB0DAEF96A65176A0FB1CD0B         9A810E3B766E089FFB27C70F11B595CEDC4AEBB5         81CABC23EECA0790E8989B361FF96E10F0E13706         && echo "Checking download signature"     && wget --no-verbose --output-document=groovy.zip.asc "https://archive.apache.org/dist/groovy/${GROOVY_VERSION}/distribution/apache-groovy-binary-${GROOVY_VERSION}.zip.asc"     && gpg --batch --no-tty --verify groovy.zip.asc groovy.zip     && rm -rf "${GNUPGHOME}"     && rm groovy.zip.asc         && echo "Cleaning up build dependencies"     && apk del .build-deps         && echo "Installing Groovy"     && unzip groovy.zip     && rm groovy.zip     && mv "groovy-${GROOVY_VERSION}" "${GROOVY_HOME}/"     && ln -s "${GROOVY_HOME}/bin/grape" /usr/bin/grape     && ln -s "${GROOVY_HOME}/bin/groovy" /usr/bin/groovy     && ln -s "${GROOVY_HOME}/bin/groovyc" /usr/bin/groovyc     && ln -s "${GROOVY_HOME}/bin/groovyConsole" /usr/bin/groovyConsole     && ln -s "${GROOVY_HOME}/bin/groovydoc" /usr/bin/groovydoc     && ln -s "${GROOVY_HOME}/bin/groovysh" /usr/bin/groovysh     && ln -s "${GROOVY_HOME}/bin/java2groovy" /usr/bin/java2groovy         && echo "Editing startGroovy to include java.xml.bind module"     && sed --in-place 's|startGroovy ( ) {|startGroovy ( ) {\n    JAVA_OPTS="$JAVA_OPTS --add-modules=ALL-SYSTEM"|' "${GROOVY_HOME}/bin/startGroovy"
# Fri, 18 Mar 2022 23:29:23 GMT
USER groovy
# Fri, 18 Mar 2022 23:29:27 GMT
RUN set -o errexit -o nounset     && echo "Testing Groovy installation"     && groovy --version
```

-	Layers:
	-	`sha256:3d243047344378e9b7136d552d48feb7ea8b6fe14ce0990e0cc011d5e369626a`  
		Last Modified: Thu, 17 Mar 2022 04:02:41 GMT  
		Size: 2.8 MB (2812636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d724c850e02b04db420d6d1310332dafdcbf4f8f4280d76ed66954a1b5d0f4d`  
		Last Modified: Thu, 17 Mar 2022 08:46:33 GMT  
		Size: 430.3 KB (430324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f18a9760068ac64523c143e38e0c7c7b63da1c06298ad26adb34e8797372fe49`  
		Last Modified: Thu, 17 Mar 2022 08:48:51 GMT  
		Size: 191.9 MB (191924807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fecfa7b1878eb6c7a49d406f9cc5801a355db58b763f6fadb74db9447e43f179`  
		Last Modified: Thu, 17 Mar 2022 08:48:34 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa64305fabd559ebad4b9729045fbc8c05552bef5b024da712e4eb9f12fd4675`  
		Last Modified: Fri, 18 Mar 2022 23:31:42 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d577a67d944d3d2da6c26d4beb3e20d9bf31ed45540a862efff0b74eace759c2`  
		Last Modified: Fri, 18 Mar 2022 23:31:45 GMT  
		Size: 44.2 MB (44191555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15f9f31cb5e0657a0ac0c9c48db9d6497a026350c7fda3a89d22e764f2eadcc8`  
		Last Modified: Fri, 18 Mar 2022 23:31:42 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
