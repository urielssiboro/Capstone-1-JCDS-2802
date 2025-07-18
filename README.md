
# Capstone-1-JCDS-2802
## 🏋️‍♂️ FitClub Membership Management System

A terminal-based gym membership CRUD program written in Python.
Allows admins and members to manage membership & personal trainer (PT) data.

---

## Main Features
✅ Multi-role login (Admin & Member)
✅ CRUD operations on member data (Create, Read, Update, Delete)
✅ New member registration (non-member)
✅ Extend membership & PT sessions with payment simulation
✅ View membership & PT package prices

---

## System Flowchart
https://imgur.com/a/0i9z7rz

---

## Data Structure

Variable Name         | Description
--------------------- | -------------------------------------------------------
admin_id              | List of dicts containing admin usernames & passwords
data_member           | List of dicts for member data (ID, name, age, etc.)
informasi_paket       | Membership packages (name, price, duration in months)
informasi_paket_pt    | Personal trainer packages (name, price, number of sessions)

---

## Menus and Functionalities

Admin
- Login (max. 3 attempts)
- Admin Menu:
  - View member list
  - Add new member
  - Delete member
  - Back to main menu

---

## Member
- Login (id_member + first name) (max. 3 attempts)
- Member Menu:
  - Extend membership (choose package)
  - Extend PT sessions (choose package)
  - Check remaining membership & PT sessions
  - Back to main menu

---

## Non-Member
- View membership package prices
- Register as a new member
- Return to main menu

---

## Payment Simulation
- Enter the amount of money to pay.
- If the amount is sufficient → data is updated & transaction succeeds.
- If insufficient → transaction fails.
- Change is displayed if applicable.

---

## CRUD Member Data

Operation | Who Can Access      | Functions
--------- | ------------------  | -----------------------------------------------
Create    | Admin & Non-Member  | tambah_member(), daftar_member_baru()
Read      | Admin               | tunjukkan_member()
Update    | Member              | payment_member(), payment_member_pt()
Delete    | Admin               | delete_member()

---

## Validation & Security
- Unique ID check when adding a new member.
- Validate integer inputs (age, ID, payment amount).
- Max. 3 login attempts.

---

## Main File & Functions
Contains all the main functionalities:
- main_menu()
- admin_login(), menu_admin()
- member_login(), menu_member()
- non_member_menu()
- CRUD: tambah_member(), delete_member(), tunjukkan_member()
- Payment: payment_member(), payment_member_pt(), proses_pembayaran()
- Utils: input_id_unik(), tunjukkan_harga_membership(), tunjukkan_harga_pt()

---

## Notes
- Program runs in CLI (terminal).
- Data is stored in memory only; not saved permanently.
- Suitable for learning CRUD concepts, validation, and Python data structures.

---

## License
This project is created for educational purposes. Free to use & modify.
