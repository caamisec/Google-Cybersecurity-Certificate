This project presents a **Portfolio Activity** conducted as part of the **Google Cybersecurity Professional Certificate**. The objective was to demonstrate hands-on experience using Linux commands to manage file permissions for a research team, ensuring appropriate authorization levels and system security. This activity showcases practical Linux administration skills essential for cybersecurity professionals.

## 🎯 Scenario

You are a security professional at a large organization working primarily with the research team. Your task is to examine existing permissions on the file system and determine if they match the authorization that should be given. The goal is to modify permissions to authorize appropriate users and remove any unauthorized access, ensuring the system remains secure while maintaining necessary functionality for the research team.

## 🔍 Applied Methodology

- **Tool**: Linux Bash shell and command line interface
- **Commands Used**: `ls -la`, `chmod`, file system navigation
- **Approach**: Systematic permission analysis and modification
- **Focus**: User, group, and other permission management (read, write, execute)

## 📊 Key Findings

### **Permission Management Tasks Completed:**

**File System Analysis:**

- Used `ls -la` command to examine current file and directory permissions
- Identified 4 .txt files, 1 drafts directory, and 1 hidden file (.project_x.txt)
- Analyzed 10-character permission strings for security compliance

**Permission Modifications:**

- **project_k.txt**: Removed write permission for "others" group (`chmod o-w`)
- **.project_x.txt (hidden file)**: Removed write permissions for all users (`chmod u-w,g-w,o+r`)
- **drafts directory**: Modified directory access permissions (`chmod g+x`)

**Security Improvements:**

- Ensured archived files remain read-only as required
- Maintained appropriate access levels for user and group categories
- Implemented principle of least privilege for system security

## 🎯 Analysis Results

Successfully managed file permissions across multiple files and directories using Linux commands. The systematic approach ensured that research team members have appropriate access while maintaining security best practices. All permission changes were implemented according to organizational requirements, demonstrating practical Linux administration skills.

## 📁 Documentation

- **Portfolio Project**: Complete file permissions management demonstration
- **Command Documentation**: Step-by-step Linux commands with explanations
- **Permission Analysis**: Before and after permission string breakdowns
- **Security Justification**: Rationale for each permission modification

## 💼 Skills Demonstrated

- Linux command line proficiency and file system navigation
- File and directory permission management using chmod
- Security analysis and permission string interpretation
- Principle of least privilege implementation
- System administration and access control
- Technical documentation and process explanation