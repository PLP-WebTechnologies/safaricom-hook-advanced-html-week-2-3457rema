### Assignment: Building a Multimedia Webpage and a Registration Form  

#### Objective: 
The goal of this assignment is to create a multimedia-rich webpage featuring audio and video elements and design a simple registration form with built-in HTML validation.  

---

### Part 1: Multimedia Webpage 
Create an HTML webpage that includes the following:  
1. **Audio Element**:  
   - Add an audio file using the `<audio>` tag.  
   - Provide controls to play, pause, and adjust the volume.  
   - Use at least one source format (e.g., `.mp3` or `.ogg`).  

2. **Video Element**:  
   - Add a video file using the `<video>` tag.  
   - Provide controls to play, pause, and adjust the volume.  
   - Include at least two source formats for compatibility (e.g., `.mp4` and `.webm`).  
   - Add a poster image that displays before the video plays.  

**Example Output:**  
A webpage where users can play an audio track and watch a video.  

---

### **Part 2: Registration Form **  
Design a user registration form with the following requirements:  

1. **Form Elements**:  
   - Full Name (Text input)  
   - Email Address (Input of type `email`)  
   - Password (Input of type `password`)  
   - Age (Input of type `number`, with a minimum value of 18)  
   - Gender (Radio buttons for Male, Female, Other)  
   - Terms and Conditions (Checkbox to agree before submitting)  

2. **Validation**:  
   - Use HTML5 validation attributes such as `required`, `min`, `maxlength`, etc.  
   - Ensure the email field has proper validation for email format.  
   - Make the password field require at least 8 characters.  

3. **Submit Button**:  
   - Include a "Register" button to submit the form.  

**Example Output:**  
A user-friendly registration form that prevents submission if required fields are not filled correctly.  
  Solution


  Part 1: Multimedia Webpage
html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Multimedia Webpage</title>
</head>
<body>
    <h1>Welcome to My Multimedia Page</h1>

    <h2>Audio Player</h2>
    <audio controls>
        <source src="audio.mp3" type="audio/mp3">
        <source src="audio.ogg" type="audio/ogg">
        Your browser does not support the audio element.
    </audio>

    <h2>Video Player</h2>
    <video controls poster="poster-image.jpg">
        <source src="video.mp4" type="video/mp4">
        <source src="video.webm" type="video/webm">
        Your browser does not support the video element.
    </video>

</body>
</html>
Part 2: Registration Form
html
Copy code
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Registration Form</title>
</head>
<body>
    <h1>User Registration</h1>

    <form action="submit_form.php" method="post" novalidate>
        <label for="fullname">Full Name:</label>
        <input type="text" id="fullname" name="fullname" required maxlength="100">
        <br><br>

        <label for="email">Email Address:</label>
        <input type="email" id="email" name="email" required>
        <br><br>

        <label for="password">Password:</label>
        <input type="password" id="password" name="password" required minlength="8">
        <br><br>

        <label for="age">Age:</label>
        <input type="number" id="age" name="age" required min="18">
        <br><br>

        <label>Gender:</label>
        <input type="radio" id="male" name="gender" value="male" required> Male
        <input type="radio" id="female" name="gender" value="female" required> Female
        <input type="radio" id="other" name="gender" value="other" required> Other
        <br><br>

        <label for="terms">
            <input type="checkbox" id="terms" name="terms" required>
            I agree to the Terms and Conditions
        </label>
        <br><br>

        <button type="submit">Register</button>
    </form>

</body>
</html>
