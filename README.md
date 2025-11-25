# Cover Letter Generator
The Cover Letter Generator is a simple and efficient tool designed to help users create professional and personalized cover letters quickly. It allows users to input their personal details, job information, and career highlights, and then generates a tailored cover letter that can be copied or downloaded.
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Cover Letter Generator</title>
    <style>
        :root {
            --primary-color: #3498db;
            --secondary-color: #2980b9;
            --light-color: #ecf0f1;
            --dark-color: #2c3e50;
            --success-color: #2ecc71;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }
        
        body {
            background-color: #f5f5f5;
            color: #333;
            line-height: 1.6;
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }
        
        header {
            background-color: var(--dark-color);
            color: white;
            padding: 20px 0;
            text-align: center;
            margin-bottom: 30px;
            box-shadow: 0 2px 5px rgba(0,0,0,0.1);
        }
        
        h1 {
            font-size: 2.5rem;
            margin-bottom: 10px;
        }
        
        .subtitle {
            font-size: 1.2rem;
            opacity: 0.9;
        }
        
        .main-content {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
        }
        
        .form-section, .preview-section {
            flex: 1;
            min-width: 300px;
            background-color: white;
            padding: 25px;
            border-radius: 8px;
            box-shadow: 0 2px 10px rgba(0,0,0,0.1);
        }
        
        .section-title {
            color: var(--primary-color);
            margin-bottom: 20px;
            padding-bottom: 10px;
            border-bottom: 2px solid var(--light-color);
        }
        
        .form-group {
            margin-bottom: 20px;
        }
        
        label {
            display: block;
            margin-bottom: 8px;
            font-weight: 600;
            color: var(--dark-color);
        }
        
        input, textarea, select {
            width: 100%;
            padding: 12px;
            border: 1px solid #ddd;
            border-radius: 4px;
            font-size: 16px;
            transition: border 0.3s;
        }
        
        input:focus, textarea:focus, select:focus {
            border-color: var(--primary-color);
            outline: none;
        }
        
        textarea {
            min-height: 120px;
            resize: vertical;
        }
        
        button {
            background-color: var(--primary-color);
            color: white;
            border: none;
            padding: 12px 20px;
            font-size: 16px;
            border-radius: 4px;
            cursor: pointer;
            transition: background-color 0.3s;
        }
        
        button:hover {
            background-color: var(--secondary-color);
        }
        
        .cover-letter {
            padding: 20px;
            border: 1px solid #ddd;
            border-radius: 4px;
            background-color: white;
            white-space: pre-line;
            line-height: 1.8;
        }
        
        .cover-letter p {
            margin-bottom: 15px;
        }
        
        .action-buttons {
            display: flex;
            gap: 10px;
            margin-top: 20px;
        }
        
        .btn-secondary {
            background-color: #95a5a6;
        }
        
        .btn-secondary:hover {
            background-color: #7f8c8d;
        }
        
        .btn-success {
            background-color: var(--success-color);
        }
        
        .btn-success:hover {
            background-color: #27ae60;
        }
        
        footer {
            text-align: center;
            margin-top: 50px;
            padding: 20px;
            color: #7f8c8d;
            font-size: 0.9rem;
        }
        
        @media (max-width: 768px) {
            .main-content {
                flex-direction: column;
            }
        }
    </style>
</head>
<body>
    <header>
        <div class="container">
            <h1>Cover Letter Generator</h1>
            <p class="subtitle">Create professional cover letters in minutes</p>
        </div>
    </header>
    
    <div class="container">
        <div class="main-content">
            <section class="form-section">
                <h2 class="section-title">Your Information</h2>
                <form id="coverLetterForm">
                    <div class="form-group">
                        <label for="yourName">Your Full Name</label>
                        <input type="text" id="yourName" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="yourAddress">Your Address</label>
                        <input type="text" id="yourAddress" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="yourEmail">Your Email</label>
                        <input type="email" id="yourEmail" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="yourPhone">Your Phone Number</label>
                        <input type="tel" id="yourPhone" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="currentDate">Date</label>
                        <input type="date" id="currentDate" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="employerName">Hiring Manager's Name</label>
                        <input type="text" id="employerName" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="companyName">Company Name</label>
                        <input type="text" id="companyName" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="companyAddress">Company Address</label>
                        <input type="text" id="companyAddress" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="jobTitle">Job Title You're Applying For</label>
                        <input type="text" id="jobTitle" required>
                    </div>
                    
                    <div class="form-group">
                        <label for="jobSource">Where Did You Find This Job?</label>
                        <select id="jobSource">
                            <option value="LinkedIn">LinkedIn</option>
                            <option value="Company Website">Company Website</option>
                            <option value="Job Board">Job Board</option>
                            <option value="Recruiter">Recruiter</option>
                            <option value="Referral">Referral</option>
                            <option value="Other">Other</option>
                        </select>
                    </div>
                    
                    <div class="form-group">
                        <label for="skillsMatch">How Your Skills Match the Job</label>
                        <textarea id="skillsMatch" required></textarea>
                    </div>
                    
                    <div class="form-group">
                        <label for="achievements">Your Relevant Achievements</label>
                        <textarea id="achievements" required></textarea>
                    </div>
                    
                    <div class="form-group">
                        <label for="enthusiasm">Why You're Excited About This Role</label>
                        <textarea id="enthusiasm" required></textarea>
                    </div>
                    
                    <div class="action-buttons">
                        <button type="button" id="generateBtn" class="btn-primary">Generate Cover Letter</button>
                        <button type="reset" class="btn-secondary">Reset Form</button>
                    </div>
                </form>
            </section>
            
            <section class="preview-section">
                <h2 class="section-title">Cover Letter Preview</h2>
                <div id="coverLetterPreview" class="cover-letter">
                    <p>Your generated cover letter will appear here.</p>
                    <p>Fill out the form on the left and click "Generate Cover Letter" to create your personalized cover letter.</p>
                </div>
                
                <div class="action-buttons">
                    <button id="downloadBtn" class="btn-success" disabled>Download as PDF</button>
                    <button id="copyBtn" class="btn-secondary" disabled>Copy to Clipboard</button>
                </div>
            </section>
        </div>
    </div>
    
    <footer>
        <div class="container">
            <p>©️ 2023 Cover Letter Generator | All Rights Reserved</p>
        </div>
    </footer>
    
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const today = new Date().toISOString().split('T')[0];
            document.getElementById('currentDate').value = today;
            
            document.getElementById('generateBtn').addEventListener('click', generateCoverLetter);
            
            document.getElementById('copyBtn').addEventListener('click', copyToClipboard);
            
            document.getElementById('downloadBtn').addEventListener('click', downloadAsPDF);
            
            function generateCoverLetter() {
                const yourName = document.getElementById('yourName').value;
                const yourAddress = document.getElementById('yourAddress').value;
                const yourEmail = document.getElementById('yourEmail').value;
                const yourPhone = document.getElementById('yourPhone').value;
                const currentDate = formatDate(document.getElementById('currentDate').value);
                const employerName = document.getElementById('employerName').value;
                const companyName = document.getElementById('companyName').value;
                const companyAddress = document.getElementById('companyAddress').value;
                const jobTitle = document.getElementById('jobTitle').value;
                const jobSource = document.getElementById('jobSource').value;
                const skillsMatch = document.getElementById('skillsMatch').value;
                const achievements = document.getElementById('achievements').value;
                const enthusiasm = document.getElementById('enthusiasm').value;
                
                if (!yourName || !yourAddress || !employerName || !companyName || !jobTitle) {
                    alert('Please fill in all required fields.');
                    return;
                }
                
                const coverLetter = `
${yourName}
${yourAddress}
${yourEmail} | ${yourPhone}
${currentDate}

${employerName}
${companyName}
${companyAddress}

Dear ${employerName},

I am excited to apply for the ${jobTitle} position at ${companyName}. I found this opportunity through ${jobSource} and after reviewing the job description, I believe my skills and experience align perfectly with your requirements.

${skillsMatch}

Some of my relevant achievements include:
${achievements}

${enthusiasm}

I would welcome the opportunity to discuss how my background and skills would be a great fit for ${companyName}. Thank you for your time and consideration. I look forward to the possibility of contributing to your team and am available at your earliest convenience for an interview.

Sincerely,
${yourName}
                `;
                
                document.getElementById('coverLetterPreview').innerHTML = coverLetter;
                
                document.getElementById('downloadBtn').disabled = false;
                document.getElementById('copyBtn').disabled = false;
            }
            
            function formatDate(dateString) {
                const options = { year: 'numeric', month: 'long', day: 'numeric' };
                return new Date(dateString).toLocaleDateString('en-US', options);
            }
            
            function copyToClipboard() {
                const coverLetter = document.getElementById('coverLetterPreview').textContent;
                navigator.clipboard.writeText(coverLetter)
                    .then(() => {
                        alert('Cover letter copied to clipboard!');
                    })
                    .catch(err => {
                        console.error('Failed to copy: ', err);
                        alert('Failed to copy cover letter. Please try again.');
                    });
            }
            
            function downloadAsPDF() {
                alert('In a real implementation, this would download a PDF. For this demo, please use the "Copy to Clipboard" button instead.');
            }
        });
    </script>
</body>
</html>
