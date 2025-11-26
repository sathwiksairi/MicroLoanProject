
# Micro-Loan DeFi Protocol

A decentralized micro-loan system built using **React.js, Node.js, Express.js, MongoDB, LocalStorage, and Truffle.**
The platform enables borrowers to request and repay crypto-based micro-loans using automated smart contracts deployed on a local blockchain environment.

## 📌 Overview
The **Micro-Loan DeFi Protocol** provides a simple and transparent way for borrowers to access small crypto loans without relying on traditional lenders. The system uses a treasury-backed lending model, where a smart contract manages loan approvals, repayments, due dates, and the treasury balance.

Borrowers interact with the application through a modern web interface built in React, while all financial logic is executed inside Solidity smart contracts deployed via Truffle. A Node.js–Express backend handles user metadata, and LocalStorage supports persistent client-side UI state. MongoDB is used for storing non-financial user data.

Since no real blockchain funds were available, the project operates entirely on a local blockchain environment using Truffle Develop, allowing complete testing of the loan process.
## ✨ Key Features
* Automated smart contract–based micro-loans

* Simple borrower-only system (no lenders required)

* Loan request, approval, issuance, and repayment

* Local blockchain deployment using Truffle

* Full-stack UI with real-time loan status updates

* User metadata storage with MongoDB

* Persistent UI session using LocalStorage

* No intermediaries or manual verification needed
## 🛠️ Tech Stack
**Frontend:**

* React.js

* LocalStorage

**Backend:**

* Node.js

* Express.js

* MongoDB

**Blockchain:**

* Solidity

* Truffle Framework (Compilation, Deployment & Testing)

* Truffle Develop (Local Blockchain Network)
## 🏗️ Architecture
```
User (Borrower)
      ↓
React.js Frontend (Loan Interface)
      ↓
Node.js + Express Backend (User Metadata)
      ↓
MongoDB (Database for Non-Financial Data)
      ↓
Truffle Develop (Local Blockchain Network)
      ↓
Solidity Smart Contract (Treasury + Loan Logic)
```

## 🚀 How It Works
1. Borrower opens the React.js loan interface.

2. Application loads borrower session data from LocalStorage.

3. When a loan is requested, the frontend triggers a blockchain transaction via Truffle’s local RPC.

4. The smart contract checks treasury balance and approves or rejects the request.

5. Loan details are stored on-chain; borrower info is stored in MongoDB.

6. Borrower repays the loan through the same UI.

7. Smart contract updates the treasury and marks the loan as completed.

## 📁 Project Structure
```
/client                   → React.js frontend
/server                   → Node.js + Express backend
/contracts                → Solidity smart contracts
/migrations               → Contract deployment scripts (Truffle)
/build                    → Compiled contract artifacts

```

## 📜 Smart Contracts
* **LoanContract.sol**
Handles loan creation, repayment, interest, and loan restrictions.

* **Treasury.sol**
Maintains on-chain loanable balance used for issuing loans.

## 🧪 Testing
All features were tested using:

+ Truffle Develop local blockchain

+ React-Express integrated environment

+ Loan lifecycle tests

+ Treasury balance updates

+ MongoDB metadata validation

+ UI session persistence with LocalStorage

Because no external funds were available, testnet or mainnet deployment was not performed.

## ⚠️ Limitations
* Works only on local blockchain (no testnet deployment)

* Borrower-only model (no lenders/staking)

* Limited treasury size

* No MetaMask or external wallets

## 🚧 Future Enhancements

* Add lender pools or staking

* Deploy to public blockchain networks

* Build a loan history dashboard

* Add role-based admin controls

* Improve interest + repayment models
