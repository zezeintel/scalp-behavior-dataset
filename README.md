# 📊 Scalp Behavior Dataset Framework

> Multivariate Dataset linking Scalp Health Metrics with Behavioral & Lifestyle Factors
> > **ZEZE Intelligence** | TTE Elephant Research Division
> >
> > ---
> >
> > ## 1. Problem Statement
> >
> > Scalp conditions are rarely studied in conjunction with behavioral and lifestyle variables. Existing clinical datasets focus only on physical symptoms, missing the broader context of how **stress, sleep quality, diet, and daily habits** influence scalp health over time.
> >
> > This dataset framework was designed to bridge this gap — enabling researchers to study the **correlation between behavioral patterns and measurable scalp outcomes** across a real-world population sample in Malaysia.
> >
> > ---
> >
> > ## 2. Methodology
> >
> > Data is collected through a **dual-stream pipeline**:
> >
> > **Stream A — Scalp Metrics (Objective)**
> > - Computer vision scan output (via `ai-scalp-analysis` system)
> > - - Variables: follicle density score, oil level index, sensitivity rating
> >  
> >   - **Stream B — Behavioral Survey (Self-Reported)**
> >   - - Digital survey administered via ZEZE app / TTE Elephant platform
> >     - - Variables: stress score (PSS-10 adapted), sleep hours, sleep quality, dietary pattern, water intake, exercise frequency
> >      
> >       - **Data Schema (simplified):**
> >       - ```json
> >         {
> >           "participant_id": "ZZ-00142",
> >           "date": "2025-09-14",
> >           "scalp_metrics": {
> >             "follicle_density": 84,
> >             "oil_index": 0.68,
> >             "sensitivity_score": 0.42
> >           },
> >           "behavioral": {
> >             "stress_score": 22,
> >             "sleep_hours": 5.5,
> >             "sleep_quality": "poor",
> >             "diet_type": "high_processed",
> >             "water_intake_L": 1.2,
> >             "exercise_days_per_week": 1
> >           }
> >         }
> >         ```
> >
> > ---
> >
> > ## 3. Sample Output
> >
> > **Anonymized example records (5 participants):**
> >
> > | ID | Follicle Density | Oil Index | Stress Score | Sleep (hrs) | Sleep Quality |
> > |----|-----------------|-----------|--------------|-------------|---------------|
> > | ZZ-001 | 91 | 0.41 | 12 | 7.5 | good |
> > | ZZ-002 | 76 | 0.79 | 28 | 5.0 | poor |
> > | ZZ-003 | 88 | 0.55 | 18 | 6.5 | fair |
> > | ZZ-004 | 63 | 0.91 | 35 | 4.0 | poor |
> > | ZZ-005 | 94 | 0.38 | 9  | 8.0 | good |
> >
> > *Pattern observed: higher stress + poor sleep correlates with elevated oil index and lower follicle density.*
> >
> > ---
> >
> > ## 4. Research Relevance
> >
> > This dataset directly supports hypothesis testing around the **stress-scalp feedback loop** — a research area with limited published data in Southeast Asian populations.
> >
> > Key academic applications:
> > - Training supervised ML models to predict scalp condition from behavioral inputs
> > - - Longitudinal cohort study (baseline + 3-month + 6-month tracking)
> >   - - Basis for university collaboration on behavioral health + dermatology intersection
> >    
> >     - **Planned dataset size:** 500+ participants (ongoing collection via TTE Elephant)
> >     - **Ethics:** Data is anonymized and collected with informed consent via ZEZE app
> >    
> >     - ---
> >
> > ## Repository Structure
> >
> > ```
> > scalp-behavior-dataset/
> > ├── schema/           # JSON + CSV data schema definitions
> > ├── examples/         # Anonymized sample records (50 participants)
> > ├── surveys/          # Survey instrument design (stress, sleep, diet)
> > ├── codebook/         # Variable definitions & encoding guide
> > └── README.md
> > ```
> >
> > ---
> >
> > *Built by ZEZE Intelligence | TTE Elephant Research Division*
