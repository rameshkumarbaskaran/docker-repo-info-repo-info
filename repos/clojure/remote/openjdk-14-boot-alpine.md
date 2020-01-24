## `clojure:openjdk-14-boot-alpine`

```console
$ docker pull clojure@sha256:7faa699e3c7e9f90612bc21ff6e7e71b07c783909bf65331eb321759afb5fb48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-14-boot-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:9e497894fb89a6940bdb8e9626b55b1e8a9f93051bbfccd32c8e8b0a07d7cb1b
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **261.6 MB (261552278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1e7f31007d709b7e7b1f8685f11865fea5235a6882707d6ac0cee02aedea086`
-	Default Command: `["boot","repl"]`

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
# Fri, 24 Jan 2020 15:03:09 GMT
ENV BOOT_VERSION=2.8.3
# Fri, 24 Jan 2020 15:03:09 GMT
ENV BOOT_INSTALL=/usr/local/bin/
# Fri, 24 Jan 2020 15:03:09 GMT
WORKDIR /tmp
# Fri, 24 Jan 2020 15:03:11 GMT
RUN apk add --update --no-cache bash openssl && mkdir -p $BOOT_INSTALL && wget -q https://github.com/boot-clj/boot-bin/releases/download/latest/boot.sh && echo "Comparing installer checksum..." && echo "f717ef381f2863a4cad47bf0dcc61e923b3d2afb *boot.sh" | sha1sum -c - && mv boot.sh $BOOT_INSTALL/boot && chmod 0755 $BOOT_INSTALL/boot && apk del openssl
# Fri, 24 Jan 2020 15:03:11 GMT
ENV PATH=/opt/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/usr/local/bin/
# Fri, 24 Jan 2020 15:03:11 GMT
ENV BOOT_AS_ROOT=yes
# Fri, 24 Jan 2020 15:04:07 GMT
RUN boot
# Fri, 24 Jan 2020 15:04:07 GMT
CMD ["boot" "repl"]
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
	-	`sha256:95b33294ee4e1c6f5adbddb49468093628321ea09dc3832a24cae192f296385b`  
		Last Modified: Fri, 24 Jan 2020 15:05:22 GMT  
		Size: 1.2 MB (1217249 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a096e464a1b498cac74e8bbc1c6f4418ba7a25bd70785aaf0344b790674b56a`  
		Last Modified: Fri, 24 Jan 2020 15:05:59 GMT  
		Size: 58.8 MB (58821018 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
