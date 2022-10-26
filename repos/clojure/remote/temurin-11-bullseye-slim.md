## `clojure:temurin-11-bullseye-slim`

```console
$ docker pull clojure@sha256:9633d2510f958ce791a6a8c42b46f0e0a203e34d7c058396a985140239a22757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:d300d647429606ba9a00c93efb629cd84aa6e49d55ada77a24f0dd69c4532b12
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.0 MB (291017277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71cfb3034d31848f263f96c3b25926f015ad7e3c54dd5357308cd875ea2e2242`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 25 Oct 2022 01:43:53 GMT
ADD file:8644a8156a07a656a35c41e2b2a458befb660309f8592e3efd5b43d46156cec2 in / 
# Tue, 25 Oct 2022 01:43:53 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 02:33:26 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 21:50:03 GMT
COPY dir:80db6f3290e8de5c875b6f069ca1d81f6b5c9f4e34668a64373c380a024a607d in /opt/java/openjdk 
# Wed, 26 Oct 2022 21:50:04 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 21:53:34 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 26 Oct 2022 21:53:34 GMT
WORKDIR /tmp
# Wed, 26 Oct 2022 21:53:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 26 Oct 2022 21:53:54 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 26 Oct 2022 21:53:54 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e9995326b091af7b3ce352fad4d76cf3a3cb62b7a0c35cc5f625e8e649d23c50`  
		Last Modified: Tue, 25 Oct 2022 01:47:55 GMT  
		Size: 31.4 MB (31420038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c841fe95a1d54b7ca4c2b99fafd39b67e5751811eec91ebb5a03381e515360e`  
		Last Modified: Wed, 26 Oct 2022 22:07:24 GMT  
		Size: 198.1 MB (198124716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b14a47c8bdca112cecf91ccda0cb2890b0f430e8fb7b0940adbe051cb8cb7ad6`  
		Last Modified: Wed, 26 Oct 2022 22:09:20 GMT  
		Size: 61.5 MB (61471905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6060bc58c730b47f708b1a2e707a2816f4a2edf09f7eaafa4d07459d840e0655`  
		Last Modified: Wed, 26 Oct 2022 22:09:12 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:73d85186334f065cc6b2fe270fd44e20514282def13159501686c1ad00e5b1c8
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **286.5 MB (286523949 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a32c18261d7cdba062ea1ef3feb83aea74b9994c59713d7650586a3fd34219a8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 25 Oct 2022 05:46:02 GMT
ADD file:d3de9d6279224464018a7153274276a9969483d143046bebe898b59aeaf3a518 in / 
# Tue, 25 Oct 2022 05:46:03 GMT
CMD ["bash"]
# Tue, 25 Oct 2022 10:46:03 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 26 Oct 2022 15:38:30 GMT
COPY dir:0c9c8c2b9cd43799d246d5824c591352650ad79f5d15544287f00c2deb1e4608 in /opt/java/openjdk 
# Wed, 26 Oct 2022 15:38:34 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Oct 2022 15:43:38 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 26 Oct 2022 15:43:38 GMT
WORKDIR /tmp
# Wed, 26 Oct 2022 15:44:06 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 26 Oct 2022 15:44:06 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 26 Oct 2022 15:44:06 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:dd6189d6fc13cb03db0f4a3d9659b6b6044fd5858019d659001eaf8367584d67`  
		Last Modified: Tue, 25 Oct 2022 05:49:06 GMT  
		Size: 30.1 MB (30063910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5a3d7b35da3e357173d5404cc59df1a4394d6031ee4598b02de7918d2110bae`  
		Last Modified: Wed, 26 Oct 2022 15:58:03 GMT  
		Size: 194.9 MB (194866982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbade15d78b9b4157d08f1b59bcaf584087766f92529468dcfa03dbf51883a08`  
		Last Modified: Wed, 26 Oct 2022 15:59:54 GMT  
		Size: 61.6 MB (61592438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a905da6f58673902d868ada3df855423b7efe1c8a5b21827a5b0c05c340dcfe9`  
		Last Modified: Wed, 26 Oct 2022 15:59:48 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
