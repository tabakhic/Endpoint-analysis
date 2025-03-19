# 🕵️ Forela Forum Breach Investigation

## Task 1: Identify the External Contractor

- **Contractor Username**: `apoole1`

![Contractor Username](https://imgur.com/6eRswCW.png) 
*Ref 1: Forum logs showing the contractor's username `apoole1`*

---

## Task 2: Identifying the Contractor's IP Address

- **IP Address Used by the Contractor**: `10.10.0.78`

![Contractor's IP](https://i.imgur.com/PBU1lUq.png)
*Ref 2: Logs confirming account creation from IP `10.10.0.78`*

---

## Task 3: Identifying the Malicious Post

- **Post ID of Malicious Post**: `9`

![Malicious Post](https://imgur.com/nktWsfc.png)
*Ref 3: Forum post ID `9` made by the contractor*

---

## Task 4: Credential Stealer's Destination URL

- **Full URI Sending Stolen Data**: `http://10.10.0.78/update.php`

![Stealer URI](https://i.imgur.com/9UkPYDO.png)
*Ref 4: Network logs showing stolen data being sent to `10.10.0.78/update.php`*

---

## Task 5: Contractor's Admin Login Time

- **Login Time as Administrator (UTC)**: `26/04/2023 10:53:12`

![Admin Login](https://i.imgur.com/7gc82fN.png)
*Ref 5: Logs showing contractor's login as `administrator`*

---

## Task 6: Plaintext LDAP Password

- **LDAP Password**: `Passw0rd1`

![LDAP Password](https://i.imgur.com/uxN8CjD.png)
*Ref 6: Database logs exposing plaintext LDAP password*

---

## Task 7: Administrator User Agent

- **User Agent of Administrator**:  
  `Mozilla/5.0 (Macintosh; Intel Mac OS X 10_15_7) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/112.0.0.0 Safari/537.36`

![Admin User Agent](https://i.imgur.com/W2eHK8G.png)
*Ref 7: Logs showing admin's browser user agent*

---

## Task 8: Time Contractor Added Themselves to Admin Group

- **Admin Group Addition Time (UTC)**: `26/04/2023 10:53:51`

![Admin Privilege Escalation](https://i.imgur.com/x6nepyU.png)
*Ref 8: Logs showing contractor adding themselves to the Administrator group*

---

## Task 9: Database Backup Download Time

- **Database Backup Download Time (UTC)**: `26/04/2023 11:01:38`

![Database Download](https://i.imgur.com/fGapK7g.png)
*Ref 9: Logs confirming database backup download*

---

## Task 10: Database Backup File Size

- **Size of Database Backup (Bytes)**: `34707`

![Database File Size](https://i.imgur.com/IR5Gzpp.png)
*Ref 10: Logs showing database backup file size*

---

### **Findings and Mitigation Steps:**

- **Attack Vector**: Credential theft via a malicious forum post.
- **Persistence Mechanism**: Escalated privileges by adding themselves to the Administrator group.
- **Mitigation Steps**:
  - **Disable Guest Wi-Fi access to internal resources.**
  - **Monitor and log administrative privilege changes.**
  - **Enforce strong authentication (e.g., MFA) for forum logins.**
  - **Regularly audit database security to prevent plaintext credential storage.**
  - **Restrict external contractors' permissions to minimize security risks.**

---

🚀 **This investigation highlights the importance of monitoring guest network activity, securing administrator accounts, and regularly auditing system logs to detect malicious actions early.**
