### Chapter 6: Authentication and Access Control

#### 6.1 Authentication Process

**Definition and Importance:**
- Authentication is the fundamental building block and primary line of defense in security.
- It is the basis for most types of access control and user accountability [1].

**RFC 4949 Definition:**
- Authentication is defined as the process of verifying an identity claimed by or for a system entity.
- It consists of two steps:
  - **Identification Step:** Presenting an identifier to the security system (e.g., User ID).
  - **Verification Step:** Presenting or generating authentication information that corroborates the binding between the entity and the identifier (e.g., Password) [1].

#### 6.2 Means of Authentication

**Types of Authentication:**
Authentication can be based on four main categories:

1. **Something You Know:**
   - Passwords, PINs, answers to prearranged questions.
   - Example: Passwords are secret combinations of letters, numbers, and/or characters [2].

2. **Something You Have:**
   - Smartcards, electronic keycards, physical keys.
   - Example: Token-based authentication using specialized devices or smartphones [2].

3. **Something You Are:**
   - Physiological biometrics (fingerprint, retina, face) and cognitive biometrics (voice pattern, handwriting).
   - Example: Fingerprint scanners and facial recognition software [2].

4. **Something You Do:**
   - Behavioral biometrics (keystroke dynamics).
   - Example: Recognizing a user's unique typing rhythm [2].

##### 6.2.1 Password Authentication

- **Common Issues:**
  - Users find it difficult to memorize and recall long and complex passwords.
  - Users often reuse passwords or use weak passwords due to these challenges [2].

- **Attacks on Passwords:**
  - Pass the Hash Attack/Password Cracker
  - Password Spraying
  - Brute Force Attack
  - Rule Attack
  - Dictionary Attack
  - Rainbow Tables
  - Password Collections
  Each of these attacks exploits different vulnerabilities in password systems [2].

##### 6.2.2 Token-Based Authentication

- **Multifactor Authentication (MFA):**
  - Combines what a user knows (password) with what they have (token).
  - Examples include smart cards, windowed tokens, smartphones, and security keys [2].

- **Specialized Devices:**
  - Smart Cards: Require specialized hardware readers; vulnerable to card cloning.
  - Windowed Tokens: Display dynamic one-time passwords (OTPs); can be time-based (TOTP) or event-driven (HOTP) [2].

- **Smartphones:**
  - Authentication via phone calls, SMS text messages, or authentication apps.
  - Despite convenience, using smartphones for authentication is not considered highly secure due to phishing risks and malware [2].

- **Security Keys:**
  - Dedicated tokens inserted into USB ports or held near endpoints using NFC.
  - Feature attestation keys for cryptographic proof of device authenticity [2].

##### 6.2.3 Biometric Authentication

- **Physiological Biometrics:**
  - Uses unique body parts such as retinas, fingerprints, veins, gait, voice, iris, and face.
  - Requires specialized scanners or standard input devices like microphones and webcams [2].

- **Cognitive Biometrics:**
  - Based on perception, thought process, and understanding of the user.
  - Examples include Windows Picture Passwords where users select points of interest in an image [2].

##### 6.2.4 Behavioral Biometrics

- **Keystroke Dynamics:**
  - Recognizes users based on their unique typing rhythm.
  - Measures dwell time and flight time between keystrokes; requires no specialized hardware [2].

#### 6.3 User Authentication Security Issues and Solutions

**Security Issues:**

- Various attacks such as eavesdropping, host attacks, replay attacks, Trojan horses, denial-of-service attacks threaten user authentication systems.

**Solutions:**

- **Password Security:**
    * Salts: Random strings added to plaintext passwords before hashing to prevent dictionary and brute force attacks.
    * Key Stretching: Algorithms like bcrypt and PBKDF2 slow down password hashing; Argon2 is a stronger key stretching algorithm [1].

- **Managing Passwords:**
    * Password Length: Longer passwords are harder to crack.
    * Password Vaults: Secure repositories for storing passwords; includes password generators, online vaults, and password management applications [1].

- **Secure Authentication Technologies:**
    * Single Sign-On (SSO): Allows users to access multiple accounts with one set of credentials.
    * Authentication Services: RADIUS, Kerberos, directory services, SAML provide secure access to systems and applications [1].

#### 6.4 Access Control

**Definitions:**

- NIST IR 7298 defines access control as granting or denying requests to obtain and use information or enter physical facilities.
- RFC 4949 defines access control as regulating system resource use according to a security policy [1].

**Components of Access Control:**

- **Authentication:** Verification that user credentials are valid.
- **Authorization:** Granting rights or permissions to access system resources.
- **Audit:** Independent review of system records to ensure compliance with policies and detect security breaches [1].

**Types of Access Control Policies:**

1. **Discretionary Access Control (DAC):**
   - Controls access based on the identity of the requestor and access rules set by owners.
   - Implemented in most operating systems; uses an access control matrix [1].

2. **Mandatory Access Control (MAC):**
   - Controls access based on comparing security labels with security clearances.
   - More secure than DAC; prevents users from overriding policies [1].

3. **Role-Based Access Control (RBAC):**
   - Controls access based on roles within the system.
   - Users can be assigned multiple roles; roles have specific access rights [1].

4. **Attribute-Based Access Control (ABAC):**
   - Determines user access based on attributes associated with subjects, objects, actions, and environmental conditions.
   - Solves complexities in modern digital environments such as cloud services and IoT [1].

### Summary

Authentication is crucial for verifying identities before granting access to system resources. Various methods include passwords, tokens, biometrics, and behavioral biometrics. Each method has its own set of challenges and vulnerabilities but can be strengthened through solutions like salts, key stretching, password vaults, SSO, and secure authentication technologies.

Access control ensures that only authorized entities can use system resources by implementing policies such as DAC, MAC, RBAC, and ABAC. These policies regulate who can access what resources under what conditions.

Understanding these concepts is essential for maintaining robust security in today's complex digital landscape.
