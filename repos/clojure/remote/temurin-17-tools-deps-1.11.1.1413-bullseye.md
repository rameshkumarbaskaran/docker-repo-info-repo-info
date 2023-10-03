## `clojure:temurin-17-tools-deps-1.11.1.1413-bullseye`

```console
$ docker pull clojure@sha256:4901a76b2f5eb4031d44660de5e6251f9e504887169007a1728db1931cd706aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1413-bullseye` - linux; amd64

```console
$ docker pull clojure@sha256:78fdd1ebbcd368a9ead553088f93a39bb29794945c8990acb5ab95b07a2dba89
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **271.7 MB (271711260 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:adc146fa5de4e27204f728fad933522ef5ccaef4af42012009ddcd3148c6459f`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 20 Sep 2023 04:55:51 GMT
ADD file:85db4f4c5016f51f7112a5d09cb7d4620f565a1379ae4b8a03c5ffc23886a876 in / 
# Wed, 20 Sep 2023 04:55:51 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 07:21:46 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:43:41 GMT
COPY dir:762e280751e9eaacf2bfae42d6a8cb2a49846426bd7c5675b21a4c0c8ae8fb71 in /opt/java/openjdk 
# Tue, 03 Oct 2023 08:43:42 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 08:46:08 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Tue, 03 Oct 2023 08:46:08 GMT
WORKDIR /tmp
# Tue, 03 Oct 2023 08:49:17 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 03 Oct 2023 08:49:18 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 03 Oct 2023 08:49:18 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 03 Oct 2023 08:49:18 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Oct 2023 08:49:18 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ddf874abf16cc990e0fd75a154a34ca0a03ee310ad895a18fb62ae15bf4171fb`  
		Last Modified: Wed, 20 Sep 2023 05:00:41 GMT  
		Size: 55.1 MB (55056714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839a366a404f6bbe3f097947a53809bf4f2f44e369fe03fba1600160364fd8b8`  
		Last Modified: Tue, 03 Oct 2023 08:56:31 GMT  
		Size: 144.8 MB (144775733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39035a11ee945b7897c64febefde2221a5f7b50953e8ba051e5d4fefeead5168`  
		Last Modified: Tue, 03 Oct 2023 08:58:17 GMT  
		Size: 71.9 MB (71877792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2f69213b32a9ac6e8cd43eebc87420361edba29f813796be8cef245d574d76`  
		Last Modified: Tue, 03 Oct 2023 08:58:09 GMT  
		Size: 620.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f00f861fb3166ab441415c102f88eaaf8d9472a02afe4882e34cedc30ac8cb3`  
		Last Modified: Tue, 03 Oct 2023 08:58:09 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1413-bullseye` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:5846230afbb1d4d975f5b0067d0304c76b8103db2b0f0cc3342bb2ecf4a2a745
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **269.2 MB (269246923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e80e88383bc63ef6aa6962bd4b7ce44e4ca084e2e66129ddeb735920be0ca02`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:20 GMT
ADD file:46dcdcde338d2c01fed5db3fac9041736d9305145d8fc2039dd5b3714d38ede8 in / 
# Wed, 20 Sep 2023 02:44:21 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 09:47:32 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Tue, 03 Oct 2023 08:32:04 GMT
COPY dir:9add47918f86acac35c907520d4811042633ac78a65fb2fbf0acc7586100f57a in /opt/java/openjdk 
# Tue, 03 Oct 2023 08:32:08 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 08:34:21 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Tue, 03 Oct 2023 08:34:21 GMT
WORKDIR /tmp
# Tue, 03 Oct 2023 08:34:36 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 03 Oct 2023 08:34:37 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 03 Oct 2023 08:34:37 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 03 Oct 2023 08:34:37 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 03 Oct 2023 08:34:37 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:31f5dc1f52c865588c43d8ec718f14d430e149b28f0b28232da825da7ae28f76`  
		Last Modified: Wed, 20 Sep 2023 02:47:53 GMT  
		Size: 53.7 MB (53704892 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:454f2e89c1f4660d2a5b13696facffb72e0a5d41487f6b725e2eb710509b3c64`  
		Last Modified: Tue, 03 Oct 2023 08:40:54 GMT  
		Size: 143.5 MB (143543519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa9ffb8ea91dc2ece0939387680a58c1be75aab996f0cd363d479545d97966eb`  
		Last Modified: Tue, 03 Oct 2023 08:42:33 GMT  
		Size: 72.0 MB (71997496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f4a6a521fc4f295c61d1b8b1ac12da8e53da7b5d6d437afe3713b982305753d`  
		Last Modified: Tue, 03 Oct 2023 08:42:26 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56aba91f99562f55705cb7127d757e402bb8f917d73c0f27a8bb7120b7cffec2`  
		Last Modified: Tue, 03 Oct 2023 08:42:26 GMT  
		Size: 399.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
