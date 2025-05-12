<div align="center">
<img src="https://readme-typing-svg.herokuapp.com?color=FFB13C&size=50&width=1000&height=80&lines=Welcome-to-Hospital-Management-App"/>
</div>

# HealthHub - Advanced Hospital Management System


HealthHub is a comprehensive React-based hospital management system designed to streamline healthcare operations and improve patient care. A comprehensive hospital management system is built using JavaScript (ES6+), HTML5, CSS3, and Font Awesome icon technology. It has a user-friendly responsive interface and enables functions such as appointment management, maintenance of patient records, management of doctor information, and provides management tools. The pages of the system include a homepage, an appointment page, a patient page, a doctor page, and an administrator page.
For the deployment, the backend is deployed at https://hospital-management-server-zeta.vercel.app/.
For users who want to install and use this system, the specific steps are as follows: Clone the repository: Use the command git clone https://github.com/yazdanhaider/Hospital-Management.git to clone the project repository to the local machine and obtain the source code of the system. Navigate to the project directory: Enter cd Hospital-Management in the command line to enter the directory where the project is located, getting ready for subsequent operations. Install dependencies: Execute the npm i command to automatically install all kinds of dependency packages required for the project to run, ensuring the integrity of the system functions. Run the development server: Start the development server by using the npm run dev command, allowing the system to run properly in the local environment, which is convenient for debugging and testing.
During the actual use, users can easily browse different parts of the system through the top navigation bar and quickly locate the required functional modules. They can use the appointment form to arrange new appointments, and the operation process is simple and clear. In the patient management section, operations such as adding, editing, and deleting patient records can be carried out to achieve dynamic management of patient information. In the doctor information section, relevant information of doctors can be viewed and managed to reasonably arrange the work of medical staff. Administrators can log in to the Admin panel using "admin" as both the username and password to access management functions and perform advanced management operations on the system.

- - <by---莫杰---->


The code for the React component mainly aims to initialize and manage the state of doctor information in a hospital management system. The  useState  hook is used to create the  doctors  state, which stores detailed information about multiple doctors, including identity identifiers, personal information, professional fields, business data, professional qualifications, profile pictures, and introductions, etc. Subsequently, this information can be utilized to display the doctor list, doctor details, etc., on the interface, providing data support for doctor-related functions (such as patient appointments, doctor introduction displays, etc.) in the hospital management system.
 
-  id : The unique identification number of a doctor, used to distinguish different doctors in the system, such as  id: 3 ,  id: 4 , etc., and it is an integer type.
-  name : The name of the doctor, in the format of a string, such as "Dr. Williams", "Dr. Brown", where "Dr." represents the doctor's title.
-  specialty : The professional field of the doctor, presented as a string, for example, "Orthopedics" (orthopedics), "Neurology" (neurology), "Dermatology" (dermatology).
-  patients : Represents the number of patients served by the doctor, and it is an integer type, such as 150, 100.
-  appointments : The number of scheduled appointments for the doctor, an integer type, such as 500, 350.
-  experience : The doctor's work experience, with the unit likely being years, represented as an integer, like 12, 18, 8.
-  qualifications : The doctor's qualifications and professional titles, in the form of a string, for example, "MD, FAAOS", "MD, PhD", "MD, FAAD", where "MD" is the Doctor of Medicine degree, and the subsequent ones are relevant professional society certifications, etc.
-  image : A link to the doctor's profile picture, in the string type, and the link comes from  randomuser.me , used to display the doctor's profile picture in the system.
-  bio : The doctor's personal introduction, in the string type, introducing the doctor's professional expertise and the fields of treatment they are good at, for example, "Dr. Williams specializes in sports medicine and joint replacement surgeries, helping patients regain mobility and ..."
- - <by---刘蓉蓉---->

## Pages

1. **Home**: Welcome page with quick access to key features.
## 1. In HomePage.jsx and Home.jsx

## HomePage.jsx code
It only contains a welcome title.
```jsx
<Layout>
  <h1 className="text-3xl font-bold text-center my-8">Welcome to Hospital Management System</h1>
  {/* Add more sections or components as needed */}
</Layout>
```
It introduces the `Header` and other layout elements through the `<Layout>` component.

### Home.jsx code
It has a complete implementation of the home page.
It includes rich features:
 Hero area ("Welcome to Health Nest")
 Featured function display (6 medical-related functions)
 About Us section (with image carousel)
 Patient reviews carousel
 Call-to-Action area ("Sign Up")
 Review component
