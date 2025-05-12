<div align="center">
<img src="https://readme-typing-svg.herokuapp.com?color=FFB13C&size=50&width=1000&height=80&lines=Welcome-to-Hospital-Management-App"/>
</div>

# HealthHub - Advanced Hospital Management System

HealthHub 是一个基于 React 的综合医院管理系统，旨在简化医疗保健运营并改善患者护理。 运用JavaScript（ES6+）、HTML5、CSS3 、Font Awesome图标技术构建的综合医院管理系统， 具备用户友好的响应式界面，可进行预约管理、维护患者记录、管理医生信息，设有管理工具。 其页面含主页、预约、患者、医生、管理员页，在部署方面，后端部署于 https://hospital-management-server-zeta.vercel.app/ 。 对于想要安装使用该系统的用户，具体步骤如下： 1、克隆仓库：使用命令  git clone https://github.com/yazdanhaider/Hospital-Management.git  ，将项目仓库克隆到本地，获取系统的源代码。 2、导航至项目目录：在命令行中输入  cd Hospital-Management  ，进入项目所在的目录，为后续操作做好准备。 3、安装依赖项：执行  npm i  命令，自动安装项目运行所需的各类依赖包，确保系统功能的完整性。 4、运行开发服务器：通过  npm run dev  启动开发服务器，使系统能够在本地环境中正常运行，方便进行调试和测试。 在实际使用过程中，用户可以通过顶部导航栏轻松浏览系统的不同部分，快速定位到所需功能模块； 使用预约表单进行新预约的安排，操作流程简洁明了； 在患者管理部分，对患者记录进行添加、编辑、删除等操作，实现患者信息的动态管理； 在医生信息部分，查看和管理医生的相关资料，合理安排医疗人员工作； 管理员可以使用 “admin” 作为用户名和密码登录 Admin 面板，访问管理功能，进行系统的高级管理操作。
- - <by---莫杰---->

**Doctor Directory**: Access a list of doctors with their specialties and patient counts.
在APP.jsx中 

代码中React组件代码主要想表达的是初始化并管理一个医院管理系统中医生信息的状态。通过useState钩子创建doctors状态，存储多个医生的详细信息，包括身份标识、个人信息、专业领域、业务数据、职业资历、头像及简介等。后续可利用这些信息在界面上展示医生列表、医生详情等内容，为医院管理系统中与医生相关的功能（如患者预约、医生介绍展示等）提供数据支撑。

-  id ：医生的唯一标识编号，用于在系统中区分不同医生，像 id: 3  、 id: 4 等，是一个整数类型。
-  name ：医生的姓名，格式为字符串，如 "Dr. Williams"  、 "Dr. Brown"  ，其中 Dr.  表示医生头衔。
-  specialty ：医生的专业领域，以字符串呈现，例如 "Orthopedics" （骨科 ）、 "Neurology" （神经学 ）、 "Dermatology" （皮肤病学 ） 。
-  patients ：表示该医生服务过的患者数量，是整数类型，比如 150 、 100  。
-  appointments ：医生已安排的预约数量，整数类型，如 500  、 350  。
-  experience ：医生的从业经验，单位可能是年，以整数表示，像 12  、 18  、 8   。
-  qualifications ：医生的资质和职称，字符串类型，例如 "MD, FAAOS"  、 "MD, PhD"  、 "MD, FAAD"  ，其中 MD  是医学博士学位，后面的是相关专业学会认证等。
-  image ：指向医生头像图片的链接，字符串类型，链接来自 randomuser.me  ，用于在系统中展示医生头像。
-  bio ：医生的个人简介，字符串类型，介绍医生的专业特长和擅长治疗的领域等，例如 "Dr. Williams specializes in sports medicine and joint replacement surgeries, helping patients regain mobility and ..."  。
- - <by---刘蓉蓉---->
 
  

## 页面
## 1.在HomePage.jsx和Home.jsx 
    <Layout>
      <h1 className="text-3xl font-bold text-center my-8">Welcome to Hospital Management System</h1>
      {/* Add more sections or components as needed */}
    </Layout>
    通过  <Layout>  组件引入 Header 和其他布局元素。

Home.jsx的代码 
有完整的主页实现
   包含丰富的功能：
     英雄区域(Welcome to Health Nest)
     特色功能展示(6个医疗相关功能)
     关于我们部分(带图片轮播)
     患者评价轮播
     行动号召区域(Sign Up)
     评论组件(Review)
   使用了动画效果(motion)和响应式设计
   包含多个子组件和外部库(如react-slick)

