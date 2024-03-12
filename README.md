# Monthly Dues Calculator

This script calculates the monthly dues for a set of users. It fetches the latest bills from specific email threads, updates a Google Sheet with the bill amounts, and sends out emails to the users with their respective dues.

## Functions

- `getMonthlyDues()`: This is the main function that orchestrates the entire process. It fetches the latest electric and water bills from specific email threads and updates the Google Sheet with these values.

- `findBillAmount(threads, regex)`: This function takes in email threads and a regular expression to match the bill amount in the email body. It returns the bill amount if found, else returns 0.

- `updateGoogleSheet(waterBill, electricBill)`: This function updates the Google Sheet with the fetched water and electric bill amounts. It also creates a copy of the updated sheet with a new name and saves it in a specific folder.

- `sendEmails(sheetUrl, spreadsheet, month)`: This function sends out emails to the users with their respective dues. The email body contains the total amount due and a link to the Google Sheet for more information.

- `validateEmail(email)`: This function validates an email address using a regular expression and returns true if the email is valid, else returns false.

- `clearSheetForNextMonth(sheet)`: This function clears specific ranges in the sheet to prepare it for the next month's calculations.

## Usage

To use this script, simply call the `main()` function which in turn calls `getMonthlyDues()`.

```javascript
function main() {
  getMonthlyDues();
}
