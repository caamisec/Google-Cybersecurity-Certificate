This project presents a **Portfolio Activity** conducted as part of the **Google Cybersecurity Professional Certificate**. The objective was to develop a Python algorithm that automates the process of updating access control files by removing unauthorized IP addresses from an allow list. This activity demonstrates practical programming skills in file manipulation, data processing, and cybersecurity automation essential for security professionals managing access controls.

## 🎯 Scenario

You are a security professional working at a healthcare company responsible for regularly updating a file that identifies employees who can access restricted content containing personal patient records. Employee access is controlled based on their IP addresses through an allow list for the restricted subnetwork. A separate remove list identifies which employees must be removed from the allow list. The task was to create a Python algorithm that automatically checks and removes IP addresses from the allow list file when they appear on the remove list.

## 🔍 Applied Methodology

- **Tool**: Python programming with file I/O operations
- **Algorithm Components**: File reading, string/list conversion, iteration, conditional logic, file writing
- **Approach**: Automated access control management through systematic IP address removal
- **Focus**: Healthcare data security and employee access control automation

## 📊 Key Findings

### **Python Algorithm Development:**

**File Processing Operations:**

- **File Opening**: Used `with open()` statements for secure file handling and resource management
- **Data Reading**: Applied `.read()` method to convert file contents into string format
- **Data Conversion**: Utilized `.split()` method to transform IP address strings into manageable lists
- **Data Writing**: Implemented `.write()` method with proper file modes for updating allow list

**Logic Implementation:**

- **Iteration Control**: Developed `for` loops to process each IP address in the remove list
- **Conditional Logic**: Created `if` statements to verify IP address existence before removal
- **Error Prevention**: Implemented safeguards to avoid errors when removing non-existent elements
- **Data Formatting**: Used `.join()` method to convert processed lists back to file-ready strings

**Access Control Automation:**

- **Allow List Management**: Automated removal of unauthorized IP addresses from access control files
- **Healthcare Compliance**: Ensured restricted patient data access remains properly controlled
- **Process Efficiency**: Eliminated manual file updates through systematic automation

## 🎯 Analysis Results

The Python algorithm successfully automated the access control update process, demonstrating how programming can enhance cybersecurity operations. The systematic approach to file manipulation and data processing created a reliable, repeatable solution for managing employee access to restricted healthcare information while maintaining security best practices.

## 📁 Documentation

- **Portfolio Project**: Complete Python algorithm development for cybersecurity automation
- **Code Documentation**: Step-by-step explanation of algorithm components and functionality
- **Healthcare Security**: Access control implementation for patient data protection
- **Automation Benefits**: Demonstration of programming efficiency in security operations

## 💼 Skills Demonstrated

- Python programming fundamentals and file I/O operations
- Cybersecurity automation and access control management
- Healthcare data security and compliance considerations
- Algorithm development and logical problem-solving
- Code documentation and professional technical communication
- Security process improvement through programming automation