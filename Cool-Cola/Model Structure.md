# 💡 Data Model Structure Overview

This Power BI data model was intentionally designed using **two fact tables** — `Sales Results` and `Consumer Survey` — to reflect two distinct data domains with **different levels of granularity and refresh cycles**:

- `Sales Results`: Daily transactional sales data  
- `Consumer Survey`: Monthly aggregated survey data

Rather than forcing a classic star schema, this hybrid model supports **flexibility, clarity, and performance** by treating these two sources separately, while still allowing high-level comparison through shared dimension tables.

## 🧩 Key Benefits of This Structure:
- ✅ Clear separation of logic between sales and survey data  
- ✅ Better performance and scalability by avoiding unnecessary joins  
- ✅ Easier maintenance with independent data refresh logic  
- ✅ Simplified user experience with unified slicers and visuals

This design ensures that the **final report remains intuitive and efficient**, especially when combining demographic insights with product performance, all within a single unified dashboard.

<img width="1240" height="740" alt="image" src="https://github.com/user-attachments/assets/b8314276-fa3e-41ba-b1aa-fe30685302bc" />

## ⭐ Why a Many-to-Many Relationship?

A many-to-many relationship between the two fact tables (via the `Country` dimension) allows both datasets to be **filtered simultaneously** based on the selected country — without duplicating or denormalizing dimension tables.


---

### [⬅️ Back to PowerBI-Portfolio home page](https://github.com/oskarmarciniak/PowerBI-Portfolio)
