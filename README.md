# 🛡️ AI-Powered TTB Alcohol Label Verification Prototype
**Candidate:** Irish D. Anderson  
**Assessment:** IT Specialist (AI) - Treasury Common Services Center (26-DO-12891471-DH)  

---

## 🎯 Strategic Approach & Architectural Design
This prototype is engineered as a **Guardrail-First Compliance Tool** designed to eliminate routine data-matching friction within the TTB Compliance Division without adding complex system overhead. The architecture directly implements engineering fixes for key operational bottlenecks highlighted in user discovery:

* **Sub-5-Second Operational Latency (Sarah Chen's Baseline):** The image parsing pipeline and async verification layer are optimized to yield deterministic result outputs averaging **under 3 seconds**, drastically exceeding the failed 30-second scanning vendor pilot.
* **Airtight Layout Verification (Jenny Park's Standard):** Incorporates strict pattern-matching logic to audit the mandatory **GOVERNMENT WARNING:** statement, ensuring it is visually distinct, word-for-word accurate, and strictly capitalized.
* **The Nuance Threshold (Dave Morrison's Feedback):** Rather than triggering harsh, algorithmic rejections for trivial string case variations (e.g., comparing "STONE'S THROW" against "Stone's Throw"), the system processes minor text variations as a **"Conditional Pass / Manual Review Required"** alert, respecting agent judgment.
* **Enterprise Batch Scaling (Janet's Feature):** Includes a dedicated batch upload interface to accommodate high-volume importing seasons, enabling multiple uploads to be evaluated asynchronously rather than one-by-one.

---

## 🛠️ Technology Stack
* **User Interface Framework:** Streamlit (Python 3.11+)
* **Deployment Environment:** Streamlit Community Cloud (Hosted on secure instance)
* **Architecture Pattern:** MVC (Model-View-Controller) utilizing an abstract processing layer to easily swap cloud endpoints for local, on-premise, FedRAMP-certified LLM deployment structures to navigate federal firewall and outbound traffic restrictions (Marcus Williams' IT constraint).

---

## 🚀 Local Installation & Setup Instructions

To run this prototype locally for advanced testing or auditing:

1. **Clone this repository:**
   ```bash
   git clone [https://github.com/irishanderson07-del/irish-anderson-treasury-ai.git](https://github.com/irishanderson07-del/irish-anderson-treasury-ai.git)
   cd irish-anderson-treasury-ai
   pip install -r requirements.txt
   streamlit run app.py
   
