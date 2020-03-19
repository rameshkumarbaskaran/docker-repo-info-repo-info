## `openjdk:nanoserver`

```console
$ docker pull openjdk@sha256:7be0f7049ae92237d9602740fba5c594c8b1521bcfeeb97cb06c5c0ddb3fc266
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1098; amd64

### `openjdk:nanoserver` - windows version 10.0.17763.1098; amd64

```console
$ docker pull openjdk@sha256:be88db4c6117430bd4077c85d0620735d53c15b10ce4cd88c2d064bb455c167c
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **298.6 MB (298561149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acca5fd653535cf10f7db9a134d60d74611e5e8d6518dbead1a049c64bea3c6`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Wed, 04 Mar 2020 13:28:48 GMT
RUN Apply image 1809-amd64
# Wed, 11 Mar 2020 14:56:25 GMT
SHELL [cmd /s /c]
# Wed, 11 Mar 2020 15:01:30 GMT
ENV JAVA_HOME=C:\openjdk-14
# Wed, 11 Mar 2020 15:01:31 GMT
USER ContainerAdministrator
# Wed, 11 Mar 2020 15:01:45 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH%
# Wed, 11 Mar 2020 15:01:46 GMT
USER ContainerUser
# Wed, 11 Mar 2020 15:01:47 GMT
ENV JAVA_VERSION=14
# Wed, 11 Mar 2020 15:02:44 GMT
COPY dir:0d7510b7a9b226b4119fe9742b05f867c4806b739843cccbc6742c7969c1cdd8 in C:\openjdk-14 
# Wed, 11 Mar 2020 15:03:06 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version
# Wed, 11 Mar 2020 15:03:07 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8e709836e4dce2fa52689be79fedc1e3d040ba47ec2da2fc3b23f33fc6944b50`  
		Size: 101.1 MB (101050245 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:4a66be005a5120fc8bbc31290c77aa0e6580d02bc61948ef0602bf09a6ab61ba`  
		Last Modified: Wed, 11 Mar 2020 15:26:11 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a09634ed84f623cd3211a24ac7cc0357d00c18f46a5e6f199a15d0e15b3d5ef`  
		Last Modified: Wed, 11 Mar 2020 15:27:59 GMT  
		Size: 911.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc35fbcd83ad8900a6833c3c597a513b87cee176f1164216e7a15c7d5237641`  
		Last Modified: Wed, 11 Mar 2020 15:27:59 GMT  
		Size: 938.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4070d6d1f467b6563aa750bd2872fdfaba6a916b785fbcb98b1ca687961d9dc7`  
		Last Modified: Wed, 11 Mar 2020 15:27:59 GMT  
		Size: 63.8 KB (63817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70546ab1b2856c7569064bc70ce1faab4f12aa1f81232874271741104a79f4dc`  
		Last Modified: Wed, 11 Mar 2020 15:27:55 GMT  
		Size: 934.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2b49cd51f4bc6e40b466ed76bbc71d66e02c4e436626073f7ed2f94a6889150`  
		Last Modified: Wed, 11 Mar 2020 15:27:55 GMT  
		Size: 933.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae574a991bd102d2b495d984db6373b4f2e3dfd9a8bd8a57c8051eaf1b68b431`  
		Last Modified: Wed, 11 Mar 2020 15:28:32 GMT  
		Size: 194.0 MB (193965635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0ae45682397b0752ed4716dc05ba284421e576b9158b6b6631506440aef404`  
		Last Modified: Wed, 11 Mar 2020 15:27:56 GMT  
		Size: 3.5 MB (3475847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03ab3e99b890c00f795b294bb23200737c139af3019ada602f7d0bf54282006`  
		Last Modified: Wed, 11 Mar 2020 15:27:55 GMT  
		Size: 956.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
