function registerUser() {
    const name = document.getElementById("name").value.trim();
    const email = document.getElementById("email").value.trim();
    const gender = document.getElementById("gender").value;
    const dob = document.getElementById("dob").value;
    const address = document.getElementById("address").value.trim();
    const age = document.getElementById("age").value.trim();
    if (!name || !email || !gender || !dob || !address || !age) {
        alert("Please fill out all fields.");
        return;
    }

    const output = document.getElementById("output");
    output.style.display = "block";
    output.innerHTML = `
        <h3>Registration Details</h3>
        <p><strong>Name:</strong> ${name}</p>
        <p><strong>Email:</strong> ${email}</p>
        <p><strong>Gender:</strong> ${gender}</p>
        <p><strong>Date of Birth:</strong> ${dob}</p>
        <p><strong>Address:</strong> ${address}</p>
        <p><strong>Age:</strong> ${age}</p>
    `;
    document.getElementById("regForm").reset();
}
