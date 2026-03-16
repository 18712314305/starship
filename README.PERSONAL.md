# starship 的 fork 仓库

## 说明
在这里更新和维护 配置和日志文档


## 个性化方案
在仓库中新增了两个目录
    - local.logs: 记录各设备使用 starship 的错误/警告日志, 每台独立设备独立一个子目录
        - myEdge: z890 刀锋钛

    - local.configs: 记录各设备的个性化配置, 每台设备独立一个子目录
        - myEdge: z890 刀锋钛
            - starship.init.toml: 初次下载 starship 尝试初始化配置


## 维护说明
1. 每一台新设备首次部署 starship 时, clone 该仓库到本地
2. 在上述两个个性化目录中, 新建该新设备的子目录, 
3. 若采用其他设备上现有的配置文件, 软链接到新设备子目录中
4. 将新设备要采用的配置文件, 软链接到 `$HOME/.config/starship.toml` 文件, 注意是文件不是目录!!!
4. 在 .zshrc(或其他 shell 配置文件)中, 修改日志存放目录, 添加命令如: `export STARSHIP_CACHE=$HOME/git.repo/starship/local.logs/myEdge` (即新建的设备日志目录在新设备上的实际路径)