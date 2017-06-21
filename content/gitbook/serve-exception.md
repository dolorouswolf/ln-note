异常： `Error: ENOENT: no such file or directory, stat`

>编辑 ~/.gitbook/versions/3.2.2/lib/output/website/copyPluginAssets.js
>将最后的fs.copyDir中的confirm改为false

	logger.debug.ln('copy resources from plugin', assetsFolder);
	
	return fs.copyDir(
		assetsFolder,
		assetOutputFolder,
		{
			deleteFirst: false,
            overwrite: true,
			confirm: false
		}
	);
	
