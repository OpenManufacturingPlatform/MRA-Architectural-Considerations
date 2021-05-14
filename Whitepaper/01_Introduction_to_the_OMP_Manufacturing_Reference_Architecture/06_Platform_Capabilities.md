[< Use Case Considerations for Architecture design](05_Use_Case_Considerations.md)

# Platform Capabilities 

As introduced in chapter 2.2 the platform has a functional and a
technical layer. Each Use Case is demanding different capabilities from
these layers. By cross-referencing the capabilities required,
manufacturers understand how to design the platform and the applications
on top of it both in the initial phase and in the long term.

The following capabilities should be a priority:

-   ***Data Governance:*** The orchestration of people, processes, and
    technology for democratization of data enable organizations to
    leverage their data as an enterprise-wide business asset as well as
    in cross-company data exchanges, becoming an important capability of
    a smart factory platform.

-   ***Data Integration***: Both sensor and other data captured from the
    machinery must be integrated with other data from applications such
    as ERP, MES, to form an analytical data set.

-   ***Data pre-processing:*** Data can be pre-filtered or compressed on
    the edge to avoid massive data upload from unnecessary data:
    filtering and aggregation as examples.

-   ***Data Processing & Analytics***: Data processing occurs when data
    is collected and translated into usable information. It is important
    for the success to do it correctly as not to negatively affect the
    data output. The well-defined output will then be consumed for
    analytical workloads to find relevant relationships to transform
    information into actionable insights. In some cases (near real-time
    use cases) capabilities in this pillar need to be available close to
    the shop floor.

-   ***Data Transformation:*** Data should be stored in its raw data
    format for the highest fidelity. However, to make data consumable
    and actionable, adding a) context to transform them into information
    and b) access layers for transformed and enriched data/information
    is required.

-   ***Data Accessibility***: It is critical to make data accessible in
    quality ensured and secure data pipelines to lead to informed
    decisions and actions. Data accessibility capability needs to be
    designed with the context of data ownership, data quality, data
    flexibility incl. centralized data schemas.

-   ***Data Reusability***: Data should be stored in their raw format to
    create a multi-purpose data foundation. It can be transformed as
    required by individual use cases through different zones. In
    general, a defined data schema across all factories needs to be
    applied.

    -   Although there is a strong initial preference for creating this
        data foundation on the cloud, the reference architecture must
        support those cases where cloud connectivity is not reliable or
        desirable. This could be due to sub-standard connectivity SLAs
        in a particular location, the sheer volume of data required to
        be processed for a use case, or security concerns.

    -   Ingested data, common data quality routines, and data
        preparation tasks need to be cataloged for easy use and reuse
        across several use cases ranging in complexity from AI to more
        simplistic dashboarding.

-   ***Support diverse personas***: As discussed above, the reference
    architecture will be designed to support multiple diverse personas.
    These personas have different IT backgrounds and skill levels.
    Applications could range from low-code applications using toolkits
    as well as custom-coded SQL-driven analytics, artificial
    intelligence, and machine learning for more complex use cases.

<!-- -->

-   ***Control Loop Execution***: It is anticipated that manufacturers
    will increase their digital maturity over time, so the architecture
    cannot just propose an action, it must also support a control loop
    to bypass manual interaction with machines. The reference
    architecture will broadly support three levels of maturity:

    -   Open-loop control: Analytic outputs are via a reporting tool or
        similar, and actions are taken by people.

    -   Interactive control: Analytic outputs are fed back via the edge
        to the Human-Machine-Interface (HMI) for an operator to act on.

    -   Closed-loop control: Analytic outputs directly drive a change in
        machine settings or behavior via the edge, without operator
        input.

-   ***Offline Support***: Some use cases will be rated as
    business-critical, so the application needs full offline support to
    enable production to continue if cloud links are down.

Besides the “functional” platform capabilities, the platform needs to
provide functionality to manage and control the full solution space.
Some important capabilities are:

-   ***Network and Communication***: Smart factory workloads increasing
    network requirements on the shop floor. For example, workloads with
    video streaming for safety or visual inspection use cases need a lot
    of bandwidth.

-   ***Edge Computing***: Like the network requirements, edge computing
    capabilities are required to enable "offline" scenarios as well as
    near real-time AI scenarios.

-   ***Operation Management***: In hybrid environments the importance of
    a harmonized operation management toolchain increases. Device and
    runtime management, as well as application telemetry and operations,
    should be considered from day 1.

-   ***Security and Authentication***: Depending on the scenarios,
    external access to resources might be required. For example, if you
    provide order status information, last-minute production changes, or
    sustainability data to your customers, you need to consider
    authentication capabilities for B2B or B2C scenarios in addition to
    the standard security requirements.

-   ***Front-End***: To increase the platform’s value, it should support
    not only reporting and application frameworks, but with increased
    adoption of the platform, the need for a “low-code” solution
    environment is getting more and more important for process engineers
    or other officers providing applications.

-   ***24/7 DevOps***: Whilst data scientists are implementing AI-based
    solutions, the organization needs to be prepared for a “24/7” DevOps
    organization. Besides the organizational challenges, it is important
    to provide a toolchain that supports the full lifecycle for
    applications and machine learning workloads.


[Architecture Design Principles >](07_Architecture_Design_Principles.md)