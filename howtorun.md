# How to Run the Flask Backend

## 1️⃣ Create & Activate Virtual Environment  
If you haven't created a virtual environment, run:  
Windows (PowerShell):  
```powershell
python -m venv venv
venv\Scripts\activate
```
Linux/Mac:  
```bash
python3 -m venv venv
source venv/bin/activate
```

## 2️⃣ Install Dependencies  
Ensure all required packages are installed:  
```bash
pip install -r requirements.txt
```

## 3️⃣ Set Environment Variables (Optional)  
If using Flask in development mode, set the environment variable:  
Windows (CMD):  
```cmd
set FLASK_APP=app.py
set FLASK_ENV=development
```
PowerShell:  
```powershell
$env:FLASK_APP="app.py"
$env:FLASK_ENV="development"
```
Linux/Mac:  
```bash
export FLASK_APP=app.py
export FLASK_ENV=development
```

## 4️⃣ Run the Flask Server  
```bash
python app.py
```
or using Flask CLI:  
```bash
flask run
```

## 5️⃣ Test API Endpoints  
- Create a User:  
  ```bash
  curl -X POST http://127.0.0.1:5000/users -H "Content-Type: application/json" -d '{"name": "John Doe", "email": "john@example.com"}'
  ```
- Fetch Users:  
  ```bash
  curl -X GET http://127.0.0.1:5000/users
  ```

