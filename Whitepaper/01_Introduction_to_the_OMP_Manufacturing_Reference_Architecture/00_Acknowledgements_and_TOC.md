<img src="media/image1.jpeg" style="width:11.81437in;height:7.38168in" />
<img src="media/image2.png" style="width:3.5359in;height:0.54236in" />

<br/>

# Introduction to the OMP Manufacturing Reference Architecture <!-- omit in toc -->
## General Approach & Design Considerations <!-- omit in toc -->

|Published|Version|
|---------|-------|
|May 13, 2021|1.0|


<br/>

### Legal Disclaimers <!-- omit in toc -->

Copyright (c) 2021 Joint Development Foundation Projects, LLC, OMP Series and
its contributors. All rights reserved.
  
THESE MATERIALS ARE PROVIDED "AS IS." The
parties expressly disclaim any warranties (express, implied, or otherwise),
including implied warranties of merchantability, non-infringement, fitness for a
particular purpose, or title, related to the materials. The entire risk as to
implementing or otherwise using the materials is assumed by the implementer and
user. IN NO EVENT WILL THE PARTIES BE LIABLE TO ANY OTHER PARTY FOR LOST PROFITS
OR ANY FORM OF INDIRECT, SPECIAL, INCIDENTAL, OR CONSEQUENTIAL DAMAGES OF ANY
CHARACTER FROM ANY CAUSES OF ACTION OF ANY KIND WITH RESPECT TO THIS DELIVERABLE
OR ITS GOVERNING AGREEMENT, WHETHER BASED ON BREACH OF CONTRACT, TORT (INCLUDING
NEGLIGENCE), OR OTHERWISE, AND WHETHER OR NOT THE OTHER MEMBER HAS BEEN ADVISED
OF THE POSSIBILITY OF SUCH DAMAGE.


<br/>

### ACKNOWLEDGMENTS

This document is a work product of the Open Manufacturing Platform -
Manufacturing Reference Architecture Working Group, chaired by Martina
Pickhardt (Microsoft) and co-chaired by Nils Jensen (PwC).

<br/>

### AUTHORS

Open Manufacturing Platform / Manufacturing Reference Architecture
Working Group

<br/>

### CONTRIBUTORS

| Contributer | Company |
|--|--|
| Alexandra Belata | VMWare |
| Lukas Birn | Capgemini |
| Chris Clayton | Microsoft |
| Nils Jensen | PricewaterhouseCoopers (PwC) | 
| Bernd Kammholz | VMware |
| Monica McDonnell | Teradata |
| Klaus Merk | Microsoft |
| Martina Pickhardt | Microsoft |
| Wolfram Richter| Red Hat |
| Jethro Ridl | Reply |
| Harald Ruckriegel | Red Hat |
| Michael Schuldenfrei | NI |
| Joachim Sprinz| ZF |
| Jürgen Vischer | Forcam |

<br/>

### Table of Contents

- [Introduction](./01_Introduction.md#introduction)
  - [Context](./01_Introduction.md#context)
  - [Intended Audience](./01_Introduction.md#intended-audience)
- [Approach](./02_Approach.md#approach)
  - [Vision and Mission](./02_Approach.md#vision-and-mission)
  - [Scope and System Structure](./02_Approach.md#scope-and-system-structure)
- [Manufacturing Characteristics](./03_Manufacturing_Characteristics.md#manufacturing-characteristics)
  - [Distributed Data Generation](./03_Manufacturing_Characteristics.md#distributed-data-generation)
  - [Distributed Decision Making](./03_Manufacturing_Characteristics.md#distributed-decision-making)
  - [Cyber-physical Processes](./03_Manufacturing_Characteristics.md#cyber-physical-processes)
  - [Extreme Asset Diversity](./03_Manufacturing_Characteristics.md#extreme-asset-diversity)
  - [Extreme System Diversity](./03_Manufacturing_Characteristics.md#extreme-system-diversity)
  - [Varying Response Time Requirements](./03_Manufacturing_Characteristics.md#varying-response-time-requirements)
  - [Heterogenous Ecosystem](./03_Manufacturing_Characteristics.md#heterogenous-ecosystem)
- [Key challenges](./04_Key_Challenges.md#key-challenges)
  - [From Initial Pilots to Scaled Adoption](./04_Key_Challenges.md#from-initial-pilots-to-scaled-adoption)
  - [Self-Funding Transformation](./04_Key_Challenges.md#self-funding-transformation)
  - [Lacking IT Skills](./04_Key_Challenges.md#lacking-it-skills)
  - [Sidecar vs. Rip-and-Replace Approach](./04_Key_Challenges.md#sidecar-vs-rip-and-replace-approach)
  - [Ambition Order of Magnitude](./04_Key_Challenges.md#ambition-order-of-magnitude)
- [Use Case Considerations for Architecture design](./05_Use_Case_Considerations.md#use-case-considerations-for-architecture-design)
- [Platform Capabilities](./06_Platform_Capabilities.md#platform-capabilities)
- [Architecture Design Principles](./07_Architecture_Design_Principles.md#architecture-design-principles)
  - [Platform Agnostic and Open](./07_Architecture_Design_Principles.md#platform-agnostic-and-open)
  - [Simplicity](./07_Architecture_Design_Principles.md#simplicity)
  - [Security-by-Design](./07_Architecture_Design_Principles.md#security-by-design)
  - [The Edge is an Extension of the Centralized Compute Power](./07_Architecture_Design_Principles.md#the-edge-is-an-extension-of-the-centralized-compute-power)
  - [Information is the Center of Gravity](./07_Architecture_Design_Principles.md#information-is-the-center-of-gravity)
  - [Cost is a Factor](./07_Architecture_Design_Principles.md#cost-is-a-factor)
  - [Design for Business Continuity, Disaster Recovery, and Compliance](./07_Architecture_Design_Principles.md#design-for-business-continuity-disaster-recovery-and-compliance)
- [Conclusion](./08_Conclusion.md#conclusion)
- [Appendix](./09_Appendices.md#appendix)
  - [Definitions and Terms](#definitions-and-terms)


<br/>

### Table of Figures

Figure 1: [Overcome the Purdue ISA-95 model to build a smart manufacturing platform. - RAMI 4.0 inherited and evolved the standard IEC:62264 hierarchy](./02_Approach.md#fig1)

Figure 2: [Data Flows and Use Cases are the main driver of the Manufacturing Reference Architecture](./02_Approach.md#fig2)

Figure 3: [Scope of Manufacturing Reference Architecture](./02_Approach.md#fig3)

Figure 4: [Example Use Case Themes supported by the Manufacturing Reference Architecture](./05_Use_Case_Considerations.md#fig4)

<br/>

[Introduction >](01_Introduction.md)