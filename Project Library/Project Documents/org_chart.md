graph TD
    Customer["Customer"]
    User["User"]
    Analysts["Requirements Analysts/Business Analysts"]
    Developers["Designers and Developers"]
    Testers["Testers"]
    Quality["Quality"]
    ChangeManagement["Change Management"]
    TechSupport["Tech Support"]
    ProjectManagement["Project Management"]

    Customer --> Analysts
    Customer --> User
    User --> Analysts
    Analysts --> Developers
    Developers --> Testers
    Testers --> Quality
    ChangeManagement --> Quality
    TechSupport --> ProjectManagement
    ProjectManagement --> Developers

    subgraph SCM Team
        SCMLib["SCM Librarian"]
        SCMToolsmith["SCM Toolsmith"]
        SCMManager["SCM Manager"]
    end

    subgraph CCB
        CCBLeader["CCB Leader (Chair)"]
        CCBMembers["CCB Members"]
        CCBScreener["CCB Screener"]
        CCBRecorder["CCB Recorder"]
        ImpactAnalysis["Impact Analysis Team"]
        SMEs["Subject Matter Experts"]
        UserRep["Customer/User Representative"]
        Management["Management-Level Personnel"]
    end

    SCMManager --> SCMLib
    SCMManager --> SCMToolsmith
    CCBLeader --> CCBMembers
    CCBMembers --> CCBScreener
    CCBMembers --> CCBRecorder
    ImpactAnalysis --> SMEs
    SMEs --> UserRep
    UserRep --> Management
