## `clojure:openjdk-15-tools-deps-1.10.1.536-alpine`

```console
$ docker pull clojure@sha256:e8a9d2c11e209e8f7662cdf42786a0f9a29ed16c45aaadb032ac52cd5fee5058
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `clojure:openjdk-15-tools-deps-1.10.1.536-alpine` - linux; amd64

```console
$ docker pull clojure@sha256:ee8e0b81136062645ac93870657801c52d1ab9b1fb53c3d686ba6d8cd76db9f8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **225.2 MB (225200565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e00ea0212b17091717018c22894022e391f6da2715ce3d168b97f8c47235205`
-	Default Command: `["sh","-c","sleep 1 && exec clj"]`

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
# Tue, 02 Jun 2020 00:29:07 GMT
ENV CLOJURE_VERSION=1.10.1.536
# Tue, 02 Jun 2020 00:29:07 GMT
WORKDIR /tmp
# Tue, 02 Jun 2020 00:29:15 GMT
RUN apk add --update --no-cache curl bash make && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "83b824091723afe8e0f4e958bf74a2f7cd4c4caddd34e31af6ef1a4323c45ff1 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apk del curl
# Tue, 02 Jun 2020 00:29:15 GMT
CMD ["sh" "-c" "sleep 1 && exec clj"]
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
	-	`sha256:5c5d3ad0fb8589ba54d3044d4e1a1f6b93cdb3585216bceda50f67ee583f8f03`  
		Last Modified: Tue, 02 Jun 2020 00:35:02 GMT  
		Size: 22.5 MB (22509758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
