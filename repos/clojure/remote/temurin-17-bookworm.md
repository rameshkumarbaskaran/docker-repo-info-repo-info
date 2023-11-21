## `clojure:temurin-17-bookworm`

```console
$ docker pull clojure@sha256:3f41c77023a7d155b9e72c2d57db29f9fc9b03052f49b20cad001e7c5f8321c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:a3b38d9c1b6e0df96289b56920ea893f4c4433abdd460e241009a0e322ca1f67
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **277.8 MB (277819728 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17e6a203556f84f307ecde4c2ca886d4f84ba893208cce379c9b230e9c3902ff`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:37 GMT
ADD file:3e9b6405f11dd24ce62105c033f1d8b931d9409298553f63b03af1b6dd1dda35 in / 
# Wed, 01 Nov 2023 00:20:38 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:10:45 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:22:31 GMT
COPY dir:33a61da93c3e1252ff87d5fd5f9955ca53f9f7f200758827548096d130b4307b in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:22:32 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:26:19 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 01 Nov 2023 01:26:19 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:26:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Nov 2023 01:26:37 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Nov 2023 01:26:37 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 01 Nov 2023 01:26:37 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Nov 2023 01:26:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:8457fd5474e70835e4482983a5662355d892d5f6f0f90a27a8e9f009997e8196`  
		Last Modified: Wed, 01 Nov 2023 00:25:05 GMT  
		Size: 49.6 MB (49582024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a05faf0cd98c5e3023b81d5851ba37c4093d2fdd6da9fc527471ac1aa01955`  
		Last Modified: Wed, 01 Nov 2023 01:39:48 GMT  
		Size: 144.9 MB (144873950 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:618bf9fe95adeafb6ba7a2d876c16b2b43131bd9fa28fd996af75f1c02d373cc`  
		Last Modified: Wed, 01 Nov 2023 01:41:58 GMT  
		Size: 83.4 MB (83362735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c051d7bc43ae166845750b9083aeff5f17f25f1712b739c0af0842dc3107a675`  
		Last Modified: Wed, 01 Nov 2023 01:41:49 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:401c0cb93af6a5f507908d3b88cca00466996657c0ca643bb47ab28d9a78bca5`  
		Last Modified: Wed, 01 Nov 2023 01:41:49 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:b37fc6821dd08a49038c870a9b2ea76dd2e99e71166a395a3b1edcd41c4858f6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **276.4 MB (276409435 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f47ccaff2c62e6b448c83b069c3ce79b6556a637475a80fda2c2ad12942dcdf`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:26:54 GMT
ADD file:6550a7c17e64067114283d098e85f9a74d4707f2879b53c2e4cae99f329c9025 in / 
# Tue, 21 Nov 2023 06:26:55 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:20:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 21 Nov 2023 07:30:54 GMT
COPY dir:888224b00e9a6a59c49b2cf85eae979985f73b3b17bec354827bf57eb1896417 in /opt/java/openjdk 
# Tue, 21 Nov 2023 07:30:58 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 21 Nov 2023 07:34:13 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Tue, 21 Nov 2023 07:34:13 GMT
WORKDIR /tmp
# Tue, 21 Nov 2023 07:34:28 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 21 Nov 2023 07:34:28 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 21 Nov 2023 07:34:29 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 21 Nov 2023 07:34:29 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 21 Nov 2023 07:34:29 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:df2021ddb7d686bdbb125598b2a6163d63035f080356b3014595f354ea0b40d6`  
		Last Modified: Tue, 21 Nov 2023 06:30:07 GMT  
		Size: 49.6 MB (49612650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bb7eea93e806cda12688c1cef1abab3769a83178187c1b5813f675ffa83e80f`  
		Last Modified: Tue, 21 Nov 2023 07:46:23 GMT  
		Size: 143.7 MB (143681765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e9df293bc46a766cadb0bb16ef4d05eb9a03bc186097ae00857642af197262`  
		Last Modified: Tue, 21 Nov 2023 07:48:17 GMT  
		Size: 83.1 MB (83114002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94ef02a7c9bebd22f2ffaa69787c62c8de2c6b0bd5dda72db2ca5da0ee6336d1`  
		Last Modified: Tue, 21 Nov 2023 07:48:08 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2e3bf7d31f6eca50d38f8dd85756cf388e5767b8de71ca08e181ec10caa4c1e`  
		Last Modified: Tue, 21 Nov 2023 07:48:08 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
