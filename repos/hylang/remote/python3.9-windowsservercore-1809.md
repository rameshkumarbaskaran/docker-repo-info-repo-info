## `hylang:python3.9-windowsservercore-1809`

```console
$ docker pull hylang@sha256:a2933b37e0d75b96cede37203228078afd150621fe30f110d3f83dbf16948c75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	windows version 10.0.17763.1999; amd64

### `hylang:python3.9-windowsservercore-1809` - windows version 10.0.17763.1999; amd64

```console
$ docker pull hylang@sha256:67f0ad61f71655f9dbd2c32aa0e018905fc4f162b94ef68dbe980bada49f1cfc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2698692015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de828d8350a72092f492594702f60518154f90647f404a9e09cdd9db85b85dda`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Sun, 06 Jun 2021 04:28:43 GMT
RUN Install update 1809-amd64
# Wed, 09 Jun 2021 12:10:31 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 09 Jun 2021 12:15:45 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 09 Jun 2021 16:09:32 GMT
ENV PYTHON_VERSION=3.9.5
# Wed, 09 Jun 2021 16:09:34 GMT
ENV PYTHON_RELEASE=3.9.5
# Wed, 09 Jun 2021 16:11:07 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=0', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		Write-Host 'Complete.'
# Wed, 09 Jun 2021 16:11:10 GMT
ENV PYTHON_PIP_VERSION=21.1.2
# Wed, 09 Jun 2021 16:11:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/936e08ce004d0b2fae8952c50f7ccce1bc578ce5/public/get-pip.py
# Wed, 09 Jun 2021 16:11:15 GMT
ENV PYTHON_GET_PIP_SHA256=8890955d56a8262348470a76dc432825f61a84a54e2985a86cd520f656a6e220
# Wed, 09 Jun 2021 16:12:11 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 09 Jun 2021 16:12:14 GMT
CMD ["python"]
# Wed, 09 Jun 2021 16:30:55 GMT
ENV HY_VERSION=1.0a1
# Wed, 09 Jun 2021 16:31:39 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 09 Jun 2021 16:31:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:639bb6bb2beb4cfdcacb9f0844344448fe26494665d5fe78a494419f86fbb18f`  
		Size: 923.3 MB (923252167 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:7863ef96846d497ea06fe442ea13dcecaf5c248ce238c69800475281a4fa848e`  
		Last Modified: Wed, 09 Jun 2021 12:20:41 GMT  
		Size: 1.4 KB (1431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5789912c867ed5d9d277acf797c2a9373efb14a0496fb5ec7fce90fb3907d5b7`  
		Last Modified: Wed, 09 Jun 2021 12:21:19 GMT  
		Size: 1.4 KB (1393 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c2825160f2400387323106e3da106c44eb478e5e3ba96bbcd5305f8f4bc921d`  
		Last Modified: Wed, 09 Jun 2021 16:26:44 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53b9db3e1030a7cd33dd50ee8c5a44783be2f03c7f0021e7138d294b76c82485`  
		Last Modified: Wed, 09 Jun 2021 16:26:44 GMT  
		Size: 1.4 KB (1421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ee8ffd3e9bbe844d1490a7a32f916f182ac06a2101983de626dfd6ff329d581`  
		Last Modified: Wed, 09 Jun 2021 16:27:42 GMT  
		Size: 49.7 MB (49653807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4606f5b0ad6e2dc648bcd05daf0e18cd2587338d67a4756cea4d8b25285792d`  
		Last Modified: Wed, 09 Jun 2021 16:26:41 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d116b7ce60af860319df936e93e22abbb1b687888cbdd80e68c4ec99895963`  
		Last Modified: Wed, 09 Jun 2021 16:26:41 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a022d5cc971008b79c567d6c7b39ee294ffea0e00d51b398391ce8409d3155aa`  
		Last Modified: Wed, 09 Jun 2021 16:26:41 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674d44b67cbb52a9e5b516b6a1247285176c8ebfd646b7b8414b4bf0a98dce86`  
		Last Modified: Wed, 09 Jun 2021 16:26:48 GMT  
		Size: 6.3 MB (6263839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8c37dc4a717b87c004a879caebf56a988771d3e6153c2be717e13aadcdc05b6`  
		Last Modified: Wed, 09 Jun 2021 16:26:41 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43ea3340f8cb4be330f8fcdc108a18a3ab2840e9292b416e1a2218f34f2bfedd`  
		Last Modified: Wed, 09 Jun 2021 16:42:01 GMT  
		Size: 1.4 KB (1432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2a85b4838796446332597781c5279f055b2aea135e749f578fa482b7d2fd6b4`  
		Last Modified: Wed, 09 Jun 2021 16:42:02 GMT  
		Size: 1.2 MB (1175168 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebab5b6b9bb0df9f09323acad6785b877f25c4e69fa89046a72f6585653433fd`  
		Last Modified: Wed, 09 Jun 2021 16:42:01 GMT  
		Size: 1.4 KB (1422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
