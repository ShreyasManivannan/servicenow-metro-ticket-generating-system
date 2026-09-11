# 🚇 ServiceNow Metro Ticket Generating System

A **digital metro ticket booking and QR-based ticket generation system** developed using **ServiceNow**. This project automates the metro ticket booking process by allowing users to select stations, enter journey details, calculate fares automatically, and generate a digital ticket with a QR code.

---

## 📌 Project Overview

The **Metro Ticket Generating System** is designed to modernize and simplify the traditional metro ticket booking process using the capabilities of the **ServiceNow platform**.

Users can book metro tickets through a **Service Catalog form** by selecting their source and destination stations, entering passenger and journey details, and choosing the journey type. The system validates the information, calculates the ticket fare automatically, and generates a digital ticket with a QR code after successful submission.

The project demonstrates the use of ServiceNow's automation, scripting, catalog management, and workflow capabilities to create an efficient ticket management solution.

---

## ✨ Key Features

* 🚉 Source and destination station selection
* 🎫 Digital metro ticket booking
* 💰 Automatic fare calculation
* 👥 Passenger-based fare calculation
* 🔄 Single and return journey support
* ✅ Mandatory field validation
* 👁️ Conditional field visibility
* ⚙️ Automated field mapping and population
* 📱 QR code-based digital ticket generation
* 🔔 Automated notifications
* 📋 Ticket and request tracking
* 🔐 ServiceNow-based data and access management

---

## 🛠️ Technologies Used

| Technology                 | Purpose                                       |
| -------------------------- | --------------------------------------------- |
| **ServiceNow**             | Application development platform              |
| **Service Catalog**        | Metro ticket booking interface                |
| **Catalog Items**          | Ticket request creation                       |
| **Catalog Client Scripts** | Client-side validation and automation         |
| **UI Policies**            | Dynamic field visibility and mandatory fields |
| **Business Rules**         | Server-side business logic                    |
| **Flow Designer**          | Process automation and workflow management    |
| **Notifications**          | Automated user notifications                  |
| **JavaScript**             | Custom scripting and validations              |
| **QR Code Generation**     | Digital ticket verification                   |

---

## 🏗️ System Architecture

The application follows a structured ServiceNow-based workflow:

```text
User
  │
  ▼
Service Catalog
  │
  ▼
Metro Ticket Booking Form
  │
  ├── Source Station
  ├── Destination Station
  ├── Journey Type
  └── Passenger Details
  │
  ▼
Client-Side Validation
  │
  ▼
Fare Calculation
  │
  ▼
Order Submission
  │
  ▼
Business Rules / Flow Designer
  │
  ▼
Ticket Generation
  │
  ▼
QR Code Generation
  │
  ▼
Digital Metro Ticket
  │
  ▼
User Notification
```

---

## 🔄 System Workflow

### Step 1: Open Metro Ticket Catalog

The user accesses the **Metro Ticket Generating System** through the ServiceNow Service Catalog.

### Step 2: Enter Journey Details

The user enters the required information, including:

* Source station
* Destination station
* Journey type
* Number of passengers
* Passenger details

### Step 3: Validate User Input

Catalog Client Scripts and UI Policies validate the entered information.

The system ensures:

* All mandatory fields are completed.
* Source and destination stations are selected.
* Invalid journey information is prevented.
* Relevant fields are displayed based on user selections.

### Step 4: Calculate Fare

The system automatically calculates the ticket fare based on:

* Selected source station
* Selected destination station
* Number of passengers
* Journey type

### Step 5: Submit Ticket Request

After successful validation, the user submits the metro ticket request.

### Step 6: Process Ticket Request

ServiceNow automation processes the submitted request using:

* Business Rules
* Flow Designer
* Process Automation

### Step 7: Generate Digital Ticket

The system creates a digital metro ticket containing the journey and passenger details.

### Step 8: Generate QR Code

A QR code is generated and associated with the digital ticket for ticket verification.

### Step 9: Send Notification

The user receives an automated notification confirming the successful ticket generation.

---

## 📋 Service Catalog Form

The Metro Ticket Booking Form collects the required journey information.

### Example Fields

| Field                | Description                   |
| -------------------- | ----------------------------- |
| Passenger Name       | Name of the passenger         |
| Source Station       | Starting metro station        |
| Destination Station  | Destination metro station     |
| Journey Type         | Single or Return              |
| Number of Passengers | Total number of passengers    |
| Journey Date         | Date of travel                |
| Total Fare           | Automatically calculated fare |

---

## 💰 Fare Calculation

The system calculates the metro fare automatically based on the journey details.

### Fare Calculation Logic

```text
Total Fare = Base Fare × Number of Passengers
```

For return journeys:

```text
Total Fare = Base Fare × Number of Passengers × 2
```

The fare calculation can be extended to support:

* Distance-based fares
* Zone-based fares
* Peak-hour pricing
* Discounts
* Special passenger categories

---

## ⚙️ ServiceNow Components Used

### 📦 Service Catalog

The Service Catalog provides the user interface for booking metro tickets.

Users can submit ticket requests through a structured catalog item.

---

### 🧾 Catalog Item

A dedicated **Metro Ticket Booking** catalog item is created to collect journey and passenger information.

The catalog item contains:

* Variables
* Variable Sets
* Mandatory fields
* Reference fields
* Choice fields

---

### 💻 Catalog Client Scripts

Catalog Client Scripts are used to perform client-side operations such as:

* Validating user input
* Calculating ticket fares
* Updating field values
* Preventing invalid submissions

---

### 👁️ UI Policies

UI Policies are used to dynamically control form behavior.

Examples include:

* Showing return journey fields only when required.
* Making fields mandatory based on journey type.
* Hiding unnecessary fields.
* Controlling field accessibility.