## 2.医院管理系统主页 - 功能、项目介绍与效果

1. 主要功能
欢迎区域
大标题动画显示"Welcome to Health Nest"  
副标题展示系统简介  
"Get Started"按钮（跳转至注册页）  

核心特色功能展示（6项）  
现代化医疗设施（'FaHospital'）  
专业医疗团队（'FaUserMd'）  
便捷预约系统（'FaCalendarCheck'）  
全面医疗服务（'FaHeartbeat'）  
24/7急救服务（'FaAmbulance'）  
远程医疗支持（'FaLaptopMedical'）  

关于我们
图片轮播展示医院环境  
文字介绍系统目标和优势  
"Learn More"按钮（跳转至关于页面）  

患者评价 
轮播展示6条患者评价  
包含用户头像、姓名和评语  
悬停动画效果  

行动号召（CTA）
鼓励用户注册（"Sign Up Now"按钮）  

动画与交互
使用framer-motion实现滚动、悬停动画  
响应式设计（适配手机、平板、电脑）  

2. 项目介绍 
项目名称：Health Nest（医院管理系统）  
技术栈：  
前端：React.js + Tailwind CSS  
动画库：Framer Motion  
图标：React Icons（Font Awesome）  
轮播组件：react-slick  

代码结构：  
HomePage.jsx：主页入口，负责整体布局（如导航栏、页脚）。  
Home.jsx：主页核心内容，包含所有功能模块。  

设计特点：  
现代化UI，圆角卡片+阴影效果  
医疗主题配色（蓝、白、橙）  
移动端优先，适配不同屏幕尺寸  

3. 实现效果
动态视觉效果：  
文字渐显、按钮缩放、卡片悬停上浮  
平滑的图片轮播和评价滑动  
用户友好交互：  
点击按钮跳转至对应功能页（如注册、关于）  
轮播自动播放，支持手动切换  

响应式布局：  
  电脑端：3列功能展示  
  平板端：2列  
  手机端：1列（内容堆叠）  

 

预约：预约和管理患者预约。   
在Server.jsx和Appointments.jsx
1. Services.jsx
定位：服务列表展示页
预约相关内容：
在服务列表中包含 "Appointment Scheduling"（预约排班） 项
仅作为文字说明，无实际功能
作用：向用户说明系统支持预约功能，但需跳转到其他页面（如Appointments.jsx）才能操作。


2. Appointments.jsx
定位：完整的预约管理功能页
核心功能：
 新建预约
表单包含患者姓名、选择医生、日期时间、备注  
使用 DatePicker 组件选择时间  
输入验证（姓名格式、未来时间校验）
  管理预约
搜索预约（按患者名或医生名）  
标记预约为“已完成”  
删除预约  
  数据展示
卡片式布局显示预约详情（患者、医生、时间、状态）  
状态标签（Scheduled/Completed）  
操作按钮（编辑、删除、完成）

技术实现：  
  使用 useState 管理状态  
  动画效果（framer-motion）  
  响应式设计（适配手机/电脑）

## 1. Services.jsx 的功能、项目介绍与效果

功能
服务列表展示：静态列出医院管理系统的主要功能，包括：  
患者管理（Patient Management）  
预约排班（Appointment Scheduling）  
电子健康记录（EHR）  
账单管理（Billing and Invoicing）  
药品库存管理（Inventory Management）  
员工管理（Staff Management）  
数据分析（Reporting and Analytics）  
远程医疗（Telemedicine Integration）  

项目介绍 
定位：服务介绍页，用于向用户说明系统提供的功能。  
技术实现：  
使用 React 构建静态页面。  
采用 Tailwind CSS 进行简单样式布局。  
无动态数据交互，仅渲染固定内容。  

效果  
UI 示例：  
  ```plaintext
  Our Services
  • Patient Management
  • Appointment Scheduling
  • Electronic Health Records
  • Billing and Invoicing
  • ...（其他服务项）
  ```
交互：  
纯静态页面，无点击事件或表单提交。  
适合作为系统功能概览页，引导用户进入具体功能模块。  

##( 代码结构：
 
- 基础布局：通过  <Layout>  组件引入头部和页脚。
 
