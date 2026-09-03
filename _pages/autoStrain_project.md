graph TD
    A[Input: DICOM Cine Loops<br/>A4C, A2C, A3C] --> B[AI Cardiac View Detection]
    B --> C[AI Chamber/Myocardium Segmentation]
    C --> D{User Approval}
    D -- "Reject" --> C
    D -- "Approve" --> E[AI Speckle Tracking Pipeline]
    E --> F[Automated Quantification<br/>GLS, Strain-Rate, EF]
    F --> G[Visualization: Bullseye & Volumetrics]
    G --> H[Clinical Report Generation]

    style A fill:#f9f9f9,stroke:#333
    style H fill:#d4edda,stroke:#28a745
    style E fill:#fff3cd,stroke:#ffc107

