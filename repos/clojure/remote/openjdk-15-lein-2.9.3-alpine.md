## `clojure:openjdk-15-lein-2.9.3-alpine`

```console
$ docker pull clojure@sha256:289370a5b7c1acd02fdb97a900e6094a1eb6de5f93e33e4e45bc2d0719667b83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-15-lein-2.9.3-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:a1ad38ac1f095499b36ea3fb3b3ec1002c20827703f77795127f5c488f303464
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.8 MB (220820275 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca830e9c11bdd2d7698777d5bfdd9f7c5de85b4ab2caa7a3bfe2601d0e76e7f4`
-	Default Command: `["lein","repl"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:03 GMT
ADD file:b91adb67b670d3a6ff9463e48b7def903ed516be66fc4282d22c53e41512be49 in / 
# Fri, 24 Apr 2020 01:05:03 GMT
CMD ["/bin/sh"]
# Fri, 24 Apr 2020 16:13:45 GMT
ENV JAVA_HOME=/opt/openjdk-15
# Fri, 24 Apr 2020 16:13:45 GMT
ENV PATH=/opt/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Apr 2020 16:13:45 GMT
ENV JAVA_VERSION=15-ea+10
# Fri, 24 Apr 2020 16:13:45 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/alpine/10/binaries/openjdk-15-ea+10_linux-x64-musl_bin.tar.gz
# Fri, 24 Apr 2020 16:13:46 GMT
ENV JAVA_SHA256=15a5e8002e24ed129b82bfe55ffe4bdbf3cfd0a7e5ad3399879cdd44175bfd06
# Fri, 22 May 2020 01:23:07 GMT
RUN set -eux; 		wget -O /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 		mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		java -Xshare:dump; 		java --version; 	javac --version
# Fri, 22 May 2020 01:23:07 GMT
CMD ["jshell"]
# Tue, 02 Jun 2020 00:28:29 GMT
ENV LEIN_VERSION=2.9.3
# Tue, 02 Jun 2020 00:28:30 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Tue, 02 Jun 2020 00:28:30 GMT
WORKDIR /tmp
# Tue, 02 Jun 2020 00:28:33 GMT
RUN apk add --update --no-cache ca-certificates bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha256sum lein-pkg && echo "42e18e8a833b863ddfba1c5565bd5d78b54bcee661ec86e94a8bdc67b1733e63 *lein-pkg" | sha256sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver keys.openpgp.org --recv-key 20242BACBBE95ADA22D0AFD7808A33D379C806C3 && echo "Verifying file PGP signature..." && gpg --batch --verify leiningen-$LEIN_VERSION-standalone.zip.asc leiningen-$LEIN_VERSION-standalone.zip && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del ca-certificates tar openssl gnupg
# Tue, 02 Jun 2020 00:28:33 GMT
ENV PATH=/opt/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Tue, 02 Jun 2020 00:28:33 GMT
ENV LEIN_ROOT=1
# Tue, 02 Jun 2020 00:28:37 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.1"]])' > project.clj   && lein deps && rm project.clj
# Tue, 02 Jun 2020 00:28:38 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:cbdbe7a5bc2a134ca8ec91be58565ec07d037386d1f1d8385412d224deafca08`  
		Last Modified: Thu, 23 Apr 2020 14:07:19 GMT  
		Size: 2.8 MB (2813316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f63f940b2b97f71dd63758ea307855eda42b2ad6ad589e300590ccbc4d456b2`  
		Last Modified: Fri, 22 May 2020 01:27:30 GMT  
		Size: 199.9 MB (199877491 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59b24efc5c168a889aa3ba6b8bd897ab3f7bda88afbb8c1704c2d8f30f1ad45a`  
		Last Modified: Tue, 02 Jun 2020 00:34:42 GMT  
		Size: 14.0 MB (13961257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aff4d44ce070ffc5c01020c044886c564e2152048f5ee7e5b2b0888d13a0812`  
		Last Modified: Tue, 02 Jun 2020 00:34:42 GMT  
		Size: 4.2 MB (4168211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
