## `hylang:0-python3.7-windowsservercore-ltsc2016`

```console
$ docker pull hylang@sha256:be6ca4e51ffc20f0d74ee4377675d21b5ffedd75c497db4b5b9de1befe555508
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.14393.3686; amd64

### `hylang:0-python3.7-windowsservercore-ltsc2016` - windows version 10.0.14393.3686; amd64

```console
$ docker pull hylang@sha256:238f44f8193f06990915d99362d73957ee3e1bbf6006201cf9ba4f471259eb7e
```

-	Docker Version: 18.09.11
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5804561444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4579be0225e57b60ab194a971e5fab33b628540a9f621326fb5a54d01752aa45`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Mon, 04 May 2020 15:24:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 13 May 2020 12:34:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 May 2020 15:09:58 GMT
ENV PYTHON_VERSION=3.7.7
# Wed, 13 May 2020 15:09:59 GMT
ENV PYTHON_RELEASE=3.7.7
# Wed, 13 May 2020 15:12:23 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	Start-Process python.exe -Wait 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 		Write-Host 'Complete.'
# Wed, 13 May 2020 15:12:25 GMT
ENV PYTHON_PIP_VERSION=20.1
# Wed, 13 May 2020 15:12:26 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/1fe530e9e3d800be94e04f6428460fc4fb94f5a9/get-pip.py
# Wed, 13 May 2020 15:12:27 GMT
ENV PYTHON_GET_PIP_SHA256=ce486cddac44e99496a702aa5c06c5028414ef48fdfd5242cd2fe559b13d4348
# Wed, 13 May 2020 15:14:07 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 13 May 2020 15:14:09 GMT
CMD ["python"]
# Wed, 13 May 2020 21:26:53 GMT
ENV HY_VERSION=0.18.0
# Wed, 13 May 2020 21:28:25 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 13 May 2020 21:28:26 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:b940e70a4619b357d89f3dcabf4ac263d1efc65e1ef3af64cb0e8fbeaccc64dd`  
		Size: 1.7 GB (1661903967 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e3e9730c43354781e87aa51e853bff3b1e8c1ca7004f527139638a8f9d499c49`  
		Last Modified: Wed, 13 May 2020 12:59:27 GMT  
		Size: 1.2 KB (1151 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26503d42ff8b128026bc1e72726e8b1cffb43850f533c063dc5cba2c8c990b3b`  
		Last Modified: Wed, 13 May 2020 15:20:14 GMT  
		Size: 1.1 KB (1128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0efe71f3b91733bb1cab3310144ba8508043fbe42b88153ed4fe60d1f0e5176`  
		Last Modified: Wed, 13 May 2020 15:20:13 GMT  
		Size: 1.1 KB (1146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2878cd24a46ab0833ba402ea28de6794c88c8ff1cf26c10b7dacdfed52515c8a`  
		Last Modified: Wed, 13 May 2020 15:20:23 GMT  
		Size: 56.0 MB (56048471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83706cb85c07982b691baf5c62fc4ed1c0c7a2eec2e2fb25662d2534ae66c9de`  
		Last Modified: Wed, 13 May 2020 15:20:10 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e705f010295f9060567b65598d3249479e2f6262621cfa4b34b6cb348cc79aaa`  
		Last Modified: Wed, 13 May 2020 15:20:10 GMT  
		Size: 1.2 KB (1187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d98f23c59cfeaad076bb1f39a15fda0696ccf091ebed2051601bf038c81b059b`  
		Last Modified: Wed, 13 May 2020 15:20:09 GMT  
		Size: 1.1 KB (1130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52a947c6e6ca699c5a00b81af1f200d9831669b3c9ac2267d3263758aa357ed`  
		Last Modified: Wed, 13 May 2020 15:20:12 GMT  
		Size: 10.5 MB (10474792 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6540521279bedbd15b613ea5ebf255172c17f2a388e04eae54b91ae4de18b9d8`  
		Last Modified: Wed, 13 May 2020 15:20:10 GMT  
		Size: 1.1 KB (1124 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65380bb31d239bab254eaf5c3014362deca523bd56237798c53d7cc5b395dea5`  
		Last Modified: Wed, 13 May 2020 21:30:38 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fece3643cea85fda19471e8bdbf7a787e34e79f1f23466eff48d3aeea283bc03`  
		Last Modified: Wed, 13 May 2020 21:30:39 GMT  
		Size: 6.1 MB (6138024 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9de9d67478dfac2bd974823f368d8c311ecf55c64cd3f89a2043249b7dd4cc00`  
		Last Modified: Wed, 13 May 2020 21:30:38 GMT  
		Size: 1.1 KB (1150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
