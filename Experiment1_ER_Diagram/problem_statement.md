# Experiment 1: Entity-Relationship (ER) Diagram

## 🎯 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Choose One Scenario:

### 🔹 Scenario 1: University Database
Design a database to manage students, instructors, programs, courses, and student enrollments. Include prerequisites for courses.

**User Requirements:**
- Academic programs grouped under departments.
- Students have admission number, name, DOB, contact info.
- Instructors with staff number, contact info, etc.
- Courses have number, name, credits.
- Track course enrollments by students and enrollment date.
- Add support for prerequisites (some courses require others).

---

### 🔹 Scenario 2: Hospital Database
Design a database for patient management, appointments, medical records, and billing.

**User Requirements:**
- Patient details including contact and insurance.
- Doctors and their departments, contact info, specialization.
- Appointments with reason, time, patient-doctor link.
- Medical records with treatments, diagnosis, test results.
- Billing and payment details for each appointment.

---

## 📝 Tasks:
1. Identify entities, relationships, and attributes.
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).
3. Include:
   - Cardinality & participation constraints
   - Prerequisites for University OR Billing for Hospital
4. Explain:
   - Why you chose the entities and relationships.
   - How you modeled prerequisites or billing.

# ER Diagram Submission - Student Name

## Scenario Chosen:
Hospital 

## ER Diagram:
![ER Diagram](./DBMS%20Hospital%20Database.png)

## Entities and Attributes:
Medical Record: Diagnoses, Medication, Treatments, Test Result

Hospital: Name, Address, Hospital ID, Contact No, Email ID

Department: Department ID, Department Name, Department Head

Doctor: Doctor ID, Full Name, Specialization, Email ID, Phone No

Patient: Patient ID, Full Name, Date Of Birth, Gender, Phone No, Address, Email ID, Age

Appointment: Appointment ID, Appointment Date, Appointment Time, Appointment Reason


## Relationships and Constraints:
Medical Record - Hospital (Maintain Electronic Record): One-to-One, Mandatory

Hospital - Department (Consist): One-to-Many, Mandatory

Hospital - Patient (Manage Information): One-to-Many, Mandatory

Department - Doctor (Employee): One-to-Many, Mandatory

Doctor - Work Schedule: One-to-One, Mandatory

Doctor - Medical Consultation: One-to-Many, Mandatory

Patient - Appointment (Schedule): One-to-Many, Mandatory

Appointment - Medical Consultation: One-to-One, Mandatory

## Extension (Billing):
Billing are not explicitly modeled in the provided diagram. However, these could be integrated by adding a Billing entity with attributes such as Billing ID, Amount, and Payment Method. This entity would be linked to Patient and Appointment to capture relevant transactions.

## Design Choices:
* The entities were chosen based on common elements found in a hospital management system, ensuring comprehensive data management.

* The relationships reflect real-world interactions, ensuring mandatory participation where necessary to maintain integrity.

* Assumptions include that each hospital manages its own records, departments, doctors, and patients, and that appointments are scheduled and linked to consultations.
## RESULT
The image represents a hospital management system with structured entities and relationships, ensuring efficient handling of medical records, scheduling, and consultations. This model ensures proper data flow and integrity within the system.
