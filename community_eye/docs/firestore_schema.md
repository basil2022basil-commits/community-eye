# CommunityEye Firestore Schema

## Collections

### 1. departments
Stores all government departments.

Fields:
- name (string)
- email (string)
- phone (string)
- isActive (boolean)

Example Documents:
- roads
- police
- health
- water
- electricity
- education
- environment

---

### 2. categories
Stores complaint categories.

Fields:
- name (string)
- departmentId (string)
- priority (string)
- isActive (boolean)

Examples:
- bad_roads
- flooding
- illegal_dumping
- water_outage
- electricity_outage
- school_repairs
- suspicious_gangs
- fighting
- kidnapping_attempt
- vandalism
- corruption

---

### 3. users

Fields:
- fullName (string)
- email (string)
- phone (string)
- role (string)
- departmentId (string)
- isActive (boolean)
- createdAt (timestamp)

Roles:
- admin
- agent
- citizen

---

### 4. complaints

Fields:
- title (string)
- description (string)
- citizenId (string)
- categoryId (string)
- departmentId (string)
- status (string)
- priority (string)
- latitude (number)
- longitude (number)
- mediaUrls (array)
- isAnonymous (boolean)
- createdAt (timestamp)
- updatedAt (timestamp)

Status values:
- Pending
- In Progress
- Resolved