# Zen Class MongoDB Project

## 📌 Project Description
This project demonstrates the use of **MongoDB** to manage a Zen Class program database.  
The database contains collections for:

- **Users** – Student details  
- **Topics** – Topics taught in the class  
- **Tasks** – Tasks assigned for each topic  
- **Mentors** – Mentors and their mentee count  
- **Company Drives** – Placement drives with appeared students  
- **Codekata** – Number of problems solved by users  
- **Attendance** – Attendance status of users  

The data has been **created and stored in MongoDB Compass**.

---

## 🗄 Database Collections

| Collection Name   | Description |

| Users            | Student details (`_id`, `name`, `email`) |
| Topics           | Topics taught (`_id`, `topic_name`, `date`, `description`) |
| Tasks            | Tasks assigned (`_id`, `task_name`, `topic_name`, `date`, `submitted_by`, `not_submitted_by`) |
| Mentors          | Mentors (`_id`, `name`, `email`, `mentee_count`) |
| Company Drives   | Placement drives (`_id`, `company_name`, `drive_date`, `appeared_students`) |
| Codekata         | Problems solved by users (`_id`, `user_id`, `problems_solved`) |
| Attendance       | Attendance (`_id`, `user_id`, `date`, `status`) |

---

## 🔹 Queries

All queries used in this project are also uploaded in the `queries.txt` file.

### 1️⃣ Find all topics and tasks taught in October
```js
db.topics.find({ date: { $gte: ISODate("2020-10-01"), $lte: ISODate("2020-10-31") } });
db.tasks.find({ date: { $gte: ISODate("2020-10-01"), $lte: ISODate("2020-10-31") } });
