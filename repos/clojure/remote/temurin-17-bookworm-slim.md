## `clojure:temurin-17-bookworm-slim`

```console
$ docker pull clojure@sha256:cb2b7894173c7ca361e5d625bed0aca410af41fc111e83cbab56b5569bc127d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-bookworm-slim` - linux; amd64

```console
$ docker pull clojure@sha256:bc587c9792cd5d68796b5c10120c5fbd593312505e17c93691724944d5da106f
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **245.9 MB (245859983 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c8693751b30fec65bf1a3bea6d844b38f215c6ef03179f5b14ac5434b81a6e6`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:28:06 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:34:34 GMT
COPY dir:762e280751e9eaacf2bfae42d6a8cb2a49846426bd7c5675b21a4c0c8ae8fb71 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:34:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:36:37 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 01:36:37 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:36:54 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 01:36:55 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 01:36:55 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:36:55 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:36:55 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb33a0642e97b629944310a73d2b5516fe91caf4addd502df39d147e81101246`  
		Last Modified: Fri, 13 Oct 2023 01:48:38 GMT  
		Size: 144.8 MB (144775771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5028220d4f2c4c99e48da6d8cfda328e389b842abc2b7396cbf4c8d01e6170`  
		Last Modified: Fri, 13 Oct 2023 01:49:47 GMT  
		Size: 71.9 MB (71933322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d06345d332a4fd046bd820bda8a61c2d181e40d8076e8e0adf46f019f00d349`  
		Last Modified: Fri, 13 Oct 2023 01:49:39 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fa52963f6c5677060b4328656bce258745ee3c6d7df6d9ed7cdf2a97e574e38`  
		Last Modified: Fri, 13 Oct 2023 01:49:39 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-bookworm-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:217acd47ad6f4bbb28abb20ec99c7b2a70c8c0d4b823b79bf0f0824fd9d1f564
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **244.4 MB (244418613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e199a0c2aba5912d69476d2c7130cead9b962252ea0acc9d248aebef523aae`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:59:51 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:05:21 GMT
COPY dir:9add47918f86acac35c907520d4811042633ac78a65fb2fbf0acc7586100f57a in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:05:24 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:07:05 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 01:07:06 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:07:20 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 01:07:21 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 01:07:21 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Fri, 13 Oct 2023 01:07:22 GMT
ENTRYPOINT ["entrypoint"]
# Fri, 13 Oct 2023 01:07:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4166017b3dfdb8fbf19b3063aec8aef41ca6e3d6c0e0f45f95bbf5bc223dddb2`  
		Last Modified: Fri, 13 Oct 2023 01:17:16 GMT  
		Size: 143.5 MB (143543519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:059bcc00c9ed6b62af17861f0c0ff7d124c47016f0570732aa9c61d58c4bab77`  
		Last Modified: Fri, 13 Oct 2023 01:18:20 GMT  
		Size: 71.7 MB (71694797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af79f020b87b70af66b4afcfeb8d079b5e77ba78c4df1ebfe9036e41a68f4edf`  
		Last Modified: Fri, 13 Oct 2023 01:18:13 GMT  
		Size: 614.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62a89f41a68ac54929ea6bc6ce3c26773c69f1485d97e27bb0a6607b559fe78d`  
		Last Modified: Fri, 13 Oct 2023 01:18:13 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
