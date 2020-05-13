<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kibana`

-	[`kibana:6.8.9`](#kibana689)
-	[`kibana:7.7.0`](#kibana770)

## `kibana:6.8.9`

```console
$ docker pull kibana@sha256:9dd93b95d53912f9c076dc18186b82f35b39b6a4aed4dec7e2bbd74a39b5fdb9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kibana:6.8.9` - linux; amd64

```console
$ docker pull kibana@sha256:a071ae8a5694c56a1adb265f880639d0180e8522f28fb19b4d99e4b335ad4ae2
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **325.5 MB (325502947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d3ea3cfe77cbe76807208b5b2d9be7b83c19ec9392e8affbd1e81cac537bee7`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 12 Nov 2019 00:20:33 GMT
ADD file:45a381049c52b5664e5e911dead277b25fadbae689c0bb35be3c42dff0f2dffe in / 
# Tue, 12 Nov 2019 00:20:33 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20191001
# Tue, 12 Nov 2019 00:20:33 GMT
CMD ["/bin/bash"]
# Mon, 04 May 2020 17:47:53 GMT
EXPOSE 5601
# Mon, 04 May 2020 17:49:06 GMT
RUN yum update -y && yum install -y fontconfig freetype && yum clean all
# Mon, 04 May 2020 17:49:55 GMT
COPY --chown=1000:0dir:514270c67778718ce2510ade289dd9d26fccbb6fe10322459aaa920bd8318646 in /usr/share/kibana 
# Mon, 04 May 2020 17:49:56 GMT
WORKDIR /usr/share/kibana
# Mon, 04 May 2020 17:49:58 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Mon, 04 May 2020 17:49:59 GMT
ENV ELASTIC_CONTAINER=true
# Mon, 04 May 2020 17:49:59 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 04 May 2020 17:49:59 GMT
COPY --chown=1000:0file:60b6181f28c99b362092ea6139b6d4112ddd0bef32d52563c33b26bdc2b51318 in /usr/share/kibana/config/kibana.yml 
# Mon, 04 May 2020 17:50:00 GMT
COPY --chown=1000:0file:7d472d1939e23e2f10e7c5fd1e9166eefd646214aa0d8a1c09d92af71c9cbd87 in /usr/local/bin/ 
# Mon, 04 May 2020 17:50:03 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Mon, 04 May 2020 17:50:04 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Mon, 04 May 2020 17:50:04 GMT
USER kibana
# Mon, 04 May 2020 17:50:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=6.8.9 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License license=Elastic License
# Mon, 04 May 2020 17:50:04 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:ab5ef0e5819490abe86106fd9f4381123e37a03e80e650be39f7938d30ecb530`  
		Last Modified: Tue, 12 Nov 2019 00:23:38 GMT  
		Size: 75.8 MB (75780712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23cbc13a0688f63d7384a46253a743d3ae6922eb32c43bf799b9b9b372e5fec7`  
		Last Modified: Wed, 13 May 2020 16:15:11 GMT  
		Size: 58.9 MB (58884751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca66cc76169f559359bbfa4cfb5824e5226ded731e7055633e22a52644d7041`  
		Last Modified: Wed, 13 May 2020 16:15:24 GMT  
		Size: 190.8 MB (190832733 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89ace943305d43fbe1bbffd528cbf8da1ecf77943dca11057c8c7470289711be`  
		Last Modified: Wed, 13 May 2020 16:14:54 GMT  
		Size: 132.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a7db9bd16dbeda670c81a7624a961e534beecd9de951ed2f0847468320745a`  
		Last Modified: Wed, 13 May 2020 16:14:54 GMT  
		Size: 393.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3432c6ed675ce3e93d2eb53e575270d78f8a5c8befaeb4a769ad5e539ee9e99f`  
		Last Modified: Wed, 13 May 2020 16:14:54 GMT  
		Size: 2.3 KB (2263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ad0d8b2180e6bd671011fafc6063827f20eedc0887c407c944fbca3d777a255`  
		Last Modified: Wed, 13 May 2020 16:14:54 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6f1d80adca03c97797f3f47b3b30fabfff42352926769981522f318fd164d16`  
		Last Modified: Wed, 13 May 2020 16:14:54 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `kibana:7.7.0`

```console
$ docker pull kibana@sha256:bdecba797e8fce118abd17f603a8cf466f28821b911d406efe15c47217fb2048
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64

### `kibana:7.7.0` - linux; amd64

```console
$ docker pull kibana@sha256:3ee868176cc4b6e4be1a0788d640b14769bee774713beb3540694d2f04e01822
```

-	Docker Version: 19.03.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **368.1 MB (368120791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eadc7b3d59dd47b1b56f280732f38d16a4b31947cbc758516adbe1df5472b407`
-	Entrypoint: `["\/usr\/local\/bin\/dumb-init","--"]`
-	Default Command: `["\/usr\/local\/bin\/kibana-docker"]`

```dockerfile
# Tue, 05 May 2020 21:20:06 GMT
ADD file:38e2d2a1a0cd8694bd5086f257fdf7504f0c2481bf4f746c9bd1c8d9f3f6430d in / 
# Tue, 05 May 2020 21:20:06 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20200504 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-05-04 00:00:00+01:00
# Tue, 05 May 2020 21:20:07 GMT
CMD ["/bin/bash"]
# Tue, 12 May 2020 03:31:31 GMT
EXPOSE 5601
# Tue, 12 May 2020 03:32:05 GMT
RUN yum update -y && yum install -y fontconfig freetype shadow-utils && yum clean all
# Tue, 12 May 2020 03:32:07 GMT
RUN curl -L -o /usr/local/bin/dumb-init https://github.com/Yelp/dumb-init/releases/download/v1.2.2/dumb-init_1.2.2_amd64
# Tue, 12 May 2020 03:32:11 GMT
RUN echo "37f2c1f0372a45554f1b89924fbb134fc24c3756efaedf11e07f599494e0eff9  /usr/local/bin/dumb-init" | sha256sum -c -
# Tue, 12 May 2020 03:32:14 GMT
RUN chmod +x /usr/local/bin/dumb-init
# Tue, 12 May 2020 03:34:11 GMT
COPY --chown=1000:0dir:75bec89022659829c7798602478486d988c2e569ace1b9544d0dc3669dd705f2 in /usr/share/kibana 
# Tue, 12 May 2020 03:34:13 GMT
WORKDIR /usr/share/kibana
# Tue, 12 May 2020 03:34:16 GMT
RUN ln -s /usr/share/kibana /opt/kibana
# Tue, 12 May 2020 03:34:17 GMT
ENV ELASTIC_CONTAINER=true
# Tue, 12 May 2020 03:34:18 GMT
ENV PATH=/usr/share/kibana/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 May 2020 03:34:18 GMT
COPY --chown=1000:0file:ea1f294356f14dfc1a50e3303613e69f187589962058569d5b3282460d7f28cb in /usr/share/kibana/config/kibana.yml 
# Tue, 12 May 2020 03:34:19 GMT
COPY --chown=1000:0file:8b9c2df36b5315bd3ada649a3e73f7f4011b1df2137c375bb98daad4b6b913c3 in /usr/local/bin/ 
# Tue, 12 May 2020 03:34:23 GMT
RUN chmod g+ws /usr/share/kibana && find /usr/share/kibana -gid 0 -and -not -perm /g+w -exec chmod g+w {} \;
# Tue, 12 May 2020 03:34:26 GMT
RUN find / -xdev -perm -4000 -exec chmod u-s {} +
# Tue, 12 May 2020 03:34:29 GMT
RUN groupadd --gid 1000 kibana && useradd --uid 1000 --gid 1000 --home-dir /usr/share/kibana --no-create-home kibana
# Tue, 12 May 2020 03:34:30 GMT
USER kibana
# Tue, 12 May 2020 03:34:30 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.vendor=Elastic org.label-schema.name=kibana org.label-schema.version=7.7.0 org.label-schema.url=https://www.elastic.co/products/kibana org.label-schema.vcs-url=https://github.com/elastic/kibana org.label-schema.license=Elastic License org.label-schema.usage=https://www.elastic.co/guide/en/kibana/index.html org.label-schema.build-date=2020-05-12T03:25:49.654Z license=Elastic License
# Tue, 12 May 2020 03:34:31 GMT
ENTRYPOINT ["/usr/local/bin/dumb-init" "--"]
# Tue, 12 May 2020 03:34:31 GMT
CMD ["/usr/local/bin/kibana-docker"]
```

-	Layers:
	-	`sha256:524b0c1e57f8ee5fee01a1decba2f301c324a6513ca3551021264e3aa7341ebc`  
		Last Modified: Tue, 05 May 2020 21:23:14 GMT  
		Size: 75.9 MB (75880141 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e61b1f90b23287342e6d7645b968c5d23f4aee9fcf8842354a1719be29954e26`  
		Last Modified: Wed, 13 May 2020 14:04:15 GMT  
		Size: 10.0 MB (9976636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a66f864b28eb4f7b405eb691b4ddc265a6b5fc2cacfb262f775c7c81016b78e`  
		Last Modified: Wed, 13 May 2020 14:04:14 GMT  
		Size: 31.7 KB (31682 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b75dfe443da24a535924e0a78b2f0500316920f61e725a8e645cbfc9fa164e4`  
		Last Modified: Wed, 13 May 2020 14:04:13 GMT  
		Size: 30.2 KB (30192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e30df36828bcd4061a02f9513af542105c72bba51ac2905098db9168f9e00de4`  
		Last Modified: Wed, 13 May 2020 14:06:40 GMT  
		Size: 282.0 MB (281996125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36ad9a2e1f435db3ced84f5ff1511643d7797dd3e4e7e070887d63e7cbc01ed7`  
		Last Modified: Wed, 13 May 2020 14:05:42 GMT  
		Size: 133.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f992ad0090ccb14838270667650dc6083c4ab500a28ff984418013e99d07567b`  
		Last Modified: Wed, 13 May 2020 14:05:42 GMT  
		Size: 387.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3ab12547dc45a54b5b3a55899b09f2337ab10cf4e0454c7b4110b71961ef2b3`  
		Last Modified: Wed, 13 May 2020 14:05:42 GMT  
		Size: 2.9 KB (2923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f02eb38205ba11e51f5a87398795d78ad2430da9de592fdcf8b62293c3f1930`  
		Last Modified: Wed, 13 May 2020 14:05:42 GMT  
		Size: 149.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479e48043a140bb13f54c54d0c9050979eab9a5c637dfde6da141d58c9298b57`  
		Last Modified: Wed, 13 May 2020 14:04:11 GMT  
		Size: 200.6 KB (200612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c55fddd514eaafb559e342ccd8eac21c11ad69bef26a2fef44ffcc1dad3d26c0`  
		Last Modified: Wed, 13 May 2020 14:05:42 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
