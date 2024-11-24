describe('NGX Admin Modals and Overlays Tests', () => {
  it('Should open the website and interact with modals and checkboxes', () => {
    // Step 1: Visit the application on localhost
    cy.visit('http://localhost:4200');

    // Step 2: Navigate to Modals and Overlays
    cy.contains('Modals & Overlays').click();

    // Step 3: Click on the Toaster
    cy.contains('Toaster').click();

    // Step 4: Inspect and click on the Toaster in the application
    cy.get('.toaster') // Adjust selector based on the actual class or identifier
      .should('be.visible')
      .click();

    // Step 5: Select all three checkboxes
    const checkboxes = [
      'input[type="checkbox"][value="checkbox1"]', // Adjust based on your actual values
      'input[type="checkbox"][value="checkbox2"]',
      'input[type="checkbox"][value="checkbox3"]',
    ];

    checkboxes.forEach(checkbox => {
      cy.get(checkbox).check(); // Check all checkboxes
    });

    // Step 6: Click on only the second checkbox
    cy.get(checkboxes[1]).click(); // Click on the second checkbox
  });
});
- 👋 Hi, I’m @Rachitha-prog
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...
- 😄 Pronouns: ...
- ⚡ Fun fact: ...

<!---
Rachitha-prog/Rachitha-prog is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
