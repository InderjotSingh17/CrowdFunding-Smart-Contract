# CrowdFunding Smart Contract 💰

A secure and transparent crowdfunding smart contract written in Solidity for Ethereum-based blockchain networks. This contract allows contributors to fund a campaign, vote on spending requests, and ensures only majority-approved requests are paid out.

## 📜 Contract Overview

This smart contract implements a decentralized crowdfunding mechanism with the following features:

- Only contributors can vote on spending requests.
- Refunds are allowed if the target is not met before the deadline.
- Funds are only released if more than 50% of contributors approve a request.
- Manager (creator) can create spending requests but **cannot misuse funds** without community approval.

## 🛠️ Technologies Used

- Solidity ^0.8.x
- Remix IDE / Hardhat / Truffle (for deployment & testing)
- Ethereum blockchain (compatible with testnets like Goerli, Sepolia)

---

## 🚀 Features

- ✅ Minimum contribution enforcement (`1 ETH`)
- ✅ Contributor tracking and vote locking (one vote per request)
- ✅ Refund mechanism if the campaign fails
- ✅ Payment allowed **only after majority approval**
- ✅ Secure use of `require` and `modifiers` to restrict access

---

## 🔧 Functions

### ✅ Public Functions
| Function | Description |
|---------|-------------|
| `sendEth()` | Contribute ETH to the campaign |
| `getContractBalance()` | Returns the current ETH balance of the contract |
| `refund()` | Allows contributors to claim a refund if the target isn't met before the deadline |
| `voteRequest(uint _requestNo)` | Contributors vote to approve a spending request |

### ✅ Manager-Only Functions
| Function | Description |
|----------|-------------|
| `createRequests(string, address, uint)` | Create a new spending request |
| `makePayment(uint)` | Transfer funds to the recipient if majority approves |

🔐 Security Notes
Prevents double voting using voters mapping

Contributions and refunds are accurately tracked

onlyManager modifier restricts sensitive functions

Uses require to ensure logic correctness

🧑‍💻 Author
Inderjot Singh
👨‍💻 GitHub: @InderjotSingh17
📧 Email: singhinderjot816@gmail.com
📱 Phone: +91 8373920505

📄 License
This project is licensed under the MIT License.