---

### ⚙️ Business Rules

Business Rules handle server-side processing and business logic.

They can be used for:

* Processing submitted ticket requests.
* Validating request data.
* Updating ticket records.
* Triggering backend operations.

---

### 🔄 Flow Designer

Flow Designer automates the ticket generation workflow.

The flow can perform actions such as:

1. Detect a new ticket request.
2. Retrieve the submitted journey details.
3. Create a ticket record.
4. Generate a unique ticket identifier.
5. Generate a QR code.
6. Send a confirmation notification.

---

### 🔔 Notifications

ServiceNow notifications inform users about the status of their ticket.

Notifications can include:

* Ticket booking confirmation
* Ticket number
* Journey details
* Fare amount
* QR code information

---

## 📱 QR Code-Based Ticket Generation

After the ticket request is successfully processed, the system generates a digital ticket containing a unique identifier.

A QR code can be used to store or reference information such as:

* Ticket ID
* Passenger details
* Source station
* Destination station
* Journey date
* Ticket status

The QR code can be scanned during ticket verification.

---

## 🖥️ Project Screenshots

Add your project screenshots in the `screenshots` folder and update the paths below.

### Metro Ticket Booking Form

```text
screenshots/metro-ticket-booking-form.png
```

![Metro Ticket Booking Form](screenshots/metro-ticket-booking-form.png)

---

### Fare Calculation

```text
screenshots/fare-calculation.png
```

![Fare Calculation](screenshots/fare-calculation.png)

---

### Digital Ticket

```text
screenshots/digital-ticket.png
```

![Digital Ticket](screenshots/digital-ticket.png)

---

### QR Code Generation

```text
screenshots/qr-ticket.png
```

![QR Code Ticket](screenshots/qr-ticket.png)

---

## 📂 Project Structure

```text
servicenow-metro-ticket-generating-system
│
├── README.md
│
├── Documentation
│   ├── Project_Report.pdf
│   ├── Requirement_Analysis.md
│   ├── Technical_Blueprint.md
│   └── Setup_Manual.md
│
├── Screenshots
│   ├── metro-ticket-booking-form.png
│   ├── fare-calculation.png
│   ├── digital-ticket.png
│   └── qr-ticket.png
│
└── ServiceNow
    ├── Catalog_Items
    ├── Client_Scripts
    ├── UI_Policies
    ├── Business_Rules
    └── Flow_Designer
```

---

## 🚀 Installation and Setup

### Prerequisites

Before setting up the project, ensure that you have:

* Access to a ServiceNow instance.
* Administrator or developer access.
* Access to Service Catalog.
* Access to Flow Designer.

---

### Setup Steps

#### 1. Create a ServiceNow Instance

Create or use an existing ServiceNow developer instance.

#### 2. Create the Catalog Item

Navigate to:

```text
Service Catalog → Catalog Definitions → Maintain Items
```

Create a new catalog item named:

```text
Metro Ticket Booking
```

---

#### 3. Create Catalog Variables

Add the required variables, including:

* Passenger Name
* Source Station
* Destination Station
* Journey Type
* Number of Passengers
* Journey Date
* Total Fare

---

#### 4. Configure Client Scripts

Create Catalog Client Scripts to:

* Validate the selected stations.
* Calculate fares.
* Update form fields dynamically.

---

#### 5. Configure UI Policies

Create UI Policies to manage:

* Field visibility.
* Mandatory fields.
* Conditional behavior.

---

#### 6. Create Business Rules

Configure Business Rules to handle backend processing and ticket record management.

---

#### 7. Configure Flow Designer

Create a Flow Designer workflow to:

* Process ticket requests.
* Generate ticket information.
* Create digital tickets.
* Trigger notifications.

---

#### 8. Configure Notifications

Create notifications to inform users when their ticket has been successfully generated.

---

## 🔐 Security and Data Management

The project uses ServiceNow's platform capabilities to manage application data and user access.

Security considerations include:

* Role-based access control.
* Controlled access to ticket records.
* Server-side validation.
* Secure data handling.
* User authentication through ServiceNow.

---

## 🧪 Testing

The application should be tested for the following scenarios:

* ✅ Successful ticket booking
* ✅ Source and destination validation
* ✅ Mandatory field validation
* ✅ Single journey booking
* ✅ Return journey booking
* ✅ Multiple passenger booking
* ✅ Correct fare calculation
* ✅ Ticket generation
* ✅ QR code generation
* ✅ Notification delivery

---

## 📈 Future Enhancements

The system can be further extended with:

* 💳 Online payment integration
* ❌ Ticket cancellation
* 💰 Automated refund processing
* 🚆 Real-time train information
* 📱 Mobile application integration
* 📜 Ticket booking history
* 🗺️ Multiple metro-line support
* 🔔 Advanced passenger notifications
* 📍 Real-time station information
* 💵 Dynamic and distance-based fare calculation
* 🎟️ QR code scanning and verification
* 👤 Passenger profile management

---

## 🎯 Learning Outcomes

This project demonstrates practical experience with:

* ServiceNow application development
* Service Catalog configuration
* Catalog Items and Variables
* Catalog Client Scripts
* UI Policies
* Business Rules
* Flow Designer
* Process Automation
* ServiceNow Notifications
* JavaScript
* Data management
* Workflow automation

---

## 👨‍💻 Author

**Shreyas Manivannan**

ServiceNow Developer | Application Developer

GitHub: https://github.com/ShreyasManivannan

---

## 📄 License

This project is created for educational and learning purposes.

You are free to use and modify the project for learning and personal development.

---

## ⭐ Support

If you found this project useful, consider giving the repository a **star ⭐**.

Your support is appreciated!

---

### 🚇 Simplifying Metro Ticket Booking with ServiceNow Automation
