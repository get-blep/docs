# User Onboarding & Authentication Module

At BLEP, we've engineered a seamless module that streamlines the onboarding and login processes for users, eliminating the need for a separate wallet, as commonly found in other web3 applications. Our goal is to make user onboarding and login experiences as smooth and intuitive as those in traditional web2 applications, ensuring a hassle-free journey into the BLEP ecosystem.

**New User Onboarding (Signup)**

When a new user decides to join BLEP, the process is designed to be user-friendly and straightforward. Here's how it works:

1. **User Interaction**: The user interacts with the BLEP app and provides the necessary information required for registration.
2. **Authentication**: The information provided by the user undergoes authentication through BLEP's internal services. This step ensures the uniqueness of the user's information and identity.
3. **On-Chain Registration**: Once the user's information is authenticated, it is encrypted and relayed to the blockchain, specifically to the BLEP Registry smart contract. This action registers the user within the BLEP ecosystem.
4. **Creating a Wallet**: To facilitate future interactions within the web3 environment, a wallet is generated for the user. Importantly, this process is designed to be discreet and seamlessly integrated, resembling the onboarding experience of a typical web2 app. This wallet will later serve the user for NFT / Token holdings and various web3 actions within the app.

\[Insert a detailed diagram here illustrating the onboarding process]

**Existing User Login**

For users who are already part of the BLEP community, logging in is a straightforward process. Here's how it works:

1. **User Interaction**: The existing user interacts with the BLEP app and enters their relevant login information.
2. **Web2 Authenticator Integration (Future Enhancement)**: We are actively working on integrating a web2 authenticator to further streamline the login process. This integration will simplify the login experience, making it even more user-friendly.
3. **Off-Chain Authentication**: The user's provided information is authenticated off-chain to ensure its accuracy and validity.
4. **Web3 Authentication**: BLEP's web3 authenticator service checks the user's information on-chain. Upon successful verification, the user's information is securely returned.
5. **Logging In**: With their validated information, the user is logged into the BLEP app, gaining access to their wallet and the entire BLEP ecosystem.

\[Insert a detailed diagram here illustrating the Login process]