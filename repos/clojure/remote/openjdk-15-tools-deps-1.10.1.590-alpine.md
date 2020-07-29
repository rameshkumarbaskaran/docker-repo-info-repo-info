## `clojure:openjdk-15-tools-deps-1.10.1.590-alpine`

```console
$ docker pull clojure@sha256:eaf81cd18c9f6d51f5f8aed5e281b790316afe0f21b310fac768f4c4e0eba9d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-15-tools-deps-1.10.1.590-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:488b60ba52fe9b7bdc0e053fad0dfb31aa2fb1fcde1f5d2681183019f789dc9f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **223.0 MB (223040408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f69076bd6aa6fc91b0b573b49b1ee805e694b4531201215db40e3311b6bf722`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

```dockerfile
# Fri, 29 May 2020 21:19:46 GMT
ADD file:c92c248239f8c7b9b3c067650954815f391b7bcb09023f984972c082ace2a8d0 in / 
# Fri, 29 May 2020 21:19:46 GMT
CMD ["/bin/sh"]
# Wed, 22 Jul 2020 01:05:44 GMT
RUN apk add --no-cache java-cacerts
# Wed, 22 Jul 2020 01:07:14 GMT
ENV JAVA_HOME=/opt/openjdk-15
# Wed, 22 Jul 2020 01:07:14 GMT
ENV PATH=/opt/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jul 2020 01:07:14 GMT
ENV JAVA_VERSION=15-ea+31
# Wed, 22 Jul 2020 01:07:15 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/alpine/31/binaries/openjdk-15-ea+31_linux-x64-musl_bin.tar.gz
# Wed, 22 Jul 2020 01:07:15 GMT
ENV JAVA_SHA256=da7abd4d3b3511ed2da8aba25b7ff67863261a0c8b5e7e771cf0fbfadcc7f4fd
# Wed, 22 Jul 2020 01:08:07 GMT
RUN set -eux; 		wget -O /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		java -Xshare:dump; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java --version; 	javac --version
# Wed, 22 Jul 2020 01:08:07 GMT
CMD ["jshell"]
# Tue, 28 Jul 2020 23:28:05 GMT
ENV CLOJURE_VERSION=1.10.1.590
# Tue, 28 Jul 2020 23:28:06 GMT
WORKDIR /tmp
# Tue, 28 Jul 2020 23:28:15 GMT
RUN apk add --update --no-cache curl bash make && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "92a606c1b373ddee338c209f9fecd6f0a40b3354b5eb762962b9cc64f226ce53 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Tue, 28 Jul 2020 23:28:15 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
```

-	Layers:
	-	`sha256:df20fa9351a15782c64e6dddb2d4a6f50bf6d3688060a34c4014b0d9a752eb4c`  
		Last Modified: Fri, 29 May 2020 21:20:06 GMT  
		Size: 2.8 MB (2797541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a2e4aad8c98294e53534e7aef0572d7a04cc37264f1b4b75d0878244e59c7f`  
		Last Modified: Wed, 22 Jul 2020 01:13:01 GMT  
		Size: 926.4 KB (926401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa15118984fa68e4bdb9010318493fccb170122e25dac619d5cefdb32c4d32b`  
		Last Modified: Wed, 22 Jul 2020 01:14:18 GMT  
		Size: 196.8 MB (196795740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecfd963f5e0b08bac00bdb771cb546eeb6ba73b37c659410f32416af256ab8da`  
		Last Modified: Tue, 28 Jul 2020 23:31:50 GMT  
		Size: 22.5 MB (22520726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
