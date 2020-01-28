## `openjdk:14-jdk-alpine`

```console
$ docker pull openjdk@sha256:b8082268ef46d44ec70fd5a64c71d445492941813ba9d68049be6e63a0da542f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:14-jdk-alpine` - linux; amd64

```console
$ docker pull openjdk@sha256:7c29ddf86e7fc5ea5fe01e1ad3e3439422fc50dc2c568b00d6bd79bdb026bfdf
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.1 MB (203142832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8273876b08aa52f215e5f471799f2f8c931db245772d2c55ebb3767c32e80a90`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 22:15:00 GMT
ENV JAVA_HOME=/opt/openjdk-14
# Thu, 23 Jan 2020 22:15:00 GMT
ENV PATH=/opt/openjdk-14/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Jan 2020 01:03:57 GMT
ENV JAVA_VERSION=14-ea+33
# Tue, 28 Jan 2020 01:03:57 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/alpine/33/binaries/openjdk-14-ea+33_linux-x64-musl_bin.tar.gz
# Tue, 28 Jan 2020 01:03:58 GMT
ENV JAVA_SHA256=25344fdf7438d05166fb3471a591aacf72e5fc7ca334b59b3f90ff34ee3b27e5
# Tue, 28 Jan 2020 01:05:39 GMT
RUN set -eux; 		wget -O /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 28 Jan 2020 01:05:39 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:345cf19c142c73b4673b7f5195d90723d77f452a902206b91c63c6ddca4e6bb7`  
		Last Modified: Tue, 28 Jan 2020 01:09:10 GMT  
		Size: 200.4 MB (200355870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
