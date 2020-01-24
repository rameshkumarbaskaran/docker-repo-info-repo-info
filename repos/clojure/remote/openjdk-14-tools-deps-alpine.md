## `clojure:openjdk-14-tools-deps-alpine`

```console
$ docker pull clojure@sha256:e37bbb90920c4dffd563904ce244a2d41f3a2dc9f969bdc6a57684e734b0f6e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-14-tools-deps-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:953391e0491bfd51f893ae823f445405049e32d9d4d1361f8043dc8a7c9dd860
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **224.5 MB (224451919 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ea831c5f55902822b8a0379509e681b818d01054f6b51fce3ee976d9d7f3b4d`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

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
# Fri, 24 Jan 2020 15:04:12 GMT
ENV CLOJURE_VERSION=1.10.1.502
# Fri, 24 Jan 2020 15:04:12 GMT
WORKDIR /tmp
# Fri, 24 Jan 2020 15:04:21 GMT
RUN apk add --update --no-cache curl bash make && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Fri, 24 Jan 2020 15:04:21 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
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
	-	`sha256:d5fe372e5c788e22453d7dd0abc7e8a7efaba7d335c41001f3c82c228c337644`  
		Last Modified: Fri, 24 Jan 2020 15:06:19 GMT  
		Size: 22.9 MB (22937908 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
