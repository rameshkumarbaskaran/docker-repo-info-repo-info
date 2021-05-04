## `python:rc-windowsservercore`

```console
$ docker pull python@sha256:50943dd525438a587e8bf1a41781db39ff270432906ee93f0b6984ea31ef0d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1879; amd64
	-	windows version 10.0.14393.4350; amd64

### `python:rc-windowsservercore` - windows version 10.0.17763.1879; amd64

```console
$ docker pull python@sha256:77cf55712d3c9dc90cdcc13ce6672fb5625d7cbd0dc7216aed83d535378cebe8
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 GB (2527318285 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b25db0613fc265868bc1afd67ebc808429bd82b7a9b55fc554f5aec7b279204`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 09 Apr 2021 20:34:41 GMT
RUN Install update 1809-amd64
# Wed, 14 Apr 2021 12:09:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 12:14:23 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 14 Apr 2021 16:12:03 GMT
ENV PYTHON_VERSION=3.10.0a7
# Wed, 14 Apr 2021 16:12:05 GMT
ENV PYTHON_RELEASE=3.10.0
# Wed, 14 Apr 2021 16:14:03 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Mon, 03 May 2021 21:15:20 GMT
ENV PYTHON_PIP_VERSION=21.1.1
# Mon, 03 May 2021 21:15:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1954f15b3f102ace496a34a013ea76b061535bd2/public/get-pip.py
# Mon, 03 May 2021 21:15:22 GMT
ENV PYTHON_GET_PIP_SHA256=f499d76e0149a673fb8246d88e116db589afbd291739bd84f2cd9a7bca7b6993
# Mon, 03 May 2021 21:16:23 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Mon, 03 May 2021 21:16:24 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:399f118dfaa9a753e98d128238b944432c7bcabea88a2998a6efbbece28ed303`  
		Size: 751.4 MB (751421005 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:106dbf3373fce4f0ba5e00ad54824c597f2894605fa7d8ef446ad7ea3b97449f`  
		Last Modified: Wed, 14 Apr 2021 12:58:04 GMT  
		Size: 1.4 KB (1413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bc61c4265bfe314fb772d57da4c3023d46cacdbdab9bb6fd5c475f11696dbab`  
		Last Modified: Wed, 14 Apr 2021 16:38:19 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26dd937ed415aed6d7b55658d64c0e64b6c00fabc9149cdcf5f46807a0badf6`  
		Last Modified: Wed, 14 Apr 2021 16:38:18 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b30c610741e32638ad88b3a931d9dba27429d342f46764e0c15547f009758783`  
		Last Modified: Wed, 14 Apr 2021 16:38:18 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89eb0760941830a6e773c8ee0bbbe78705e8c0996304aad223f690e8772ff4f8`  
		Last Modified: Wed, 14 Apr 2021 16:39:21 GMT  
		Size: 51.3 MB (51252865 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a2cdb0921377b0723b913a9dbac151fc0d7bb026626b601fcf11b99bf00878a`  
		Last Modified: Mon, 03 May 2021 21:25:32 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b85a2f33c8050e616c34ba6bf1efa7778df511e5fe39d0248cb0557ab93e4f`  
		Last Modified: Mon, 03 May 2021 21:25:32 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:131d47dca43df714f01cb796c83e3f3e565d921a66f3fa4966b76c93c1b71de6`  
		Last Modified: Mon, 03 May 2021 21:25:32 GMT  
		Size: 1.4 KB (1408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e18f4a0df0443ce26eef052acfe81e54eb2df3c36752cea4148db60b5921332`  
		Last Modified: Mon, 03 May 2021 21:25:34 GMT  
		Size: 6.3 MB (6300308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca7774078acbe355a2fd56f986567e56dd641e80f0e9d0b32f8cd530bc422d90`  
		Last Modified: Mon, 03 May 2021 21:25:32 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:rc-windowsservercore` - windows version 10.0.14393.4350; amd64

```console
$ docker pull python@sha256:64f9b7d29b6282246d0343d07c0186124fb2aae1cfea67168a63fd065f67c2a0
```

-	Docker Version: 19.03.5
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.9 GB (5862704696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f418dbef8db58fa80552c720a65bc18e8719fcf92d9eb94b6531a74cc23c6b5`
-	Default Command: `["python"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 07 Apr 2021 21:54:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 14 Apr 2021 12:35:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 Apr 2021 16:15:18 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 14 Apr 2021 16:15:19 GMT
ENV PYTHON_VERSION=3.10.0a7
# Wed, 14 Apr 2021 16:15:20 GMT
ENV PYTHON_RELEASE=3.10.0
# Wed, 14 Apr 2021 16:18:14 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Mon, 03 May 2021 21:16:33 GMT
ENV PYTHON_PIP_VERSION=21.1.1
# Mon, 03 May 2021 21:16:34 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1954f15b3f102ace496a34a013ea76b061535bd2/public/get-pip.py
# Mon, 03 May 2021 21:16:35 GMT
ENV PYTHON_GET_PIP_SHA256=f499d76e0149a673fb8246d88e116db589afbd291739bd84f2cd9a7bca7b6993
# Mon, 03 May 2021 21:18:32 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Mon, 03 May 2021 21:18:33 GMT
CMD ["python"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:00b4edb823e6a375d179a28cbfa682c2379d62179e1518485902d6e68b9a9d1e`  
		Size: 1.7 GB (1724897968 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:bb52885e05952959b0fa7aaff23561fcf14d294aed336112b388c94e67709e4f`  
		Last Modified: Wed, 14 Apr 2021 12:59:14 GMT  
		Size: 1.4 KB (1406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32b4598ab88dab64b25b4257872564af9825cc6cd41fc8cc1ad11c32958d0da9`  
		Last Modified: Wed, 14 Apr 2021 16:39:38 GMT  
		Size: 1.4 KB (1412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1311eb2840794f0fcf4ebfe6e57fefbd0bd92a00118e655c18e3a75392e4cd54`  
		Last Modified: Wed, 14 Apr 2021 16:39:41 GMT  
		Size: 1.4 KB (1435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b09619313575c6e229a1fa5368aca94a22dbcb2460d205d2df906d7985431214`  
		Last Modified: Wed, 14 Apr 2021 16:39:42 GMT  
		Size: 1.4 KB (1402 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:208f3c11f1d3691183615afa032ff11a8bad281acb95472f389252c31370c0df`  
		Last Modified: Wed, 14 Apr 2021 16:39:50 GMT  
		Size: 56.3 MB (56263121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8828fa9484b645a9026c68952fb4f0d3621507d110a58a835db9d393c2b5622`  
		Last Modified: Mon, 03 May 2021 21:25:47 GMT  
		Size: 1.4 KB (1352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b28ba45b77a41a684ef6ea8eb1a5ddbb912e1bc449e58eefbcb282d79f786965`  
		Last Modified: Mon, 03 May 2021 21:25:47 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8524a002976dd73c26d8abf6dc986cebccff1f519f99e1bf731e48b0740c81af`  
		Last Modified: Mon, 03 May 2021 21:25:47 GMT  
		Size: 1.4 KB (1365 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ec25afe62e213df3b8e0612d56e0990a1e04554dabac87b1fc66efa67ed7a1`  
		Last Modified: Mon, 03 May 2021 21:25:50 GMT  
		Size: 11.5 MB (11546563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:017f48b151dab5a7efe90111b51bdd98f4abfe65054dff1e3ab03b6fda29a9bc`  
		Last Modified: Mon, 03 May 2021 21:25:47 GMT  
		Size: 1.4 KB (1382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
