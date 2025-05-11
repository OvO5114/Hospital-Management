
计科2205班黄建霖2205308050352
🏥 Doctors Component
展示医生信息列表的 React 组件，支持搜索、查看详情及预约功能。适用于医疗类 Web 应用程序中的医生展示页面。

📸 预览图（可选）
你可以在此处插入一张组件渲染后的截图或 GIF 动画，展示医生卡片布局、搜索框和模态框效果。

🧩 功能特性
✅ 展示医生头像、姓名、专长等基本信息
🔍 支持按姓名或专长进行模糊搜索
📄 点击医生卡片或信息按钮（"i"）弹出详细信息模态框
📅 提供“预约”按钮跳转至预约页面并携带医生 ID 参数
🎨 使用 Tailwind CSS 构建响应式 UI
🎞️ 使用 framer-motion 添加按钮悬停动画


🛠 技术栈
技术	版本/用途
React	核心框架
React Router DOM	页面导航
Framer Motion	按钮动画
Font Awesome Icons	图标库
Tailwind CSS	样式设计
📁 文件结构

src/
├── components/
│   └── Doctors.jsx        # 医生列表主组件
│   └── DoctorProfile.jsx  # （未实际使用）医生详情模态框组件（建议封装后使用）
📦 Props 说明
该组件接收一个 doctors 的 prop，数据格式如下：

Js

[
  {
    id: 1,
    name: "Dr. John Smith",
    specialty: "Cardiology",
    image: "https://example.com/dr-john.jpg",
    experience: 10,
    patients: 1200,
    bio: "Experienced cardiologist with a focus on heart health..."
  },
  // 更多医生...
]

🔧 使用说明：
安装依赖
确保你的项目中已安装以下依赖：

Bash

npm install react-router-dom framer-motion @fortawesome/react-fontawesome
同时确保已配置 Tailwind CSS。

示例调用
Jsx
import Doctors from './Doctors';

function App() {
  const doctors = [
    {
      id: 1,
      name: 'Dr. Alice Chen',
      specialty: 'Dermatology',
      image: 'doctor1.jpg',
      experience: 8,
      patients: 950,
      bio: 'Skin care expert with over 8 years of experience.'
    }
  ];

  return <Doctors doctors={doctors} />;
}
📲 页面跳转逻辑
点击“预约”按钮后，会跳转到 /appointments 页面，并在 URL 中携带医生 ID：

Text
/appointments?doctorId=1
💡 可扩展性建议
✅ 将模态框部分提取为独立组件 DoctorModal，提高复用性
🔄 增加加载状态与错误处理（如从 API 获取医生数据时）
📱 添加移动端适配样式优化
🔍 支持更多搜索条件（如科室、医院等）
📚 License
MIT License - see the LICENSE file for details.




🏥Patients Component
这是一个使用 React、Framer Motion 和 Axios 构建的简单而优雅的患者管理界面，适用于医疗或诊所环境中的患者记录管理。

此组件提供了清晰的用户界面来：

查看患者列表
添加新患者并进行验证
根据姓名搜索患者
删除现有患者

🧩 功能特点
功能	描述
✅ 查看患者	以响应式网格卡片显示患者的列表。
✅ 添加新患者	表单用于注册新患者，并包含验证功能。
✅ 搜索功能	实时根据姓名过滤患者。
✅ 删除患者	通过API调用删除患者。
⚠️ 编辑患者	占位符存在；尚未实现该功能。
🎨 响应式设计	使用TailwindCSS实现移动端友好的布局。
🎞️ 动画效果	Framer Motion支持平滑过渡和悬停效果。
🛠️ 使用的技术
React – 组件化的UI库
Framer Motion – 用于动画和交互
Tailwind CSS – 实用优先的样式框架
Axios – HTTP客户端用于API请求
React Icons – 图标库（如FaUserPlus, FaSearch等）
📁 文件结构

src/
└── components/
    └── Patients.jsx       # 主组件文件
📦 依赖项
确保安装了以下包：

Bash