It uses animation effects (`motion`) and responsive design.
It contains multiple sub-components and external libraries (such as `react-slick`).

## 2. Hospital Management System Home Page - Features, Project Introduction and Effects

## 1. Main Features
Welcome Area
 The large title is animated to display "Welcome to Health Nest".
 The subtitle shows an introduction to the system.
 "Get Started" button (jumps to the registration page).
Core Featured Functions Display (6 items)
 Modern medical facilities ('FaHospital')
 Professional medical team ('FaUserMd')
 Convenient appointment system ('FaCalendarCheck')
 Comprehensive medical services ('FaHeartbeat')
 24/7 emergency services ('FaAmbulance')
 Telemedicine support ('FaLaptopMedical')
About Us
 Image carousel shows the hospital environment.
 Text introduction of the system's goals and advantages.
 "Learn More" button (jumps to the about page).
Patient Reviews
 Carousel shows 6 patient reviews.
 Includes user avatars, names, and comments.
 Hover animation effect.
Call-to-Action (CTA)
 Encourages users to register ("Sign Up Now" button).

## Animation and Interaction
 Uses `framer-motion` to implement scrolling and hovering animations.
 Responsive design (adapts to mobile phones, tablets, and computers).

## 2. Project Introduction
Project Name: Health Nest (Hospital Management System)
Technology Stack:
 Front-end: React.js + Tailwind CSS
 Animation Library: Framer Motion
 Icons: React Icons (Font Awesome)
 Carousel Component: react-slick
Code Structure:
 HomePage.jsx: The entry point of the home page, responsible for the overall layout (such as the navigation bar and footer).
 Home.jsx: The core content of the home page, containing all functional modules.
Design Features:
 Modern UI with rounded corner cards + shadow effect.
 Medical-themed color scheme (blue, white, orange).
 Mobile-first, adapting to different screen sizes.

## 3. Implementation Effects
Dynamic Visual Effects:
 Gradual text appearance, button scaling, and card hovering and floating up.
 Smooth image carousel and review sliding.
User-Friendly Interaction:
  Clicking the button jumps to the corresponding function page (such as registration, about).
  The carousel plays automatically and supports manual switching.
Responsive Layout:
  On desktop: 3-column function display.
  On tablet: 2-column.
  On mobile phone: 1-column (content stacked).  

2. Appointments: Book and manage patient appointments.
## In Server.jsx and Appointments.jsx

 1. Services.jsx
Positioning: Service list display page
Appointment - related content:
Include the item "Appointment Scheduling" in the service list. It is only a text description without actual functionality.
Function:
Inform users that the system supports the appointment function, but they need to jump to other pages (such as Appointments.jsx) to perform operations.

## 2. Appointments.jsx
Positioning: A complete appointment management function page

Core functions:
 Create new appointments:
The form includes patient name, doctor selection, date and time, and remarks. Use the DatePicker component to select the time. Input validation (name format, future time verification).
 Manage appointments:
Search for appointments (by patient name or doctor name). Mark appointments as "completed". Delete appointments.
 Data display:
Display appointment details in a card layout (patient, doctor, time, status). Status labels (Scheduled/Completed). Action buttons (edit, delete, complete).

Technical implementation:
Use useState to manage state. Animation effects (framer - motion). Responsive design (compatible with mobile/desktop).

## 1. Functions, Project Introduction and Effects of Services.jsx

Functions
Service list display:
Static listing of the main functions of the hospital management system, including:
Patient Management
Appointment Scheduling
Electronic Health Records (EHR)
Billing and Invoicing
Drug Inventory Management
Staff Management
Data Analysis (Reporting and Analytics)
Telemedicine Integration

Project Introduction
Positioning: Service introduction page, used to inform users about the functions provided by the system.
Technical implementation:
Build a static page using React. Use Tailwind CSS for simple layout styling. There is no dynamic data interaction, only rendering fixed content.

Effects
UI example:
```plaintext
Our Services
• Patient Management
• Appointment Scheduling
• Electronic Health Records
• Billing and Invoicing
•... (other service items)
```
Interaction:
A purely static page with no click events or form submissions. It is suitable as an overview page of system functions to guide users to specific functional modules.

### Code Structure:
- **Basic Layout**: Introduce the header and footer through the `<Layout>` component.
- **Content Structure**: Use a card-style layout (rounded corners + shadows) to list functions item by item, and pair with icons (such as `FaList`) to enhance recognition.

