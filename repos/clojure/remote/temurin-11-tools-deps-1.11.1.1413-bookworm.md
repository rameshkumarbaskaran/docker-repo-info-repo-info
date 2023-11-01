## `clojure:temurin-11-tools-deps-1.11.1.1413-bookworm`

```console
$ docker pull clojure@sha256:e259bf5c1d71c28cdd87a1fc1f6a6aa5ae0e70f1df3805a416ac269302d9c182
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-11-tools-deps-1.11.1.1413-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a6f93ea05d7841425ad56501db9c4485414297c0423389f7efba55234a40cd94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **278.2 MB (278213205 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e388f89dda831c53dccb32a3d7201c627319ed1ee6bcbd3867bc08ab8f11cc0d`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:37 GMT
ADD file:3e9b6405f11dd24ce62105c033f1d8b931d9409298553f63b03af1b6dd1dda35 in / 
# Wed, 01 Nov 2023 00:20:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:10:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:17:13 GMT
COPY dir:a96babc4beed1ce86268c08da8bb1232eedf77a64576d0e7cc109ca29beb78ef in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:17:14 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:20:58 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 01 Nov 2023 01:20:58 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:21:15 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Nov 2023 01:21:16 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Nov 2023 01:21:16 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:8457fd5474e70835e4482983a5662355d892d5f6f0f90a27a8e9f009997e8196`  
		Last Modified: Wed, 01 Nov 2023 00:25:05 GMT  
		Size: 49.6 MB (49582024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c52bf082e2f57af3aac777d96ce5e6d17154d3e9980eb8b5ffbaffaa59e38fbe`  
		Last Modified: Wed, 01 Nov 2023 01:36:16 GMT  
		Size: 145.3 MB (145266685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978d70079c178f74ed8e29e616b7bedaef1aa4a3cab2a9b0898186c3229f0351`  
		Last Modified: Wed, 01 Nov 2023 01:38:27 GMT  
		Size: 83.4 MB (83363876 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a36d7b3cb7af58b7cda5498cd4d3847627637d632a267e97288d1a92849ea7`  
		Last Modified: Wed, 01 Nov 2023 01:38:19 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-11-tools-deps-1.11.1.1413-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:c103cfdd23f7031e52311381939d6b3323e13d788dfe8794d0184ed3adb27eb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **274.7 MB (274729135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a59e8c48b2c21589158474ef4e44c489071648c94c266fb251ebbc3b6058b2d`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 00:56:49 GMT
COPY dir:434bcbe7e3d8ce2c5a3427f1d3fb9b84e4c00833b8498e54aed72311e918f97b in /opt/java/openjdk 
# Tue, 31 Oct 2023 00:56:53 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 01:02:07 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Tue, 31 Oct 2023 01:02:07 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 01:02:23 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 31 Oct 2023 01:02:24 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 31 Oct 2023 01:02:24 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1c4e8ef7ccc180ff3f55a838440893d12f85b3230824ad344a7d06524ac494`  
		Last Modified: Tue, 31 Oct 2023 01:17:21 GMT  
		Size: 142.0 MB (142001954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f0274d7a1c8643644fd2d9334080379619b20357441ebc8a1b42053dc3c806c`  
		Last Modified: Tue, 31 Oct 2023 01:20:11 GMT  
		Size: 83.1 MB (83113989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6ce319dfb20dd06be047ee8007e01471e08b671c1ccb48e7baef85806165dfa`  
		Last Modified: Tue, 31 Oct 2023 01:20:01 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
