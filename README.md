# MySQL Workbench — Create a New Connection

## 1. Log in as Root

Open MySQL Workbench and connect using the existing **root** connection.

Open a new SQL Editor and run:

```sql
CREATE USER 'DM'@'localhost' IDENTIFIED BY 'password';

GRANT ALL PRIVILEGES ON *.* TO 'DM'@'localhost';

FLUSH PRIVILEGES;
```

### Verify the user

```sql
SELECT User, Host FROM mysql.user;
```

Expected result should include:

```text
root    localhost
DM      localhost
```

---

## 2. Create a New Workbench Connection

On the MySQL Workbench home screen, click **+** next to **MySQL Connections**.

Enter:

| Field | Value |
|---|---|
| Connection Name | `Practice` |
| Connection Method | `Standard (TCP/IP)` |
| Hostname | `localhost` |
| Port | `3306` |
| Username | `DM` |
| Password | `password` |

For the password, click **Store in Vault...** and enter:

```text
password
```

Then click **Test Connection**.

You should see:

> Successfully made the MySQL connection

Click **OK** and then double-click the new **Practice** connection.

---

## 3. Connection Details

```text
Connection Name: Practice
Username:        DM
Password:        password
Hostname:        localhost
Port:            3306
```

## Important

Keep the **root connection**. Do not delete it yet.

The `Practice` connection name is only a label in MySQL Workbench. It does not have to match the MySQL username.

The MySQL user is:

```text
DM
```

and the password is:

```text
password
```
