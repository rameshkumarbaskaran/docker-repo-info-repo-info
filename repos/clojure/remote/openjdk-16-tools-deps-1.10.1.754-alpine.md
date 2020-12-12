## `clojure:openjdk-16-tools-deps-1.10.1.754-alpine`

```console
$ docker pull clojure@sha256:56e81d3cb8276e49eec6eff99c96097862fa1ef79da2723729e2de0c0d81601c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-16-tools-deps-1.10.1.754-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:543b91e1a71e880e32262ea712ab362be5a4fc5afee12a1a1a60ff446e03a83f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **210.6 MB (210570969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:071a0207ecd6e9f2234f9e82125d6e9dd6ea93bea7f8530894a9b30a96b36332`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

```dockerfile
# Fri, 11 Dec 2020 02:04:06 GMT
ADD file:62a1e09319acb6d1bad91ef1c35aabdc7e5e19883a77f30f1951ccfffc812124 in / 
# Fri, 11 Dec 2020 02:04:07 GMT
CMD ["/bin/sh"]
# Fri, 11 Dec 2020 15:37:11 GMT
RUN apk add --no-cache java-cacerts
# Fri, 11 Dec 2020 15:37:11 GMT
ENV JAVA_HOME=/opt/openjdk-16
# Fri, 11 Dec 2020 15:37:12 GMT
ENV PATH=/opt/openjdk-16/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Dec 2020 15:37:12 GMT
ENV JAVA_VERSION=16-ea+23
# Fri, 11 Dec 2020 15:37:48 GMT
RUN set -eux; 		arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64) 			downloadUrl=https://download.java.net/java/early_access/alpine/23/binaries/openjdk-16-ea+23_linux-x64-musl_bin.tar.gz; 			downloadSha256=4e1d9054a4407e63fbb74155b247cf3926cffe9491074ace6d8a51d78dd0958d; 			;; 		*) echo >&2 "error: unsupported architecture: '$arch'"; exit 1 ;; 	esac; 		wget -O openjdk.tgz "$downloadUrl"; 	echo "$downloadSha256 *openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract 		--file openjdk.tgz 		--directory "$JAVA_HOME" 		--strip-components 1 		--no-same-owner 	; 	rm openjdk.tgz; 		rm -rf "$JAVA_HOME/lib/security/cacerts"; 	ln -sT /etc/ssl/certs/java/cacerts "$JAVA_HOME/lib/security/cacerts"; 		java -Xshare:dump; 		fileEncoding="$(echo 'System.out.println(System.getProperty("file.encoding"))' | jshell -s -)"; [ "$fileEncoding" = 'UTF-8' ]; rm -rf ~/.java; 	javac --version; 	java --version
# Fri, 11 Dec 2020 15:37:48 GMT
CMD ["jshell"]
# Sat, 12 Dec 2020 04:19:32 GMT
ENV CLOJURE_VERSION=1.10.1.754
# Sat, 12 Dec 2020 04:19:33 GMT
WORKDIR /tmp
# Sat, 12 Dec 2020 04:19:42 GMT
RUN apk add --update --no-cache curl bash make && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "1c623dd76ea75cb89623ffc71a5ec59297c785c0c19fc5c2fa0fe9428efe8a3d *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Sat, 12 Dec 2020 04:19:42 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
```

-	Layers:
	-	`sha256:05e7bc50f07f000e9993ec0d264b9ffcbb9a01a4d69c68f556d25e9811a8f7f4`  
		Last Modified: Fri, 11 Dec 2020 02:04:37 GMT  
		Size: 2.8 MB (2796945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3030ddbe078fa840b91b9c4cdecffd7efa208af278d07528dad2fec84d6fcd14`  
		Last Modified: Fri, 11 Dec 2020 15:43:38 GMT  
		Size: 926.4 KB (926397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b68ff00bbded1d7455a824d6f54c9d200746afa482ceaa4a54644064f00c0b`  
		Last Modified: Fri, 11 Dec 2020 15:43:54 GMT  
		Size: 184.3 MB (184293642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad396c543fbfa5fd209f8dc3d53534e7a6f46b4c45607dda4b3c26f1fb7b1d20`  
		Last Modified: Sat, 12 Dec 2020 04:25:03 GMT  
		Size: 22.6 MB (22553985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
