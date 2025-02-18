# 💰 CrowdFunding Smart Contract

This is a **decentralized crowdfunding smart contract** written in **Solidity**, allowing users to contribute ETH to a funding campaign. The funds can be utilized only if the majority of contributors approve the spending request.

---

## 📜 Smart Contract Overview

| **Variable**       | **Description** |
|--------------------|----------------|
| `manager`         | Address of the campaign manager |
| `minContribution` | Minimum ETH required to contribute |
| `deadline`        | Timestamp indicating the deadline for contributions |
| `target`          | Fundraising target in wei |
| `raisedAmount`    | Total ETH raised |
| `noOfContributors` | Number of unique contributors |
| `contributors`    | Mapping of contributor addresses to their respective contributions |
| `requests`        | Mapping of spending requests |
| `numRequests`     | Total number of spending requests |

### 🎯 Key Features

- **Fundraising Campaign**: Users contribute ETH, and funds are locked until the goal is met.
- **Refund System**: If the target is not reached before the deadline, contributors can claim refunds.
- **Request & Voting Mechanism**: The manager creates spending requests, and contributors vote on them.
- **Secure Payment Release**: Only if the majority approves, payments are made to the recipient.

---

## 🔧 Functions & Usage

| **Function** | **Description** |
|-------------|----------------|
| `sendEth()` | Allows users to contribute ETH to the campaign |
| `getContractBalance()` | Returns the total balance in the contract |
| `refund()` | Refunds contributors if the target is not reached before the deadline |
| `createRequests(_description, _recipient, _value)` | Manager creates a fund withdrawal request |
| `voteRequest(_requestNo)` | Contributors vote on a specific spending request |
| `makePayment(_requestNo)` | Manager releases funds if a request gets majority approval |

---

## 🚀 Deployment Instructions

1. **Open Remix IDE** and create a new file named **`CrowdFunding.sol`**.
2. **Copy & paste** the contract code.
3. **Compile** using Solidity version **0.5.x**.
4. **Deploy** on any of the following:
   - Remix VM (Local)
   - Goerli Testnet
   - Sepolia Testnet
   - Ethereum Mainnet (after extensive testing).

---

## ⚠️ Security Considerations

✅ **Test before deploying** on the Ethereum Mainnet.  
✅ **Double-check recipient addresses** before transferring funds.  
✅ **Ensure the deadline and target values are correctly set** to avoid contract misbehavior.  
✅ **Keep the manager address secure**, as it has control over fund requests.  

---

## 📝 License

This project is licensed under the **GPL-3.0 License**.

---

**💡 Happy Building! 🚀**
