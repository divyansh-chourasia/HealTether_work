# HealTether screens

Three React screens for a clinic, and a shared text input. `package.json` is a Vite, React, and Tailwind setup named `test-vite-tailwindcss`, and it also depends on Chart.js. The repo has no `index.html`, no Vite config, and no file that renders `LoginPage`, `Dashboard`, or `PatientsRecord`.

`LoginPage/LoginPage.jsx` is a two-column sign-in. The left column says welcome, then the HealTether logo, "Empower your Practice!", and an "Approved by" line next to a National Health Authority image. Those two images are imported from `../assets/`. That folder is not here. `HealTetherLogo.png` and `national-health-authority.jpg` are in the repo root.

`LoginPage/LoginForm.jsx` keeps the form in component state and moves through three steps. Step 1 is a mobile number. Next goes to step 2. "Create new account" is text. Step 2 is a password. "Forgot Password?" jumps to step 3, which asks for a new password and a confirmation. Submit prints the fields to the console. It does not compare the two new passwords, and it does not sign anyone in. Previous on step 3 returns to the password step.

`Dashboard/Dashboard.jsx` greets Dr. Ajit Bhalla. A clock updates every second and shows hours and minutes. Next to the greeting is the weekday, the day of the month, and the month name. The patient search box, the help and notification icons, and Schedule Appointment do not change the page. The doughnut is Chart.js with fixed numbers: Remaining 4 and Completed 10. The label in the middle is `4/10`.

`PatientsRecord.jsx` is one long form: name and mobile, personal details, contact, file fields for medical records, payment history, procedure records, and appointment history, then ID, bank, and UPI fields. `FormInput.jsx` draws each row. Typing copies the field into React state when the input's `name` matches a key there. The birthday input is named `birhtday`, so it misses the `birthday` key. The inputs receive a `values` prop, so that state is not written back into them. Save Changes and Start Consultation submit the form, and the handler only calls `preventDefault`.