- 内容结构：使用卡片式布局（圆角+阴影）分点列出功能，搭配图标（如  FaList ）增强识别。
 
效果
 
1. 视觉设计：
 
- 医疗主题配色（主色：蓝色，辅助色：白色/橙色）。
 
- 每个功能项含图标+标题，简洁清晰（例： FaUserGroup  对应“患者管理”）。
 
2. 交互体验：
 
- 预约排班 文字可点击（或带箭头图标），提示用户跳转至  Appointments.jsx  操作。
 
- 响应式布局：手机端堆叠显示，电脑端分两列/三列排列。
 
3. 作用：
 
- 快速传达系统能力，引导用户进入具体功能模块（如预约管理）。)

## 2. Appointments.jsx 的功能、项目介绍与效果 

 功能 
预约管理全流程：  
新建预约：填写患者姓名、选择医生、设定时间、添加备注。  
搜索预约：按患者或医生姓名实时筛选。  
状态管理：标记预约完成（Completed）或删除预约。  
数据验证：确保患者姓名合法、预约时间在未来。  
动态数据模拟：  
默认展示 2 条预约数据（可扩展为 API 请求）。  
提供 3 名医生选项（可扩展为动态加载）。  

 项目介绍  
定位：核心业务页，提供完整的预约增删改查（CRUD）功能。  
技术实现：  
React Hooks（useState, useContext）管理状态。  
Framer Motion 实现动画（表单弹出、卡片悬停）。  
React DatePicker 选择预约时间。  
权限控制：未登录用户跳转至登录页（依赖 LoginContext）。  
响应式布局：适配手机、平板、电脑（Tailwind CSS 网格）。  

 效果 
UI 示例：  
  顶部操作栏：  
“新建预约”按钮（点击展开表单）。  
搜索框（实时过滤预约）。  
  预约卡片：  
显示患者、医生、时间、状态（Scheduled/Completed）。  
操作按钮（删除、标记完成）。  
  表单弹窗：  
    - 带输入验证的预约提交表单。  
  交互体验：  
动画：表单渐显、卡片悬停上浮。  
即时反馈：输入错误时弹出提示。  

- - <by---陈丽芹---->


## 技术栈

- **ReactJs**  
  基于组件化架构构建现代化、响应式的前端界面，通过状态管理和虚拟DOM提升应用性能。

- **JavaScript (ES6+)**  
  使用箭头函数、解构赋值、async/await等现代语法，结合模块化开发（import/export）提高代码可读性和可维护性。

- **HTML5**  
  构建页面基础结构，采用语义化标签（如`<header>`, `<nav>`, `<main>`）提升SEO和可访问性。

- **CSS3**  
  实现页面样式和动画效果，采用模块化CSS和响应式设计原则，确保跨设备显示一致性。

- **Font Awesome**  
  集成丰富的矢量图标库，增强界面视觉效果和交互体验，支持自定义图标样式。

- **jsPDF**  
  实现前端PDF报告生成功能，支持数据导出和打印，可自定义报告格式和内容。

- **其他关键依赖**  
  - **React Router DOM**：实现单页面应用路由管理  
  - **Framer Motion**：创建流畅的动画和过渡效果  
  - **Axios**：处理HTTP请求，与后端API进行数据交互  
  - **MongoDB & Mongoose**：构建数据库模型和数据持久化  
  - **NextAuth**：实现用户认证和权限管理  
  - **React Datepicker**：提供直观的日期选择组件
 
- - <by---农氏线---->

 
  ## 安装与设置指南
- 1. 环境准备
 首先需要在你的机器上安装以下软件：
 Git (版本控制工具)
Node.js (v16+ 建议使用 LTS 版本)
npm (Node.js 包管理器，通常随 Node.js 一起安装)

- **验证环境安装**
  bash

- **检查 Git 版本**

  git --version

- **检查 Node.js 版本**

  node --version

- **检查 npm 版本**

  npm --version

- 2. 获取项目源代码
 打开终端或命令提示符，执行以下命令克隆项目仓库：
   bash

  git clone https://github.com/yazdanhaider/Hospital-Management.git

  cd Hospital-Management


- 3. 安装项目依赖
  在项目根目录下执行以下命令安装前端和后端依赖：
  bash

- **安装前端依赖**

  npm install

  如果你需要单独安装后端依赖（如果项目结构包含后端目录）
  cd backend
  npm install

- 4. 配置环境变量
  在项目根目录下创建 .env 文件，并配置以下环境变量：
  env

