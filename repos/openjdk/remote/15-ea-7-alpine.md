## `openjdk:15-ea-7-alpine`

```console
$ docker pull openjdk@sha256:023b41fc2518de0469207fcfb4ad5e6b0f5c62d64417b5358b70aebcf9391eea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `openjdk:15-ea-7-alpine` - linux; amd64

```console
$ docker pull openjdk@sha256:11ab53cea6259661a19af0f563d255bbcb1a402717acd78133c71abbfc518502
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **203.2 MB (203166392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3810a00a5a6a5baea34b414e9a6225e259c2e676b4bb2844f1e926db9aea2af5`
-	Default Command: `["jshell"]`

```dockerfile
# Sat, 18 Jan 2020 01:19:37 GMT
ADD file:e69d441d729412d24675dcd33e04580885df99981cec43de8c9b24015313ff8e in / 
# Sat, 18 Jan 2020 01:19:37 GMT
CMD ["/bin/sh"]
# Tue, 11 Feb 2020 01:23:05 GMT
ENV JAVA_HOME=/opt/openjdk-15
# Tue, 11 Feb 2020 01:23:05 GMT
ENV PATH=/opt/openjdk-15/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 11 Feb 2020 01:23:05 GMT
ENV JAVA_VERSION=15-ea+7
# Tue, 11 Feb 2020 01:23:05 GMT
ENV JAVA_URL=https://download.java.net/java/early_access/alpine/7/binaries/openjdk-15-ea+7_linux-x64-musl_bin.tar.gz
# Tue, 11 Feb 2020 01:23:06 GMT
ENV JAVA_SHA256=4e68bb97ffd64d0d84137cea9251ac47908fbbdcc62ae8c623a8f7fe06c87e7d
# Tue, 11 Feb 2020 01:24:40 GMT
RUN set -eux; 		wget -O /openjdk.tgz "$JAVA_URL"; 	echo "$JAVA_SHA256 */openjdk.tgz" | sha256sum -c -; 	mkdir -p "$JAVA_HOME"; 	tar --extract --file /openjdk.tgz --directory "$JAVA_HOME" --strip-components 1; 	rm /openjdk.tgz; 		java -Xshare:dump; 		java --version; 	javac --version
# Tue, 11 Feb 2020 01:24:41 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:c9b1b535fdd91a9855fb7f82348177e5f019329a58c53c47272962dd60f71fc9`  
		Last Modified: Fri, 17 Jan 2020 08:04:01 GMT  
		Size: 2.8 MB (2802957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f64d6539cf0791880e29bdec433c929ce2c0f4cbc58aa9c35de567fd0bddd694`  
		Last Modified: Tue, 11 Feb 2020 01:29:27 GMT  
		Size: 200.4 MB (200363435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
