# 📚 智慧课程表系统

[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](https://opensource.org/licenses/MIT)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)

一个现代化的在线课程表管理系统，采用玻璃态设计风格，集成验证码保护、侧边栏计算器等实用功能，为医学检验技术专业学生打造的智能课表查询工具。

[在线演示](#) | [报告问题](https://github.com/yourusername/smart-schedule/issues) | [功能建议](https://github.com/yourusername/smart-schedule/issues/new)

---

## ✨ 主要特性

### 🎨 现代化界面设计

- **玻璃态卡片** - 采用 Glassmorphism 设计风格
- **渐变背景** - 动态流动的渐变色背景
- **响应式布局** - 完美适配手机、平板和桌面端
- **平滑动画** - 流畅的交互动画效果
- **3D 悬停效果** - 卡片悬停时的立体效果

### 🔐 安全验证系统

- **数学验证码** - 集成中文数学验证码 API
- **虚拟键盘** - 自带数字输入键盘
- **自动重试** - 验证失败自动刷新验证码
- **调试模式** - 开发者可查看验证详情
- **防暴力破解** - 多次失败后需要重新加载

### 🧮 实用工具集成

- **侧边栏计算器** 
  - 完整的四则运算功能
  - 优雅的滑入滑出动画
  - 支持小数点运算
  - 退格和清空功能

### 📊 课表管理功能

- **多周次切换** - 支持查看不同周次的课表
- **今日高亮** - 自动标记今天是星期几
- **课程统计** - 实时显示今日/本周课程数量
- **教师信息** - 显示任课教师和上课地点
- **一键打印** - 支持打印课表功能

### 📢 通知与提醒

- **课程调整通知** - 显示临时课程变动
- **考试安排** - 展示期末考试时间表
- **重要事项** - 突出显示重要通知
- **动态更新** - 日期时间自动更新

---

## 🚀 快速开始

### 在线使用

1. 访问网站地址
2. 完成数学验证码验证
3. 进入课表查询界面
4. 选择周次查看课表

### 本地部署

1. **克隆仓库**
   ```bash
   git clone https://github.com/yourusername/smart-schedule.git
   cd smart-schedule
   ```

2. **打开文件**
   
   直接在浏览器中打开 `index.html` 文件即可使用。

3. **或使用本地服务器**（推荐）
   ```bash
   # 使用 Python
   python -m http.server 8000
   
   # 或使用 Node.js
   npx http-server
   
   # 或使用 PHP
   php -S localhost:8000
   ```
   
   然后访问 `http://localhost:8000`

---

## 📖 使用指南

### 验证码验证

1. **查看验证码**
   - 页面加载后自动显示数学验证码
   - 图片显示一个中文数学算式

2. **输入答案**
   - 使用虚拟键盘输入答案
   - 或使用实体键盘输入（移动端建议使用虚拟键盘）

3. **提交验证**
   - 点击"验证并进入"按钮
   - 验证成功后自动进入课表界面

4. **验证失败**
   - 显示错误提示
   - 自动清空输入框
   - 自动刷新新的验证码

5. **看不清楚**
   - 点击验证码图片或"看不清？换一张"链接
   - 立即加载新的验证码

### 侧边栏计算器

1. **打开计算器**
   - 点击右侧"🧮 计算器"按钮
   - 计算器面板从右侧滑入

2. **使用计算器**
   - 点击数字按钮输入数字
   - 点击运算符进行计算
   - 支持加减乘除和小数运算

3. **关闭计算器**
   - 点击计算器标题栏的 ✕ 按钮
   - 或再次点击"🧮 计算器"按钮

### 课表查询

1. **选择周次**
   - 点击"选择周次"下拉菜单
   - 选择想要查看的周次
   - 点击"查询课表"按钮

2. **查看课程**
   - 课程卡片显示：课程名称、教师、地点
   - 不同颜色标识不同类型课程
   - 今日课程自动高亮显示

3. **今日高亮**
   - 点击"今日高亮"按钮
   - 自动定位并高亮显示今天的课程

4. **打印课表**
   - 点击"打印"按钮
   - 进入打印预览
   - 可保存为 PDF 或直接打印

### 数据统计

- **今日课程**：显示今天的课程数量
- **本周课程**：显示本周总课程数
- **任课教师**：显示总教师人数

---

## 🎯 功能特点

### 验证码系统

- **API 集成**：使用 xxapi.cn 中文验证码服务
- **自动加载**：页面打开自动加载验证码
- **智能验证**：支持多种验证成功判断逻辑
- **错误处理**：完善的网络错误处理机制

### 课表数据结构

```javascript
scheduleData = {
  "周次标识": {
    "date_range": "日期范围",
    "schedule": {
      "星期一": {
        "上午1-2节": "课程名称",
        "上午3-4节": "课程名称",
        // ...
      },
      // ...
    }
  }
}
```

### 教师信息

```javascript
teachers = {
  "课程名称": "教师姓名",
  // ...
}
```

---

## 🛠️ 技术栈

### 前端技术
- **HTML5** - 语义化标签
- **CSS3** - 现代样式特性
  - Glassmorphism（玻璃态）
  - CSS Grid & Flexbox
  - CSS 动画与过渡
  - 渐变背景动画
- **JavaScript ES6+** - 原生 JavaScript

### 外部 API
- **验证码 API** - [xxapi.cn](https://xxapi.cn) 中文验证码服务

### 设计特色
- **Google Fonts** - Inter 字体
- **Material Design** - 设计灵感
- **Glassmorphism** - 玻璃态设计风格

---

## 📋 项目结构

```
smart-schedule/
│
├── index.html          # 主应用文件（单文件架构）
├── README.md           # 项目文档
├── LICENSE             # MIT 开源协议
└── screenshots/        # 截图目录（可选）
    ├── login.png
    ├── schedule.png
    └── calculator.png
```

---

## 🎨 自定义配置

### 修改主题颜色

可以通过修改 CSS 渐变背景来改变主题：

```css
body {
  background: linear-gradient(135deg, #a8e6cf 0%, #dcedc1 50%, #ffd3b6 100%);
}

/* 绿色主题（当前） */
.glass-card {
  background: rgba(255, 255, 255, 0.9);
  border: 1px solid rgba(255, 255, 255, 0.5);
}

/* 蓝色主题示例 */
body {
  background: linear-gradient(135deg, #667eea 0%, #764ba2 50%, #f093fb 100%);
}
```

### 修改课表数据

在 JavaScript 代码中找到 `scheduleData` 对象：

```javascript
const scheduleData = {
  "周次": {
    "date_range": "日期范围",
    "schedule": {
      // 在这里修改课程信息
    }
  }
};
```

### 修改教师信息

```javascript
const teachers = {
  "课程名称": "教师姓名",
  // 添加或修改教师信息
};
```

---

## 🔧 核心功能模块

### 1. 验证码模块

```javascript
// 加载验证码
async function loadCaptcha()

// 验证用户输入
async function verifyCaptcha()

// 虚拟键盘输入
function inputNumber(num)
```

### 2. 计算器模块

```javascript
// 切换计算器显示
function toggleCalculator()

// 计算器输入
function calcInput(value)

// 执行计算
function calcEquals()

// 清空计算器
function calcClear()
```

### 3. 课表模块

```javascript
// 渲染课表
function renderSchedule(weekKey)

// 高亮今日
function highlightToday()

// 更新日期显示
function updateCurrentDate()
```

---

## 📱 响应式设计

### 移动端优化

- 小于 768px 自动调整布局
- 触摸友好的按钮大小
- 虚拟键盘优化
- 侧边栏全屏显示

### 平板端

- 网格自动调整列数
- 保持良好的视觉效果
- 优化的触摸交互

### 桌面端

- 最大化利用屏幕空间
- 悬停效果增强体验
- 快捷键支持（未来）

---

## 🎓 适用场景

### 教育机构
- 大学课程表管理
- 中学课程安排
- 培训班课表

### 个人使用
- 学生查询课表
- 教师查看课程
- 家长了解孩子课程

### 企业培训
- 培训课程安排
- 会议室预定
- 活动日程管理

---

## 🤝 贡献指南

欢迎贡献代码、报告问题或提出建议！

### 贡献流程

1. Fork 本仓库
2. 创建特性分支 (`git checkout -b feature/AmazingFeature`)
3. 提交更改 (`git commit -m 'Add some AmazingFeature'`)
4. 推送到分支 (`git push origin feature/AmazingFeature`)
5. 开启 Pull Request

### 开发规范

- 保持代码风格一致
- 添加必要的中文注释
- 测试新功能的兼容性
- 更新相关文档
- 保持响应式设计

---

## 📋 待办事项

### 功能增强
- [ ] 添加课程提醒功能
- [ ] 支持自定义课表数据
- [ ] 实现课表导出功能（iCal、Excel）
- [ ] 添加课程笔记功能
- [ ] 支持多人课表对比
- [ ] 集成日历视图

### 界面优化
- [ ] 暗黑模式
- [ ] 更多主题选择
- [ ] 自定义颜色方案
- [ ] 桌面端快捷键
- [ ] 手势操作（移动端）

### 技术优化
- [ ] PWA 支持（离线使用）
- [ ] 数据本地缓存
- [ ] 后端 API 集成
- [ ] 用户系统
- [ ] 数据云端同步

---

## ⚠️ 注意事项

### 浏览器兼容性

- ✅ Chrome 90+
- ✅ Firefox 88+
- ✅ Safari 14+
- ✅ Edge 90+
- ⚠️ IE 11 不支持

### 验证码 API

- 依赖第三方 API 服务
- 需要稳定的网络连接
- API 可能有访问频率限制
- 建议部署时配置备用方案

### 数据安全

- 课表数据存储在前端代码中
- 不涉及用户隐私数据
- 验证码不存储用户信息
- 建议使用 HTTPS 部署

### 使用建议

1. **网络环境**
   - 确保网络连接稳定
   - 建议使用 Wi-Fi 或 4G/5G
   - API 服务可能在部分地区受限

2. **浏览器设置**
   - 允许 JavaScript 执行
   - 允许加载外部图片
   - 清除缓存后可能需重新验证

3. **数据更新**
   - 课表数据需手动更新代码
   - 建议每学期开始前更新
   - 及时同步课程调整信息

---

## 📄 开源协议

本项目采用 [MIT License](LICENSE) 开源协议。

```
MIT License

Copyright (c) 2025 Smart Schedule System

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.
```

---

## 🙏 致谢

- **xxapi.cn** - 提供中文验证码 API 服务
- **Google Fonts** - 提供 Inter 字体
- **Lorem Picsum** - 设计灵感来源
- 所有为项目提供反馈的用户和贡献者

---

## 📞 联系方式

- 作者: Your Name
- 邮箱: your.email@example.com
- GitHub: [@yourusername](https://github.com/yourusername)
- 问题反馈: [Issues](https://github.com/yourusername/smart-schedule/issues)

---

## 🌟 Star History

如果这个项目对你有帮助，请给它一个 ⭐ Star！

[![Star History Chart](https://api.star-history.com/svg?repos=yourusername/smart-schedule&type=Date)](https://star-history.com/#yourusername/smart-schedule&Date)

---

## 📸 界面预览

### 验证码界面
- 清新的绿色渐变背景
- 玻璃态卡片设计
- 虚拟数字键盘
- 自动刷新功能

### 课表主界面
- 现代化表格设计
- 今日课程高亮
- 3D 统计卡片
- 实时数据更新

### 侧边栏计算器
- 优雅的滑入动画
- 完整的计算功能
- 大按钮易操作
- 支持小数运算

---

## 💡 使用技巧

### 快速查询
1. 验证码输入完毕后按回车键（未来功能）
2. 使用"今日高亮"快速定位今天课程
3. 打印前先预览确认内容

### 数据管理
1. 定期更新课表数据
2. 备份重要的课程信息
3. 记录教师联系方式

### 性能优化
1. 定期清理浏览器缓存
2. 使用最新版本浏览器
3. 避免同时打开过多标签页

---

<div align="center">

**[⬆ 回到顶部](#-智慧课程表系统)**

Made with 💚 for Education

**让学习更有条理 | 让管理更加高效**

</div>
