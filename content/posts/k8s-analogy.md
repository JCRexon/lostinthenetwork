+++  
title = "Kubernetes School Analogy"  
date = 2026-06-15T14:35:17+06:00  
draft = false  
+++  
## Alternative ELI5 Approach for Kubernetes Architectures  
As of late I have been studying for the Certified Kubernetes Administrator (CKA) certification. I've been using the excellent KodeKloud CKA course (see below for links\!) and I found their ship analogy to be a strong way to simplify the Kubernetes architecture & components. I was considering the analogy last week and questioned if there's an alternative analogy that would be accessible to individuals that don't have a clear conceptual understanding of ships.

My son is 3.5 years old and is often interested in what I am doing. He does not have a strong conceptual understanding of ships or boats. He does have an understanding of schools and how they function (albeit currently limited to his kindergarten environment). I appreciate we are 1.5 years early, but it gives me time to finesse things :)

## ELI5 - Kubernetes School  
When we consider the Kubernetes architecture & components, I believe we can map this neatly to a school environment. Admittedly, some of the analogous components are a reach but in the round the overarching analogy is fairly solid.

This post will set out the cast of the analogy and subsequent posts will dive into each concept in greater detail. For now, the cast of the analogy…

| School | Kubernetes | Reasoning |
| ----- | ----- | ----- |
| Student | **Container** | A running doer/learner. The student occupies a seat, expends mental & physical resources (CPU/mem), can misbehave and be sent out (crash → restart), crucially a student is *placed* into a room, does not own it. |
| Desk | **Pod** | A desk usually maps to one Student. Sometimes the desk may be provided to a student + a dedicated one-to-one aide, both sharing the same desk and notes. The *desk* is the unit that gets *placed*. |
| Classroom | **Node** | The Classroom has finite seats and hosts many desks at once. Classrooms can be closed for redecorating (cordon/drain). A classroom can also be torn down which also takes down the desks within it. |
| Room caretaker | **kubelet** | Sets up each desk in the classroom and reports the status, "classroom is fine, lesson is running", back to the front office. One per classroom. |
| Timetabler | **Scheduler** | Assigns students to classrooms by their fit (free seats) and by room requirements (lab, gym). |
| Head Office | **You** (`kubectl apply`) | Authors the school syllabus — the **desired state**. |
| Register | **etcd** | One book, two columns: syllabus (desired) and progress (observed). |
| Teachers | **Controllers** | Teachers compare the current syllabus against current progress, Teachers work toward the goal of completing the syllabus and reporting back current state. Teachers are key in the reconciliation of current vs. target state via Front Office. |
| Front Office | **API server** | The *only* thing allowed to write to the Register. Everyone that wants to read/write must use the Front Office. |
| Administration | **Control plane** | Head Office + Front Office + Timetabler + Teachers. *Not* "the whole school" — the school includes the students. |

## Looking Forward
Next post will be breaking down the Student <> Container analogy and looking at how the considerations for Containers knit up with considerations for Students.

*Links*
* https://kodekloud.com/
* https://kodekloud.com/learning-path/cka
* https://learn.kodekloud.com/user/courses/cka-certification-course-certified-kubernetes-administrator
