# 📥 Email Order Extraction to SharePoint using Power Automate

## 🔍 Overview

This project shows how to automate the process of **extracting structured order data from emails** and storing it in a **SharePoint list** using **Microsoft Power Automate**. It’s designed for businesses that receive standardized order details via email and need to centralize that data efficiently.

### ✅ Benefits
- Eliminates manual data entry
- Ensures data consistency and accuracy
- Streamlines order processing
- Centralizes order data for reporting and tracking

---

## 📌 Real-World Scenario

In this case, **vendors send order confirmations via structured emails** in a fixed format. Since replacing the email process with Microsoft Forms wasn't viable (due to external user limitations), I implemented an automated solution using Power Automate to parse the email and log the data in SharePoint.

---

## ✉️ Sample Email Format

The incoming email body follows a consistent layout:

<p align="center">
  <img src="https://github.com/Hareendranatha/Email-Content-Extraction-Automate/blob/main/Screenshots%20of%20flow%20and%20other/Email.jpg" width="600" />
</p>


---

## ⚙️ Flow Logic

The Power Automate flow consists of the following key steps:

1. **Trigger – When a New Email Arrives (V3)**  
   Monitors a mailbox for incoming vendor emails.

   <p align="left">
  <img src="https://github.com/Hareendranatha/Email-Content-Extraction-Automate/blob/main/Screenshots%20of%20flow%20and%20other/01_When%20a%20new%20email%20arrives%20(V3).JPG" width="600" />
</p>


2. **Action – HTML to Text**  
   Converts the HTML email body into plain text for easier parsing.

   <p align="left">
  <img src="https://github.com/Hareendranatha/Email-Content-Extraction-Automate/blob/main/Screenshots%20of%20flow%20and%20other/02_Html%20to%20text.JPG" width="600" />
</p>

3. **Action – Find Text Position**  
   Searches for the location of each field label (e.g., "Order Number:", "Product Name:").

   <p align="left">
  <img src="https://github.com/Hareendranatha/Email-Content-Extraction-Automate/blob/main/Screenshots%20of%20flow%20and%20other/03_Find%20text%20position.JPG" width="600" />
</p>


4. **Action – Substring**  
   Extracts the value after each field label using string manipulation.

   <p align="left">
  <img src="https://github.com/Hareendranatha/Email-Content-Extraction-Automate/blob/main/Screenshots%20of%20flow%20and%20other/04_Substring_Starting%20Position.JPG" width="600" />
</p>
   <p align="left">
  <img src="https://github.com/Hareendranatha/Email-Content-Extraction-Automate/blob/main/Screenshots%20of%20flow%20and%20other/05_Substring_Length.JPG" width="600" />
</p>

5. **Action – Create Item in SharePoint**  
   Adds the extracted order data into a SharePoint list with corresponding columns:
   - Order Number
   - Order Status
   - Vendor ID
   - Product ID
   - Product Name
   - Category
   - Size
   - Color
   - Material
   - Quantity
   - Unit Price
   - Subtotal
   - Discount
   - Shipping Costs
   - Total Price
   - Order Date
   - Expected Delivery Date
   - Delivery Address

   <p align="left">
  <img src="https://github.com/Hareendranatha/Email-Content-Extraction-Automate/blob/main/Screenshots%20of%20flow%20and%20other/06_Sharepoint%20Create%20item.JPG" width="600" />
</p>

---

## 🧠 What I Learned

> This project strengthened my ability to:
> - Build structured data extractors in Power Automate  
> - Parse long email bodies using string functions  
> - Integrate automation with SharePoint  
> - Deliver no-code solutions under real-world constraints

---

## 🔄 Future Enhancements

- ✅ Add AI Builder to parse PDF/Word attachments  
- ✅ Include validation or approval flows before entry  
- ✅ Send confirmation or success email after logging order  
- ❇️ Add logging or error handling for extraction failures


---

## 🧰 Tools & Technologies

- Power Automate (Cloud Flows)  
- Microsoft SharePoint  
- Microsoft Outlook (V3 Trigger)  
- Text-based data extraction  
- Low-code/no-code design  

---

## 🤝 Connect With Me

Interested in improvements or collaboration?


Connect on : [LinkedIn](https://www.linkedin.com/in/hareendra-muthukumarana-b8609b22b/)


---




