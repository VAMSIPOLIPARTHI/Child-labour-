// Function to handle form submission
document.getElementById("incidentReportForm").addEventListener("submit", function(event) {
    event.preventDefault(); // Prevent the default form submission
  
    // Get form data
    const formData = {
      date: document.getElementById("incidentDate").value,
      time: document.getElementById("incidentTime").value,
      location: document.getElementById("incidentLocation").value,
      description: document.getElementById("incidentDescription").value,
      typeOfWork: document.getElementById("typeOfWork").value,
      // Add other form fields...
    };
  
    // Simulated API call to send form data to the server
    // Replace this with your actual API endpoint and handling
    simulateReportSubmission(formData);
  });
  
  // Simulated function to handle form submission (replace with actual API call)
  function simulateReportSubmission(formData) {
    // Simulated asynchronous API call
    setTimeout(() => {
      console.log("Report submitted:", formData);
  
      // Generate a random token number
      const tokenNumber = Math.floor(Math.random() * 1000000); // Generate a random number
  
      // Display a prompt message with the token number
      alert(`Report submitted successfully! Your token number is: ${tokenNumber}`);
  
      // Reset the form after submission if needed
      document.getElementById("incidentReportForm").reset();
    }, 1000); // Simulating a delay
  }
  