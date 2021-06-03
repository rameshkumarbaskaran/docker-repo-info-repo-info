## `maven:3-openjdk-17`

```console
$ docker pull maven@sha256:fcbbee341e0130336fc11d19121e27f90ebf01005c0113f2343826a8cb749e64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `maven:3-openjdk-17` - linux; amd64

```console
$ docker pull maven@sha256:5ae570b581ab1b359e15bdf859eb99231ccf8a6e688661af7ff0fccfd4610f3c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **415.3 MB (415275426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e7b7b408f52da1d7e0ad7d5cedcbbc99a4e345b3c22fce180d71c86b17f993d`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 02 Jun 2021 17:21:00 GMT
ADD file:b4c18f27ab03ed63f96174673a8d97d4b1b6abb552b6fe3201c6aec934e8312f in / 
# Wed, 02 Jun 2021 17:21:00 GMT
CMD ["/bin/bash"]
# Wed, 02 Jun 2021 17:37:54 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 02 Jun 2021 17:37:55 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Wed, 02 Jun 2021 17:37:55 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Jun 2021 17:37:55 GMT
ENV LANG=C.UTF-8
# Wed, 02 Jun 2021 17:37:55 GMT
ENV JAVA_VERSION=17-ea+24
# Wed, 02 Jun 2021 17:38:07 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/24/GPL/openjdk-17-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='30b8cc8945c42ab310bca47ecfe2acdf2a0285d26dfeb6bfba46ebc5947aef6e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/24/GPL/openjdk-17-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='61d192356099180ee3beec3a22cb9e97cb810c7f55f2c870a73841c3ac61abcb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 02 Jun 2021 17:38:08 GMT
CMD ["jshell"]
# Wed, 02 Jun 2021 18:12:44 GMT
ARG MAVEN_VERSION=3.8.1
# Wed, 02 Jun 2021 18:12:44 GMT
ARG USER_HOME_DIR=/root
# Wed, 02 Jun 2021 18:12:45 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Wed, 02 Jun 2021 18:12:45 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Wed, 02 Jun 2021 18:13:09 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN microdnf install findutils git
# Wed, 02 Jun 2021 18:13:16 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 02 Jun 2021 18:13:17 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 02 Jun 2021 18:13:17 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 02 Jun 2021 18:13:17 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 02 Jun 2021 18:13:17 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 02 Jun 2021 18:13:17 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 02 Jun 2021 18:13:17 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:5a581c13a8b96af42c06955acd88fdb3aff53edcbdd33faa7bca9854fd8bfbaf`  
		Last Modified: Wed, 02 Jun 2021 17:22:10 GMT  
		Size: 42.2 MB (42183647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26cd02acd9c2b40dba18c3fe68882bcb5ebda0caeb5e550965d9ac81e3b55fbf`  
		Last Modified: Wed, 02 Jun 2021 17:43:15 GMT  
		Size: 13.4 MB (13400021 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13f8e1f5ebf50abc2e5ca10733d192a1de25938182003de38c39c2906db03ba2`  
		Last Modified: Wed, 02 Jun 2021 17:43:27 GMT  
		Size: 186.2 MB (186232558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79126526d6d748228d8c027f82c60feab3550cf5cb5ec3202514cb179aed41e1`  
		Last Modified: Wed, 02 Jun 2021 18:16:58 GMT  
		Size: 163.8 MB (163847014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28e4194c4981cf41805f3c353aa48b20e4fdfab9c91ca1a595208780a0f13afb`  
		Last Modified: Wed, 02 Jun 2021 18:16:44 GMT  
		Size: 9.6 MB (9610973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefce39d94101d99830e8dd4d8caaac07467215d7a58cdc96f19b0c78acca5b0`  
		Last Modified: Wed, 02 Jun 2021 18:16:43 GMT  
		Size: 856.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8247d7130f9aad1d91c3c8e7f8e728f704b1580f98c5c05a4e014970a3bc236`  
		Last Modified: Wed, 02 Jun 2021 18:16:43 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `maven:3-openjdk-17` - linux; arm64 variant v8

```console
$ docker pull maven@sha256:6e5386d18a12b0f227d61f896c95b7e42147557a3caafa9ee9bad7b4ce040762
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **390.9 MB (390888541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36ada277d17c86f69a6cb2f2bf55ea1830884492887f1208470d8b64f9efee14`
-	Entrypoint: `["\/usr\/local\/bin\/mvn-entrypoint.sh"]`
-	Default Command: `["mvn"]`

```dockerfile
# Wed, 02 Jun 2021 17:41:03 GMT
ADD file:78235baf524ed2a030d5aee5012599777d5026bf83699d8d03662420d6804653 in / 
# Wed, 02 Jun 2021 17:41:03 GMT
CMD ["/bin/bash"]
# Wed, 02 Jun 2021 17:58:06 GMT
RUN set -eux; 	microdnf install 		gzip 		tar 				binutils 		freetype fontconfig 	; 	microdnf clean all
# Wed, 02 Jun 2021 17:58:06 GMT
ENV JAVA_HOME=/usr/java/openjdk-17
# Wed, 02 Jun 2021 17:58:07 GMT
ENV PATH=/usr/java/openjdk-17/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Jun 2021 17:58:07 GMT
ENV LANG=C.UTF-8
# Wed, 02 Jun 2021 17:58:07 GMT
ENV JAVA_VERSION=17-ea+24
# Wed, 02 Jun 2021 17:58:19 GMT
RUN set -eux; 		arch="$(objdump="$(command -v objdump)" && objdump --file-headers "$objdump" | awk -F '[:,]+[[:space:]]+' '$1 == "architecture" { print $2 }')"; 	case "$arch" in 		'i386:x86-64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/24/GPL/openjdk-17-ea+24_linux-x64_bin.tar.gz'; 			downloadSha256='30b8cc8945c42ab310bca47ecfe2acdf2a0285d26dfeb6bfba46ebc5947aef6e'; 			;; 		'aarch64') 			downloadUrl='https://download.java.net/java/early_access/jdk17/24/GPL/openjdk-17-ea+24_linux-aarch64_bin.tar.gz'; 			downloadSha256='61d192356099180ee3beec3a22cb9e97cb810c7f55f2c870a73841c3ac61abcb'; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		curl -fL -o openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum --strict --check -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz*; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/pki/ca-trust/extracted/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		ln -sfT "$JAVA_HOME" /usr/java/default; 	ln -sfT "$JAVA_HOME" /usr/java/latest; 	for bin in "$JAVA_HOME/bin/"*; do 		base="$(basename "$bin")"; 		[ ! -e "/usr/bin/$base" ]; 		alternatives --install "/usr/bin/$base" "$base" "$bin" 20000; 	done; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Wed, 02 Jun 2021 17:58:19 GMT
CMD ["jshell"]
# Wed, 02 Jun 2021 18:32:44 GMT
ARG MAVEN_VERSION=3.8.1
# Wed, 02 Jun 2021 18:32:45 GMT
ARG USER_HOME_DIR=/root
# Wed, 02 Jun 2021 18:32:45 GMT
ARG SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d
# Wed, 02 Jun 2021 18:32:45 GMT
ARG BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries
# Wed, 02 Jun 2021 18:33:07 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN microdnf install findutils git
# Wed, 02 Jun 2021 18:33:13 GMT
# ARGS: BASE_URL=https://apache.osuosl.org/maven/maven-3/3.8.1/binaries MAVEN_VERSION=3.8.1 SHA=0ec48eb515d93f8515d4abe465570dfded6fa13a3ceb9aab8031428442d9912ec20f066b2afbf56964ffe1ceb56f80321b50db73cf77a0e2445ad0211fb8e38d USER_HOME_DIR=/root
RUN mkdir -p /usr/share/maven /usr/share/maven/ref   && curl -fsSL -o /tmp/apache-maven.tar.gz ${BASE_URL}/apache-maven-${MAVEN_VERSION}-bin.tar.gz   && echo "${SHA}  /tmp/apache-maven.tar.gz" | sha512sum -c -   && tar -xzf /tmp/apache-maven.tar.gz -C /usr/share/maven --strip-components=1   && rm -f /tmp/apache-maven.tar.gz   && ln -s /usr/share/maven/bin/mvn /usr/bin/mvn
# Wed, 02 Jun 2021 18:33:13 GMT
ENV MAVEN_HOME=/usr/share/maven
# Wed, 02 Jun 2021 18:33:13 GMT
ENV MAVEN_CONFIG=/root/.m2
# Wed, 02 Jun 2021 18:33:13 GMT
COPY file:1b3da5c58894f705e7387946301c0c52edb6271761ea3cd80b86a848847a64cd in /usr/local/bin/mvn-entrypoint.sh 
# Wed, 02 Jun 2021 18:33:14 GMT
COPY file:2bbb488dd73c55d658b91943cfdf9c26975a320ceafc45dda94c95b03e518ad3 in /usr/share/maven/ref/ 
# Wed, 02 Jun 2021 18:33:14 GMT
ENTRYPOINT ["/usr/local/bin/mvn-entrypoint.sh"]
# Wed, 02 Jun 2021 18:33:14 GMT
CMD ["mvn"]
```

-	Layers:
	-	`sha256:4a780b35fbf92abdbd808aa7d8f30cb6c03db446424f04738aa715ba4935a1f6`  
		Last Modified: Wed, 02 Jun 2021 17:42:09 GMT  
		Size: 42.1 MB (42068993 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b11c9e8386348cc9050d7280e19b5987140671e2de847d978f53d4ec578f94`  
		Last Modified: Wed, 02 Jun 2021 18:08:16 GMT  
		Size: 14.2 MB (14183644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32f52be335c2cc54dfee2029f1a762bb018fb3e0eb6fbc72c0ab61faef01a66a`  
		Last Modified: Wed, 02 Jun 2021 18:08:30 GMT  
		Size: 182.3 MB (182290733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:888b72da534d6bfd577f157c00544cb1f61c1f9f688ea8d3861181ed19a92534`  
		Last Modified: Wed, 02 Jun 2021 18:38:45 GMT  
		Size: 142.7 MB (142732987 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd842717ef490b9c96b0ebd6f8917a9a6c1fbe162610c6bdce0e3b19a66b0cfd`  
		Last Modified: Wed, 02 Jun 2021 18:38:27 GMT  
		Size: 9.6 MB (9610970 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b0659b930f73d1ecdad9a8e90d75fc77bc51244d02a22043e88daec4a9b79d1`  
		Last Modified: Wed, 02 Jun 2021 18:38:26 GMT  
		Size: 855.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c482dd8bcfd8b0691e3bee60e75b95e0259d26d81aec1bda418203d2c03d7ac8`  
		Last Modified: Wed, 02 Jun 2021 18:38:26 GMT  
		Size: 359.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
