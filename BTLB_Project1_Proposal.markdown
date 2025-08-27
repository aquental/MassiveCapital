# Case Study - Massive Capital Project 1

<div style="text-align: right">
        <i>Antonio Quental</i>
    </div>

## Approach

To create a system that identifies Texas landowners who "really want to sell" or "really need to sell," I propose an AI-driven data consolidation and marketing platform for Big Texas Land Buyers (BTLB). The solution leverages data sources (County Data, Cell Phone/Email, Demographics, and Meta Data) to build a robust database and employs AI/ML to prioritize high-intent sellers. The approach includes:

1. **Data Integration and Enrichment**:

   - Aggregate state-level property data to identify landowners across Texas (targeting 2-3 million).
   - Enrich with demographic data (e.g., age, income, financial status) to assess seller motivation.
   - Use Verism Meta Data to validate contact information (cell phone, email) and add behavioral insights (e.g., recent property searches or financial distress signals).
   - Store and process data in a centralized cloud-based database for scalability.

2. **AI-Driven Seller Scoring**:

   - Develop an AI/ML model to score landowners based on likelihood to sell, using features like property size, tax delinquency, financial demographics, and behavioral signals.
   - Train the model with historical sales data and enriched demographics to identify patterns of "want to sell" (e.g., owners listing properties online) and "need to sell" (e.g., owners with liens or financial distress).
   - Continuously refine the model with feedback from outreach campaigns.

3. **Agentic Automation**:

   - Deploy AI agents (Calling, Texting, Email) via Twilio and Vapi.ai to execute personalized outreach at scale.
   - Implement a Follow-up Coaching Agent to guide acquisition managers with insights on high-priority leads.
   - Use a Performance Agent to monitor campaign metrics (e.g., response rates, conversions) and optimize outreach strategies.
   - Employ a Data Management Agent to ensure data quality, compliance, and real-time updates.

4. **Human-AI Collaboration**:
   - Enable the Acquisition Team to focus on high-scoring leads identified by AI, streamlining negotiations.
   - Provide an intuitive dashboard for the Acquisition Manager to oversee AI agent performance and prioritize leads.
   - Train the Ad/SEO Manager to leverage insights from the Performance Agent for targeted digital campaigns.

This approach ensures BTLB efficiently targets motivated sellers, maximizes outreach impact, and scales operations with minimal staff (4 employees).

## Tech Stack

- **Cloud Provider**: AWS
  - **Amazon Aurora RDS**: For relational database management of property and demographic data.
  - **Amazon S3**: For storing raw and enriched data sets.
  - **Amazon SageMaker**: For building, training, and deploying the AI seller scoring model.
  - **AWS Lambda**: For serverless execution of AI agent tasks (e.g., triggering outreach).
  - **Amazon API Gateway**: To manage integrations with Twilio and Vapi.ai.
- **Communication Platforms**:
  - **Twilio**: For texting and email outreach.
  - **Vapi.ai**: For automated calling.
- **Data Enrichment**:
  - **Third-Party APIs**: Integrate with Verism for metadata and demographic providers for enriched insights.
- **Frontend**:
  - **React with Tailwind CSS**: For a responsive dashboard to manage leads and monitor AI agent performance.
- **Compliance and Security**:
  - **AWS IAM and Cognito**: For secure access control and user authentication.
  - **TCPA Compliance Tools**: To ensure legal adherence in automated outreach (TCPA: Telephone Consumer Protection Act).
- **Startup Grants**:
  - Apply for **AWS Activate Portfolio** to receive up to $100,000 in credits for startups, covering compute, storage, and AI services.
  - Explore **Texas Enterprise Fund** for technology-driven real estate initiatives, emphasizing job creation and innovation.

## Team

### Estimated Team

To execute the project efficiently with a lean team of 4 employees, supplemented by contract roles, the following structure is proposed:

- **Acquisition Manager (Full-Time)**: Oversees deal negotiations, prioritizes AI-generated leads, and closes transactions.
- **AI Agents Manager (Full-Time)**: Manages AI agent performance, oversees integrations (Twilio, Vapi.ai), and ensures system reliability.
- **Ad/SEO Manager (Full-Time)**: Runs digital marketing campaigns, optimizes SEO, and leverages Performance Agent insights for targeted ads.
- **Administrative Support (Full-Time)**: Handles compliance (e.g., TCPA), data privacy, and general operations support.
- **Contract Roles**:
  - **Data Analyst (3-Month Contract)**: Assists with initial data integration, enrichment, and AI model training.
  - **DevOps Engineer (2-Month Contract)**: Sets up AWS infrastructure (RDS, S3, Lambda, API Gateway).
  - **Frontend Developer (2-Month Contract)**: Builds the React-based dashboard with Tailwind CSS.

### Strategies to Compress Timeline

