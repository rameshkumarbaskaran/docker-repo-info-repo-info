## `crate:latest`

```console
$ docker pull crate@sha256:9d5c87be9c09ceddf9e03e13599f0d79f340de63d47a7bd7edd51e93532f8725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8

### `crate:latest` - linux; amd64

```console
$ docker pull crate@sha256:ce6fddeaaf7a1ea9ba268fbaad872df5687afdcd685854b13086bfea2c75647a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **331.7 MB (331654566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0fda302fafc2a715b8b478370bc6259a05c49a8af3aa0c92fb01270c15a0eb1f`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Sat, 14 Nov 2020 00:20:04 GMT
ADD file:b3ebbe8bd304723d43b7b44a6d990cd657b63d93d6a2a9293983a30bfc1dfa53 in / 
# Sat, 14 Nov 2020 00:20:04 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:20:04 GMT
CMD ["/bin/bash"]
# Tue, 09 Mar 2021 20:19:32 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 05 May 2021 18:22:33 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.5.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.5.1.tar.gz.asc crate-4.5.1.tar.gz     && rm -rf "$GNUPGHOME" crate-4.5.1.tar.gz.asc     && tar -xf crate-4.5.1.tar.gz -C /crate --strip-components=1     && rm crate-4.5.1.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 05 May 2021 18:22:36 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 05 May 2021 18:22:36 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 May 2021 18:22:37 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 05 May 2021 18:22:38 GMT
RUN mkdir -p /data/data /data/log
# Wed, 05 May 2021 18:22:38 GMT
VOLUME [/data]
# Wed, 05 May 2021 18:22:38 GMT
WORKDIR /data
# Wed, 05 May 2021 18:22:38 GMT
EXPOSE 4200 4300 5432
# Wed, 05 May 2021 18:22:38 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 05 May 2021 18:22:39 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 05 May 2021 18:22:39 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-05-03T15:59:20.942294 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.5.1
# Wed, 05 May 2021 18:22:39 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 05 May 2021 18:22:39 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 May 2021 18:22:39 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:2d473b07cdd5f0912cd6f1a703352c82b512407db6b05b43f2553732b55df3bc`  
		Last Modified: Sat, 14 Nov 2020 00:21:39 GMT  
		Size: 76.1 MB (76097157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926db4efe32a315f470abd127b4b539a23e0b3d91f7bd574eea57006cbc72b94`  
		Last Modified: Tue, 09 Mar 2021 20:25:32 GMT  
		Size: 2.3 KB (2254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d77e66e7a495364e3292d53e767bfc87f5301c6f297b1bd11b24c45b9547aaf`  
		Last Modified: Wed, 05 May 2021 18:23:43 GMT  
		Size: 254.0 MB (253971094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4583e2e61296f4f5fce69e5431e73ccd87f2f1c61f4fdf00f5e594fc63ec564`  
		Last Modified: Wed, 05 May 2021 18:23:20 GMT  
		Size: 1.6 MB (1582182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8de716c3a1bbe6d064e0382be690611a7941f1fb03f7b4ad6f8700feaaf669a7`  
		Last Modified: Wed, 05 May 2021 18:23:19 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93cc412351d56849c52e9a7f1e9e4f84d7dfb0b70c9b69b3fc94cbbc7f7e75f`  
		Last Modified: Wed, 05 May 2021 18:23:19 GMT  
		Size: 264.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b51d9d9c12d08f60b9e18162fc8b2efa375ea75de86ce021ae2791c666b3536`  
		Last Modified: Wed, 05 May 2021 18:23:19 GMT  
		Size: 955.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e33470e2bac366dc8818750cfddf46e5cd8a82d18ed57ae7af7ddb587b732c1b`  
		Last Modified: Wed, 05 May 2021 18:23:19 GMT  
		Size: 503.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `crate:latest` - linux; arm64 variant v8

```console
$ docker pull crate@sha256:c3bbdffbd2ec09306d54b15296b44ae1c51134fe98ffe4bdc86e26f598eae192
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.7 MB (360682255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18522adbd24ab765fa73043f866b49dce7251efe445a30378b4c0bc8d65745bb`
-	Entrypoint: `["\/docker-entrypoint.sh"]`
-	Default Command: `["crate"]`

```dockerfile
# Sat, 14 Nov 2020 00:40:26 GMT
ADD file:5b1e63a3cb041177b802b501dedcd71a86f1773ea0f69f048f2eb3901097711d in / 
# Sat, 14 Nov 2020 00:40:31 GMT
LABEL org.label-schema.schema-version=1.0 org.label-schema.name=CentOS Base Image org.label-schema.vendor=CentOS org.label-schema.license=GPLv2 org.label-schema.build-date=20201113 org.opencontainers.image.title=CentOS Base Image org.opencontainers.image.vendor=CentOS org.opencontainers.image.licenses=GPL-2.0-only org.opencontainers.image.created=2020-11-13 00:00:00+00:00
# Sat, 14 Nov 2020 00:40:32 GMT
CMD ["/bin/bash"]
# Sat, 14 Nov 2020 00:57:11 GMT
RUN groupadd crate && useradd -u 1000 -g crate -d /crate crate
# Wed, 05 May 2021 18:40:43 GMT
RUN yum install -y yum-utils     && yum makecache     && yum install -y python36 openssl     && yum clean all     && rm -rf /var/cache/yum     && export PLATFORM="$(         case $(uname --m) in             x86_64)  echo x64_linux ;;             aarch64) echo aarch64_linux ;;         esac)"     && export CRATE_URL=https://cdn.crate.io/downloads/releases/cratedb/${PLATFORM}/crate-4.5.1.tar.gz     && curl -fSL -O ${CRATE_URL}     && curl -fSL -O ${CRATE_URL}.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crate-4.5.1.tar.gz.asc crate-4.5.1.tar.gz     && rm -rf "$GNUPGHOME" crate-4.5.1.tar.gz.asc     && tar -xf crate-4.5.1.tar.gz -C /crate --strip-components=1     && rm crate-4.5.1.tar.gz     && ln -sf /usr/bin/python3.6 /usr/bin/python3
# Wed, 05 May 2021 18:40:50 GMT
RUN curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0     && curl -fSL -O https://cdn.crate.io/downloads/releases/crash_standalone_0.27.0.asc     && export GNUPGHOME="$(mktemp -d)"     && gpg --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 90C23FC6585BC0717F8FBFC37FAAE51A06F6EAEB     && gpg --batch --verify crash_standalone_0.27.0.asc crash_standalone_0.27.0     && rm -rf "$GNUPGHOME" crash_standalone_0.27.0.asc     && mv crash_standalone_0.27.0 /usr/local/bin/crash     && chmod +x /usr/local/bin/crash
# Wed, 05 May 2021 18:40:51 GMT
ENV PATH=/crate/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 May 2021 18:40:52 GMT
ENV CRATE_HEAP_SIZE=512M
# Wed, 05 May 2021 18:40:54 GMT
RUN mkdir -p /data/data /data/log
# Wed, 05 May 2021 18:40:55 GMT
VOLUME [/data]
# Wed, 05 May 2021 18:40:55 GMT
WORKDIR /data
# Wed, 05 May 2021 18:40:56 GMT
EXPOSE 4200 4300 5432
# Wed, 05 May 2021 18:40:57 GMT
COPY --chown=1000:0file:bff8d2f33b7a44d36fcd66fc7e7d92b0ee463d0eb0df2a56e42511d4f1b3e9b2 in /crate/config/crate.yml 
# Wed, 05 May 2021 18:40:58 GMT
COPY --chown=1000:0file:5f0d1b776d3a6517508a00a88f8053bd0933a642599374c9dff00dc3b632fd09 in /crate/config/log4j2.properties 
# Wed, 05 May 2021 18:40:59 GMT
LABEL maintainer=Crate.io <office@crate.io> org.opencontainers.image.created=2021-05-03T15:59:20.942294 org.opencontainers.image.title=crate org.opencontainers.image.description=CrateDB is a distributed SQL database handles massive amounts of machine data in real-time. org.opencontainers.image.url=https://crate.io/products/cratedb/ org.opencontainers.image.source=https://github.com/crate/docker-crate org.opencontainers.image.vendor=Crate.io org.opencontainers.image.version=4.5.1
# Wed, 05 May 2021 18:41:00 GMT
COPY file:2e0f9e8c9006d6d56e9be42bd5646f68ec854481fcfbe51bafbf8695dc44b38a in / 
# Wed, 05 May 2021 18:41:01 GMT
ENTRYPOINT ["/docker-entrypoint.sh"]
# Wed, 05 May 2021 18:41:01 GMT
CMD ["crate"]
```

-	Layers:
	-	`sha256:6717b8ec66cd6add0272c6391165585613c31314a43ff77d9751b53010e531ec`  
		Last Modified: Sat, 14 Nov 2020 00:41:36 GMT  
		Size: 108.4 MB (108374945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6312a055314d3cb5a347fd7eb62a5fb7ad8e03a999e1c964f320a28325cf017d`  
		Last Modified: Sat, 14 Nov 2020 01:06:26 GMT  
		Size: 2.3 KB (2254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d8dc229d76fbeffd1a95212ff197b3c8e0706e806bf162d2920fea414ebad0f`  
		Last Modified: Wed, 05 May 2021 18:42:34 GMT  
		Size: 250.7 MB (250720981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc28486f7948fc68b842d7e6bc174e370fabd9acc09802b65223cfd307b0a2d`  
		Last Modified: Wed, 05 May 2021 18:41:54 GMT  
		Size: 1.6 MB (1582190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be5387d8443e971053c9647b4d3b843b465a6524b3cf043230bb6ba3a8de66fb`  
		Last Modified: Wed, 05 May 2021 18:41:54 GMT  
		Size: 157.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9d15534a24a40c7036c5b7e36d219ec1cb03d7ab746eee4dfca22923d48efc2`  
		Last Modified: Wed, 05 May 2021 18:41:55 GMT  
		Size: 266.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea464548b90eedced9b6a8141126a7517e12078e65709184b9b4a88d3611cd4`  
		Last Modified: Wed, 05 May 2021 18:41:54 GMT  
		Size: 957.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15a60870a37db50408203c0a8011e116fee856593050f1eb96a799b2a35253a1`  
		Last Modified: Wed, 05 May 2021 18:41:54 GMT  
		Size: 505.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
