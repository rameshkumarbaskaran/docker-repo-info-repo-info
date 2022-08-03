## `tomcat:jre8`

```console
$ docker pull tomcat@sha256:8600f3ae6859f847359f83fe6165f87966c9c12c65fa5b3496d6f58ce6a43903
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; ppc64le

### `tomcat:jre8` - linux; amd64

```console
$ docker pull tomcat@sha256:f80c113a9ac929be693dab5dc35e44e775a69c203bc7d32317ab252fbcd5026e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **99.9 MB (99865858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c28075757cd5eaea3fcf7a4e5a572c37ecb139c31bff8bce3395aea5dfa47c09`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Mon, 06 Jun 2022 22:21:25 GMT
ADD file:11157b07dde10107f3f6f2b892c869ea83868475d5825167b5f466a7e410eb05 in / 
# Mon, 06 Jun 2022 22:21:26 GMT
CMD ["bash"]
# Tue, 07 Jun 2022 00:13:10 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 07 Jun 2022 00:13:45 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 07 Jun 2022 00:13:45 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Tue, 07 Jun 2022 00:14:15 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 07 Jun 2022 00:14:15 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Jun 2022 00:14:16 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Tue, 28 Jun 2022 00:58:20 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Tue, 28 Jun 2022 00:58:20 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jun 2022 00:58:20 GMT
RUN mkdir -p "$CATALINA_HOME"
# Tue, 28 Jun 2022 00:58:20 GMT
WORKDIR /usr/local/tomcat
# Tue, 28 Jun 2022 00:58:20 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jun 2022 00:58:21 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Tue, 28 Jun 2022 00:58:21 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Tue, 28 Jun 2022 00:58:21 GMT
ENV TOMCAT_MAJOR=10
# Wed, 27 Jul 2022 01:34:30 GMT
ENV TOMCAT_VERSION=10.0.23
# Wed, 27 Jul 2022 01:34:30 GMT
ENV TOMCAT_SHA512=0e0263e8280f2ccfb4bef916444a6105fef689a3d95c334c8a7bfe59f1e3966d48ea624727f1818a4df331a603f1ac5e21b908dda3cae676ddc1aef90c2d12ab
# Wed, 27 Jul 2022 01:34:31 GMT
COPY dir:ff2a51680483f0bcdc5a24b13ef2136dc5eeea781d447302626b579d05dc3ee3 in /usr/local/tomcat 
# Wed, 27 Jul 2022 01:34:35 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Jul 2022 01:34:37 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 27 Jul 2022 01:34:37 GMT
EXPOSE 8080
# Wed, 27 Jul 2022 01:34:37 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:405f018f9d1d0f351c196b841a7c7f226fb8ea448acd6339a9ed8741600275a2`  
		Last Modified: Wed, 01 Jun 2022 03:03:39 GMT  
		Size: 30.4 MB (30423715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c045aca8dd90fbfb1afd1343ec6ce2e08ab62f20e8943d3e313dd745e22ee37`  
		Last Modified: Tue, 07 Jun 2022 00:19:41 GMT  
		Size: 12.1 MB (12116064 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:629fad70af7cb351e9f42a3a36ab80637019c27077d945d9d913404cc68e213c`  
		Last Modified: Tue, 07 Jun 2022 00:20:23 GMT  
		Size: 41.8 MB (41798988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd75a7d67a11a379e56a07ebc38971531ffbb2e81c154c22919758d8182313cf`  
		Last Modified: Tue, 07 Jun 2022 00:20:18 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b8b791b38424d1019adda83fc896c1dc5bc8877c4db4f909f11e3f3bfd9bba`  
		Last Modified: Tue, 28 Jun 2022 01:27:00 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da7e295191caa4a18cef62c35878bb1c950822faf668519e684084083539c0ce`  
		Last Modified: Wed, 27 Jul 2022 02:00:44 GMT  
		Size: 12.6 MB (12567395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d4ff640c7705009976bfa35a2d8c266275ef649a4ab88d2bbcf8560524eb09e`  
		Last Modified: Wed, 27 Jul 2022 02:00:44 GMT  
		Size: 3.0 MB (2959236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b60d898be47844c84548121fea0c55f7c1f179ba833c425f1dceff3edc4a116d`  
		Last Modified: Wed, 27 Jul 2022 02:00:43 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8` - linux; arm variant v7

```console
$ docker pull tomcat@sha256:b2914fa5bca8f4d228480caa98dd1aa8d17b264164f29942f924b28cfabe7802
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.2 MB (93204060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40bf07386cfd8b5ceeb5634107921958ef615500c39912f34780a22603ad32bb`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 07 Jun 2022 05:51:35 GMT
ADD file:26c86cfcbc153addbca421974e648a7af07234cb3f741bfb030aa0db90b6a7c6 in / 
# Tue, 07 Jun 2022 05:51:36 GMT
CMD ["bash"]
# Sat, 30 Jul 2022 02:49:53 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Sat, 30 Jul 2022 02:50:09 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Sat, 30 Jul 2022 02:50:09 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Sat, 30 Jul 2022 02:50:55 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Sat, 30 Jul 2022 02:50:56 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jul 2022 02:50:56 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Sat, 30 Jul 2022 12:59:43 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Sat, 30 Jul 2022 12:59:43 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 30 Jul 2022 12:59:43 GMT
RUN mkdir -p "$CATALINA_HOME"
# Sat, 30 Jul 2022 12:59:43 GMT
WORKDIR /usr/local/tomcat
# Sat, 30 Jul 2022 12:59:43 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Sat, 30 Jul 2022 12:59:43 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Sat, 30 Jul 2022 12:59:43 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Sat, 30 Jul 2022 12:59:43 GMT
ENV TOMCAT_MAJOR=10
# Sat, 30 Jul 2022 12:59:44 GMT
ENV TOMCAT_VERSION=10.0.23
# Sat, 30 Jul 2022 12:59:44 GMT
ENV TOMCAT_SHA512=0e0263e8280f2ccfb4bef916444a6105fef689a3d95c334c8a7bfe59f1e3966d48ea624727f1818a4df331a603f1ac5e21b908dda3cae676ddc1aef90c2d12ab
# Sat, 30 Jul 2022 12:59:44 GMT
COPY dir:b1edfbbdc118d8a806934ca83b9e3c657076cd12131fd38ea723fcb4142567aa in /usr/local/tomcat 
# Sat, 30 Jul 2022 12:59:53 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Sat, 30 Jul 2022 12:59:54 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Sat, 30 Jul 2022 12:59:54 GMT
EXPOSE 8080
# Sat, 30 Jul 2022 12:59:54 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:5aeb313108e16ff98084efb2ae2830cbe915ea38b3e2fd1e32688dd9d8c11320`  
		Last Modified: Tue, 07 Jun 2022 05:56:03 GMT  
		Size: 27.0 MB (27017432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19fdce069a7dff1a637320e689a92f499bee9dae5c6492ede30168a6194ccd3`  
		Last Modified: Sat, 30 Jul 2022 02:57:14 GMT  
		Size: 11.7 MB (11712882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:941469b8653d3cb920ffd931e080cb9419c0e469c67ef0577373dd664f085a21`  
		Last Modified: Sat, 30 Jul 2022 02:57:57 GMT  
		Size: 39.5 MB (39527899 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94926e41171023a32b1aeaafee54ab43a92c5a45477eee06d190329c8a5cb57c`  
		Last Modified: Sat, 30 Jul 2022 02:57:52 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:983e2d3ed4a8cb2f0bba64e3dc7196c1e760cf2eaaa120bd2aa9eee0885c730e`  
		Last Modified: Sat, 30 Jul 2022 13:33:35 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bfe2de4b8044840c824a68f3e12e4f9c4e864f1f42a6f16a65e49200d11f78f`  
		Last Modified: Sat, 30 Jul 2022 13:33:37 GMT  
		Size: 12.5 MB (12503194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5470f9758cc6db62dc14592a8f0fb33b883ed6375aa0faacc9d777d6daa59f`  
		Last Modified: Sat, 30 Jul 2022 13:33:36 GMT  
		Size: 2.4 MB (2442191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a04182708ec153e54c93cbd4f75034a9a112e36db782ffab827fddaaee05e139`  
		Last Modified: Sat, 30 Jul 2022 13:33:35 GMT  
		Size: 130.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8` - linux; arm64 variant v8

```console
$ docker pull tomcat@sha256:e4a8612eb5ff0ebb8e9c974adf759c6c5c5f8cf2d44ad228c81093973a9ca2fd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **94.0 MB (94041480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e30da5036482fc408cfc80068aa1198f4cc9c73f38e74390f338857169fda94`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 02 Aug 2022 01:18:59 GMT
ADD file:3db67543ea64bf6723921d19cc5d0483db5c6658fc95834d8b2b5ed48a4cbacd in / 
# Tue, 02 Aug 2022 01:18:59 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 17:51:30 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Tue, 02 Aug 2022 17:51:46 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 17:51:46 GMT
ENV JAVA_VERSION=jdk8u342-b07
# Tue, 02 Aug 2022 17:52:30 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='7e6cb9ee2bbbc1b960e5e443fe7e6145a46e06678b6d0b0683fd4996d40c8fcf';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_aarch64_linux_hotspot_8u342b07.tar.gz';          ;;        armhf|arm)          ESUM='50d826bd3f77f137a89abf0cdd135cb2715c2f673f48fa0801612b4e33e1fff0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_arm_linux_hotspot_8u342b07.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='d27ef577eaa68aaea944bfc6c8d695b2b0c770a26116b9977d54025265f1756b';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_ppc64le_linux_hotspot_8u342b07.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='8362dc39dd92faff221c7ca314ed2ff289c17e1447cd2ed01f3b8541c9f1e9eb';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u342-b07/OpenJDK8U-jre_x64_linux_hotspot_8u342b07.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Tue, 02 Aug 2022 17:52:31 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 17:52:32 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 03 Aug 2022 01:57:52 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 03 Aug 2022 01:57:53 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Aug 2022 01:57:54 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 03 Aug 2022 01:57:55 GMT
WORKDIR /usr/local/tomcat
# Wed, 03 Aug 2022 01:57:56 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 03 Aug 2022 01:57:57 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 03 Aug 2022 01:57:58 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 03 Aug 2022 01:57:59 GMT
ENV TOMCAT_MAJOR=10
# Wed, 03 Aug 2022 01:58:00 GMT
ENV TOMCAT_VERSION=10.0.23
# Wed, 03 Aug 2022 01:58:01 GMT
ENV TOMCAT_SHA512=0e0263e8280f2ccfb4bef916444a6105fef689a3d95c334c8a7bfe59f1e3966d48ea624727f1818a4df331a603f1ac5e21b908dda3cae676ddc1aef90c2d12ab
# Wed, 03 Aug 2022 01:58:03 GMT
COPY dir:bddcf6200fb51e19298b11fc5305274a098f5f54d715282f8ab2095d77f4156e in /usr/local/tomcat 
# Wed, 03 Aug 2022 01:58:11 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 Aug 2022 01:58:13 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 03 Aug 2022 01:58:14 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 01:58:15 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:4a3049d340b7d3651a954fd25a32c42feb1086889d6287e2f15468aef865c5c4`  
		Last Modified: Tue, 02 Aug 2022 01:20:49 GMT  
		Size: 28.4 MB (28381155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1a97efc1a354ae767e234943d1f6e30a9985c45f60c828e9af06c2cd98ae470`  
		Last Modified: Tue, 02 Aug 2022 18:00:04 GMT  
		Size: 12.1 MB (12078076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7accc7ee53add0adb19450468bce960c24d14996cf5cd3ba0fbb8a387fc1d775`  
		Last Modified: Tue, 02 Aug 2022 18:01:13 GMT  
		Size: 40.8 MB (40796599 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82dbf05fdfd1d2d9a9e303acaa3de10f5d1b61ba3c2ca5676eeab561751cc6a7`  
		Last Modified: Tue, 02 Aug 2022 18:01:08 GMT  
		Size: 128.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e105f1b2e03f8b0542fd9e92392642b440c44b3cc3a7065242a6cbc9493390`  
		Last Modified: Wed, 03 Aug 2022 03:06:17 GMT  
		Size: 137.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2901e796c77010e0ce7de512b64e1a8ec24839896f236b3437b189c3608f669c`  
		Last Modified: Wed, 03 Aug 2022 03:06:19 GMT  
		Size: 12.6 MB (12573023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ec029889079a690bdb11d9f11f0e4ee735035df02b6bcd643c965080a3f643`  
		Last Modified: Wed, 03 Aug 2022 03:06:18 GMT  
		Size: 212.4 KB (212362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `tomcat:jre8` - linux; ppc64le

```console
$ docker pull tomcat@sha256:6db90109f8208660714fb869b365fb4e63cbbf22616aac15efba5dac5da08525
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **105.7 MB (105727282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87c2fc01b0f2dfb01ef66ffc1e242ea33c5282ef7a04cff1dac1acb9f82a0c93`
-	Default Command: `["catalina.sh","run"]`

```dockerfile
# Tue, 07 Jun 2022 05:46:49 GMT
ADD file:62ec907c651e833838867bd541cf824f5f609ea4e2b19c4b26cec74a57b60470 in / 
# Tue, 07 Jun 2022 05:46:54 GMT
CMD ["bash"]
# Wed, 27 Jul 2022 00:35:22 GMT
ENV LANG=en_US.UTF-8 LANGUAGE=en_US:en LC_ALL=en_US.UTF-8
# Wed, 27 Jul 2022 00:35:59 GMT
RUN apt-get update     && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends tzdata curl ca-certificates fontconfig locales     && echo "en_US.UTF-8 UTF-8" >> /etc/locale.gen     && locale-gen en_US.UTF-8     && rm -rf /var/lib/apt/lists/*
# Wed, 27 Jul 2022 00:36:00 GMT
ENV JAVA_VERSION=jdk8u332-b09
# Wed, 27 Jul 2022 00:38:07 GMT
RUN set -eux;     ARCH="$(dpkg --print-architecture)";     case "${ARCH}" in        aarch64|arm64)          ESUM='be92e658ed7f6b14b3b945700d7a4f87467c682b70dfbf682ca4562b93cfc8e0';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_aarch64_linux_hotspot_8u332b09.tar.gz';          ;;        armhf|arm)          ESUM='72adfae646b7866aedd28c20a874181c8f3835ccb16610c47e0ca0780f8f9a9c';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_arm_linux_hotspot_8u332b09.tar.gz';          apt-get update          && DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends libatomic1          && rm -rf /var/lib/apt/lists/*          ;;        ppc64el|powerpc:common64)          ESUM='3c7434b248b0edd23a5ac0d8244382725d90e1214f0ddc73a0ead5ad5ceffdaa';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_ppc64le_linux_hotspot_8u332b09.tar.gz';          ;;        amd64|i386:x86-64)          ESUM='34454309b43d585047baaefc36c1850d0192cccc8b52cdc4aadb192b8e3e4c81';          BINARY_URL='https://github.com/adoptium/temurin8-binaries/releases/download/jdk8u332-b09/OpenJDK8U-jre_x64_linux_hotspot_8u332b09.tar.gz';          ;;        *)          echo "Unsupported arch: ${ARCH}";          exit 1;          ;;     esac;     curl -LfsSo /tmp/openjdk.tar.gz ${BINARY_URL};     echo "${ESUM} */tmp/openjdk.tar.gz" | sha256sum -c -;     mkdir -p /opt/java/openjdk;     cd /opt/java/openjdk;     tar -xf /tmp/openjdk.tar.gz --strip-components=1;     rm -rf /tmp/openjdk.tar.gz;
# Wed, 27 Jul 2022 00:38:08 GMT
ENV JAVA_HOME=/opt/java/openjdk PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 00:38:09 GMT
RUN echo Verifying install ...     && echo java -version && java -version     && echo Complete.
# Wed, 27 Jul 2022 14:58:33 GMT
ENV CATALINA_HOME=/usr/local/tomcat
# Wed, 27 Jul 2022 14:58:33 GMT
ENV PATH=/usr/local/tomcat/bin:/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 14:58:35 GMT
RUN mkdir -p "$CATALINA_HOME"
# Wed, 27 Jul 2022 14:58:35 GMT
WORKDIR /usr/local/tomcat
# Wed, 27 Jul 2022 14:58:35 GMT
ENV TOMCAT_NATIVE_LIBDIR=/usr/local/tomcat/native-jni-lib
# Wed, 27 Jul 2022 14:58:36 GMT
ENV LD_LIBRARY_PATH=/usr/local/tomcat/native-jni-lib
# Wed, 27 Jul 2022 14:58:36 GMT
ENV GPG_KEYS=A9C5DF4D22E99998D9875A5110C01C5A2F6059E7
# Wed, 27 Jul 2022 14:58:37 GMT
ENV TOMCAT_MAJOR=10
# Wed, 27 Jul 2022 14:58:37 GMT
ENV TOMCAT_VERSION=10.0.23
# Wed, 27 Jul 2022 14:58:37 GMT
ENV TOMCAT_SHA512=0e0263e8280f2ccfb4bef916444a6105fef689a3d95c334c8a7bfe59f1e3966d48ea624727f1818a4df331a603f1ac5e21b908dda3cae676ddc1aef90c2d12ab
# Wed, 27 Jul 2022 14:58:38 GMT
COPY dir:e8248f6fd61c0a28673884d722a7510d06b1f556cd31ca149df9ded3c2adc3eb in /usr/local/tomcat 
# Wed, 27 Jul 2022 14:58:47 GMT
RUN set -eux; 	apt-get update; 	xargs -rt apt-get install -y --no-install-recommends < "$TOMCAT_NATIVE_LIBDIR/.dependencies.txt"; 	rm -rf /var/lib/apt/lists/*
# Wed, 27 Jul 2022 14:58:51 GMT
RUN set -eux; 	nativeLines="$(catalina.sh configtest 2>&1)"; 	nativeLines="$(echo "$nativeLines" | grep 'Apache Tomcat Native')"; 	nativeLines="$(echo "$nativeLines" | sort -u)"; 	if ! echo "$nativeLines" | grep -E 'INFO: Loaded( APR based)? Apache Tomcat Native library' >&2; then 		echo >&2 "$nativeLines"; 		exit 1; 	fi
# Wed, 27 Jul 2022 14:58:51 GMT
EXPOSE 8080
# Wed, 27 Jul 2022 14:58:51 GMT
CMD ["catalina.sh" "run"]
```

-	Layers:
	-	`sha256:b851cfa9fcbcb74629241502e21ebbae255fe40a2f26949573f278672b65c308`  
		Last Modified: Tue, 07 Jun 2022 05:49:53 GMT  
		Size: 35.7 MB (35717509 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62cafa1747753931a54cd680bfab88daa275922d652dd97af00c278ecbddb7a1`  
		Last Modified: Wed, 27 Jul 2022 00:50:36 GMT  
		Size: 12.9 MB (12861467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d71968ebe833ccf1511f9a241468321ed0c86d38defafd584a5312742eb4548e`  
		Last Modified: Wed, 27 Jul 2022 00:51:59 GMT  
		Size: 41.2 MB (41205891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bec144cc20729466250bbe09bb0bb5f4e2a70e98c52b67fc9727208d2bbd98f9`  
		Last Modified: Wed, 27 Jul 2022 00:51:51 GMT  
		Size: 160.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780a6d55cc9ef8980ac403bbdc633cc6104d368d2909476e21a0cf62a413014e`  
		Last Modified: Wed, 27 Jul 2022 15:39:11 GMT  
		Size: 172.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25dd2cbc4ef03c8d0f62a770ff757f69ad45a3ca7d318ab0f6c137a310bbc120`  
		Last Modified: Wed, 27 Jul 2022 15:39:13 GMT  
		Size: 12.6 MB (12594878 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f2dba89b133e1c88133da352d817d093eeab6d24aa2a60b699cbef721332584`  
		Last Modified: Wed, 27 Jul 2022 15:39:12 GMT  
		Size: 3.3 MB (3347076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1829281d9ac745d86e1abe6ec7739d5ed3dbc8c88095d6be8f287444f4c4cd45`  
		Last Modified: Wed, 27 Jul 2022 15:39:11 GMT  
		Size: 129.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
