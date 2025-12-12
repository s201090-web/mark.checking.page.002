# mark.checking.page.002


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>School Management System Login</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background: linear-gradient(135deg, #1a2980, #26d0ce);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }
        
        .container {
            width: 100%;
            max-width: 480px;
            background-color: rgba(255, 255, 255, 0.95);
            border-radius: 20px;
            box-shadow: 0 15px 35px rgba(0, 0, 0, 0.2);
            overflow: hidden;
        }
        
        .header {
            background: linear-gradient(to right, #2c3e50, #4a6491);
            color: white;
            padding: 30px 30px;
            text-align: center;
            position: relative;
        }
        
        .header h1 {
            font-size: 28px;
            margin-bottom: 8px;
            letter-spacing: 1px;
        }
        
        .header p {
            opacity: 0.9;
            font-size: 15px;
        }
        
        .logo {
            position: absolute;
            top: 25px;
            left: 30px;
            width: 50px;
            height: 50px;
            background-color: #fff;
            border-radius: 50%;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #2c3e50;
            font-size: 24px;
            font-weight: bold;
        }
        
        .login-form {
            padding: 35px 40px;
        }
        
        .user-type-selector {
            display: flex;
            border-radius: 10px;
            overflow: hidden;
            margin-bottom: 30px;
            border: 2px solid #e1e5ee;
        }
        
        .user-type {
            flex: 1;
            text-align: center;
            padding: 15px 5px;
            background-color: #f8f9fa;
            cursor: pointer;
            transition: all 0.3s;
            font-weight: 600;
            color: #555;
        }
        
        .user-type i {
            display: block;
            font-size: 22px;
            margin-bottom: 8px;
        }
        
        .user-type.active {
            background-color: #3498db;
            color: white;
        }
        
        .user-type:nth-child(2).active {
            background-color: #2ecc71;
        }
        
        .user-type:nth-child(3).active {
            background-color: #9b59b6;
        }
        
        .user-type:hover:not(.active) {
            background-color: #e9ecef;
        }
        
        .form-group {
            margin-bottom: 25px;
        }
        
        .form-group label {
            display: block;
            margin-bottom: 8px;
            color: #2c3e50;
            font-weight: 600;
            font-size: 15px;
        }
        
        .form-control {
            width: 100%;
            padding: 15px;
            border: 2px solid #e1e5ee;
            border-radius: 10px;
            font-size: 16px;
            transition: all 0.3s;
        }
        
        .form-control:focus {
            border-color: #3498db;
            outline: none;
            box-shadow: 0 0 0 3px rgba(52, 152, 219, 0.2);
        }
        
        .btn-login {
            width: 100%;
            padding: 17px;
            background: linear-gradient(to right, #2c3e50, #4a6491);
            color: white;
            border: none;
            border-radius: 10px;
            font-size: 18px;
            font-weight: 600;
            cursor: pointer;
            transition: all 0.3s;
            margin-top: 10px;
            letter-spacing: 1px;
        }
        
        .btn-login:hover {
            background: linear-gradient(to right, #34495e, #5a7ab8);
            transform: translateY(-2px);
            box-shadow: 0 5px 15px rgba(0, 0, 0, 0.1);
        }
        
        .btn-login:active {
            transform: translateY(0);
        }
        
        .info-box {
            background-color: #f8f9fa;
            border-radius: 10px;
            padding: 18px;
            margin-top: 25px;
            font-size: 14px;
            color: #555;
            border-left: 4px solid #3498db;
        }
        
        .info-box h3 {
            color: #2c3e50;
            margin-bottom: 10px;
            font-size: 16px;
        }
        
        .info-box ul {
            padding-left: 20px;
        }
        
        .info-box li {
            margin-bottom: 6px;
        }
        
        .footer {
            text-align: center;
            padding: 20px;
            color: #7f8c8d;
            font-size: 14px;
            border-top: 1px solid #eee;
        }
        
        @media (max-width: 500px) {
            .container {
                max-width: 95%;
            }
            
            .login-form {
                padding: 25px 20px;
            }
            
            .header {
                padding: 20px 15px;
            }
            
            .logo {
                position: relative;
                top: 0;
                left: 0;
                margin: 0 auto 15px;
            }
            
            .header h1 {
                font-size: 24px;
            }
        }
        
        /* Animation effects */
        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }
        
        .form-group, .user-type-selector, .btn-login, .info-box {
            animation: fadeIn 0.5s ease-out forwards;
            opacity: 0;
        }
        
        .user-type-selector { animation-delay: 0.1s; }
        .form-group:nth-child(2) { animation-delay: 0.2s; }
        .form-group:nth-child(3) { animation-delay: 0.3s; }
        .btn-login { animation-delay: 0.4s; }
        .info-box { animation-delay: 0.5s; }
        
        .demo-accounts {
            margin-top: 20px;
            padding: 15px;
            background-color: #e8f4fc;
            border-radius: 10px;
            font-size: 13px;
            color: #2c3e50;
        }
        
        .demo-accounts h4 {
            margin-bottom: 8px;
            font-size: 14px;
        }
        
        .demo-accounts p {
            margin-bottom: 5px;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <div class="logo">
                <i class="fas fa-graduation-cap"></i>
            </div>
            <h1>School Management System</h1>
            <p>Please select your role and enter credentials</p>
        </div>
        
        <div class="login-form">
            <div class="user-type-selector">
                <div class="user-type active" data-type="student">
                    <i class="fas fa-user-graduate"></i>
                    <span>Student</span>
                </div>
                <div class="user-type" data-type="teacher">
                    <i class="fas fa-chalkboard-teacher"></i>
                    <span>Teacher</span>
                </div>
                <div class="user-type" data-type="principal">
                    <i class="fas fa-user-tie"></i>
                    <span>Principal</span>
                </div>
            </div>
            
            <div class="form-group">
                <label for="user-id"><i class="fas fa-id-card"></i> ID Number</label>
                <input type="text" id="user-id" class="form-control" placeholder="Enter your student ID">
            </div>
            
            <div class="form-group">
                <label for="password"><i class="fas fa-lock"></i> Password</label>
                <input type="password" id="password" class="form-control" placeholder="Enter your password">
            </div>
            
            <button class="btn-login" id="login-btn">
                <i class="fas fa-sign-in-alt"></i> Login
            </button>
            
            <div class="info-box">
                <h3><i class="fas fa-info-circle"></i> Login Information by Role</h3>
                <ul>
                    <li><strong>Student</strong>: Use your student ID and personal password</li>
                    <li><strong>Teacher</strong>: Use your teacher ID and assigned password</li>
                    <li><strong>Principal</strong>: Use administrator credentials for full access</li>
                </ul>
            </div>
            
            <div class="demo-accounts">
                <h4><i class="fas fa-key"></i> Demo Accounts (for testing):</h4>
                <p><strong>Student</strong>: ID: S1001 | Password: student123</p>
                <p><strong>Teacher</strong>: ID: T2001 | Password: teacher123</p>
                <p><strong>Principal</strong>: ID: P3001 | Password: principal123</p>
            </div>
        </div>
        
        <div class="footer">
            <p>&copy; 2023 School Management System | For Educational Purposes</p>
        </div>
    </div>


    <script>
        // Select user type
        const userTypes = document.querySelectorAll('.user-type');
        let selectedUserType = 'student';
        
        userTypes.forEach(type => {
            type.addEventListener('click', function() {
                // Remove active class from all
                userTypes.forEach(t => t.classList.remove('active'));
                // Add active class to clicked element
                this.classList.add('active');
                // Update selected user type
                selectedUserType = this.getAttribute('data-type');
                
                // Update placeholder based on selected role
                const idInput = document.getElementById('user-id');
                
                switch(selectedUserType) {
                    case 'student':
                        idInput.placeholder = 'Enter your student ID';
                        break;
                    case 'teacher':
                        idInput.placeholder = 'Enter your teacher ID';
                        break;
                    case 'principal':
                        idInput.placeholder = 'Enter administrator ID';
                        break;
                }
            });
        });
        
        // Login button click event
        document.getElementById('login-btn').addEventListener('click', function() {
            const userId = document.getElementById('user-id').value.trim();
            const password = document.getElementById('password').value.trim();
            
            // Simple validation
            if (!userId) {
                alert('Please enter your ID number!');
                document.getElementById('user-id').focus();
                return;
            }
            
            if (!password) {
                alert('Please enter your password!');
                document.getElementById('password').focus();
                return;
            }
            
            // Button animation and state change
            const btn = this;
            const originalText = btn.innerHTML;
            btn.innerHTML = '<i class="fas fa-spinner fa-spin"></i> Logging in...';
            btn.disabled = true;
            
            // Simulate login process (replace with actual authentication)
            setTimeout(() => {
                // Demo credentials for testing
                const demoAccounts = {
                    'student': {id: 'S1001', password: 'student123'},
                    'teacher': {id: 'T2001', password: 'teacher123'},
                    'principal': {id: 'P3001', password: 'principal123'}
                };
                
                // Check if using demo credentials
                const demoAccount = demoAccounts[selectedUserType];
                let loginSuccess = false;
                let message = '';
                
                if (userId === demoAccount.id && password === demoAccount.password) {
                    loginSuccess = true;
                    message = `Login successful!\nRole: ${getUserTypeName(selectedUserType)}\nID: ${userId}\n\n(Demo mode - would redirect to dashboard in real system)`;
                } else {
                    // For any other credentials, show success (for demo purposes)
                    loginSuccess = true;
                    message = `Login successful!\nRole: ${getUserTypeName(selectedUserType)}\nID: ${userId}\n\n(Note: This is a demo. In a real system, credentials would be validated.)`;
                }
                
                if (loginSuccess) {
                    btn.innerHTML = '<i class="fas fa-check"></i> Login Successful!';
                    btn.style.background = 'linear-gradient(to right, #27ae60, #2ecc71)';
                    
                    setTimeout(() => {
                        alert(message);
                        
                        // Reset button
                        btn.innerHTML = originalText;
                        btn.style.background = 'linear-gradient(to right, #2c3e50, #4a6491)';
                        btn.disabled = false;
                        
                        // Clear form (optional)
                        // document.getElementById('user-id').value = '';
                        // document.getElementById('password').value = '';
                    }, 500);
                }
            }, 1500);
        });
        
        // Login on Enter key press
        document.getElementById('password').addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                document.getElementById('login-btn').click();
            }
        });
        
        // Get user type name for display
        function getUserTypeName(type) {
            switch(type) {
                case 'student': return 'Student';
                case 'teacher': return 'Teacher';
                case 'principal': return 'Principal';
                default: return 'User';
            }
        }
        
        // Pre-fill demo credentials on click (for easier testing)
        document.addEventListener('DOMContentLoaded', function() {
            // Add click event to demo accounts to auto-fill
            const demoAccountsSection = document.querySelector('.demo-accounts');
            demoAccountsSection.addEventListener('click', function(e) {
                if (e.target.tagName === 'P' || e.target.tagName === 'STRONG') {
                    const text = e.target.textContent || e.target.parentElement.textContent;
                    
                    if (text.includes('Student')) {
                        // Set to student and fill credentials
                        userTypes[0].click();
                        document.getElementById('user-id').value = 'S1001';
                        document.getElementById('password').value = 'student123';
                    } else if (text.includes('Teacher')) {
                        // Set to teacher and fill credentials
                        userTypes[1].click();
                        document.getElementById('user-id').value = 'T2001';
                        document.getElementById('password').value = 'teacher123';
                    } else if (text.includes('Principal')) {
                        // Set to principal and fill credentials
                        userTypes[2].click();
                        document.getElementById('user-id').value = 'P3001';
                        document.getElementById('password').value = 'principal123';
                    }
                }
            });
        });
    </script>
</body>
</html>


