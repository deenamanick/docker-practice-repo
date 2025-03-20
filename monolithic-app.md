
---

## **✅ Step 1: Install Dependencies**
Make sure you have **Node.js** and **MySQL** installed:  

### **1️⃣ Install Node.js (Skip if already installed)**
Check your Node.js version:
```bash
node -v
npm -v
```
If missing, install it:
```bash
sudo apt update && sudo apt install -y nodejs npm
```
For macOS:
```bash
brew install node
```

### **2️⃣ Install MySQL (Skip if already installed)**
Check MySQL version:
```bash
mysql --version
```
If missing, install it:
```bash
sudo apt install mysql-server
```
Start MySQL:
```bash
sudo systemctl start mysql
```
---

## **✅ Step 2: Set Up the MySQL Database**
1. Log in to MySQL:
   ```bash
   mysql -u root -p
   ```
2. Run these SQL commands:
   ```sql
   CREATE DATABASE restaurant_db;
   USE restaurant_db;

   CREATE TABLE restaurants (
     id INT AUTO_INCREMENT PRIMARY KEY,
     name VARCHAR(100),
     location VARCHAR(100),
     cuisine VARCHAR(50)
   );
   ```
3. Exit MySQL:
   ```sql
   EXIT;
   ```

---

## **✅ Step 3: Configure Environment Variables**
Create a **`.env`** file in your project folder:
```env
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=your_mysql_password
DB_NAME=restaurant_db
PORT=3000
```

---

## **✅ Step 4: Install Node.js Dependencies**
Navigate to your project folder:
```bash
cd /path/to/restaurant-app
```
Run:
```bash
npm install
```

---

## **✅ Step 5: Start the Server**
Run:
```bash
npm start
```
Expected output:
```
✅ Server running on http://localhost:3000
✅ MySQL Connected...
```

---

## **✅ Step 6: Test the App**
### **1️⃣ Load Restaurants in Browser**
Open:
```
http://localhost:3000/index.html
```

### **2️⃣ Test API Endpoints**
Run:
```bash
curl -X GET http://localhost:3000/restaurants
```
or use **Postman**.

---
