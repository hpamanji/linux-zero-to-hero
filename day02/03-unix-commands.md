## 1. User and Session Management

The commands below help in viewing logged-in users, switching user accounts, managing passwords, checking user/group IDs, and reviewing historical login sessions.

### 1.1 **who**
- **Purpose**: Shows which users are currently logged in.  
- **Examples**:  
  - `who` – Displays all logged-in users.  
  - `who am i` – Shows your own session details.

### 1.2 **passwd**
- **Purpose**: Change or manage user passwords.  
- **Examples**:  
  - `passwd <user_name>` – Change the password of `<user_name>`.  
  - `passwd -l <user_name>` – Lock a user’s password.  
  - `passwd -u <user_name>` – Unlock a user’s password.  
  - `passwd -d <user_name>` – Remove a user’s password.

### 1.3 **su**
- **Purpose**: Switch user accounts.  
- **Examples**:  
  - `su - <user_name>` – Switch to `<user_name>`’s environment.  
  - If you and the user are in the same group, you can access that group’s files.

### 1.4 **id**
- **Purpose**: Shows user and group ID information.  
- **Examples**:  
  - `id` – Displays current user’s UID and GID.  
  - `id <user_name>` – Displays UID and GID for `<user_name>`.

### 1.5 **last** / **lastb**
- **Purpose**: Shows a list of last logged-in (or last bad login) sessions.  
- **Examples**:  
  - `last -n 5` – Shows the last 5 successful logins.  
  - `lastb -n 5` – Shows the last 5 bad (failed) logins.
