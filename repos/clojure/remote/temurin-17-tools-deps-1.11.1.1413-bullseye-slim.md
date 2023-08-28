## `clojure:temurin-17-tools-deps-1.11.1.1413-bullseye-slim`

```console
$ docker pull clojure@sha256:b5df5dd2b8b465fc9af2de6082a6ec212d800f6bbd440a928d06cf2f9bcaa07b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm64 variant v8

### `clojure:temurin-17-tools-deps-1.11.1.1413-bullseye-slim` - linux; arm64 variant v8

```console
$ docker pull clojure@sha256:056794ddc1b751aca582f9b4f134bedaf81cfdb8917ccc9bcda40354dafdf00c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **235.2 MB (235213377 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c9f99328989b8e9480ca3692767540b77bbd8a539f49931ac2526b88ec25ccd`
-	Entrypoint: `["entrypoint"]`
-	Default Command: `["-M","--repl"]`

```dockerfile
# Tue, 15 Aug 2023 23:40:11 GMT
ADD file:ea912fd82699af55c10b8136b5dc4b5ce9d08b8a01f9c06f6783d94dc430335a in / 
# Tue, 15 Aug 2023 23:40:11 GMT
CMD ["bash"]
# Wed, 16 Aug 2023 01:46:48 GMT
ENV JAVA_HOME=/opt/java/openjdk
# Wed, 16 Aug 2023 17:25:53 GMT
COPY dir:5a6bdf68753afdd79dcc6e0d47fad53f85321d9f35fef7ea9a683b5f91d77eec in /opt/java/openjdk 
# Wed, 16 Aug 2023 17:25:56 GMT
ENV PATH=/opt/java/openjdk/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 28 Aug 2023 19:44:02 GMT
ENV CLOJURE_VERSION=1.11.1.1413
# Mon, 28 Aug 2023 19:44:02 GMT
WORKDIR /tmp
# Mon, 28 Aug 2023 19:44:16 GMT
RUN apt-get update && apt-get install -y curl make git rlwrap wget && rm -rf /var/lib/apt/lists/* && wget https://download.clojure.org/install/linux-install-$CLOJURE_VERSION.sh && sha256sum linux-install-$CLOJURE_VERSION.sh && echo "ad9aa1e99c59a4f7eb66450914fbec543337d9fada60dd9d34eec7fe18ae4965 *linux-install-$CLOJURE_VERSION.sh" | sha256sum -c - && chmod +x linux-install-$CLOJURE_VERSION.sh && ./linux-install-$CLOJURE_VERSION.sh && rm linux-install-$CLOJURE_VERSION.sh && clojure -e "(clojure-version)" && apt-get purge -y --auto-remove curl wget
# Mon, 28 Aug 2023 19:44:17 GMT
COPY file:b0aef3ea203de7b5c2ea645debf58c8231445a2e3070b72749b54614f4a89b82 in /usr/local/bin/rlwrap 
# Mon, 28 Aug 2023 19:44:17 GMT
COPY file:137b40904568e30898cd031ef34f77e7f132846ba4eec91d04ae4b93dddfbb8d in /usr/local/bin/entrypoint 
# Mon, 28 Aug 2023 19:44:17 GMT
ENTRYPOINT ["entrypoint"]
# Mon, 28 Aug 2023 19:44:17 GMT
CMD ["-M" "--repl"]
```

-	Layers:
	-	`sha256:41f92d5a73b9bee296c7b4a3817b28098b22fb60112608b42bb03570ca296115`  
		Last Modified: Tue, 15 Aug 2023 23:43:58 GMT  
		Size: 30.1 MB (30062816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed4e1713a1018eae13a831df1ed9b8fd5e8788a4ef59b3f122c903b9e1c2857b`  
		Last Modified: Wed, 16 Aug 2023 17:34:20 GMT  
		Size: 143.5 MB (143538106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8a9e7a31ddef16c881d57fa829519342195a240ae01b25acafcc71bf366ea27`  
		Last Modified: Mon, 28 Aug 2023 19:50:11 GMT  
		Size: 61.6 MB (61611441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:113b8168308837e77be89c16781e922145dc25f17842eb6b237ea002f9660e7e`  
		Last Modified: Mon, 28 Aug 2023 19:50:05 GMT  
		Size: 616.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:626e07aa43f0413eb494468591cba14f7666e2df5c6d5c8ab4492c90340210a8`  
		Last Modified: Mon, 28 Aug 2023 19:50:05 GMT  
		Size: 398.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