### Effects
1. **Visual Design**:
    - Medical-themed color scheme (primary color: blue, secondary colors: white/orange).
    - Each function item contains an icon and a title, which is simple and clear (for example, `FaUserGroup` corresponds to "Patient Management").
2. **Interactive Experience**:
    - The text "Appointment Scheduling" is clickable (or accompanied by an arrow icon) to prompt users to jump to the `Appointments.jsx` for operations.
    - Responsive layout: Stacked display on mobile devices and arranged in two or three columns on desktop devices.
3. **Function**:
    - Quickly convey the system capabilities and guide users to enter specific functional modules (such as appointment management). 
    
### 2. Functions, Project Introduction and Effects of Appointments.jsx

Functions
Full - process appointment management:
 Create new appointments: Fill in patient name, select doctor, set time, and add remarks.
 Search for appointments: Real - time filtering by patient or doctor name.
 Status management: Mark appointments as completed or delete appointments.
 Data validation: Ensure that the patient name is legal and the appointment time is in the future.
 Dynamic data simulation:
By default, display 2 appointment data (can be extended to API requests). Provide 3 doctor options (can be extended to dynamic loading).

#### Project Introduction
Positioning: Core business page, providing complete appointment CRUD (Create, Read, Update, Delete) functions.
Technical implementation:
Use React Hooks (useState, useContext) to manage state. Use Framer Motion to implement animations (form pop - up, card hover). Use React DatePicker to select appointment time. Permission control: Redirect unlogged - in users to the login page (depends on LoginContext). Responsive layout: Compatible with mobile, tablet, and desktop (Tailwind CSS grid).

Effects
UI example:
 Top operation bar:
"Create new appointment" button (click to expand the form). Search box (real - time filtering of appointments).
 Appointment cards:
Display patient, doctor, time, and status (Scheduled/Completed). Action buttons (delete, mark as completed).
 Form pop - up window:
A reservation submission form with input validation.

Interaction experience:
 Animation: The form fades in, and the card hovers and floats up.
 Immediate feedback: Pop up a prompt when there is an input error.

- - <by---陈丽芹---->


## Technologies Used

- **ReactJs**  
  Build modern, responsive front-end interfaces with a component-based architecture, leveraging state management and virtual DOM for optimal performance.

- **JavaScript (ES6+)**  
  Utilize modern syntax features such as arrow functions, destructuring, and async/await, combined with modular development (import/export) for improved code readability and maintainability.

- **HTML5**  
  Provide the structural foundation with semantic markup (e.g., `<header>`, `<nav>`, `<main>`) to enhance SEO and accessibility.

- **CSS3**  
  Implement styling and animations with modular CSS and responsive design principles to ensure consistent cross-device rendering.

- **Font Awesome**  
  Integrate a comprehensive library of vector icons to enhance visual appeal and user experience, supporting custom icon styling.

- **jsPDF**  
  Enable front-end PDF report generation for data export and printing, with customizable report formatting and content.

- **Other Key Dependencies**  
  - **React Router DOM**: Manage routing for single-page applications  
  - **Framer Motion**: Create smooth animations and transitions  
  - **Axios**: Handle HTTP requests for API data interactions  
  - **MongoDB & Mongoose**: Build database models and ensure data persistence  
  - **NextAuth**: Implement user authentication and authorization  
  - **React Datepicker**: Provide intuitive date selection components
  - - <by---农氏线---->

 
  -  ## Setup and Installation
1. Install Node.js:
   ```
   Visit https://nodejs.org/en/download to download and install Node.js.
   ```
2. Clone the repository:
   ```
   git clone https://github.com/yazdanhaider/Hospital-Management.git
   ```
3. Navigate to the Backend Project Directory:
   ```
   cd Hospital-Management Backend
   ```
4. Install dependencies:
   ```
   npm install
   ```
5. Run the Backend Server:
   ```
   npm run dev
   ``` 
6. Navigate to the Backend Project Directory:
   ```
   cd Hospital-Management/Frontend
   ```
7. Install dependencies:
   ```
   npm install
   ```
8. Run the Backend Server:
   ```
   npm run dev
   ``` 
- - <by---罗钰慧---->
  
  
  **Usage**

