## `clojure:temurin-17-bullseye-slim`

```console
$ docker pull clojure@sha256:f0f99a0b50055e248208eedac7d543d18345ce958f9d9cba4ba5d788dd19b9d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:89d65df906098d7a113bc04d9ff06b7cde952fbbf3284606cc6c22fe4cf24593
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **285.0 MB (285028856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243d41c115cdf96dba2bcb138e0181b59ac33e77de1d406461d3258890a870e5`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:39 GMT
ADD file:b78b777208be08edd8f297035cdfbacddb45170ad778fd643c792ee045187e39 in / 
# Tue, 04 Oct 2022 23:26:39 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:31:07 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:37:41 GMT
COPY dir:4a40d0ddbd507a7d3b3a97117be800fbf93534cac954d63629e4fb22f3cd41ad in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:37:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:39:35 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 05 Oct 2022 01:39:35 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:39:53 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Oct 2022 01:39:53 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Oct 2022 01:39:53 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:39:53 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:39:53 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:bd159e379b3b1bc0134341e4ffdeab5f966ec422ae04818bb69ecef08a823b05`  
		Last Modified: Tue, 04 Oct 2022 23:30:54 GMT  
		Size: 31.4 MB (31420102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f886809c89616aad77af0691ec37718e30fdcda3a35959fe64d1b37b7e2cfda5`  
		Last Modified: Wed, 05 Oct 2022 01:50:00 GMT  
		Size: 192.1 MB (192137460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be27e38d9ac5b4bbdb1da03cf3fcfe6821c8df59f02301f7e99475a7b198fae1`  
		Last Modified: Wed, 05 Oct 2022 01:51:12 GMT  
		Size: 61.5 MB (61470277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15abc83ea67ee64955620d18a9f25659d3c22bf4ac0d01e8b4e64351f73f984c`  
		Last Modified: Wed, 05 Oct 2022 01:51:04 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa0deac99fd55f465604feeea35991dbbfad35558de9328280bd2bc35870143`  
		Last Modified: Wed, 05 Oct 2022 01:51:04 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:df93c6cbe47f8f83573dd0da44760523f7d11d1bea43f6990fb29d0d875796ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **282.4 MB (282362580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:307811bb45cffc99a9c84b10572704091f4ac5e21fb1460e3139a8f59f940849`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:42 GMT
ADD file:dcb96c5906228cc8195f87d079b2a65ab49cde56edd7f0ccd238cdc65f9b693c in / 
# Tue, 04 Oct 2022 23:44:43 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:53 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:01:21 GMT
COPY dir:e8b09aac8a69a5f07df362ceeac55cf5f3321b4ba40e9b02e12250e34b34e83e in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:01:21 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:03:51 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 05 Oct 2022 01:03:51 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:04:09 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Oct 2022 01:04:10 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Oct 2022 01:04:11 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:04:11 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:04:12 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:df8e44b0463f16c791d040e02e9c3ef8ec2a84245d365f088a80a22a455c71e8`  
		Last Modified: Tue, 04 Oct 2022 23:50:23 GMT  
		Size: 30.1 MB (30064395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1a6c1d832d4d9011c73ee876bbbbdc9b3b0a7d057d4ff04d3b4078597e6a527`  
		Last Modified: Wed, 05 Oct 2022 01:18:30 GMT  
		Size: 190.9 MB (190904314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dfc6b9bdd6742e3bd3f7619df6bb96676f5029cd6558e49afbd115870f99886`  
		Last Modified: Wed, 05 Oct 2022 01:19:51 GMT  
		Size: 61.4 MB (61392850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e10727d43e3048110171ff4c901315f7460e0801c9c2f8246d170049bca56ea6`  
		Last Modified: Wed, 05 Oct 2022 01:19:43 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25aee392bcefd7122e2f744fc4a23f67bc3869ce130db9287f724906821f694b`  
		Last Modified: Wed, 05 Oct 2022 01:19:43 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
