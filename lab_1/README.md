# Transaction Analyzer Project

## Project Setup Instructions

**Prerequisites:**
>Ensure that Node.js is installed on your computer.

## Description of the Individual Work

This project represents a program for analyzing transaction data. The project includes a TransactionAnalyzer class that provides various methods for filtering and analyzing transactions based on different criteria. Key features include:

+ Adding new transactions.
+ Filtering transactions by date, type, and other parameters.
+ Calculating totals and averages.
+ Outputting transaction data in different formats.

The project uses JSON data containing transaction details such as type, amount, date, and other attributes.


## Project Documentation
**TransactionAnalyzer Class Constructor**

```JavaScript
constructor(transactions: Array<Object>)
```

>Accepts an array of objects representing transactions.

**Methods**
```JavaScript
addTransaction(transaction) // Adds a new transaction to the list.

getAllTransactions() // Returns all transactions.

getUniqueTransactionTypes() // Returns unique transaction types.

calculateTotalAmount() // Returns the total amount of all transactions.

calculateTotalAmountByDate(year, month, day) // Returns the total amount of transactions for the specified year, month, and day (year, month, and day are optional).

getTransactionByType(type) // Returns transactions of the specified type (e.g., 'debit' or 'credit').

getTransactionsInDateRange(startDate, endDate) // Returns transactions within the specified date range.

getTransactionsByMerchant(merchantName) // Returns transactions made with the specified merchant.

calculateAverageTransactionAmount() // Returns the average transaction amount.

getTransactionsByAmountRange(minAmount, maxAmount) // Returns transactions with amounts within the specified range.

calculateTotalDebitAmount() // Returns the total amount of debit transactions.

findMostTransactionsMonth() // Returns the month with the highest number of transactions.

findMostDebitTransactionMonth() // Returns the month with the highest number of debit transactions.

mostTransactionTypes() // Determines which transaction type occurs more frequently (either debit or credit).

getTransactionsBeforeDate(date) // Returns transactions before the specified date.

findTransactionById(id) // Finds a transaction by its unique ID.

mapTransactionDescriptions() // Returns an array of all transaction descriptions.

string() // Returns a string representation of all transactions in JSON format.
```

## Examples of Using the Project
```JavaScript
const analyzer = new TransactionAnalyzer(transactionsData);

// Get unique transaction types
console.log('Unique transaction types:', analyzer.getUniqueTransactionTypes());

// Calculate the total amount of all transactions
console.log('Total amount of transactions:', analyzer.calculateTotalAmount());

// Get the average transaction amount
console.log('Average transaction amount:', analyzer.calculateAverageTransactionAmount());

// Get all debit transactions
console.log('Debit transactions:', analyzer.getTransactionByType('debit'));

// Get transactions in January 2019
console.log('Transactions in January 2019:', analyzer.calculateTotalAmountByDate(2019, 1));
```

Sample data format:
```JSON
[
  {
    "transaction_id": "1",
    "transaction_type": "debit",
    "transaction_amount": 100.5,
    "transaction_date": "2019-01-01T12:00:00Z",
    "merchant_name": "Merchant A",
    "transaction_description": "Purchase at Merchant A"
  },
  {
    "transaction_id": "2",
    "transaction_type": "credit",
    "transaction_amount": 200.0,
    "transaction_date": "2019-02-01T12:00:00Z",
    "merchant_name": "Merchant B",
    "transaction_description": "Refund from Merchant B"
  }
]
```

## List of Sources Used

+ [Node.js](https://nodejs.org/en)
+ [JavaScript MDN Documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript)