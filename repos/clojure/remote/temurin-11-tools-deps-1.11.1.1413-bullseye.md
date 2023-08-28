## `clojure:temurin-11-tools-deps-1.11.1.1413-bullseye`

```console
$ docker pull clojure@sha256:8a820eb9d49ea026649ea21f8705d8390025f915a4d775ab36b81c461bf32df5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1413-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:16128155111886885a672803c23e7f05f707f3a4791603c757ba46b78da7c1ae
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **267.3 MB (267268469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684bfe1929ecc53351968bf1e2775d01276a270988c644d0752d454094c2ef71`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:21:45 GMT
COPY dir:6acc55ac013a722a8db4af8f0ce8de9270cd9aeb372e6c734b449d15adcc5218 in /opt/java/openjdk 
# Wed, 16 Aug 2023 17:21:49 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Aug 2023 19:42:19 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Mon, 28 Aug 2023 19:42:19 GMT
WORKDIR /tmp
# Mon, 28 Aug 2023 19:42:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 28 Aug 2023 19:42:34 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 28 Aug 2023 19:42:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:175ec2cb09b3952032a7dbf0cdc9f641b1c5035ea846b712b44240d849a2979f`  
		Last Modified: Wed, 16 Aug 2023 17:31:34 GMT  
		Size: 141.6 MB (141565216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e502d0f759d91d159ace796b8939e60fa98dcfbd1858906f1b200b7267bb86f`  
		Last Modified: Mon, 28 Aug 2023 19:48:36 GMT  
		Size: 72.0 MB (71997856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b5226c107d1aaa6232833e16181835e6d33b070908f765d2750316ddfc8da5b`  
		Last Modified: Mon, 28 Aug 2023 19:48:30 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
