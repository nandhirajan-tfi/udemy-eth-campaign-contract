# udemy-eth-campaign-contract

### Design
- Variables
    - manager - address- Address of the person managing the contract
    - minimumContribution - uint - Minimum donation to be considered as a approver
    - approvers - address[] - List of address who donated to the contract
    - requests - Request[] - List of requests that the manager has created to release the funds.Request is the struct type, it will have
        - description - Descripes why the request is being created
        - value - Amount of money the manager wanted to send
        - recepient - Address of the receiver
        - complete - status - true/false
        - approvals - mapping - track who has voted
        - approvalCount - track number of approvals

- Functions
    - Campaign - Constructor function that sets the minimumContribution and the owner
    - contribute - Called when someone wants to donate money to the campaign and become approver
    - createRequest - Called by the manager to create a new "Spending Request"
    - approveRequest - Called by each contributor to approve a spending request
    - finalizeRequest - After a request has gotten enough approvals, the manager can call this method to send the fund

- Voting Requirements
    - No multiple votings for the user
    - System can't wait for the voting for all approvers

- Use of memory keyword
- Use of storage keyword