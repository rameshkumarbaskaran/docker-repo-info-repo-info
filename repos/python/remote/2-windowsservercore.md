## `python:2-windowsservercore`

```console
$ docker pull python@sha256:c2e51a41dcff94bfb8331a26c4cc489315b7683968757d4cbf3fa0e9b0cddd01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3384; amd64
	-	windows version 10.0.17763.914; amd64

### `python:2-windowsservercore` - windows version 10.0.14393.3384; amd64

```console
$ docker pull python@sha256:1f64a705b5444342a468e489d55c54122479720f983d5d172cca113ef590e3ac
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5781116042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e29cac384be539e91fde3238df08b910c029b9b9c503b11f9e3db98cc0d0a483`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 00:35:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 01:03:56 GMT
ENV PYTHON_VERSION=2.7.17
# Wed, 11 Dec 2019 01:03:58 GMT
ENV PYTHON_RELEASE=2.7.17
# Wed, 11 Dec 2019 01:06:27 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.msi'; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		Write-Host 'Complete.'
# Wed, 11 Dec 2019 01:06:29 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Wed, 11 Dec 2019 01:06:31 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Wed, 11 Dec 2019 01:06:32 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Wed, 11 Dec 2019 01:08:31 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2019 01:09:39 GMT
RUN pip install --no-cache-dir virtualenv
# Wed, 11 Dec 2019 01:09:41 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:530e4240d4261ce165890648d1df6230dc4f9ce5df2e6cf9f0d5876694c3d4f0`  
		Last Modified: Wed, 11 Dec 2019 01:14:39 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0fc5ac64f92b1725178e8a81bf7c984989e70bcd1dd8f35aa1018cfc462da7`  
		Last Modified: Wed, 11 Dec 2019 01:20:34 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f9350657917fdc4491f23a8efb1bf94834a13e5c4a218fd05bf003a79fb350`  
		Last Modified: Wed, 11 Dec 2019 01:20:31 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8519793d32284fec35cb6975fe742fdafc521ef0ce25db012db0560a8670a860`  
		Last Modified: Wed, 11 Dec 2019 01:20:56 GMT  
		Size: 39.7 MB (39665149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b772691d1b71be25bb80a2bb2d1ab747979f975d716bfac502802e3b1e84fe7`  
		Last Modified: Wed, 11 Dec 2019 01:20:32 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf765289fdc9959f788ba53990776f7684bce5679b5eb9db4d537dc6459ad5`  
		Last Modified: Wed, 11 Dec 2019 01:20:28 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ffe4a93e5cde7661ee3a6471e2e4f2bb6e45eab43d6ed88932337979b491f1`  
		Last Modified: Wed, 11 Dec 2019 01:20:28 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5ef19b9966b41728d6fe2f6cab9f87b157d0c4e2e3979bb45e23cd92b24cdd`  
		Last Modified: Wed, 11 Dec 2019 01:20:43 GMT  
		Size: 10.0 MB (9978917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fca74f16b84172ba7f24cb6adb91662adc5910d988c953971a2da575c58c1d`  
		Last Modified: Wed, 11 Dec 2019 01:20:31 GMT  
		Size: 8.8 MB (8759784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23af693f219d1cb74719f5e27f2c5e8feb7055c6c43dd1df99b886edd47e1295`  
		Last Modified: Wed, 11 Dec 2019 01:20:28 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:2-windowsservercore` - windows version 10.0.17763.914; amd64

```console
$ docker pull python@sha256:080ec0f5f4d4c0e2dc026c3d1dab003f0feae6f05bd5e9eb2d8545da6c0bfe43
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2264003913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b121ad23f538a9c235f55e3981c7a861526106e0a2d990c70187fb32a4c09aea`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Tue, 10 Dec 2019 21:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 01:10:01 GMT
ENV PYTHON_VERSION=2.7.17
# Wed, 11 Dec 2019 01:10:02 GMT
ENV PYTHON_RELEASE=2.7.17
# Wed, 11 Dec 2019 01:11:59 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.msi'; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		Write-Host 'Complete.'
# Wed, 11 Dec 2019 01:12:01 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Wed, 11 Dec 2019 01:12:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Wed, 11 Dec 2019 01:12:04 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Wed, 11 Dec 2019 01:13:09 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2019 01:13:36 GMT
RUN pip install --no-cache-dir virtualenv
# Wed, 11 Dec 2019 01:13:37 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:faf31ee0aa3d3c60a38dd03c7554d632065cef50eab052ef1444590786249d07`  
		Size: 681.6 MB (681618026 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e147f14e0d6a9cbd5261162dea8f3aac7a34db5d9f6a587a9aac6b88722a2da4`  
		Last Modified: Tue, 10 Dec 2019 22:07:34 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e149e4386bb4e3ef4905fba057c6de2e777c90363739d26403684d35647fa62`  
		Last Modified: Wed, 11 Dec 2019 01:21:31 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fbc4f495276c58d77356bafa24bf14bb038dacef91110c764ddd2c68e60475`  
		Last Modified: Wed, 11 Dec 2019 01:21:30 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b834aea9069dae57ddf9692b9128c582add906d47aaf68548b698b3c50621b2f`  
		Last Modified: Wed, 11 Dec 2019 01:21:52 GMT  
		Size: 38.9 MB (38937795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2691f02b84e7e134c4c5f542bae1d79121d716db61a3bc2968ae4e985b32e6ec`  
		Last Modified: Wed, 11 Dec 2019 01:21:29 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09013b363839e63e6de1f6b87708d08a2a93aa6fbb142168882be83de78b40e9`  
		Last Modified: Wed, 11 Dec 2019 01:21:26 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274b0016f46ca64020ffca139291e6cd1a838b081630353f436adf905d697ee1`  
		Last Modified: Wed, 11 Dec 2019 01:21:26 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0849fb1bad3788fc9bc13ecba31d08ccaa9442077137960b66329785e46443c`  
		Last Modified: Wed, 11 Dec 2019 01:21:50 GMT  
		Size: 5.0 MB (4974605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c4b55641e7e1383fa4e862c0c84775701a6ec16b5798c5b40314eae00b0a41`  
		Last Modified: Wed, 11 Dec 2019 01:21:28 GMT  
		Size: 3.8 MB (3779861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d033a1b453e66df13cc14cd4b0641f7153534e35fec5e1ea7cce1929729c38f2`  
		Last Modified: Wed, 11 Dec 2019 01:21:26 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
