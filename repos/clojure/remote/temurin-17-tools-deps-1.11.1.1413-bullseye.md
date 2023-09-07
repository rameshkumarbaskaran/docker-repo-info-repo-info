## `clojure:temurin-17-tools-deps-1.11.1.1413-bullseye`

```console
$ docker pull clojure@sha256:34e0d5a883db599991dac8e0fa8087a1d5d968548fa0b82c6522cd54f5c3ef0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1413-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:5381b8b93795e196b913c763c2031d932c060f0897a94c4c5b28c7bda1ea2ed6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271711020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c014c5a406a5abbba58cbcae78fad985828eb67a8684299df2f64668a87029c`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Thu, 07 Sep 2023 00:21:01 GMT
ADD file:144dff349a666134b5e98a9f1c6650fd9d6e4a88a6f98857f26eb84989360b91 in / 
# Thu, 07 Sep 2023 00:21:02 GMT
CMD ["bash"]
# Thu, 07 Sep 2023 03:17:24 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Thu, 07 Sep 2023 03:23:42 GMT
COPY dir:61bbef45bd137d5078f6a6f774d9bc49d275ae5fe27274294232d075ae1a5bf2 in /opt/java/openjdk 
# Thu, 07 Sep 2023 03:23:43 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 07 Sep 2023 03:25:37 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Thu, 07 Sep 2023 03:25:37 GMT
WORKDIR /tmp
# Thu, 07 Sep 2023 03:25:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Thu, 07 Sep 2023 03:25:55 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Thu, 07 Sep 2023 03:25:55 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Thu, 07 Sep 2023 03:25:55 GMT
ENTRYPOINT ["entrypoint"]
# Thu, 07 Sep 2023 03:25:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:5dea071bb9782209397443f024a630052ab7583e365894d414f1e39cd0f65025`  
		Last Modified: Thu, 07 Sep 2023 00:25:41 GMT  
		Size: 55.1 MB (55056245 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d64f659b2aacdd3e2363ebb3332a830f2dcd93164a10995d976ac13e700435f5`  
		Last Modified: Thu, 07 Sep 2023 03:33:07 GMT  
		Size: 144.8 MB (144775757 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3c2fd9aea5363425f5a26bf81871b4b12659c5373a7ecc858422ce15dd9ca4a`  
		Last Modified: Thu, 07 Sep 2023 03:34:10 GMT  
		Size: 71.9 MB (71877999 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d482ab4cbe79626fb5f974306bbb7254b3ccffe47574f1f974f8abe454c53a0`  
		Last Modified: Thu, 07 Sep 2023 03:34:02 GMT  
		Size: 619.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa34da6f62a4fb7b4f12a5535dc47d419905ea7acb5408d95497416d467c5a0`  
		Last Modified: Thu, 07 Sep 2023 03:34:02 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1413-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:6febc48d78ffbff7bab49b17ab82ae0fb59b183e33eec8aa86315da3fbbaad4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269247053 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbca2de04615f196b099515fab55d25ee1219144560ff9d0a56974184d3607ca`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:03 GMT
ADD file:8973cddb2d84a543b71001635599951bea6485a3526ae4ff916443b584864c83 in / 
# Tue, 15 Aug 2023 23:40:04 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:14 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Sep 2023 01:47:28 GMT
COPY dir:ffc7dc4725a3524e0b294e59a90d1e58e69ec448374b50aef6bef0cfa219cb0f in /opt/java/openjdk 
# Sat, 02 Sep 2023 01:47:31 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 02 Sep 2023 01:49:37 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Sat, 02 Sep 2023 01:49:37 GMT
WORKDIR /tmp
# Sat, 02 Sep 2023 01:49:51 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Sat, 02 Sep 2023 01:49:52 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Sat, 02 Sep 2023 01:49:52 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Sat, 02 Sep 2023 01:49:52 GMT
ENTRYPOINT ["entrypoint"]
# Sat, 02 Sep 2023 01:49:52 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:e837d9f05c625de5b814b851adbc03559ba02ea7078f57c81a01e18fc65bf42b`  
		Last Modified: Tue, 15 Aug 2023 23:43:37 GMT  
		Size: 53.7 MB (53704779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c782a1c2165dbdac384abd088ebc99d9f013b55fa39e22661861b6b10083b60`  
		Last Modified: Sat, 02 Sep 2023 01:55:28 GMT  
		Size: 143.5 MB (143543490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78f0abc7e257ecccb3255aeeff9edab7864b279263e5a15948e422bcd62b4c2a`  
		Last Modified: Sat, 02 Sep 2023 01:57:02 GMT  
		Size: 72.0 MB (71997768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd76f79d0cf59e6f65f1df3fc198bd95267efd4dc6285cc91ef21edb3ad4c68a`  
		Last Modified: Sat, 02 Sep 2023 01:56:55 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:147ecffdccfd1fc5156e85e078b02dea0dc3c48b6d0d52f081d2b9fdb4dd3ad0`  
		Last Modified: Sat, 02 Sep 2023 01:56:55 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
