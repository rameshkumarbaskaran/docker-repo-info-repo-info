## `clojure:openjdk-14-alpine`

```console
$ docker pull clojure@sha256:e9ddd431a3c483e9fb10d6ff2636422db02de0c82b078b598b9c1b70a2c1e07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-14-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:a47e34f63ff53107eb48d03a5394b05dd3461468ec28a391f1d655b44320844e
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **220.0 MB (220029717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c87d581482cf7024f3fc0c8598eb8225a7ec317fac002cc4271cc27870ba5cf`
-	Default Command: `["lein","repl"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:15:00 GMT
ENV JAVA_HOME=/opt/openjdk-14
# Thu, 23 Jan 2020 22:15:00 GMT
ENV PATH=/opt/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 22:15:00 GMT
ENV JAVA_VERSION=14-ea+15
# Thu, 23 Jan 2020 22:15:00 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/alpine/15/binaries/openjdk-14-ea+15_linux-x64-musl_bin.tar.gz
# Thu, 23 Jan 2020 22:15:01 GMT
ENV JAVA_SHA256=76091da1b6ed29788f0cf85454d23900a4134286e5feb571247e5861f618d3cd
# Thu, 23 Jan 2020 22:16:42 GMT
RUN set -eux; 		wget -O /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		java -Xshare:dump; 		java --version; 	javac --version
# Thu, 23 Jan 2020 22:16:42 GMT
CMD ["jshell"]
# Fri, 24 Jan 2020 15:02:57 GMT
ENV LEIN_VERSION=2.9.1
# Fri, 24 Jan 2020 15:02:57 GMT
ENV LEIN_INSTALL=/usr/local/bin/
# Fri, 24 Jan 2020 15:02:58 GMT
WORKDIR /tmp
# Fri, 24 Jan 2020 15:03:00 GMT
RUN apk add --update --no-cache bash tar openssl gnupg && mkdir -p $LEIN_INSTALL && wget -q https://raw.githubusercontent.com/technomancy/leiningen/$LEIN_VERSION/bin/lein-pkg && echo "Comparing lein-pkg checksum ..." && sha1sum lein-pkg && echo "93be2c23ab4ff2fc4fcf531d7510ca4069b8d24a *lein-pkg" | sha1sum -c - && mv lein-pkg $LEIN_INSTALL/lein && chmod 0755 $LEIN_INSTALL/lein && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip && wget -q https://github.com/technomancy/leiningen/releases/download/$LEIN_VERSION/leiningen-$LEIN_VERSION-standalone.zip.asc && gpg --batch --keyserver pool.sks-keyservers.net --recv-key 2B72BF956E23DE5E830D50F6002AF007D1A7CC18 && echo "Verifying Jar file signature ..." && gpg --verify leiningen-$LEIN_VERSION-standalone.zip.asc && rm leiningen-$LEIN_VERSION-standalone.zip.asc && mkdir -p /usr/share/java && mv leiningen-$LEIN_VERSION-standalone.zip /usr/share/java/leiningen-$LEIN_VERSION-standalone.jar && apk del tar openssl gnupg
# Fri, 24 Jan 2020 15:03:01 GMT
ENV PATH=/opt/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 24 Jan 2020 15:03:01 GMT
ENV LEIN_ROOT=1
# Fri, 24 Jan 2020 15:03:05 GMT
RUN echo '(defproject dummy "" :dependencies [[org.clojure/clojure "1.10.1"]])' > project.clj   && lein deps && rm project.clj
# Fri, 24 Jan 2020 15:03:05 GMT
CMD ["lein" "repl"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7429ae8c261d6aa4d644ad3ea6a358cb2363e002bc4b2ca644cf5968e1ed3eb`  
		Last Modified: Thu, 23 Jan 2020 22:19:12 GMT  
		Size: 198.7 MB (198727049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afbf31856adc8dbecde2e22d5e6f71dea566280e611a28e57c89fc5824ee2742`  
		Last Modified: Fri, 24 Jan 2020 15:05:16 GMT  
		Size: 14.3 MB (14347582 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:207cd98985f58d710e8564da2b8975b5d5cb766d3cf69ee6d702a6f9c0da30a7`  
		Last Modified: Fri, 24 Jan 2020 15:05:15 GMT  
		Size: 4.2 MB (4168124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
