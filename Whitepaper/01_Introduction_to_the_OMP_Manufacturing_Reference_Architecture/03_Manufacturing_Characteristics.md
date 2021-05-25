[< Approach](02_Approach.md)

# Manufacturing Characteristics

Every company is unique, and manufacturing businesses are shaped by
their history and product portfolio. But all manufacturing companies
share the following characteristics to some extent.

## Distributed Data Generation

Data in manufacturing is generated in diverse locations, systems, and
devices. The data generation and collection processes are therefore
highly heterogeneous. There is no easy way to comprehend the initial
data gravity as the data generation stream has so many different sources
and flow characteristics. High frequent vibration detection in machines
is equally important as stock level changes from an ERP system.

## Distributed Decision Making

Decisions in manufacturing are made across the production network.
Centrally introduced orders are executed in plants that are typically in
some kind of coopetition. Plants have a lot of decision power and
therefore are driving many decisions to optimize the processes inside
their own perimeter. This is an antagonist for standardization efforts.
Inside plants decisions are made on different levels and by different
actors from OT and IT. Data must be provided in different qualities to
enable these decision processes. While in most cases these are made by
humans there will be many more machine-driven decisions in the future.

## Cyber-physical Processes

Manufacturing is the physical transformation of material to products.
Familiar IT concepts like “undo” or “rollback” are therefore
complicated. Reversing a physical transformation is challenging and
usually requires a lot of effort and dedicated processes like rework.
Therefore, architectures must be designed to allow alignment with
physical transformation steps.

## Extreme Asset Diversity

The most important elements on the shop floor are the assets, which can
be broken down into machines and devices. In brownfield installations,
there are typically many different product generations working
side-by-side and some of them might be operational for many decades
already. Connecting them for both data acquisition and command
execution, therefore, is a challenging task and many generations of
protocols (Profibus, Profinet, OPC UA, etc.) are examples of this. The
missing standards in data semantics are adding to this complexity.

## Extreme System Diversity

As with asset diversity, the manufacturing system landscape is typically
a brownfield scenario with huge differences between the plants. The
heterogeneity of the systems is typically growing with the overall
company size. Often comparable capabilities are implemented differently
from one plant to another. A broad variety of products being produced
and company mergers in the past are fueling these differences.

## Varying Response Time Requirements

Response time and network latency have highly deviating requirements,
depending on the context of the specific use case and fit within the
overall reference architecture. While PLC control loops may be measured
in milliseconds and have the need for defined cycle times, for other
contexts like interaction with an MES or alert acknowledgment seconds or
even hours are sufficient. The architecture must be able to satisfy both
extremes. Therefore, it is important that supporting operations and
infrastructure can be placed accordingly. As an example, for low latency
requirements on the shop floor a component will need to be able to run
on the edge, while in more latency tolerant scenarios it may be well
placed in a cloud environment.

There are specific requirements that are more typical to the operations
side of the network that may require technologies such as time-sensitive
networks (TSN) to be supported.

## Heterogenous Ecosystem

Manufacturing is relying on a complex ecosystem of different partners
within a company as well as external partners, suppliers, and customers.

They have different information needs and are granted individual data
access. Cybersecurity and data privacy is, therefore, a huge challenge
for balancing protection and open collaboration.

[Key Challenges >](04_Key_Challenges.md)