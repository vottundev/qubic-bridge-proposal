
# Vottun Platform Qubic Bridge - Proposal

## Bridge Overview

![Bridge Overview](https://github.com/vottunio/qubic-bridge-proposal/blob/main/bridge-overview.png)

## How does it work
This bridge connects the Qubic (non-EVM) network with Ethereum / Arbitrum One, allowing users to transfer tokens between the two networks. The system operates as follows:

### 1. User Interface (Frontend):
- Users interact with the Vottun platform through an interface that allows them to connect their wallet (We assume that there is a wallet to use in front end. We are investigating what wallet extension to use by the users. Metamask Flask could be an option but it is in an experimental phase).
- Once connected, users select the type of swap they want to perform: sending tokens from Qubic to Ethereum & Arbitrum One, or vice versa.

### 2. Origin Chain Operations:
- If the user decides to swap Qubic (Qub) to Ethereum/Arbitrum One, the Back End sends an order to smart contracts on the Qubic network to execute the corresponding transfer.
- If the user decides to swap (wQub) to Qubic, the Back End sends an order to smart contracts on the Ethereum/Arbitrum One networks to execute the corresponding transfer.

### 3. Operations on Vottun (Backend):
- Vottun Back End acts as the intermediary between the two networks, managing transactions and validating that the orders on Qubic/Ethereum/Arbitrum One have been correctly executed.
- Once the operation on chain is validated, the Back End communicates with the appropriate smart contract on the other chain to execute the inverse operation and complete the swap.

### 4. Destination Chain Operations:
- If the user decides to swap wrapped Qubic (wQub) to Qubic, the Back End sends an instruction to smart contracts on Ethereum/Arbitrum One to execute the order to reflect the equivalent amount
- If the user decides to swap wrapped Qubic (wQub) to Qubic, the Back End sends an instruction to smart contracts on the Ethereum/Arbitrum One network to execute the corresponding transfer, reflecting the equivalent amount of Qubic (Qub) in the user’s wallet on the Qubic network.
- In both cases, the order is updated with the transfer transaction hash.


### Process Summary:
- **Qub to wQub**: Smart contracts on Qubic and Ethereum/Arbitrum One execute the swap orders to reflect the tokens on both networks.
- **wQub to Qub**: Smart contracts on Ethereum/Arbitrum One and Qubic execute the reverse swap orders to reflect the tokens.
- **Vottun**: manages the process between both networks, ensuring that the orders are executed correctly.


---

## Project Scope

### Objectives:
- Create a bridge for **token swaps** between Qubic and Ethereum & Arbitrum One .
- Develop a **user-friendly interface** for wallet connection and swap selection.
- Build a **backend** to handle swap orders and communicate with smart contracts on both networks.

### Scope of Work:
1. **Frontend Development** Interface for connecting wallets(pending to confirm by Qubic which wallet solution to apply).
2. **Backend Development** Manage communication between Qubic and Ethereum/Arbitrum One smart contracts. Monitor transaction status and ensure accurate execution of swaps.

3. **Smart Contract Development & Integration**.
4. **Testing and Security**: Test and audit to ensure secure and reliable swaps.

### Deliverables:
- Functional bridge between Qubic and Ethereum/Arbitrum One.
- **Frontend** for user interaction.
- **Backend** to manage swaps and smart contract execution.

### Out of Scope:
- Any Extra development not considered in the proposal.

---

## Development Proposal - Option 1 (SC by Vottun)
**Total Development**
- User Interface Development
- Ethereum, Arbitrum One & Qubic Smart Contract development
- Vottun Backend development
- Liquidity Pools creation
- Integration with Metamask Flask or other compatible Wallets
  
**Total Development Hours**: 280  

**Testing And Deployment Hours**: 40

**GO-LIVE**: 8

**Total Budget: 26,500 USD**

---

## Development Proposal - Option 2 (SC by Qubic)
**Total Development**

- User Interface Development
- Support and integration with Qubic Smart Contracts
- Vottun Backend development
- Liquidity Pools creation

**Total Development Hours**: 232  

**Testing And Deployment Hours**: 40

**GO-LIVE**: 8

**Total Budget: 22,600 USD**


## Service Bridge for both proposals

**Infrastructure (12 Months)**: 6,000 USD

**LIQUIDITY MANAGEMENT (LIQUIDITY POOL MANAGE QUBIC ALLOWANCE FUNDS)**: 2,400 USD

**TX FEE**: TBD

**Total BUDGET**: **8,400 USD + TX FEES**

**SERVICE PROVIDER OPERATIONAK¿L SUPPORT (12 MONTHS)**: **8,000 USD**


---


## Milestones
The project will be divided in 3 milestones in order to deliver the Grant: 

## Milestone 1: Definition, Design, and Set-Up
This phase focuses on planning and setting up the framework for the bridge, establishing the tools and initial environment for the project.

### Deliverables:
- **Project Definition and Requirements:**
  - Finalize the project scope and requirements.
  - Confirm the wallet solution for Qubic integration.
  - Define the architecture of the bridge (Frontend, Backend, and Smart Contract interactions).

- **Design:**
  - Create the user flow and wireframes for the user interface (wallet connection and token swap UI).
  - Design the backend structure to manage communication between Qubic and Ethereum/Arbitrum One.

- **Set-Up:**
  - Set up the development environment for smart contracts, backend, and frontend.
  - Establish communication protocols between Qubic and Ethereum/Arbitrum One networks.

**Amount Unlocked End of Milestone 1**: 20% --> Option 1: 5.300 USD / Option 2: 4.520 USD 


---


## Milestone 2: Smart Contract Development (only applies with Option 1)
This phase covers the creation of the smart contracts and interaction logic needed for token swaps between the Qubic and Ethereum/Arbitrum One networks.

### Deliverables:
- **Smart Contracts:**
  - Develop smart contracts on Qubic for token swap operations.
  - Develop smart contracts on Ethereum/Arbitrum One to handle wrapped Qubic (wQub).
  - Ensure cross-chain communication logic between Qubic and Ethereum/Arbitrum One.

- **Contract Deployment:**
  - Deploy smart contracts on test networks (Qubic, Ethereum, and Arbitrum One).
  - Set up liquidity pools for the swap functionality.

- **Initial Testing:**
  - Test the smart contract functions in isolation, ensuring correct swaps between Qubic and Ethereum/Arbitrum One.

**Amount Unlocked End of Milestone 2**: 40% --> Option 1: 10.600 USD


---


## Milestone 3: Frontend, Backend, SC Integration & Testing
This phase covers the development of the user interface, backend logic, integration of the system, and full-scale testing of the entire bridge.

### Deliverables:
- **Frontend Development:**
  - Build the interface for wallet connection (based on the wallet solution defined in Milestone 1).
  - Develop UI for token swap selection and transaction tracking.

- **Backend Development:**
  - Implement backend logic to handle swap requests.
  - Integrate the backend with the smart contracts on Qubic and Ethereum/Arbitrum One.
  - Ensure that the backend manages order validation and updates users' wallets accurately.

- **Integration & Testing:**
  - Integrate the frontend, backend, and smart contracts for seamless user interaction.
  - Conduct extensive testing to ensure secure and accurate token swaps.
  - Perform a security audit to validate the system's reliability.

**Amount Unlocked End of Milestone 3**: 40% --> Option 1: 10.600 USD / 80% --> Option 2: 18.080 USD

## Considerations:
- The infrastructure is shared; to have a dedicated infrastructure, a separate quotation will be required.
- The proposal does not cover other developments outside those established; any additional development must be evaluated and treated as an other open project.
- The blockchain must commit to releasing funds at least 30% the beginning and the rest based on the milestones achieved for the project.
- The blockchain must commit to signing the collaboration contract within a maximum of 14 days from the agreement on the project and its terms.
- Understanding that timing is important, the blockchain must commit to responding to any Vottun technical question within a maximum of 2 business days.
- As part of this project, Vottun has the right to publish the project on its platform and request collaboration from its developer community 
- If the project is published in its platform, Vottun has the right to establish bounties or rewards for its developer community according to the work required and its platform rules.
- If the project is published in its platform, Vottun is responsible of all the potential payments of bounties and rewards to its community. This bounties and rewards are included in the current budget and payments are normally based on milestones achieved and verified by Vottun's & Blockchain curators.
- For project implementation, the blockchain will be required to provide all necessary materials; Vottun will not be responsible for delays caused by late deliveries from the blockchain. 
- Vottun is not responsible for verifying the content and materials provided by the blockchain.
- It is strongly recommended that all smart contracts are audited by a third party. Vottun works with Certik. 

