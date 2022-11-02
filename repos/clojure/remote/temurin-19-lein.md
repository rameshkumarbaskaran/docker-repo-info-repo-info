## `clojure:temurin-19-lein`

```console
$ docker pull clojure@sha256:f90ea1a36c53c0a1e135b633dc9baaff628a006b2aa21122ab1108257579cb97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-19-lein` - linux; amd64

```console
$ docker pull clojure@sha256:8598a9fe1c43ac59a6150c4b78dfb5d3e60aeb080ea74d4d698a4a160d9c5f6a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **265.0 MB (265044699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22e28938402247682f80d1a6909643d192fb622c86689a5b6a39b49d73407d88`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 02 Nov 2022 18:25:55 GMT
ADD file:29c72d5be8c977acaeb6391aeb23ec27559b594e25a0bb3a6dd280bac2847b7f in / 
# Wed, 02 Nov 2022 18:25:55 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 18:43:42 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 18:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 18:43:42 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 18:45:37 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 18:46:23 GMT
ENV JAVA_VERSION=jdk-19+36
# Wed, 02 Nov 2022 18:46:37 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9b5de40b0f6fe0ab32e8d035720dbbc87bf41b758ed67351ad781ca6505f5294';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_aarch64_linux_hotspot_19_36.tar.gz';          ;;        armhf|arm)          ESUM='34a786548033391de80b857fe02a9c7bd42fcb94243e7273e89012df73f1adef';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_arm_linux_hotspot_19_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='55cc9382227433fa7cc1486a12af59d5bcbea9c40eaeae9608278e056b7d86db';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_ppc64le_linux_hotspot_19_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a5452599d0172ff6a72ae92436042ee8ce0598583197d6ca5c3501a1b379eb0c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_s390x_linux_hotspot_19_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='d10becfc1ea6586180246455ee8d462875f97655416a7d7c5a1c60d0570dbc8f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_linux_hotspot_19_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 02 Nov 2022 18:46:40 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 02 Nov 2022 18:46:40 GMT
CMD ["jshell"]
# Wed, 02 Nov 2022 20:19:06 GMT
ENV LEIN_VERSION=2.9.10
# Wed, 02 Nov 2022 20:19:06 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 02 Nov 2022 20:19:06 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:19:33 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 02 Nov 2022 20:19:33 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Nov 2022 20:19:33 GMT
ENV LEIN_ROOT=1
# Wed, 02 Nov 2022 20:19:36 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 02 Nov 2022 20:19:36 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 02 Nov 2022 20:19:36 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Nov 2022 20:19:36 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:e96e057aae67380a4ddb16c337c5c3669d97fdff69ec537f02aa2cc30d814281`  
		Last Modified: Wed, 02 Nov 2022 03:03:36 GMT  
		Size: 30.4 MB (30425607 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:014fa72e018dd1c616d4bdb23d6fbb735820db9a943b470a787973556d4ee24e`  
		Last Modified: Wed, 02 Nov 2022 18:50:22 GMT  
		Size: 17.0 MB (16986189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5be68af618289efb6a189cb5adf042aeb201cc90dc568832de1d22bf09c28239`  
		Last Modified: Wed, 02 Nov 2022 18:51:22 GMT  
		Size: 200.9 MB (200852998 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aabe61642fd50a00b1e64bb99d83f68065ea661478fb56e5b682b868401aeda8`  
		Last Modified: Wed, 02 Nov 2022 18:51:06 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a1c4586c952c4e7df648baa627dbcc1714c9e96188001b201d701002e12aa5c`  
		Last Modified: Wed, 02 Nov 2022 20:31:01 GMT  
		Size: 12.4 MB (12380688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d37c073cd4cb9107084e4c330340885cd85a3e7390f468dc61a899bd8128d54`  
		Last Modified: Wed, 02 Nov 2022 20:31:00 GMT  
		Size: 4.4 MB (4398640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f8afe30156eb4c27dc8533a47b9db2d68105cbe7f463d7ca3151990a79ce5df`  
		Last Modified: Wed, 02 Nov 2022 20:30:59 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-19-lein` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:7b213e3cdf555258a3a960d26d8c4636499fd77d24d1878a4679a518b645f43d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **263.2 MB (263166734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e36187923a40bae006fdd442f0f1688547d297975b1d8aab19e018ad1c8a3b3f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["repl"]`

```dockerfile
# Wed, 02 Nov 2022 18:49:40 GMT
ADD file:a934fb007525d0b56966a52a22ab22560bf48b6e09917f05324042129d4d894a in / 
# Wed, 02 Nov 2022 18:49:40 GMT
CMD ["bash"]
# Wed, 02 Nov 2022 19:44:20 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 02 Nov 2022 19:44:20 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Nov 2022 19:44:20 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 02 Nov 2022 19:45:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl wget ca-certificates fontconfig locales binutils     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 02 Nov 2022 19:46:27 GMT
ENV JAVA_VERSION=jdk-19+36
# Wed, 02 Nov 2022 19:46:41 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='9b5de40b0f6fe0ab32e8d035720dbbc87bf41b758ed67351ad781ca6505f5294';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_aarch64_linux_hotspot_19_36.tar.gz';          ;;        armhf|arm)          ESUM='34a786548033391de80b857fe02a9c7bd42fcb94243e7273e89012df73f1adef';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_arm_linux_hotspot_19_36.tar.gz';          ;;        ppc64el|powerpc:common64)          ESUM='55cc9382227433fa7cc1486a12af59d5bcbea9c40eaeae9608278e056b7d86db';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_ppc64le_linux_hotspot_19_36.tar.gz';          ;;        s390x|s390:64-bit)          ESUM='a5452599d0172ff6a72ae92436042ee8ce0598583197d6ca5c3501a1b379eb0c';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_s390x_linux_hotspot_19_36.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='d10becfc1ea6586180246455ee8d462875f97655416a7d7c5a1c60d0570dbc8f';          BINARY_URL='https://github.com/adoptium/temurin19-binaries/releases/download/jdk-19%2B36/OpenJDK19U-jdk_x64_linux_hotspot_19_36.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac; 	  wget -O /tmp/openjdk.tar.gz ${BINARY_URL}; 	  echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -; 	  mkdir -p "$JAVA_HOME"; 	  tar --extract 	      --file /tmp/openjdk.tar.gz 	      --directory "$JAVA_HOME" 	      --strip-components 1 	      --no-same-owner 	  ;     rm /tmp/openjdk.tar.gz;     find "$JAVA_HOME/lib" -name '*.so' -exec dirname '{}' ';' | sort -u > /etc/ld.so.conf.d/docker-openjdk.conf;     ldconfig;     java -Xshare:dump;
# Wed, 02 Nov 2022 19:46:44 GMT
RUN echo Verifying install ...     && fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java     && echo javac --version && javac --version     && echo java --version && java --version     && echo Complete.
# Wed, 02 Nov 2022 19:46:44 GMT
CMD ["jshell"]
# Wed, 02 Nov 2022 20:53:49 GMT
ENV LEIN_VERSION=2.9.10
# Wed, 02 Nov 2022 20:53:49 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Wed, 02 Nov 2022 20:53:49 GMT
WORKDIR /tmp
# Wed, 02 Nov 2022 20:54:01 GMT
RUN set -eux; apt-get update && apt-get install -y make gnupg wget && rm -rf /var/lib/apt/lists/* && mkdir -p $LEIN_INSTALL && wget -q https://codeberg.org/leiningen/leiningen/raw/tag/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "dbb84d13d6df5b85bbf7f89a39daeed103133c24a4686d037fe6bd65e38e7f32 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && export GNUPGHOME="$(mktemp -d)" && export FILENAME_EXT=jar && if printf '%s\n%s\n' "2.9.7" "$LEIN_VERSION" | sort -cV; then               gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys 6A2D483DB59437EBB97D09B1040193357D0606ED;             else               gpg --batch --keyserver hkps://keyserver.ubuntu.com --recv-keys 20242BACBBE95ADA22D0AFD7808A33D379C806C3;               FILENAME_EXT=zip;             fi && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && wget -q https://codeberg.org/leiningen/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT && gpgconf --kill all && rm -rf "$GNUPGHOME" leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.$FILENAME_EXT /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apt-get purge -y --auto-remove gnupg wget
# Wed, 02 Nov 2022 20:54:01 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Wed, 02 Nov 2022 20:54:01 GMT
ENV LEIN_ROOT=1
# Wed, 02 Nov 2022 20:54:03 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.11.1"]])' > project.clj   && lein deps && rm project.clj
# Wed, 02 Nov 2022 20:54:03 GMT
COPY file:cf90f595e38d932dff3bdcd4221efe7c65fb3432787490053b55b6917f06e4cd in /usr/local/bin/entrypoint 
# Wed, 02 Nov 2022 20:54:03 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 02 Nov 2022 20:54:03 GMT
CMD ["repl"]
```

-	Layers:
	-	`sha256:0509fae36eb0656f8bdb23f8ae64100d893bcea2563e97468d337e04d2d0410b`  
		Last Modified: Wed, 02 Nov 2022 18:50:21 GMT  
		Size: 28.4 MB (28382154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a8d9c230ad7b20621780183623ce76b7c296e1db90d16a51deeb03f19e2493c`  
		Last Modified: Wed, 02 Nov 2022 19:49:51 GMT  
		Size: 18.4 MB (18416178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ad0c2cd6437a19e827e089c26dc673cb9b759584447394ca75a59d7262cbbc`  
		Last Modified: Wed, 02 Nov 2022 19:50:48 GMT  
		Size: 199.6 MB (199589982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb7bc6d25e82c611ff8eda9d3d6ce3092c1680a8f792973b0f5a9b5d1775da39`  
		Last Modified: Wed, 02 Nov 2022 19:50:34 GMT  
		Size: 171.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b999744acbb1f5103ca16acbceaa0ae1dea0afbc84add16d7a4d42651e95f44`  
		Last Modified: Wed, 02 Nov 2022 21:04:42 GMT  
		Size: 12.4 MB (12379166 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51a24e0838fd8b5e7a5c9ca296765a93d4c89e2d298b6e832873211ec5ab70e0`  
		Last Modified: Wed, 02 Nov 2022 21:04:38 GMT  
		Size: 4.4 MB (4398684 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2e0a6b9a22783114fe319a789b8ef0a676c7744eca9aa5733f66401929dfa4`  
		Last Modified: Wed, 02 Nov 2022 21:04:38 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
