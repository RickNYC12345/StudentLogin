<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tech Support Student Check-in</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f5f5f5;
        }
        h1 {
            color: #2c3e50;
            text-align: center;
        }
        .container {
            display: flex;
            flex-direction: column;
            max-width: 1200px;
            margin: 0 auto;
        }
        .form-container {
            background-color: white;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
            margin-bottom: 20px;
        }
        .list-container {
            background-color: white;
            border-radius: 8px;
            padding: 20px;
            box-shadow: 0 2px 4px rgba(0,0,0,0.1);
        }
        .form-group {
            margin-bottom: 15px;
        }
        .form-row {
            display: flex;
            gap: 15px;
        }
        .form-row .form-group {
            flex: 1;
        }
        label {
            display: block;
            margin-bottom: 5px;
            font-weight: bold;
        }
        input[type="text"], 
        input[type="number"],
        select {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 16px;
            box-sizing: border-box;
        }
        button {
            background-color: #3498db;
            color: white;
            border: none;
            padding: 12px 20px;
            border-radius: 4px;
            cursor: pointer;
            font-size: 16px;
            width: 100%;
        }
        button:hover {
            background-color: #2980b9;
        }
        .action-button {
            width: auto;
            margin-left: 10px;
        }
        table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 20px;
        }
        th, td {
            padding: 12px;
            text-align: left;
            border-bottom: 1px solid #ddd;
        }
        th {
            background-color: #f2f2f2;
        }
        tr:hover {
            background-color: #f5f5f5;
        }
        .header {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 20px;
        }
        .button-group {
            display: flex;
        }
        .date-display {
            font-size: 18px;
            font-weight: bold;
        }
        .error {
            color: red;
            margin-top: 5px;
        }
        .success {
            color: green;
            margin-top: 5px;
            text-align: center;
        }
        @media (max-width: 768px) {
            .container {
                padding: 10px;
            }
            .button-group {
                flex-direction: column;
            }
            .action-button {
                margin-left: 0;
                margin-top: 10px;
            }
            .form-row {
                flex-direction: column;
                gap: 0;
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Tech Support Student Check-in</h1>
        
        <div class="form-container">
            <div class="header">
                <h2>Student Check-in Form</h2>
                <div class="date-display" id="currentDate"></div>
            </div>
            
            <form id="checkInForm">
                <div class="form-group">
                    <label for="name">Full Name:</label>
                    <input type="text" id="name" name="name" required>
                </div>
                
                <div class="form-row">
                    <div class="form-group">
                        <label for="studentId">Student ID:</label>
                        <input type="text" id="studentId" name="studentId" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="technician">Tech:</label>
                        <input type="text" id="technician" name="technician" placeholder="Technician Initials" required>
                    </div>
                </div>
                
                <div class="form-group">
                    <label for="project">Project Description:</label>
                    <input type="text" id="project" name="project" required>
                </div>
                
                <div class="form-group">
                    <label for="level">Student Level:</label>
                    <select id="level" name="level" required>
                        <option value="">Select Level</option>
                        <option value="UG">UG</option>
                        <option value="PGT">PGT</option>
                        <option value="PGR">PGR</option>
                        <option value="Funded Research">Funded Research</option>
                        <option value="Teaching Support">Teaching Support</option>
                        <option value="Commercial">Commercial</option>
                        <option value="Outreach">Outreach</option>
                        <option value="Student Society">Student Society</option>
                        <option value="Technical Services">Technical Services</option>
                        <option value="Internal -work">Internal -work</option>
                        <option value="Misc">Misc</option>
                        <option value="Chemistry">Chemistry</option>
                        <option value="Physics">Physics</option>
                        <option value="Bio-Medical">Bio-Medical</option>
                    </select>
                </div>
                
                <button type="submit">Check In</button>
                <div id="formMessage" class="success"></div>
            </form>
        </div>
        
        <div class="list-container">
            <div class="header">
                <h2>Today's Check-ins</h2>
                <div class="button-group">
                    <button id="exportCsv" class="action-button">Export to CSV</button>
                </div>
            </div>
            
            <table>
                <thead>
                    <tr>
                        <th>Time</th>
                        <th>Name</th>
                        <th>Student ID</th>
                        <th>Tech</th>
                        <th>Project</th>
                        <th>Level</th>
                    </tr>
                </thead>
                <tbody id="checkinsList">
                    <!-- Student check-ins will be listed here -->
                </tbody>
            </table>
        </div>
    </div>

    <script>
        // Display current date
        function updateDate() {
            const now = new Date();
            const options = { weekday: 'long', year: 'numeric', month: 'long', day: 'numeric' };
            document.getElementById('currentDate').textContent = now.toLocaleDateString('en-US', options);
        }
        
        // Initialize app
        function initApp() {
            updateDate();
            loadCheckIns();
            
            // Form submission handler
            document.getElementById('checkInForm').addEventListener('submit', function(e) {
                e.preventDefault();
                
                const name = document.getElementById('name').value;
                const studentId = document.getElementById('studentId').value;
                const technician = document.getElementById('technician').value;
                const project = document.getElementById('project').value;
                const level = document.getElementById('level').value;
                
                if (!name || !studentId || !technician || !project || !level) {
                    showMessage('Please fill in all fields', 'error');
                    return;
                }
                
                addCheckIn(name, studentId, technician, project, level);
                this.reset();
                showMessage('Check-in successful!', 'success');
            });
            
            // Export to CSV
            document.getElementById('exportCsv').addEventListener('click', exportToCsv);
        }
        
        // Add a new check-in
        function addCheckIn(name, studentId, technician, project, level) {
            const now = new Date();
            const checkInTime = now.toLocaleTimeString('en-US', { hour: '2-digit', minute: '2-digit' });
            
            const checkIn = {
                time: checkInTime,
                date: now.toLocaleDateString('en-US'),
                name: name,
                studentId: studentId,
                technician: technician,
                project: project,
                level: level
            };
            
            // Get existing check-ins
            let checkIns = JSON.parse(localStorage.getItem('studentCheckIns')) || [];
            
            // Add new check-in
            checkIns.push(checkIn);
            
            // Save to localStorage
            localStorage.setItem('studentCheckIns', JSON.stringify(checkIns));
            
            // Refresh the list
            loadCheckIns();
        }
        
        // Load and display check-ins for today
        function loadCheckIns() {
            const checkInsList = document.getElementById('checkinsList');
            checkInsList.innerHTML = '';
            
            let checkIns = JSON.parse(localStorage.getItem('studentCheckIns')) || [];
            
            // Filter to show only today's check-ins
            const today = new Date().toLocaleDateString('en-US');
            checkIns = checkIns.filter(checkIn => checkIn.date === today);
            
            if (checkIns.length === 0) {
                checkInsList.innerHTML = '<tr><td colspan="6" style="text-align: center;">No check-ins yet today</td></tr>';
                return;
            }
            
            // Sort by time (most recent first)
            checkIns.sort((a, b) => {
                return new Date('1970/01/01 ' + b.time) - new Date('1970/01/01 ' + a.time);
            });
            
            // Display check-ins
            checkIns.forEach(checkIn => {
                const row = document.createElement('tr');
                row.innerHTML = `
                    <td>${checkIn.time}</td>
                    <td>${checkIn.name}</td>
                    <td>${checkIn.studentId}</td>
                    <td>${checkIn.technician || ''}</td>
                    <td>${checkIn.project}</td>
                    <td>${checkIn.level}</td>
                `;
                checkInsList.appendChild(row);
            });
        }
        
        // Export check-ins to CSV file
        function exportToCsv() {
            // Get all check-ins
            let checkIns = JSON.parse(localStorage.getItem('studentCheckIns')) || [];
            
            // Filter to show only today's check-ins
            const today = new Date().toLocaleDateString('en-US');
            const todaysCheckIns = checkIns.filter(checkIn => checkIn.date === today);
            
            if (todaysCheckIns.length === 0) {
                alert('No check-ins to export');
                return;
            }
            
            // Sort by time (earliest first for CSV)
            todaysCheckIns.sort((a, b) => {
                return new Date('1970/01/01 ' + a.time) - new Date('1970/01/01 ' + b.time);
            });
            
            // Create CSV header
            let csvContent = 'Date,Time,Name,Student ID,Technician,Project,Level\r\n';
            
            // Add each check-in as a row
            todaysCheckIns.forEach(checkIn => {
                // Escape fields that might contain commas
                const escapedName = `"${checkIn.name.replace(/"/g, '""')}"`;
                const escapedProject = `"${checkIn.project.replace(/"/g, '""')}"`;
                const escapedTech = checkIn.technician ? `"${checkIn.technician.replace(/"/g, '""')}"` : '';
                
                csvContent += `${checkIn.date},${checkIn.time},${escapedName},${checkIn.studentId},${escapedTech},${escapedProject},${checkIn.level}\r\n`;
            });
            
            // Create a download link
            const encodedUri = 'data:text/csv;charset=utf-8,' + encodeURIComponent(csvContent);
            const link = document.createElement('a');
            
            // Format today's date for the filename (YYYY-MM-DD format)
            const dateObj = new Date();
            const year = dateObj.getFullYear();
            const month = String(dateObj.getMonth() + 1).padStart(2, '0');
            const day = String(dateObj.getDate()).padStart(2, '0');
            const formattedDate = `${year}-${month}-${day}`;
            
            link.setAttribute('href', encodedUri);
            link.setAttribute('download', `student-checkins-${formattedDate}.csv`);
            document.body.appendChild(link);
            
            // Trigger the download
            link.click();
            
            // Clean up
            document.body.removeChild(link);
        }
        
        // Show message to the user
        function showMessage(message, type) {
            const messageElement = document.getElementById('formMessage');
            messageElement.textContent = message;
            messageElement.className = type;
            
            // Clear message after 3 seconds
            setTimeout(() => {
                messageElement.textContent = '';
            }, 3000);
        }
        
        // Initialize the app when the page loads
        window.addEventListener('load', initApp);
    </script>
</body>
</html>
