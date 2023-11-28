## `docker:cli`

```console
$ docker pull docker@sha256:ce11346bbd77bffc5e3ba31311599866640ef48c968272244574a92d7e1dc755
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 7
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `docker:cli` - linux; amd64

```console
$ docker pull docker@sha256:4e8c8cce9bdd64300b69286f02c0884327f6ddf13bf5eb5f3a05c1ac3de74e7d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56865737 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ff5d4e91c9838821f620ccd35d8e9aa5259ba322721d907dea8da199e57311d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Thu, 23 Nov 2023 12:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Nov 2023 12:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Nov 2023 12:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c7f669f95cf000dcf527c3eb1647199df200d2fd38e0746f4df4b261bf660e8`  
		Last Modified: Tue, 28 Nov 2023 19:12:06 GMT  
		Size: 2.0 MB (2014312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3def34df6a7f8d94bc16e74bbce4ef30adff863fca4813bee67fe861b3efd7f9`  
		Last Modified: Tue, 28 Nov 2023 19:12:06 GMT  
		Size: 16.4 MB (16400387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:83813b2e4d53f3a949885bb792f627b50f780b398febf7ec513221cd392a13e1`  
		Last Modified: Tue, 28 Nov 2023 19:12:07 GMT  
		Size: 17.2 MB (17195305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44e1cb8c6d1314476c630884568292e90361681ceb17e28f39eb467efc7c212a`  
		Last Modified: Tue, 28 Nov 2023 19:12:06 GMT  
		Size: 17.9 MB (17852056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d42b36eb6fd91fed88ba7205433a8d2a362b60012ace8fde33846d98f635315`  
		Last Modified: Tue, 28 Nov 2023 19:12:07 GMT  
		Size: 544.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca6404f088e2e907e02c438adfb67b7ab471ff1efa6599d57aee311ba15288fe`  
		Last Modified: Tue, 28 Nov 2023 19:12:07 GMT  
		Size: 1.0 KB (1020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df1967c9b940323180067fd6f65624cb7fab180ca14a1e0207d20cd8b4118c62`  
		Last Modified: Tue, 28 Nov 2023 19:12:08 GMT  
		Size: 114.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:fdd676fed0fc257703188b6b4ddcaea279a877b98aadddd2e505cd87816eee6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.9 KB (373876 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9e1916e9e6945a9ebd0367dc25d201c6f845662bc1604142734f65788eb9635`

```dockerfile
```

-	Layers:
	-	`sha256:349833d322e82a12ff75f2768acd9201a58098fd661e0ed2316c9bd3dcbd6229`  
		Last Modified: Tue, 28 Nov 2023 19:12:06 GMT  
		Size: 338.1 KB (338093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76ccde26175409fe78f1a241b422405b425a273c9a79e67d4654b94f2d411d03`  
		Last Modified: Tue, 28 Nov 2023 19:12:06 GMT  
		Size: 35.8 KB (35783 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm variant v6

```console
$ docker pull docker@sha256:778c2f6af6c0ac6e0cb1dd85ac3078c1bab2c9ba8ca8b6fb136ce18a1c7b3a9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53335716 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35da819df0c2c149b4a4a6fd609cc5b3b45a0ab806849dcea1656461ab80386e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:49:16 GMT
ADD file:2222b03381ff0fce22edd647f5c60529ec6a72202f8d3cb1d6e4648ebcd19a1e in / 
# Thu, 28 Sep 2023 20:49:16 GMT
CMD ["/bin/sh"]
# Thu, 23 Nov 2023 12:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Nov 2023 12:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Nov 2023 12:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:91cb83b91ee16f1ee0d588fccef56ab5dbb5689a64e5373caf33d7e4fe52ceb4`  
		Last Modified: Thu, 28 Sep 2023 20:51:25 GMT  
		Size: 3.1 MB (3145291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749ab9fb78d5310f50a86ca9fc51b51ccfc7c6fb8285aea647b6faa49409ecf2`  
		Last Modified: Tue, 14 Nov 2023 02:37:28 GMT  
		Size: 2.1 MB (2088618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b83996d78fa3bf1f1f666c6867d86d9ec6df58b6779c0b69c27930534055f0a`  
		Last Modified: Fri, 17 Nov 2023 19:21:13 GMT  
		Size: 15.1 MB (15132561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5954e168cb50fb104f1abe5e1ab8f36cb2d56137292f600f518364011e3df1b`  
		Last Modified: Fri, 17 Nov 2023 19:21:13 GMT  
		Size: 16.1 MB (16099973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fba80cd41230572d2e61c882e276e23e4e653695ea3d64e4f43c9ca19cecc6f`  
		Last Modified: Tue, 28 Nov 2023 19:07:01 GMT  
		Size: 16.9 MB (16867555 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17dc9b74c0fced27dbfbd84aeb920cb8fa629e8a8c12bf7b884bd48207accd91`  
		Last Modified: Tue, 28 Nov 2023 19:06:58 GMT  
		Size: 546.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84c801a3f93d9b38c251297d9f6a759542957fac70fc8547e2cd0ef398429bbb`  
		Last Modified: Tue, 28 Nov 2023 19:06:58 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99646cba94d1826df0410849aba5ee8e002ee667282977621f3d3740739c4135`  
		Last Modified: Tue, 28 Nov 2023 19:06:58 GMT  
		Size: 116.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `docker:cli` - linux; arm variant v7

```console
$ docker pull docker@sha256:5b2cedf867a9d834110ea619099c97ac072d79085a2d23202fce8a3d99c9100e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52840998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e62deee1a4ca54ce5ce74817312f009e2b5f1a5ce4a3f06d82d1c13a0d02134`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:59:24 GMT
ADD file:61f54a318ad79861c6177783bb4c604412b5d952f45a9aa12ff97f4dccba7f73 in / 
# Thu, 28 Sep 2023 20:59:24 GMT
CMD ["/bin/sh"]
# Thu, 23 Nov 2023 12:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Nov 2023 12:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Nov 2023 12:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:622a0779436eb93ceea635e910268f867c2eba47d4f62f0bd45f0bd165af3572`  
		Last Modified: Thu, 28 Sep 2023 21:00:50 GMT  
		Size: 2.9 MB (2899905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b7fbc844f0c4a3436052544093f56c4d5061b5302239d5e8f50afb7d503a29c`  
		Last Modified: Tue, 03 Oct 2023 00:57:56 GMT  
		Size: 1.9 MB (1875250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734588fa8ce31adf2dc94210cd8342f969f8b0e95bce00cca1ee11f8caeb8f81`  
		Last Modified: Fri, 27 Oct 2023 16:51:50 GMT  
		Size: 15.1 MB (15127058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be094786016ada203d28b6bd689aaa0c804ba33e6aae16aeace1a803c87d448c`  
		Last Modified: Fri, 17 Nov 2023 19:26:56 GMT  
		Size: 16.1 MB (16084089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81853b0eeb244f06eeb7c8ef4e1f90c467b0e2847e88e50017d1aee0626bbc74`  
		Last Modified: Tue, 28 Nov 2023 19:12:53 GMT  
		Size: 16.9 MB (16852976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68896c6f3710a285bab553e9bd5aa250909b5eea6aa2f4e99a2d6164e1d52f4e`  
		Last Modified: Tue, 28 Nov 2023 19:12:52 GMT  
		Size: 547.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ae0c590f7b1ad7c063b9bd5ec53e1885a39c7265a2a0cffa6e8f30a6533b35a`  
		Last Modified: Tue, 28 Nov 2023 19:12:52 GMT  
		Size: 1.0 KB (1025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fafc2cd3a5b8b5a0dc09e4eaed853b8eb3a087bb8fb6cabfe2a374c2ae5a170e`  
		Last Modified: Tue, 28 Nov 2023 19:12:52 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:ff3c9e4192a672e821b2561f82f2b5dda31c0c7f21d045cd3d601795c867849c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.9 KB (373897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:732ee5f53b3c9efc399f83d166f8b5d7b1bc46becaf6ce019e0353ba5e462f43`

```dockerfile
```

-	Layers:
	-	`sha256:64e8f3f76b39f425cdb49e553bd8b4c51c5554e4ef49a889e8ad7b09c47d53b5`  
		Last Modified: Tue, 28 Nov 2023 19:12:52 GMT  
		Size: 338.1 KB (338137 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:93ba268ca3325fd25b53138d1d5185f823b32765cca7d21f23d863755fbc87cd`  
		Last Modified: Tue, 28 Nov 2023 19:12:51 GMT  
		Size: 35.8 KB (35760 bytes)  
		MIME: application/vnd.in-toto+json

### `docker:cli` - linux; arm64 variant v8

```console
$ docker pull docker@sha256:64d35b4b9380e951e28256600490c5a9ad2893f3b84f214d7909594e5e5f3eb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52750556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c5850ea108bccbc647db89d0ada2ae928158c70e4e315bbe95cf4b59a4ffd5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["sh"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Thu, 23 Nov 2023 12:04:14 GMT
RUN apk add --no-cache 		ca-certificates 		openssh-client # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
RUN [ -e /etc/nsswitch.conf ] && grep '^hosts: files dns' /etc/nsswitch.conf # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_VERSION=24.0.7
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://download.docker.com/linux/static/stable/x86_64/docker-24.0.7.tgz'; 			;; 		'armhf') 			url='https://download.docker.com/linux/static/stable/armel/docker-24.0.7.tgz'; 			;; 		'armv7') 			url='https://download.docker.com/linux/static/stable/armhf/docker-24.0.7.tgz'; 			;; 		'aarch64') 			url='https://download.docker.com/linux/static/stable/aarch64/docker-24.0.7.tgz'; 			;; 		*) echo >&2 "error: unsupported 'docker.tgz' architecture ($apkArch)"; exit 1 ;; 	esac; 		wget -O 'docker.tgz' "$url"; 		tar --extract 		--file docker.tgz 		--strip-components 1 		--directory /usr/local/bin/ 		--no-same-owner 		'docker/docker' 	; 	rm docker.tgz; 		docker --version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_BUILDX_VERSION=0.12.0
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-amd64'; 			sha256='7c393b92c148a0ce26c76a2abc99960be1d1097f0471978d41dc51d0c1a4471e'; 			;; 		'armhf') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v6'; 			sha256='62d9162f526c3bb7f67768a5b0d81a8b3ad0371406dfc1f0775e4f62dfca7fe1'; 			;; 		'armv7') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm-v7'; 			sha256='d941d6a5b072de775222d31d9f8467b4c1b1f56e3b08d1b78f828a9244c16464'; 			;; 		'aarch64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-arm64'; 			sha256='781caebb36551b035cb9dcfaf91088543d09c73c4a2549341e6417d86b8bbb50'; 			;; 		'ppc64le') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-ppc64le'; 			sha256='ab5bda4532528d6b0801c877999fce9def10c6a37624673fd13c668fdcde16b7'; 			;; 		'riscv64') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-riscv64'; 			sha256='a2b846919c44128c6db9165ad24545e7e10035b6f0ad01559fcfbb2a13017127'; 			;; 		's390x') 			url='https://github.com/docker/buildx/releases/download/v0.12.0/buildx-v0.12.0.linux-s390x'; 			sha256='81c2ada65624e2ac6bb4123f3a3bb933d04cfb08aa45fc55dd201ba523d96d30'; 			;; 		*) echo >&2 "warning: unsupported 'docker-buildx' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-buildx' "$url"; 	echo "$sha256 *"'docker-buildx' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-buildx'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-buildx' "$plugin"; 	chmod +x "$plugin"; 		docker buildx version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_COMPOSE_VERSION=2.23.3
# Thu, 23 Nov 2023 12:04:14 GMT
RUN set -eux; 		apkArch="$(apk --print-arch)"; 	case "$apkArch" in 		'x86_64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-x86_64'; 			sha256='a836e807951db448f991f303cddcc9a4ec69f4a49d58bc7d536cb91c77c04c33'; 			;; 		'armhf') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv6'; 			sha256='b712693945360155842b578beace00effa723b604bfe1ccd6421645523e15d86'; 			;; 		'armv7') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-armv7'; 			sha256='4068bcbe1dd90034c8fe8d2c65b600ba793fc19bdb65db3c2dbf80b8a078de6c'; 			;; 		'aarch64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-aarch64'; 			sha256='71f38f0923b8a9b80ad02c823ec3207d94677547aa5c618ca41b81d29fe6b9d9'; 			;; 		'ppc64le') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-ppc64le'; 			sha256='6110b0d30baee103c98ca5503bea24acb9d52bd333a67d3bf3c57d383c585c62'; 			;; 		'riscv64') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-riscv64'; 			sha256='3ac26e5f272deb1364c9b8760af44c4dbd87d6faa42fc53bfec95885cfa8ae77'; 			;; 		's390x') 			url='https://github.com/docker/compose/releases/download/v2.23.3/docker-compose-linux-s390x'; 			sha256='2886dd4eddaea1eeb03537bdc596ec8947eb3ef7908c955284f8aad9170d3098'; 			;; 		*) echo >&2 "warning: unsupported 'docker-compose' architecture ($apkArch); skipping"; exit 0 ;; 	esac; 		wget -O 'docker-compose' "$url"; 	echo "$sha256 *"'docker-compose' | sha256sum -c -; 		plugin='/usr/local/libexec/docker/cli-plugins/docker-compose'; 	mkdir -p "$(dirname "$plugin")"; 	mv -vT 'docker-compose' "$plugin"; 	chmod +x "$plugin"; 		ln -sv "$plugin" /usr/local/bin/; 	docker-compose --version; 	docker compose version # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
COPY modprobe.sh /usr/local/bin/modprobe # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENV DOCKER_TLS_CERTDIR=/certs
# Thu, 23 Nov 2023 12:04:14 GMT
RUN mkdir /certs /certs/client && chmod 1777 /certs /certs/client # buildkit
# Thu, 23 Nov 2023 12:04:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Nov 2023 12:04:14 GMT
CMD ["sh"]
```

-	Layers:
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ecd494fa26a8aad94a0d22885340d6ee599258b2e67c6c22f91ed6221294435`  
		Last Modified: Fri, 29 Sep 2023 02:55:37 GMT  
		Size: 2.0 MB (2024548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99624a4fd86a4c6eda9530ba81d64e854494d3513e2b65182d975a3e73659f6a`  
		Last Modified: Fri, 27 Oct 2023 17:27:58 GMT  
		Size: 15.4 MB (15449538 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f8d0b91b302e88cfdcf7ce318907c82d76a6158db3fbc7d2a269b8cf13135b3`  
		Last Modified: Fri, 17 Nov 2023 19:28:11 GMT  
		Size: 15.6 MB (15640599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa124432a61f628946ce8ddcb274464518422bc8972d4ccad1afe27b4ca10cb9`  
		Last Modified: Tue, 28 Nov 2023 19:13:16 GMT  
		Size: 16.3 MB (16302322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3749b22a5c11e7412fefa557069b6edd72445a6405870eebf37b8a46395f58d9`  
		Last Modified: Tue, 28 Nov 2023 19:13:15 GMT  
		Size: 546.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a5e7969bcf4efbac87f2cb6121e87482f0bbd2442c5b9ffc7810ae2ac7a5bd2`  
		Last Modified: Tue, 28 Nov 2023 19:13:15 GMT  
		Size: 1.0 KB (1024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c071a01e9172836ccf3193bfb6301e15a716b9edd306c569018cfc40cc9490ed`  
		Last Modified: Tue, 28 Nov 2023 19:13:16 GMT  
		Size: 116.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `docker:cli` - unknown; unknown

```console
$ docker pull docker@sha256:be16ce286be8c44865f69b0fe3d2cbfa56ac7d93b4b76fbd4bb8cfbc6b97c533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.7 KB (373735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:435cb01884578bee33b6f592a3502e3cf473c8e8617fc489a845ece6e138a417`

```dockerfile
```

-	Layers:
	-	`sha256:f7e9ae14bb91ecde47d191b817354a9665b8131a8129bfb3a198c30d284309e8`  
		Last Modified: Tue, 28 Nov 2023 19:13:16 GMT  
		Size: 338.1 KB (338106 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3508fd883bddefb92d24e2434d667f4e466d15fa5033b1da14f7f5dbdee8167c`  
		Last Modified: Tue, 28 Nov 2023 19:13:15 GMT  
		Size: 35.6 KB (35629 bytes)  
		MIME: application/vnd.in-toto+json