To accelerate the Timeline from 8 months to approximately 6 months, I propose:

1. **Parallel Task Execution**:
   - Run data collection and AWS infrastructure setup concurrently, leveraging pre-built AWS templates to reduce setup time.
   - Overlap AI model development with dashboard development by using pre-trained models in SageMaker, fine-tuned with BTLB data.
2. **Pre-Built Tools**:
   - Use Twilio's pre-configured APIs for texting/email and Vapi.ai's out-of-the-box call automation to cut integration time by 2 weeks.
   - Adopt open-source React dashboard templates to reduce frontend development time by 50%.
3. **Outsourcing and Automation**:
   - Hire contract DevOps and frontend developers to expedite infrastructure and UI tasks, freeing the core team to focus on strategy and testing.
   - Automate data validation using Data Management Agent scripts to reduce manual effort in the enrichment phase.
4. **Early Pilot Testing**:
   - Launch a smaller pilot in early 2026 during AI agent deployment to gather early feedback, allowing optimization before the full pilot in March 2026.
5. **Grant Acceleration**:
   - Fast-track AWS Activate Portfolio application in August 2025 to secure credits early, enabling immediate infrastructure scaling.

These strategies compress the Timeline by approximately 2 months, targeting a full launch by March 1, 2026.

We should refine the plan! This plan was based solely on a slide deck; more information leads to a better plan.

## Timeline

```mermaid
gantt
 title Project 1 Timeline (Compressed)
 dateFormat  YYYY-MM-DD
 axisFormat  %m/%Y

 section Data
 Data Collection & Integration :active, 2025-09-01, 2025-10-01
 Data Enrichment & Validation  :active, 2025-10-02, 2025-11-01

 section Infrastructure
 AWS Setup (RDS, S3, Lambda)  :active, 2025-09-01, 2025-10-01
 API Integrations (Twilio, Vapi.ai) :active, 2025-10-02, 2025-10-31

 section AI and Automation
 AI Model Development (SageMaker) :active, 2025-10-15, 2025-12-15
 Agent Deployment (Calling, Texting, Email) :active, 2025-12-16, 2026-01-31
 Dashboard Development (React) :active, 2025-12-01, 2026-01-15

 section Admin
 Team Training & Testing :active, 2026-01-16, 2026-02-15
 Pilot Launch & Optimization :active, 2026-02-16, 2026-02-28
 Full Launch :milestone, 2026-03-01
```

> [!WARNING]
> This is a high-level estimate and subject to change after a more thorough discovery phase.

## Go to Market

### Strategy

1. **Pilot Phase** (early 2026):
   - Launch in 2-3 high-priority Texas counties identified from county data analysis.
   - Test AI-driven outreach (texts, calls, emails) on a subset of landowners initially, scaling by late February.
   - Use Performance Agent to measure response rates and refine messaging.
2. **Digital Marketing**:
   - Leverage the Ad/SEO Manager to run targeted Google Ads and social media campaigns (e.g., Facebook, X) emphasizing BTLB's motto: "Transform Your Vacant Land into Cash Today!"
   - Optimize SEO for keywords like "sell land fast Texas" and "Houston commercial land buyers."
3. **Full Launch** (March 2026):
   - Scale outreach to 500,000 landowners across target counties.
   - Use AI insights to personalize offers, increasing conversion rates.
   - Promote success stories from the pilot phase to build trust.
4. **Partnerships**:
   - Collaborate with local real estate agents and title companies to source leads and streamline transactions.
   - Partner with demographic data providers for continuous enrichment.

### Resources Needed

- **Personnel**:
  - Acquisition Manager: Oversees deals and lead prioritization.
  - Integration Manager: Manages AI agent performance and integrations.
  - Ad/SEO Manager: Runs digital campaigns and optimizes visibility.
  - Administrative Support: Handles compliance and operations.
  - Data Analyst (Contract): Supports initial data integration and model training.
  - DevOps Engineer (Contract): Sets up AWS infrastructure.
  - Frontend Developer (Contract): Builds React dashboard.
- **Technology**:
  - AWS infrastructure (RDS, S3, SageMaker, Lambda, API Gateway).
  - Twilio and Vapi.ai subscriptions for communication.
  - React-based dashboard for team use.
- **Budget**:
  - AWS credits via Activate Portfolio (target $50,000-$100,000).
  - Marketing budget: $50,000 for pilot phase ads (Google, X, Facebook).
  - Data enrichment subscriptions: $20,000/year for Verism and demographic APIs.
- **Compliance**:
  - Legal consultation for TCPA compliance in automated outreach.
  - Data privacy training for employees to handle sensitive landowner information.

This strategy positions BTLB to efficiently acquire $10 million in land annually by targeting motivated sellers with precision and scaling outreach effectively.
