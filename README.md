# 基于若依管理系统的终端机系统前端ui
项目为前端UI，后台可直接使用若依的后台项目，部署方式相同，只需把前端的vue项目更换使用本项目即可

## 开发

```bash
# 克隆项目
git clone https://github.com/fenghuijiuzhuan/RuoYi-terminal.git

# 进入项目目录
cd RuoYi-terminal

# 安装依赖
npm install

# 建议不要直接使用 cnpm 安装依赖，会有各种诡异的 bug。可以通过如下操作解决 npm 下载速度慢的问题
npm install --registry=https://registry.npm.taobao.org

# 启动服务
npm run dev
```

浏览器访问 http://localhost:80

## 发布

```bash
# 构建测试环境
npm run build:stage

# 构建生产环境
npm run build:prod
```
