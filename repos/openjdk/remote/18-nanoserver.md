## `openjdk:18-nanoserver`

```console
$ docker pull openjdk@sha256:d57b3582f7615af256c20480f6445dace87537adf72f5da37491d8b993c08106
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2686; amd64

### `openjdk:18-nanoserver` - windows version 10.0.17763.2686; amd64

```console
$ docker pull openjdk@sha256:c20ad394579f8fb7b76118b24d416a3e640286dd63d1d45686ac566ffc0adc5d
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **290.7 MB (290670157 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d313dba45ccd6a5a465713f573b7f899a6501e4d3980099e802c95c88ab136`
-	Default Command: `["jshell"]`
-	`SHELL`: `["cmd","\/s","\/c"]`

```dockerfile
# Thu, 03 Mar 2022 14:36:26 GMT
RUN Apply image 1809-amd64
# Tue, 08 Mar 2022 21:56:20 GMT
SHELL [cmd /s /c]
# Wed, 09 Mar 2022 17:18:37 GMT
ENV JAVA_HOME=C:\openjdk-18
# Wed, 09 Mar 2022 17:18:37 GMT
USER ContainerAdministrator
# Wed, 09 Mar 2022 17:18:46 GMT
RUN echo Updating PATH: %JAVA_HOME%\bin;%PATH% 	&& setx /M PATH %JAVA_HOME%\bin;%PATH% 	&& echo Complete.
# Wed, 09 Mar 2022 17:18:47 GMT
USER ContainerUser
# Wed, 09 Mar 2022 17:18:48 GMT
ENV JAVA_VERSION=18
# Wed, 09 Mar 2022 17:19:01 GMT
COPY dir:9514de164eda2cdb5e3ddd51197372d790fb5291cfc39842e090e2c568516144 in C:\openjdk-18 
# Wed, 09 Mar 2022 17:19:16 GMT
RUN echo Verifying install ... 	&& echo   javac --version && javac --version 	&& echo   java --version && java --version 	&& echo Complete.
# Wed, 09 Mar 2022 17:19:17 GMT
CMD ["jshell"]
```

-	Layers:
	-	`sha256:8e36e211379dc6a584a05a445fe37d396de6e76a42cc6742213c3cc3c656dd48`  
		Size: 103.1 MB (103054555 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e0065cd23a657c8f30ae5af121fd18451d2307835a1124ea57c80683eda26c94`  
		Last Modified: Tue, 08 Mar 2022 22:37:21 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f287433c772568106f9ee4fde27dc6b22d7b4fbfd3a47f2050a04e8a71a66071`  
		Last Modified: Wed, 09 Mar 2022 17:44:03 GMT  
		Size: 1.2 KB (1157 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5428cb9d915f363c4a521b05f6027228f9c2297ebb6f4b1a3e0208603e2022`  
		Last Modified: Wed, 09 Mar 2022 17:44:03 GMT  
		Size: 1.1 KB (1138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a9899dd7ef90d2406d61c40028a820140ba7bed5f4924d9ff318fe07db513a1`  
		Last Modified: Wed, 09 Mar 2022 17:44:03 GMT  
		Size: 68.1 KB (68136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:167d0a9bdbf4897335509ecc55faeac12df1bf74cc7cf6c4ceefb16b2431f7f9`  
		Last Modified: Wed, 09 Mar 2022 17:44:01 GMT  
		Size: 1.2 KB (1179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2be9fda0ab49f5d606b50c11f251a480ed372a88efb9cb06e933ddda204e32f9`  
		Last Modified: Wed, 09 Mar 2022 17:44:01 GMT  
		Size: 1.2 KB (1175 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6df1a373edb26d1cf9627fcdd1fb5ff5e77c010a3fc66c8828b5ed6a8b201fe`  
		Last Modified: Wed, 09 Mar 2022 17:44:22 GMT  
		Size: 184.0 MB (183987920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be5e08144df0c47683bcecafa2a791d7913888bd40575f60a00c7a1652c9597`  
		Last Modified: Wed, 09 Mar 2022 17:44:02 GMT  
		Size: 3.6 MB (3552568 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21e5abfcd871c2fe50782c00af74b758b430a075cb36be589861296c46575f23`  
		Last Modified: Wed, 09 Mar 2022 17:44:01 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
