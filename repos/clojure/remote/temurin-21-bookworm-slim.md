## `clojure:temurin-21-bookworm-slim`

```console
$ docker pull clojure@sha256:29c71286cd038dcdb843d0e8c6e3492616e29ed1faeb195f4d6ab6746c76f42a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-21-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:20ba15e7daff3948d0563ce8ab6833a59bbefc15d2dc806038f5b547d2f982bc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **259.7 MB (259714371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30d4f1119baeb625e790b5941110cb70eafbb5e6619dbb3c4c1ba50e90218566`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 01 Nov 2023 00:20:49 GMT
ADD file:fbd8521c24ed758023728505c18d7a0d6d101bc77fd772a4af9b65049b943864 in / 
# Wed, 01 Nov 2023 00:20:49 GMT
CMD ["bash"]
# Wed, 01 Nov 2023 01:12:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 01 Nov 2023 01:27:52 GMT
COPY dir:e6025cb107ac582823e7222bca84438ae7fa7384431777ac5a68b80c2a5b3d9d in /opt/java/openjdk 
# Wed, 01 Nov 2023 01:27:54 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Nov 2023 01:29:32 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Wed, 01 Nov 2023 01:29:32 GMT
WORKDIR /tmp
# Wed, 01 Nov 2023 01:29:49 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Wed, 01 Nov 2023 01:29:50 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Wed, 01 Nov 2023 01:29:50 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Wed, 01 Nov 2023 01:29:50 GMT
ENTRYPOINT ["entrypoint"]
# Wed, 01 Nov 2023 01:29:50 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:578acb154839e9d0034432e8f53756d6f53ba62cf8c7ea5218a2476bf5b58fc9`  
		Last Modified: Wed, 01 Nov 2023 00:25:30 GMT  
		Size: 29.1 MB (29149836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8034556024290c864d3a30b2dfb77cc1736954d8ddd6d5c03097e22ed9f2fe1d`  
		Last Modified: Wed, 01 Nov 2023 01:43:42 GMT  
		Size: 158.6 MB (158630541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a082a0f7d9b0698b20e7346147983f08f98104efbfb187efd474ab089979ec04`  
		Last Modified: Wed, 01 Nov 2023 01:45:31 GMT  
		Size: 71.9 MB (71932975 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d9056a3d98879a9947b339101e38eef1263e58bedf826a3d6121be2fb88c3a`  
		Last Modified: Wed, 01 Nov 2023 01:45:23 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e95718913089ebd998882a826a5d22a6c2f741bb6721f621cabe9709b38d03dd`  
		Last Modified: Wed, 01 Nov 2023 01:45:22 GMT  
		Size: 402.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-21-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:f1a9ff8e780f3f534c167c84858a1f0912b3e20076ed10546cfa4b1d175ad50c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **257.7 MB (257746547 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f71f3a954fd57dbe85e7ab5741625c57fe387121fd81ccaa8aeb96a35070d46`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:59:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 31 Oct 2023 01:11:43 GMT
COPY dir:6c09b6d38e0ce748c3ef1f9f172525f08b1f5fa7d2d583b56755ceb9d38b6e61 in /opt/java/openjdk 
# Tue, 31 Oct 2023 01:11:47 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Oct 2023 01:13:29 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Tue, 31 Oct 2023 01:13:29 GMT
WORKDIR /tmp
# Tue, 31 Oct 2023 01:13:44 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 31 Oct 2023 01:13:44 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 31 Oct 2023 01:13:44 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 31 Oct 2023 01:13:44 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 31 Oct 2023 01:13:44 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cd8871b0e55f38ce56a8b880f769b75073ab825edb77933a13b1470ee65187e`  
		Last Modified: Tue, 31 Oct 2023 01:27:30 GMT  
		Size: 156.9 MB (156872118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ce7117dee78a89e739ecd1fc535d8e61abeb0f9ea3c74d2f0a706bf3fe7c3d0`  
		Last Modified: Tue, 31 Oct 2023 01:29:20 GMT  
		Size: 71.7 MB (71694130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0d4f183d87e73ec031a6ba30989ded2c83b60b279773d4f896514a82a5ede93`  
		Last Modified: Tue, 31 Oct 2023 01:29:14 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e823ed0aa86e2c2809e515fe68bd661d5f71a2eba8b5906c0c5e4e0f30048686`  
		Last Modified: Tue, 31 Oct 2023 01:29:14 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
