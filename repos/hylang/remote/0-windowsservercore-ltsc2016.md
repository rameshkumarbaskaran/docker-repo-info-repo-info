## `hylang:0-windowsservercore-ltsc2016`

```console
$ docker pull hylang@sha256:fd1ff50826dee3d557df713a8ebed67f49de0331272eb28e523f1fe01d6f26dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3630; amd64

### `hylang:0-windowsservercore-ltsc2016` - windows version 10.0.14393.3630; amd64

```console
$ docker pull hylang@sha256:757ba0ff657e1448b64bc6adf88e3ca21a235779915ad4965072e46959373e66
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5797462344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6aaca30749fb097f71444860ecd7c8e3ed78f19504ca3542e7be1ac517d268e`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Tue, 07 Apr 2020 17:30:00 GMT
RUN Install update ltsc2016-amd64
# Tue, 14 Apr 2020 21:35:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 15 Apr 2020 17:05:37 GMT
ENV PYTHON_VERSION=3.8.2
# Wed, 15 Apr 2020 17:05:38 GMT
ENV PYTHON_RELEASE=3.8.2
# Wed, 15 Apr 2020 17:07:43 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 29 Apr 2020 17:21:18 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 29 Apr 2020 17:21:19 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 29 Apr 2020 17:21:20 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 29 Apr 2020 17:22:59 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 29 Apr 2020 17:23:00 GMT
CMD ["python"]
# Wed, 29 Apr 2020 18:08:22 GMT
ENV HY_VERSION=0.18.0
# Wed, 29 Apr 2020 18:09:43 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 29 Apr 2020 18:09:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:d0099407ec8ccaf0472e55152e38b262bdf0b2cf8dfd2e8afcc89d728ba3f5a0`  
		Size: 1.7 GB (1658081673 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7ac0134cee91589d04e97f11994235cce86faef5c581d15f2e143ecb90e92572`  
		Last Modified: Tue, 14 Apr 2020 22:16:36 GMT  
		Size: 1.1 KB (1149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:775137087fc01e1d559cc5f83e20ae7ede521f5419f3eb74180f9943ca44e0f1`  
		Last Modified: Wed, 15 Apr 2020 17:27:19 GMT  
		Size: 1.1 KB (1132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c37f9a6ba915a26c649bad66215d831c784f2b25898304960b5f790fa5d38fb`  
		Last Modified: Wed, 15 Apr 2020 17:27:19 GMT  
		Size: 1.1 KB (1116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5790ee59a1dd6e257ba2f04a0c390d0ab34b38397ea7912e7f3ab9facdb314be`  
		Last Modified: Wed, 15 Apr 2020 17:27:26 GMT  
		Size: 52.7 MB (52674827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c79197c69fd78739ffafa84fdbe3fad1ad5fd55d795c0decbedc454776039373`  
		Last Modified: Wed, 29 Apr 2020 17:29:26 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e7d631569f6df4d95c1864ddb8044825cfcae0756142bf093a07af5637353ff`  
		Last Modified: Wed, 29 Apr 2020 17:29:25 GMT  
		Size: 1.1 KB (1145 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed5009531508be3ec9f5e7356175c573105bb7bf09a668ac3850652c15909879`  
		Last Modified: Wed, 29 Apr 2020 17:29:26 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42d6fccec6f0d7a545fcf88a36f41d3cbb77f6fbad4096cf3bb1bc90f8790901`  
		Last Modified: Wed, 29 Apr 2020 17:29:29 GMT  
		Size: 10.5 MB (10546143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1d4a423984a2fe835272ac76c8a90f8f71e02c5fb71e38f805118e0d7f09c9a`  
		Last Modified: Wed, 29 Apr 2020 17:29:26 GMT  
		Size: 1.1 KB (1126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28f64c96a112833ec200d113de3bff8456af6b0d4ff75aafa0fbdbd95f924c75`  
		Last Modified: Wed, 29 Apr 2020 18:43:36 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f825576e59b988c4db43cac8703f775f4c7b0b4aa862198f439acd674656898`  
		Last Modified: Wed, 29 Apr 2020 18:43:38 GMT  
		Size: 6.2 MB (6163589 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad4c9697fa26832ee536bee3c4d8c2b15281e6d8fc61b9362a0d74dbbb29c9e6`  
		Last Modified: Wed, 29 Apr 2020 18:43:36 GMT  
		Size: 1.1 KB (1148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
