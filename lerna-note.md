# lerna 常用命令

1. lerna bootstrap  
    把所有包安装到根node_modules

2. lerna add package[@version] [--dev] [--exact] [--peer]
    --dev 将新包添加到devDependencies而不是dependencies.
    --exact 添加具有确切版本（例如1.0.1）而不是默认^semver 范围（例如^1.0.1）的新包。
    --peer 将新包添加到peerDependencies而不是dependencies.

3. lerna add module-1 packages/prefix-*
    将 module-1 包添加到 'prefix-' 前缀文件夹中的包中

4. lerna add module-1 --scope=module-2
    将模块 1 安装到模块 2

5. lerna add module-1 --scope=module-2 --dev
    在 devDependencies 中将 module-1 安装到 module-2

6. lerna add module-1 --scope=module-2 --peer
    在 peerDependencies 中安装 module-1 到 module-2

7. lerna add module-1
    在除module-1之外的所有模块中安装module-1

8. lerna add babel-core
   在所有模块中安装 babel-core