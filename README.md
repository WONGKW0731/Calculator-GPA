# Professional GPA Calculator 📊

A feature-rich, client-side web application designed to help users calculate their Grade Point Average (GPA) with detailed control over subjects, coursework, and final exams. It boasts a clean, professional user interface, provides insightful grade predictions, and persists all data locally in the browser.

<!-- Optional: Add a screenshot or GIF here -->
![image](https://github.com/user-attachments/assets/bc1c8db4-dd94-405b-9c22-0f66c71e4077)



## ✨ Core Features

*   **📚 Dynamic Subject Management:**
    *   Add multiple subjects to calculate GPA.
    *   Assign custom names to each subject (e.g., "Introduction to Programming").
    *   Easily remove individual subjects with a confirmation prompt.

*   **📝 Detailed Grade Input per Subject:**
    *   **Credit Hours:** Specify the credit hours for each subject.
    *   **Final Exam Configuration:**
        *   Toggle whether a subject has a final exam.
        *   If yes, select the **Coursework to Final Exam Ratio** (e.g., 50:50, 60:40, 70:30, 40:60).
        *   Input **Final Exam Marks** (0-100).
    *   **Granular Coursework Breakdown:**
        *   Specify the **Number of Coursework Parts** for each subject (1-10 parts).
        *   For each part, input:
            *   Marks obtained (0-100).
            *   Ratio/Weighting of that part towards the total coursework grade (e.g., Assignment 1 - 40%, Quiz - 20%).
        *   Real-time validation ensures coursework part ratios sum to 100%.

*   **🧮 GPA Calculation & Comprehensive Results:**
    *   **Overall GPA:** A main button triggers the calculation, displaying the cumulative GPA.
    *   **Individual Subject Results:** For each subject, view:
        *   Subject Name
        *   Total Marks (%)
        *   Subject-specific GPA
        *   Letter Grade (e.g., A+, B, C-)
        *   Coursework/Final exam contribution split, if applicable.
    *   **Grading Scale Reference:** An easily accessible, collapsible section displays the grading scale used (Percentage Range, Letter Grade, GPA Point).

*   **🔮 Grade Prediction/Outlook (Per Subject):**
    *   Displays current **Coursework Mark** and **Current Overall Mark** for the subject.
    *   If the subject has a final exam:
        *   Calculates and shows the **Final Exam Marks needed** to achieve higher letter grades (e.g., "To get A+, you need ~X% in the final.").
        *   Provides warnings if certain higher grades are mathematically unattainable based on current coursework.
        *   Highlights marks needed to achieve a passing grade if currently below the threshold.

*   **🖥️ User Interface & Experience (UI/UX):**
    *   **Professional Design:** Clean, modern layout with a consistent theme (CSS variables) and Font Awesome icons.
    *   **Interactive & Dynamic:** Subject blocks and coursework fields are added/removed smoothly with subtle animations.
    *   **Robust Input Validation:**
        *   Real-time validation for marks, credit hours, and ratios (min/max values).
        *   Clear error messages appear next to invalid fields.
        *   Inputs are highlighted (e.g., red border) upon error.
        *   Visual warning if coursework ratios don't sum to 100%.
    *   **User Feedback:**
        *   "Calculating..." loading state for the GPA button.
        *   Toast notifications for actions like "Progress auto-saved!", "Subject removed", "Reset All", and calculation errors.
        *   Informative tooltips (info icons) provide explanations for complex fields.
    *   **Empty State Handling:** A helpful message is shown when no subjects have been added.

*   **💾 Data Persistence & Management:**
    *   **Local Storage:** All subject data is securely saved in the browser's local storage.
    *   **Auto-Save:** Data is automatically saved (debounced) shortly after user input changes.
    *   **Save on Exit:** Ensures data is saved when the user is about to leave or close the page.
    *   **Load on Startup:** Previously saved data is automatically loaded when the calculator is reopened.
    *   **Reset All:** A dedicated button allows users to clear all stored data with a confirmation prompt.

## 🛠️ How It Works (Technical Highlights)

*   **Client-Side Logic:** All calculations and data management are handled entirely by JavaScript in the user's browser. No server-side processing is required.
*   **DOM Manipulation:** JavaScript dynamically creates, updates, and removes HTML elements for subjects and coursework parts, providing a responsive experience.
*   **Event Handling:** Uses event listeners for clicks on buttons and changes in input fields to trigger actions like adding subjects, calculating GPA, or saving data.
*   **Validation Functions:** A set of validation functions ensure data integrity before processing calculations.
*   **Data Structure:** Subject data, including nested coursework parts, is managed as an array of JavaScript objects, which is then serialized to JSON for storage in `localStorage`.
*   **Modern CSS Styling:** Utilizes CSS variables for easy theming, flexbox/grid for layout, and Font Awesome for iconography.

##🚀 Getting Started / How to Use

1.  **Open the `index.html` file** in your web browser.
2.  **Add Subjects:**
    *   Click the "Add Subject" button.
    *   Name your subject.
    *   Enter the Credit Hours.
3.  **Configure Grading:**
    *   Specify if the subject has a final exam and select the coursework/final ratio.
    *   Enter the number of coursework parts.
    *   For each coursework part, input the marks obtained and its ratio towards the total coursework.
    *   If there's a final exam, input the final exam marks (if known, or leave blank for prediction).
4.  **Calculate GPA:**
    *   Click the "Calculate GPA" button.
    *   View your overall GPA and detailed results for each subject, including grade predictions.
5.  **Manage Data:**
    *   Your data is auto-saved.
    *   Use the "Reset All" button if you want to clear all entries.
    *   View the "Grading Scale" if needed.

## 💻 Technologies Used

*   **HTML5:** For the structure of the web page.
*   **CSS3:** For styling, layout (Flexbox), and responsiveness.
    *   CSS Variables for theming.
    *   Font Awesome for icons.
*   **JavaScript (ES6+):** For all the application logic, DOM manipulation, calculations, and local storage interaction.
