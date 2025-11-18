# 🛒 Urban Grocers – API Testing & Automation
API testing and automation project for the Urban Grocers REST API.  
Includes manual API validation, automated test scripts (Pytest), Postman collections, and documentation.

---

## 🚀 Scope
- API Functional Testing  
- Automation with Pytest (Python)  
- JSON response validation  
- Negative testing  
- Authentication testing  
- Bug reporting  
- Git version control  

---

## 📂 Project Structure

urban-grocers-api-testing/
│
├── README.md
├── postman/
│ └── Urban-Grocers.postman_collection.json
│
├── automation/
│ ├── test_orders.py
│ ├── test_auth.py
│ └── conftest.py
│
├── bug-reports/
│ ├── bug-001.json
│ └── bug-002.json
│
└── evidence/
├── screenshots/
└── api-logs/


---

## 🧪 Pytest Automation Example

```python
import requests

BASE_URL = "https://urban-grocers.com/api"

def test_create_order_success():
    payload = {
        "user_id": 12,
        "items": ["milk", "bread"],
        "payment_method": "card"
    }
    
    response = requests.post(f"{BASE_URL}/orders", json=payload)
    
    assert response.status_code == 201
    json_resp = response.json()
    assert "order_id" in json_resp
GET /orders/123

Expected Response:
{
  "order_id": 123,
  "status": "delivered",
  "items": ["milk", "bread"]
}
🛠 Tools Used

Postman

Pytest

Python

Git

Swagger

👩‍💻 Author

Anyelly Natalia Flórez
QA Engineer — Manual & Automation
