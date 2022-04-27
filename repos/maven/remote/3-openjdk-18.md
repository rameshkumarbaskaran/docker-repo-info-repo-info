## `maven:3-openjdk-18`

```console
$ docker pull maven@sha256:9263ff6fde67d964e537d490c3becedf94e077a380a84862786f5e368222ba79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-18` - linux; amd64

```console
$ docker pull maven@sha256:95c07a10e80534a09811ee0a69cff01b40af189aef32ed203cdc33ffc29bb71d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.2 MB (433248010 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc384e4b69a12e2149bbad19aa669a598f8078520fc8ef93b4d77e30b4a78c3b`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 27 Apr 2022 20:33:04 GMT
ADD file:9893213a9ea238f53ac68d87a3cf2f05d86763688392e5ddb6a2c9b60d3550a6 in / 
# Wed, 27 Apr 2022 20:33:05 GMT
CMD ["/bin/bash"]
# Wed, 27 Apr 2022 21:53:12 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 27 Apr 2022 21:53:49 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 27 Apr 2022 21:53:50 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Apr 2022 21:53:50 GMT
ENV LANG=C.UTF-8
# Wed, 27 Apr 2022 21:53:50 GMT
ENV JAVA_VERSION=18.0.1
# Wed, 27 Apr 2022 21:53:59 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1/3f48cabb83014f9fab465e280ccf630b/10/GPL/openjdk-18.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='56b06ade89a6a0f941682e7b2bc4039a105ddaa9bc10cad85bb426b9eb503943'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1/3f48cabb83014f9fab465e280ccf630b/10/GPL/openjdk-18.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='ecc0d07ebc4a8fc337a6a65484f092b4d5cf0da0f773dcfe1870b361394d5b95'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 27 Apr 2022 21:54:00 GMT
CMD ["jshell"]
# Wed, 27 Apr 2022 23:01:01 GMT
RUN microdnf install findutils git
# Wed, 27 Apr 2022 23:01:02 GMT
ARG MAVEN_VERSION=3.8.5
# Wed, 27 Apr 2022 23:01:03 GMT
ARG USER_HOME_DIR=/root
# Wed, 27 Apr 2022 23:01:03 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Wed, 27 Apr 2022 23:01:03 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Wed, 27 Apr 2022 23:01:11 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 27 Apr 2022 23:01:11 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 27 Apr 2022 23:01:11 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 27 Apr 2022 23:01:11 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 27 Apr 2022 23:01:11 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 27 Apr 2022 23:01:11 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 27 Apr 2022 23:01:11 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:38a980f2cc8accf69c23deae6743d42a87eb34a54f02396f3fcfd7c2d06e2c5b`  
		Last Modified: Wed, 27 Apr 2022 20:33:57 GMT  
		Size: 42.1 MB (42114164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de849f1cfbe60b1c06a1db83a3129ab0ea397c4852b98e3e4300b12ee57ba111`  
		Last Modified: Wed, 27 Apr 2022 22:01:52 GMT  
		Size: 13.5 MB (13525123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6567c815126edcad94891827b30a80b3f1d65f19164f410c3c919d08b82297`  
		Last Modified: Wed, 27 Apr 2022 22:03:15 GMT  
		Size: 188.7 MB (188727415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf84b543e809870a61b12bae3e86e3aa42ed031d90f7bf25b2329587948dd75`  
		Last Modified: Wed, 27 Apr 2022 23:05:25 GMT  
		Size: 180.1 MB (180143700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f9bdabbb92933471117126e0cc4b816c0cf4fff1b97f50fbc632da897320fcd`  
		Last Modified: Wed, 27 Apr 2022 23:05:11 GMT  
		Size: 8.7 MB (8736392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:724cb4c6a4eaed436d30c7fdd66befcb3d5a453c67cfb0ff490486c08d5dc723`  
		Last Modified: Wed, 27 Apr 2022 23:05:10 GMT  
		Size: 857.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8026b97a59dfe86a94f500cb5f268fe47876bc67a3ce307a75a3c5a7de436d84`  
		Last Modified: Wed, 27 Apr 2022 23:05:10 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-18` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:21695131f425bcdb515c63df193f0feed3e93984684896a91fd950e61aad12ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **433.4 MB (433385552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbbc067c52c213819a9ce84d8e090d205ec68842642d2ee8dc78bbd747bcc974`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Tue, 29 Mar 2022 18:27:10 GMT
ADD file:08d6d9fea731c201f517e2e96a93c19200773de2ddaa9bed138d10224f7d61e7 in / 
# Tue, 29 Mar 2022 18:27:11 GMT
CMD ["/bin/bash"]
# Wed, 30 Mar 2022 08:57:29 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 30 Mar 2022 09:00:19 GMT
ENV JAVA_HOME=/usr/java/openjdk-18
# Wed, 30 Mar 2022 09:00:20 GMT
ENV PATH=/usr/java/openjdk-18/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 30 Mar 2022 09:00:21 GMT
ENV LANG=C.UTF-8
# Thu, 21 Apr 2022 22:31:51 GMT
ENV JAVA_VERSION=18.0.1
# Thu, 21 Apr 2022 22:32:06 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1/3f48cabb83014f9fab465e280ccf630b/10/GPL/openjdk-18.0.1_linux-x64_bin.tar.gz'; 			downloadSha256='56b06ade89a6a0f941682e7b2bc4039a105ddaa9bc10cad85bb426b9eb503943'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/GA/jdk18.0.1/3f48cabb83014f9fab465e280ccf630b/10/GPL/openjdk-18.0.1_linux-aarch64_bin.tar.gz'; 			downloadSha256='ecc0d07ebc4a8fc337a6a65484f092b4d5cf0da0f773dcfe1870b361394d5b95'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Thu, 21 Apr 2022 22:32:07 GMT
CMD ["jshell"]
# Fri, 22 Apr 2022 01:20:06 GMT
RUN microdnf install findutils git
# Fri, 22 Apr 2022 01:20:06 GMT
ARG MAVEN_VERSION=3.8.5
# Fri, 22 Apr 2022 01:20:07 GMT
ARG USER_HOME_DIR=/root
# Fri, 22 Apr 2022 01:20:08 GMT
ARG SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743
# Fri, 22 Apr 2022 01:20:09 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries
# Fri, 22 Apr 2022 01:20:17 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.5/binaries MAVEN_VERSION=3.8.5 SHA=89ab8ece99292476447ef6a6800d9842bbb60787b9b8a45c103aa61d2f205a971d8c3ddfb8b03e514455b4173602bd015e82958c0b3ddc1728a57126f773c743 USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Fri, 22 Apr 2022 01:20:18 GMT
ENV MAVEN_HOME=/usr/share/maven
# Fri, 22 Apr 2022 01:20:19 GMT
ENV MAVEN_CONFIG=/root/.m2
# Fri, 22 Apr 2022 01:20:21 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Fri, 22 Apr 2022 01:20:22 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Fri, 22 Apr 2022 01:20:22 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Fri, 22 Apr 2022 01:20:23 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:293fbd461d2c2a94e5d457aa3c7b18429b8457b06d5c2ad1a57113b1cac6d657`  
		Last Modified: Tue, 29 Mar 2022 18:28:25 GMT  
		Size: 42.0 MB (42019098 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d200eb5167ed838a74239544d81e10c3d37a59ea571f23c1d6ed6e0c207cf997`  
		Last Modified: Wed, 30 Mar 2022 09:18:31 GMT  
		Size: 14.3 MB (14293802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aeb82bbcd3abb1f576cfee66faf103d902c4f87801c560f44884d7db782f0e5b`  
		Last Modified: Thu, 21 Apr 2022 22:46:27 GMT  
		Size: 187.6 MB (187646417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:140d360b24eb56696376f35ad5af575681cf853fdecb05e4de9525e4258bb8ac`  
		Last Modified: Fri, 22 Apr 2022 01:24:41 GMT  
		Size: 180.7 MB (180688677 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a733a632ccb2a5d28fdd63fc87fec8b5fd2616552aa6cba2e32ba67b004911d4`  
		Last Modified: Fri, 22 Apr 2022 01:24:25 GMT  
		Size: 8.7 MB (8736338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2942e8730fdaf713077a85acb87f92e52196dedb21091340d2baaa36ce883c93`  
		Last Modified: Fri, 22 Apr 2022 01:24:24 GMT  
		Size: 858.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ccfb974e12761f7167818589a0d627381c7448f3f3593cd6092bcac0bebccd`  
		Last Modified: Fri, 22 Apr 2022 01:24:25 GMT  
		Size: 362.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
