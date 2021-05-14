[< Platform Capabilities](./06_Platform_Capabilities.md)

# Architecture Design Principles 

Successfully creating a reference architecture that is actionable by a
large community of implementors requires a modular, extensible,
adaptable, and flexible design, deferring implementation decisions until
the last practical point (e.g., implementation platform selection and or
toolchain). To support this a set of guiding principles have been
defined to assist the implementor in aligning with current and future
architecture concepts as well as supporting educated decision making. By
understanding and - when in question - reflecting on these principles,
the implementor will understand the intended concept and why certain
decisions were made.

## Platform Agnostic and Open

The reference architecture will not have an opinion on the platform or
toolchain, leaving that to the implementor. To support this deferral and
maintain flexibility services and components will maintain a separation
of concerns, exposing clearly defined demarcation points, contracts, and
interfaces for interoperability with other components in the
architecture. When possible, any outward-facing exposed surfaces of the
component will leverage industry and or open standards, vs. proprietary
or bespoke ones.

While the reference architecture may have opinions on characteristics
and locale of one or more components and services (e.g., the OT
connectivity components should maintain affinity to the OT asset’s
location) the contractual approach enables the services to be migrated
between the enterprise locations and plants as appropriate.

The pluggable nature of the reference architecture supporting well-known
contracts for integrations allows it to be platform-agnostic while
choosing to implement platform-specific components and services as
appropriate for cost, scale, or availability reasons.

## Simplicity

As history has taught us simplicity tends to win out over complexity if
the simple solution can deliver on the required business needs. Reasons
for this include more comprehensive reasoning about the solution by its
designers, lower chance of faults in operations, and easier support by
the responsible teams. When options exist and all solutions to the
problem address the business solution select the simplest version with
the assumption that adjustments can be made over time if required.

## Security-by-Design

We have seen many architectures fail as cross-cutting aspects like
security and compliance decisions have not been decided upon up front
(“we don’t need this in our MVP”). But security, privacy, and compliance
have severe implications that can’t be delayed for later decision
making. If production data is not allowed to leave the data center
located at the plant a public cloud solution might not viable.

Security must be integrated from the start, easy integration and
adoption of additional security and compliance requirements is a must.
Many of these principles require fast implementations and violations
have a huge impact. Define features and components in a way that enables
easy integration and adoption of the current security and compliance
stances of the operator.

## The Edge is an Extension of the Centralized Compute Power

Centralized information and compute power offer significant benefits
when it is a viable choice. Cloud computing offers such centralization
and is currently becoming the de facto approach for new IT developments.
This introduces the need to encourage a cooperative solution that
extends from the centralized compute power (e.g., Cloud) to the outer
reaches of the edges. This will include the decision to make all
information accessible from or in the cloud. This does not mean all
information must be streamed or low latency, but it should be available
centralized for enterprise-wide analytics and data mining.

## Information is the Center of Gravity

Over the years there have been several movements associated with
centralized and decentralized processing and storage, and it is
currently in a centralized trend with the public cloud. As discussed
before the goal of the solution should be to make all information
discoverable, accessible, and actionable based regardless of its
location.

Information can be moved to and from the edge and cloud as appropriate
based upon different “temperatures” *(see Note)* representing latency
and velocity requirements.

---------------------------------------------------------------------
>***Excursion***
>
>-   ***Cold Information** is typically moved to and from the cloud or
>    facility based on a timer or the arrival of a file allowing for
>    large batches as required for performance and scale. This has a
>    higher latency and is typically used for post-processing and
>    analytics.*
>
>-   ***Hot Information** is typically moved to and from the cloud or
>    facility through a streaming technique with a requirement of being
>    to its endpoint with as low latency as reasonable. Examples of this
>    may be tied to an alert on a piece of machinery that identifies a
>    looming production outage.*
>
>-   ***Warm Information** is a combination of the Cold Information and
>    Hot Information paths, where a condition that is transferred via the
>    Hot Information path triggers a Cold Information transfer. For
>    example, consider a rolling 2-minute window of vibrations that is
>    being tracked for a generator. When a power spike occurs, it
>    triggers a Hot Information data movement then immediately follows
>    with a Cold Information movement of the vibrations file.*
---------------------------------------------------------------------

Common data access and analysis patterns have existed for many years
with two higher-level solution domains that should inform the decisions
when designing or implementing components and services:

-   **High-Performance Computing (HPC)** is used when data is easier to
    move vs. coming up with enough processing power to perform the
    required operations. In this case, the data is moved to the compute
    resources and processed in many smaller sets, only later being
    reconstituted into the results.

-   **Big Data** is leveraged when data is too large or too high
    velocity, so the compute resources are placed closer to the data to
    perform the operations.

The solution should borrow concepts and decisions from these two
domains when solving problems to identify locations of execution and
where data should be maintained and at what velocity (information
temperature). In addition to this, as much data as reasonably possible
should be moved to the cloud to take advantage of the best AI/machine
learning models and avoid the requirement to move massive amounts of
data in the future. Options should still exist to perform distributed
analytics at the edge.

## Cost is a Factor

Due to the sheer volume of data, usage of resources, and the complexity
of the analytical routines required to implement a solution, cost is
always a factor. Individual projects under this larger umbrella term
must return a net benefit. Thus, the reference architecture will be
designed with principles that will help reduce overall cost. In
particular:

-   **Data reusability**: The foundation of many use cases is sensor
    data from machines. Capturing, preparing, and storing this data has
    an overhead cost. Sharing this overhead across multiple use cases
    will improve the RoI of individual projects. In addition, data reuse
    will reduce the cost of data quality.

-   **Analytic reusability**: Like use cases, there are common
    analytic functions (for example in data quality and preparation) in
    addition to common analytic use cases. Analysts should be able to
    draw on pre-existing models, processes, and tools for either direct
    reuse or adaptation for new use cases.

These two factors combined imply a need for Governance. Both data
governance and the governance of analytic routines – especially for
common transformations. Governance covers a broad array of use cases,
but at minimum, the reference architecture will consider:

-   Data cataloging, including stewardship functionality

-   Data quality

-   Data retention policies

-   Access and security, including consideration if data privacy
    regulation will apply

-   Analytical Operations - systems and processes to automate and govern
    analytical routines from experimentation to production

An additional aspect of the cost considerations prescribes the need to
balance scale vs. cost where that may be dynamically adjusted during
operations. This is sometimes referred to as the elastic nature of the
component, service, or solution.

## Design for Business Continuity, Disaster Recovery, and Compliance

Business continuity and disaster recovery are first-order concepts in
all services and components. Each of these components, services, and/or
capabilities will define a business continuity strategy from the start,
along with confirmation and testing recommendations.

Compliance and or regulatory requirements must be inputs into the
decision process for all aspects.

[Conclusion >](./08_Conclusion.md)