# Tax-Calculator  
https://anshuldtu.github.io/Tax-Calculator/
## Challenge outline: Tax Calculator

Design a website that allows for tax calculation based on a users input.
This is a simple tax calculator implemented in JavaScript. It calculates the overall income after considering gross income, extra income, age group and deductions. Additionally, it provides validation for input fields.
References & Requirements

    The tax calculation works based on this formula -
        Overall income (after deductions) under 8 (≤) Lakhs is not taxed.
            Ex - if Gross Annual Income + Extra Income - Deductions = 6 Lakhs, no tax
            if Gross Annual Income + Extra Income - Deductions = 9 Lakhs, tax
        Income over 8 (>) Lakhs, the amount over 8 Lakhs is taxed at
            30% for people with age < 40
            40% for people with age ≥ 40 but < 60
            10% for people with age ≥ 60
            Example
                Age = 34, Income = 40 Lakhs, no deductions, tax = .3 * (40 - 8) = .3 * 32 = 9.6 Lakhs
    Do not restrict the user from entering incorrect values like characters in the number fields
        Highlight an error icon to the right of the input field (shown as an example in the above image as a circle with !). Hovering over it should show the error in a tooltip
        If no errors are present, don't show the error icon
        This should be present in all the number fields
    The age dropdown field should have 3 values -
        <40
        ≥ 40 & < 60
        ≥ 60
        If the user has not entered this value and clicks on submit, show an error icon hovering over which should show that the input field is mandatory
    Error icons should not be visible in the form by default.
    Clicking on submit should show a modal which would show the final values based on the above calculations.

Assumptions

    Input Validation:
        Input values are validated on focus, change, and when the submit button is clicked.
        Errors are displayed to the user under the following conditions:
            Typing a number less than zero results in an error message "Please type non-negative numbers".
            Clicking on an input field and not typing anything or leaving any field empty and clicking the submit button results in an error message "This input field is mandatory".
            Typing anything other than a number results in an error message "Please type numbers only".
    Overall Income Calculation:
        If the sum of gross income, extra income, and deductions is less than or equal to 8 lakhs, the overall income is displayed as the sum of gross income and extra income.
Test Cases

Case 1: A tooltip appears when the question mark icons are hovered over.
<br><img width="581" alt="Screenshot 2024-04-14 at 10 13 58 PM" src="https://github.com/anshulDTU/Tax-Calculator/assets/101987357/f1282f27-8693-463e-b5ff-b2d034da48f6"><br>
Case 2: Error icons should be displayed when the submit button is clicked without any input provided, accompanied by an error message.
"This input field is mandatory"
Screenshot 1: Default State
<br><img width="544" alt="Screenshot 2024-04-14 at 10 16 08 PM" src="https://github.com/anshulDTU/Tax-Calculator/assets/101987357/ccecb857-70cd-406d-be0f-578afd9c2e1d"><br>
Screenshot 2: After clicking the submit button for empty fields
<br><img width="619" alt="Screenshot 2024-04-14 at 10 17 30 PM" src="https://github.com/anshulDTU/Tax-Calculator/assets/101987357/1e66746e-a1cc-4fe1-9e88-21d3fabe60ff"><br>
Case 3: If a negative value is entered into the Number fields, error icons will be shown. These fields exclusively accept 0 or positive numbers. The error message will indicate: "Please input non-negative numbers only."
<br><img width="498" alt="Screenshot 2024-04-14 at 10 18 35 PM" src="https://github.com/anshulDTU/Tax-Calculator/assets/101987357/127703e1-597e-4720-bf50-4130648f791a"><br>
Case 4: If characters are entered into the Number fields instead of a numerical value, error icons will be displayed. The error message will state: "Please input numbers only."
<br><img width="518" alt="Screenshot 2024-04-14 at 10 19 35 PM" src="https://github.com/anshulDTU/Tax-Calculator/assets/101987357/b5165454-c044-4143-a098-15136c7e2a9f"><br>
Case 5: Error icons will be displayed if all number fields are filled, buthe age group is not selected
<br><img width="546" alt="Screenshot 2024-04-14 at 10 22 27 PM" src="https://github.com/anshulDTU/Tax-Calculator/assets/101987357/3718fe65-7355-46b5-95b3-c00c530c119a"><br>
Case 6: If the sum of Gross Income and Extra Income minus Total Deductions is less than or equal to 8 lakhs, no income tax will apply. Therefore, the overall income will be Gross Income plus Extra Income.
<br><img width="522" alt="Screenshot 2024-04-14 at 10 33 50 PM" src="https://github.com/anshulDTU/Tax-Calculator/assets/101987357/cc5c93d1-d1c0-4b12-9ed2-1e2a1c5037ce"><br>
<br><img width="611" alt="Screenshot 2024-04-14 at 10 33 53 PM" src="https://github.com/anshulDTU/Tax-Calculator/assets/101987357/1ad9c257-0b07-4adc-9be5-130e6a3edeab"><br>
Case 7: If the sum of Gross Income and Extra Income minus Total Deductions exceeds 8 lakhs, income tax will be applicable based on the age group. Therefore, the overall income will be calculated accordingly.
1. Age < 40
<br><img width="533" alt="Screenshot 2024-04-14 at 10 35 56 PM" src="https://github.com/anshulDTU/Tax-Calculator/assets/101987357/b9f39790-fb06-41cc-bb00-3158b850c9f4"><br>
<br><img width="585" alt="Screenshot 2024-04-14 at 10 36 00 PM" src="https://github.com/anshulDTU/Tax-Calculator/assets/101987357/e31f75a3-ab4c-43dd-a3c6-d3e561b21d6c"><br>
2. Age ≥ 40 & < 60
<br><img width="561" alt="Screenshot 2024-04-14 at 10 44 00 PM" src="https://github.com/anshulDTU/Tax-Calculator/assets/101987357/aa11d848-3bbe-45d4-8eb3-6d6b758d312e"><br>
<br><img width="601" alt="Screenshot 2024-04-14 at 10 44 06 PM" src="https://github.com/anshulDTU/Tax-Calculator/assets/101987357/c15c557f-47eb-48f0-b16b-6ea25cc66e1f"><br>
3. Age ≥ 60
<br><img width="567" alt="Screenshot 2024-04-14 at 10 45 23 PM" src="https://github.com/anshulDTU/Tax-Calculator/assets/101987357/343635f1-284f-4884-8dff-00db8990fe95"><br>
<br><img width="618" alt="Screenshot 2024-04-14 at 10 45 27 PM" src="https://github.com/anshulDTU/Tax-Calculator/assets/101987357/d14aa8ef-b867-45f8-8d64-7b2086f3ea89"><br>

