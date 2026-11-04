# 薪情不错 · 日工资进度

一个纯前端的实时日工资进度显示器。输入日工资、上下班和午休时间后，页面会按秒显示今天已赚金额、工作进度和下班倒计时。

## 本地预览

项目无需安装依赖。进入项目目录后运行：

```bash
python3 -m http.server 8080 --directory dist
```

然后访问 `http://localhost:8080`。

## 部署到服务器

### 方式一：Nginx

将 `dist/` 目录中的文件复制到 Nginx 的站点目录，例如：

```bash
sudo cp -R dist/* /var/www/html/
```

### 方式二：Docker

```bash
docker build -t daily-wage-progress .
docker run -d --name daily-wage-progress -p 8080:80 daily-wage-progress
```

访问 `http://服务器地址:8080` 即可。

## 数据说明

工资和工作时间只保存在浏览器的 `localStorage` 中，不会上传到服务器。
