# Task 3 - Codebase 1
# Prompt 1
You are an expert software security researcher and blockchain architect conducting an exhaustive, read-only analysis of the Bitcoin Core C++ codebase for an academic Master's thesis. Your objective is to thoroughly explore the source code provided in this workspace, utilizing your maximum analytical capacity to trace the complete transaction lifecycle. 

Execute a deep structural analysis focusing specifically on the script execution engine and the consensus-critical transaction validation logic. You are expected to autonomously navigate and inspect the core implementation files (including, but not limited to, `src/script/interpreter.cpp`, `src/consensus/tx_verify.cpp`, and `src/validation.cpp`). 

Based on your comprehensive code exploration, generate a rigorously structured markdown file named `thesis_bitcoin_phase1.md` containing exactly these two sections:

1. "Module and Architecture Map": Detail the hierarchical structure and interaction flow of the primary components responsible for transaction validation, the UTXO set management, and script evaluation. Describe the exact C++ interfaces, data structures, and state management mechanisms that connect these modules.
2. "Core Consensus and Execution Mechanism": Provide an in-depth, highly technical, yet formally written explanation of the end-to-end transaction validation process within this specific codebase. You must explicitly break down the execution loop of the script interpreter, explaining how stack operations are evaluated. Crucially, you must detail the integration and execution mechanics of Taproot-related opcodes (BIP 341/342), including Schnorr signature validation and Merkelized Alternative Script Trees (MAST) path execution.

Maintain a strictly formal, academic tone. Ground every architectural claim in the actual source code structure you observe. Do not include any other sections. Once the file is written and saved to the root directory, stop execution.





# Prompt 2
Continue your rigorous academic security analysis of the Bitcoin Core codebase. First, load and read the file `thesis_bitcoin_phase1.md` that you generated previously to establish the complete architectural context and consensus baseline.

Now, deploy your maximum analytical capabilities to perform a granular, function-by-function inspection of the security-critical execution paths you identified. Trace the exact flow of data through the script interpreter and the signature verification logic.

Generate a new markdown file named `thesis_bitcoin_phase2.md` containing exactly these two sections:

1. "Security-Critical Code Paths Summary": Document the critical code paths responsible for state transition logic, bytecode execution, and cryptographic verification. You MUST explicitly cite the exact C++ file names, class names, and function signatures you analyzed. Describe how these specific paths handle edge cases, memory allocation, and execution boundaries.
2. "Potential Vulnerabilities and Weak Patterns": Formulate an analytical breakdown of potential vulnerabilities, architectural weak points, or dangerous coding patterns within the inspected C++ logic. You MUST perform a historical cross-reference: match your identified weak patterns against known Common Vulnerabilities and Exposures (CVEs) or historically documented bugs specifically associated with Bitcoin's script and consensus layers (e.g., signature malleability vectors, integer overflow handling in script arithmetic, resource exhaustion, or specific edge cases in OP_CODES execution). 

Your analysis must bridge the gap between theoretical vulnerability classes and the concrete C++ implementation in the workspace. Maintain a formal academic tone. Save the file and stop execution.





# Prompt 3
You are an expert blockchain security researcher finalizing a crucial chapter for an academic Master's thesis in Computer Science. Your task is to compile the final report by strictly preserving previous work and generating ONLY the final missing section.

Follow these exact execution steps in Build mode:
1. Read the complete content of `thesis_bitcoin_phase1.md`.
2. Read the complete content of `thesis_bitcoin_phase2.md`.
3. Create a new file named `thesis_bitcoin_FINAL_REPORT.md`.
4. Write the main title at the top: `# Codebase 1 Analysis: Bitcoin Source Code`
5. COPY the entire, exact text from `thesis_bitcoin_phase1.md` into the new file. DO NOT summarize, paraphrase, or omit a single character. Preserve it exactly as it was originally written.
6. COPY the entire, exact text from `thesis_bitcoin_phase2.md` into the new file, directly below the Phase 1 content. DO NOT summarize, paraphrase, or omit a single character. Preserve it exactly as it was originally written.
7. Generate and append a completely new, exhaustive section at the bottom titled: `## 5. Complexity and Readability Estimate`.

For Section 5, use your maximum analytical capabilities to generate a profoundly detailed, highly technical evaluation of the codebase's complexity and readability. Analyze the software engineering maintainability of the consensus and script modules you explored. Discuss the cyclomatic complexity of the execution paths, the architectural coupling between validation layers, and the cognitive load required for a developer to safely maintain the Taproot and MAST implementations. Provide a definitive, mathematically and architecturally substantiated academic conclusion on the overall security posture.

CRITICAL DIRECTIVE: Do not waste output tokens rewriting, condensing, or refining sections 1 to 4. Preserve their original depth completely, and focus 100% of your generative capacity on making Section 5 massive, highly analytical, and academically rigorous. Once saved, stop execution.



# Task 3 - Codebase 2
# Prompt 1
You are an expert software security researcher and blockchain architect conducting an exhaustive, read-only analysis of the go-ethereum (Geth) Go codebase for an academic Master's thesis. Your objective is to thoroughly explore the source code provided in this workspace, utilizing your maximum analytical capacity to trace the complete EVM transaction lifecycle.

Execute a deep structural analysis focusing specifically on the EVM execution loop, gas accounting mechanisms, and the state transition function. You are expected to autonomously navigate and inspect the core implementation files (including, but not limited to, `core/state_transition.go`, `core/vm/evm.go`, `core/vm/interpreter.go`, and `core/state/statedb.go`).

Based on your comprehensive code exploration, generate a rigorously structured markdown file named `thesis_geth_phase1.md` containing exactly these two sections:

1. "Module and Architecture Map": Detail the hierarchical structure and interaction flow of the primary components responsible for Ethereum state transitions, the EVM execution environment, and gas metering. Describe the exact Go interfaces, structs (e.g., `StateDB`, `EVM`, `EVMInterpreter`), and state management mechanisms that connect these modules.
2. "Core Consensus and Execution Mechanism": Provide an in-depth, highly technical, yet formally written explanation of how a transaction changes state end-to-end within this specific codebase. You must explicitly break down the EVM execution loop, detailing how opcodes are fetched and dispatched, how the call stack is managed, and how gas is consumed dynamically during the state transition function before a state is finally committed or reverted.

Maintain a strictly formal, academic tone. Ground every architectural claim in the actual Go source code structure you observe. Do not include any other sections. Once the file is written and saved to the root directory, stop execution.

# Prompt 2
Continue your rigorous academic security analysis of the go-ethereum (Geth) codebase. First, load and read the file `thesis_geth_phase1.md` that you generated previously to establish the complete architectural context of the EVM and state transition layer.

Now, deploy your maximum analytical capabilities to perform a granular, function-by-function inspection of the security-critical execution paths you identified. Trace the exact flow of data through the EVM call stack, memory expansion routines, and gas accounting functions.

Generate a new markdown file named `thesis_geth_phase2.md` containing exactly these two sections:

