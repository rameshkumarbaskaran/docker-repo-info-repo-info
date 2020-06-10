## `hylang:0-windowsservercore-ltsc2016`

```console
$ docker pull hylang@sha256:2222c6dd63608e27ffb094bbabec3377aa4176c3cfd21847bb105967573a1799
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3750; amd64

### `hylang:0-windowsservercore-ltsc2016` - windows version 10.0.14393.3750; amd64

```console
$ docker pull hylang@sha256:fa183763135460404a27afb4062fce71af4a9e5be860e11a63fe963fce3c3809
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5808337465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1ebf01e728d7109593e4e3cf8e55143489a86e3b51909829fd87dc11dff2a2e`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 01 Jun 2020 18:53:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 09 Jun 2020 22:36:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Jun 2020 23:45:06 GMT
ENV PYTHON_VERSION=3.8.3
# Tue, 09 Jun 2020 23:45:07 GMT
ENV PYTHON_RELEASE=3.8.3
# Tue, 09 Jun 2020 23:47:40 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Tue, 09 Jun 2020 23:47:41 GMT
ENV PYTHON_PIP_VERSION=20.1.1
# Tue, 09 Jun 2020 23:47:42 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/eff16c878c7fd6b688b9b4c4267695cf1a0bf01b/get-pip.py
# Tue, 09 Jun 2020 23:47:44 GMT
ENV PYTHON_GET_PIP_SHA256=b3153ec0cf7b7bbf9556932aa37e4981c35dc2a2c501d70d91d2795aa532be79
# Tue, 09 Jun 2020 23:49:30 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 09 Jun 2020 23:49:31 GMT
CMD ["python"]
# Wed, 10 Jun 2020 00:25:29 GMT
ENV HY_VERSION=0.18.0
# Wed, 10 Jun 2020 00:27:00 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 10 Jun 2020 00:27:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:375fbabb84945635805b46a02a17ac15a3177bcaae7404cfab5f1ceb0460cb60`  
		Size: 1.7 GB (1664011795 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c938241e0507e1ada5f864325483d86fd08533a5a31e7cb6ec1357db9891b245`  
		Last Modified: Tue, 09 Jun 2020 23:18:33 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d3e04457ea7475dd69e5af2326512ed9da9a226de555104ff0043992ed9c9e`  
		Last Modified: Wed, 10 Jun 2020 00:05:02 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d5fee970b245bda5ea87fa306cfd1a0d10b7e05d78386ee5b64c40236b3ee52`  
		Last Modified: Wed, 10 Jun 2020 00:05:01 GMT  
		Size: 1.1 KB (1147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc46623e1e8e76b396ff66676c140f175db08c8edac30b6e333abdca84767231`  
		Last Modified: Wed, 10 Jun 2020 00:05:11 GMT  
		Size: 57.6 MB (57639986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b1f495afd2b57bce97c1f839b6d526c976d0de51c03df93446e627a81638813`  
		Last Modified: Wed, 10 Jun 2020 00:04:59 GMT  
		Size: 1.1 KB (1120 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da6247301deb69dbb6ca233b75d7f46abf92102e5190b087aa9248752be5f28e`  
		Last Modified: Wed, 10 Jun 2020 00:04:59 GMT  
		Size: 1.1 KB (1127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5904c98f5e6baf8ff885bb91a9436d3c4b87bf0965e2879dd91e4f17c00ff9fe`  
		Last Modified: Wed, 10 Jun 2020 00:04:59 GMT  
		Size: 1.1 KB (1100 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9240c5fc07255136d4bb14472244efab19ffcdf000fd84eb1e492510356a51c0`  
		Last Modified: Wed, 10 Jun 2020 00:05:02 GMT  
		Size: 10.5 MB (10530156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b99edb54d564024b171f8b73368eb1c857952d903988b6e9ef2cabfe28d65cb0`  
		Last Modified: Wed, 10 Jun 2020 00:04:59 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9486ee07927d8bb3fc50bb9cc7123338790b75d358ca2b579aa6308351bd8fb`  
		Last Modified: Wed, 10 Jun 2020 00:30:51 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dfc43f812619be2849aa8c5d467eab0ee1d2a1ae7426f2d4fffc2b5200f1a80`  
		Last Modified: Wed, 10 Jun 2020 00:30:53 GMT  
		Size: 6.2 MB (6159470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e759e93d09a4bdbfe229693d1af2d33a9f910af7a715c65c82d1f874aaaa138`  
		Last Modified: Wed, 10 Jun 2020 00:30:51 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