npm install react react-dom axios framer-motion @react-icons/all-files
或者使用yarn:

Bash

yarn add react react-dom axios framer-motion @react-icons/all-files
🔧 后端API端点（假设）
组件期望有以下后端API：

方法	端点	目的
GET	/api/patients/get-patients	获取所有患者
POST	/api/patients/register	注册新患者
POST	/api/patients/delete-patient	根据ID删除患者
根据你的后端设置，可能需要配置Axios的基础URL或代理设置。

📋 使用示例
要使用此组件，只需将其导入并在应用程序中渲染即可：

Jsx

import Patients from "./components/Patients";

function App() {
  return (
    <div>
      <Patients />
    </div>
  );
}

export default App;

🧪 验证规则
姓名: 至少4个字符长，必须以字母开头。
手机号码: 必须遵循类似1234567890的格式（10位数字）。
邮箱: 必填字段。
性别: 必选选项。
年龄: 必填数字输入。
🧹 待办事项 / 未来改进
 实现编辑患者的功能
 在删除前添加确认对话框
 使用Formik或React Hook Form进行更好的表单处理
 在API调用期间显示加载指示器
 对于大数据集实现分页
 添加用户角色和权限
 显示成功/错误提示通知而不是警告框
📜 许可
MIT License - 详情请参阅LICENSE文件。




🏥 Health Nest - Admin Dashboard
一个基于 React 的简单医院管理员仪表盘页面，支持登录验证、数据展示和 PDF 报告生成功能。

📝 简介
该项目是一个前端管理后台界面，主要面向医院管理系统中的管理员用户，提供了以下核心功能：

✅ 登录验证（用户名 + 密码）
📊 数据统计面板展示
📄 PDF 报告生成
🎨 动态交互与动画效果
🧰 技术栈
技术	用途
React	前端框架
jsPDF	PDF 文档生成
Framer Motion	动画交互
React Icons (Font Awesome)	图标库
Tailwind CSS（类名使用）	样式设计（需额外引入）
🔐 登录系统
默认用户名：admin
默认密码：password
登录逻辑
Jsx

if (username === 'admin' && password === 'password') {
    setIsLoggedIn(true);
} else {
    alert('Invalid credentials');
}
⚠️ 当前为静态验证，建议在实际项目中接入 API 认证服务。

📊 数据统计面板
显示以下关键指标：

指标	数值
医生数量	50
患者数量	1000
预约总数	1500
收入金额	$500,000
每个卡片都带有图标和颜色标识，并通过 Framer Motion 实现了悬停放大和点击缩放的交互效果。

📄 PDF 报告生成功能
点击按钮后会自动生成并下载一份包含统计数据的 PDF 文件，文件名为：


hospital_report.pdf
报告内容包括：

医院名称
生成时间
各项统计数据
💅 UI 设计与交互
使用 Grid 布局实现响应式设计。
登录表单居中显示，提升用户体验。
卡片和按钮添加了动画交互，增强视觉反馈。
所有样式使用 Tailwind CSS 类名（需引入 Tailwind 才能生效）。
🛠️ 安装与运行
确保你已安装 Node.js 和 npm。

1. 安装依赖
Bash

npm install
2. 安装所需库（如未安装）
Bash

npm install react react-dom
npm install jspdf
npm install framer-motion
npm install @react-icons/all-files
3. 启动开发服务器
Bash

npm start
📁 项目结构

src/
├── components/
│   └── Admin.jsx      # 主组件
├── App.jsx              # 应用入口
├── index.jsx            # 渲染入口
└── styles/              # 可选样式文件
🚀 后续优化建议
接入真实后端接口获取动态数据
添加权限控制和角色管理
使用图表库（如 ECharts、Recharts）可视化数据
实现多语言支持
增加更多管理模块（如医生管理、患者管理、预约记录等）
📬 联系我
如有任何问题或建议，请随时联系！

📧 Email: your-email@example.com

💻 GitHub: [your-github-url]

📜 开源许可
MIT License © [Your Name]
