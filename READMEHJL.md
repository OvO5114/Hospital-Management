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
MIT License © [Your Name]
