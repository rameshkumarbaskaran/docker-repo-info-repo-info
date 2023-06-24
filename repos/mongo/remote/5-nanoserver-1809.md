## `mongo:5-nanoserver-1809`

```console
$ docker pull mongo@sha256:349814cf8308934509ae346235cd092159ed9a931505c71588c135890703620f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.4499; amd64

### `mongo:5-nanoserver-1809` - windows version 10.0.17763.4499; amd64

```console
$ docker pull mongo@sha256:240f2cb231bbaa6b349da96cc484f42b1885a9179aebbc712b5a43910efc46ef
```

-	Docker Version: 20.10.21
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **417.4 MB (417359170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36eb612145847c01ba44178b28d020c46cf5e20cbfb840f69290ef927b6a49f8`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["cmd","\/S","\/C"]`

```dockerfile
# Wed, 21 Jun 2023 07:40:33 GMT
RUN Apply image 10.0.17763.4499
# Sat, 24 Jun 2023 01:50:24 GMT
SHELL [cmd /S /C]
# Sat, 24 Jun 2023 02:33:09 GMT
USER ContainerAdministrator
# Sat, 24 Jun 2023 02:33:23 GMT
RUN setx /m PATH "C:\mongodb\bin;%PATH%"
# Sat, 24 Jun 2023 02:33:24 GMT
USER ContainerUser
# Sat, 24 Jun 2023 02:53:18 GMT
COPY multi:9a4a91c322ba6325a22891e3a40eb7306a49c53e11d5828931f2326770a3f548 in C:\Windows\System32\ 
# Sat, 24 Jun 2023 02:53:19 GMT
ENV MONGO_VERSION=5.0.18
# Sat, 24 Jun 2023 02:53:46 GMT
COPY dir:ab74dbf9ad27d2154a3f270894c5c95f10fe56a2d5ec4c1875a57c2afdba8cff in C:\mongodb 
# Sat, 24 Jun 2023 02:53:57 GMT
RUN mongo --version && mongod --version
# Sat, 24 Jun 2023 02:53:58 GMT
VOLUME [C:\data\db C:\data\configdb]
# Sat, 24 Jun 2023 02:53:59 GMT
EXPOSE 27017
# Sat, 24 Jun 2023 02:54:00 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:09087aac643f57e5e24f95fe0a1c8519d0f93dfcf4500263516c0f3874290109`  
		Last Modified: Fri, 23 Jun 2023 02:23:11 GMT  
		Size: 104.4 MB (104400893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0712dde7e721d063ebcbe80a9968c96e3b3af1f54a33928786e0d37335da4cd`  
		Last Modified: Sat, 24 Jun 2023 02:18:04 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d8a638f113f886e54e8e494347981d25a36f28873f1b9e0905cef7ef9ef0227`  
		Last Modified: Sat, 24 Jun 2023 06:33:56 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b4deb983b7c23277ea52231f8a02797b91fd72aad7b9b8234cceb857505961`  
		Last Modified: Sat, 24 Jun 2023 06:33:54 GMT  
		Size: 69.6 KB (69575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3592f8eaf22ebd67118459d39e793af2168190561abf11f80b1f570fb5a468f9`  
		Last Modified: Sat, 24 Jun 2023 06:33:54 GMT  
		Size: 1.2 KB (1163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa83bb255dac1342d46c74b00ab672aa77772aecbd463ea10848b3db8c2257f`  
		Last Modified: Sat, 24 Jun 2023 06:50:26 GMT  
		Size: 263.5 KB (263520 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3d3a9bc2bbdd6ab6b2d46dfd1876a294841a8a904095f2f607149f85b534d57`  
		Last Modified: Sat, 24 Jun 2023 06:50:26 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6047d846f5732ffdae8417b26a75afb18b5177827a0672fc05e2f7d6deac0371`  
		Last Modified: Sat, 24 Jun 2023 06:51:16 GMT  
		Size: 312.5 MB (312540268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3dcfb1ed0ea20ba63ed0178f30ba16d76621616e47927b25226150b63c8b415`  
		Last Modified: Sat, 24 Jun 2023 06:50:24 GMT  
		Size: 76.8 KB (76805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:725dbe32666aa268b151e005f04de2f765b941cd17561a130770066ca85f3837`  
		Last Modified: Sat, 24 Jun 2023 06:50:24 GMT  
		Size: 1.2 KB (1156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3ca4bb5a835bb5f2afb55e4cc00ce5e40d6ffd5a770915cdc30ba9e2419eafb`  
		Last Modified: Sat, 24 Jun 2023 06:50:24 GMT  
		Size: 1.1 KB (1117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:909f98c902bb2abcebdde1fac47fc137f12af6af74896a2fd27938513ea4ca99`  
		Last Modified: Sat, 24 Jun 2023 06:50:24 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
