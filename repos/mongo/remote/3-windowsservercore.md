## `mongo:3-windowsservercore`

```console
$ docker pull mongo@sha256:863715547ef6c5ee090b9d663dd6a0ec97005e4623b3ad4a8ac6f4a2024b777b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3986; amd64
	-	windows version 10.0.17763.1518; amd64

### `mongo:3-windowsservercore` - windows version 10.0.14393.3986; amd64

```console
$ docker pull mongo@sha256:9530a5ad2b2286ad0d9e676a8bc8aa717c4ad168e1805f0967e11cbe3bbe9373
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.4 GB (6436897846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:131971729d29463de051a5a1af812816e1a171c68a598443f3ef4391716a5826`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Fri, 02 Oct 2020 17:07:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Oct 2020 13:36:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Oct 2020 21:23:55 GMT
ENV MONGO_VERSION=3.6.20
# Wed, 14 Oct 2020 21:23:55 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.20-signed.msi
# Wed, 14 Oct 2020 21:23:56 GMT
ENV MONGO_DOWNLOAD_SHA256=341d1163c192488596e01219b50c14c9113ad0c305b0aef73f271d9746e44aa1
# Wed, 14 Oct 2020 21:47:13 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 21:47:15 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Oct 2020 21:47:16 GMT
EXPOSE 27017
# Wed, 14 Oct 2020 21:47:16 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:17a32268498b2feefa5457f0423ac15473596d514e48c694ef54d740a9a5067d`  
		Size: 1.7 GB (1671365753 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb0caa156c690c0274404e38041b8eb56dcd2c15edbc269fc4c619eb667cb7ff`  
		Last Modified: Wed, 14 Oct 2020 16:03:09 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9875d6371a610f089fa17e2ad38eba6216398b1dab279e035bd6d1da13f1b493`  
		Last Modified: Wed, 14 Oct 2020 23:55:42 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c3bc5009df74efef73e0f8ffad383091e5502a19767ba1fe077f2799e983cf`  
		Last Modified: Wed, 14 Oct 2020 23:55:42 GMT  
		Size: 1.1 KB (1143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7911fa7a5f428ed9eb4607316ba18faffb23ca1b4a7859c573e3cb790a64839c`  
		Last Modified: Wed, 14 Oct 2020 23:55:39 GMT  
		Size: 1.2 KB (1161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6485b7d792a4acc440618729ddec2cdb5c997d8443860b1d906de6c672c8c37`  
		Last Modified: Wed, 14 Oct 2020 23:57:25 GMT  
		Size: 695.5 MB (695538179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2777b1831872fe6c9795b5cf7513c6beb04935a890c28da6ae181bf60eb305b`  
		Last Modified: Wed, 14 Oct 2020 23:55:38 GMT  
		Size: 1.2 KB (1173 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde6031df331f8bc2a1c63c7c5d120c980d20c49cf3de94502069c8bc79300e5`  
		Last Modified: Wed, 14 Oct 2020 23:55:39 GMT  
		Size: 1.2 KB (1162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5dc916c949218426175a8c011fcaba117859f9a76d00b5de65a254f1a655abfe`  
		Last Modified: Wed, 14 Oct 2020 23:55:39 GMT  
		Size: 1.1 KB (1121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `mongo:3-windowsservercore` - windows version 10.0.17763.1518; amd64

```console
$ docker pull mongo@sha256:b8fefcddbb21895882a3482395682ef472c52db6ba6eb096740c55bcca6828d8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 GB (3069087808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29ab4912c4fd77cd0395d2cd593e631bd8e6c28c10524af7140e31c60f21262f`
-	Default Command: `["mongod","--bind_ip_all"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 01 Oct 2020 02:26:38 GMT
RUN Install update 1809-amd64
# Wed, 14 Oct 2020 12:58:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop';]
# Wed, 14 Oct 2020 21:47:31 GMT
ENV MONGO_VERSION=3.6.20
# Wed, 14 Oct 2020 21:47:31 GMT
ENV MONGO_DOWNLOAD_URL=https://fastdl.mongodb.org/win32/mongodb-win32-x86_64-2008plus-ssl-3.6.20-signed.msi
# Wed, 14 Oct 2020 21:47:32 GMT
ENV MONGO_DOWNLOAD_SHA256=341d1163c192488596e01219b50c14c9113ad0c305b0aef73f271d9746e44aa1
# Wed, 14 Oct 2020 22:11:52 GMT
RUN Write-Host ('Downloading {0} ...' -f $env:MONGO_DOWNLOAD_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	(New-Object System.Net.WebClient).DownloadFile($env:MONGO_DOWNLOAD_URL, 'mongo.msi'); 		if ($env:MONGO_DOWNLOAD_SHA256) { 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:MONGO_DOWNLOAD_SHA256); 		if ((Get-FileHash mongo.msi -Algorithm sha256).Hash -ne $env:MONGO_DOWNLOAD_SHA256) { 			Write-Host 'FAILED!'; 			exit 1; 		}; 	}; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'mongo.msi', 			'/quiet', 			'/qn', 			'INSTALLLOCATION=C:\mongodb', 			'ADDLOCAL=all' 		); 	$env:PATH = 'C:\mongodb\bin;' + $env:PATH; 	[Environment]::SetEnvironmentVariable('PATH', $env:PATH, [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  mongo --version'; mongo --version; 	Write-Host '  mongod --version'; mongod --version; 		Write-Host 'Removing ...'; 	Remove-Item C:\windows\installer\*.msi -Force; 	Remove-Item mongo.msi -Force; 		Write-Host 'Complete.';
# Wed, 14 Oct 2020 22:11:54 GMT
VOLUME [C:\data\db C:\data\configdb]
# Wed, 14 Oct 2020 22:11:55 GMT
EXPOSE 27017
# Wed, 14 Oct 2020 22:11:56 GMT
CMD ["mongod" "--bind_ip_all"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:406ffb8432a757e84f7594e85c676620dec6955e0475ac271aa4dd5c0531190d`  
		Size: 655.8 MB (655757265 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d839ec6fa74e5e869036dfd823e95452a7afcde18ac997af483c88c21b92ad8c`  
		Last Modified: Wed, 14 Oct 2020 16:02:33 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24247f3bb51d1d4e86da74443bc2c07ab23d165aa6e07f2a5a2d99cf05c7e09f`  
		Last Modified: Wed, 14 Oct 2020 23:57:46 GMT  
		Size: 1.2 KB (1154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad14823774a10cba45ad99901994ea512b74289f543aad2974750f173ca9bee0`  
		Last Modified: Wed, 14 Oct 2020 23:57:47 GMT  
		Size: 1.1 KB (1123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:082fab4a2a46a94445439e0ffbca86e7d33ca34a8471e9912ba73b5677f59305`  
		Last Modified: Wed, 14 Oct 2020 23:57:44 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:322ee7b70d12bd5de38d86cec245f4e621040b3ab8f19193a78ffe5b16895f9c`  
		Last Modified: Thu, 15 Oct 2020 00:04:56 GMT  
		Size: 695.0 MB (694989660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07f92a202efa518a36564623a29e77f98156933bad8ae7cd1aa620c26135d22`  
		Last Modified: Wed, 14 Oct 2020 23:57:44 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e53e24915deaffd8e1fe632ebb6ccee3d6189366052f323b4739dcfc5af05978`  
		Last Modified: Wed, 14 Oct 2020 23:57:43 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651fa935973ca4316c01b23f45eb6a2dacb626bd8df8ff766a1483ee06a1c327`  
		Last Modified: Wed, 14 Oct 2020 23:57:44 GMT  
		Size: 1.1 KB (1137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
