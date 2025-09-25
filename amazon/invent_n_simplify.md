
[[related to other LP]]
[[Headlink Banks- reuseable for for differrent LPs ]]
## Question: 
Leaders expect innovation and invention, always seeking ways to simplify processes. They stay externally aware and aren’t constrained by “not invented here” thinking  Interview Question: 

**Can you provide an example where you introduced a new, simplified approach to a complex technical problem?**

---

Here’s a **polished STAR-HR answer** you can rehearse for the  
AWS leadership principle _Invent and Simplify_—based entirely on your discussion with Charles and the Swimming Australia project.

---

### **H (Headline / Direct answer)**

“One simplified approach I introduced was an **automated buffering and upload solution** for Swimming Australia’s video-analytics platform.  
It removed manual steps, coped with patchy connectivity, and guaranteed 100 % feedback data where previously up to 50 % was lost.  
Let me walk you through the details.”

---

### **S (Situation)**

- **When/Where:** Last year, as an AWS consultant on an eight-week engagement with Swimming Australia.
    
- **Context:** Coaches used an edge-device app running ML/computer-vision models to track swimmers’ stroke rate, lap time, and other metrics.
    
- **Problem:** Many training and competition venues had unreliable or no internet. The existing pipeline tried to upload live video and metrics to the cloud. If the connection failed, staff had to manually trigger local scripts to cache and re-upload.
    
- **Business Impact:** Roughly **50 % of coaching sessions** lacked complete video/metrics, meaning missed insights and poorer feedback to athletes.
    

---

### **T (Task)**

- **Goal:** Guarantee full data capture and simplify operations so that **any coach—not just technical staff—could rely on automatic uploads**.
    
- **Challenge:** The system had been in development for over a year, including with AWS Professional Services, but connectivity gaps still caused lost data and heavy manual work.
    

---

### **A (Action)**

- **Discovery & Design:**
    
    - Analysed the failure points and used _root-cause questioning_ (“why” multiple times) to isolate bandwidth loss as the key issue.
        
    - Chose a **fallback-first design**: default to cloud upload; if bandwidth dropped, seamlessly cache on the edge device.
        
- **Technology choices (why/how):**
    
    - Used **AWS IoT Greengrass** for edge orchestration,
        
    - **Kinesis Video Streams** for resilient video ingestion, and
        
    - **MQTT** for lightweight, event-driven messaging.
        
    - Designed an **event-driven workflow** so uploads resumed automatically when connectivity returned.
        
- **Execution:**
    
    - Created and gained sign-off for the new architecture in **two weeks**, implemented and tested in the next **two weeks**—well within the eight-week engagement.
        
    - Ensured coaches needed **zero manual triggers**, reducing human error.
        

---

### **R (Result)**

- **Operational:** Achieved **100 % video and metric capture**, even at venues with no internet.
    
- **Business:**
    
    - Restored full feedback loops for **every training squad (5–10 staff per swimmer)**.
        
    - Enabled data-driven coaching decisions and continuous improvement.
        
    - Cut on-site technical intervention to near-zero, freeing specialists for higher-value work.
        
- **Recognition:** Delivered in **one-quarter of the time** earlier attempts had already consumed (2 weeks design + 2 weeks build vs. a year of previous efforts).
    

---

### **Reflection (HR piece)**

“Looking back, this project reinforced how **simplicity drives reliability**.  
By focusing on _why_ failures happened and leaning on managed AWS services instead of reinventing components, we not only solved a long-standing technical issue but also created clear business value—exactly the mindset Amazon prizes.”

---

✅ **Quick memory hook:**  
_Venue connectivity gaps → root-cause analysis → Greengrass/Kinesis/MQTT auto-buffer → 100 % feedback, 4 weeks total, year-old issue solved._

---

Use this structure to answer confidently, keeping the **headline short** and the **STAR detail crisp**, while weaving in the _how and why_ to stand out.