- **Switch between different sections via the top navigation bar**:
The operation of switching between sections: There is an intuitive and clear web navigation bar at the top of the page. It covers multiple core sections. The website is named "Health Nest". The navigation bar includes "Home", "Appointments", "Patients", "Doctors", "About", "Contact", etc. Additionally, there are "Sign Up" and "Log In". Just tap on the corresponding text labels or icons, and you can quickly and smoothly switch to the target section to obtain different types of information and services. For example, by clicking on "Doctors", you can view the information of many doctors and then make a selection.
The operation of switching between sections: There is an intuitive and clear web navigation bar at the top of the page. It covers multiple core sections. The website is named "Health Nest". There are several major sections on the navigation bar, which is convenient for users to jump between different pages.
1. **Home**: Click to return to the website's homepage and access the main information and functional entrances of the website.
2. **Appointments**: Used to enter the appointment-related interface and arrange service appointments.
3. **Patients**: Displays information related to patients, such as patient account management, patient-related data, etc.
4. **Doctors**: Click to view the information of doctors on the website so that users can select suitable doctors.
5. **About**: Introduces relevant information such as the background, purpose, and development history of the website.
6. **Contact**: Provides contact information related to the website, such as the customer service email address and telephone number, etc.
7. **Sign Up**: New users can click this option to register and create their own accounts.
8. **Log In**: Existing users click to log in and enter their personal accounts after entering the correct account and password.

- **Arrange new appointments using the appointment form**
Guidance on the appointment process: If you have a need for service appointments, you can complete a new appointment through the following steps:
1. Guidance on the appointment process: If you have a need for service appointments, you can complete a new appointment through the following steps:
First, click "Appointments" in the navigation bar to enter the appointment interface.
Next, fill in the patient's name, select the doctor for the appointment, the appointment date and time period, and other main information in sequence according to the prompts.
2. Next, fill in the patient's name, select the doctor for the appointment, the appointment date and time period, and other main information in sequence according to the prompts.
After filling it out, carefully check all the contents to ensure the accuracy of the information.
Finally, click the "Submit" button. The system will respond immediately and generate an appointment confirmation prompt. You can view the appointment details in "My Appointments", and if there are any problems, you can contact the online customer service for assistance at any time.
3. Finally, click the "Submit" button. The system will respond immediately and generate an appointment confirmation prompt. You can view the appointment details in "My Appointments", and if there are any problems, you can contact the online customer service for assistance at any time. 
- - <by---莫莉华---->
 
 计科2205班黄建霖2205308050352
🏥 Doctors Component
A React component that displays a list of doctors with search, detailed view, and appointment booking functionality. Suitable for use in medical or healthcare-related web applications.

📸 Preview (Optional)
You can insert a screenshot or GIF here showing the layout of the doctor cards, search bar, and modal popup.

🧩 Features
✅ Display doctor avatar, name, specialty, experience, and patient count
🔍 Search doctors by name or specialty
📄 Click on a doctor card or info button ("i") to open a modal with detailed info
📅 "Book Appointment" button navigates to an appointment page with the doctor's ID as a query param
🎨 Built with Tailwind CSS for responsive UI
🎞️ Animated buttons using framer-motion
🛠 Tech Stack
Technology	Version / Use
React	Core framework
React Router DOM	Navigation
Framer Motion	Button animations
Font Awesome Icons	Icon library
Tailwind CSS	Styling
📁 File Structure
src/
├── components/
│   └── Doctors.jsx         # Main doctor list component
│   └── DoctorProfile.jsx   # (Currently unused) Suggested modal component (can be refactored)
📦 Props Overview
This component accepts a doctors prop with the following structure:

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
  // More doctors...
]
🔧 Usage Instructions
Install Dependencies
Make sure you have the following packages installed:

Bash
npm install react-router-dom framer-motion @fortawesome/react-fontawesome
Ensure Tailwind CSS is properly configured in your project.

Example Usage
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
📲 Navigation Behavior
Clicking the "Book Appointment" button will navigate to /appointments and pass the doctor ID in the URL:

Text
/appointments?doctorId=1
💡 Suggestions for Enhancement
✅ Extract the modal into a separate DoctorModal component for better modularity and reusability
🔄 Add loading and error states (especially if fetching data from an API)
📱 Improve mobile responsiveness and design
🔍 Support additional search filters like department or hospital
📚 License
MIT License - see the LICENSE file for details.




🏥Patients Component
A simple and elegant Patient Management Interface built with React, Framer Motion, and Axios for managing patient records in a healthcare or clinic setting.

This component provides a clean UI to:

View list of patients
Add new patients with validation
Search patients by name
Delete existing patients
📷 Preview

 (You can add a screenshot here if available)

