<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `api-firewall`

-	[`api-firewall:0.6.10`](#api-firewall0610)
-	[`api-firewall:0.6.11`](#api-firewall0611)
-	[`api-firewall:0.6.9`](#api-firewall069)
-	[`api-firewall:latest`](#api-firewalllatest)

## `api-firewall:0.6.10`

```console
$ docker pull api-firewall@sha256:bf1f35ccfbba73d57492b530212e17969ba0aba8e3e3a649f66a4fa601d8d61e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.6.10` - linux; amd64

```console
$ docker pull api-firewall@sha256:f10fbfa16f9d40b5429dec0f56f87bedb42c57d26435401b2f5d543766fb624a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8918675 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84253d385c9301049775151f4020fb707da26889ac8f098ef5d3e163fd8ab429`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 05:33:10 GMT
ENV APIFW_PATH=/opt/api-firewall
# Thu, 15 Jun 2023 05:33:11 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 05:33:11 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 15 Jun 2023 05:33:16 GMT
ENV APIFIREWALL_VERSION=v0.6.10
# Thu, 15 Jun 2023 05:33:18 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='774d29f694142984e11e31443398a973a882d19c491e06390de13f0ceabd04a4';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='6ef69fbafb2503c7b01681d39138ea1abe99da910912fde33b1c317a819d2804';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='a9ccd2757bb4703b70aeea44b8aa992ce0dc1025d36accf311a023d87b1b6f57';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 15 Jun 2023 05:33:18 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 15 Jun 2023 05:33:18 GMT
USER api-firewall
# Thu, 15 Jun 2023 05:33:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 05:33:18 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349e807e86b7ffdc03e6eecfe7a5ddb13e56e23f32c7764bfa125fff25429bca`  
		Last Modified: Thu, 15 Jun 2023 05:33:32 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e8c0996a6e69f1212f0dcb85656661c55e36acaac4c19a4073bf0d9de8accfe`  
		Last Modified: Thu, 15 Jun 2023 05:33:40 GMT  
		Size: 5.5 MB (5542403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f0a23b3cfecff84f227fd89baaadb04367bba41265df73ba7b27baf865c02df`  
		Last Modified: Thu, 15 Jun 2023 05:33:40 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.10` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:bc12d5e059c48f59f4ba3e481c05353cf85ffe7ad1be28011bd11df5f5af2719
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 MB (8430808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f24e325ed2b4da2da2694cfae1182bd3ed08691fe5366699856da30bded3d3dd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:55:45 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 14 Jun 2023 22:55:45 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 22:55:45 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 14 Jun 2023 22:55:49 GMT
ENV APIFIREWALL_VERSION=v0.6.10
# Wed, 14 Jun 2023 22:55:51 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='774d29f694142984e11e31443398a973a882d19c491e06390de13f0ceabd04a4';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='6ef69fbafb2503c7b01681d39138ea1abe99da910912fde33b1c317a819d2804';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='a9ccd2757bb4703b70aeea44b8aa992ce0dc1025d36accf311a023d87b1b6f57';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 14 Jun 2023 22:55:51 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 14 Jun 2023 22:55:51 GMT
USER api-firewall
# Wed, 14 Jun 2023 22:55:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 22:55:51 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7088b7a9c2f02d26362553ecf88235bb03c90adb851cbd1abaf221335f7caf`  
		Last Modified: Wed, 14 Jun 2023 22:56:05 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:776279e32c9294345566bc5d94b001947b7435d5e358b38b97bf37cbccc3f026`  
		Last Modified: Wed, 14 Jun 2023 22:56:14 GMT  
		Size: 5.2 MB (5168115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:918254eaaab2ae9f40dbc157cc36a9aff6e8e9fab822d64b32bff2c3c11cebb0`  
		Last Modified: Wed, 14 Jun 2023 22:56:13 GMT  
		Size: 352.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.10` - linux; 386

```console
$ docker pull api-firewall@sha256:39749ae6be7f15e0eda421ef3feb84ab45ed1529eba9b9d16d3839c0905facf4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.8 MB (8817516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ddb35bf5f070a076a99e9346576b01d4e6f3f4a564d557d95bd41aca55efb9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:26 GMT
ADD file:39180f040ebe17a01f8b9502d7b463edade8158d87fa99e47ac0b1f369e11a65 in / 
# Wed, 14 Jun 2023 22:33:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 02:08:11 GMT
ENV APIFW_PATH=/opt/api-firewall
# Thu, 15 Jun 2023 02:08:11 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 02:08:12 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 15 Jun 2023 02:08:16 GMT
ENV APIFIREWALL_VERSION=v0.6.10
# Thu, 15 Jun 2023 02:08:18 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='774d29f694142984e11e31443398a973a882d19c491e06390de13f0ceabd04a4';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='6ef69fbafb2503c7b01681d39138ea1abe99da910912fde33b1c317a819d2804';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='a9ccd2757bb4703b70aeea44b8aa992ce0dc1025d36accf311a023d87b1b6f57';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 15 Jun 2023 02:08:19 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 15 Jun 2023 02:08:19 GMT
USER api-firewall
# Thu, 15 Jun 2023 02:08:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 02:08:19 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:187bd96dd637d3adfc7a9b61a1e7465181bbfe90dbf7a2830dfba97e4e3243a4`  
		Last Modified: Wed, 14 Jun 2023 22:34:01 GMT  
		Size: 3.4 MB (3412675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901786a36f196525d5402759b7a330478a2bae4cf05fb5a41affa6a4d1f14e7f`  
		Last Modified: Thu, 15 Jun 2023 02:08:34 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6086348e46831d12317116d9d4acc8842c02810e75eb723ce5ecdc5edba8f89`  
		Last Modified: Thu, 15 Jun 2023 02:08:45 GMT  
		Size: 5.4 MB (5403286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2d831bee9bb32a0a3066001dc99785df8ffebeacade0c9ccdef8ac456fb52e9`  
		Last Modified: Thu, 15 Jun 2023 02:08:43 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:0.6.11`

```console
$ docker pull api-firewall@sha256:5d995644d43c7deae9213f7161c2926fbee2cf27160998355d8b4101f52cede1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.6.11` - linux; amd64

```console
$ docker pull api-firewall@sha256:345ae3e8dcd5307c6afde0d77bfa3bb5c7e78d88665a9081ca326bf7aa6d44ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8983374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde1cf559be6badf237436d453d610a668e5dda7462b15f06ddaac749eb14b49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 05:33:10 GMT
ENV APIFW_PATH=/opt/api-firewall
# Thu, 15 Jun 2023 05:33:11 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 05:33:11 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 15 Jun 2023 05:33:11 GMT
ENV APIFIREWALL_VERSION=v0.6.11
# Thu, 15 Jun 2023 05:33:13 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c76cdb6c6185038ea619e364acc71066831de85aefe7e32f8fdbdcc110125cc1';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='786b645dd11cb34ce2ee512b1f75b8929095e25de0027bff5817dedc895eb883';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='351af5ba7af8a010c941416f863bfd52d3e4f04f6ebba77cdf388c37b39e7c75';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 15 Jun 2023 05:33:13 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 15 Jun 2023 05:33:13 GMT
USER api-firewall
# Thu, 15 Jun 2023 05:33:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 05:33:13 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349e807e86b7ffdc03e6eecfe7a5ddb13e56e23f32c7764bfa125fff25429bca`  
		Last Modified: Thu, 15 Jun 2023 05:33:32 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965c3a2ae45828a347ba83005340cc4aa897d4d85502cacb485df71100ead3dd`  
		Last Modified: Thu, 15 Jun 2023 05:33:33 GMT  
		Size: 5.6 MB (5607101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a5d401777a938dc44851454327af6078b000614e01f2bd9d6f2dccee2a3e1c`  
		Last Modified: Thu, 15 Jun 2023 05:33:32 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.11` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:3233013d824d2b14368c4799de0622db298d100232771b6eb2279ae2c24973c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8491181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf7552534c17bfb79c344e9e84d2d6e7ed4eab5df285f6f4181068f0c8f93b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:55:45 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 14 Jun 2023 22:55:45 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 22:55:45 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 14 Jun 2023 22:55:45 GMT
ENV APIFIREWALL_VERSION=v0.6.11
# Wed, 14 Jun 2023 22:55:47 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c76cdb6c6185038ea619e364acc71066831de85aefe7e32f8fdbdcc110125cc1';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='786b645dd11cb34ce2ee512b1f75b8929095e25de0027bff5817dedc895eb883';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='351af5ba7af8a010c941416f863bfd52d3e4f04f6ebba77cdf388c37b39e7c75';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 14 Jun 2023 22:55:47 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 14 Jun 2023 22:55:47 GMT
USER api-firewall
# Wed, 14 Jun 2023 22:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 22:55:48 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7088b7a9c2f02d26362553ecf88235bb03c90adb851cbd1abaf221335f7caf`  
		Last Modified: Wed, 14 Jun 2023 22:56:05 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74abfa69820d287e8e6a6ed724ac3c6b65f35741c610af350bad754533d3b50c`  
		Last Modified: Wed, 14 Jun 2023 22:56:06 GMT  
		Size: 5.2 MB (5228486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02b3eb7e151fac5d7c1fd8e70ae1a10b09476b1083751b9160714f25b3b8a94`  
		Last Modified: Wed, 14 Jun 2023 22:56:05 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.11` - linux; 386

```console
$ docker pull api-firewall@sha256:3ae39e4b491f7f2a06e7d61114c156033520986e1ecedbd546d6c165637bf133
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8880878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d97f70e37546d85e2f401f6cd5b0b8badf0959acb34f23b77c53f858eeccc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:26 GMT
ADD file:39180f040ebe17a01f8b9502d7b463edade8158d87fa99e47ac0b1f369e11a65 in / 
# Wed, 14 Jun 2023 22:33:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 02:08:11 GMT
ENV APIFW_PATH=/opt/api-firewall
# Thu, 15 Jun 2023 02:08:11 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 02:08:12 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 15 Jun 2023 02:08:12 GMT
ENV APIFIREWALL_VERSION=v0.6.11
# Thu, 15 Jun 2023 02:08:14 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c76cdb6c6185038ea619e364acc71066831de85aefe7e32f8fdbdcc110125cc1';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='786b645dd11cb34ce2ee512b1f75b8929095e25de0027bff5817dedc895eb883';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='351af5ba7af8a010c941416f863bfd52d3e4f04f6ebba77cdf388c37b39e7c75';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 15 Jun 2023 02:08:15 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 15 Jun 2023 02:08:15 GMT
USER api-firewall
# Thu, 15 Jun 2023 02:08:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 02:08:15 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:187bd96dd637d3adfc7a9b61a1e7465181bbfe90dbf7a2830dfba97e4e3243a4`  
		Last Modified: Wed, 14 Jun 2023 22:34:01 GMT  
		Size: 3.4 MB (3412675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901786a36f196525d5402759b7a330478a2bae4cf05fb5a41affa6a4d1f14e7f`  
		Last Modified: Thu, 15 Jun 2023 02:08:34 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034d481f2915e997685ad96e87fed18e5d47055bb9dcec676c10f1867b5e6c00`  
		Last Modified: Thu, 15 Jun 2023 02:08:35 GMT  
		Size: 5.5 MB (5466644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687518b0bce7c58ea178369f74d4600cae1beb1a74f00f8f1aebdb7cbae0ce4f`  
		Last Modified: Thu, 15 Jun 2023 02:08:34 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:0.6.9`

```console
$ docker pull api-firewall@sha256:7f16b85cd2d367b82a5388374ff2091dd0509c27b4b51ccaa719ad2b74d859ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:0.6.9` - linux; amd64

```console
$ docker pull api-firewall@sha256:2f636561cfb1341df9618c747e8bae2370a167a26f391cdab0d027ac2a147d69
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 MB (7997173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a3bdc3f7f9acab255b6193e1bcd01c13190992884dcd15a3e4c863d733f2409`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:09 GMT
ADD file:4af69326e088b3c0f82320e9cd97b60c28bf019b984787c6f1c22489e6221f29 in / 
# Wed, 14 Jun 2023 20:42:09 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 05:33:20 GMT
ENV APIFW_PATH=/opt/api-firewall
# Thu, 15 Jun 2023 05:33:21 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 05:33:21 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 15 Jun 2023 05:33:21 GMT
ENV APIFIREWALL_VERSION=v0.6.9
# Thu, 15 Jun 2023 05:33:23 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='12f0b039e84f71298ebc17777910cdd7618e76f65f3356d2e890c3b45f01ef19';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='4f31329e9f2391460450e83096b0b17afa08649e17870f8667f1187aacc5ae00';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='acdce9e1e3d5ecc46be56d3a6b5a70a84de44c53d342a02b8e5f848624ae4b16';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 15 Jun 2023 05:33:23 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 15 Jun 2023 05:33:23 GMT
USER api-firewall
# Thu, 15 Jun 2023 05:33:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 05:33:23 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:c1d6d1b2d5a367259e6e51a7f4d1ccd66a28cc9940d6599d8a8ea9544dd4b4a8`  
		Last Modified: Wed, 14 Jun 2023 20:42:45 GMT  
		Size: 2.8 MB (2807669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:238f441af54c0abd61665dbfafca61a055da5f598d96f816a021a46cddb329cd`  
		Last Modified: Thu, 15 Jun 2023 05:33:46 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fa5b554ff2f58ca575d33c8c1b98ea1974df1914ee474cef05463b4db6b31fe`  
		Last Modified: Thu, 15 Jun 2023 05:33:47 GMT  
		Size: 5.2 MB (5187949 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28298ed652721d7439c10242a79fd78397d5a6759c42713265a92302ebd6fe9`  
		Last Modified: Thu, 15 Jun 2023 05:33:46 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.9` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:884261a0409903fc86a8795720265c1b37f6386e561f8d99cc815e103ec5f1cc
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.5 MB (7490541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5676e08f6bc8ead8cecec17653000257cb54c7834255ece0ba179886ccb1d264`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:07 GMT
ADD file:e80eabe59d1f87ef41634428d9f8fdeb633c2128ac97564f96f5495ef6bf2c72 in / 
# Wed, 14 Jun 2023 20:49:07 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:55:53 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 14 Jun 2023 22:55:53 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 22:55:54 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 14 Jun 2023 22:55:54 GMT
ENV APIFIREWALL_VERSION=v0.6.9
# Wed, 14 Jun 2023 22:55:57 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='12f0b039e84f71298ebc17777910cdd7618e76f65f3356d2e890c3b45f01ef19';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='4f31329e9f2391460450e83096b0b17afa08649e17870f8667f1187aacc5ae00';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='acdce9e1e3d5ecc46be56d3a6b5a70a84de44c53d342a02b8e5f848624ae4b16';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 14 Jun 2023 22:55:57 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 14 Jun 2023 22:55:57 GMT
USER api-firewall
# Wed, 14 Jun 2023 22:55:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 22:55:57 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:a880266d3b77f75696023df2da1ef66c3c565e0f70596242395c9e68de955c7c`  
		Last Modified: Wed, 14 Jun 2023 20:49:43 GMT  
		Size: 2.7 MB (2707906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2cce8b99e5b37ed8f7bf314f9778a1ec62e2dde13bf53991a11ca1a155abad4`  
		Last Modified: Wed, 14 Jun 2023 22:56:20 GMT  
		Size: 1.2 KB (1201 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fdffd72a6322a073b6b4b83fa8f829e39e2c60165b970cc55bfcb24094c2508`  
		Last Modified: Wed, 14 Jun 2023 22:56:20 GMT  
		Size: 4.8 MB (4781081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1699e475ab8311b9b829f625d8f22be9072a863606454aa2a8ff47509e51b71`  
		Last Modified: Wed, 14 Jun 2023 22:56:20 GMT  
		Size: 353.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:0.6.9` - linux; 386

```console
$ docker pull api-firewall@sha256:a5e20995d57df4cc5ae6124e91c175f0946b8d51998d448e30b396b62ee6d8e5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 MB (7856148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c5bd40976593ff547c49998e7bcb9b8bcd3f3aea896285059dbccd8aa643cb43`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:30 GMT
ADD file:9b22a3b9a2009266eccfbbf15fbc348f6c854a6c496df29e5c4f0a832b796c67 in / 
# Wed, 14 Jun 2023 22:33:30 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 02:08:20 GMT
ENV APIFW_PATH=/opt/api-firewall
# Thu, 15 Jun 2023 02:08:21 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 02:08:21 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 15 Jun 2023 02:08:21 GMT
ENV APIFIREWALL_VERSION=v0.6.9
# Thu, 15 Jun 2023 02:08:23 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='12f0b039e84f71298ebc17777910cdd7618e76f65f3356d2e890c3b45f01ef19';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='4f31329e9f2391460450e83096b0b17afa08649e17870f8667f1187aacc5ae00';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='acdce9e1e3d5ecc46be56d3a6b5a70a84de44c53d342a02b8e5f848624ae4b16';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 15 Jun 2023 02:08:24 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 15 Jun 2023 02:08:24 GMT
USER api-firewall
# Thu, 15 Jun 2023 02:08:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 02:08:24 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:ca79a18e143c0859a7d07fda202e645a6564d97bbda6a486c576b234535bda07`  
		Last Modified: Wed, 14 Jun 2023 22:34:09 GMT  
		Size: 2.8 MB (2810568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3a1bdec48bc32f28510ac29b21b570b2230a5d50a1d1cc72c608f5ce5f7bc7`  
		Last Modified: Thu, 15 Jun 2023 02:08:50 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a6e8786d9d1d4b79fd2e65145f521baca8b11a94f4d58c032008bebf77ee0e6`  
		Last Modified: Thu, 15 Jun 2023 02:08:51 GMT  
		Size: 5.0 MB (5044020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc0384a0f6f61fba336f905b980934d61025b6b6a4cef385344dce9d92b28f5b`  
		Last Modified: Thu, 15 Jun 2023 02:08:50 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `api-firewall:latest`

```console
$ docker pull api-firewall@sha256:5d995644d43c7deae9213f7161c2926fbee2cf27160998355d8b4101f52cede1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `api-firewall:latest` - linux; amd64

```console
$ docker pull api-firewall@sha256:345ae3e8dcd5307c6afde0d77bfa3bb5c7e78d88665a9081ca326bf7aa6d44ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 MB (8983374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fde1cf559be6badf237436d453d610a668e5dda7462b15f06ddaac749eb14b49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 14 Jun 2023 20:42:04 GMT
ADD file:828b07e74c184e7f251ed992ff195cdc50fdca345f13ff484e258851d928d950 in / 
# Wed, 14 Jun 2023 20:42:04 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 05:33:10 GMT
ENV APIFW_PATH=/opt/api-firewall
# Thu, 15 Jun 2023 05:33:11 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 05:33:11 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 15 Jun 2023 05:33:11 GMT
ENV APIFIREWALL_VERSION=v0.6.11
# Thu, 15 Jun 2023 05:33:13 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c76cdb6c6185038ea619e364acc71066831de85aefe7e32f8fdbdcc110125cc1';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='786b645dd11cb34ce2ee512b1f75b8929095e25de0027bff5817dedc895eb883';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='351af5ba7af8a010c941416f863bfd52d3e4f04f6ebba77cdf388c37b39e7c75';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 15 Jun 2023 05:33:13 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 15 Jun 2023 05:33:13 GMT
USER api-firewall
# Thu, 15 Jun 2023 05:33:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 05:33:13 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:4db1b89c0bd13344176ddce2d093b9da2ae58336823ffed2009a7ea4b62d2a95`  
		Last Modified: Wed, 14 Jun 2023 20:42:37 GMT  
		Size: 3.4 MB (3374713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:349e807e86b7ffdc03e6eecfe7a5ddb13e56e23f32c7764bfa125fff25429bca`  
		Last Modified: Thu, 15 Jun 2023 05:33:32 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:965c3a2ae45828a347ba83005340cc4aa897d4d85502cacb485df71100ead3dd`  
		Last Modified: Thu, 15 Jun 2023 05:33:33 GMT  
		Size: 5.6 MB (5607101 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9a5d401777a938dc44851454327af6078b000614e01f2bd9d6f2dccee2a3e1c`  
		Last Modified: Thu, 15 Jun 2023 05:33:32 GMT  
		Size: 358.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; arm64 variant v8

```console
$ docker pull api-firewall@sha256:3233013d824d2b14368c4799de0622db298d100232771b6eb2279ae2c24973c8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.5 MB (8491181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf7552534c17bfb79c344e9e84d2d6e7ed4eab5df285f6f4181068f0c8f93b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:04 GMT
ADD file:6f6c919dc1fe5a56c2664a26a702d77203039cdd4c91e39da57063ea5d3f3094 in / 
# Wed, 14 Jun 2023 20:49:04 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:55:45 GMT
ENV APIFW_PATH=/opt/api-firewall
# Wed, 14 Jun 2023 22:55:45 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Jun 2023 22:55:45 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Wed, 14 Jun 2023 22:55:45 GMT
ENV APIFIREWALL_VERSION=v0.6.11
# Wed, 14 Jun 2023 22:55:47 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c76cdb6c6185038ea619e364acc71066831de85aefe7e32f8fdbdcc110125cc1';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='786b645dd11cb34ce2ee512b1f75b8929095e25de0027bff5817dedc895eb883';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='351af5ba7af8a010c941416f863bfd52d3e4f04f6ebba77cdf388c37b39e7c75';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Wed, 14 Jun 2023 22:55:47 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Wed, 14 Jun 2023 22:55:47 GMT
USER api-firewall
# Wed, 14 Jun 2023 22:55:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 22:55:48 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:edb6bdbacee93be93e930669f43e2e922c8594676aa342a70e2221361fd1914d`  
		Last Modified: Wed, 14 Jun 2023 20:49:35 GMT  
		Size: 3.3 MB (3261139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7088b7a9c2f02d26362553ecf88235bb03c90adb851cbd1abaf221335f7caf`  
		Last Modified: Wed, 14 Jun 2023 22:56:05 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74abfa69820d287e8e6a6ed724ac3c6b65f35741c610af350bad754533d3b50c`  
		Last Modified: Wed, 14 Jun 2023 22:56:06 GMT  
		Size: 5.2 MB (5228486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f02b3eb7e151fac5d7c1fd8e70ae1a10b09476b1083751b9160714f25b3b8a94`  
		Last Modified: Wed, 14 Jun 2023 22:56:05 GMT  
		Size: 354.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `api-firewall:latest` - linux; 386

```console
$ docker pull api-firewall@sha256:3ae39e4b491f7f2a06e7d61114c156033520986e1ecedbd546d6c165637bf133
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.9 MB (8880878 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85d97f70e37546d85e2f401f6cd5b0b8badf0959acb34f23b77c53f858eeccc9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["api-firewall"]`

```dockerfile
# Wed, 14 Jun 2023 22:33:26 GMT
ADD file:39180f040ebe17a01f8b9502d7b463edade8158d87fa99e47ac0b1f369e11a65 in / 
# Wed, 14 Jun 2023 22:33:26 GMT
CMD ["/bin/sh"]
# Thu, 15 Jun 2023 02:08:11 GMT
ENV APIFW_PATH=/opt/api-firewall
# Thu, 15 Jun 2023 02:08:11 GMT
ENV PATH=/opt/api-firewall:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Jun 2023 02:08:12 GMT
RUN set -eux;     adduser -u 1000 -H -h /opt -D -s /bin/sh api-firewall
# Thu, 15 Jun 2023 02:08:12 GMT
ENV APIFIREWALL_VERSION=v0.6.11
# Thu, 15 Jun 2023 02:08:14 GMT
RUN set -eux;         apk add --no-cache wget;         arch="$(apk --print-arch)";     case "$arch" in         'x86_64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-amd64-musl.tar.gz";             sha256='c76cdb6c6185038ea619e364acc71066831de85aefe7e32f8fdbdcc110125cc1';             ;;         'aarch64')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-arm64-musl.tar.gz";             sha256='786b645dd11cb34ce2ee512b1f75b8929095e25de0027bff5817dedc895eb883';             ;;         'x86')             url="https://github.com/wallarm/api-firewall/releases/download/${APIFIREWALL_VERSION}/api-firewall-386-musl.tar.gz";             sha256='351af5ba7af8a010c941416f863bfd52d3e4f04f6ebba77cdf388c37b39e7c75';             ;;         *)             echo >&2 "error: current architecture ($arch) does not have a corresponding API-Firewall binary release";             exit 1;             ;;     esac;         wget -O api-firewall.tar.gz "$url";     echo "$sha256 *api-firewall.tar.gz" | sha256sum -c;         mkdir -p "$APIFW_PATH";     tar -xzf api-firewall.tar.gz -C "$APIFW_PATH" --strip-components 1;     rm api-firewall.tar.gz;         chmod 755 $APIFW_PATH/api-firewall;         api-firewall -v
# Thu, 15 Jun 2023 02:08:15 GMT
COPY file:d278e8d8f9cc8e98b02127f87703b4379a8a938a57e107aac5dd34c716907f87 in /opt/api-firewall/ 
# Thu, 15 Jun 2023 02:08:15 GMT
USER api-firewall
# Thu, 15 Jun 2023 02:08:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Jun 2023 02:08:15 GMT
CMD ["api-firewall"]
```

-	Layers:
	-	`sha256:187bd96dd637d3adfc7a9b61a1e7465181bbfe90dbf7a2830dfba97e4e3243a4`  
		Last Modified: Wed, 14 Jun 2023 22:34:01 GMT  
		Size: 3.4 MB (3412675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901786a36f196525d5402759b7a330478a2bae4cf05fb5a41affa6a4d1f14e7f`  
		Last Modified: Thu, 15 Jun 2023 02:08:34 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:034d481f2915e997685ad96e87fed18e5d47055bb9dcec676c10f1867b5e6c00`  
		Last Modified: Thu, 15 Jun 2023 02:08:35 GMT  
		Size: 5.5 MB (5466644 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:687518b0bce7c58ea178369f74d4600cae1beb1a74f00f8f1aebdb7cbae0ce4f`  
		Last Modified: Thu, 15 Jun 2023 02:08:34 GMT  
		Size: 357.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
