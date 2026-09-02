// ======================================================
// PUBLIC INFRASTRUCTURE REPORTING SYSTEM
// MAIN JAVASCRIPT
// ======================================================


// ======================================================
// REGISTER
// ======================================================

const registerForm = document.getElementById("registerForm");

if (registerForm) {

    registerForm.addEventListener("submit", function (event) {

        event.preventDefault();

        const name = document.getElementById("name").value.trim();
        const email = document.getElementById("email").value.trim();
        const password = document.getElementById("password").value;
        const confirmPassword =
            document.getElementById("confirmPassword").value;


        // Check password
        if (password !== confirmPassword) {

            alert("Passwords do not match.");

            return;
        }


        // Get existing users
        let users =
            JSON.parse(localStorage.getItem("users")) || [];


        // Check existing email
        const alreadyExists = users.some(function (user) {

            return user.email.toLowerCase() === email.toLowerCase();

        });


        if (alreadyExists) {

            alert("This Email ID is already registered.");

            return;
        }


        // Create new account
        const newUser = {

            name: name,

            email: email,

            password: password

        };


        // Save user
        users.push(newUser);

        localStorage.setItem(
            "users",
            JSON.stringify(users)
        );


        alert("Account created successfully!");


        // Go to login
        window.location.href = "index.html";

    });
}



// ======================================================
// LOGIN
// ======================================================

const loginForm = document.getElementById("loginForm");

if (loginForm) {

    loginForm.addEventListener("submit", function (event) {

        event.preventDefault();

        const email =
            document.getElementById("email").value.trim();

        const password =
            document.getElementById("password").value;


        // Get users
        const users =
            JSON.parse(localStorage.getItem("users")) || [];


        // Find user
        const user = users.find(function (account) {

            return (
                account.email.toLowerCase() ===
                email.toLowerCase()
                &&
                account.password === password
            );

        });


        if (!user) {

            alert("Invalid Email ID or Password.");

            return;
        }


        // Save logged-in user
        localStorage.setItem(
            "loggedInUser",
            JSON.stringify(user)
        );


        alert("Login successful!");


        // Open dashboard
        window.location.href = "dashboard.html";

    });
}



// ======================================================
// REPORT ISSUE
// ======================================================

const reportForm = document.getElementById("reportForm");

if (reportForm) {

    const imageInput =
        document.getElementById("image");

    const imagePreview =
        document.getElementById("imagePreview");

    const locationBtn =
        document.getElementById("locationBtn");



    // --------------------------------------------------
    // IMAGE PREVIEW
    // --------------------------------------------------

    if (imageInput) {

        imageInput.addEventListener(
            "change",
            function () {

                const file = imageInput.files[0];

                if (!file) {

                    imagePreview.innerHTML = "";

                    return;
                }


                const reader =
                    new FileReader();


                reader.onload = function (event) {

                    imagePreview.innerHTML = `
                        <img
                            src="${event.target.result}"
                            alt="Issue Image"
                            style="
                                width:200px;
                                max-width:100%;
                                margin-top:10px;
                                border-radius:8px;
                            ">
                    `;

                };


                reader.readAsDataURL(file);

            }
        );

    }



    // --------------------------------------------------
    // LOCATION DETECTION
    // --------------------------------------------------

    if (locationBtn) {

        locationBtn.addEventListener(
            "click",
            function () {

                if (!navigator.geolocation) {

                    alert(
                        "Location detection is not supported."
                    );

                    return;
                }


                locationBtn.textContent =
                    "Detecting location...";


                navigator.geolocation.getCurrentPosition(

                    function (position) {

                        const latitude =
                            position.coords.latitude;

                        const longitude =
                            position.coords.longitude;


                        document.getElementById(
                            "location"
                        ).value =
                            latitude +
                            ", " +
                            longitude;


                        locationBtn.textContent =
                            "📍 Location Detected";

                    },


                    function () {

                        alert(
                            "Unable to detect location. Please enter it manually."
                        );


                        locationBtn.textContent =
                            "📍 Detect My Location";

                    }

                );

            }
        );

    }



    // --------------------------------------------------
    // SUBMIT REPORT
    // --------------------------------------------------

    reportForm.addEventListener(
        "submit",
        function (event) {

            event.preventDefault();


            const category =
                document.getElementById(
                    "category"
                ).value;


            const description =
                document.getElementById(
                    "description"
                ).value.trim();


            const location =
                document.getElementById(
                    "location"
                ).value.trim();


            const imageFile =
                imageInput.files[0];


            // Check fields
            if (
                !category ||
                !description ||
                !location
            ) {

                alert(
                    "Please fill all required fields."
                );

                return;
            }


            // Check login
            const loggedInUser =
                JSON.parse(
                    localStorage.getItem(
                        "loggedInUser"
                    )
                );


            if (!loggedInUser) {

                alert(
                    "Please login before submitting a report."
                );


                window.location.href =
                    "index.html";


                return;
            }


            // If image exists, read it first
            if (imageFile) {

                const reader =
                    new FileReader();


                reader.onload = function (event) {

                    saveReport(
                        event.target.result
                    );

                };


                reader.readAsDataURL(
                    imageFile
                );

            } else {

                saveReport("");

            }

        }
    );



    // --------------------------------------------------
    // SAVE REPORT
    // --------------------------------------------------

    function saveReport(imageData) {

        const loggedInUser =
            JSON.parse(
                localStorage.getItem(
                    "loggedInUser"
                )
            );


        let reports =
            JSON.parse(
                localStorage.getItem(
                    "reports"
                )
            ) || [];


        const newReport = {

            id: Date.now(),

            userName:
                loggedInUser.name,

            userEmail:
                loggedInUser.email,

            category:
                document.getElementById(
                    "category"
                ).value,

            description:
                document.getElementById(
                    "description"
                ).value.trim(),

            location:
                document.getElementById(
                    "location"
                ).value.trim(),

            image:
                imageData,

            status:
                "Submitted",

            createdAt:
                new Date().toLocaleString()

        };


        // Add report
        reports.push(newReport);


        // Save reports
        localStorage.setItem(
            "reports",
            JSON.stringify(reports)
        );


        // Success
        alert(
            "Report submitted successfully!"
        );


        // Clear form
        reportForm.reset();


        if (imagePreview) {

            imagePreview.innerHTML = "";

        }


        if (locationBtn) {

            locationBtn.textContent =
                "📍 Detect My Location";

        }

    }

}