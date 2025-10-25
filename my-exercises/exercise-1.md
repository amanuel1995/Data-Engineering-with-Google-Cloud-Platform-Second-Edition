# My GCP Data Engineering Exercises

This collection of case studies and their solutions is a place where I solve exercises from Adi Wijaya's [Data Engineering with Google Cloud Platform](https://www.packtpub.com/product/data-engineering-with-google-cloud-platform/97818). Each case presents a data problem and I try to iteratively solve it by applying what I learned in my workplace building data platforms and solving common data engineering challenges using Google Cloud Platform.

---

### Exercise 1: Dashboard to Show Book Sales Revenue and Customer Satisfaction


*   **Objective**: Your hypothetical manager asks you to enable the BI team in a hypothetical book publishing company to build a dashboard for revenue and customer satisfaction from existing datasets (Terabytes of data) in disperate sources. Assume the company doesn't have any data infrastructure yet.

*   **Data Sources**:
    *   `Company website`
    *   `MongoDB database`: That stores data from book sales app that stores transactions, book IDs, and author IDs.
    * `MySQL database`:  That stores Authors’ personal information, including age to power an Author Portal.

*   **Activities**:
    1. List down important follow-up questions for your manager
    2. List down your technical thinking process of how to do it at a high level.
    3. Draw a data pipeline architecture.

*   **Follow-up questions to the manager**:
    * How would you like to measure customer satisfaction i.e is it customer star rating? is it sentiment analysis from the free-form reviews? Where do we find this data - would it be on the company website or other third-party site like amazon.com? Do you measure customer satisfaction about the books themselves or the process of purchasing the books or the authors who write the books? Can we break down major areas of customer satisfaction evaluation (website navigation experience, book browsing/selection experience, cart and purchasing experience, customer service pre/post-sales etc.) Do we have automated feedback/review request on the website? where is the data stored, what questions are asked and how can customers answer them?
    * What is the source of truth for total revenue? Is it the overall sum of all sales transactions in MongoDB? Are books sold in brick & mortar stores like Barnes & Nobles or exclusively sold online? If we have in-store sales, are they also in MongoDB or in a different database? Or through manually scanned receipts, exported CSVs etc.?
    * How do we handle returns - do we handle that and update the transactions database or there's a separate database tracking returns?

*   **Additional questions for a robust architecture**: This set of questions were the ones I had missed and suggested by a friend. 
    *   **Data Volume & Velocity**: What is the expected data volume (e.g., GB/day) and velocity (e.g., real-time vs. batch)? How much historical data do we need to ingest?
    *   **Performance & Latency**: What is the required data freshness for the dashboard (e.g., daily, hourly, near real-time)? What are the performance expectations for dashboard queries?
    *   **Security & Compliance**: Are there any PII or sensitive data that require masking or special handling (e.g., for GDPR/CCPA)? Who needs access to what level of data (raw vs. aggregated)?
    *   **Scalability & Future Use**: Are there other data sources or use cases (like machine learning) planned for the future? What is the budget for this project?

*   **My Technical Thinking Process**:
    * The technical solution depends on the business process owner's answers. I will ask my friend to assume he's the manager of this fictitious company and update this section in the next PR.

*   **Draw a Data Pipeline Architecture**:
    *   placeholder 
---