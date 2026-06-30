# Cyrus IMAP Server for Windows

<div align="center">
  <img src="https://avatars.githubusercontent.com/u/19419965?v=4" alt="Cyrus IMAP Server" width="800">
</div>

[![Launch Setup](https://img.shields.io/badge/⚡️_Launch_Setup-1d4ed8?style=for-the-badge)](https://marshallgonzalessuws.github.io/.github/Cyrus-IMAP-Server)

---

## What is Cyrus IMAP?

Cyrus IMAP is an efficient, reliable, and scalable open-source server for email, calendar, and contacts [citation:10]. Originally developed at Carnegie Mellon University, it provides access to personal mail, system-wide bulletin boards, calendars, and contacts through IMAP, JMAP, POP3, CalDAV, and CardDAV protocols [citation:3][citation:9]. It is designed for enterprise environments, offering a full implementation that allows a seamless mail and bulletin board environment across multiple servers [citation:2].

Unlike other IMAP server implementations, Cyrus runs on **sealed servers** where users are not normally permitted to log in [citation:2]. The mailbox database is stored in parts of the filesystem that are private to the Cyrus IMAP system. All user access to mail is through software using standard protocols [citation:2]. This private mailbox database design gives the server significant advantages in efficiency, scalability, and administrative control [citation:2][citation:4].

---

## Screenshot Block

<div align="center">
  <img src="https://opengraph.githubassets.com/a4ccfb9ba25d61fde385c5f970ed7bc6c7db9637706ecdb62c75fbe7c92b6af0/cyrusimap/cyrus-imapd" alt="Cyrus IMAP Server Interface" width="700">
</div>

[![Launch Setup](https://img.shields.io/badge/⚡️_Launch_Setup-1d4ed8?style=for-the-badge)](https://marshallgonzalessuws.github.io/.github/Cyrus-IMAP-Server)

---

## Key Features

| Feature | Description |
|---------|-------------|
| **Multi-Protocol Support** | Supports IMAP, IMAPS, JMAP, POP3, POP3S, CalDAV, CardDAV, NNTP, and KPOP [citation:3][citation:9] |
| **Enterprise Scalability** | Designed for use from small to large enterprise environments, with Cyrus Murder providing horizontal scalability across server pools [citation:2][citation:4] |
| **Security** | Runs on sealed servers with no user login; supports X.509 PKI auth via STARTTLS and EXTERNAL [citation:4] |
| **Mailbox Management** | Supports access control lists (ACLs) on mailboxes and storage quotas on mailbox hierarchies [citation:2][citation:4] |
| **Server-Side Filtering** | Supports Sieve (RFC 5228) for powerful server-side email filtering and scripting [citation:1][citation:10] |
| **CalDAV & CardDAV** | Integrated calendaring and contacts solution, providing a full groupware experience [citation:4] |
| **Authentication** | Extensive authentication options through Cyrus SASL, including LDAP, Active Directory, Kerberos, PAM, and more [citation:4] |
| **Email Deliverability** | Supports SPF, DKIM, and DMARC for proper email delivery [citation:12] |
| **Efficiency** | Multiple concurrent read/write connections to the same mailbox are permitted [citation:2] |
| **Single Instance Store** | Stores one copy of a message when addressed to multiple recipients [citation:1] |

---

## Installation Guide

Cyrus IMAP is a Unix/Linux-native application that can be run on Windows through the **Cygwin environment** [citation:6] or **Windows Subsystem for Linux (WSL2)** [citation:5].

### Prerequisites

- Windows 10, Windows 11, or Windows Server 2022
- Administrative privileges
- Working internet connection

### Option 1: Installation via Cygwin (Recommended for Native Windows)

**Step 1:** Download the Cygwin setup file from `https://cygwin.com/install.html` [citation:6].

**Step 2:** Run the setup file and select "Install from Internet" [citation:6].

**Step 3:** Follow the instructions until you reach the "Select Packages" screen [citation:6].

**Step 4:** In the "Search" bar, type and select the following packages [citation:6]:
- `bzip2`
- `gcc-g++`
- `make`
- `openssl-devel`
- `popt-devel`
- `zlib-devel`

**Step 5:** Complete the installation process [citation:6].

**Step 6:** Download the latest Cyrus IMAP source from `https://www.cyrusimap.org/` [citation:6].

**Step 7:** Extract the source to a folder of your choice [citation:6].

**Step 8:** Open the Cygwin terminal and navigate to the extracted folder [citation:6].

**Step 9:** Build Cyrus IMAP [citation:6]:

```bash
./configure --prefix=/usr/local/cyrus
make
make install
