[![Netlify 状态](https://api.netlify.com/api/v1/badges/43142525-7095-45a7-928f-f304c211a54a/deploy-status)](https://app.netlify.com/sites/resume-cubxxw/deploys)

<p align="center">
    <a href="./README.md"><b>英文</b></a> •
    <a href="./README_zh-CN.md"><b>中文</b></a>
</p>

## 安装指南

* [克隆](https://github.com/cubxxw/resume/fork)此代码仓库；
* 进入设置并将 master 分支设置为 GitHub Pages 源；
* 您的新网站将可在 `https://<用户名>.github.io/resume/` 地址找到；
* 网站的可打印版本可在 `https://<用户名>.github.io/resume/print` 找到。使用第三方链接如 https://pdflayer.com/，https://www.web2pdfconvert.com/ 等来获取 PDF 版本。

从一个地方更改所有细节：`_data/data.yml`。

### 使用 Docker 本地预览/编辑

```sh
docker-compose up
```

使用 *docker-compose.yml* 文件创建一个容器，可以在 <http://localhost:4000> 访问。更改 *_data/data.yml* 后，内容会在一段时间后显示。

### 本地机器

* 将仓库克隆到您的电脑上

```bash
git clone https://github.com/cubxxw/resume.git
```

* 安装所需的 Ruby 宝石

```bash
bundle install
```

* 本地启动网站

```bash
bundle exec jekyll serve
```

* 访问 `http://localhost:4000`


## 使用 `_config.yml` 配置您的网站 🛠️

在 `_config.yml` 文件中，您可以配置 Jekyll 站点的核心方面。这个 YAML 文件是您站点设置的核心，定义了从基本设置到高级功能的一切。

以下是提供的配置选项的详细解释：

```yaml
# 通过编辑 _data 文件夹中的 data.yml 文件更新所有部分。

# 站点设置
title: 我的简历                   # 站点的标题
url: 'https://resume.nsddd.top'  # 站点的 URL

# 根据您的仓库名称进行更改
# 禁用，因为我们使用自定义域名
#baseurl: '/online-cv'           # 如果您的项目托管在子路径中的基本 URL

description: 一个美观的 Jekyll 主题，用于创建简历  # SEO 的描述
# 只有在重启构建或服务后才会应用样式。选择其中一个选项即可。
theme_skin: green               # 选择一个颜色主题：蓝色，绿松石，绿色，浆果，橙色，陶瓷
chrome_mobile_color:            # Chrome 移动搜索栏的 HEX 颜色 (例如，#1976d2)

# 跟踪器
analytics: UA-83979019-1        # Google Analytics 跟踪 ID

# Sass/SCSS
sass:
  sass_dir: _sass               # Sass 文件的目录
  style: compressed             # CSS 的输出样式：嵌套，展开，紧凑，压缩

# 构建设置
compress-site: yes              # 启用/禁用站点压缩

encoding: "utf-8"               # 字符编码标准
compress_html:                  # HTML 压缩设置
  clippings: all
  ignore:
    envs: development           # 在开发模式下忽略 HTML 压缩

# 开发设置
port: 4000                      # 本地运行 Jekyll 的端口号
host: 0.0.0.0                   # 本地运行时绑定的主机
safe: false                     # 禁用自定义插件，安全模式
```

在 `_config.yml` 文件中定义的配置字段是管理您的 Jekyll 站点各方面设置的关键部分。下面是这些字段的详细解释：

- **title（标题）**：这是您的网站显示的标题，它是站点身份和搜索引擎优化（SEO）的重要部分。
- **url（网址）**：您的网站的完整网址。如果您使用自定义域名，这将非常重要。
- **baseurl（基础网址）**：如果您的网站不是托管在域名的根目录下，而是一个子目录中，这里应该设置那个子目录的路径。这个字段通常在使用 GitHub Pages 时需要设置。

- **description（描述）**：这是一个简短的描述，用于改善您的网站在搜索引擎结果中的显示。它描述了您的网站或网页的主要内容和功能。
- **theme_skin（主题皮肤）**：允许您选择网站的颜色主题，以匹配您的个人或品牌风格。选项可能包括蓝色、绿松石、绿色等。
- **chrome_mobile_color（Chrome 移动颜色）**：设置 Android 设备上 Chrome 浏览器地址栏的颜色，这是一个 HEX（十六进制）颜色码。

- **analytics（分析）**：Google Analytics 的跟踪 ID，用于收集访问您站点的用户数据，帮助您分析访问者行为模式。

- **Sass/SCSS 配置**：
  - **sass_dir**：定义存放 Sass 文件的目录。
  - **style**：定义生成 CSS 的样式，如压缩（compressed），展开（expanded）等，影响 CSS 文件的最终大小和格式。

- **compress-site（站点压缩）**：这个选项允许您开启或关闭网站内容的压缩功能，可以减少传输数据量，提高加载速度。

- **encoding（编码）**：设置网站的字符编码，通常使用 "utf-8"，以支持国际字符集。

- **compress_html（HTML 压缩）**：HTML 压缩的详细设置，可以进一步优化站点性能。包括：
  - **clippings**：选择压缩的部分。
  - **ignore**：定义在哪些环境（如开发环境）中忽略 HTML 压缩。

- **Development Settings（开发设置）**：
  - **port**：定义运行 Jekyll 服务时使用的本地端口号。
  - **host**：定义运行服务时绑定的主机地址。
  - **safe**：当设置为 `true` 时，Jekyll 将在安全模式下运行，不加载任何自定义插件。
