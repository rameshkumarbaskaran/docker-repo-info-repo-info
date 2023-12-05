## `clojure:temurin-17-tools-deps-1.11.1.1429-bullseye-slim`

```console
$ docker pull clojure@sha256:c5079af899f98519706174ceef805d76cd407bf098044cdd50b995bff1433b54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1429-bullseye-slim` - linux; amd64

```console
$ docker pull clojure@sha256:c89c51aad44202cc1bcee5df8964490b413ae391516a62b2d91dd1c417973b8a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **238.0 MB (237999271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bc83c99a8a8ab2e04dfb040e12a0f4a0d9a2f249028419a06ac915d7a6ab0f9`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Nov 2023 05:21:58 GMT
ADD file:e9f63d1defc55282fec6525ac2886c735dc2189e34105d7fe64c2420d6673922 in / 
# Tue, 21 Nov 2023 05:21:58 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 10:09:56 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 07:35:48 GMT
COPY dir:e13dbcd57950f4d4d23f4aba8428b6fbbf838d8f4801d32a25e344d37d33c37e in /opt/java/openjdk 
# Sat, 02 Dec 2023 10:03:26 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 18:30:05 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 05 Dec 2023 18:30:05 GMT
WORKDIR /tmp
# Tue, 05 Dec 2023 18:30:22 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 05 Dec 2023 18:30:22 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 05 Dec 2023 18:30:22 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 05 Dec 2023 18:30:22 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 05 Dec 2023 18:30:22 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:b7f91549542cca4b35a34cdee5364339f17468971ea730bb072864d3e78c8b94`  
		Last Modified: Tue, 21 Nov 2023 05:26:39 GMT  
		Size: 31.4 MB (31417824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db4929994d0853caabbfd68ce7ab07e3af7c0e483db2f66881247df513f25c95`  
		Last Modified: Sat, 02 Dec 2023 07:40:56 GMT  
		Size: 144.9 MB (144873901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a4d2ab7b222bd06a9f5ae8e21bc36eb6f2ac19355aa3082f6f40f84fba1477`  
		Last Modified: Tue, 05 Dec 2023 18:41:38 GMT  
		Size: 61.7 MB (61706529 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43cb3d5839a03d345c7436325c5b7fb451f771bc8de5d418a95917255cf78834`  
		Last Modified: Tue, 05 Dec 2023 18:41:30 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c895adb5cda418e8cee3aa01dc94e45b8a4ca146dad3552493f7c29886c5e1c`  
		Last Modified: Tue, 05 Dec 2023 18:41:30 GMT  
		Size: 400.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-17-tools-deps-1.11.1.1429-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:dd4b9ede4fb56e8d776487f9e755e9b8187c124a85f0ed84cd3f4456225f0fe9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.6 MB (235572155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a27d08cf149dedd5a5750f1941325e215a121f3953384d079d4632adf993fef`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 21 Nov 2023 06:27:20 GMT
ADD file:7b5bbc3b85f671aaf7b38dbe3fc76aae162bbff29c525bcd127f8a26a53bc664 in / 
# Tue, 21 Nov 2023 06:27:21 GMT
CMD ["bash"]
# Tue, 21 Nov 2023 07:22:57 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Sat, 02 Dec 2023 08:54:33 GMT
COPY dir:b97789a1c2e6d715436236e063679209ed5b51287e172faadc90d7cbd7bc1135 in /opt/java/openjdk 
# Sat, 02 Dec 2023 08:54:36 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 05 Dec 2023 19:45:50 GMT
ENV CLOJURE_VERSION=1.11.1.1429
# Tue, 05 Dec 2023 19:45:50 GMT
WORKDIR /tmp
# Tue, 05 Dec 2023 19:46:05 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "bf08cfeb007118b7277aa7423734f5d507604b868f7fc44c0f9929ca9cd94ed4 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Tue, 05 Dec 2023 19:46:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Tue, 05 Dec 2023 19:46:05 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Tue, 05 Dec 2023 19:46:05 GMT
ENTRYPOINT ["entrypoint"]
# Tue, 05 Dec 2023 19:46:05 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:ca426296fe928600d0b4b844aee43e2b70a05c6f4032de5f65dcc49f5cedfd82`  
		Last Modified: Tue, 21 Nov 2023 06:31:08 GMT  
		Size: 30.1 MB (30064123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39d93fb72555944d51d7e18e85dbba1405725af6fa11dc155f20ab3dc455df52`  
		Last Modified: Sat, 02 Dec 2023 09:08:50 GMT  
		Size: 143.7 MB (143681749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:540ac3f0e3c16138439415410534e926d1add8a878e5a859a5423ba006f47fb9`  
		Last Modified: Tue, 05 Dec 2023 19:55:31 GMT  
		Size: 61.8 MB (61825264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e966c3e0e1218db8f57be58a8906d564ff93c8d732c15c9ea3274599e4c4df`  
		Last Modified: Tue, 05 Dec 2023 19:55:25 GMT  
		Size: 618.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64d4802c1efac8c5c9e63087b898f19ee19d0f42591786e3be1380f169c60aff`  
		Last Modified: Tue, 05 Dec 2023 19:55:25 GMT  
		Size: 401.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
