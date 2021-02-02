## `hylang:python3.7-windowsservercore-ltsc2016`

```console
$ docker pull hylang@sha256:37808e27772eb267128891fdec66c31aa887f4c9515e1c6ce0d9f52110bc9edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.4169; amd64

### `hylang:python3.7-windowsservercore-ltsc2016` - windows version 10.0.14393.4169; amd64

```console
$ docker pull hylang@sha256:18c55ff94f8989ddc0579e3a41f817974d881c07022e471ba0765f67793d2e8d
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5877161060 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75dc052606edda53deec1da0c281148bf4c0c51afa801007adfc0744ba3e747d`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Thu, 07 Jan 2021 11:30:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 Jan 2021 13:37:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Jan 2021 19:15:14 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 13 Jan 2021 19:36:14 GMT
ENV PYTHON_VERSION=3.7.9
# Wed, 13 Jan 2021 19:36:15 GMT
ENV PYTHON_RELEASE=3.7.9
# Wed, 13 Jan 2021 19:38:37 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Mon, 01 Feb 2021 22:23:17 GMT
ENV PYTHON_PIP_VERSION=21.0.1
# Mon, 01 Feb 2021 22:23:18 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4be3fe44ad9dedc028629ed1497052d65d281b8e/get-pip.py
# Mon, 01 Feb 2021 22:23:18 GMT
ENV PYTHON_GET_PIP_SHA256=8006625804f55e1bd99ad4214fd07082fee27a1c35945648a58f9087a714e9d4
# Mon, 01 Feb 2021 22:24:59 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Mon, 01 Feb 2021 22:25:00 GMT
CMD ["python"]
# Mon, 01 Feb 2021 22:49:57 GMT
ENV HY_VERSION=0.20.0
# Mon, 01 Feb 2021 22:51:34 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Mon, 01 Feb 2021 22:51:35 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bd091f41e44cabc11504b7e130c74a7ef654f58840ba102e3507c4fdf2bae994`  
		Size: 1.7 GB (1723908142 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:51e9c5c519fdcd28aa0ed033a3cc16cf37dd76bea8ec06b2dc4a344415bdd224`  
		Last Modified: Wed, 13 Jan 2021 15:10:27 GMT  
		Size: 1.2 KB (1164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:036493f24213085956c7e7402a5d91f9c1e8e833f024c212f39aee0efbe03044`  
		Last Modified: Wed, 13 Jan 2021 19:42:33 GMT  
		Size: 1.1 KB (1129 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47dd734616e005333ddb53da60c37235239d8c6707f41a1f0a6fe732d016641`  
		Last Modified: Wed, 13 Jan 2021 19:46:34 GMT  
		Size: 1.1 KB (1135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bb3fc5f9d5da313802360243ee600190788a036700c72c14506d137bcfca2a4`  
		Last Modified: Wed, 13 Jan 2021 19:46:33 GMT  
		Size: 1.1 KB (1125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ad16f05d616751491421729282d14cab26a5d652ec58d536373b58bcad0be5f`  
		Last Modified: Wed, 13 Jan 2021 19:46:42 GMT  
		Size: 56.7 MB (56710217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c1ba70b86e6e5f0fb966d736e4f889c9fa02027f08d715f012cdbe59a70e85d`  
		Last Modified: Mon, 01 Feb 2021 22:28:16 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0bdb5b1ee122175135638857b5ec2e858d28d0242ba8b81a81b17e617b2c58a`  
		Last Modified: Mon, 01 Feb 2021 22:28:16 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c902c1635a0c556c6f02dcf72c40a0a36bd8c3e42726a40af907d50a5f63f0b0`  
		Last Modified: Mon, 01 Feb 2021 22:28:16 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f41db7c30c5f01b2f57e3604b247c527197ea27ae97b4a348661d0b2c2188ce4`  
		Last Modified: Mon, 01 Feb 2021 22:28:34 GMT  
		Size: 15.6 MB (15609094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f63379970ae03e392566346d528cd12ae568634da433ffae6ce90f456cb704`  
		Last Modified: Mon, 01 Feb 2021 22:28:16 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61a1be14c7bc47ec93f34660ca7e612445b5dde66d907037c3d0f272149e8f83`  
		Last Modified: Mon, 01 Feb 2021 22:53:59 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:842b479b767ace7235f9fa0fd6916ba83b207b3868aeae9cb18af3b4a82f0836`  
		Last Modified: Mon, 01 Feb 2021 22:54:02 GMT  
		Size: 10.9 MB (10934914 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33a9af3415f9f5ac779e82a0b50b3ece7bc7b7452316f363afd6909fcd3f18e5`  
		Last Modified: Mon, 01 Feb 2021 22:53:59 GMT  
		Size: 1.4 KB (1418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