- ## 开发环境配置

  REACT_APP_API_URL=https://hospital-management-server-zeta.vercel.app/api



- ## 其他可能需要的配置项

  REACT_APP_PORT=3000


- 5. 数据库配置（如果需要本地数据库）
  如果项目使用本地数据库，需要：
  安装 MongoDB 数据库服务
  启动 MongoDB 服务
  在 .env 文件中配置数据库连接信息：
  env
  DB_CONNECTION_STRING=mongodb://localhost:27017/hospital-management

- 6. 运行开发环境
   在项目根目录下执行以下命令启动开发服务器：
   bash

- **启动前端开发服务器**

   npm run dev


- **如果需要同时启动后端服务器（在另一个终端窗口）**

  cd backend

  npm start

  开发服务器启动后，访问 http://localhost:3000 即可看到应用界面。

- 7. 生产环境构建与部署
  构建生产版本
  bash

**构建生产优化版本**

  npm run build



  构建完成后，会在项目根目录生成 build 文件夹，包含优化后的静态文件。

 **部署选项**
  选项 1: 使用 Vercel/Netlify 自动部署
  将项目推送到 GitHub 仓库
  在 Vercel/Netlify 平台绑定 GitHub 仓库
  配置构建命令为 npm run build
  设置发布目录为 build
  平台会自动检测代码变更并触发部署


- 8. 验证部署
  部署完成后，访问配置的域名或 IP 地址，确保应用正常运行。使用管理员账户（用户名：admin，密码：admin）登录系统，验证所有功能模块是否正常工作。

- 9. 故障排除
  如果遇到问题，可以检查以下方面：
  确认所有依赖正确安装，没有错误信息
  检查环境变量配置是否正确
  查看终端日志输出，定位具体错误
  确认后端 API 服务是否正常运行
  检查浏览器开发者工具中的网络请求和控制台错误
 

 - - <by---罗钰慧---->

  
  
  **使用方法**

-通过顶部导航栏在不同板块间切换:
板块间切换操作：在页面顶部，设有直观清晰的导航栏，是一个网页导航栏。涵盖多个核心板块，其中 “Health Nest” 是网站名称，可直译为 “健康巢” 。导航栏上有 “Home（首页）”“Appointments（预约）”“Patients（患者）”“Doctors（医生）”“About（关于）”“Contact（联系）” 等 ，方便用户在不同页面间跳转。此外，还有 “Sign Up（注册）” 和 “Log In（登录）” 仅需轻点对应文字标签或图标，即可快速、流畅地切换至目标板块，获取不同类型的信息与服务。例如，点击“Doctors（医生）”，可以看到很多医生的信息，从而进行选择。
板块间切换操作：在页面顶部，设有直观清晰的导航栏，是一个网页导航栏。涵盖多个核心板块，其中 “Health Nest” 是网站名称，可直译为 “健康巢” 。导航栏上有几大板块，方便用户在不同页面间跳转。
1. Home（首页）：点击可返回网站首页，获取网站的主要信息和功能入口。
 
2. Appointments（预约）：用于进入预约相关的界面，安排服务预约。
 
3. Patients（患者）：展示与患者相关的信息，如患者账户管理、患者相关数据等。
 
4. Doctors（医生）：点击可查看网站上的医生信息，以便用户选择合适的医生。
 
5. About（关于）：介绍网站的背景、宗旨、发展历程等相关信息。
 
6. Contact（联系）：提供与网站相关的联系方式，如客服邮箱、电话等。
 
7. Sign Up（注册）：新用户可点击此选项进行注册，创建自己的账户。
 
8. Log In（登录）：已有账户的用户点击登录，输入正确的账号密码后进入个人账户。

-使用预约表单安排新的预约
预约流程指引：若您有服务预约需求，可通过以下步骤完成新预约：
1.预约流程指引：若您有服务预约需求，可通过以下步骤完成新预约：
首先，点击导航栏中的“Appointments（预约）”,进入预约界面；
接着，按提示依次填写病人姓名、选择预约的医生、预约日期及时间段以及主要的信息；
2.接着，按提示依次填写病人姓名、选择预约的医生、预约日期及时间段以及主要的信息；
填写完成后，请仔细核对各项内容，确保信息准确无误；
最后，点击「提交」按钮，系统将即时响应并生成预约确认提示。您可在「我的预约」中查看预约详情，如有问题也可随时联系在线客服协助处理。
3.最后，点击「提交」按钮，系统将即时响应并生成预约确认提示。您可在「我的预约」中查看预约详情，如有问题也可随时联系在线客服协助处理。
 
 - - <by---莫莉华---->
  

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
 - - <by---黄建霖--->


  
