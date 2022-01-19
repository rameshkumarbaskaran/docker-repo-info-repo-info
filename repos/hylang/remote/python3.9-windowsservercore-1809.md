## `hylang:python3.9-windowsservercore-1809`

```console
$ docker pull hylang@sha256:43a5fef8aa28f16f593cdfb55f42e44663ff9beac2ac3c87e092c8e7d9d09ebb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	windows version 10.0.17763.2452; amd64

### `hylang:python3.9-windowsservercore-1809` - windows version 10.0.17763.2452; amd64

```console
$ docker pull hylang@sha256:c06230c53c52b4781833e8d562fb8898428b7ba02e5a55fbbb5de37b0486634a
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.8 GB (2769306323 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d0fe2845198ee3ee2ac2670f0bffc4a4b13d89c61321243662075aaaea714f`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 07 Jan 2022 22:48:13 GMT
RUN Install update 1809-amd64
# Wed, 12 Jan 2022 05:11:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Jan 2022 06:13:45 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 19 Jan 2022 17:43:57 GMT
ENV PYTHON_VERSION=3.9.10
# Wed, 19 Jan 2022 17:43:58 GMT
ENV PYTHON_RELEASE=3.9.10
# Wed, 19 Jan 2022 17:46:00 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 19 Jan 2022 17:46:02 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Wed, 19 Jan 2022 17:46:03 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Wed, 19 Jan 2022 17:46:05 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3cb8888cc2869620f57d5d2da64da38f516078c7/public/get-pip.py
# Wed, 19 Jan 2022 17:46:06 GMT
ENV PYTHON_GET_PIP_SHA256=c518250e91a70d7b20cceb15272209a4ded2a0c263ae5776f129e0d9b5674309
# Wed, 19 Jan 2022 17:47:38 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 		('setuptools=={0}' -f $env:PYTHON_SETUPTOOLS_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 19 Jan 2022 17:47:40 GMT
CMD ["python"]
# Wed, 19 Jan 2022 18:13:06 GMT
ENV HY_VERSION=1.0a4
# Wed, 19 Jan 2022 18:13:07 GMT
ENV HYRULE_VERSION=0.1
# Wed, 19 Jan 2022 18:14:19 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 19 Jan 2022 18:14:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:635f15ebd5b486e8a00bf217a0574a29550e5bbf08c1d021e1e308100b2e49b5`  
		Size: 993.9 MB (993898043 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3a70d5fd54e2005efbf590b48700ed40509210354a0d8f3f18c3b444a5325896`  
		Last Modified: Wed, 12 Jan 2022 06:20:33 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ec0edebd1ddbb9c1b3b254bb09452f2077c1a30226af03c61c009222a6c5c1`  
		Last Modified: Wed, 12 Jan 2022 06:21:32 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e658fe72a615e91dfb6d7e7dad93e2bca9446fa910af922e45ace5a272aa5b6f`  
		Last Modified: Wed, 19 Jan 2022 17:53:33 GMT  
		Size: 1.4 KB (1401 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ecc48ba26fc692bad88594733f016e138b28cd4b0907ab34b537e2e99b3a7a`  
		Last Modified: Wed, 19 Jan 2022 17:53:33 GMT  
		Size: 1.4 KB (1397 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ea2208e073314c40ce748d84f8319a9727dea587d29b8cda656dea6a6d70b1d`  
		Last Modified: Wed, 19 Jan 2022 17:54:26 GMT  
		Size: 49.8 MB (49803380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa30ea246aef2e269adb3111797c01418c79afaf8beb00a7d05aeb8e9950797`  
		Last Modified: Wed, 19 Jan 2022 17:53:33 GMT  
		Size: 1.4 KB (1427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2cfa2cf7cdacacfc230d5d7047c863b52039bf9c9affac6e2e467d5e86f34bd`  
		Last Modified: Wed, 19 Jan 2022 17:53:31 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef90f17277f2150c2b3d03974eefc54f15b0c0bf13a3265cdc5081618582e290`  
		Last Modified: Wed, 19 Jan 2022 17:53:31 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48e02d297fbbda684a34f18fd15146567d6d9db9d55b1443940c10b814c4028c`  
		Last Modified: Wed, 19 Jan 2022 17:53:31 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa4ef3ead7cdef9b4940dad556b52a2ffe90148f58b048b24cce2d6785c7669e`  
		Last Modified: Wed, 19 Jan 2022 17:53:33 GMT  
		Size: 6.3 MB (6305798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc907d639d8d725d041c87eb8694f58ff7ce5cd813ce1eb3eaa82dd06408ea64`  
		Last Modified: Wed, 19 Jan 2022 17:53:31 GMT  
		Size: 1.4 KB (1439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab1eae193800b951745360ed39ea042b585a93146a93ef5af891d1eb92e20b0`  
		Last Modified: Wed, 19 Jan 2022 18:15:23 GMT  
		Size: 1.4 KB (1420 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc502bd13f8f6b9d345b2fe8995f926997853cf5675a48a6280197bff4ff6cbd`  
		Last Modified: Wed, 19 Jan 2022 18:15:23 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee8d5479c55aa8d21da3bf4dc3ab23e4d99b7ae707f7e9bd8fe1173aff4eb55f`  
		Last Modified: Wed, 19 Jan 2022 18:15:24 GMT  
		Size: 949.2 KB (949244 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cdcdfe988192357d3ac4baed9db27a740efea147eb12c888fc969a660c6c48a`  
		Last Modified: Wed, 19 Jan 2022 18:15:23 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