1. "Security-Critical Code Paths Summary": Document the critical code paths responsible for executing smart contracts, managing call depths, and tracking state changes. You MUST explicitly cite the exact Go file names, struct methods, and function signatures you analyzed (e.g., `ApplyMessage`, `Run`, `Call`, and gas calculation functions like `gasCall`). Describe how these specific paths handle edge cases, memory bounds, Out-Of-Gas (OOG) errors, and state reverts via snapshots.
2. "Potential Vulnerabilities and Weak Patterns": Formulate an analytical breakdown of potential vulnerabilities, architectural weak points, or dangerous coding patterns within the inspected Go logic. You MUST perform a historical cross-reference: match your identified weak patterns against known vulnerability classes and historically documented bugs specific to EVM node implementations (e.g., reentrancy-adjacent execution paths within the node's state handling, integer overflow handling in gas or memory calculations, and gas-related Denial of Service patterns). 

Your analysis must bridge the gap between theoretical EVM vulnerability classes and the concrete Go implementation in the workspace. Maintain a formal academic tone. Save the file and stop execution.

# Prompt 3
You are an expert blockchain security researcher finalizing a crucial chapter for an academic Master's thesis in Computer Science. Your task is to compile the final report for Codebase 2 by strictly preserving previous work and generating ONLY the final missing section.

Follow these exact execution steps in Build mode:
1. Read the complete content of `thesis_geth_phase1.md`.
2. Read the complete content of `thesis_geth_phase2.md`.
3. Create a new file named `thesis_geth_FINAL_REPORT.md`.
4. Write the main title at the top: `# Codebase 2 Analysis: go-ethereum Source Code`
5. COPY the entire, exact text from `thesis_geth_phase1.md` into the new file. DO NOT summarize, paraphrase, or omit a single character. Preserve it exactly as it was originally written.
6. COPY the entire, exact text from `thesis_geth_phase2.md` into the new file, directly below the Phase 1 content. DO NOT summarize, paraphrase, or omit a single character. Preserve it exactly as it was originally written.
7. Generate and append a completely new, exhaustive section at the bottom titled: `## 5. Complexity and Readability Estimate`.

For Section 5, use your maximum analytical capabilities to generate a profoundly detailed, highly technical evaluation of the codebase's complexity and readability. Analyze the software engineering maintainability of the EVM loop and state management modules you explored. Discuss the cyclomatic complexity of the opcode dispatcher (e.g., inside `Run`), the architectural coupling between the gas accounting logic and the state database (`StateDB`), and the cognitive load required for a developer to safely manage Go's concurrency, pointer semantics, and interface abstractions within the EVM. Provide a definitive, architecturally substantiated academic conclusion on the overall security posture of this node implementation.

CRITICAL DIRECTIVE: Do not waste output tokens rewriting, condensing, or refining sections 1 to 4. Preserve their original depth completely, and focus 100% of your generative capacity on making Section 5 massive, highly analytical, and academically rigorous. Once saved, stop execution.





# Task 3 - Codebase 3
# Prompt 1 
You are an expert software security researcher and blockchain architect conducting an exhaustive, read-only analysis of the Qubic smart contract execution environment for an academic Master's thesis. Your objective is to thoroughly explore the source code provided in this workspace.

CRITICAL DIRECTIVE: Qubic is highly esoteric and lacks extensive public documentation or historical training data. Do not rely on pre-trained knowledge of Ethereum or Bitcoin. You must deduce the system's logic purely from reading the actual C++ source files in this workspace.

Execute a deep structural analysis focusing specifically on how smart contracts are executed and how they integrate with Qubic's unique consensus mechanism. 

Based on your comprehensive code exploration, generate a rigorously structured markdown file named `thesis_qubic_phase1.md` containing exactly these two sections:

1. "Module and Architecture Map": Detail the hierarchical structure and interaction flow of the primary components responsible for smart contract execution. Describe the exact interfaces, core data structures, and state management mechanisms you found in the code.
2. "Core Consensus and Execution Mechanism": Provide an in-depth, highly technical explanation of the execution environment. Explicitly break down how a contract is invoked, how its execution is validated, and how state changes are finalized. Ground every explanation strictly in the code you observed.

Maintain a strictly formal, academic tone. Do not include any other sections. Once the file is written and saved to the root directory, stop execution.

# Prompt 2
Continue your rigorous academic security analysis of the Qubic codebase. First, load and read the file `thesis_qubic_phase1.md` that you generated previously to establish the complete architectural context.

Now, perform a granular, function-by-function inspection of the security-critical execution paths you identified. Because there is no historical CVE database for Qubic, you must act as a zero-day vulnerability researcher, deducing flaws purely from code semantics.

Generate a new markdown file named `thesis_qubic_phase2.md` containing exactly these two sections:

1. "Security-Critical Code Paths Summary": Document the critical code paths responsible for executing smart contracts and state transitions. You MUST explicitly cite the exact file names, classes, and function signatures you analyzed. Describe how these specific paths handle edge cases, memory bounds, execution halting, and malicious input.
2. "Potential Vulnerabilities and Weak Patterns": Formulate an analytical breakdown of potential vulnerabilities or architectural weak points. Since you cannot cross-reference historical CVEs, you MUST deduce these patterns theoretically from the source code (e.g., lack of bounds checking, unhandled exception paths, race conditions in consensus synchronization, or memory leaks in the contract execution loop). Explain mathematically or logically how an attacker might exploit the observed code structures.

Your analysis must be empirically grounded in the raw code. Maintain a formal academic tone. Save the file and stop execution.

# Prompt 3
You are an expert blockchain security researcher finalizing the final and most difficult chapter for an academic Master's thesis in Computer Science. Your task is to compile the final report for Codebase 3 by strictly preserving previous work and generating ONLY the final missing section.

Follow these exact execution steps in Build mode:
1. Read the complete content of `thesis_qubic_phase1.md`.
2. Read the complete content of `thesis_qubic_phase2.md`.
3. Create a new file named `thesis_qubic_FINAL_REPORT.md`.
4. Write the main title at the top: `# Codebase 3 Analysis: Qubic Source Code`
5. COPY the entire, exact text from `thesis_qubic_phase1.md` into the new file. DO NOT summarize, paraphrase, or omit a single character. Preserve it exactly as it was originally written.
6. COPY the entire, exact text from `thesis_qubic_phase2.md` into the new file, directly below the Phase 1 content. DO NOT summarize, paraphrase, or omit a single character. Preserve it exactly as it was originally written.
7. Generate and append a completely new, exhaustive section at the bottom titled: `## 5. Complexity and Readability Estimate`.

For Section 5, use your maximum analytical capabilities to generate a profoundly detailed, highly technical evaluation of the codebase's complexity and readability based purely on your direct code inspection. Analyze the software engineering maintainability of the contract execution loop and consensus integration modules. Discuss the cyclomatic complexity of the execution pathways, the architectural coupling between the network consensus and local state, and the cognitive load required for a developer to safely write and audit smart contracts within this specific ecosystem. Provide a definitive, architecturally substantiated academic conclusion on the overall security posture.

CRITICAL DIRECTIVE: Do not waste output tokens rewriting, condensing, or refining sections 1 to 4. Preserve their original depth completely, and focus 100% of your generative capacity on making Section 5 massive, highly analytical, and academically rigorous. Once saved, stop execution.



# Bitcoin Taproot dApp – Proposal Generation

## 1. Role and Objective

Act as a senior Bitcoin developer, blockchain architect and decentralized application designer.

Your task is to design the strongest possible decentralized application (dApp) based on Bitcoin Taproot, specifically exploiting its Script Path spending mechanism.

The objective is to propose an original, useful and technically sound application that can be fully implemented, deployed and tested as part of an undergraduate computer science thesis.

You have complete freedom to choose the application concept. Do not assume a predefined use case or simply reproduce a conventional blockchain application.

The proposal should demonstrate the practical value of Bitcoin Taproot Script Path rather than using it as a superficial or unnecessary feature.

## 2. Proposal Selection and Optimization

Before producing your final proposal, consider different possible application concepts and select the one that offers the strongest overall balance across the following criteria:

1. **Protocol integration:** Taproot Script Path must be essential to the application's main functionality.
2. **Technical correctness:** The proposed design must respect Bitcoin's actual protocol rules and limitations.
3. **Practical usefulness:** The application should solve a meaningful problem or provide a useful service.
4. **Originality:** Prefer an interesting application concept over a basic demonstration of Bitcoin transactions.
5. **Implementation feasibility:** The application must be realistically implementable with available technologies.
6. **Security:** The design must account for transaction validation, spending conditions and potential security risks.
7. **Testability:** Its essential functionality must be objectively verifiable on a Bitcoin Regtest network.
8. **Manageable complexity:** The project should be sufficiently substantial for a thesis without requiring an unnecessarily complex infrastructure.

Select ONE proposal that best satisfies these criteria.

Do not present alternative proposals. Provide only the selected application and a concise justification of its suitability.

## 3. Mandatory Technical Requirements

The proposed dApp must satisfy all the following requirements:

- Make genuine and essential use of Bitcoin Taproot Script Path spending.
- Use actual Tapscript spending conditions to implement part of the application's core logic.
- Explain how the Taproot output and its script tree (taptree) would be constructed.
- Describe the conditions under which the relevant script paths can be executed.
- Explain how a transaction spending the Taproot output through a script path would be constructed, signed and broadcast.
- Include a complete web-based frontend and the necessary backend components.
- Be realistically deployable and testable on Bitcoin Regtest.

A conventional Bitcoin payment, a key-path-only implementation or a standard transaction interface is not sufficient.

The application must demonstrate why Taproot Script Path is necessary for its proposed functionality.

Respect the actual capabilities and limitations of Bitcoin Script and Tapscript. Do not assume the existence of arbitrary smart contract execution, unsupported opcodes, covenant functionality or other protocol features that Bitcoin does not natively provide.

Clearly identify any functionality that requires additional off-chain logic or external infrastructure.

## 4. Required Proposal Structure

### 4.1 Project Overview

Provide:
- Application name.
- Brief description.
- Problem statement.
- Main objective.
- Target users.
- Practical use cases.

### 4.2 Core Functionality

Describe:
- The application's main features.
- The operations available to users.
- The complete user workflow, step by step.
- The expected behavior in normal and alternative scenarios.
- The role of Bitcoin transactions in the application.

Clearly distinguish between on-chain operations and off-chain operations.

### 4.3 Bitcoin Taproot Integration

Explain the technical integration in detail:

- Why Taproot Script Path is essential to the application.
- How the Taproot output and taptree are designed.
- The number and purpose of the proposed script leaves.
- The spending conditions implemented by each relevant script.
- How the script-path spending process works.
- How the spending transaction and witness are constructed.
- How the application verifies that the spending conditions have been satisfied.

Identify the relevant Bitcoin standards, particularly BIP-341 and BIP-342.

Explain any assumptions about cryptographic signatures, keys, timelocks and transaction construction.

### 4.4 Technical Architecture

Describe the complete application architecture.

**Backend:**
- Main components and responsibilities.
- Transaction construction and broadcasting.
- Interaction with a Bitcoin Regtest node.
- Wallet and signing integration.
- Transaction monitoring and confirmation handling.
- Database or persistent storage requirements.

**Frontend:**
- Main pages and interface components.
- Wallet connection and interaction.
- User operations.
- Transaction creation and confirmation flow.
- Display of balances, transaction status and relevant information.

**System Integration:**

Explain how the frontend, backend, wallets and Bitcoin network interact.

Include a clear description of the complete data and transaction flow.

### 4.5 Security Analysis

Identify the main security considerations:

- Unauthorized spending attempts.
- Incorrect script conditions.
- Signature and key management.
- Transaction construction errors.
- Malicious user inputs.
- Backend and frontend vulnerabilities.
- Potential misuse or failure scenarios.

Explain how the proposed architecture addresses these risks.

### 4.6 Implementation Requirements and Feasibility

Identify the technologies required to implement the application:

- Programming languages.
- Bitcoin libraries and SDKs.
- Wallet software or wallet APIs.
- Backend framework.
- Frontend framework.
- Bitcoin Core Regtest node.
- Additional infrastructure and dependencies.

Explain:
- How the application would be deployed on Bitcoin Regtest.
- Which features can be tested on Regtest.
- Which components require external services.
- The main implementation challenges.
- The estimated development complexity.
- Whether the complete application is realistically achievable within an undergraduate thesis.

Prefer established and documented tools. Do not assume that a library supports a specific Taproot feature without technical justification.

### 4.7 Expected Functional Tests

Identify between 3 and 5 essential functional operations that could later be used to evaluate the completed application.

For each operation, specify:

- Test objective.
- Required initial conditions.
- Action to perform.
- Expected result.
- Evidence that can be used to verify success.

At least one test must explicitly verify successful Taproot Script Path spending.

Include relevant negative scenarios where appropriate, such as an attempt to spend funds without satisfying the required script conditions.

Do not produce the complete test plan at this stage.

## 5. Design Constraints

The proposal must follow these principles:

- Prioritize a fully working application over an ambitious but incomplete concept.
- Avoid unnecessary features that do not contribute to the core objective.
- Minimize external dependencies and infrastructure requirements.
- Ensure that the main functionality can be demonstrated through a web interface.
- Ensure that the blockchain operations can be independently verified.
- Do not rely on a centralized backend to enforce conditions that are supposed to be enforced by Bitcoin scripts.
- Clearly distinguish protocol-level guarantees from application-level assumptions.
- Do not invent technical capabilities or claim that an operation is possible without explaining how it would work.
- Use Bitcoin Regtest as the exclusive blockchain environment for development and functional testing.
- Do not require Signet, Testnet or Mainnet for any part of the implementation or evaluation.
- Assume that a locally controlled Bitcoin Core Regtest node is available, allowing blocks to be generated on demand and transactions to be tested without waiting for public network confirmations.
- Prefer local infrastructure and deterministic test conditions wherever possible.

## 6. Final Assessment

Conclude with a brief assessment covering:

- Why this is a strong use case for Taproot Script Path.
- Its main technical advantages.
- Its most significant implementation risks.
- Its overall feasibility for a complete implementation and Regtest demonstration within the scope of an undergraduate thesis.

## Final Instructions

Propose exactly ONE Bitcoin Taproot dApp.

Do not generate source code, scripts or implementation files.

Do not begin development, deployment or testing.

Do not provide alternative application concepts.

Focus exclusively on producing the best technically sound, useful, secure and realistically implementable proposal you can design.

The output must be sufficiently detailed to serve as the technical specification for a subsequent implementation phase.





# Bitcoin Taproot dApp – Repair Prompt

The generated project has been executed and tested. An error or unexpected behavior has been encountered.

Your task is to analyze and fix the reported problem in your existing implementation.

## Instructions

1. Examine the existing project files and identify the root cause of the reported error.
2. Fix the problem directly in the existing code.
3. Preserve the original project requirements, architecture and intended functionality.
4. Do not remove existing features or change the application's intended behavior to avoid the error.
5. Make only the changes necessary to resolve the reported problem.
6. Do not perform unnecessary refactoring or rewrite working components.
7. Do not introduce unrelated features or functionality.
8. Ensure that any changes remain compatible with the existing project.
9. If the problem involves Bitcoin, verify that the proposed correction follows the actual Bitcoin protocol rules and Taproot specifications.
10. Do not replace real blockchain operations with simulated transactions or placeholder implementations.
11. Do not simply suppress errors or bypass validation to make the application appear functional.
12. Preserve security requirements and correct transaction validation.
13. The target blockchain environment is Bitcoin Regtest. Preserve Regtest as the exclusive network for development and testing. Do not migrate the application to Signet, Testnet or Mainnet, even as a workaround for an implementation problem.
14. Ensure that any changes involving Bitcoin nodes, RPC connections, wallets or transaction broadcasting remain compatible with a locally running Bitcoin Core Regtest node.

## Error Report

The following error or unexpected behavior was encountered while running the project:

[INSERT THE EXACT ERROR MESSAGE, LOG OR FAILED TEST RESULT HERE]

## Verification

After implementing the correction:

- Check that the reported problem has been addressed.
- Run the relevant installation, build, startup or test commands when available.
- Check that the correction has not introduced new errors.
- Verify that existing functionality remains intact.
- Verify that Bitcoin operations use the local Regtest network.
- Do not claim that a test has passed unless it has actually been executed successfully.

If the issue cannot be fully resolved, explain what remains broken and identify any additional information or configuration required.

## Final Response

Provide a brief report containing:

1. Root cause of the problem.
2. Description of the correction implemented.
3. Files modified.
4. Tests or commands executed and their results.
5. Any remaining errors or limitations.

Fix the existing implementation without changing the original project requirements.

Do not redesign or replace the application. Focus exclusively on resolving the reported problem.





# Bitcoin Taproot dApp – Generation Prompt

## 1. Role and Objective

Act as an experienced Bitcoin developer, blockchain engineer and full-stack software architect.

Your task is to design and implement a complete, functional, web-based decentralized application (dApp) based on the project description provided below.

The application must include all necessary backend and frontend components and must be capable of interacting with the Bitcoin blockchain.

The primary objective is to deliver a working application rather than a prototype or a conceptual demonstration.

## 2. Project Description

[INSERT THE MODEL-SPECIFIC DAPP PROPOSAL HERE]

Implement the application according to this project description. Preserve its main objectives, functionality and requirements.

## 3. General Functional Requirements

- Implement all essential features described in the project specification.
- Provide a complete and usable web-based frontend.
- Implement the necessary backend functionality.
- Ensure that frontend and backend components communicate correctly.
- Support the complete application workflow, from initial user interaction to blockchain transaction execution.
- Provide appropriate input validation and error handling.
- Display relevant transaction information and application status to users.
- Ensure that the application behaves correctly in both successful and unsuccessful scenarios.
- Avoid implementing placeholder functionality for features that are expected to work.

## 4. Bitcoin and Taproot Requirements

The application must make genuine use of Bitcoin Taproot Script Path spending as an essential part of its functionality.

Requirements:

- Implement Taproot output construction and the required script tree.
- Implement the necessary Tapscript spending conditions.
- Support the construction and signing of Taproot transactions.
- Correctly construct script-path witnesses, including the required script and control block.
- Ensure that transactions satisfy Bitcoin consensus rules.
- Support broadcasting transactions and monitoring their status.
- Use Bitcoin Regtest as the exclusive target network for development and functional testing.
- Follow the relevant Bitcoin standards, particularly BIP-341 and BIP-342.
- Do not rely exclusively on Taproot Key Path spending.
- Do not assume that Bitcoin Script provides general-purpose smart contract execution.
- Do not use nonexistent opcodes or unsupported protocol features.

Select appropriate libraries and tools for Taproot transaction construction, wallet integration and blockchain interaction.

Clearly distinguish between on-chain functionality and off-chain application logic.

### Regtest-specific requirements

- Use a locally controlled Bitcoin Core Regtest node as the blockchain infrastructure.
- Configure the application to communicate with the node through its Regtest RPC interface.
- Make the RPC host, port and authentication credentials configurable through environment variables.
- Do not hard-code RPC credentials or other sensitive configuration values.
- Support wallet creation or loading and the necessary wallet operations on Regtest.
- Allow blocks to be generated on demand when necessary to confirm transactions and test timelocks.
- Use Regtest mining capabilities, such as `generatetoaddress`, when appropriate.
- Do not depend on public blockchain explorers, public testnet APIs or external services for essential blockchain operations.
- Do not use Signet, Testnet or Mainnet as a fallback.
- Ensure that the application can independently verify transactions, UTXOs and confirmations through the local Bitcoin Core node.

## 5. Backend Requirements

Implement all necessary backend components.

The backend should:

- Handle application logic and business operations.
- Construct Bitcoin transactions and relevant scripts.
- Manage Taproot output and spending information.
- Interact with the local Bitcoin Core Regtest node through RPC.
- Support transaction broadcasting and monitoring.
- Validate user inputs and transaction parameters.
- Handle errors and unsuccessful blockchain operations.
- Persist application data when required by the project.
- Support the generation of Regtest blocks when required for transaction confirmation and testing.

The backend must not store or expose users' private keys. Signing should be performed through an appropriate wallet or secure local signing mechanism compatible with Regtest.

## 6. Frontend Requirements

Implement a complete web-based user interface.

The frontend should:

- Provide an intuitive interface for the application's main operations.
- Allow users to connect and interact with a compatible Bitcoin wallet or secure local signing mechanism that supports the Regtest environment.
- Display relevant Bitcoin Regtest network information.
- Allow users to perform the operations described in the project specification.
- Show transaction details, status and confirmation information.
- Provide clear feedback for successful operations and errors.
- Validate user input before submitting operations.

The frontend must be connected to the actual backend functionality. Do not create buttons or interface components that do not perform their intended operations.

Do not silently switch to another Bitcoin network if a wallet does not support Regtest. Select a technically compatible signing solution and clearly document any required configuration.

## 7. Security and Reliability

- Follow Bitcoin consensus and transaction validation rules.
- Validate transaction parameters before broadcasting.
- Ensure that spending conditions are correctly enforced by Bitcoin scripts.
- Protect private keys and sensitive information.
- Validate user inputs on both frontend and backend.
- Handle rejected transactions, insufficient funds and network failures.
- Avoid exposing secrets or sensitive configuration values in source code.
- Use environment variables for configurable credentials and service endpoints.
- Avoid unnecessary external dependencies and insecure implementation patterns.

## 8. Expected Project Files

Generate all files necessary for a complete and functional application.

The project should include, where appropriate:

- Package and dependency configuration files.
- Backend source code.
- Frontend source code.
- Bitcoin transaction and Taproot implementation components.
- Wallet integration.
- Configuration files and environment variable examples.
- Database or persistent storage components, if required.
- Scripts for installation, startup and other necessary operations.
- A README containing setup, installation, configuration and execution instructions.

Additional files and directories may be created when technically necessary. Do not restrict the implementation to a predefined number of files.

Organize the project clearly and consistently.

## 9. Implementation Instructions

- Generate the complete application, not just an architectural proposal or code snippets.
- Implement all essential functionality described in the project specification.
- Choose appropriate technologies and libraries based on their actual capabilities.
- Use compatible and documented library functions.
- Ensure that all required components are properly connected.
- Include appropriate error handling and logging.
- Provide clear instructions for configuring the environment and running the application.
- Do not omit implementation details by replacing them with TODO comments or placeholders.
- Do not assume that external infrastructure is already configured unless explicitly stated.
- Clearly document any manual setup requirements.
- Ensure that the application uses Bitcoin Regtest throughout its implementation and does not contain dependencies on Signet, Testnet or Mainnet.

If additional files are necessary to make the application work correctly, create them.

## 10. Final Requirements

The final result must be a complete application that can be installed, started and tested on Bitcoin Regtest.

Prioritize:

1. Functional correctness.
2. Correct Bitcoin Taproot Script Path implementation.
3. Security and compliance with Bitcoin protocol rules.
4. Reliable backend and frontend integration.
5. Ease of installation and execution.
6. Clear project organization and documentation.

Do not provide only a theoretical explanation of the proposed architecture.

Generate the actual project files and implement the application.

The final response should summarize:

- Implemented functionality.
- Project structure.
- Technologies and libraries used.
- Installation and startup instructions.
- Required environment configuration.
- Any known limitations or incomplete features.




# Ethereum EIP-7702 dApp – Proposal Generation

## 1. Role and Objective

Act as a senior Ethereum developer, blockchain architect and decentralized application designer.

Your task is to design the strongest possible decentralized application (dApp) based on Ethereum EIP-7702, specifically exploiting its account delegation mechanism to enable programmable functionality for Externally Owned Accounts (EOAs).

The objective is to propose an original, useful and technically sound application that can be fully implemented, deployed and tested as part of an undergraduate computer science thesis.

The application must demonstrate the practical value of EIP-7702 rather than using it as a superficial feature or simply implementing a conventional smart contract application.

You have complete freedom to choose the application concept. Do not assume a predefined use case or simply reproduce a conventional blockchain application.

The application must use a locally controlled Geth node running in Developer Mode (`--dev`) as its exclusive Ethereum network for development and functional testing.

## 2. Proposal Selection and Optimization

Before producing your final proposal, consider different possible application concepts and select the one that offers the strongest overall balance across the following criteria:

1. **Protocol integration:** EIP-7702 must be essential to the application's main functionality, not merely used to connect a wallet or authorize a standard transaction.
2. **Technical correctness:** The proposed design must respect EIP-7702 specifications, Ethereum transaction rules and actual EVM capabilities.
3. **Practical usefulness:** The application should solve a meaningful problem or provide a useful service.
4. **Originality:** Prefer an interesting application concept over a basic demonstration of account delegation.
5. **Implementation feasibility:** The project must be realistically implementable with available technologies and compatible wallet interfaces.
6. **Security:** The design must account for authorization signatures, delegation, smart contract execution, transaction validation and potential vulnerabilities.
7. **Testability:** Its essential functionality must be objectively verifiable on a local Geth Developer Mode network.
8. **Manageable complexity:** The project should be sufficiently substantial for an undergraduate thesis without requiring unnecessarily complex infrastructure.

Select ONE proposal that best satisfies these criteria.

Do not present alternative proposals. Provide only the selected application and a concise justification of its suitability.

## 3. Mandatory Technical Requirements

The proposed dApp must satisfy all the following requirements:

- Make genuine and essential use of Ethereum EIP-7702.
- Use EIP-7702 account delegation to allow an EOA to execute code from an already deployed smart contract implementation.
- Explain how an EOA is authorized to delegate its code and how the delegated implementation is used.
- Include actual EIP-7702 authorization signatures and the corresponding transaction mechanism.
- Explain how the delegated smart contract implements the application's core functionality.
- Describe how the original EOA retains its identity, address, balance and signing authority after delegation.
- Explain how delegated execution interacts with the EOA's storage and account context.
- Describe how the application handles delegation replacement and revocation.
- Include a complete web-based frontend and the necessary backend components.
- Be realistically deployable and testable using Geth Developer Mode.

### 3.1 EIP-7702 Protocol Requirements

The proposal must demonstrate an accurate understanding of EIP-7702.

In particular, explain the following mechanisms:

**Delegation authorization:**

- EIP-7702 introduces a new transaction type, identified by `0x04`.
- The transaction contains an authorization list.
- Each authorization tuple has the following structure:

  `[chain_id, address, nonce, y_parity, r, s]`

- The authorization signature must be generated according to the EIP-7702 signing procedure, using the digest:

  `keccak256(0x05 || rlp([chain_id, address, nonce]))`

- Explain the distinction between the authorization signature and the outer transaction signature.
- Explain the role of the authority account, the delegated contract address and the transaction sender.
- Explain how an authorization is validated and applied by the Ethereum execution layer.

**Delegation mechanism:**

- Explain how the delegation indicator `0xef0100 || address` is stored in the EOA account's code.
- Explain how Ethereum resolves the delegated implementation when executing operations against the delegated account.
- Explain that the implementation's code executes in the context of the authority EOA, including its address, balance and storage.
- Explain that the delegation remains active until it is replaced or removed through another valid authorization.
- Explain how delegation can be reset by authorizing delegation to the zero address.

**Authorization and execution behavior:**

- Explain chain ID validation, nonce handling and replay protection.
- Explain the difference between the authority signing an authorization and the account that submits or pays for the outer transaction.
- Explain how a relayer or another account could submit an authorized transaction on behalf of the EOA, if the proposed application requires it.
- Explain the order in which authorization processing and transaction execution occur.
- Account for the fact that a successfully processed delegation authorization is not rolled back merely because the subsequent execution portion of the transaction reverts.
- Respect the requirement for a non-empty authorization list in type-4 transactions and the applicable transaction validation rules.

Do not assume that EIP-7702 automatically provides all smart account capabilities.

In particular:

- Transaction batching must be implemented by the delegated smart contract.
- Custom permissions and spending restrictions must be implemented and enforced by the delegated smart contract.
- Session keys and restricted signing authority require explicit implementation.
- Gas sponsorship requires an actual transaction sponsor or relayer that pays the transaction fee.
- Security policies, recovery mechanisms and additional account features must not be attributed to EIP-7702 itself unless they are explicitly implemented by the application.

Clearly distinguish between protocol-level functionality and application-level smart contract logic.

### 3.2 Wallet Integration Requirements

You have complete freedom to choose the wallet integration and signing architecture that best supports the proposed application.

The selected approach must:

- Be technically compatible with the EIP-7702 authorization workflow.
- Support the generation and signing of genuine EIP-7702 authorization tuples.
- Support the construction, signing and submission of type-4 transactions.
- Be compatible with the locally controlled Geth Developer Mode network.
- Allow the user to interact with the application through its web interface.
- Provide a clear and secure mechanism for connecting or selecting the authority EOA.
- Correctly handle authorization signatures and outer transaction signatures.
- Clearly distinguish between wallet connection, authorization signing and transaction submission.

You may choose an existing browser wallet, a suitable SDK, a local signing mechanism or another technically justified integration.

Do not select a wallet or library merely because it supports ordinary Ethereum transactions. Verify that the chosen solution supports the specific EIP-7702 authorization workflow required by the application.

Do not assume that ordinary transaction signing or `personal_sign` is equivalent to EIP-7702 authorization signing.

If the selected wallet or signing mechanism does not support the required authorization functionality on a custom local Geth network, identify this limitation explicitly and evaluate a technically viable alternative.

Never simulate a wallet connection or pretend that an authorization or transaction has been signed successfully.

Never request or expose the user's private key or seed phrase through the application.

Explain the reasons for selecting the proposed wallet integration and identify its compatibility limitations and implementation risks.

## 4. Required Proposal Structure

### 4.1 Project Overview

Provide:

- Application name.
- Brief description.
- Problem statement.
- Main objective.
- Target users.
- Practical use cases.

Explain why EIP-7702 offers a meaningful advantage for the proposed application compared with a conventional EOA and a conventional smart contract.

### 4.2 Core Functionality

Describe:

- The application's main features.
- The operations available to users.
- The complete user workflow, step by step.
- The expected behavior in normal and alternative scenarios.
- The role of EIP-7702 delegation in the application.
- The role of the delegated smart contract.
- The role of conventional Ethereum smart contracts, where required.
- The role of the user's EOA and any external transaction sponsor.

Clearly distinguish between:

- Operations executed by the delegated EOA.
- Operations executed by other smart contracts.
- Operations handled by the backend.
- Operations requiring user authorization.
- Operations requiring an external relayer or sponsor.

The application must remain understandable and usable through its web interface.

### 4.3 Ethereum EIP-7702 Integration

Explain the technical integration in detail:

- Why EIP-7702 is essential to the application.
- Which EOA account is delegated.
- Which smart contract serves as the delegated implementation.
- How the implementation contract is deployed.
- How the EOA authorizes the delegation.
- How the authorization tuple is constructed and signed.
- How the type-4 transaction is created, signed and submitted.
- How the delegated account executes the application's core operations.
- How any additional smart contracts interact with the delegated account.
- How the application verifies the delegation and execution results.
- How the delegation can be updated or revoked.

Include a clear explanation of the complete transaction lifecycle.

Describe which operations are performed in one transaction and which require separate transactions.

Explain how the application handles:

- Authorization nonces.
- Chain ID restrictions.
- Authorization signatures.
- Transaction signatures.
- Delegation persistence.
- Execution failures and transaction reverts.
- Invalid or expired authorizations, where applicable.
- Replay attempts and unauthorized operations.

Identify the relevant Ethereum standards, particularly EIP-7702, EIP-2718 and any other relevant standards.

Respect the actual behavior of Ethereum's authorization processing and EVM execution.

Do not assume that EIP-7702 automatically turns an EOA into an independently deployed smart contract account or that multiple delegated implementations can be active simultaneously for the same EOA.

### 4.4 Technical Architecture

Describe the complete application architecture.

**Backend:**

- Main components and responsibilities.
- Interaction with the local Geth JSON-RPC endpoint.
- Smart contract deployment and interaction.
- EIP-7702 authorization preparation and transaction construction.
- Transaction submission and monitoring.
- Event and transaction receipt handling.
- Database or persistent storage requirements.
- Management of application data and user activity.
- Any optional relayer or sponsorship component, if required.

The backend must not impersonate the user or bypass wallet authorization.

**Frontend:**

- Main pages and interface components.
- Wallet connection or account selection.
- Local Geth network detection and selection.
- Delegation status display.
- Authorization and delegation workflow.
- User operations provided by the application.
- Transaction creation and confirmation flow.
- Display of balances, transaction status and relevant information.
- Delegation replacement or revocation interface, where applicable.

**Smart Contracts:**

Describe:

- The delegated implementation contract.
- Any additional contracts required by the application.
- The responsibilities of each contract.
- How storage is organized in the delegated EOA context.
- How access control and execution restrictions are enforced.
- How contract initialization is performed securely.
- How contracts interact with external contracts, if required.

**System Integration:**

Explain how the frontend, selected wallet or signing mechanism, backend, delegated implementation contracts, other smart contracts and Geth interact.

Include a clear description of the complete data and transaction flow, from the user's initial interaction to the final on-chain result.

### 4.5 Security Analysis

Identify the main security considerations:

- Unauthorized EOA delegation.
- Malicious or compromised delegated implementation contracts.
- Compromised authorization signatures.
- Replay attacks and incorrect nonce management.
- Incorrect chain ID restrictions.
- Unauthorized transaction submission.
- Malicious or unrestricted relayer behavior.
- Unauthorized transfers of ETH or tokens.
- Incorrect implementation of batch execution.
- Reentrancy and external contract interactions.
- Incorrect storage handling in the delegated EOA context.
- Front-running of initialization.
- Transaction execution failures and unexpected delegation persistence.
- Malicious user inputs.
- Backend and frontend vulnerabilities.
- Private key and signing security.

Explain how the proposed architecture addresses these risks.

Pay particular attention to the fact that delegated implementation code can have substantial control over the authority EOA's assets and storage.

Explain how the application restricts targets, calldata, transaction values and execution permissions where appropriate.

Do not rely exclusively on frontend validation or backend checks to enforce permissions that must be enforced on-chain.

Clearly distinguish between security guarantees provided by Ethereum and those implemented by the application.

### 4.6 Implementation Requirements and Feasibility

Identify the technologies required to implement the application:

- Programming languages.
- Solidity compiler.
- Ethereum development libraries and SDKs.
- EIP-7702-compatible transaction and authorization tooling.
- Wallet integration and its supported interfaces.
- Backend framework.
- Frontend framework.
- Geth Ethereum client.
- Database or persistent storage.
- Additional infrastructure and dependencies, if necessary.

Prefer established and documented tools.

Do not assume that a library supports EIP-7702 authorization signing or type-4 transaction construction without technical justification.

**Geth Developer Mode configuration:**

The exclusive blockchain environment must be a locally controlled Geth node running in Developer Mode (`--dev`).

The proposal must account for the following characteristics:

- Geth Developer Mode creates a single-node local Ethereum network.
- The node does not connect to external Ethereum peers.
- A pre-funded developer account is available for local testing.
- Blocks can be generated on demand when transactions are pending.
- Transactions and smart contracts are executed locally without using real ETH.
- The node exposes a local JSON-RPC interface.

Use the default local RPC endpoint as a reference:

`http://127.0.0.1:8545`

However, verify the actual configured endpoint instead of assuming it is fixed.

Do not hardcode a Chain ID. The application must retrieve the actual chain ID through the RPC interface using `eth_chainId`.

**EIP-7702 compatibility:**

- Verify that the installed Geth version supports EIP-7702.
- Ensure that the Developer Mode chain configuration activates the necessary protocol rules, including the Prague/Pectra fork or a later compatible fork.
- Verify that type-4 transactions and authorization lists are actually accepted and processed by the local node.
- Do not assume that using `--dev` alone proves that all required EIP-7702 functionality works.

**Persistence and deployment:**

- Explain how Geth's data directory is configured.
- Account for Developer Mode's ephemeral behavior when no persistent data directory is configured.
- Prefer a dedicated local data directory when preserving the blockchain state between application restarts is necessary.
- Explain how smart contracts are deployed to the local network.
- Ensure that the application can be restarted and used consistently during the experiments.

Explain:

- How the application would be deployed on Geth Developer Mode.
- Which features can be tested locally.
- Which components require external services, if any.
- The main implementation challenges.
- The estimated development complexity.
- Whether the complete application is realistically achievable within an undergraduate thesis.

### 4.7 Expected Functional Tests

Identify between 3 and 5 essential functional operations that could later be used to evaluate the completed application.

For each operation, specify:

- Test objective.
- Required initial conditions.
- Action to perform.
- Expected result.
- Evidence that can be used to verify success.

The tests must objectively demonstrate that the application uses EIP-7702 rather than merely interacting with conventional smart contracts.

At least one test must explicitly verify successful EOA delegation using an actual EIP-7702 authorization and type-4 transaction.

Include relevant negative scenarios where appropriate, such as:

- Invalid authorization signatures.
- Incorrect chain IDs.
- Reused authorization nonces.
- Unauthorized delegated operations.
- Operations violating the application's permission rules.
- Failed execution and the resulting delegation state.

Do not produce the complete test plan at this stage.

## 5. Design Constraints

The proposal must follow these principles:

- Prioritize a fully working application over an ambitious but incomplete concept.
- EIP-7702 must be essential to the application's main functionality.
- Avoid unnecessary features that do not contribute to the core objective.
- Minimize external dependencies and infrastructure requirements.
- Ensure that the main functionality can be demonstrated through a web interface.
- Ensure that blockchain operations can be independently verified through Geth RPC.
- Choose the wallet integration and signing architecture freely, based on technical compatibility, security and implementation feasibility.
- Use Geth Developer Mode (`--dev`) as the exclusive blockchain environment for development and functional testing.
- Do not use Ethereum Mainnet, Sepolia, Holesky or any other public network for implementation or evaluation.
- Do not use Anvil, Hardhat Network or Ganache as alternative blockchain execution environments.
- Development tools may be used for compiling, deploying and testing contracts, provided that all blockchain operations execute on the Geth Developer Mode network.
- Assume that a locally controlled Geth node is available, allowing transactions and blocks to be tested without waiting for public network confirmations.
- Prefer local infrastructure and deterministic test conditions wherever possible.
- Do not simulate EIP-7702 authorization, wallet connections, delegation, transaction submission or execution results.
- Do not claim that gas sponsorship, transaction batching, session keys or custom permissions are provided automatically by EIP-7702.
- Do not rely on a centralized backend to enforce conditions that should be enforced by the delegated smart contract.
- Clearly distinguish protocol-level guarantees from application-level assumptions.
- Do not invent technical capabilities or claim that an operation is possible without explaining how it would work.
- Do not include unnecessary dependencies such as ERC-4337 bundlers or external paymaster infrastructure unless the chosen concept genuinely requires them and their local implementation is justified.

## 6. Final Assessment

Conclude with a brief assessment covering:

- Why this is a strong use case for EIP-7702.
- Its main technical advantages.
- The specific EIP-7702 capabilities that make the application possible.
- Its most significant implementation and signing compatibility risks.
- Its overall feasibility for a complete implementation and local Geth Developer Mode demonstration within the scope of an undergraduate thesis.

## Final Instructions

Propose exactly ONE Ethereum EIP-7702 dApp.

Do not generate source code, scripts or implementation files.

Do not begin development, deployment or testing.

Do not provide alternative application concepts.

Focus exclusively on producing the best technically sound, useful, secure and realistically implementable proposal you can design.

The output must be sufficiently detailed to serve as the technical specification for a subsequent implementation phase.

When describing technical feasibility, explicitly identify any assumptions that must be verified against the installed Geth version, the EIP-7702 implementation and the selected wallet or signing interface.

Do not present unverified wallet or protocol capabilities as established facts.




# Ethereum EIP-7702 dApp – Repair Prompt

The generated project has been executed and tested. An error or unexpected behavior has been encountered.

Your task is to analyze and fix the reported problem in your existing implementation.

## Instructions

1. Examine the existing project files and identify the root cause of the reported error.
2. Fix the problem directly in the existing code.
3. Preserve the original project requirements, architecture and intended functionality.
4. Do not remove existing features or change the application's intended behavior to avoid the error.
5. Make only the changes necessary to resolve the reported problem.
6. Do not perform unnecessary refactoring or rewrite working components.
7. Do not introduce unrelated features or functionality.
8. Ensure that any changes remain compatible with the existing project.
9. If the problem involves Ethereum, verify that the proposed correction follows the actual Ethereum protocol rules and EIP-7702 specifications.
10. Do not replace real blockchain operations, EIP-7702 authorizations or smart contract interactions with simulated transactions or placeholder implementations.
11. Do not simply suppress errors or bypass validation to make the application appear functional.
12. Preserve security requirements, correct authorization handling, transaction validation and smart contract execution rules.
13. The target blockchain environment is a locally running Geth node in Developer Mode (`--dev`). Preserve this as the exclusive network for development and testing. Do not migrate the application to Ethereum Mainnet, Sepolia, Holesky or any other public network, even as a workaround for an implementation problem.
14. Ensure that any changes involving Ethereum nodes, RPC connections, account signing, EIP-7702 authorizations, transaction submission or smart contract interactions remain compatible with the existing local Geth Developer Mode environment.
15. Do not assume that ordinary transaction signing is equivalent to EIP-7702 authorization signing. Preserve the correct authorization signature and type-4 transaction workflow.
16. Do not hardcode an assumed Chain ID or RPC endpoint when the application can retrieve the actual network configuration through Geth JSON-RPC.
17. Do not expose private keys, seed phrases or sensitive signing material through the frontend, backend logs or application interface.
18. Do not claim that EIP-7702 delegation, transaction batching, permission restrictions, gas sponsorship or other account features work unless they are actually implemented and verified.

## Error Report

The error or unexpected behavior encountered while running the project is described below:

[INSERT THE ERROR DESCRIPTION HERE]

Please investigate the reported problem and fix its underlying cause without changing the original project requirements.

After implementing the correction, explain which files were modified and provide the commands and steps required to restart and retest the application.

## Verification

After implementing the correction:

- Check that the reported problem has been addressed.
- Run the relevant installation, build, startup or test commands when available.
- Check that the correction has not introduced new errors.
- Verify that existing functionality remains intact.
- Verify that blockchain operations use the local Geth Developer Mode network.
- Verify that the actual network supports the EIP-7702 functionality required by the application.
- When relevant, verify authorization signatures, authorization nonces, chain ID restrictions, type-4 transaction construction and transaction execution.
- Do not claim that a test has passed unless it has actually been executed successfully.

If the issue cannot be fully resolved, explain what remains broken and identify any additional information or configuration required.

## Final Response

Provide a brief report containing:

1. Root cause of the problem.
2. Description of the correction implemented.
3. Files modified.
4. Tests or commands executed and their results.
5. Any remaining errors or limitations.

Fix the existing implementation without changing the original project requirements.

Do not redesign or replace the application. Focus exclusively on resolving the reported problem.




# Ethereum EIP-7702 dApp – Generation Prompt

## 1. Role and Objective

Act as an experienced Ethereum developer, blockchain engineer and full-stack software architect.

Your task is to design and implement a complete, functional, web-based decentralized application (dApp) based on the project description provided below.

The application must include all necessary backend and frontend components and must be capable of interacting with the Ethereum blockchain.

The primary objective is to deliver a working application rather than a prototype or a conceptual demonstration.

## 2. Project Description

[INSERT THE MODEL-SPECIFIC ETHEREUM EIP-7702 DAPP PROPOSAL HERE]

Implement the application according to this project description. Preserve its main objectives, functionality and requirements.

## 3. General Functional Requirements

- Implement all essential features described in the project specification.
- Provide a complete and usable web-based frontend.
- Implement the necessary backend functionality.
- Ensure that frontend and backend components communicate correctly.
- Support the complete application workflow, from initial user interaction to blockchain transaction execution.
- Provide appropriate input validation and error handling.
- Display relevant transaction information and application status to users.
- Ensure that the application behaves correctly in both successful and unsuccessful scenarios.
- Avoid implementing placeholder functionality for features that are expected to work.

## 4. Ethereum and EIP-7702 Requirements

The application must make genuine use of Ethereum EIP-7702 (Set Code for EOAs) as an essential part of its functionality.

Requirements:

- Implement EIP-7702 authorization processing according to the official specification.
- Support the creation and signing of EIP-7702 authorization tuples.
- Correctly handle authorization fields, including chain ID, delegate contract address, nonce and signature components.
- Implement the required authorization signing and validation workflow.
- Construct and submit valid EIP-7702 type-4 transactions.
- Correctly encode and process authorization lists (`authorizationList`).
- Implement the delegation of an Externally Owned Account (EOA) to a designated smart contract implementation.
- Correctly handle delegated execution through the EOA.
- Ensure that the application correctly distinguishes between the EOA, the delegated implementation contract and other target contracts.
- Verify the delegation status through the account's on-chain code.
- Support the execution of the application's intended operations through the delegated account.
- Correctly handle transaction nonces, gas estimation, fees and authorization processing.
- Follow Ethereum consensus rules and the EIP-7702 specification.
- Do not simulate authorization or delegated execution. All essential operations must be performed through genuine blockchain transactions.

Select appropriate libraries and tools for EIP-7702 transaction construction, wallet integration, authorization signing and blockchain interaction.

Clearly distinguish between on-chain functionality and off-chain application logic.

### Geth-specific requirements

- Use a locally controlled Geth development node (`--dev`) as the exclusive blockchain infrastructure for development and functional testing.
- Configure the application to communicate with Geth through its JSON-RPC interface.
- Use the Geth development network with Chain ID 1337.
- Use the local RPC endpoint `http://127.0.0.1:8545`, unless a configurable equivalent is required by the execution environment.
- Configure the RPC endpoint through environment variables where appropriate.
- Do not hard-code private keys or other sensitive configuration values.
- Support the use of Geth development accounts for funding and testing.
- Ensure that the application can retrieve account balances, nonces, transaction information, deployed contract code and block information through Geth RPC.
- Support local block production and transaction confirmation using Geth's development mode.
- Ensure that EIP-7702 functionality is supported by the selected Geth version and active development fork configuration.
- Do not use Ethereum Mainnet, Sepolia, Holesky or other public networks.
- Do not use Anvil, Hardhat Network, Ganache or other alternative local blockchain environments.
- Do not depend on public blockchain explorers or external RPC providers for essential blockchain operations.
- Ensure that the application can independently verify transactions, account delegation and contract execution through the local Geth node.

## 5. Backend Requirements

Implement all necessary backend components.

The backend should:

- Handle application logic and business operations.
- Construct and process EIP-7702 authorization data.
- Support the creation and validation of authorization tuples.
- Interact with the local Geth node through JSON-RPC.
- Construct and submit EIP-7702 type-4 transactions.
- Manage delegated account execution and smart contract interactions.
- Handle transaction broadcasting and monitoring.
- Retrieve account balances, nonces, code and transaction receipts.
- Validate user inputs and transaction parameters.
- Handle errors and unsuccessful blockchain operations.
- Persist application data when required by the project.
- Support local development and testing workflows.

The backend must not expose users' private keys or compromise wallet security. Authorization signing and transaction signing should be performed through an appropriate wallet or secure local signing mechanism.

## 6. Frontend Requirements

Implement a complete web-based user interface.

The frontend should:

- Provide an intuitive interface for the application's main operations.
- Allow users to connect and interact with a compatible Ethereum wallet.
- Support the EIP-7702 authorization signing workflow.
- Display the connected wallet address and the currently connected network.
- Clearly identify whether the connected account has an active EIP-7702 delegation.
- Display the delegated implementation address when delegation is active.
- Allow users to perform the operations described in the project specification.
- Show transaction details, status, hash and confirmation information.
- Provide clear feedback for successful operations and errors.
- Validate user input before submitting operations.
- Clearly distinguish between authorization, delegation and subsequent delegated execution transactions.

The frontend must be connected to the actual backend functionality. Do not create buttons or interface components that do not perform their intended operations.

Use a technically compatible wallet integration capable of signing EIP-7702 authorizations and submitting the required transactions.

Do not silently switch to another Ethereum network. Clearly report network incompatibility and require the appropriate Geth development network configuration.

## 7. Security and Reliability

- Follow Ethereum consensus rules and the EIP-7702 specification.
- Validate authorization data and signatures before submission.
- Correctly handle chain ID and nonce validation.
- Ensure that delegation is established only through valid authorization processing.
- Prevent unauthorized execution of delegated functionality.
- Validate transaction parameters before broadcasting.
- Protect private keys and sensitive information.
- Validate user inputs on both frontend and backend.
- Handle rejected signatures, insufficient funds, invalid nonces and network failures.
- Avoid exposing secrets or sensitive configuration values in source code.
- Use environment variables for configurable credentials and service endpoints.
- Avoid unnecessary external dependencies and insecure implementation patterns.

## 8. Expected Project Files

Generate all files necessary for a complete and functional application.

The project should include, where appropriate:

- Package and dependency configuration files.
- Backend source code.
- Frontend source code.
- EIP-7702 authorization and transaction implementation components.
- Smart contracts required by the application.
- Wallet integration.
- Geth configuration and startup scripts.
- Configuration files and environment variable examples.
- Database or persistent storage components, if required.
- Scripts for installation, compilation, deployment and startup.
- Automated tests for relevant smart contracts and application functionality.
- A README containing setup, installation, configuration and execution instructions.

Additional files and directories may be created when technically necessary. Do not restrict the implementation to a predefined number of files.

Organize the project clearly and consistently.

## 9. Implementation Instructions

- Generate the complete application, not just an architectural proposal or code snippets.
- Implement all essential functionality described in the project specification.
- Choose appropriate technologies and libraries based on their actual capabilities and EIP-7702 compatibility.
- Use compatible and documented library functions.
- Ensure that all required components are properly connected.
- Include appropriate error handling and logging.
- Provide clear instructions for configuring the environment and running the application.
- Do not omit implementation details by replacing them with TODO comments or placeholders.
- Do not assume that external infrastructure is already configured unless explicitly stated.
- Clearly document any manual setup requirements.
- Ensure that the application uses Geth `--dev` throughout its implementation and does not contain dependencies on public Ethereum networks or alternative local blockchain environments.

If additional files are necessary to make the application work correctly, create them.

## 10. Final Requirements

The final result must be a complete application that can be installed, started and tested on a local Geth development network.

Prioritize:

1. Functional correctness.
2. Correct EIP-7702 authorization and delegated execution implementation.
3. Security and compliance with Ethereum protocol rules.
4. Reliable backend and frontend integration.
5. Compatibility with the selected Geth development environment.
6. Ease of installation and execution.
7. Clear project organization and documentation.

Do not provide only a theoretical explanation of the proposed architecture.

Generate the actual project files and implement the application.

The final response should summarize:

- Implemented functionality.
- Project structure.
- Technologies and libraries used.
- Installation and startup instructions.
- Required environment configuration.
- Geth development network configuration.
- EIP-7702 authorization and delegation workflow.
- Any known limitations or incomplete features.

