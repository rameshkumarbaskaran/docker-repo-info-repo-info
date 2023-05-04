## `clojure:temurin-11-tools-deps-bullseye`

```console
$ docker pull clojure@sha256:e0d60f4ea30654892b1c4e26f80fb24ac4610ce6f32e6004582f44e7ff05846d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:e4e1b1f31c85dacc3bd5a13c514e54cb3317428bb646041c6e02a396eddfe806
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325479325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db7275718c9a7d1f644617c0df184c724e8e968ad2b854c030e27715f4b452c8`
-	Default Command: `["clj"]`

```dockerfile
# Tue, 02 May 2023 23:46:50 GMT
ADD file:fc290cf8ddb984325474583faa79c5a98c5ea0ec7f606bf360251f63acecf389 in / 
# Tue, 02 May 2023 23:46:51 GMT
CMD ["bash"]
# Wed, 03 May 2023 20:24:09 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 03 May 2023 20:26:50 GMT
COPY dir:df592a42a629b9630bdf0ab57a63e6c60f66d91934439985e01efbb58723e9ee in /opt/java/openjdk 
# Wed, 03 May 2023 20:26:51 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 20:28:48 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Wed, 03 May 2023 20:28:48 GMT
WORKDIR /tmp
# Wed, 03 May 2023 20:29:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 03 May 2023 20:29:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 03 May 2023 20:29:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:918547b9432687b1e1d238e82dc1e0ea0b736aafbf3c402eea98c6db81a9cb65`  
		Last Modified: Tue, 02 May 2023 23:49:58 GMT  
		Size: 55.0 MB (55049070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:127538ce586198e269e9a4ff9f0268aed32fd316a7287fcdb85700312b200f6e`  
		Last Modified: Wed, 03 May 2023 20:36:35 GMT  
		Size: 198.5 MB (198549535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efde4265af1c9ef6a51cd739653e0b5cd4b90da3817cebafcee4afd60a2f104e`  
		Last Modified: Wed, 03 May 2023 20:37:33 GMT  
		Size: 71.9 MB (71880106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cbde4bd405e33106857ec299076983ebf93148ea6bc4370de80ba9279574e89`  
		Last Modified: Wed, 03 May 2023 20:37:25 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5eaaaee84b9f5f93f6a2cdbded6b36482997e7883af802082be50c4d96fbe3fe
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **321.0 MB (321014323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49295209ddcdcc0e9928c20a35b83778a8e8ad979e787081266730c88bb73c12`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 03 May 2023 00:22:41 GMT
ADD file:f930fdb659332a615b0042ca415d6d7feda9ba6b2f58222e3e5bbed326db4d40 in / 
# Wed, 03 May 2023 00:22:42 GMT
CMD ["bash"]
# Wed, 03 May 2023 17:43:29 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 04 May 2023 10:10:06 GMT
COPY dir:377359689ec5fd1035465458ec6eb78fc3e8352f259756650a4953f3054fef1a in /opt/java/openjdk 
# Thu, 04 May 2023 10:10:10 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 04 May 2023 10:12:41 GMT
ENV CLOJURE_VERSION=1.11.1.1273
# Thu, 04 May 2023 10:12:41 GMT
WORKDIR /tmp
# Thu, 04 May 2023 10:13:03 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "4938afe6c0690d2a6553141857742d94a7350c02b4fa57cd6a9c1b7cbe66492e *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 04 May 2023 10:13:04 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 04 May 2023 10:13:04 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:d677c78be691f8dcbe9d44ce576b97ad205b3dd78557dc62794e59eb19553ee9`  
		Last Modified: Wed, 03 May 2023 00:25:31 GMT  
		Size: 53.7 MB (53692705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:750c5a6a1f6f22a3a543fac8f9799adc5539c91b044752b8b8e66c73d3c5014f`  
		Last Modified: Thu, 04 May 2023 10:19:50 GMT  
		Size: 195.3 MB (195324193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:102c752f56f44ed5d3327c73bd2a66642a56d58ed6ca2de96f6f4641d09628b9`  
		Last Modified: Thu, 04 May 2023 10:21:07 GMT  
		Size: 72.0 MB (71996812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edfc314801d38073b3359abb6edc11137e333b50b5d4dec9e7014057c467cbc4`  
		Last Modified: Thu, 04 May 2023 10:21:01 GMT  
		Size: 613.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
