# HackMyVM OSINT - Challenge 006

## 📝 Challenge Information

* **Category:** OSINT / Network Reconnaissance
* **Challenge Name:** OSINT 006
* **Created by:** sml
* **Objective:** Find the hidden flag based on the hint: `hackmyvm.eu. 100 IN TXT`
<img width="1645" height="1209" alt="image" src="https://github.com/user-attachments/assets/e3b57e8d-0d91-4560-b179-a9aed5a9b575" />

---

## 🔍 Investigation Methodology

### Step 1: Analyzing the Hint
The challenge description provides a specific string: `hackmyvm.eu. 100 IN TXT`. 
In networking, `TXT` stands for a **Text DNS record**, which is often used to verify domain ownership or store arbitrary human-readable text. The number `100` represents the Time to Live (TTL) value.
<img width="1708" height="811" alt="image" src="https://github.com/user-attachments/assets/81ab281d-2c8f-4b17-b93a-f3c860392968" />

### Step 2: Querying DNS Records
Since the hint points directly to a DNS TXT record for the domain `hackmyvm.eu`, I used the standard network administration tool **`nslookup`** (or alternative tools like `dig`) to query the domain's TXT records.

I executed the following command in the terminal:
nslookup -q=txt hackmyvm.eu
