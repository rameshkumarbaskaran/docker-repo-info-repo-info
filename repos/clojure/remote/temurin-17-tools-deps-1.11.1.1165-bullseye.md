## `clojure:temurin-17-tools-deps-1.11.1.1165-bullseye`

```console
$ docker pull clojure@sha256:48a36d619e3fafc90865fb99053a29ad10e0a395fa7a8602f2cb1e657d0f5bb4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1165-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:1f748392a1f7516628da5a15152905608f1d7fd12ea4f8a0f0d81ab1d8e4a8ce
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **294.5 MB (294481000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:638a22c1fa3d9dff26b4da947d29d6427a4e29e5362f2008ebf57d35762c2828`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:26:27 GMT
ADD file:d1268789456d2cdace6e50149e60404ad5a849b7c61e8fc8bc7b6e0eb6eeb7ca in / 
# Tue, 04 Oct 2022 23:26:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 01:30:18 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:37:02 GMT
COPY dir:4a40d0ddbd507a7d3b3a97117be800fbf93534cac954d63629e4fb22f3cd41ad in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:37:03 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:39:15 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 05 Oct 2022 01:39:15 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:39:31 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Oct 2022 01:39:31 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Oct 2022 01:39:32 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:39:32 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:39:32 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:f606d8928ed378229f2460b94b504cca239fb906efc57acbdf9340bd298d5ddf`  
		Last Modified: Tue, 04 Oct 2022 23:30:27 GMT  
		Size: 55.0 MB (55046248 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:246324c7fe2aef771872cc58b2263426b55fe7dac3971cdd927d7d8f31e97361`  
		Last Modified: Wed, 05 Oct 2022 01:49:36 GMT  
		Size: 192.1 MB (192137613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d072b86498a00745ae1031f0597a1f54e7200ef7016590dbe80e3e8cfb1f7280`  
		Last Modified: Wed, 05 Oct 2022 01:50:52 GMT  
		Size: 47.3 MB (47296125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01ecde663b6c7c439f9bd56825ba481ad5c3a9fe4e7f6c74e4c5abc8eec366e2`  
		Last Modified: Wed, 05 Oct 2022 01:50:47 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d92ebe25b5f2f27a4a92b0422aaf625d25d1ac670c0f2ad6830ae4c34a5e93`  
		Last Modified: Wed, 05 Oct 2022 01:50:47 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1165-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f04dd591d6de2086c8659232a9e7c184f7912c88b2ca0a018fa9858f8ab72bb7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **291.7 MB (291692522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aab1454d92b7ce4b6587f79344f7b2c0b682f78f85a1a32be193c7523056e3b`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 04 Oct 2022 23:44:26 GMT
ADD file:59bc45fad9cada77bf8e44ebdd982c7f6e575816b5ed6b7d1d8494faddd9b8b9 in / 
# Tue, 04 Oct 2022 23:44:27 GMT
CMD ["bash"]
# Wed, 05 Oct 2022 00:53:15 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 05 Oct 2022 01:00:39 GMT
COPY dir:e8b09aac8a69a5f07df362ceeac55cf5f3321b4ba40e9b02e12250e34b34e83e in /opt/java/openjdk 
# Wed, 05 Oct 2022 01:00:39 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Oct 2022 01:03:24 GMT
ENV CLOJURE_VERSION=1.11.1.1165
# Wed, 05 Oct 2022 01:03:25 GMT
WORKDIR /tmp
# Wed, 05 Oct 2022 01:03:40 GMT
RUN apt-get update && apt-get install -y curl make rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "72d662bdc99b79037f9e34996272384de35e01e0416d8eb79cc940ee0f0fc808 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 05 Oct 2022 01:03:41 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 05 Oct 2022 01:03:42 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 05 Oct 2022 01:03:42 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 05 Oct 2022 01:03:43 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:172730635f67c8f081f43275b390514bd8a05a4a7c3c467ae74ee42a029dce2b`  
		Last Modified: Tue, 04 Oct 2022 23:49:51 GMT  
		Size: 53.7 MB (53700625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:132b7e60c64f8a4fd0d535e40cea1fe52e0d5b1669f1b30376daf898759039f9`  
		Last Modified: Wed, 05 Oct 2022 01:18:02 GMT  
		Size: 190.9 MB (190904260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45322c2105a195ad09c4a06b9861f8b226018a40c501eb5609d9c801442f3db0`  
		Last Modified: Wed, 05 Oct 2022 01:19:29 GMT  
		Size: 47.1 MB (47086620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40a2d9405a23f1c90c94495987baeeca08050bf3ec91b4cffda8e95fb555a31d`  
		Last Modified: Wed, 05 Oct 2022 01:19:23 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66c622b33d7da7c7ed2cf99fd986c8fc46b92e181324cad18045e24c6eb4a27c`  
		Last Modified: Wed, 05 Oct 2022 01:19:23 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
