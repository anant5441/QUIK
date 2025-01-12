# QUIK (Quintessential Urban Infrastructure Kranti)

QUIK is an innovative platform designed to enhance inter-departmental cooperation in urban governance, addressing the critical challenges faced in Indian cities. By fostering collaboration and coordination between various departments and administrative levels, QUIK aims to reduce inefficiencies and streamline urban project management.

## Overview
Indian cities face several pressing issues due to:
- **Delays Due to Miscoordination**
- **Multiplicity of Authorities**
- **Inadequate Data Sharing**
- **Ineffective Communication Channels**
- **Environmental, Social, and Economic Impacts**

QUIK leverages modern technologies to address these challenges and provide a platform for better collaboration.

## Key Features
1. **Increased Transparency**: Enhance the visibility of project progress, roles, and decision-making processes.
2. **Resource Optimization**: Ensure efficient allocation and utilization of resources.
3. **Reduced Delays**: Minimize project delays by improving communication and coordination.
4. **Improved Coordination**: Facilitate better interaction between departments and streamline workflows.

## Project Structure
### 1. **Backend**
- Built with **Python** and **Flask** for handling API requests and database management.
- Uses **SQLite** for lightweight database storage.

### 2. **Database**
The database is organized using Flask-SQLAlchemy. It includes:
- **User Table**: Stores information about users (IDs, passwords, and roles like Department Representative, Contractor, and Admin).
- **Project Table**: Manages details about urban projects (ID, start/end dates, budgets, location details, and current status).
- **Project Estimation Table**: Captures project cost estimations submitted by contractors.

### 3. **Frontend**
- The user interface is built with **HTML**, **CSS**, and **JavaScript**.
- Provides role-specific dashboards and forms to interact with the system.

### 4. **Key Components**
#### **Python Scripts**
- `app.py`: The main application script that defines routes, models, and the application logic.
- `createDB.py`: Initializes the database tables.
- `addData.py`: Populates the database with initial user data.

#### **HTML Templates**
- **Role-based Dashboards**:
  - Admin Dashboard (`aAction.html`)
  - Contractor Dashboard (`cActions.html`)
  - Department Representative Dashboard (`drActions.html`)
- **Forms**:
  - Add Project (`add_project.html`)
  - Update Project Status (`update_project_status.html`)
  - Add Project Estimation (`add_estimation.html`)
  - Approve Forums (`approveforum.html`)

#### **CSS**
- `drForum.css`: Styles for the forum request interface.
- `drProject.css`: General styles for project-related interfaces.

#### **JavaScript**
- `forumModel.js`: Handles interactivity for the forum modal.
- `prModel.js`: Manages the "Add Project" modal functionality.

## Installation and Setup
### Prerequisites
1. Python 3.8 or higher
2. Flask
3. Flask-SQLAlchemy
4. SQLite
5. Bootstrap (for styling)
6. Gunicorn (for production deployment)

### Steps
1. Clone the repository:
   ```bash
   git clone <repository-url>
   cd QUIK
   ```

2. Create and activate a virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/Mac
   venv\Scripts\activate  # Windows
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Initialize the database:
   ```bash
   python createDB.py
   ```

5. Add initial user data:
   ```bash
   python addData.py
   ```

6. Run the application:
   ```bash
   flask run
   ```
   The application will be accessible at `http://127.0.0.1:5000/`.

## Usage
1. **Login**: Access the application by logging in as a Department Representative, Contractor, or Admin.
2. **Admin Actions**:
   - Approve forums.
   - Schedule projects.
3. **Contractor Actions**:
   - Submit project estimations.
   - Update project status.
   - Request forums for project discussions.
4. **Department Representative Actions**:
   - Add new projects.
   - Request forums.
   - View projects and guidelines.

## Contributions
Contributions to improve or extend QUIK are welcome. Please create a pull request or submit an issue in the repository.

## License
This project is licensed under the MIT License.

## Authors
Developed by DarkStarz (Anant Bhardwaj).

