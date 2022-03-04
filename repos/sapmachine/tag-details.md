<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `sapmachine`

-	[`sapmachine:11`](#sapmachine11)
-	[`sapmachine:11.0.14.1`](#sapmachine110141)
-	[`sapmachine:17`](#sapmachine17)
-	[`sapmachine:17.0.2`](#sapmachine1702)
-	[`sapmachine:latest`](#sapmachinelatest)
-	[`sapmachine:lts`](#sapmachinelts)

## `sapmachine:11`

```console
$ docker pull sapmachine@sha256:c3422055c250950a5b78e6c297444382a24aa8f48ddcc3cac7e1167acfa09665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11` - linux; amd64

```console
$ docker pull sapmachine@sha256:3c13a6ff72085be89893e7a378549e9d055b99655e882a99b46868d228806433
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234595025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920edf16dd81dfed126d6773301ee0bf2253e927ab9f8fc7b622b765ef75cdc6`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:30:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:30:32 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.14.1     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:30:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 03 Mar 2022 23:30:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ab19b53a1b84fb848704b282f933869153728103e9a9276d9ad881cf6a4c71`  
		Last Modified: Thu, 03 Mar 2022 23:31:22 GMT  
		Size: 8.3 MB (8318294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27de5ce49c862e59e6339d565ab8ad01196ed8fc48e6dc4f6ef06907244e133`  
		Last Modified: Thu, 03 Mar 2022 23:31:35 GMT  
		Size: 197.7 MB (197710980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:11.0.14.1`

```console
$ docker pull sapmachine@sha256:c3422055c250950a5b78e6c297444382a24aa8f48ddcc3cac7e1167acfa09665
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:11.0.14.1` - linux; amd64

```console
$ docker pull sapmachine@sha256:3c13a6ff72085be89893e7a378549e9d055b99655e882a99b46868d228806433
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.6 MB (234595025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:920edf16dd81dfed126d6773301ee0bf2253e927ab9f8fc7b622b765ef75cdc6`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:30:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:30:32 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-11-jdk=11.0.14.1     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:30:32 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-11
# Thu, 03 Mar 2022 23:30:32 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ab19b53a1b84fb848704b282f933869153728103e9a9276d9ad881cf6a4c71`  
		Last Modified: Thu, 03 Mar 2022 23:31:22 GMT  
		Size: 8.3 MB (8318294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27de5ce49c862e59e6339d565ab8ad01196ed8fc48e6dc4f6ef06907244e133`  
		Last Modified: Thu, 03 Mar 2022 23:31:35 GMT  
		Size: 197.7 MB (197710980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17`

```console
$ docker pull sapmachine@sha256:f56e984143daaa39d463cee8ed5c16e1413c2d72901df0e12cfe39e2ed60d4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17` - linux; amd64

```console
$ docker pull sapmachine@sha256:b8f829c57e21906864244ef67ba3b3951f097474feb230769818ff96a6912641
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234531573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733a4604f5cc634b5f544945b86167c54006b29f7b993c49bc880cd5272db972`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:30:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:31:06 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:31:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 03 Mar 2022 23:31:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ab19b53a1b84fb848704b282f933869153728103e9a9276d9ad881cf6a4c71`  
		Last Modified: Thu, 03 Mar 2022 23:31:22 GMT  
		Size: 8.3 MB (8318294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab28bae6333343ba1ffc77a643493edc6891fa046da6da726f0944a2b157491e`  
		Last Modified: Thu, 03 Mar 2022 23:32:00 GMT  
		Size: 197.6 MB (197647528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:17.0.2`

```console
$ docker pull sapmachine@sha256:f56e984143daaa39d463cee8ed5c16e1413c2d72901df0e12cfe39e2ed60d4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:17.0.2` - linux; amd64

```console
$ docker pull sapmachine@sha256:b8f829c57e21906864244ef67ba3b3951f097474feb230769818ff96a6912641
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234531573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733a4604f5cc634b5f544945b86167c54006b29f7b993c49bc880cd5272db972`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:30:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:31:06 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:31:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 03 Mar 2022 23:31:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ab19b53a1b84fb848704b282f933869153728103e9a9276d9ad881cf6a4c71`  
		Last Modified: Thu, 03 Mar 2022 23:31:22 GMT  
		Size: 8.3 MB (8318294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab28bae6333343ba1ffc77a643493edc6891fa046da6da726f0944a2b157491e`  
		Last Modified: Thu, 03 Mar 2022 23:32:00 GMT  
		Size: 197.6 MB (197647528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:latest`

```console
$ docker pull sapmachine@sha256:f56e984143daaa39d463cee8ed5c16e1413c2d72901df0e12cfe39e2ed60d4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:latest` - linux; amd64

```console
$ docker pull sapmachine@sha256:b8f829c57e21906864244ef67ba3b3951f097474feb230769818ff96a6912641
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234531573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733a4604f5cc634b5f544945b86167c54006b29f7b993c49bc880cd5272db972`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:30:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:31:06 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:31:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 03 Mar 2022 23:31:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ab19b53a1b84fb848704b282f933869153728103e9a9276d9ad881cf6a4c71`  
		Last Modified: Thu, 03 Mar 2022 23:31:22 GMT  
		Size: 8.3 MB (8318294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab28bae6333343ba1ffc77a643493edc6891fa046da6da726f0944a2b157491e`  
		Last Modified: Thu, 03 Mar 2022 23:32:00 GMT  
		Size: 197.6 MB (197647528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `sapmachine:lts`

```console
$ docker pull sapmachine@sha256:f56e984143daaa39d463cee8ed5c16e1413c2d72901df0e12cfe39e2ed60d4da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; amd64

### `sapmachine:lts` - linux; amd64

```console
$ docker pull sapmachine@sha256:b8f829c57e21906864244ef67ba3b3951f097474feb230769818ff96a6912641
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **234.5 MB (234531573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:733a4604f5cc634b5f544945b86167c54006b29f7b993c49bc880cd5272db972`
-	Default Command: `["jshell"]`

```dockerfile
# Thu, 03 Mar 2022 20:19:33 GMT
ADD file:8a50ad78a668527e974b05a3dfbfd64760de3cb643ceb8a8805d21f6ceab3389 in / 
# Thu, 03 Mar 2022 20:19:33 GMT
CMD ["bash"]
# Thu, 03 Mar 2022 23:30:03 GMT
RUN apt-get update     && apt-get install -y --no-install-recommends wget ca-certificates gnupg2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:31:06 GMT
RUN export GNUPGHOME="$(mktemp -d)"     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.old.key | gpg --batch --import     && gpg --batch --export --armor 'DA4C 00C1 BDB1 3763 8608 4E20 C7EB 4578 740A EEA2' > /etc/apt/trusted.gpg.d/sapmachine.old.gpg.asc     && wget -q -O - https://dist.sapmachine.io/debian/sapmachine.key | gpg --batch --import     && gpg --batch --export --armor 'CACB 9FE0 9150 307D 1D22 D829 6275 4C3B 3ABC FE23' > /etc/apt/trusted.gpg.d/sapmachine.gpg.asc     && gpgconf --kill all && rm -rf "$GNUPGHOME"     && echo "deb http://dist.sapmachine.io/debian/amd64/ ./" > /etc/apt/sources.list.d/sapmachine.list     && apt-get update     && apt-get -y --no-install-recommends install sapmachine-17-jdk=17.0.2     && rm -rf /var/lib/apt/lists/*
# Thu, 03 Mar 2022 23:31:06 GMT
ENV JAVA_HOME=/usr/lib/jvm/sapmachine-17
# Thu, 03 Mar 2022 23:31:06 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:7c3b88808835aa80f1ef7f03083c5ae781d0f44e644537cd72de4ce6c5e62e00`  
		Last Modified: Thu, 03 Mar 2022 20:20:44 GMT  
		Size: 28.6 MB (28565751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51ab19b53a1b84fb848704b282f933869153728103e9a9276d9ad881cf6a4c71`  
		Last Modified: Thu, 03 Mar 2022 23:31:22 GMT  
		Size: 8.3 MB (8318294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab28bae6333343ba1ffc77a643493edc6891fa046da6da726f0944a2b157491e`  
		Last Modified: Thu, 03 Mar 2022 23:32:00 GMT  
		Size: 197.6 MB (197647528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