🧩 Features
Feature	Description
✅ View Patients	Displays a list of patients in responsive grid cards.
✅ Add New Patient	Form to register a new patient with validation.
✅ Search Functionality	Filter patients by name in real-time.
✅ Delete Patient	Remove a patient via API call.
⚠️ Edit Patient	Placeholder exists; functionality not yet implemented.
🎨 Responsive Design	Mobile-friendly layout using TailwindCSS.
🎞️ Animations	Smooth transitions and hover effects powered by Framer Motion.
🛠️ Technologies Used
React – Component-based UI library
Framer Motion – For animations and interactions
Tailwind CSS – Utility-first styling
Axios – HTTP client for API calls
React Icons – For icons (FaUserPlus, FaSearch, etc.)
📁 File Structure

src/
└── components/
    └── Patients.jsx       # Main component file
📦 Dependencies
Make sure the following packages are installed:

Bash

npm install react react-dom axios framer-motion @react-icons/all-files
Or with yarn:

Bash

yarn add react react-dom axios framer-motion @react-icons/all-files
🔧 Backend API Endpoints (Assumed)
The component expects the following backend APIs:

Method	Endpoint	Purpose
GET	/api/patients/get-patients	Fetch all patients
POST	/api/patients/register	Register a new patient
POST	/api/patients/delete-patient	Delete a patient by ID
You may need to configure Axios base URL or proxy settings depending on your backend setup.

📋 Usage Example
To use this component, simply import and render it inside your app:

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

🧪 Validation Rules
Name: At least 4 characters long, must start with a letter.
Mobile Number: Must follow format like 1234567890 (10 digits).
Email: Required field.
Gender: Required selection.
Age: Required number input.
🧹 To-Do / Future Improvements
 Implement edit patient functionality
 Add confirmation dialog before deletion
 Use Formik or React Hook Form for better form handling
 Add loading indicators during API calls
 Implement pagination for large datasets
 Add user roles and permissions
 Show success/error toast notifications instead of alerts
📜 License
MIT License – see LICENSE for details.







🏥 Health Nest - Admin Dashboard
A simple hospital admin dashboard built with React, featuring login authentication, data visualization, and PDF report generation.

📝 Introduction
This project is a frontend admin interface designed for hospital management systems. It provides the following core features:

✅ Login authentication (username + password)
📊 Data statistics dashboard
📄 PDF report generation
🎨 Interactive animations and responsive UI
🧰 Tech Stack
Technology	Purpose
React	Frontend framework
jsPDF	PDF document generation
Framer Motion	Animation & interaction
React Icons (Font Awesome)	Icon library
Tailwind CSS (class usage)	Styling (requires installation)
🔐 Login System
Default username: admin
Default password: password
Authentication Logic
Jsx

if (username === 'admin' && password === 'password') {
    setIsLoggedIn(true);
} else {
    alert('Invalid credentials');
}
⚠️ This is a static validation. For production, consider integrating with an API or using token-based authentication.

📊 Dashboard Statistics
Displays the following key metrics:

Metric	Value
Doctors	50
Patients	1000
Appointments	1500
Revenue	$500,000
Each card includes an icon and color indicator. Framer Motion adds hover and tap effects for better user interaction.

📄 PDF Report Generation
Clicking the button generates and downloads a PDF file containing statistical data. The file name is:


hospital_report.pdf
The report includes:

Hospital name
Generation date
Statistical summary
💅 UI Design & Interaction
Responsive grid layout
Centered login form for better UX
Animated cards and buttons using Framer Motion
Tailwind CSS classes used for styling (ensure Tailwind is installed)
🛠️ Installation & Usage
Make sure you have Node.js and npm installed.

1. Install Dependencies
Bash

npm install
2. Install Required Libraries (if not already)
Bash

npm install react react-dom
npm install jspdf
npm install framer-motion
npm install @react-icons/all-files
3. Start Development Server
Bash

npm start
📁 Project Structure

src/
├── components/
│   └── Admin.jsx      # Main component
├── App.jsx              # App entry point
├── index.jsx            # Root render
└── styles/              # Optional style files
🚀 Future Improvements
Fetch dynamic data from backend APIs
Add role-based access control
Visualize data with chart libraries like ECharts or Recharts
Implement internationalization (i18n)
Expand admin modules (e.g., doctor/patient/appointment management)
📬 Contact Me
If you have any questions or suggestions, feel free to reach out!