### 1. 管理员
- 🛡️ 安全登录/登出系统
- 📊 实时数据可视化（柱状图/饼图）
- 📄 可视化PDF报告生成
- 📈 核心指标统计（医生/患者/预约/营收）
- 🎯 交互式图表支持（Chart.js）

### 2. 患者系统
- 👥 患者全生命周期管理（CRUD）
- 🔍 实时搜索过滤（姓名关键字）
- 📝 数据验证表单（前端校验规则）
- 🗂️ 患者信息卡片管理
- 🎬 交互动画系统（Framer Motion）

## 技术架构

| 分类            | 技术栈                                                                 |
|-----------------|----------------------------------------------------------------------|
| 核心框架        | React 18                                                             |
| 样式方案        | Tailwind CSS 3                                                       |
| 数据可视化      | Chart.js 4 + html2canvas 1.4                                        |
| PDF生成        | jsPDF 2.5                                                           |
| 网络请求        | Axios 1.3                                                           |
| 动画引擎        | Framer Motion 10                                                     |
| 图标库          | React Icons 4.7 (Font Awesome)                                      |

## 快速启动

### 环境要求
- Node.js 16+
- npm 8+

### 安装依赖
```bash
npm install react react-icons axios framer-motion jspdf chart.js react-chartjs-2 html2canvas
npm start

#管理员
- **认证系统**：
  - 默认凭证：admin/password
  - 登录状态持久化
  - 退出登录清理机制

- **数据看板**：
  - 实时统计卡片（悬停动效）
  - 双图表展示：
    - 柱状图（运营数据对比）
    - 饼图（资源分布比例）

- **智能报告**：
  - 一键生成PDF功能
  - 包含元素：
    - 医院基本信息
    - 关键指标数据
    - 可视化图表截图
    - 生成时间戳
#患者
- **搜索系统**：
  - 实时过滤患者列表
  - 自适应移动端布局
  - 无延迟输入响应

- **表单验证**：
  - 姓名：最小4字符，字母开头
  - 联系方式：XXX-XXX-XXXX格式
  - 邮箱：标准格式校验
  - 年龄：数字范围限制

- **动画系统**：
  - 表单展开动画（y轴位移）
  - 卡片入场动画（渐显效果）
  - 按钮交互动效（按压缩放）
  
   API接口
  # 已实现接口
   模块	端点	方法	功能	状态码
患者管理	/api/patients/get-patients	GET	获取患者列表	200/500
患者管理	/api/patients/delete-patient	POST	删除患者记录	200/404

  # 待实现接口
  - [ ] `POST /api/patients/register` - 患者注册（请求示例）：
  ```json
  {
    "name": "John Doe",
    "age": 35,
    "gender": "Male",
    "mobile": "1234567890",
    "email": "john@example.com"
  }
POST /api/auth/login - 管理员登录（JWT认证）

GET /api/hospital/stats - 获取医院统计数据

## 数据管理

### 状态结构
```javascript
// 管理员模块
const [isLoggedIn, setIsLoggedIn] = useState(false); // 登录状态
const [statsData] = useState([...]); // 统计数据

// 患者模块
const [patients, setPatients] = useState([...]); // 患者列表
const [newPatient, setNewPatient] = useState({
  name: "",      // 患者姓名
  age: "",       // 年龄
  gender: "",    // 性别
  mobile: "",    // 联系方式
  email: ""      // 电子邮箱
});

###报告图表可视化
// 柱状图配置示例
const barChartData = {
  labels: ['Patients', 'Doctors', 'Appointments', 'Revenue'],
  datasets: [{
    label: '医院统计',
    data: [1000, 50, 1500, 500000],
    backgroundColor: 'rgba(54, 162, 235, 0.5)',
    borderColor: 'rgba(54, 162, 235, 1)'
  }]
};

// PDF生成优化参数
const pdfOptions = {
  pageSize: 'A4',         // 页面尺寸
  chartScale: 0.8,        // 图表缩放比例
  imageQuality: 0.95      // 图片质量
};
 - - <by---陶利合--->
