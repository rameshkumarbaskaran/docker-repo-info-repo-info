## `clojure:temurin-8-tools-deps-1.11.1.1413-bookworm`

```console
$ docker pull clojure@sha256:4dbe71a8dcde5d0fcb6970c93adef7118679ef699a9d124233c9ffcf1ad74e2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 2
	-	linux; amd64
	-	linux; arm64 variant v8

### `clojure:temurin-8-tools-deps-1.11.1.1413-bookworm` - linux; amd64

```console
$ docker pull clojure@sha256:25653421190b563684b628367aa666ff7a1086ec3911682d68e89ad63f64e4ec
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **236.5 MB (236533003 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebfddc3aea3ded3aef8cd362bc5903e1b0d919ebfdbb52171070f3c1e5b8e273`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:37 GMT
ADD file:1e4dd5dab602337b5d5ef8d84b8dbe8b1ac62225f077b29b27d045842486d8e2 in / 
# Wed, 11 Oct 2023 18:34:37 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 01:26:33 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 01:27:34 GMT
COPY dir:66cfc1773e07dead4d108eefca05e38bbe528aec6797deefc0559c5a4d41e721 in /opt/java/openjdk 
# Fri, 13 Oct 2023 01:27:35 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:29:46 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 01:29:46 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:30:04 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 01:30:05 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 01:30:05 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:0a9573503463fd3166b5b1f34a7720dac28609e98d731e50e7068f92e79b8545`  
		Last Modified: Wed, 11 Oct 2023 18:39:10 GMT  
		Size: 49.6 MB (49582224 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1de82c0f73ff6fa256f1fe1c33f18ffe9340b6034d90e0f84a2b65951b4e4920`  
		Last Modified: Fri, 13 Oct 2023 01:44:19 GMT  
		Size: 103.6 MB (103585016 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a079a9adac1d6382445b97d7bc8e11557eb5ea6cdc2256e4d29e5af50e1b5236`  
		Last Modified: Fri, 13 Oct 2023 01:45:28 GMT  
		Size: 83.4 MB (83365147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ee93937baf7595b38f84679298cea04f6ab19828f24552be9e5d07a06e14d1`  
		Last Modified: Fri, 13 Oct 2023 01:45:18 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `clojure:temurin-8-tools-deps-1.11.1.1413-bookworm` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:72f240667f4b92aa035fd046d8eb1ff7bdebf3c47113db37df523dd22748546a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.4 MB (235421705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1294f5c7e5c694d25ae60df7f7a043a2bc503d308d348a8a6b446c655c437c5`
-	Default Command: `["clj"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:43 GMT
ADD file:bf4264671bd91eb30c67d512144ebcf7f5c55a3e490ebe7876fa9b20d433bf7b in / 
# Wed, 11 Oct 2023 18:24:44 GMT
CMD ["bash"]
# Fri, 13 Oct 2023 00:57:54 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Fri, 13 Oct 2023 00:58:44 GMT
COPY dir:b83f0a0f236c1f97de459c8ae266f437d3630abb3700f3b868301c8fe017c49a in /opt/java/openjdk 
# Fri, 13 Oct 2023 00:58:46 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 13 Oct 2023 01:01:17 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Fri, 13 Oct 2023 01:01:17 GMT
WORKDIR /tmp
# Fri, 13 Oct 2023 01:01:33 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Fri, 13 Oct 2023 01:01:34 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Fri, 13 Oct 2023 01:01:34 GMT
CMD ["clj"]
```

-	Layers:
	-	`sha256:e720f94321d63ecb6efa873b294dce7eaa1c3a5ddcd5bf7daddf375b955669a4`  
		Last Modified: Wed, 11 Oct 2023 18:28:04 GMT  
		Size: 49.6 MB (49612578 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f775b99f3d26acccb021520058d84b450dc9bf368a53027ca58bcdb52b2eabe4`  
		Last Modified: Fri, 13 Oct 2023 01:13:16 GMT  
		Size: 102.7 MB (102690442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:feacf0232cd8e78c5c8c59b1736666004e3249aeb466156df0f41705c0e24ba4`  
		Last Modified: Fri, 13 Oct 2023 01:14:17 GMT  
		Size: 83.1 MB (83118068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:023b5a95cb5b5d8392ff4b93b73b59c68e7d6e7bb36cecf6e57226caf79b9f82`  
		Last Modified: Fri, 13 Oct 2023 01:14:10 GMT  
		Size: 617.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