📧 Email: your-email@example.com

💻 GitHub: [your-github-url]

📜 License
MIT Licens]
- - <by---黄建霖 ---->
 

## Feature Modules

### 1. Admin Dashboard
- 🛡️ Secure Login/Logout System
- 📊 Real-time Data Visualization (Bar/Pie Charts)
- 📄 Visual PDF Report Generation
- 📈 Core Metrics Statistics (Doctors/Patients/Appointments/Revenue)
- 🎯 Interactive Chart Support (Chart.js)

### 2. Patient Management System
- 👥 Full Patient Lifecycle Management (CRUD)
- 🔍 Real-time Search Filter (Name Keywords)
- 📝 Data Validation Forms (Frontend Rules)
- 🗂️ Patient Information Card Management
- 🎬 Interactive Animation System (Framer Motion)

## Technology Stack

| Category           | Technologies                                                                 |
|--------------------|-----------------------------------------------------------------------------|
| Core Framework     | React 18                                                                    |
| Styling Solution   | Tailwind CSS 3                                                              |
| Data Visualization | Chart.js 4 + html2canvas 1.4                                                |
| PDF Generation     | jsPDF 2.5                                                                  |
| Network Requests   | Axios 1.3                                                                  |
| Animation Engine   | Framer Motion 10                                                            |
| Icon Library       | React Icons 4.7 (Font Awesome)                                             |

## Quick Start

### Requirements
- Node.js 16+
- npm 8+

### Install Dependencies
```bash
npm install react react-icons axios framer-motion jspdf chart.js react-chartjs-2 html2canvas
npm start
Feature Details
Admin Module

- **Authentication System**:
  - Default Credentials: admin/password
  - Login State Persistence
  - Logout Cleanup Mechanism

- **Data Dashboard**:
  - Real-time Statistics Cards (Hover Effects)
  - Dual Chart Display:
    - Bar Chart (Operational Data Comparison)
    - Pie Chart (Resource Distribution)

- **Smart Reporting**:
  - One-click PDF Generation
  - Includes:
    - Hospital Basic Information
    - Key Performance Metrics
    - Visual Chart Screenshots
    - Generation Timestamp
Patient Management Module

- **Search System**:
  - Real-time Patient Filtering
  - Mobile-responsive Layout
  - Instant Input Response

- **Form Validation**:
  - Name: Min 4 characters, alphabetic start
  - Contact: XXX-XXX-XXXX format
  - Email: Standard format validation
  - Age: Numeric range restriction

- **Animation System**:
  - Form Expansion Animation (Y-axis transition)
  - Card Entrance Animation (Fade-in effect)
  - Button Interaction Effects (Press scaling)
API Documentation
Implemented Endpoints
Module	Endpoint	Method	Functionality	Status Codes
Patient	/api/patients/get-patients	GET	Retrieve patient list	200/500
Patient	/api/patients/delete-patient	POST	Delete patient record	200/404
Pending Endpoints

- [ ] `POST /api/patients/register` - Patient Registration (Request Body Example):
  ```json
  {
    "name": "John Doe",
    "age": 35,
    "gender": "Male",
    "mobile": "1234567890",
    "email": "john@example.com"
  }
POST /api/auth/login - Admin Login (JWT Authentication)

GET /api/hospital/stats - Get Hospital Statistics



## Data Management

### State Structure
```javascript
// Admin Module
const [isLoggedIn, setIsLoggedIn] = useState(false); // Login status
const [statsData] = useState([...]); // Statistical data

// Patient Module
const [patients, setPatients] = useState([...]); // Patient list
const [newPatient, setNewPatient] = useState({
  name: "",      // Patient name
  age: "",       // Age
  gender: "",    // Gender
  mobile: "",    // Contact
  email: ""      // Email
});

Chart Configuration
// Bar Chart Configuration Example
const barChartData = {
  labels: ['Patients', 'Doctors', 'Appointments', 'Revenue'],
  datasets: [{
    label: 'Hospital Statistics',
    data: [1000, 50, 1500, 500000],
    backgroundColor: 'rgba(54, 162, 235, 0.5)',
    borderColor: 'rgba(54, 162, 235, 1)'
  }]
};

// PDF Generation Optimization
const pdfOptions = {
  pageSize: 'A4',         // Paper size
  chartScale: 0.8,        // Chart scaling
  imageQuality: 0.95      // Image quality
};
- - <by---陶利合---->

 
