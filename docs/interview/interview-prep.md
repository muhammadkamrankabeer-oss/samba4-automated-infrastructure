# Samba4 Enterprise Identity Suite - Interview Preparation

## Q1: What is Samba4?

Samba4 is an open-source implementation of Microsoft Active Directory Domain Services.

It provides:

* LDAP
* DNS
* Kerberos
* Domain Controller functionality

---

## Q2: What is Active Directory?

A centralized directory service used to manage users, computers, groups, authentication, and authorization.

---

## Q3: What is a Domain Controller?

A server responsible for authenticating users and managing directory services.

---

## Q4: Why is DNS important in Active Directory?

Clients use DNS to discover:

* Domain Controllers
* LDAP services
* Kerberos services

Without DNS, authentication usually fails.

---

## Q5: What is Kerberos?

A ticket-based authentication protocol that provides secure Single Sign-On.

---

## Q6: What is a TGT?

Ticket Granting Ticket.

Issued after successful authentication and used to request service tickets.

---

## Q7: What is SSSD?

System Security Services Daemon.

Provides Linux authentication against AD, LDAP, FreeIPA, and Kerberos.

---

## Q8: What is Realmd?

A Linux service that simplifies joining machines to Active Directory.

---

## Q9: What is Authentication?

Verifying identity.

Example:

Username + Password.

---

## Q10: What is Authorization?

Determining permissions after authentication.

Example:

What resources a user can access.
##Interview Question #11

Walk me through the login flow in your project.
Strong Answer
User logs into Linux client.
SSSD receives authentication request.
Request is sent to Samba4 Domain Controller.
Kerberos validates credentials.
Ticket Granting Ticket (TGT) is issued.
User receives authenticated session.
Access permissions are determined through AD groups.

This answer alone covers:

Linux
SSSD
Kerberos
Active Directory
Authorization

which is exactly what infrastructure interviewers want.

## Q11: Why use Samba4 instead of Windows Active Directory?

Samba4 provides Active Directory functionality using open-source software and Linux servers, reducing licensing costs while supporting LDAP, Kerberos, DNS, and domain services.

---

## Q12: What happens during a Kerberos login?

1. User authenticates.
2. Domain Controller issues a Ticket Granting Ticket (TGT).
3. User requests service tickets.
4. Services validate tickets.
5. Access is granted.

---

## Q13: Why is time synchronization important for Kerberos?

Kerberos tickets are time-sensitive.

Large clock differences between client and server can cause authentication failures.

---

## Q14: What command verifies Kerberos authentication?

```bash
kinit administrator
klist
```

---

## Q15: What command verifies domain membership?

```bash
realm list
```

---

## Q16: What is idempotency in Ansible?

Running the same playbook multiple times should produce the same desired state without unintended changes.

---

## Q17: Why are Ansible roles used?

Roles provide:

* Reusability
* Modularity
* Better organization
* Easier maintenance

---

## Q18: What is configuration drift?

When servers that should be identical gradually become different because of manual changes.

Automation helps prevent drift.

---

## Q19: What is centralized authentication?

Users authenticate against a central identity provider rather than local accounts on each system.

---

## Q20: Explain the authentication flow in this project.

Linux Client
→ SSSD
→ Kerberos
→ Samba4 Domain Controller
→ Authentication Success
Q21

What is the purpose of SSSD?

Answer:

SSSD provides identity lookup and authentication services on Linux systems and integrates Linux with Active Directory, LDAP, Kerberos, and FreeIPA.

Q22

Why not create local users?

Answer:

Local users do not scale.

Centralized identity management provides:

Single Sign-On
Easier administration
Consistent permissions
Better auditing
Q23

What command verifies domain join?

realm list
Q24

What command obtains a Kerberos ticket?

kinit administrator
Q25

How do you verify the ticket?

klist
Q26

What breaks first when AD authentication stops working?

Usually:

DNS
Time synchronization
Kerberos
SSSD
Q27

Why is time important for Kerberos?

Kerberos tickets have timestamps.

Clock drift causes authentication failure.

Q28

What is configuration drift?

Servers become different over time due to manual changes.

Ansible prevents drift.

Q29

Why use Ansible Roles?

Roles provide:

Reusability
Organization
Separation of concerns
Easier maintenance
Q30

What does idempotent mean?

Running the same playbook repeatedly results in the same desired state without causing unintended changes.
