function toggleForm() {
    var loginForm = document.getElementById("loginForm");
    var signupForm = document.getElementById("signupForm");
  
    loginForm.style.display = (loginForm.style.display === "none") ? "block" : "none";
    signupForm.style.display = (signupForm.style.display === "none") ? "block" : "none";
  }
  
  function validateLoginForm() {
    var email = document.getElementById("loginEmail").value;
    var password = document.getElementById("loginPassword").value;
  
    // Example validation (check if email contains '@')
    if (!email.includes('@')) {
      alert("Invalid email!");
      return false;
    }
  
    // Other validations as needed...
  
    // If all validations pass, navigate to another page
    window.location.href = 'dashboard.html';
    // Replace with your desired URL
    return false; // Prevents the form from submitting normally
  }
  
  function validateSignupForm() {
    var signupEmail = document.getElementById("signupEmail").value;
    var signupPassword = document.getElementById("signupPassword").value;
    var confirmPassword = document.getElementById("confirmPassword").value;
  
    // Example validation (check if passwords match)
    if (signupPassword !== confirmPassword) {
      alert("Passwords do not match!");
      return false;
    }
  
    // Other validations as needed...
  
    // If all validations pass, navigate to another page
    window.location.href = "login.html"; // Replace with your desired URL
    return false; // Prevents the form from submitting normally
  }
  