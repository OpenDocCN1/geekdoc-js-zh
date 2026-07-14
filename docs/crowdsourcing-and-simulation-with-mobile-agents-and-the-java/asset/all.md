![](cover.png)

# Table Of Contents

# Introduction

Agents are well known as human beings that operate on commission for another human being or company to fulfil an order mostly autonomously. Agents are characterized by their social interaction capabilities and social structuring. Autonomy is usually based on planning, cognition, and knowledge.

Agents can be artificial entities, too. They can be used for modelling and simulating natural systems as well as for implementing modern software with superior features. Therefore, agent-based modelling addresses social and natural science on the one hand, and computer science on the other hand.

Agent technology, in contrast, evolved over the past decades and is used to implement or support intelligent systems in unreliable and sometimes unknown environments.

Agent technology is mainly driven by:

*   Symbolic Artificial Intelligence,
*   Machine Learning,
*   Control Theory, and
*   Distributed Computing paradigms.

Agent technology is used to master complex dynamic problems in a wide range of fields. Intelligent behaviour is a fundamental feature of agents [MUE96], although the term intelligence is not defined precisely, leading to misconceptions and misunderstanding.

Agents can be used to model and implement complex systems by decomposing the system in simple interacting units, i.e., micro-level modelling, in contrast to macro-level modelling, which uses one big formula to describe the system behaviour. An agent can be a model or a computation paradigm.

This book addresses agent-based computation and agent-based simulation with the JavaScript-based open source software framework *JAM*, available for download on [github](https://github.com/bsLab/jam). JAM is a VM-in-VM concept. Only basic programming skills (in JavaScript) and a Web browser or a command terminal with node.js are required to start exploring the world of mobile agents. Crowdsourcing is a primary application using mobile agents, discussed in detail and with working examples.

## Software Paradigms

There are five major software paradigms reflecting historical changes:

1.  Machine programming;
2.  Procedural programming;
3.  Functional programming;
4.  Object-oriented programming;
5.  Agent-based goal- and role-oriented programming.

The historical development of programming paradigms is shown in Fig. [1-1](#0_introduction.xhtml_softwareparadigms). There are various challenges in the development of modern IT systems:

*   Ubiquity → 1\. Unbound to a location 2\. Environmental computing
*   Pervasiveness → Penetration of computer science into things and devices
*   Networking of devices and programs
*   Distribution and parallelization of programs
*   Intelligence and learning
*   Autonomy → Without central authorities and control
*   Robustness → 1\. The world changes 2\. The world behaves insecure
*   Adaptivity → The world has changed
*   Delegation of tasks and hierarchies
*   Human-machine interface

![no=1](images/04d365d6-8541-4b3b-b68c-9727acebcc77.png)Figure 1-1\. Historical development of programming paradigms

## Agents

### Autonomy

Agents are autonomous systems interacting in a specific environment (the world). The environment can consist of data and physical entities that can be manipulated by agents. An agent can observe the world through sensors, creating some degree of knowledge about the world. This knowledge can be used to plan decisions and perform actions. Agents communicate with their environment and effect changes in the environment. An agent is always part of the environment, too. Agents are basically characterized by their capabilities and features, discussed in the Section [Agent Capabilities]. There are different understandings and models of agents, basically coupled to diverse scientific communities using agents for different purposes. The science disciplines range from social science to computer science, with an impact from economy, business, and production.

In computer science, the agent concept is used to establish a paradigm shift from the traditional and still widely used client-server architecture towards distributed agent systems performing data processing and communication, as illustrated in Fig. [1-2](#0_introduction.xhtml_mobagcomm1).

![alt=images/fig2.eps](images/90fcfaef-8cfa-4753-920c-639f01da3d1e.png)Figure 1-2\. From the client-server communication architecture (a) towards distributed agent-based and agent-controlled communication (b)

In addition to the general agent concept, mobile agents are defined by two concepts: Mobility and agency [CAO12]. Mobile agents can reduce communication costs and can increase robustness through adaptivity and replication.

### Metrics

Agents can be classified by the following metrics:

1.  Physical Agents

    9.  Hardware Agents
    10.  Software Agents
    11.  Social Agents
2.  Computational Agents

    9.  Interface Agents (Human-Machine and Machine-Machine)
    10.  Data Processing Agents
3.  Mobile Agents

    9.  Physical Agents
    10.  Computational Agents

In this book, two different agent classes are used in conjunction:

Physical Behavioural Agents

represent physical entities, i.e., individual artificial humans, animals, vehicles, or more general machines. This agent category is divided into hardware agents, i.e., being robots or machines, and software agents, representing physical entities. A sub-set of software agents are social agents, which model the behaviour and interaction of social systems. Agents in simulation are considered as physical agents, too, since they represent physical entities.

Computational Agents

represent software and processes performing computational tasks, i.e., used for distributed data processing and digital communication, or implementing chatbots. Computational agents require an Agent Processing Platform (APP) for their execution.

Mobile Agents

can be considered as a super-set of physical and computational agents. Mobility of physical agents means the capability of spatial movement of the hardware or software agents (or the migration of social entities). Mobility of computational agents, represented by computational processes, means the transfer of a process snapshot between agent processing platforms.

Among the basic agent classifications from above, dividing the agents by their impact on and interaction with the environment, agent-based methods can be classified by their deployment and usage with five domains:

* * *

1.  Agent-based Modelling (ABM)
2.  Agent-based Simulation (ABS)
3.  Agent-based Modelling and Simulation (ABMS)
4.  Agent-based Computing (ABC)
5.  Agent-based Simulation and Computing (ABX)

* * *

This book discusses the different modelling and deployment fields of agents and finally presents a fusion of all four levels (ABX) using the JavaScript Agent Machine.

### Model

An agent, independent of its classification, interacts with an environment by basically two mechanisms:

1.  Perception: performing environmental sensing and interpreting sensor values;
2.  Action: performing modification of the environment.

The simplest agent behaviour model and architecture is shown in Fig. [1-3](#0_introduction.xhtml_agentbeh1) and consists of a cyclic data flow between the agent and the environment.

An agent poses a set of sensors *S*=( *s*[1,] *s*[2,] .. , *s*[*n*] ) used for perception, and a set of actuators *A*=( *a*[1] , .. , *a*[*m*] ) used for the modification of the environment.

The basic black box model of the agent's behaviour is a function *Ag* that maps the sensor input vector *S* to the actuator output vector *A*:

| ![image-placeholder](images/66c83bf8-1c36-4381-af00-67bcca23dcc8.png) | (1-1) |

![alt=images/fig3.eps](images/45c8d44b-bbd8-4802-8a54-58d1c3ff7ba5.png)Figure 1-3\. Simple reactive agent behaviour model and architecture

Sensors can be classified in:

1.  Physical Sensors - intrinsic and extrinsic measuring different physical properties:

    *   Temperature (ambient, body, remote, device, component)
    *   Motion (Acceleration, rotation, translation)
    *   Position (Global, local, absolute, relative)
    *   Light (Intensity, colour, wavelength, spectrum)
    *   Radiation (electromagnetic, nuclear)
    *   Pressure (Air, loading)
    *   Humidity, Moisture
2.  Data-driven logical sensors delivering data from:

    *   WEB Content
    *   Data bases
    *   Networks
    *   Social Media
    *   Text and Graphics
3.  Virtual Sensors (Aggregated from physical and logical sensors)

Actuators can be classified in:

1.  Actuators that change the physical world
2.  Logical Actuators (Data) modify the digital world

## Modelling Concepts

There are basically two different modelling approaches for systems:

1.  Top-down Modelling;
2.  Bottom-up Modelling.

Top-down models start with the specification of the global system level and divide the system model into smaller modules directly derived from and coupled to the system level specification. The behaviour of the system level is known in advance and can be verified. The behaviour of the modules is directly derived from the system level. In contrast to top-down modelling, bottom-up models start with a set of simple interacting cells, eventually composing a system from these cells. The system level is a result of the interaction of cells and their behaviour, not known and specified in advance. Agent-based modelling belongs to the bottom-up class.

## Capabilities of Agents

An agent provides a set of features and capabilities that distinguish agents from traditional software:

* * *

*   Autonomy
*   Self-* capabilities:
    *   Self-organization
    *   Self-coordination
    *   Self-adaptivity
    *   Self-optimisation
    *   Self-learning
    *   Self-awareness
*   Divide-and-Conquer enables the composition of complex systems with simple entities similar to Cellular Automata
*   Resilience and robustness
*   Learning and adaptivity of behaviour
*   Planning and Cognition
*   Knowledge Representation, Induction, and Deduction
*   Symbolic Reasoning
*   Social capabilities like
    *   Coordination
    *   Cooperation
    *   Negotiation
*   Emergence behaviour in multi-agent systems, i.e., only the aggregate behaviour of the system is relevant, not individual behaviour of agents (and failure)
*   Loosely coupling between agents and agents and the execution platform (API)

* * *

Agents are similar to cellular automata, which are used to model complex systems by connecting simple basic cells. The main difference between cellular automata (usually only implementing simple input-output functions) and agents is their interaction distance, which is short range (limited to the neighbourhood) in cellular automata and arbitrary in agent-based systems.

### Emergence

The observation of emergent properties is the global or collective behaviour of a system composed of a collection of loosely coupled simple entities or agents.Emergence is a result of self-organization, self-adaptivity, and self-coordination. On one hand, the emergent behaviour vanishes if the system is broken down into individual parts (operating in isolation) or if a relevant fraction of individual parts of the system is removed. On the other hand, the removal or malfunction of a small fraction of individual parts does not affect the emergent properties of the global system significantly [DAM13].

The emergent behaviour of the system can neither be modelled at an individual entity level directly, nor at a system level by a global function. This emergent behaviour is usually observed. Although, the emergent behaviour is determined by the individual behaviour of the agents. But multi-agent systems aim to reverse engineer emergent phenomena. Typical examples are ant colonies, the economy and trading, and the immune system.

An example of emergent behaviour is segregation, i.e., long-term movements of individuals forming spatial clusters, e.g., in town areas. The Shilling model is a well-known clustering model based on very simple behaviour and interaction. The Sakoda model is less known, but can be parametrized at an individual level. Some simulation results of globally visible segregation effects are shown in Fig. [1-4](#0_introduction.xhtml_sakofasimu01). The Sakoda model is based on an individual local utility (satisfaction) function that calculates a utility to stay at the current or at another place under specific environmental conditions (other agents in the neighbourhood) [BOS19C].

![#sakofasimu01](images/7562c53e-24a2-4500-a91a-af6b621d9d33.png)Figure 1-4\. (a) Simulation world with 200/200 randomly distributed artificial Sakoda behaviour agents of class a/b (blue/red squares) (b) Simulation world with social organisation based on mobility, forming strong isolated homogeneous clusters after 200 simulation steps [BOS19C]

## JavaScript

The agent processing platform as well as the programming of agents is done with pure JavaScript. JavaScript, originally named ECMAScript, is a partially functional and object-oriented imperative programming language with one control flow (strict single-threaded without pre-emption) and automatic memory management. JavaScript programs consist of polymorphic variables and functions. JavaScript is dynamically typed, i.e., data types and function interfaces are evaluated at run-time. There are basically only six defined core data types:

1.  Number (commonly double precision float)
2.  String (immutable)
3.  Boolean
4.  Object
5.  Function
6.  Undefined

Arrays and structures are both objects. Arrays are poly-sorted, i.e., different elements of an array can be of different data types. Arrays are commonly created incrementally by the *push* operation. Array elements are accessed by the bracket operator. Structure elements (object properties) are accessed by the dot operator by providing the property name as an identified. Alternatively, the property can be selected by the bracket operator, too, by providing the name as a string. Pure data objects (records) and arrays can be created on the fly:

* * *

```
[](#cb1-1)var a = []
[](#cb1-2)for(var i=0;i<10;i++) a.push(i);
[](#cb1-3)a[1]=a[2]-1;
[](#cb1-4)var img = {
[](#cb1-5)  x:1,
[](#cb1-6)  y:-1
[](#cb1-7)}
[](#cb1-8)var absimg=Math.pow(img.x,2)+Math.pow(img.y,2)
[](#cb1-9)var struct1 = { x:1, y:2 }
[](#cb1-10)struct1.x=struct1.y
[](#cb1-11)struct["y"]++;
[](#cb1-12)var array1 = [1,2,3,'A','B']
[](#cb1-13)array1[0]=array[1]+1
[](#cb1-14)function foo () { .. }
[](#cb1-15)var foo2 = foo
[](#cb1-16)var foo3 = function () { .. }
[](#cb1-17)var foo4 = () => { }
```

* * *

Object classes were originally supported by adding prototype functions to object constructor functions:

* * *

```
[](#cb2-1)function cls() { this.data = ε; .. }
[](#cb2-2)cls.prototype.method = function () { this.data= ε }
[](#cb2-3)var obj = new cls()
[](#cb2-4)obj.method(..)
```

* * *

Each prototype function can access the instatiated object by using the `this` variable. All objects instantiated from the same constructor function share the same set of prototype functions.

A variable can hold any value, but initially the value `undefined`.

> Any value can be assigned at anytime to a variable, including named and anonymous functions. Functions can be serialized anytime to text again, an important feature for object (agent) snapshots and check-pointing. All non-cyclic and objects without prototype bindings can be serialized to text in the JSON format.

There are only two scopes of identifiers (i.e., variables and functions): The global scope and the function body scope. All variable definitions in the same scope are merged, function definitions are overridden in the order they appear:

* * *

```
[](#cb3-1)var top=1
[](#cb3-2)function foo (localparam) {
[](#cb3-3)  var local=2
[](#cb3-4)}
[](#cb3-5)var top=2 // overrides line 1
```

* * *

Function are objects, too. Each function provides at least the *prototype* property referencing the set of dynamic functions, and can be extended with user defined properties, e.g., static functions or data values:

* * *

```
[](#cb4-1)function foo () {}
[](#cb4-2)foo.name = 'foo'
[](#cb4-3)foo.info = function () { return foo.name }
```

* * *

Text serialization and deserialization of data and functions are major features of JavaScript important for the support of mobile agents via process snapshots.

# Crowdsourcing

At the beginning of this chapter, a short terminology should be introduced that will be used throughout the book:

* * *

Sensor

Physical converters that convert one physical quantity into another physical quantity (usually analogue, electrical or digital). Examples of physical quantities are temperature, light intensity, acoustic waves, and mechanical strain.

Virtual Sensor

Functions with an input and output interface for further processing and fusion of sensor signals. Aggregate variables (e.g., average) can be computed by virtual sensors.

Sourcing

Creation of added value: Source of information with the provision of data but also the provision of work performance; Collection of goods;

Sensing

Process of acquisition and collection of sensor data ***X***={*x*[1],..,*x*[i]}, typically periodically or event-based along the longitudinal time axis, i.e., *x*=*x*(*t*).

Perception

Perception and interpretation of sensory information

Survey

In addition to providing sensory data, ***X***={*x*[1],..,*x*[i]} (if necessary, passive), there may be active participation in data collection, i.e. for model testing or model calibration, e.g., social network models.

| ![image-placeholder](images/6e132d10-41b1-402b-b706-eaa5fe445097.png) | (2-1) |

Data Mining

Derivation of information from data (variables ***X***=*x*[1],..,*x*[i]) often without accurate (statistical) models and correlation of variables, i.e.:

| ![image-placeholder](images/376ccf79-a03b-4fdf-a398-710c0ef2221c.png) | (2-2) |

Crowdsourcing (CSO)

Provision of work performance by a larger group of people who are not directly organized (socially connected). This could include active participation in surveys, which is sensing only (i.e., *CSE* ⊂ *CSO*).

Crowdsensing (CSE)

Sensory information provided by a larger group of people who are not directly organised (socially connected) is collected and recorded.

Mobile Crowdsensing (MCS)

CWS with mobile devices and mobile users → spatial changes and the location context of sensor data are important and must be considered as additional sensor information, e.g., using GPS devices for localization with latitude, longitude, and height information, or at least based on the Internet address.

* * *

## Overview

The significance and history of crowdsourcing foremost requires the answer to the question of what is generally considered as crowdsourcing, but it is technically not [BRA13]:

*   Open Source Software Development
*   "Commons-Based Peer Production": Socio-economic production approach with numerous people working cooperatively on a project
*   "Brand engagement" forms an emotional or rational bond between a consumer and a brand. It includes aspects of brand management.
*   The creation of the Oxford English Dictionary in the 1800s was an early example of crowdsourcing? Maybe.

> Crowdsourcing has its origins in economics, business, production, marketing, etc. to increase the added value of products.

The primary goal of crowdsourcing and crowdsensing is to increase value, i.e., [LEB13]:

*   **Cost reduction**
*   **Innovation**
*   **Authenticity**

But sociology and "political science" are also increasingly recognizing the benefits of crowdsourcing! Increasingly, crowdsourcing is used for the voluntary creation of geographical knowledge databases and maps! The terms crowdsourcing and crowdsensing have not been defined uniformly. A distinction is made between: sensors (perception) and actuators (action). Therefore, the following classification should be used:

Crowdsourcing

Foremost, crowdsourcing can be understood as the utilization of human labour resources with a collective goal, i.e., actuators. Furthermore, the collection of user data (sensors) without or with the direct participation of the user or the public self-organising provision of services by users. The user is not necessarily aware of the collection of his data.

Crowdsensing

The collection of user data without or with the participation of users.The user can be aware of the collection of his data and actively participate. Crowdsensing can be understood as a subclass of crowdsourcing.

The main concept introduced in this book is based on the automated perception of sensory information to be implemented by mobile agent systems. These agents can be run on a variety of computers and mobile devices through a universal execution platform. The platforms should span a virtual network that allows the agents to "visit" different devices, including smartphones. The agents should interact with people and machines in different ways, using different interfaces:

*   Human-agent-machine interface
*   Machine-Agent-Machine Interface
*   Agent-Agent interface

The agents will perform their tasks in loosely coupled and interacting multi-agent system groups based on divide-and-conquer and self-organization principles, shown in Fig. [2-1](#1_crowdsourcing.xhtml_mcsconcept1).

The basic component of the distributed crowd software framework is the JavaScript Agent Machine (JAM) introduced in this book. JAM is basically an agent processing platform library that can be embedded in any host application programmed in JavaScript. Some dedicated pre-built applications are the command-line JAM shell (*jamsh*), the mobile JAM App (for Web browsers or smartphone application programs), and the JAM Web laboratory.

In addition to sensing, distributed computing can be implemented with the same framework, too. Distributed computing can utilize already distributed (sensor) data, featuring the concept of local data processing, or require explicit data distribution, discussed in the next sections.

![#mcsconcept1](images/877a7081-8831-4845-8fd9-21585c578fb7.png)Figure 2-1\. The principle architecture used in this book for mobile crowdsourcing and crowdsensing

## Basics

Different types of crowdsourcing systems can be distinguished [BAR14]:

*   Collective Knowledge Management (e.g., Wikipedia)
*   Collective Creativity → Art and Photography
*   Collaborative Online Gaming
*   Collaborative Voting → rating systems
*   Social Networks
*   Use of crowdsensing and crowdsourcing to optimize process flows (in production systems, etc.)
*   **Service-oriented architecture** (SOA) in crowdsourcing:
    *   **Software-based Services**
    *   **Services of persons**

The process flow of crowdsourcing can be composed of individual tasks that are either processed by corresponding web services or assigned to responsible people. A task can be outsourced to the crowd in this scenario. For this purpose, a support request is prepared, which contains various tasks to be processed by the crowd and additional metadata such as time restrictions and complexity of the task.

![#crowdsens1](images/81a3b97f-f0c0-4d0a-9493-d9ffc91bcd71.png)Figure 2-2\. General architecture of a crowdsourcing or crowdsensing system

**Crowdsourcing System Model**. A crowdsourcing or sensing system is often used for commercial applications and consists of the following entities, performing different tasks (see Fig. [2-2](#1_crowdsourcing.xhtml_crowdsens1)).

1.  Crowdsourcer (Data collector), which receives, aggregates, and analyses the data in a task-oriented manner using data mining → consists of one or more sensor-processing servers
2.  Crowd, a group of many users (data providers) whose sensory and personal data is typically collected using mobile devices such as smartphones.
3.  Both are connected via a cloud environment.

There are connections and directed flows between users and the crowdsourcer instance. In the case of surveys, the crowdsourcer will create a survey plan for negotiated participation, resulting in a bidirectional sequential protocol with flow of goods.

**Bidirectional connections and flow in surveys:**

1.  The users get a description and task of the survey task;
2.  The users have to fulfil a survey plan (directly consciously or indirectly through incentives);
3.  The crowdsourcer (surveyor) selects the users (or wins them through a public tender procedure);
4.  Users provide sensory data for a certain time *t* → Collection service;
5.  Users receive rewards, i.e., direct remuneration or monetary benefits - or voluntarily participate in self-interest.

> There must be a survey strategy that should achieve high efficiency in the survey!

Exercise 2-1\. Reward and Incentives

1.  What non-monetary rewards could there still be in crowdsensing applications?
2.  Is benefit already the acquisition of information or an advantage over others?
3.  What incentives should be given for crowdsensing applications? Are there target group-dependent factors?

### User-centred model

In this model, the crowdsourcer (surveyor) announces a set Γ={τ[1], τ[2],.., τ[m]} of tasks for selection by the user. For the surveyor, each τ[j] ∈ Γ has a task value *v*[j]> 0.

Each user *i*, depending on his preference, selects a subset of tasks Γ[i] ⊂ Γ (based on his preferences). Accordingly, the user *i* also has associated costs *c*[i], which are private and known only to himself.

An auction is started: User *i* then submits an order-bid pair (Γ[i], *b*[i]) to the crowdsourcer, where *b*[i] is the bid and the minimum price for which the user wants to sell his service. When receiving the order packages from all users, the holder selects a subset *S* of users as the winner and determines the payments *p*[i] for each winning user *i*.

The benefit for the user *i* is then:

| ![image-placeholder](images/94e46174-431d-4af5-ba12-edac7d6520cd.png) | (2-3) |

The benefit for the crowdsourcer then results from:

| ![image-placeholder](images/4558f819-bef2-49da-9ee8-de1d7eca2421.png) | (2-4) |

For the user-centred model, one can design an incentive mechanism that should meet the following four characteristics:

**Computational efficiency**: The result of the auction can be calculated in polynomial time.

**Individual rationality**: Each participating user has a non-negative benefit when he presents his true evaluation.

**Profitability**: The value that the winners bring should be at least equal to the sum of the amounts paid to them.

**Truthfulness**: No bidder can improve his benefit by making an offer that deviates from the actual valuation (which is the cost).

### Crowdsourcer-centred model

The surveyor-centred reward model can be understood as a *Stackelberg game*. At the first stage, the surveyor announces the reward. In the second phase (non-cooperative), users will strategically plan their survey time to maximize their usefulness. Three questions have to be answered to find an optimal survey strategy:

*   Question 1: Is there a set of stable strategies in the game for a given reward *R*, so that no user can gain anything by unilaterally changing his current strategy?
*   Question 2: If the answer to Q1 is positive, is the stable strategy unambiguous? If it is unique, can users be sure to choose the strategies from the same stable strategy set?
*   Question 3: How can the crowdsourcer select the value of *R* to maximize its utility?

In this model, there is only one capture task. The crowdsourcer announces a total reward of *R* ≥ 0 and motivates *n* users to participate in crowdsensing, while each user determines his level of participation based on the reward. The user's capture schedule *i* is represented by *t*[i] ≥ 0, the length of time he is willing to provide the sensory capture service or participate in surveys.

If a user sets *t*[i] = 0, the user indicates *i* that he will not participate in crowdsensing. The collection cost of the user *i* is κ[i]*t*[i], where κ[i] ∈ Θ are unit costs and Θ = { θ[1], θ[2],.., θ[l]} let be the set of unit costs.

We assume that the surveyor knows Θ and the probability distribution of users with the unit cost θ[j]. This can be learned from the analysis of historical data. Let *n*[j] represent the number of users with the unit cost θ[j], i.e. *n*=Σ*n*[j]. Suppose the reward received by user *i* is proportional to *t*[i]. Then the benefit *u*^_[0] of the user *i* is the reward minus the cost:

| ![image-placeholder](images/c49fedd4-9bb1-44d0-b777-dc409182e469.png) | (2-5) |

Therefore, all users with the same unit cost would choose the same capture plan! Is this true? The usefulness of the surveyor *u*^_[0] is then given by an evaluation function *g* (which depends on the actual perception times *t*^~[1] of the users) minus the total reward *R*:

| ![image-placeholder](images/01afa4c2-05bb-4d3a-8ca3-63b7d9999c4f.png) | (2-6) |

Simplification and determination: users with the same unit costs will provide the same survey time! So, with this model, the goal of the crowdsourcer is to determine the optimal value of *R* in such a way that it maximizes *u*^_[0]. Each user *i* independently decides on his acquisition time *t*[i] in order to maximize the specified value of *R*. Since no rational user is willing to provide a survey service for a negative utility, the user will set *i* to *t*[i] = 0 if *R* ≤ κ[i]Σ*t*[j] for all *i* ≠ *j*.

### Reward

In the previous section, the monetary reward was introduced by negotiation. There is a utility function that has to be fulfilled, and the survey time plays an essential role. Both the user (data provider) and the surveyor (data collector) have their own utility function, potentially opposite!

The reward should achieve three goals in data collection:

1.  Large number of participants → Create incentives;
2.  Broad coverage (and representativeness);
3.  Data quality (coverage of survey objectives).

So there are basically three reward classes:

1.  Incentive of participation by **monetary reward** → macro and micropayments *M*
2.  Incentive to participate through **Games**;
3.  Incentive to participate by **Improving social contacts**;
4.  Incentive to participate through **Opening Locks** → CAPTCHA principle,

> Reward is motivation!

There are two types of motivation:

**Intrinsic motivation**: Fun, challenging, learning

**Extrinsic motivation**: Monetary goals, social pressure, fame

Intrinsic motivation can be more significant than extrinsic for crowdsourcing and crowdsensing. Both types share the individual optimization of the utility function (of the user) for the individual user.

## Distributed Computing as Crowdsourcing

Using networked devices, i.e., computers connected via the Internet, two basic operations on remote computers are possible:

1.  Sensing;
2.  Computation.

Although, sensing involves computations, too, the computational capabilities of generic daily-use computers like laptops or smartphones can be used to create a large virtual computational machine. If a user opens a Web page in his browser, JavaScript is used, originally, to provide some dynamic content on the Web page, e.g., updated news headlines. But today, a significant number of Web pages are completely built dynamically by computation, and numerous communication requests are initiated programmatically. Modern JavaScript engines provide enough performance to perform Machine Learning (ML) in the browser.

So again, considering participatory and opportunistic crowdsourcing, Web pages, e.g., can be used as short-time computational containers. The mobile agent framework introduced in this work can be used to distribute computation in the Web.

Opportunistic crowdsourcing of computational power is a lot more critical and difficult than sensing. The sensing task is short and mostly not state-based. That means, if the user reloads the Web page, the sensors can be accessed again and the sampled data can be communicated to a data sink without any loss. But a long-duration computation like ML cannot be interrupted in this way - all reached computation results would be lost. Distributed computation requires therefore some kind of snapshot mechanism to save intermediate computation results that can be used for another run, either on the same computer or another.

## Mobile Crowdsensing

Mobile crowdsensing is a technology that enables the large-scale, cost-effective capture of the physical world. With mobile crowdsensing, people who devote themselves to their everyday lives become "sensors". Mobile devices, such as smartphones or smartwatches, are equipped with a variety of sensors that can be used to collect data on the environment, transport, health, and safety. Crowdsourcing and crowdsensing techniques allow people-oriented perceptions to create a comprehensive, collective perception. In conjunction with static sensor networks and Internet of Things (IoT) devices, mobile crowdsensing can make the vision of ubiquitous perception a reality.

There are essentially three components that can be seen as the basis for mobile crowdsensing:

1.  Sensor-equipped mobile devices (smartphones);
2.  Application programs for mobile devices
3.  Standardized software interfaces

Server-centric systems consist of strictly divided components:

*   Sensor source: Smartphones as sensors for extended spatial areas that deliver sensor data to servers;
*   Sensor sink: Servers that collect data. But the server also provides a service with aggregated data for the users.

> Mobile crowdsensing: People are both consumers and producers of sensory data!

In road transport and transportation, there is commonly a transportation department that can collect finely resolved and large-scale data on traffic behaviour in the country or city based on location and speed data provided by smartphones. The same information could be used to provide individualized traffic diversion to avoid traffic jams or to direct motorists to free parking spaces. Data on road quality could also be collected to help municipalities to repair roads quickly.

Similarly, photos (i.e. camera sensor data) taken by people during or after snowstorms can be automatically analysed to prioritize cleaning the roads.

> Geographical Information Systems (GIS) play an important role in mobile crowdsensing as they combine spatial and geographical information with other sensors to create a new context!

The mobile crowdsensing model treats every person wearing a mobile device as a potential sensor node and forms a large sensor network that the entire population uses. Crowdsensing can be roughly divided into two main categories:

*   Participatory manual entry, in which the manual and active intervention of the participants is required for certain inputs.
*   Opportunistic automatic sampling, in which detection occurs in the background on the participants' smartphones.

In participatory perception, each survey directly involves the participant performing certain actions, for example, taking photos of places or events. Therefore, in this procedure, participants have the greatest control over when, where, and what to record by deciding which survey tasks to accept and complete With participatory capture, it is possible that the capture is performed automatically, but participants can control the time at which the capture can be performed, the release policies, and so on.

With opportunistic capture, the actual capture is performed automatically, and the participant is not involved in the capture activity. The smartphones (acquisition software makes the appropriate decisions and initiates the acquisition and transfer of acquisition data. This sensor model transfers work load from the participants to a central sensor detection system (or to an autonomous ad-hoc network of mobile devices) to determine when, where, and on which smartphones of a participant automatic sampling is performed to meet the requirements of the survey.

The system takes into account the social aspects of the participants when making decisions regarding the task planning for the recording. These aspects include the

*   Current location;
*   A possible next location;
*   The current activity;
*   Regular daily patterns and, if necessary,
*   a health status.

This type of detection is referred to as person-centred recognition. Examples of participatory manual surveys are:

*   Photo and video journalism (reporting by citizens)
*   Road transport registration
*   Data sharing in social networks

Examples of opportunistic automatic surveys are:

*   Behavioural and social behaviour assessment
*   Traffic and road transport recording
*   Indoor location with GPS and building maps

## Sensors

There are numerous sensors available in mobile and stationary devices. Table [2-1](#1_crowdsourcing.xhtml_sensorsover1) lists some of the most commonly used sensors.

| **Motion/Position sensors** | **Environmental sensors** | **Radios** | **Other hardware** |
| --- | --- | --- | --- |
| Accelerometer, Magnetometer, Gyroscope, Proximity sensor, Pedometer | Ambient light sensor, Barometer, Temperature sensor, Air humidity sensor, Radiation sensor | GPS, Bluetooth, Wi-Fi, Cellular | Microphone, Camera, Camera flash, Touch sensor, Fingerprint |

Table 2-1\. Classification of common sensors

Acceleration (ACC)

An accelerometer records the acceleration in three mutually perpendicular axes *x*, *y*, *z*. If the smartphone is placed horizontally on a table, an axis points to the vector of gravity (*g*). Accelerometers play an essential role in measuring physical activity. As a rule, they are used to detect the orientation of a smartphone, and today they are widely used for various game and activity detection applications.

Gyroscope (GYP)

Using a gyroscope, the orientation of the smartphone is measured by its angular momentum. It can measure the rate of change of the angle along a certain axis and is usually reliable to accurately detect short-term and sudden changes in orientation. Smartphones usually use a combination of an accelerometer and a gyroscope to calibrate each other, as well as reliably detect changes in orientation, locomotion states, etc.

GPS

This is one of the most used smartphone sensors. It calculates the position of the smartphone using satellites and their ground stations as a reference. The output is usually a (latitude, longitude, and altitude tuple), along with other information such as speed and direction. GPS can be switched off (on the smartphone) and is not always available.

Light

The light sensors are generally photo-diodes that measure the light intensity via an electric current. Light sensors are used to control the screen brightness under different lighting situations or to lock the touch screen when a user holds the phone to his ear.

The light sensor can also be paired with other sensors for intelligent services, e.g. for better localization by combining sound and phone position detection (e.g. in your pocket, on the table, or in his hand) together with the accelerometer.

External sensors

In addition to the internal smartphone sensors, the detection can also be carried out by external sensors, such as body-borne sensors in the health area for monitoring patients, sensors on bicycles for monitoring daily movements or cycling routes, as well as sensors in vehicles.

These external sensors are generally accessed through various wireless technologies (especially Bluetooth, which is compatible with many external sensor devices). These external sensors will become more important in the future as the number and complexity of sensor applications increase.

Smartphones have GPS, Bluetooth, WLAN, and GSM (mobile radio), which are usually used for location and communication functions.

These communication devices, in combination with other sensors, can improve the mobile detection of the user and make a great contribution to the location data of users. In particular, the GPS location is almost always marked with all the acquisition data to make the data more meaningful and contextual.

GSM

Global mobile radio network consisting of base stations which are usually located in the outdoor area (exceptions: radio network repeaters such as in trains). Range approx. 100-2000 m.

Wi-Fi

Local stationary radio network consisting of base stations (WLAN access points), which can be located both indoors and outdoors. Range approx. 10-100 m.

Bluetooth

Bluetooth is used to exchange data over short distances between two devices via radio transmissions in the ISM band of 2400-2480 MHz.

Bluetooth can therefore detect and connect to other Bluetooth-enabled peer devices in its environment. Due to the new Bluetooth LE (Low Energy) technology, smartphones can capture proximity data more efficiently. This property has been widely used in research to estimate and record real-time social conditions, e.g., estimating population density, calculating group formation, and deriving social contexts and contacts. Range approx. 1-10 m.

## Surveys

Surveys are a powerful tool to sense the world and, most of all, people. A survey is split into several tasks:

1.  Draft of a survey *S* (Survey) starts with the definition of the goal setting of goals.

2.  The goal is frequently to answer one or more higher-level questions (*Q*) in order to test a hypothesis (*H*).

| ![image-placeholder](images/ef7c7114-9575-40ac-ae73-61df572b0e77.png) | (2-7) |

Examples of questions are:

*   Do people feel safe on the street?
*   Has the employment situation in the country changed?
*   Do people use the Internet more and differently during the pandemic?

3.  The design of the survey is divided into further steps [K]:

So the survey design must consider fundamentaly the exact definition of the population to be studied (the target population). Further consideration of the indication of what needs to be measured (the variables ***X***) and what needs to be estimated (the **population characteristics**): Where the sample is selected (the sampling frame) as well as how the sample is selected (sample design and sample size).

4.  It is important to plan the survey carefully, taking into account the above steps!

The target population must be selected:

> The definition of the target audience of the survey is one of the first steps in the stage of survey design. The target population is the population of entities to be studied. It is also the population to which the results of the survey relate. The elements of the target audience are often people, households, or companies. So the population does not necessarily consist of people.

The target population is not exactly definable, especially in mobile crowdsensing! The target population consists of the quantity:

| ![image-placeholder](images/47e9239f-6cb5-48da-b866-474a828642ec.png) | (2-8) |

with *N* representing the population size and *e* representing individual entities

There are two types of variables that must be distinguished: target variables and auxiliary variables.

Target Variables

These variables measure the characteristics of the elements in the target population. Each participant from the target population takes part in the survey to answer one or more target variables *y*:

| ![image-placeholder](images/2588162a-6e9d-4882-80f9-eb7accb6b7c0.png) | (2-9) |

Example: *q*[i]="What is the income?" → *y*[1]=answer from participant 1, *y*[2]=answer participant 2, and so on.

Auxiliary Variables

Auxiliary variables often measure the background properties of the elements. Examples of a survey auxiliary variable among people could be gender, age, marital status, and region.

Such auxiliary variables can be useful to improve the accuracy of estimates. They also play a role in correcting the negative effects of non-responses. In addition, they provide opportunities for a more detailed analysis of the survey results:

| ![image-placeholder](images/b7b89304-af11-4f6f-9211-9c2e3f7aeef2.png) | (2-10) |

There are different population parameters. A population parameter is a numerical indicator, the value of which can be obtained only from the values *y*[1], *y*[2], ..., *y*[N] depends on a target variable *y*.

The population sum is defined by:

| ![image-placeholder](images/2abcd30f-9fde-4b75-8f57-1f6043e3f4d8.png) | (2-11) |

The population mean is given by:

| ![image-placeholder](images/3c89809d-1e99-423d-bf6f-56a1302fbb75.png) | (2-12) |

And finally, the population variance is given by:

| ![image-placeholder](images/2a318f0e-1b03-4a43-bc84-3ecf39c866fa.png) | (2-13) |

The survey window is related to under- and over-coverage in a survey, as shown in Fig. [2-3](#1_crowdsourcing.xhtml_samplingframe01).

![#samplingframe01](images/faf99f1a-d060-4736-b55c-34cfdfbbfc2d.png)Figure 2-3\. The problem of under- and over-coverage in a survey is addressed by the sampling frame [Bethlehem, 2009].

A sampling frame is a list of all elements in the target population *U*. For each item in the list, there must be information on how to contact this item, i.e., the collection of metadata. Contact information can include a person's name and address, phone number, and e-mail address. Such lists can exist in paper form (a card directory for the members of a club, a telephone directory) or digital form (a database containing a register of all companies). If such lists are not available, detailed geographical information and maps are sometimes used in mobile crowdsensing (GPS, Internet address-based).

Examples of survey windows can be found in the registers of the population registration office (or the list of entities de population). But also member lists in digital social networks and discussion forums.

A sub-coverage occurs when the target population contains elements that have no counterpart in the sample frame. Such elements can never be selected in the sample. An example of underfunding is the survey, in which the sample is selected from a population register. Illegal immigrants are part of the population, but they are never encountered in the sample frame. Another example is an online survey in which respondents are selected via the Internet. In this case, there is a shortage of coverage, since people do not have Internet access.

Under-coverage can have serious consequences: if the elements outside the sampling frame are systematically different from the elements in the sampling frame, estimates of population parameters can be greatly distorted. A complicating factor is that it is often not very easy to determine the presence of a under-coverage.

Over-coverage is the situation in which the sampling frame contains elements that do not belong to the target population. If such elements end up in the sample and their data is used in the analysis, estimates of population parameters may be influenced (falsified). It should be fairly easy to detect an overlap in the fields. This should be clear from the answers to the questions.

Disturbance variables and disturbance factors are related to problems that can arise if the units in the sample frame differ from those in the target population. A typical case is when one consists of addresses and the other of people. Further disturbance variables in a survey may be differences between the target population and the result window, e.g. due to different detection parameters. An example is a survey in which households should be selected with equal probabilities and the sample frame consists of people! This can happen if the sample is selected from a population register. Now, large families have a greater probability of selection than smaller families, since larger families have more people in the sample frame. In fact, the probability of choosing a family is proportional to the size of the family.

Representative surveys raise a number of questions: do they even exist? Is the press representative balanced? Who or what stands in for? The state institution as a representative of the population? Certainly not!

According to Kruskal and Mosteller, the following list of criteria applies:

1.  **General data recognition**. It does not mean much more than a general assurance without evidence that the data is in order. This meaning of "representative" is usually used by the media without explaining what it exactly means.

2.  **Lack of selective influence**. When choosing, neither consciously nor unconsciously, preference is given to elements or groups of elements.

3.  **Miniature model** of the population. The sample can be considered a scale model of the population. The sample has the same characteristics as the population. The sample proportions are similar to the population proportions in all respects.

4.  **Typical or ideal cases**. The sample consists of elements that are "typical" for the population. These are "representative elements". (Idea of the average man - **Average value**)

5.  Recording the **heterogeneity** of the population. **Variations** that exist in the population must also be encountered in the sample. So the sample should also contain **atypical elements**.

6.  **Meaning of terms**. The semantics of terms, misunderstandings, and ambiguity are relevant problems.

7.  **Statistics**. A special sampling method was used. A form of probability sampling must have been used that gives equal selection probabilities to each element in the population.

8.  **Good estimate**. All characteristics of the population and variability must be found again in the sample so that reliable estimates of population parameters can be calculated.

9.  **Quality**. Good enough for a specific purpose. Any sample that shows that a phenomenon that is believed to be very rare or absent occurs with a certain frequency is enough.

Randomization can be used to achieve the best possible statistical distribution in a survey. That means random selection of participants from a register. But: People are terrible randomizers! A randomizer is a theoretical concept. The perfect randomizer does not exist. However, there are devices that are close to a randomizer. And that's the end of digital (synthetic) random number generators! A digital (programmatic/mathematical) random number generator always generates the same sequence of *M* from *N* numbers that repeats!

Synthetic (pseudo) random generators calculate the next "random value" from the previous one, and there is an (internal) initialization (seed):

| ![image-placeholder](images/149b00ad-cd74-4502-8309-3da8df1ff2a7.png) | (2-14) |

The beginning of a pseudo-random series is determined by the *seed* value. And the same *seed* value results in the same sequence! A simple pseudo random generator that takes the samples from the course of a sine function:

```
[](#cb5-1)var start value = 1; var STEP = 10000;
[](#cb5-2)function random2 () {
[](#cb5-3)  var x = Math.sin(seed++) * STEP;
[](#cb5-4)  return x - Math.floor (x);
[](#cb5-5)}
```

## Simulation

In addition to the collection and processing of real-world data in a distributed context to derive system aggregate variables, simulation is another common methodology to test models and derive aggregate variables, too. Commonly, a simulation is a sandbox composed of numerous simple interacting entities with synthetic world data and (very) simplified behaviour models. The main goals of MCS using JAM are to deliver real-world sensor data for simulations and to include people in the simulation loop (human-in-the-loop simulation methodology).

## Issues

The reliability of crowdsensed data is a major challenge. The collected data transmitted by the subscribers is not always reliable, since they can transmit incorrect data for compensation without performing the actual task (like in surveys giving only joke answers), mostly driven by the anonymous Internet world. Therefore, it is important to validate the collected data. Furthermore, mobile device sensors are: A.) unreliable, and B.) inaccurate!

The reward is another challenge. It is not always economical for organizations (e.g. local or state government agencies or research communities) or individuals to provide financial compensation for any type of collection task that improves public services, supports the discovery of knowledge, or facilitates our everyday life.

Therefore, it is necessary to find inexpensive solutions to stimulate participants to conduct the sensory survey.

Energy requirements and battery run-time must be considered. In the development and implementation of mobile applications, energy consumption is an essential boundary condition that developers are confronted with.

Therefore, the main goals are to minimize the energy consumption of the mobile device, control the actions of the sensors, and suspend them if necessary.

Security and privacy have to be considered. Data protection is often a major hurdle for mobile data collection. If the sensing application uses third-party sensing services, then privacy is an important concern for the smartphone user, since it is difficult to trust the owners of the servers to which the sensor data is uploaded.

In addition, these servers can also be attacked by hackers. However, users feel safe as long as the captured data remains on their mobile device. However, without sending the sensor data to sensing services, the App developers may not be able to detect complex user activity. In addition, this can lead to high energy consumption or slow response time, even if it is possible on the phone. Therefore, the App developers need to weight the application's features for users and privacy.

# Platforms and Agents

After the introduction of agent and crowdsourcing methodologies, technological implementation aspects should be discussed in detail. Distributed agent-based computing (ABC) provides some advantages over traditional data processing using central services. Decentralized solving of problems, e.g., energy management [HAR05], can be solved more efficiently than centralized solving and can reduce communication and, optionally, computational complexity. The primary methodology to satisfy the requirements is local data processing using local data and global fusion of reduced and pre-processed information. The most important features of agent-based systems are their improved resilience and robustness against partial failures. The agent taxonomy addresses three areas: Languages, tools and algorithms, and platforms, as shown in Fig. [3-1](#2_platforms-and-agents.xhtml_agataxo). A thorough discussion can be found in [BAD11].

![#agataxo](images/54864867-1362-4eef-a1d1-5946ad1ca99b.png)Figure 3-1\. Taxonomy of agents

## Programming

To simplify the development and deployment of multi-agent systems in pervasive and ubiquitous applications connected by the Internet and deployed in strong heterogeneous environments, including the IoT and mobile networks, a unified, portable, and embeddable agent processing platform is required. To achieve scalability and high performance, the agent platform architecture must be closely designed with the agent programming model hand-in-hand. This book is based on several scientific publications from the past 10 years [10-28]. All publications address the deployment of multi-agent systems and use a programmable unified agent processing platform. Initially, the programmable agents were implemented in hardware using FPGA logic [BOS13A;BOS14A], then a software and hardware implementation of a FORTH stack processor with an extended agent-specific instruction set was introduced (AgentFORTH) [BOS15A;BOS15B]. Finally, the Web and cloud deployment gained focus, and the JavaScript Agent Machine (JAM) was invented. All different platforms are based on the same meta-level language, AAPL (Activity-based Agent Programming Language) [BOS18A]. All the agent programming languages used in our past work were dialects or sub-sets of AAPL. The aim of this technical report is to provide a detailed and rigorous description of JAM and the AgentJS programming language processed by JAM with a lot of background information and design patterns. JAM is used in a wide range of applications, including distributed machine learning [BOS17A], distributed meta-material (robotic) control [BOS19A] combined with simulation, mobile crowd sensing and social data mining and chatbots [BOS18C;BOS19B;BOS21A], distributed energy management [BOS18B], and distributed traffic control [BOS20A]. JAM is used in physical systems as well as in simulations (JAM is the simulator).

There are several design choices regarding agent modelling, the programming of agents, the agent processing architecture, and agent interaction. The design choices depend on the deployment of agents, the fields of application, and most importantly, the physical and digital environment the agents are situated in. The agent behaviour models can range from lower to higher abstraction levels with different expressiveness. The lower levels are closer to traditional data processing architectures and procedural or object-oriented programming, whereas the higher abstraction levels focus on knowledge representation, cognitive representation, ontologies, typically using declarative programming models and languages. The Belief-Desires-Intentions (BDI) architecture is a well-known and widely used agent behaviour model. But still, traditional imperative and procedural/object-oriented languages like Java are used to program agents.

## Virtual Machines

Agents commonly require a virtual machine (VM) acting as an agent processing platform (APP). On one hand, the APP has to isolate agents from each other, on the other hand, the APP has to provide sufficient agent communication and interaction. The APP must fulfil a core set of features:

1.  Independence and portability from the host platform;
2.  Code (containers) processing that is isolated and optionally multithreaded;
3.  Loose coupling of code processing to the underlying API (relieving hard API matching issues common in modular software);
4.  High performance and low memory requirements;
5.  Internet and web browser deployment;
6.  Support for IoT and embedded systems.

Java is a widely used programming language and VM. Popular agent frameworks, e.g., Jade [BEL05], rely on Java. But Java only satisfies requirements 1, 2, and partially 6\. Web deployment can be achieved in a nutshell only with the "native" Web programming language JavaScript. JavaScript (originally named ECMAScript) satisfies requirements 1, 3, 4a, 5, 6, and partially 2.

Exercise 3-1\. Virtual Machines

1.  What is the benefit of automatic memory management and garbage collection?
2.  What is the disadvantage of automatic memory management?
3.  Is a stack-based VM superior to register-based and RAM-based VMs?

## Mobile and Web Deployment

Today, a main part of human-machine interaction takes place via the Web Browser. Web browsers are increasingly used for computation and communication, e.g., text processing, Machine Learning, and video conferencing. From a practical point of view, agents should be directly implemented in JavaScript (JS), which is a well-regarded and widely used programming language. JS execution platforms are available for a very broad range of devices and operating systems, e.g., Intel x86/x64, Arm32, Linux, Windows, Solaris, macOS, FreeBSD, Android, IOS, and many more. Furthermore, the implementations of mobile agents directly in JS would benefit from existing high-performance JS VMs, e.g., Google's Chrome V8 or Mozilla's SpiderMonkey engines with Just-in-Time native code compilation (JIT). At a glance, JS is a very simple but highly dynamic language covering procedural, object-oriented, and functional concepts.

## Agent Processing and JavaScript

Even if a JIT-based VM is used, full code-to-text and text-to-code transformation is preserved at any execution time, including functions and data. This enables the capability of code morphing at run-time, a prerequisite for AAPL-based agents, which is used to store the current state of an agent process (e.g., prior to migration) and to modify the behaviour of an agent by applying a re-composition to the ATG by the agent itself. In contrast to Java and common Java-based agent frameworks (e.g., JADE), JS has a loose coupling to and low dependencies on the underlying execution platform. This is a significant advantage over the Java or C programming languages, which must be compiled before the code can be executed, and are very sensitive to API and library mismatches. JS considers functions as first-order values, enabling code reconfiguration on-the-fly like any other data modification using the built-in code evaluation function.

An agent can be considered as a computational unit situated in an environment and world, which performs computation, basically hidden from the environment, and interacts with the environment to exchange basically data. A common computer is specialized to the task of calculation, and interaction with other machines is encapsulated by calculation and performed traditionally by using messages. An agent behaviour can be reactive or proactive, and it has a social ability to communicate, cooperate, and negotiate with other agents. Pro-activeness is closely related to goal-directed behaviour including estimation and intentional capabilities.

Agents record information about an environment state *e*∈*E* and history *h*:*e*[0] → *e*[1] → *e*[2]... Let *I*=*S*×*D* be the set of all internal states of the agent consisting of the set of control states *S* related to activities and internal data *D*. An agent's decision-making process is based on this information. There is a perception function *see* that maps environmental states to perceptions, a *next* function that maps internal states and perceptions *p* ∈ *Per* to internal states (state transitions), and the action-selection function *action*, which maps internal states to actions *act* ∈ *Act*.

Actions of agents modify the environment, which is seen by the agent. Thus, the agent is part of the environment. Learning agents can improve their ability to solve a given task by considering the impact of their actions on the environment. After an action is performed, the agent gets feedback in the form of a reward: *r*(*t*)=*r*(*e*[t], *a*[t]). There are strategies π: *E*→*A* that map environment states on actions. The goal of learning is to find optimal strategies π^☆ that are a subset of *p*.

The JavaScript Agent Machine (JAM) is suitable for deployment in strong, heterogeneous, and mobile environments. JAM can be used for distributed computing as well as for simulation in a unified methodology and with a unified agent programming model, finally enabling mobile crowd sensing coupled to simulation.

In the following chapters, the fundamentals of the agent model, agent adaptivity, agent interaction, and the programming language AgentJS are introduced. After the introduction of the background, JAM itself and its architecture are described. An extended part is dedicated to the description of the AgentJS programming language. JAM is based on a modular library concept. Some application programs using the JAM core library are emphasized and described with examples. In addition, the performance metrics and a performance evaluation is discussed. The simulation environment SEJAM based on JAM is presented with an extended example project. Finally, the use-case of mobile crowd sensing coupled to simulation is presented. Methodological as well as technical design choices and issues are discussed.

The novelty of JAM is its simple and unified design, which provides a high degree of portability and a broad range of fields of application. The use of the widely established JavaScript programming language enables the programming of multi-agent systems (MAS) by beginners and non-experts alike. MAS can also be used in the Internet and Web domains, which are the most popular human-machine interfaces. All programming examples can be tested using JAM or the Web JAM laboratory, available on GitHub [JAM22] (distribution and source code). Only a Web browser and the node.js core binary [NOD22] are required.

# The Agent Model

An agent behaviour model can be partitioned into the following tasks, which must be reflected by an agent programming language model by providing suitable statements, types, and structures:

Computation

One of the main tasks and the basic action is the computation of output data from input data and stored data (history). Principally, functional and procedural (or object-oriented) programming models are suitable, but history incorporating computed data and storage is handled only by the procedural programming model consequently.

Communication

Communication as the main action serves two canonical goal tuples: (data exchange and synchronization), (interaction with the environment and with other agents). The latter goal tuple can be reduced to agent interaction only if the environment is handled by an agent, too. Communication between agents can link single agents to a multi-agent system, by using peer-to-peer or group communication paradigms.

Mobility

Mobility of agents increases the perception and interaction environment significantly. Mobile agents can migrate from one computing environment to another, finally continuing their processing there. The state of an agent, consisting of the control and data state, must be preserved on migration.

Reconfiguration

Traditional computing systems have fixed behaviour and an operational set specified at design time. Adaptation in the sense of behavioural reconfiguration of a system at run-time can significantly increase the reliability and efficiency of the tasks performed.

Replication

These are the methods to create new agents, either created from templates or by forking child agents, which inherit the behaviour and state of the parent agent, finally executing in parallel. Replication is one of the major agent behaviours for composing distributed computational and reactive systems.

Agents and Objects

Modern data processing is often modelled using object-oriented programming paradigms. But there is a significant difference between agents and objects. Objects are computational units encapsulating some state and are able to perform actions (by applying methods) and communicate, commonly by message passing. Objects are related to object-oriented programming and are not (or less) autonomous, in contrast to agents, and they are commonly immobile. The common object model has nothing in common with proactive and social behaviour. But agents can be implemented on top of the object model with methods acting on objects. The modification of the behaviour engine is basically not supported by the object programming model. Agents decide for themselves, in contrast to objects that require external computational units, like operating systems or users, for the decision-making process. Though object-oriented programming can be extended by parallel and concurrent processing (multi-threading), multi-agent systems are inherently multithreaded.

Exercise 4-1\. Agents

1.  Do you know a widely used agent code that utilizes code morphing and adaption? Nearly all people using computers had contact with these agents, mostly not aware of them.
2.  What is the benefit of replication, e.g., tree-like agent families, compared with a flat list of created agents started by a master program?
3.  What is the benefit of mobile code carrying data compared with non-mobile code and mobile data?
4.  What are the disadvantages of mobile code (remember question 1, too)?

## Activity-Transition Graphs

Agent models can be roughly divided into reactive and deliberative agent behaviour models. The agent's behaviour defines

*   a set of sensors and beliefs about the world (its data set), basically stored in the agent's body variables,
*   a set of events that it will respond to (signals, tuples, sensor changes),
*   a set of goals that it may desire to achieve, basically implemented by the set of activities, and
*   a set of plans that describe how it can handle the goals or events that may arise from activating activities.

The behaviour of an activity-based agent is characterized by an agent state, which is changed by activities. Activities perform perception, plan actions, and execute actions, modifying the control and data state of the agent. Activities and transitions between activities are represented by an activity-transition graph (ATG). The transitions start activities commonly dependent on the evaluation of agent data (body variables), representing the data state of the agent, shown in Fig. [4-1](#3_the-agent-model.xhtml_atg).

![#atg](images/0156b29d-d135-486b-8c57-dd1904066ba1.png)Figure 4-1\. Agent behaviour given by an Activity-Transition Graph and the interaction with the environment is performed by actions executed within activities

The agent's behaviour is modelled with a cyclic directed Activity-Transition graph (ATG). An activity *a* from a set of activities *a*∈*A* is an active (functional) node of this graph that performs actions, i.e., basically computation, communication, migration, and agent control. Transitions are directed active (functional) edges between nodes. A transition *t* from a set of transitions *t*∈*T* can be conditional and depends on the evaluation of the agent's state. The agent state is mainly contained in the set of private body variables and the control state represented by the *next* activity pointer.

An agent is created from a class constructor *AC*[i] defining the set of activities *A*, transitions *T*, body variables *V*, procedures *P*, and signal handlers *H*:

| ![image-placeholder](images/76686633-9831-4927-a16f-0e5485720756.png) | (4-1) |

An activity *a*[i] consists of sequential statements {*st*[j]} from a set of statements *st*[j]∈*ST*. The statement set can be different for different agents and can depend on environmental settings and constraints like the privilege level of the agent.

An agent can be suspended for waiting on events (including time events). Since not all programming languages and processing environments support process control flow blocking, only transition execution and activation can be blocked. That means, there may be only one blocking operation inside one activity, e.g., sleeping or waiting on communication data (see tuple space communication, Sec. [4-4-1](#3_the-agent-model.xhtml_sec_tuple_spaces_4)).

## Dynamic Activity Transition Graphs

The ATG introduced in the previous section provided dynamic control state and state transitions through the agent body variables (data state). But the ATG itself is static. One central feature of agents is their capability to adapt their behaviour, Although this can happen through conditional expressions and statements, the modification of the agent behaviour requires the ATG modification. Therefore, the agent's behaviour can be changed by changing the functional activity set and the transition set (modelling the control flow). Adaptivity of agents is provided by self-restructuring of the ATG by adding, changing, or removing activities and transitions, resulting in a dynamic ATG (DATG).

The basic operations applied to a DATG are reduction (R), restructuring (S), and extension (X):

| ![image-placeholder](images/50a73fef-8bf3-4d33-a319-29b543c739de.png) | (4-2) |

The basic transformation principles are shown in Fig. [4-2](#3_the-agent-model.xhtml_datg). The underlying mechanism of code modification (code morphing) depends on the concrete programming language and the VM that processes the agent platform. JavaScript supports direct code-text and text-code transformations and provides first-level code morphing. Besides agent adaptivity at run-time, ATG sub-classing can be used for the creation of child agents with reduced behaviour and finally reduced code size, improving the efficiency of agents.

![#datg](images/62f8be70-7a2e-4e01-bde0-4b054f952f53.png)Figure 4-2\. Dynamic ATG with modification of activities and/or transitions

## Composition of Multi-agent Systems

A multi-agent system (MAS) is composed of multiple agents that differ in their behaviour (ATG), control and data state (body variables), and their environmental context (e.g., spatial position). Each agent processing platform provides a dictionary of agent classes (ATG). Agents can be created at run-time from the class templates (constructor functions). Additionally, agents can fork copies of themselves, typically with a modified data state (parent-child agent groups). A forked child agent inherits the ATG (the code) and the current data state (body variables) from the parent agent. The forking supports divide and conquer methods, which are required for the composition of complex systems with simple cells.

JAM supports the creation of agents either by the platform or by running agents, forking of child agents by running agents, and forking of child agents only inheriting a sub-set of the parent ATG (sub-classing) and its set of body variables.

A simple example of a multi-class MAS should demonstrate the composition using generalized and specialized agents. It is assumed that there is a two-dimensional sensor network consisting of simple sensors. Each sensor node provides one sensor *s*(*x*,*y*) at a spatial position (*x*,*y*). The nodes are connected to their direct von-Neumann neighbourhood, as shown in Fig [4-3](#3_the-agent-model.xhtml_sensor_network_mas). Usually, sensor values are correlated within a spatially bounded region. The goal of the following MAS is to find the closed boundary of extended correlated regions posing significant sensor stimuli which can be distinguished from the neighbourhood. A single sporadic sensor activity not correlated with the surrounding neighbourhood should be distinguished from an extended correlated region by marking nodes near the boundary of the region, which is the feature to be detected (edge detector). The approach presented in this example should fulfil two goals [BOS16B]:

1.  Locate correlated sensor stimulus regions;
2.  Send sensor values to computational nodes at the network's edges.

The MAS consists of four agent classes:

1.  Node agent (responsible for sensor and event processing);
2.  Exploration agent (responsible to explorer node neighbourhood for finding a correlated sensor stimulus cluster using divide and conquer strategy);
3.  Event agent (notification of sensor events and delivery of sensor values);
4.  Computational agent (processing sensor data).

![#sensor_network_mas](images/18025d61-69cc-44b5-aef7-007cf2165c32.png)Figure 4-3\. The logical view of a sensor network with a two-dimensional mesh-grid topology (left) and examples of the population with different mobile and immobile agents (right): event delivery, exploration, node, and computational processing agents. The sensor network can contain missing or broken links between neighbouring nodes [BOS16B]

The behaviour and spatial interaction of sensor event distribution agents are shown in Fig. [4-4](#3_the-agent-model.xhtml_sensor_network_mas_sev). If there is a sensor stimulus event detected, event agents are sent out by the stimulated nodes. The event agent migrates along the node connections towards the outside of the network (first in one direction, and then in the perpendicular direction), finally reaching a computational node. Along the travelling path, the event agent collects sensor values of visited nodes, too. If there is no direct connection to the next neighbour in the desired direction, an alternative route is searched using a combination of backtracking and random walking.

The spatial feature detection is performed by the mobile exploration agent, which supports three main different behaviours: exploration, diffusion, and reproduction. The diffusion behaviour is used to move into a region, mainly limited by the lifetime of the agent, and to detect the feature, e.g., the region with increased mechanical distortion (more precisely, the edge of such an area), based on local sensors *s*. The detection of the feature enables the reproduction behaviour, which induces the agent to stay at the current node, setting a feature mark and sending out more exploration agents in the neighbourhood. The local stimuli *H*(*i*,*j*) for an exploration agent to mark a specific node with the coordinate (*i*,*j*) is given by

| ![image-placeholder](images/39372c72-96ff-49d5-80e5-698606d7e55c.png) | (4-3) |

The exploration agent, as shown in Fig. [4-5](#3_the-agent-model.xhtml_sensor_network_mas_sos), forks child agents that migrate to a neighbour node, collecting the local sensor value, evaluating a boundary condition (resulting in a binary *h* value), and dividing them into additional exploration child agents until the exploration boundary is reached. An exploration agent will return to its root node and deliver the accumulated feature value *h*.

The calculation of *H* at the current location (*i*,*j*) of the agent requires the sensor values within the square area (the region of interest, ROI) *R* around this location. If a sensor value *s* (*i*+*u*,*j*+*v*) with *i*,*j* ∈ {-*R*,...,*R*} is similar to the current position value *s* (the difference is less than the parameter), *H* is increased by one.

![#sensor_network_mas_sev](images/6cbfb218-7d32-4d11-94fe-e8f248b819f6.png)Figure 4-4\. (Top) ATG behaviour model of the event agent (Bottom) Sensor data distribution with event (green) and preprocessing agents (blue): A sensor node that detects a significant change in the sensor values creates event agents, which are sent in all four directions to the network boundary (pre-computation nodes)![#sensor_network_mas_sos](images/60740ceb-c153-4466-922f-54b9e8fecbe3.png)Figure 4-5\. (Top) ATG behaviour model of the explorer and child agent class branching from the percept activity (Bottom) Feature marking of stimulated sensor clusters by using explorer agents investigating the neighbourhood of their current position using forked child agents. On successful feature detection, explorer agents are replicated, otherwise they diffuse to the neighbourhood to find features

## Interaction of Agents

Agents are computational processes that are loosely coupled to the underlying processing platform, posing low dependence on the programming interface. As a consequence, agents are weakly coupled to each other, too. Communication methods that satisfy the weak coupling paradigm are generative tuple spaces [GEL85] and event-based signals, shown in Fig. [4-6](#3_the-agent-model.xhtml_agcomm).

![#agcomm](images/719b533b-aa83-4035-8541-6bd43b368150.png)Figure 4-6\. Data-driven agent communication using tuple spaces and agent-driven communication using addressed signals

### Tuple Spaces

A tuple space is basically a database that supports producer and consumer operations. A producer process can insert new data by using tuple requests. A tuple is an ad-hoc collection of single data elements, similar to an array. In contrast to arrays, the type signature of a tuple can be heterogeneous, i.e., each element can be any data type, e.g., scalar values like numbers or Boolean values, or aggregated values like arrays or record structures. A tuple *t* is specified by the number of elements (arity) and the type signature of the tuple:

| ![image-placeholder](images/e4ce9d6d-fb73-4664-b44b-a36d2720acf8.png) | (4-4) |

A consumer process can extract tuples (either by removing them or by getting a copy) by using patterns (*p*). A pattern is a tuple that consists of actual and formal values. The pattern is applied to all tuples in the space to find matching results. Formal parameters match all data values.

Tuple space communication is anonymous and generative. Producer and consumer processes do not know each other, and a tuple can have a longer lifetime than a producer process. Tuple space communication poses a lot of advantages, but also disadvantages. The main disadvantage is the initially unlimited lifetime of a tuple, resulting in the growth and overflow of the tuple space over time. To avoid tuple space flooding, tuples can be assigned a lifetime, too. Either explicitly by the producer process or (and) by the tuple space service. Finding the right lifetime is critical since a too short lifetime misses producer-consumer communication (if the consumer comes too late) or still overflows the tuple space if the lifetime is too large. Therefore, tuple space communication is not guaranteed, which must be considered by the agent behaviour.

Aside from the producing operation *out*, there are two distinct consuming operations *rd* and *inp*. The input operation removes exactly one matching tuple from the space (atomically), whereas the read operation only returns a copy of the tuple. The consumer operations are synchronized and therefore can block the process control flow of the requesting process (blocking of control flow until a matching tuple is inserted by another process or a timeout occurs).

### Signals

Signals are simple messages consisting of a signal identifier (number or string name) and can be exchanged by agents. The destination agent must be known (in contrast to tuple space communication). In contrast to uni-cast signals with one specific destination, multicast signals can be sent to a group of agents (previously defined), or broadcast signals that can be sent to all reachable agents. Broadcasting is typically limited to agents within a given communication range (same node) and limited to a specific agent class.

Exercise 4-2\. Communication

1.  Can race conditions occur if there are two or more agents exchanging data via the tuple space?
2.  What is the major difficulty in anonymous and generative agent communication using tuples?
3.  How are tuple spaces related to temporal logic?
4.  There is a set of agents (for example, *N* = 4). One agent is a master and a data source. The other *N*-1 agents are workers and data consumers. They should process tasks assigned by the worker using a subset of the input data and map them to output data. Data transfer of input data from the master agent to worker agents, synchronisation, and data transfer from worker agents to the master agent should be performed via the tuple space. Write a master and worker program in pseudo-notation that implements the master-worker system.

## Software Implementations

The DATG approach can be implemented with a wide variety of programming languages and computer systems, initially implemented with a modified and advanced version of the FORTH programming language and executed on a parallel stack processor system [BOS15A]. The initial work had a focus on low-resource embedded systems. To enable the deployment in Web, IoT, and Cloud Internet environments, a successor of this successful low-resource implementation is based on the transition from a customized stack-based to a widely used JavaScript programming language with the AgentJS dialect, discussed in the next section.

## AgentJS

From the programming language point of view, AgentJS is pure JavaScript and conforms fully to the ES2015 standard. But there is a slightly different operational semantic and there are some restrictions. AgentJS describes agent objects and agent constructor functions. In contrast to generic JS classes and objects, there are no free variables and references to higher scopes are allowed. A compilation process will eliminate all free and out-of-scope references and bind the `this` variable to the created agent object. The basic template of an agent constructor function conforming to AgentJS is shown in Def. [4-1](#3_the-agent-model.xhtml_acf).

```
[](#cb6-1) 1: function acf(p1?,p2?,..) {
[](#cb6-2) 2: ┌
[](#cb6-3) 3: │  this.$bodyvar = ε
[](#cb6-4) 4: └
[](#cb6-5) 5: ┌  this.act = {
[](#cb6-6) 6: │    $act : () => {}
[](#cb6-7) 7: └  }
[](#cb6-8) 8: ┌  this.trans = {
[](#cb6-9) 9: │    $act : string | function : () → string
[](#cb6-10)10: └  }
[](#cb6-11)11: ┌  this.on? = {
[](#cb6-12)12: │    $signal : (arg,from) => {}
[](#cb6-13)13: └  }
[](#cb6-14)14: ┌
[](#cb6-15)15: │  this.next = string
[](#cb6-16)16: └
[](#cb6-17)17: }
[](#cb6-18)18: 
[](#cb6-19)19: function acf(p) : parameter:* → agent object
[](#cb6-20)20: 
[](#cb6-21)21: type agent: { $var:*, 
[](#cb6-22)22:                act : {function}, 
[](#cb6-23)23:                trans : {function}, 
[](#cb6-24)24:                on?: {function}, 
[](#cb6-25)25:                next:string|object  }
```

Definition 4-1\. Basic structure of an agent class constructor function

The constructor function defines body variables (must be initialized, at least with the `null` object), the activity object containing all activity functions (or lambda expressions using arrow functions), the transition object with attribute names equal to the previously defined activities, specifying the outgoing activity for a transition, an optional signal handler object, and finally the control state variable *next*, which must point to a valid start activity. A transition section entry is either a static rule providing a fixed next activity (name string or name identifier), or a dynamic transition evaluation function that can return different next activities. Depending on the source of the agent constructor function, next activities can be a string or identifier (in the agent context, all activities are accessible via an identifier related to a variable containing the name string), as shown in the following code:

* * *

```
[](#cb7-1)this.trans = {
[](#cb7-2)  // unconditional transition
[](#cb7-3)  start : 'percept',  // string
[](#cb7-4)  percept : () =>  {
[](#cb7-5)    // conditional transition
[](#cb7-6)    return this.destination?move:goback;
[](#cb7-7)  },
[](#cb7-8)  move : deliver, // identifier
[](#cb7-9)}
```

* * *

Note that a transition rule should not return the undefined or `null` object if there is currently no succeeding activity, which should result in control flow blocking. Instead, activity flow control should be accomplished through the use of *sleep* and *wakeup* statement pairs.

An agent constructor function describes parametrisable agent objects consisting of private body variables, activity functions, transition functions, and optionally event handler functions. The mandatory *next* attribute points to the next activity to be executed and must be initially set to the start activity (*next* can be considered as the agent program counter). The *next* attribute is used to preserve the agent's control state on forking or migration, too. A transition attribute from the *trans* section consists of the start activity name (that must be defined in the *act* section) and a destination activity (also defined in the *act* section). The transition can be unconditional (only one static destination activity is possible) or conditional (more than one destination activity is possible). Conditional transitions require a resolution function to return the name of the destination activity. If the agent constructor function is compiled from a string text, activity names can be provided as identifiers, otherwise they must be handled as strings.

Agent activity, transition, and handler functions are always called in the agent object context (the `this` variable always points to the agent object). All functions can use the entire operational AIOS function set with respect to the current privilege level of the agent. Blocking operations may not be chained, nested, or called inside loops. Only one blocking operation in an activity function is allowed. Blocking only inhibits the activity transition of an agent.

Agent objects are instantiated from the agent constructor function with an individual set of parameters {*p*[i]}. As there are no free variables, the constructor function parameters must be assigned directly to body variables. An example of an agent constructor function for a simple hello world agent is shown in Ex. [4-1](#3_the-agent-model.xhtml_exacf1). All body variables must be initialized by the assignment of a static or dynamic value from the function parameters, and initially undefined variables require the assignment of the null object.

```
[](#cb8-1) 1: function hello(config) {
[](#cb8-2) 2:   this.message = config.message;
[](#cb8-3) 3:   this.time = 0;
[](#cb8-4) 4:   this.delay = config.delay;
[](#cb8-5) 5:   this.data = null;
[](#cb8-6) 6:   this.act = {
[](#cb8-7) 7:     start : () => {
[](#cb8-8) 8:       log('Hello world!');
[](#cb8-9) 9:       this.time=time();
[](#cb8-10)10:       sleep(this.delay);
[](#cb8-11)11:     },
[](#cb8-12)12:     talk : () => {
[](#cb8-13)13:       log(this.message);
[](#cb8-14)14:       log('I sleep '+(time()-this.time)+' ms');
[](#cb8-15)15:       this.time=time();
[](#cb8-16)16:       sleep(random(10,100));
[](#cb8-17)17:     },
[](#cb8-18)18:     end : () => {
[](#cb8-19)19:       log('I am terminating...')
[](#cb8-20)20:       kill()
[](#cb8-21)21:     }
[](#cb8-22)22:   }
[](#cb8-23)23:   this.trans = {
[](#cb8-24)24:     start : talk,
[](#cb8-25)25:     talk  : () => {
[](#cb8-26)26:       return random(0,100)<50?"end":"talk"
[](#cb8-27)27:     },
[](#cb8-28)28:   }
[](#cb8-29)29:   this.next = "start"
[](#cb8-30)30: }
```

Example 4-1\. An example of an AgentJS constructor function (defining agent class "hello")Exercise 4-3\. Agent Programming

1.  Name the essential characteristics of reactive and event-based agents.
2.  Compare signal messaging and tuple spaces: What are the differences, benefits, and possible issues (flaws)?
3.  The ATG is composed of activities executing actions. Traditional software is composed of functions and classes (objects). What is the purpose of functions in programs? What is the purpose of the activities of agents? What should an activity of the agent achieve? How should the activities be partitioned and named?
4.  Assume a simple heater control agent. The agent samples a temperature sensor *t* (on a regular or ad hoc basis) and modifies the heating power *p* iteratively using a proportional control approach (P controller), with the goal of minimizing the error *err*=*t*-*t*[0] for a given temperature *t*[0]. Describe a minimal ATG that implements a reactive control loop. There are timer and sensor change (delta) events available.

# JavaScript Agent Machine

The JavaScript Agent Machine (JAM) is the central part of the multi-agent system framework addressed in this work. In addition to the platform features discussed in the introduction, an agent process platform must satisfy the following constraints from a software design perspective:

1.  Portability with low hardware and operating system dependencies;
2.  Possibility for deployment on low-resource platforms;
3.  Embeddable in any software application, including Web pages;
4.  Scalability with respect to agent number and computational agent complexity.

JAM is entirely programmed in JavaScript and satisfies the first and third constraints immediately. The satisfaction of the second and fourth constraints depends on the underlying JavaScript Virtual Machine (JVM). But even the node.js JVM can be deployed on embedded and mobile systems like smartphones (typically requiring at least 1000 MIPS CPU power and 50 MB main memory for satisfying responsiveness and scalability).

## Agent Worlds: Virtual and Physical Nodes

JAM provides a physical platform for agent processing. A physical JAM node includes the following components and capabilities:

*   Agent process scheduler;
*   Tuple space databases;
*   Protection and security;
*   Agent management and modification;
*   Communication including signal and agent mobility.

Besides the physical node, there is a virtualization layer providing virtual nodes all processed by the physical node. Each JAM instance has at least one virtual node and agents are associated with virtual nodes. The virtual node concept is used for simulation, discussed later. AMP communication ports (and links) are always attached to virtual nodes. This enables virtual networks with virtual circuit links inside a physical node world, as shown in Fig. [5-1](#4_javascript-agent-machine.xhtml_worlds). All virtual nodes have individual tuple spaces and process tables, but share the same agent process agent scheduler and AIOS. Therefore, virtual worlds do not provide speed-up by parallelization, in contrast, to JAM clusters, which can be easily created by the *jamsh* program. In a JAM cluster, each JAM node is processed by its own VM instance.

![#worlds](images/699e0ea8-5c9e-4fd2-9ad6-ac8b19a5ca60.png)Figure 5-1\. Virtual and physical nodes

## Agent Communication

Agents are loosely coupled processes that interact, typically by messaging. In JAM, agents use tuple spaces and signals for inter-agent communication and, in some cases, agent-platform communication. Tuple spaces provide connectionless, anonymous, non-addressed, and generative communication, whereas signals provide message-based, addressed communication between agents. Tuple space communication does not require that the agents know each other, in contrast, to signals. An agent is identified in JAM by a node-unique randomly generated identifier string (typically consisting of eight characters).

Agents can exchange data tuples if they are processed by the same physical or virtual node (local tuple space scope). Each JAM virtual node (each physical node has at least one virtual node) provides a tuple space for tuple of arity 1 up to 10 (the upper number of tuple elements can be extended by the host application). Each single tuple arity is handled independently since tuples can be only accessed by patterns that must have the same number of elements (arity). The node tuple spaces can be accessed by the host application (embedding JAM or the stand-alone JAM shell), too. The host application can provide tuple consumer handlers that are called by the tuple space API if a new tuple is inserted. Read requests can be passed to producer handler that can create new tuples on request.

Signals were originally used between agents processed on the same (virtual) node. But signals can be propagated to remote nodes, too (or other virtual nodes of a physical node), if, and only if, there is a migration trace between the sender and receiver agents. That means, two agents can exchange signals remotely if they were processed on the same node some time ago. This is always true for parent-child groups. If an agent leaves a node on migration, the current node will remember the agent id and the destination node with the outgoing network link in a temporary cache table. Each time a signal is propagated along this path, the cache table is updated. A garbage collector will clean up traces if they have not been used for some time.

Tuple spaces of remote linked nodes can be accessed by using special tuple request signals, used basically for tuple duplication or forwarding.

## Agent Input-Output System (AIOS)

The AIOS is the central bridge between the JAM platform or host applications and the agent processes, shown in Fig. [5-2](#4_javascript-agent-machine.xhtml_aios1). The AIOS provides an advanced agent scheduler that is used to schedule all agents of a physical node. It is used for the SEJAM simulator, too. The scheduler performs signal and timer handling, activates agents, call activity and transition functions, and performs error handling, as introduced in Sec. [5-4](#4_javascript-agent-machine.xhtml_sec_agent_scheduling_and_check_pointing_6).

The AIOS provides sets of operations and functions that can be accessed by an agent depending on the privilege level of the agent (AgentJS API). Each privilege level uses its own set of operations. For example, a level zero agent cannot access tuple spaces and cannot migrate. Level three agents are immobile and therefore do not have a `moveto` function in their operational set either.

![#aios1](images/ee5d13de-2a60-4b25-8e20-8c5b0621d247.png)Figure 5-2\. Basic AIOS architecture providing a bridge for the agent, host platform, and modules API

The operations set can be defined formaly:

| ![image-placeholder](images/61a586c7-2a97-4fac-afeb-d9f8b1e51eac.png) | (5-1) |

The auxiliary set provides access to helper modules, e.g., Machine Learning or database access (SQL). The host application can extend each AIOS op-level set by additional functions and objects. For example, the simulator SEJAM will extend the agent op set by simulation specific operations.

### Code and Data Serialization with JSON+ and JSOB Representation

A textual representation is used as a serialized data and code interchange format, which is a prerequisite for data and code processing in distributed strong heterogeneous platform and network environments, mixing big-and little-endian machines, different data word sizes, and data coding. Although, byte-code based interchange formats are widely used, they require strict compliance with the coding between a sender and a receiver. At any time, a JS object can be converted to text in JSON format at run-time. Originally, JSON was introduced for the portable exchange of JS data objects in a textual representation only, being much more compact and easier to interpret than XML. But JSON is limited to data elements, only. References to deeper objects (records or arrays) are always resolved and expanded. Therefore, JSON cannot represent recursive data structures. Although, JS considers functions as values of first order, traditional JSON cannot represent and encode functions. For this reason, the JSON+ format was introduced, which supports function encoding as well as special data objects like compact typed arrays and buffers.

A JAM/AgentJS agent is basically a JS object containing data (values, data objects, arrays) and functions, representing the agent activities and transitions of the ATG. This requires an extended JSON text formatter and parser supporting functions, which were introduced in JAM. An entire agent process can be converted at any time to the textual representation (JSON+) preserving its current control and data state, which can be exchanged by different network and agent platform nodes, and that is finally back converted to JS code.

Textually encoded functions and binary buffers use a base64 code and a tag prefix (e.g., `_PxEnUf_` for function code). The only existing limitations are circular (self) references inside an object, which still cannot be handled, but are not a real restriction.

Transferring text instead of binary code results in a significantly increased communication cost on agent migration, but the text can be compressed, reducing the size significantly (experiments showed that LZ compressing reduces the JSON+ text size and hence the communication costs about 5-6 times). Embedded devices can utilize hardware compressor modules, e.g., using FPGA-based coprocessors, maximizing communication efficiency without additional CPU costs.

In addition to the JSON+ format, a customized JavaScript Object (JSOB) format is supported, too. JSOB is a textual representation of a JS object, too, but does not encode functions and is more compact, as shown in Ex. [5-1](#4_javascript-agent-machine.xhtml_jsonobex).

```
ag = {
  x:1, y:2, z:[10,20,30],
  act : {
    main : () => { this.x++ },
    end  : () => { kill() }
  },
  trans : {
    main : end,
  }
  next : main
}
───── JSON+.serialize(ag) ─────
{"x":1,"y":2,"z":[10,20,30],"act":
{"main":"_PxEnUf_ZnVuY3Rpb24gKCkgeyB0aGlzLngrKyB9",
"end":"_PxEnUf_ZnVuY3Rpb24gKCkgeyBraWxsKCkgfQ=="},
"trans":{"main":"end"},"next":"main"}
───── JSOB.serialize(ag) ─────
{'x':1,'y':2,'z':[10,20,30],'act':
{'main':()=>{ this.x++ },'end':
()=>{ kill() }},'trans':
{'main':"end"},'next':"main"}
```

Example 5-1\. Examples of agent object serialization using JSON+ or JSOB format

### The AIOS Sandbox Environment

The stability and robustness of the agent processing platform is one major challenge in the design. Agents can be considered as autonomous or semi-autonomous processes and execution units. But this autonomy requires strictly bound and safe platform environments for the execution of agent processes from arbitrary sources, and the strict isolation of agent processes from each other. At least inference by accident must be excluded. An agent platform must be capable of executing hundreds or thousands of different agent processes. Although, there are extension modules for some JS VMs (e.g., Web worker processes) allowing the execution of a JS program in a separate host process (or thread), these coarse-grained methods are not portable, and they create significant overhead in time and memory space. This is related to the start-up time of threads and the fact that each thread creates a new VM instance with limited inter-process communication, as required by the AIOS.

Unfortunately, JS has a very limited and coarse-grained scope context hierarchy, essentially limited to function closures and the *this* object (in contrast to Lua, which supports function execution in a freely defined and limited scope), and with a single global space shared by all imported modules and evaluated code.This limitation initially prohibits the safe and interference-free execution of multiple agent processes within one JS VM instance. To satisfy the inference constraint, the JS `with (mask) {code}` statement can be used to execute the code with an overlaid name space given by the mask object argument. Typically, used to map bound variables onto free variables for a limited code scope, here the mask is extended by all global variable names assigned to null value and function name attributes overlaying the global reference scope.

Encapsulating the agent object and its function processing inside the `with` statement can only mask out globally visible objects and functions, but not free variables and functions visible on code evaluation. To put it another way, each agent instantiation from an agent class constructor function necessitates full code-text-code serialization and de-serialization in a masked context, which results in high computational costs if applied to each agent. A more suitable approach is the sandbox-restriction application to the agent constructor function itself (one time), i.e., the agent is created from a constructor function that was created in a masked environment that masks all undesired global and free variables by null references and by code-text-code serialization of the constructor function without any side effects. The first implementation choices using the `with` statement are shown in Alg. [5-1](#4_javascript-agent-machine.xhtml_sandboxwith).

```
[](#cb10-1) 1: mask    = ∀ $key ∈ global { $key:null }
[](#cb10-2) 2: context = ∀ $key ∈ Core { $key:global($key) } ∪ 
[](#cb10-3) 3:           ∀ $key ∈ AIOS(level) { $key:AIOS($key) } 
[](#cb10-4) 4: maskAndContext = mask ∪ context
[](#cb10-5) 5: type sandBox1: object×string → constructor function
[](#cb10-6) 6: function sandBox1(maskAndContext, acf) {
[](#cb10-7) 7:   var F
[](#cb10-8) 8:   eval('with(maskAndContext) { "use strict"; F='
[](#cb10-9) 9:               + acf + ' }');
[](#cb10-10)10:   return F
[](#cb10-11)11: }
[](#cb10-12)12: type sandBox2: object×object×string → 
[](#cb10-13)13:                constructor function
[](#cb10-14)14: function sandBox2 (mask, context, acf) {
[](#cb10-15)15:   var _mask = keys(mask).join(',');
[](#cb10-16)16:   var F = 
[](#cb10-17)17:      new Function(_mask,
[](#cb10-18)18:                   '"use strict"; with(this) { f=('+
[](#cb10-19)19:                   acf+').bind(this)} return f')
[](#cb10-20)20:                  .bind(context);
[](#cb10-21)21:   return F();
[](#cb10-22)22: }
[](#cb10-23)23: var acbound1 = sandBox1(context,acf),
[](#cb10-24)24:     acbound2 = sandBox2(mask,context,acf);
[](#cb10-25)25: var ag1 = new acbound1(parameters),
[](#cb10-26)26:     ag2 = new acbound2(parameters);
```

Algorithm 5-1\. The first two implementation choices for the sandbox restrictions of the agent constructor function use the `with` scope statement compiled by the generic `eval` statement or by using the `Function` constructor. The agent constructor function acf must be serialized to text before applying the sandbox to remove any free bindings.

The usage of the `with` statement is deprecated and can introduce a significant performance degradation of the executed agent code (each variable or function access requires the traversal of a long mask table). Another approach to transforming the non-context-constrained agent class constructor function to the scoped sandbox-restricted constructor function using the `Function` constructor with some expression magic and by splitting the agent name space into a masked global environment (*mask*) and the AIOS object *context* is shown in Alg. [5-2](#4_javascript-agent-machine.xhtml_sandboxfun). This approach avoids the usage of the `with` statement. Instead, the masked variable attributes are passed as function parameters to the scope-restricted agent constructor function evaluation and the desired context variables by a bind process.

For each AIOS privilege level and for each agent class *ac* there is one sandbox-restricted agent constructor function.

```
[](#cb11-1) 1: mask    = ∀ $key ∈ global { $key:null }
[](#cb11-2) 2: context = ∀ $key ∈ AIOS(level) { $key:AIOS($key) } ∪ 
[](#cb11-3) 3:           ∀ $key ∈ Core { $key:global($key) }
[](#cb11-4) 4: type sandBox3: object×object×string → 
[](#cb11-5) 5:                constructor function
[](#cb11-6) 6: function sandBox3 (mask, context, acf) {
[](#cb11-7) 7:  var pars = keys(context).concat(keys(mask)),
[](#cb11-8) 8:      args = pars.map(function (key) { 
[](#cb11-9) 9:         return context[key] });
[](#cb11-10)10:  pars.push('return '+acf);
[](#cb11-11)11:  var foo = new (
[](#cb11-12)12:    Function.prototype.bind.apply(
[](#cb11-13)13:      Function,
[](#cb11-14)14:      pars
[](#cb11-15)15:    ));
[](#cb11-16)16:  return foo.apply(this,args);
[](#cb11-17)17: }
```

Algorithm 5-2\. The third implementation choice for the agent constructor sandbox application uses the `Function` constructor statement only. The mask is passed via the function argument array.

The masking approach cannot limit the name space scope (scopes are chained, and higher scopes like the global one are still visible) of the agent process and its functions, but it can be used to override higher scope levels and global name qualifiers, and to invalidate references to free variables and functions without compromising other agent processes or the JAM modules. There is still one major vulnerability introduced by extendible objects, e.g., the *Array* object.

Finally, the execution of an agent process is the execution of a function with a strictly limited operational name space and no bindings to external and free variables and functions. Core objects like *Array* and *String* are replaced by non-expandable proxy versions. Migration of agents is performed by object-to-text serialization and text-to-object de-serialization. To ensure a sandbox-restricted agent object after migration (no constructor function is involved), the JSON+ parsing and evaluation is always performed inside the `with` statement with a mask environment only providing a selected AIOS set of objects and functions, depending on the agent privilege role, discussed in Section [5-6](#4_javascript-agent-machine.xhtml_sec_agent_roles_8). The creation of a new agent (from a fork or migration operation) will always first stringify the agent object, and finally evaluate a sandbox-restricted agent object free of any free and global object references, which can be executed by the AIOS agent scheduler without any interference with the platform and other agents. This approach protects the agent execution and JAM at least against failures by accident by using common JS coding styles. The capability of full intrusion protection depends on the JS VM environment itself.

Although, JS supports control flow scheduling by using asynchronous functions (defined with the *async* keyword) and the *await* statement operator, the usage must be prevented since it can create background functions beyond the control of the AIOS (as well as internal background processing using built-in *setTimeout* or *setInterval* functions). AIOS rejects code using asynchronous functions or the await statement operator, and the timer control functions are masked out. The only allowed scheduling point is at the end of an activity function or an element of a scheduling block function.

### Anonymous Functions and Lambda Expressions

The ATG is composed of anonymous functions. JS supports lambda expressions since the ES6 standard, too, in the form of arrow functions. Arrow functions are much more comfortable in programming, and beginners, in particular, prefer them over anonymous functions. But in contrast to other programming languages, anonymous (nameless) functions and arrow functions are not the same in JS. A JS function supports the `this` variable inherently, i.e., each function has its own `this` object variable. Arrow functions do not have their own `this` object, instead referencing the current `this` object of the surrounding context if they are created (compiled). This is a show-stopper on the first level for AgentJS since all first-and second-level functions reference the agent `this` (self) object. This is achieved by dynamic binding of the agent self-reference on function calls to the respective agent functions. This is not possible with arrow functions (they ignore any *bind* or *call* mapping of `this`). All arrow functions must be bound to the agent self-object reference on creation. If an agent object is instantiated from a constructor function, all arrow functions automatically reference the agent object via the `this` variable. But after text serialization and deserialization (e.g., on process migration), this is a chicken-and-egg problem. Typically, the `eval` function is used to compile functions from text (or, using the *Function* constructor). But when an arrow function is created, the agent object itself, which is still under construction, is not yet available! Instead, an initially empty agent object must be used as `this` reference that can be bound by arrow functions, finally getting the content from the temporary agent object created by the `eval` function application, shown in Alg. [5-3](#4_javascript-agent-machine.xhtml_tocodearrowfuncsafe).

```
[](#cb12-1) 1: function toCode(source,mask) {
[](#cb12-2) 2:   // arrow functions do not have a this variable
[](#cb12-3) 3:   // they are bound to this in the current context!
[](#cb12-4) 4:   // need a wrapper function and a temporary 
[](#cb12-5) 5:   // this object
[](#cb12-6) 6:   var self={},temp;
[](#cb12-7) 7:   function evalCode() {
[](#cb12-8) 8:     var code;
[](#cb12-9) 9:     try {
[](#cb12-10)10:       // execute script in private context
[](#cb12-11)11:       with (mask) {
[](#cb12-12)12:         eval('"use strict"; code = '+source);
[](#cb12-13)13:       }
[](#cb12-14)14:     } catch (e) { console.log(e) };
[](#cb12-15)15:     return code;
[](#cb12-16)16:   }
[](#cb12-17)17:   // bind evalCode to empty self == this object
[](#cb12-18)18:   temp = evalCode.call(self);
[](#cb12-19)19:   // arrow functions are now bound to self, 
[](#cb12-20)20:   // update self with temp. agent object 
[](#cb12-21)21:   // first-level attributes
[](#cb12-22)22:   self=Object.assign(self,temp);
[](#cb12-23)23:   return self; 
[](#cb12-24)24: }
```

Algorithm 5-3\. Arrow function safe agent deserialization from JSOB or expanded JSON+ format with a masked context

## Agent Scheduling and Check-pointing

JS has a strictly single-threaded execution model with one main thread, and even by using asynchronous callbacks, these callbacks are executed only if the main thread (or loop) terminates, i.e., leaves the control path. This is the second hard limitation for the execution of multiple agent processes within one JS JAM platform instance. The JAM requires strict control over agents at any time. Agents can migrate between JAM nodes, e.g., those connected by the Internet. No agent may compromise a JAM node or affect the processing of other agents, including unlimited run-time. Scheduling in modern JavaScript VMs can be easily achieved by using asynchronous functions with promises and executing them by using `await` statements. But this attractive and simple-to-use control enables the scheduling of agents with a time-multiplexed execution model. This method violates the requirement of full agent process control by the JAM. An example should demonstrate this, creating a zombie process. Assume one agent wants to sleep (within in activity function) for a specific amount of time with a control path schedule, shown in Ex. [5-2](#4_javascript-agent-machine.xhtml_asyncawait). Instead, an AIOS sleep function is used to push the agent processing onto a wait queue, where it is finally woken up by the AIOS scheduler by performing the transition to the next activity. But this simulated kind of agent process control limits the number of blocking operations within one activity to one (and blocking occurs only after the activity function returns). The calling of blocking operations in loops requires microscheduling blocks and loop transformations.

If the agent waits for the fulfilment of the promise by the background timer, the AIOS scheduler could execute another agent. But if in any case, the sleeping agent was terminated, e.g., explicitly by a kill operation or due to resource violation, the sleeping agent process persists (there is no way to resume sleeping background processes) and a zombie process is created that can continue. For this reason, any promise construction and asynchronous functions must be masked out by the sandbox-restricted context.

```
[](#cb13-1) 1: $act : async () => {
[](#cb13-2) 2:   ...
[](#cb13-3) 3: ×  await asleep(tmo);
[](#cb13-4) 4:   ...
[](#cb13-5) 5: }
[](#cb13-6) 6: async function asleep(tmo) {
[](#cb13-7) 7:   return new Promise((resolve,reject) => {
[](#cb13-8) 8:      setTimeout(resolve,tmo);
[](#cb13-9) 9:   }
[](#cb13-10)10: }
[](#cb13-11)11: $act : () => {
[](#cb13-12)12:   ...
[](#cb13-13)13:   sleep(tmo) 
[](#cb13-14)14:   // Scheduler do:
[](#cb13-15)15:   //   now: → agent.blocked → 
[](#cb13-16)16:   //          agent.timeout = now+tmo  → ...
[](#cb13-17)17:   //   now+tmo: → !agent.blocked → next(trans)
[](#cb13-18)18: }
```

Example 5-2\. A do-not-do scheduling of an agent using promised asynchronous functions

Agent processes are scheduled at an activity level, and a non-terminating agent process activity would block the entire platform (JS processing is strictly single-threaded with one control flow) . Current JS execution platforms, including VMs in Web browser programs, provide no reliable watchdog mechanism to handle non-terminating JS functions or loops. Although some browsers can detect time-outs, they are only capable of terminating the entire JS program, not a function call. To ensure the execution stability of the JAM and the JAM scheduler and to enable time-slicing, check-pointing must be injected into the agent code prior to execution if there is no watchdog support built into the VM. This step is performed in the code parsing phase by injecting a call to a checkpoint function *CP*() at the beginning of the body of each function contained in the agent code, and by injecting the *CP* call in loop conditional expressions. Though this code injection can reduce the execution performance of the agent code significantly, it is necessary until JS platforms are capable of fine-grained check-pointing and thread scheduling with time slicing. On code-to-text transformation (e.g., prior to a migration request), all *CP* calls are removed.

Using the node.js VM platform, native code modules executing functions watching the runtime in an Isolate container can be added that enables timeout detection of agent processing (of activity, transition, and signal handler function calls). If the scheduling slice time of an agent is reached, the called functions will throw an exception (`SCHEDULE`) that is handled by the AIOS agent scheduler. The watchdog modules are detected automatically. If there is no native watchdog support, the software checkpoint injection is used instead.

AIOS provides a main scheduling loop. This loop iterates over all logical nodes of the logical world, and executes one activity of all ready agent processes sequentially. If an activity execution reaches the hard time-slice limit, a SCHEDULE exception is raised, which can be handled by an optional agent exception handler (but without extending the time-slice). This agent exception handling has only an informational purpose for the agent, but offers the agent the opportunity to modify its behaviour. All consumed activity and transition execution times are accumulated, and if the agent process reaches a soft run-time limit, an EOL exception is raised. This can be handled by an optional agent exception handler, which can try to negotiate a higher CPU limit based on privilege level and available capabilities (only level-2 agents). Any ready scheduling block of an agent and signal handlers are scheduled before activity execution. The scheduling loop is executed iteratively based on event times, i.e., the next scheduler run is performed after a calculated time based on pending events (e.g., sleeping agents) and ready agents.

After an activity is executed, the next activity is computed by the schedule that calls the corresponding transition function in the transition section of the agent.

In contrast to the AAPL model that supports multiple blocking statements (e.g., IO/tuple-space access) inside activities, JS is incapable of handling any kind of process blocking (there is no process and blocking concept). For this reason, scheduling blocks can be used in AgentJS activity functions handled by the AIOS scheduler. Blocking AgentJS functions returning a value use common callback functions to handle function results, e.g., `inp(pat, function(tup) {..})`.

A scheduling block is made up of an array of functions (micro activities), i.e., `B(block) = B([function().., function()..,...])`, which the AIOS scheduler executes one by one.Each function may contain a blocking statement at the end of its body. The `this` object inside each function always references the agent object. To simplify iteration, there is a scheduling loop constructor `L(init, cond, next, block, finalize)` and an object iterator constructor `I(obj, next, block, finalize)`, used, e.g., for array iteration.

Agent execution is encapsulated in a process container handled by the AIOS. An agent process container can be blocked while waiting for an internal system-related IO event or suspended while waiting for an agent-related AIOS event (caused by the agent, e.g., the availability of a tuple). Both cases stop the agent process execution until an event occurs.

The basic agent scheduling algorithm is shown in Algorithm 8.1 and consists of an ordered scheduling processing type selection, i.e., partitioning agent processing into agent activities, transitions, signals, and scheduling blocks. In one scheduler pass, only one kind of processing is selected to guarantee scheduling fairness between different agents. There is only one scheduler used for all virtual (logical) nodes in a world (a JAM instance). A process priority is used to alternate the activity and signal handling of one agent, preventing long activity and transition processing delays due to chained signal processing if there are numerous signals pending.

```
∀ node ∈ world.nodes @do
 ∀ process ∈ node.processes @do
  @Determine what to do with prioritized conditions:
    Order of operation selection:
    0\. Process (internal) block scheduling [block]
    1\. Resource exception handling
    2\. Signal handling 6-4-2
       - Signals handled if process priority<HIGH 
       - Signal handling increase process priority 
         temporarily to allow low-latency activity
         and transition function scheduling!
    3\. Transition execution
    4\. Agent schedule block execution [schedule]
    5\. Next activity execution
       - Lowers process priority
  @if process.blocked or process.dead or 
   process.suspended and process.block=[] and 
   process.signals=[] or
   process.agent.next=none and process.signals=[] and
   process.schedule=[]
    @then @do nothing
  @elseif not process.blocked and process.block≠[]
    @then @execute next block function 
  @elseif agent resources check failed 
    @then @raise EOL exception
  @elseif process.priority < HIGH and process.signals≠[]
    then @handle next signal, increase process.priority
  @elseif not process.suspended and process.transition
    @then @get next transition or 
          @execute next transition handler function
  @elseif not process.suspended and process.schedule≠[]
    @then @execute next agent schedule block function
  @elseif not process.suspended
    @then @execute next agent activity and 
      @compute next transition, 
      @decrease process.priority
```

Algorithm 5-4\. JAM agent scheduler algorithm

## Scheduling Blocks

Scheduling blocks must be used if there is more than one blocking operation in an activity or within a loop statement, or if there are computationally long-running code parts. A scheduling block partitions the computational work into sequences or loops of micro functions. Each micro function can call one blocking operation. Although scheduling blocks can be composed of nested blocks, all blocks are flattened into one linear list.

The code templates of scheduling block iterators are shown in Def. [5-1](#4_javascript-agent-machine.xhtml_schedblocks). Each iterator provides a list of functions executed sequentially or repeating function calls in a loop. The *B* constructor is a linear list of micro functions to be scheduled. The *L* iterator supports a conditional loop iterator. First the *init* function is called, and before each iteration loop, the *cond* function is called to return the loop condition (true: execute loop body), followed by the main loop body function. An optional *finalize* function is called if the loop terminates.

```
[](#cb15-1) 1: B([
[](#cb15-2) 2:   function,
[](#cb15-3) 3:   function,
[](#cb15-4) 4:   ..
[](#cb15-5) 5: ])
[](#cb15-6) 6: L(
[](#cb15-7) 7:   init:function,
[](#cb15-8) 8:   cond:function()->boolean,
[](#cb15-9) 9:   next:function(),
[](#cb15-10)10:   block:function [],
[](#cb15-11)11:   finalize?:function
[](#cb15-12)12: )
[](#cb15-13)13: I(
[](#cb15-14)14:   data:{}|[],
[](#cb15-15)15:   next:function (element),
[](#cb15-16)16:   block: function [],
[](#cb15-17)17:   finalize?:function
[](#cb15-18)18: )
```

Definition 5-1\. Templates of AgentJS scheduling block constructor functions that can be used inside agent activity functions. B:Linear block, L:Loop, I:Iterator.Exercise 5-1\. Scheduling Blocks

1.  Create two agents (can be combined in one agent class by different behaviour sub-trees): A data producer and a data consumer agent. The producer agent send a message consisting of single tuples.
2.  The producer agent inserts an array of 10 tuples, each `["TEST",time()]`. After each injection using the *out* operation, the agent sleeps for one second (using *sleep*). A message length tuple is added to the head of the array (`["LENGTH",10]`). Use the *I* block iterator.
3.  The consumer agent should consume the tuples using the *inp* operation. First he waits for the length tuple (beginning of message). Then he should read the message tuples using the *L* iterator.

## Agent Roles

Security is another major challenge in distributed systems, especially concerning mobile agent processes. Each agent platform node (i.e., one physical VM, with multiple JAM VMs operating on the same network node) can receive agents originating either from inside trusting node networks or coming from non-trustful networks unknown to the VM. Generally, the VMs have no information about other network nodes except a sub-set of network connectivity used to receive and propagate agent code. To distinguish at least trustful and not-trustful agents, different agent privilege levels were introduced, providing different AIOS API sets.

### Privilege Levels

For security reasons and to limit denial-of-service attacks, intrusion, agent masquerading, spying, or other misuse, agents have different access levels (roles). A privilege level is related to a specific operational set of functions provided by the AIOS.

There are four levels related to different agent roles:

* * *

0

Guest (not trusting, not mobile)

1

Normal (maybe trusting, mobile)

2

Privileged (trusting, mobile)

3

System (trusting, locally, not mobile)

* * *

Privilege level 0 is the lowest level and grants agents only computational and some tuple-space IO statements. The lowest level does not allow agent replication, migration, or the creation of new agents. Level 0 agents have to negotiate their privilege level or rights by using a security capability that grants certain rights or level upgrades.

Level 1 agents can access the common AIOS API operations and capabilities, including agent replication, creation, killing, sending of signals, and code morphing. Level 2 agents are additionally capable of negotiating (set) their desired resources on the current platform, i.e., CPU time and memory limits.

An agent of level n may only create agents up to level n. The highest level (3) has an extended AIOS operation set with host platform device access capabilities. Level-3 agents cannot migrate to another node, they are fully stationary. Agents can negotiate resources (e.g., CPU time) and a level raise secured with a capability key that defines the allowed upgrades. The system level can not be negotiated.

Level-2 agents can initially only be created inside the JAM. They can fork level-2 agents, but after a migration, the destination node decides about the privilege level and can lower it, e.g., by considering the agent source not trustworthy. A migrated agent can get a higher privilege level by negotiation, requiring a valid platform capability with the appropriate rights. After migration, the privilege is lost and must be re-negotiated on a new platform using capabilities. The JAM platform decides the security level. The capability is node specific. A group of nodes can share a common key (identified by a server port). A capability consists of a server port, a rights field, and an encrypted protection field generated with a random port known by the server (node) only and the rights field.

Other constrain parameters can be negotiated at the AIOS level:

*   Scheduling time (maximal time slice for one activity execution, default is 200 ms)
*   Run time (accumulated agent execution time, default is 5 s)
*   Living time (overall time an agent can exist on a node before it is killed, default is unlimited)
*   Tuple space access limits (number of access operations)
*   Memory limits (practically fuzzy, cannot be measured exactly and monitored in JS, usually the entire size of the agent code including private data, typically limited to 50 kB of serialized code)

Resource constraints are monitored by JAM. Since JAM is executed by generic JS VMs, control of memory consumption of agents during the execution of an activity is not possible (inherently not possible by the JS programming paradigm and the automatic memory management is fully hidden from the programming level). Although bound (body) variables could be monitored by proxies, free variables are out of reach of any resource control. Only allocations accessed via the AIOS can be controlled by JAM, e.g., tuple space access.

### Security with Capabilities

Capabilities are keys to enabling specific agent API functions like migration. A capability consists of a service port, a rights bit field, and an encrypted protection field generated with a random port known only by the server (node) and the rights field. The rights bits field enables specific rights, e.g., the right to negotiate a higher privilege level. A capability is created by the respective service (e.g., the platform itself) by encoding the rights bits field in a security port using a private port and a one-way function, as shown in Fig. [5-3](#4_javascript-agent-machine.xhtml_capa). Major issues are the secret handling of capabilities on agent migration (requiring secured channels) and passing the right capability to an agent. A broker server is commonly required to distribute and pass capabilities to agents based on classical authorization and authentication.

![#capa](images/4cadde4c-aac0-43d3-b541-e11a12f3712c.png)Figure 5-3\. (Top) Capability format (a) Capability creation by encoding a private security port and a new rights field (b) Capability verification by encoding the requested rights field and a private security port and comparing it to the provided security port (based on [MUL90]).

Capabilities enable fine-grained control of operations that can be performed by agents and allow loosely coupled self-organising systems, e.g., participation in chats. In self-organizing systems, the identity of agents is not of primary interest. Instead, the actions they can perform are of primary interest.

Capabilities can be represented in a human-readable text format similar to IPv6 addresses and based on the Amoeba capability format and concepts [MUL90]:

* * *

```
[SS:SS:SS:SS:SS:SS](OBJ(RIGHTS)[PP:PP:PP:PP:PP:PP]
```

* * *

The `SS` and `PP` digits are hexadecimal numbers, `OBJ` and `RIGHTS` are decimal numbers. The service port `SS:` defines the target service of the capability, e.g., the resource negotiation service or a communication channel service (AMP). The protection port `PP:` is used to validate the capability's most sensitive rights field. Commonly, rights are encoded in weighted binary code, enabling combinations of rights, e.g., negotiation of CPU resources and AIOS level upgrade. Typical rights bits used by the AIOS are shown in Def. [5-2](#4_javascript-agent-machine.xhtml_aiosrights). The capability is finally a binary object, but it can be used and transferred in the above textual representation.

```
[](#cb17-1)enum Rights = {
[](#cb17-2)  HOST_INFO       : 0x01, HOST_READ       : 0x02,
[](#cb17-3)  HOST_WRITE      : 0x04, HOST_EXEC       : 0x08,
[](#cb17-4)  PSR_READ        : 0x01, PSR_WRITE       : 0x02,
[](#cb17-5)  PSR_CREATE      : 0x04, PSR_DELETE      : 0x08,
[](#cb17-6)  PSR_EXEC        : 0x10, PSR_KILL        : 0x20,
[](#cb17-7)  PSR_ALL         : 0xff,
[](#cb17-8)  NEG_SCHED       : 0x08, NEG_CPU         : 0x10,
[](#cb17-9)  NEG_RES         : 0x20, NEG_LIFE        : 0x40,
[](#cb17-10)  NEG_LEVEL       : 0x80,
[](#cb17-11)  PRV_ALL_RIGHTS  : 0xff
[](#cb17-12)}
```

Definition 5-2\. AIOS rights bits protecting sensitive agent operations (like negotiation with the agent platform); HOST: platform, PSR: Process control, NEG: Negotiation

For service protection and rights management, the service provider (e.g., JAM) will create a random service and random security port. Alternatively, the service port can be fixed, read from a file, or created from a human-readable string, as shown in Def. [5-3](#4_javascript-agent-machine.xhtml_capops). Typically, capabilities are created and managed by the JAM shell application program, although any JAM node (including Web browser versions) can create and distribute capabilities via the global object `Aios.aios` providing the unrestricted agent API.

```
[](#cb18-1) 1: // Shell or agent API
[](#cb18-2) 2: // 1\. Create random security and service ports
[](#cb18-3) 3: var secret  = Port.unique(),
[](#cb18-4) 4:     service = Port.unique();
[](#cb18-5) 5: // 2\. Put them together in a full rights capability
[](#cb18-6) 6: var supercap = Capability(service,
[](#cb18-7) 7:                           Private(0,0xff,secret));
[](#cb18-8) 8: log(Capability.toString())
[](#cb18-9) 9: // 3\. Restrict capability
[](#cb18-10)10: var restrcap = Capability(service,
[](#cb18-11)11:   Private.restrict(supercap.cap_priv,0x20,secret));
[](#cb18-12)12: var service2 = Port.ofString("12:34:56:78:90:12");
[](#cb18-13)13: // 4\. Check validatiy of client private part 
[](#cb18-14)14: //    and rights
[](#cb18-15)15: var cap = restrcap;
[](#cb18-16)16: if (Private.rights_check(cap.cap_priv,0x20,secret)) {
[](#cb18-17)17:   // grant service
[](#cb18-18)18: }
```

Definition 5-3\. Service provider capability operations (code API for the JAM shell or agents, JAM library requires `.Aios.Sec` prefix)

### Negotiation

Agents can negotiate specific resource constraints or can increase the privilege level by using the agent `negotiate` function with a capability providing the respective rights to perform the operations, as shown in Def. [5-4](#4_javascript-agent-machine.xhtml_negcap). The negotiation is performed by using security ports and capabilities. The capability with specific rights must be passed to the negotation function.

```
[](#cb19-1) 1: ┌ // Shell or server agent:
[](#cb19-2) 2: │ // 1\. A service port and a private random port 
[](#cb19-3) 3: │ // must be created (randomly)
[](#cb19-4) 4: │ var port = Port.unique()
[](#cb19-5) 5: │ var rand = Port.unique();
[](#cb19-6) 6: │ // 2\. The port:rand key must be registered 
[](#cb19-7) 7: │ // on the JAM platform
[](#cb19-8) 8: │ var security = {}
[](#cb19-9) 9: │ security[Port.toString(port)]=Port.toString(rand);
[](#cb19-10)10: │ // 3\. Create a restricted capability with some rights
[](#cb19-11)11: │ var cap  = Capability(
[](#cb19-12)12: │  port,
[](#cb19-13)13: │  Private.encode(0,Rights.NEG_LIFE,rand))
[](#cb19-14)14: │ // Shell: 
[](#cb19-15)15: │ // 4\. Pass capability to new client agent
[](#cb19-16)16: └ create('foo',{cap:cap});
[](#cb19-17)17: ┌ // Client agent:
[](#cb19-18)18: │ // 5\. In foo agent activity perform negotiation 
[](#cb19-19)19: │ // using this cap
[](#cb19-20)20: └ var success=negotiate('LIFE',10000,this.cap);
```

Definition 5-4\. Basic principles of resource and privilege negotiation using a capability (both the JAM node and the agent must use the same public service and secret random security ports)Exercise 5-2\. Security - if you are a JS expert

1.  After you read the previous sections, do you think JAM is safe with respect to denial-of-service attacks and intrusion?
2.  Are the agents really isolated by the presented approaches? Find the back doors and security flaws in JAM! Perform some programming experiments to compromise the JAM platform and other agents, using back doors and hidden references that cannot be masked.
3.  Is the capability protection state of the art? What are the possible issues and flaws? Read the following sections about JAM network connectivity, too.

## Agent Process Mobility and Migration

Mobility of agents requires the transfer of the relevant state of the corresponding agent process and its program code. The agent process state consists of the control and the data state.

The control state of an agent is stored in a reserved agent body variable *next*, pointing to the next activity to be executed. Additionally, there is a hidden control state if an agent activity processes a scheduling block (see Sec. [5-5](#4_javascript-agent-machine.xhtml_sec_scheduling_blocks_7)). The data state of an AgentJS agent consists only of the body variables. There are no references to variables outside the agent process context (free variable references cannot be serialized).

Migration requires a snapshot of the agent process, in this case, the agent itself, a serialization with code-to-text transformation, transportation of the text code to another logical or physical node, and a de-serialization with text-to-code conversion bound to a new sandbox-restricted environment, as shown in Fig. [5-4](#4_javascript-agent-machine.xhtml_procmibu).

The agent object is finally passed to the new node scheduler and can continue execution of the next activity or the next scheduling block entry. Text code sizes of medium-complex agents (with respect to data and control space) are reasonably low at about 10 kB. Simplified agents tend to be 1 kB. That can be significantly reduced by using LZ compression. One drawback of this method is that pending scheduling blocks exist in the snapshot. They must be entirely saved in the migrated snapshot, too, and converted back to code on the new node. Pending scheduling blocks contain function code and hence can increase the snapshot size significantly. Therefore, migration (using the `moveto` operation) requests should not be embedded in a scheduling block.

Agent migration is always performed via the Agent Management Port (AMP) with a negotiated virtual link connection between the sending and receiving node, discussed in the next section.

![#procmibu](images/62da35ee-7a01-4ba2-a236-2a2c80f51940.png)Figure 5-4\. Agent process creation and process migration work flow

## JAM Platform Connectivity

### JAM Networking

An agent can migrate to another JAM platform. JAM agents are mobile by transferring a snapshot of an agent process containing the entire data and control state, including the program specifying the agent's behaviour. Communication is a central part of agent interaction. Aside from tuple space communication, which is essentially limited to the local node level, signal messages can be addressed to agents on remote platforms, which necessitates unified but loosely coupled platform connectivity.

JAM provides a broad range of connectivity options, shown in Figure [5-5](#4_javascript-agent-machine.xhtml_jamconn), available on a broad range of host platforms. There is peer-to-peer (P2P) connectivity between neighbour nodes by using, e.g., serial links used in mesh-grid networks, and wide-area connectivity, i.e., the Internet, by using generic HTTP, TCP. or UDP protocols via the AMP discussed in the next section and/or optionally by using the Distributed Organization System layer (DOS) and a broker server.

### Agent Management Port (AMP)

Using P2P connectivity, JAM nodes communicate via the *Agent Management Port* (AMP). AMP provides messaging between JAM nodes for agent migration, signal and tuple migration, collection of statistical data, and agent control. AMP messages can be transferred via any stream-like link. Additionally, an external monitor program (debugger) can connect to a JAM node via AMP. AMP is independent of any specific data communication protocol and hence supports a wide range of communication technologies, not limited to IP communication, as shown in Fig. [5-5](#4_javascript-agent-machine.xhtml_jamconn).

![#jamconn](images/e9e604e0-4b1a-4178-8cde-dd7da481a503.png)Figure 5-5\. JAM communication and node connectivity (P2P: Peer-to-Peer, AMP: Agent Management Port, DOS: Distributed Organization Layer)

On the Internet, IP-based protocols are commonly used to provide AMP message passing between JAM nodes using UDP, TCP, or HTTP protocols. One common issue is private or virtual networks with Network Address Traversal (NAT). To establish UDP communication between NAT networks, an external public rendezvous broker providing UDP hole punching techniques can be used. In this case, JAM nodes register on the broker with their node names, and other JAM nodes can connect to the (IP hidden) JAM nodes by their node names. The broker supports domain services (partitioning of nodes into domains or groups, e.g., based on GPS data).

JAM nodes can be loosely linked via the Agent Monitor Protocol (AMP) creating a distributed platform network. AMP is used to connect JAM nodes, e.g., via the Internet, by using generic HTTP communication encapsulating AMP messages.

| Message Type | Description |
| --- | --- |
| `ACK` | Acknowledgement reply |
| `LINK` | Unidirectional link negotiation request (pair-wise, can be protected by capabilities) |
| `PING` | Keep alive messages between nodes to estimate the connectivity state |
| `PONG` | Reply to a *PING* message |
| `UNLINK` | Close a previously negotiated link |
| `RPCHEAD` | Header of a RPC message (support for connection-less protocols) |
| `RPCDATA` | Data chunk of an RPC message (support for connection-less protocols providing data fragmentation and ordering) |
| `RPCHEADDATA` | Header and data of a RPC message (only supported by connection-based protocols) |
| `SCAN` | Scan request for external services |
| `INFO` | Information request for external services |

Table 5-1\. AMP message types

The set of AMP message types are shown in Tab. [5-1](#4_javascript-agent-machine.xhtml_ampmsg). A platform *A* can be linked with a platform *B* by starting a link negotiation phase, which can be protected by a security capability. The initiator node sends a *LINK* message, that will be acknowledged by an *ACK* message and (if request is authorized) by another *LINK* message from *B* to *A*. To test the link status, *PING* and *PONG* messages are used (by both link partners). If a link is established (that may be unreliable and can vanish at any time), Remote Procedure Calls (RPC) can be executed by using the *RPCHEAD* and *RPCDATA* messages. A communication link between two nodes can be unidirectional (directed, e.g., *A* → *B*). In this case, either two unidirectional links are set up by two nodes *A* and *B* independently, or the communication is used as is without acknowledgement. This operational state is still in accordance to the multi-agent model not relying on any reliable platform capabilities including communication. Although, connection links between nodes are established prior RPC messaging, the link does not rely on an underlying connection and state-based communication channel, e.g., like in the case of TCP connections. UDP never established a persistent communication channel, and HTTP do not require a keep-alive TCP connection. In contrast, the WebSocket transport layer always rely on a connection state and is therefore not primarily suitable for creating JAM networks.

The RPC messages encapsulate agent process snapshot migration, remote signal message delivery, and remote tuple space requests. Each AMP communication port can be a communication end-point or a router, too.

![#agtraces](images/c7d74baf-c407-4dcd-be2d-c3781e32ff06.png)Figure 5-6\. Agent migration traces and crossing points (APP: JAM node). Signals can be delivered only along migration paths. Along a sub-path between two nodes there must exist a negotiated AMP link.

AMP enables the composition and connection of already distributed agent platform networks. Signal messages can be forwarded to agents on different remote nodes, but signal message propagation is limited to agent migration paths (traces), shown in Fig. [5-6](#4_javascript-agent-machine.xhtml_agtraces).

Physical channel links via AMP between nodes in common IP-based computer networks can use different underlying data and message protocols, compared side by side in the following summary:

A signal from agent *A* can only be delivered to agent *B* if at any pastime they joined the same node (this is always the case in parent-children groups). Agents on two different nodes are aware of the two different distinct nodes. Remote communication is not reliable, i.e., sending of signals or migration of agents can result in a total loss.

UDP

The User Datagram Protocol (UDP) is well suited for AMP links because it requires no state- and session-based connection. But UDP communication requires on the first level public and visible computer nodes. Using UDP hole-punching techniques (supported by AMP) it is possible to overcome limitations by NAT behind private/virtual networks. But symmetric NATs commonly still prevent bidirectional communication. And if both nodes are behind (symmetric) NATs there is no chance to establish an AMP link. UDP links are fully symmetric, i.e, both end-points provide a service.

HTTP(S)

The Hyper Text Transfer Protocol (and its secured version) is widely used in the Web. Beside WebSockets (upgrade via HTTP), this protocol is the only one that can be used in JAM Web applications. HTTP communication is asymmetric, i.e., there is one dedicated service and one or multiple client nodes establishing a TCP-based communication session. Only the HTTP service port must be visible in the network (Intra- or Intranet), the client can be hidden behind a NAT. For each AMP message transfer, a new HTTP request (GET/POST) is executed. The underlying protocol layer will decide if it reuses a TCP connection, or connects for each request to the service again. AMP sets the protocol *keepAlive* option per default. The secured version requires certificates. If the client is a Web browser the certificates must be valid and a DNS validated domain is required.

TCP

The Transmission Control Protocol (TCP) is state- and session-based, not very suitable for ad-hoc AMP links. There are three different modes supported by the AMP TCP back-end: (A) Symmetric pair of ad-hoc uni-directional TCP connections opened for each message and closed after transmission (B) Symmetric pair of permanent uni-directional TCP connections with message streams (C) Single bidirectional permanent TCP connections from "client" to "server", i.e., an AMP handler for each socket ⇒ for clients behind NATs.

AMP ports can have a uni- or multicast. A multicast port supports multiple links from remote node ports, and multiple links to this port. IP ports are typically multicast ports. In addition, AMP ports can be uni- or bidirectional. The creation of AMP ports and establishment of links between JAM nodes is described in detail in Sec. [7-2](#6_jam-for-users-and-programmers.xhtml_sec_jam_shell_1).

The following Fig. [5-7](#4_javascript-agent-machine.xhtml_ampip3) shows the data flows for the different IP protocol deployments and their usage.

![#ampip3](images/61ada48f-c18d-468c-b1dd-46ce1031457f.png)Figure 5-7\. AMP control and data flows with different IP protocols and usage (a) Connectionless UDP (b) Ad-hoc TCP (simulated UDP) (c) Pair of permanent TCP session (d) Single permanent TCP session (e) Ad-hoc HTTP(S)

Central and best suitable protocol is connectionless UDP. All AMP messages are fragmented and encapsulated in UDP packets with out-of-order defragmentation on the receiver side. Connection-based protocols like TCP and HTTP (on the top of TCP) are simulated datagram messaging, i.e., opening for each AMP message a new connection. Explicit fragmentation of larger messages is not required. HTTP is client-server orientated, i.e., only a dedicated server node provides an HTTP port, and only the client can initiate a connection.

There are two variants of the TCP protocol: Permanent session based with a pair of TCP connections, and a single TCP session initiated by a client, typically behind NAT virtual networks. HTTP can use a permanent connection for a specific time by providing the *keepAlive* option. HTTP POST requests are used to forward messages to the destination node, and GET messages are used to collect messages from the destination.

## Software Architecture and Workflow

The software architecture is composed of:

1.  AIOS;
2.  Modules (for dealing with nodes, processes, communication, and so on);
3.  Host platform API wrapper and utility function library;
4.  Applications (shell, Web laboratory, simulator).

In Fig. [5-8](#4_javascript-agent-machine.xhtml_jamsoftarch), the basic software architecture with its components is shown. In addition, the basic operational workflow is sketched starting with the compilation of agent constructor functions from source text, agent process creation and scheduling, and JAM world management.

![#jamsoftarch](images/3bb6ae09-1ad7-4e54-a0ea-c78f2b4266bd.png)Figure 5-8\. JAM components and software architecture with basic operational flow

# AgentJS API

AgentJS supports all ES 2015 JS compliant functions and statements. Due to the sandbox-restricted container encapsulation, some JS operators do not operate as expected, e.g., the `for(a in b)` operation is broken. Instead, AgentJS provides polymorphic iterator operations, introduced in the next section. There is no support for objects with prototype function bindings (cannot be serialized efficiently). Objects in AgentJS must be pure procedural, i.e., the agent or the AIOS has to provide separate functions to process objects (i.e., data records).

AgentJS programming statements can be divided into five core groups and extensions:

1.  Computational statements with extended array and object (record) operations;
2.  Agent control and environment operations, such as node information and resource negotiation;
3.  Agent management, which includes the creation, modification, and control of agents.
4.  Agent communication, which is synchronized communication using tuple spaces and signals.
5.  Agent mobility, i.e., node-to-node process snapshot migration;
6.  Machine Learning (extension) provides mostly portable (mobile, pure procedural) models and a wide range of algorithms.

The AgentJS API is provided by the AIOS API, with a set of functions depending on the privilege level of the agent (assigned on creation or after migration).

## Computation

Computations can be performed in activities, transitions, and signal handlers. This primarily modifies agent data (agent body variables) accessed by the `this` object. The agent self-reference is available in all AIOS functions in callback functions passed to AIOS functions (at least on the first level of call context). Note that AgentJS only supports bound record data objects without decoupled prototype function bindings. The computational statements are summarized in Tab. [6-1](#5_agentjs-api.xhtml_cas).

| Operation(s) | Description |
| --- | --- |
| `abs, add, angle, delta, distance, div, equal, max, min, neg, random, sum, zero` | Extended math functions |
| `array, concat, contains, copy, empty, filter, flatten, head, isin, iter, keys, last, map, matrix, pluck, reduce, reverse, sort, tail, without, Vector` | Array and object functions |
| `int, object, string` | Type conversion |

Table 6-1\. Computational agent statements

The iterator functions `concat`. `flatten`, and `iter` can be applied on array and record data structures, too. This is also the case for the functions `angle`, `contains`, `copy`, `delta`, `isin`, `neg`, and `zero`. Examples of polymorphic and mixed data type operations are shown in Ex. [6-1](#5_agentjs-api.xhtml_excas).

```
[](#cb20-1)var a = [1,2,3,4],
[](#cb20-2)    ones = array(16,1 /*init*/);
[](#cb20-3)var amin = min(a), amax = max(a),
[](#cb20-4)    arnd = random(a),
[](#cb20-5)    vrnd = random(0,1,0.01 /*frac*/);
[](#cb20-6)var v = Vector(1,1); /*{x,y}*/
[](#cb20-7)if (zero(v)) v.x=v.y=1;
[](#cb20-8)var b = [5,6,7,8]
[](#cb20-9)var c = concat(a,b);
[](#cb20-10)var d1 = { a:1, b:2 },
[](#cb20-11)    d2 = { c:0 },
[](#cb20-12)    d3 = concat(d1,d2),
[](#cb20-13)    ds = 0;
[](#cb20-14)iter(d3, (e) => { ds += e })
[](#cb20-15)if (sum(d3)!=ds) log('not equal, but must be');
[](#cb20-16)if (isin(d3,2) && isin(a,2)) log('common element 2');
[](#cb20-17)if (contains(a,[3,5]) log('contains 3 or 5');
[](#cb20-18)var d = [a,b],
[](#cb20-19)    col1 = pluck(d,1); // [2,6]
```

Example 6-1\. Examples of computational statements used in agent functions

## Agent Environment

The agent is situated in its environment, providing interaction and perception (data). The environment consists primarily of the host platform, the world around us, including other agents, and the agent itself. The agent can request multiple sensors to get information about its platform, the location of the platform, process group relations, and its state, summarized in Tab. [6-2](#5_agentjs-api.xhtml_agentjsenv). Finally, an agent has a privilege level providing restricted access to the JAM platform. The `privilege` operation returns the agent's current privilege level in the range [0,3] that can be changed by negotiation by using the `negotiate` operation, typically requiring a valid capability key with sufficient rights to negotiate resources with the platform.

| Operation(s) | Description |
| --- | --- |
| `info (cls)` | Generic sensor that provides node, location, current agent processing constraints, and limits. Node information can be requested by using *cls*='node'. This returns an object `{ id:string, position:{}, location:{ip:string ,gps:{} ,geo:{}}, type:string}` |
| `me` | Return the current agent identifier |
| `myClass` | Return the agent class (basically the name of the agent constructor function) |
| `myNode` | Return the current APP node name (identifier) |
| `myParent` | Return the agent parent (identifier) if this a forked child agent |
| `myPosition` | Return the current APP node position (if available) |
| `negotiate(what,val,cap)` | Change platform rights and restrictions |
| `privilege` | Return the current agent privilege level (0-3) |
| `time` | Current node time adjusted for world time lag (clock calibration and support for node processing pauses, e.g., in simulation mode) |

Table 6-2\. Environmental perception statements

The following parameters (Tab. [6-3](#5_agentjs-api.xhtml_agentjsnego)) can be negotiated by the agent (assuming appropriate rights given by the capability argument). Memory constraints cannot be controlled by JAM since there is no way on JS level to get information about the memory usage of specific objects, although, a normalized memory allocation factor assuming C-like memory allocation could be computed. But JAM is not aware of data allocations inside agent functions (under the VM GC control) and would require inspection of the data state after each function call, which would degrade JAM performance significantly. Only tuple space access, agent creation, and signalling can be controlled by JAM.

| Parameter | Rights | Description |
| --- | --- | --- |
| `LIFETIME` | `NEG_LIFE` | Change the agent lifetime (total accumulation) |
| `SCHEDULE` | `NEG_SCHED` | Change the maximal agent scheduling time |
| `CPU` | `NEG_CPU` | Change the maximal CPU time (sum of all schedule times) |
| `TS` | `NEG_RES` | Change the maximal number of tuple requests |
| `AGENT` | `NEG_RES` | Change the maximal number oif agents that can be created |
| `LEVEL` | `NEG_LEVEL` | Change the AIOS operational privilege level |

Table 6-3\. Platform and resource parameters that can be negotiated and the required rights

Some examples of environmental information and control operations are shown in the following Ex. [6-2](#5_agentjs-api.xhtml_apienvex1).

```
[](#cb21-1)me()
[](#cb21-2)─────────
[](#cb21-3)jireluci
[](#cb21-4)
[](#cb21-5)myNode() 
[](#cb21-6)────────
[](#cb21-7)xazorodi
[](#cb21-8)
[](#cb21-9)privilege() 
[](#cb21-10)────────
[](#cb21-11)1
[](#cb21-12)
[](#cb21-13)info('node')
[](#cb21-14)────────────
[](#cb21-15){ id: 'xazorodi',
[](#cb21-16)  position: { x: 0, y: 0 },
[](#cb21-17)  location: 
[](#cb21-18)   { ip: '31.16.196.110',
[](#cb21-19)     gps: { lat: 53.0515, lon: 8.8896 },
[](#cb21-20)     geo: 
[](#cb21-21)      { city: 'Bremen',
[](#cb21-22)        country: 'Germany',
[](#cb21-23)        countryCode: 'DE',
[](#cb21-24)        region: 'HB',
[](#cb21-25)        zip: '28309' } },
[](#cb21-26)  type: 'shell' }
[](#cb21-27)
[](#cb21-28)myPosition()
[](#cb21-29)────────────
[](#cb21-30){ ip: '31.16.196.110',
[](#cb21-31)  gps: { lat: 53.0515, lon: 8.8896 },
[](#cb21-32)  geo: 
[](#cb21-33)   { city: 'Bremen',
[](#cb21-34)     country: 'Germany',
[](#cb21-35)     countryCode: 'DE',
[](#cb21-36)     region: 'HB',
[](#cb21-37)     zip: '28309' } }
```

Example 6-2\. Examples of the output from an agent's environmental information functions

The negotiation using capabilities was already introduced and discussed in Sec. [5-6](#4_javascript-agent-machine.xhtml_sec_agent_roles_8) with shell and agent code.

## Agent Management

Agents are either created by the platform and host application from a constructor function or by agents, either from a constructor function or as a copy (child forking by the parent agent). Constructor functions must be recompiled in a restricted context with respect to the initial privilege level of the agent. To speed-up agent creation, agent constructor functions can be precompiled (and analysed) and added to the JAM platform dictionary in advance. The compilation of agent class constructor functions is only possible by the platform discussed in the application chapter [JAM for Users and Programmers], not by the agent itself. Creation of new agents by agents requires precompiled constructor functions stored in the node dictionary.

### Creation of Agents

Before an agent can be created either by the platform or by an agent itself, the constructor function must be compiled (analysed) and stored in the platform class library dictionary. Agent forking can be done without an installed agent constructor function. The fork operation creates an exact child copy of the parent agent with an optionally modified set of body variables.

| Operation(s) | Description |
| --- | --- |
| `create(class,parameter,level)` | Create an agent from a class constructor function (or alternatively, it's a string name of an already compiled agent class) with optional parameter settings. The AIOS level argument is optional and may not be higher than the level of the parent process |
| `fork (parameter)` | Make a duplicate of the calling agent with the same code and data state but (optionally) different parameter settings (direct modification of the forked agent's body variables) |

Table 6-4\. Creation of agents

In the following Ex. [6-3](#5_agentjs-api.xhtml_exagcreat) one agent is created programmatically by the JAM platform (using *jamsh*). Firstly, the agent constructor function is defined, finally compiled, and added to the JAM platform. The agent begins in activity *init* and remembers its identifier in body variable *master*. A straight transition to the *replicate* activity forks a child agent with a modified set of body variables (*message*). The identifier of the newly created agent is stored in the parent *child* variable. The child agent will move to another node via the *migrate* activity. If this variable is set, the parent agent will sleep after the *wait* activity has been processed. The child agent (having still an empty *child* variable) will print out the message it has gotten from its parent and sleep forever. After the parent is woken up, it will kill its child agent. The kill signal is forwarded from the parent to the child node.

```
[](#cb22-1)function ag (options) {
[](#cb22-2)  this.child=null;
[](#cb22-3)  this.master=null;
[](#cb22-4)  this.message=null;
[](#cb22-5)  this.act = {
[](#cb22-6)    init : () =>) {
[](#cb22-7)      this.master=me(); 
[](#cb22-8)    }, 
[](#cb22-9)    replicate : () => {
[](#cb22-10)      this.child=fork({message:'I am John.'});
[](#cb22-11)    },
[](#cb22-12)    migrate : () => {
[](#cb22-13)      var nodes = link(DIR.IP('%'));
[](#cb22-14)      if (nodes.length) moveto(DIR.NODE(random(nodes)));
[](#cb22-15)    },
[](#cb22-16)    killing : () => {
[](#cb22-17)      kill(this.child);
[](#cb22-18)    },
[](#cb22-19)    wait : () => {
[](#cb22-20)      if (this.child) {
[](#cb22-21)        sleep(1000);
[](#cb22-22)      } else {
[](#cb22-23)        log(this.message);
[](#cb22-24)        sleep();
[](#cb22-25)      }
[](#cb22-26)    },
[](#cb22-27)    end : () => {
[](#cb22-28)      kill();
[](#cb22-29)    }
[](#cb22-30)  }
[](#cb22-31)
[](#cb22-32)  this.trans = {
[](#cb22-33)    init      : replicate,
[](#cb22-34)    replicate : () => { return this.child?wait:migrate },
[](#cb22-35)    migrate   : wait,
[](#cb22-36)    killing   : end,
[](#cb22-37)    wait      : () => { return this.child?killing:wait },
[](#cb22-38)  }
[](#cb22-39)
[](#cb22-40)  this.next=init;
[](#cb22-41)
[](#cb22-42)}
[](#cb22-43)// Add agent class
[](#cb22-44)compile(ag,{verbose:false});
[](#cb22-45)// Create level 2 agent
[](#cb22-46)create('ag',{ },2);
```

Example 6-3\. Examples of agent creation either by instantiating from a constructor function or by forking (cloning). The code is processed by the jamsh program.

> Forking of child agents discards queued scheduling blocks of the parent agent, in contrast to agent migration.

Exercise 6-1\. Agent Trees

1.  Assume a two-dimensional mesh grid network of connected JAM nodes. Each node provides a sensor that can be accessed via the `v=inp(["SENSOR",_])` statement. An agent can migrate to a neighbouring node using the `DIR.NORTH`, `DIR.WEST`, and so on, directions with the `moveto` and `link` functions. An arbitrary node in the network will create one agent. This agent should sample all sensors in the network and should compute the average of all sensor values. The root agent should create two child agents by forking. The child agents should move to neighbour nodes in opposite directions, e.g., one to the West, the other to the East (if possible).
2.  After a child agent reaches the neighbour node and samples the local sensor value, it should create three more child agents, one going in the previous forward direction, and two in opposite directions orthogonal to the forward direction.
3.  Each orthogonal travelling agent should create another child agent that moves to the neighbour node in the current direction until the boundary of the network is reached.
4.  A child agent is created only if there is a neighbour node in the given direction. If an agent cannot create new agents, it returns to its root node and sends his parent agent the sampled sensor of the neighbour node via a signal.
5.  If an agent gets replies from all its children via the signal handler, which accumulates the sensor values, it will return to its root position, too, and deliver the sum of all sampled sensor values (collected by itself and its children).
6.  The root agent (number 1) will accumulate all sensor sums delivered by its children and compute the average value.
7.  Create an agent class with AgentJS that implements the divide-and-conquer approach.
8.  Test the multi-agent system using the JAM shell by creating a virtual JAM network (see Sec. [7-2-5](#6_jam-for-users-and-programmers.xhtml_sec_virtual_worlds_6)).

### Modification of Agents

Agents can modify their behaviour ATG by adding or removing activities and transitions, as shown in Tab. [6-5](#5_agentjs-api.xhtml_agm). Furthermore, activities and transitions can be modified (replacement). Transitions can be modified temporarily to create child agents with different control flows. After an agent has been forked, the original transitions can be restored. An activity update or addition requires a unique activity name and a function. A transition rule update or addition requires the start activity and either a constant end activity name or a resolution function that can return any of the existing activities (or null if there is no active transition resulting in agent blocking). Some examples are shown in Ex. [6-4](#5_agentjs-api.xhtml_exagentjsmod).

Transitions can be updated (replacing old transition rules using the *update* method) or extended with an additional transition selection function using the *add* function. See Ex. [6-4](#5_agentjs-api.xhtml_exagentjsmod) for details. If the transition function references free variables (from current activity or handler function), the transition function can be parametrized with an additional data parameter, as shown in the example "EXTEND" signal handler. For example, another agent can send a signal with an act:string,fun:string} object argument containing a new activity name and the function implementation.

| Operation(s) | Description |
| --- | --- |
| `trans{.add .delete .update} (start,end?,data?)` | Modification of transitions |
| `act{.add .delete .update} (name,function?)` | Modification of activities |

Table 6-5\. Modification of agents

```
[](#cb23-1) 1: function adapter() {
[](#cb23-2) 2:   this.v=0;
[](#cb23-3) 3:   this.act : {
[](#cb23-4) 4:     init : () => {
[](#cb23-5) 5:       // Uncondtional transition
[](#cb23-6) 6:       trans.add('more','wait');
[](#cb23-7) 7:     },
[](#cb23-8) 8:     replicate: () => {
[](#cb23-9) 9:       trans.update(replicate,migrate);
[](#cb23-10)10:       this.child=fork({dir:DIR.EAST,MAXHOP:1});
[](#cb23-11)11:       trans.update(replicate,wait);
[](#cb23-12)12:     },
[](#cb23-13)13:     percept : () => {
[](#cb23-14)14:       trans.update('explore',function () {
[](#cb23-15)15:         if (this.enoughinput<1) return 'goback';
[](#cb23-16)16:         else return 'wait';
[](#cb23-17)17:       }); 
[](#cb23-18)18: 
[](#cb23-19)19:     },
[](#cb23-20)20:     explore : () => {},
[](#cb23-21)21:     goback: () => {},
[](#cb23-22)22:     migrate : () => {},
[](#cb23-23)23:     wait : () => {},
[](#cb23-24)24:   }
[](#cb23-25)25:   this.trans : {
[](#cb23-26)26:     replicate : wait,
[](#cb23-27)27:     choices : () => {
[](#cb23-28)28:       return wait;
[](#cb23-29)29:     },
[](#cb23-30)30:   }
[](#cb23-31)31:   this.on : {
[](#cb23-32)32:     // Signal from other agent 
[](#cb23-33)33:     // data={act:string,fun:string}
[](#cb23-34)34:     "EXTEND" : (data,from) => {
[](#cb23-35)35:       data=JSON.parse(data); // JSON==JSON+
[](#cb23-36)36:       act.add('choices-'+data.act,
[](#cb23-37)37:               data.fun);
[](#cb23-38)38:       // Extend choices transition rule;
[](#cb23-39)39:       // Need to pass data to the conditional 
[](#cb23-40)40:       // rule function
[](#cb23-41)41:       trans.add('choices',(act) => {
[](#cb23-42)42:         if (this.choice=='choices-'+act)
[](#cb23-43)43:           return 'choices-'+act;
[](#cb23-44)44:       },data.act);
[](#cb23-45)45:     }
[](#cb23-46)46:   }
[](#cb23-47)47: }
```

Example 6-4\. Example usage of code morphing operations

The ATG modification can be used to replicate lower functional agents by removing unnecessary activities and transitions temporarily. The original activity, transition, and handler functions can be saved in temporary variables. They can be either directly accessed by the agent `this` object or retrieved by the return value of the respective *delete* operation in the case of activities and transitions. This is shown in the simple agent code in Ex. [6-5](#5_agentjs-api.xhtml_atgmodifork). The activity trace of the parent (root) agent is the run *a1* → *a2* → *a3*, whereas the forked child agent will execute the run *a1* → *a3*.

```
[](#cb24-1) 1: function foo (options) {
[](#cb24-2) 2:   this.child=null;
[](#cb24-3) 3:   this.act = {
[](#cb24-4) 4:     a1: () => {
[](#cb24-5) 5:       // var a2=this.act.a2
[](#cb24-6) 6:       var a2 = act.delete('a2');
[](#cb24-7) 7:       trans.update('a1','a3');
[](#cb24-8) 8:       this.child=fork({});
[](#cb24-9) 9:       act.add('a2',a2)
[](#cb24-10)10:       trans.update('a1','a2');
[](#cb24-11)11:     },
[](#cb24-12)12:     a2: () => {},
[](#cb24-13)13:     a3: () => {kill()} 
[](#cb24-14)14:   }
[](#cb24-15)15:   this.trans = {
[](#cb24-16)16:     a1:a2,
[](#cb24-17)17:     a2:a3,
[](#cb24-18)18:   }
[](#cb24-19)19:   this.next = a1
[](#cb24-20)20: } 
```

Example 6-5\. Using temporary agent behaviour modification to create sub-class agents

Modifying the parent ATG just for child agent forking is not convenient and can be error-prone. If the child agent should only inherit a sub-set of the activities, transitions, body variables, and event handlers, a simplified ad-hoc subclass composition using the *create* operation can be performed, as explained in Def. [6-1](#5_agentjs-api.xhtml_forksubclass). Only the parts that should be inherited (optionally modified) are provided. The set of body variables, activities, and optional signal handlers must be complete (i.e., only the specified parts are inherited). The transitions are automatically inherited (based on the new activity set). The transition entry only contains modified transition rules. Although the *create* operation creates standalone agents independent from the creating agent, the parent reference of the newly created child agent is set in this case.

```
[](#cb25-1) 1: var child = create({
[](#cb25-2) 2:   x : this.x,
[](#cb25-3) 3:   y : /*any other value*/,
[](#cb25-4) 4:   act : {
[](#cb25-5) 5:     a1 : a1,
[](#cb25-6) 6:     a2 : () => { /*modfied activity*/ },
[](#cb25-7) 7:     ..
[](#cb25-8) 8:   }, // or
[](#cb25-9) 9:   act : [a1,a2,..],
[](#cb25-10)10:   trans : {
[](#cb25-11)11:     a1: () => { /*modified transition*/ }
[](#cb25-12)12:   }
[](#cb25-13)13:   on : {
[](#cb25-14)14:     SIG : this.on.SIG,
[](#cb25-15)15:     ..
[](#cb25-16)16:   }
[](#cb25-17)17: },level?:number);
```

Definition 6-1\. Forking of a subclass agent using parent objects and new code or data

The following example agent shows a minimal subclassing scheme (can be executed by the JAM shell). The master agent creates a minimal child agent with only one activity and two transition rules (one explicitly defined, one inherited by the parent). The master agent executes either activity *compA* or *compB*, depending on the input *data*. The forked child agent always executes the *compA* activity.

* * *

```
[](#cb26-1)function master(xy) {
[](#cb26-2)  this.data=xy; this.z=0; this.child=null;
[](#cb26-3)  this.act = {
[](#cb26-4)    start : () => {
[](#cb26-5)      this.child = create({
[](#cb26-6)        z:0,
[](#cb26-7)        data:{
[](#cb26-8)          x:random(1,50),
[](#cb26-9)          y:random(1,50)
[](#cb26-10)        },
[](#cb26-11)        act : [compA,end],
[](#cb26-12)        trans : {
[](#cb26-13)          start:compA
[](#cb26-14)        }
[](#cb26-15)      })
[](#cb26-16)    },
[](#cb26-17)    compA: () => {
[](#cb26-18)      this.z=this.data.x+this.data.y;
[](#cb26-19)    },
[](#cb26-20)    compB: () => {
[](#cb26-21)      this.z=this.data.x*this.data.y;
[](#cb26-22)    },
[](#cb26-23)    end : () => {
[](#cb26-24)      log(this.z);
[](#cb26-25)      kill()
[](#cb26-26)    }
[](#cb26-27)  }
[](#cb26-28)  this.trans = {
[](#cb26-29)    start:() => {
[](#cb26-30)      return this.data.x<10 && 
[](#cb26-31)             this.data.y<10?compB:compA
[](#cb26-32)    },
[](#cb26-33)    compA:end,
[](#cb26-34)    compB:end
[](#cb26-35)  }
[](#cb26-36)  this.on = {
[](#cb26-37)    SIG1: () => {
[](#cb26-38)      log('got SIG1')
[](#cb26-39)    }
[](#cb26-40)  }
[](#cb26-41)  this.next=start
[](#cb26-42)}
[](#cb26-43)compile(master)
[](#cb26-44)create('master',{x:5,y:7})
[](#cb26-45)start()
```

* * *

### Control of Agents

Control of agents is primarily event-based and includes the termination of agents. Note that the termination performed by the *kill* operation only requires the agent identifier name, which should not be publicly visible. The agent control flow can be explicitly blocked either by waiting on a time event or by an explicit wake-up performed either by an agent's own signal handler or by another agent (on the same node), as shown in Tab. [6-6](#5_agentjs-api.xhtml_agx). Note that a blocking operation will not block the JS control flow. Instead, the following activity transition is blocked.

Events are commonly handled by signal handlers defined in the `this.on` section. Events can be sent from other agents (external events) or by the platform (internal events). A timer can be created and started by the `timer.add` operation, sending signals to the agent after the specified time elapses (one time or periodically). Platform events are, for example, `END`, `KILL`, and `ERROR`.

| Operation(s) | Description |
| --- | --- |
| `kill(aid)` | Send the *kill* signal to an agent (without argument kills calling agent) |
| `sleep(tmo?)` | Suspend agent execution until a wakeup event occurs (either explicitly or via a millisecond timeout). A suspended agent can still receive signals. |
| `wakeup(aid?)` | Wake up an agent, typically called from a signal handler (stop and go control). If no agent identifier is provided, this agent will be woken up (if suspend). |
| `timer.add(tmo,sig,arg,repeat)` | Add a timer to the agent process. After the time *tmo* in milliseconds has elapsed, the signal *sig* will be raised with an optional argument *arg*. The agent must have a signal handler for this signal (*on* section). If the argument *repeat* is true, the timer is fired periodically. |
| `timer.delete(sig)` | Remove a timer from the agent process. |

Table 6-6\. Control of agents

An example using the `sleep` operation in conjunction with `wakeup` is shown in the following Ex. [6-6](#5_agentjs-api.xhtml_agcontr1). A background timer is started in activity *init*, which raises the signal `WATCHDOG` after 100 ms. The *delay* activity sleeps for 1000 ms and will suspend the agent's processing (i.e., any further activity transition) until the sleeping time is over. The *await* activity calls the *sleep* operation without an argument, suspending the transition to the next activity for an indefinite time waiting for a wake-up event. If the `WaTCHDOG` signal handles the timer-generated signal, the agent will be woken up. The *process* activity finally deletes the timer (if it is still existing, otherwise the operation has no effect). Any other agent can wake up the sleeping agent, e.g., by sending a signal (`SIGUSER`), which is handled by the agent.

```
this.act : {
  init : function () {
    timer.add(100,'WATCHDOG');
  },
  delay : function () {
    sleep(1000)
  },
  await : function () {
    sleep();
  },
  process : function () {
    timer.delete('WATCHDOG');
  }
}
this.trans : {
  init:delay,
  delay:await,
  await:process
}
this.on : {
  'SIGUSER': function () {
    wakeup()
  },
  'WATCHDOG' : function (arg) {
    wakeup();
  }
}
```

Example 6-6\. Agent control with sleep and wake-up operations

## Agent Communication

Agents can communicate with each other by using undirected tuple spaces and directed signal messages, summarized in Fig. [6-1](#5_agentjs-api.xhtml_agcomm1). Tuples can only be exchanged by agents processed by the same node. Signals can be sent to agents processed on the same node or on separate nodes if there is an agent migration path between the source and destination node. Remote signal propagation can be used to access remote tuple spaces, too, basically to copy or transfer tuples between different nodes. Level 2/3 agents have access to the remote tuple space API too.

![#agcomm1](images/762d7d84-5d4b-433e-aed3-f902009bf140.png)Figure 6-1\. Basic agent-agent communication methods

Both communication methods are easy to use programmatically, requiring only simple statements:

```
[](#cb28-1)| Agent A |        | Agent B |
[](#cb28-2)
[](#cb28-3)send(B,'S',1)      on.S = (arg,from) => {..}
[](#cb28-4)out(['V',2])       inp(['V',_],(t) )> { .. })
[](#cb28-5)sleep()            wakeup(B) // same JAM
```

The following two subsections describes the programming of the anonymous generative communication using tuple spaces and the addressed communication using signal messages.

### Generative Tuple-space Communication

A tuple is a data container that binds multiple values. Formally, tuple elements cannot be accessed directly, in contrast to arrays. But AgentJS implements tuples with arrays. In contrast to arrays, tuples are poly-typed, i.e., each element can have a different data type. Arrays in JS are poly-typed, too, and can be created on the fly (as tuples). A tuple is characterized by its arity and the type signature (of all its elements).

Tuples are stored in a tuple space, which is basically a non-indexed database, i.e., tuples cannot be accessed directly in the database. Instead, patterns are used to access a subset of matching tuples.

There are basically two basic operations on tuple spaces:

out(t)

A new tuple *t* is stored (written) in the tuple space database. The tuple is fully decoupled from its source agent (there is no information about the source). A tuple exists for a limited time. There can be multiple equal tuples (multiple copies).

inp(p)

A tuple is removed from the tuple space database based on a tuple pattern *p*. The input operation is synchronous and if there is no matching tuple, the calling agent process will be blocked (suspended) until a matching tuple is stored in the database (by another agent or by the host application). The input operation is atomic. At most one tuple is removed.

In addition to the input operation, there is a read operation that does not remove a matching tuple. Instead, a copy is returned. The basic tuple space API is shown in Tab. [6-7](#5_agentjs-api.xhtml_agtupleapi). Blocking operations need a callback handler function that is called if there is a matching tuple found or a time-out occurs. A tuple is an array consisting of actual values (number, string, data record, data array) or a formal parameter represented by a null value. Formal parameters are used in patterns only.

| Operation(s) | Description |
| --- | --- |
| `alt(p [],function)`, `alt.try(tmo,[[]],function)` | Scan for multiple patterns. The first tuple matching one of the patterns is removed from the tuple space and passed to the handler function. |
| `exists(p)` or `test(p)` | Check for the existence of a tuple |
| `inp(p,cb)`, `inp.try(tmo,[],cb)` | Remove a tuple from the database based on pattern matching. The try-version waits a limited time for a matching tuple (or returns immediately with a null value if there is no tuple). |
| `mark(p,tmo)` | Store a temporary tuple in the data base with defined time-out |
| `out(t)` | Store a tuple in the data base |
| `rd(p,cb)`, `rd.try(tmo,[],cb)` | Read a tuple (copy) based on pattern matching. The try-version waits a limited time for a matching tuple (or returns immediately with a null value if there is no tuple). |
| `rm(p,all)` | Remove one or all tuples matching the given pattern. |
| `ts(p,callbackOrTimeout)` | Update a tuple by atomic test and set operation (in-place modification). If the second argument is a function, the tuple is replaced by the returned tuple. If it is a number, then the lifetime of a tuple is set or extended by this time value. |

Table 6-7\. Local tuple space operations (p: pattern, t: tuple)

The `alt` operation allows the listening of multiple tuple patterns. The first tuple that matches a pattern activates the handler function. There is one tuple handler function that is used for all tuple requests. The *alt* operation behaves like the *inp* operator by removing the matching tuple (atomic operation). The test operation can be used to test for a tuple based on a pattern. The test operation returns true if there is actually a matching tuple. After a test operation, a read or input operation can be performed. Since the agents of one physical node are scheduled sequentially, there is no consistency issue by violating atomicity between test and input. Remote tuple spaces can be accessed if the agent has the appropriate rights (privilege level) and if there is a link between its node and the remote node, as shown in Tab. [6-8](#5_agentjs-api.xhtml_agtupleapirem).

| Operation(s) | Description |
| --- | --- |
| `collect(to,p)` | Migrate all matching tuples form this source TS to the remote destination TS. |
| `copyto(to,p)` | Copy all matching tuples form this source TS to the remote destination TS. |
| `store(to,t)` | Store a tuple *t* on node *to* (node identifier). |

Table 6-8\. Remote tuple space operations require a link between source and destination nodes.

Examples of tuple space operations are shown in the following code in Ex. [6-7](#5_agentjs-api.xhtml_agtupleex). The operations should be used in agent activities. Blocking operations with callback functions may not be used in transition and signal handler functions. Operations with a timeout can return a null value, and callback functions have to check for valid tuples.

```
[](#cb29-1)alt.try(500,[
[](#cb29-2)  ['SENSOR',null],
[](#cb29-3)  ['TIME',null],
[](#cb29-4)  ['NODE',100,null]
[](#cb29-5)],(t) => {
[](#cb29-6)  if (!t) return log('timeout');
[](#cb29-7)  switch (t[0]) {
[](#cb29-8)    case 'SENSOR': .. break;
[](#cb29-9)    case 'TIME': .. break;
[](#cb29-10)    case 'NODE': .. break;
[](#cb29-11)  }
[](#cb29-12)})
[](#cb29-13)out(['SENSOR','temp',5000])
[](#cb29-14)mark(['IAMHERE',myid(),mynode()],1000 /*ms*/)
[](#cb29-15)rd(['SENSOR',null],(t) => {
[](#cb29-16)  this.sensor=t[1];
[](#cb29-17)})
[](#cb29-18)rd.try(500,['SENSOR',null],(t) => {
[](#cb29-19)  if (t) this.sensor=t[1];
[](#cb29-20)})
[](#cb29-21)t=rd.try(0,['SENSOR',null]);
[](#cb29-22)inp(['SENSOR',null],(tl) => {
[](#cb29-23)  /* tl is an array of all matching tuples */
[](#cb29-24)},true)
[](#cb29-25)if (test(['SENSOR',100])) { .. }
[](#cb29-26)ts(['SENSOR',100], (t) => {
[](#cb29-27)  /* update tuple in space */
[](#cb29-28)  t[1]++;
[](#cb29-29)  return t
[](#cb29-30)})
```

Example 6-7\. Examples of agent tuple operations

### Signals

In contrast to generative and anonymous tuple communication, signal messages are always sent to a destination with a known address (commonly the agent identifier). Signals are lightweight messages that are sent between two agents, *A* and *B*. The agent can be on different nodes, but at some time in the past they had to be processed by the same node (the crosspoint node). The agents are typically connected by first-order parent-child trees (e.g., *B* is a child of *A* created by forking or cold instantiation from a constructor function).If an agent migrates to another node, the path is remembered for some time (with a node-specific time-out). The delivery of signal messages relies on the migration tables if there is no local destination agent, and the message is forwarded to the next node until no further path elements can be resolved or a maximal hop-count is reached. An example of signalling between parent-child agents is shown in Ex. [6-8](#5_agentjs-api.xhtml_agsigex1). The script code must be executed by the JAM shell program.

| Operation(s) | Description |
| --- | --- |
| `send(to,sig,arg)` | Send a signal message of type *sig* to agent *to* with an optional argument *arg*. |
| `broadcast(ac,range,sig,arg)` | Send a signal message of type *sig* to agents of class *ac* in the given range hops with an optional argument *arg*. |
| `on."SIGNAL" : function (arg,from)` | Signals can only be received by installed agent signal handlers (in the *on* section). The signal name is the handler name attribute. |

Table 6-9\. Signal operations

In the following Ex. [6-8](#5_agentjs-api.xhtml_agsigex1), a simple ping-pong signal messaging example between a parent and child agent pair is shown. Two agents are created, passing the identifier name of the first to the second agent, enabling the sending of an addressed signal.

```
[](#cb30-1) 1: function ac(config) {
[](#cb30-2) 2:   this.parent = config.parent;
[](#cb30-3) 3:   this.act = {
[](#cb30-4) 4:     init: () => {
[](#cb30-5) 5:       log('START',this.parent);
[](#cb30-6) 6:       if (this.parent) 
[](#cb30-7) 7:         send(this.parent,'PING',random(0,100));
[](#cb30-8) 8:     },
[](#cb30-9) 9:     wait : () => { sleep(5000) },
[](#cb30-10)10:     end : () => { log('END'); kill() }
[](#cb30-11)11:   }
[](#cb30-12)12:   this.trans = {
[](#cb30-13)13:     init : wait,
[](#cb30-14)14:     wait : end,
[](#cb30-15)15:   }
[](#cb30-16)16:   this.on = {
[](#cb30-17)17:     'PING' : (arg,from) => {
[](#cb30-18)18:       log('PING',arg,from);
[](#cb30-19)19:       send(from,'PONG',random(0,100));
[](#cb30-20)20:     },
[](#cb30-21)21:     'PONG' : (arg,from) => {
[](#cb30-22)22:       log('PONG',arg,from);
[](#cb30-23)23:     }, 
[](#cb30-24)24:   }
[](#cb30-25)25:   this.next = 'init';
[](#cb30-26)26: }
[](#cb30-27)27: compile(ac,0,true);
[](#cb30-28)28: var ag1 = create('ac',{});
[](#cb30-29)29: var ag2 = create('ac',{parent:ag1});
[](#cb30-30)30: start()
```

Example 6-8\. A simple ping-pong signal messaging example between a parent and child agent pair.

## Agent Mobility

An agent can migrate from its current node to another (remote) node. This operation requires an established virtual link between the source and destination nodes. A node link can be tested by using the `link` operation. The `link` operation can be used to get all current links, too. In IP networks, the `link(DIR.IP("%"))` call returns the node identifier names, and `link(DIR.IP("*"))` returns the URL addresses of the currently linked nodes. The operations are summarized in Tab. [6-10](#5_agentjs-api.xhtml_agmobapi). Different directions specifying destination nodes used by these operations are summarized in Def. [6-2](#5_agentjs-api.xhtml_dirlinkapi). Some direction flags are static values without a parameter, some are functions returning a parametrized direction. The often used `DIR.IP()` direction expects a pattern or URL parameter. If the destination node name is known, the `DIR.NODE(name)` direction function can be used to test the link or migrate to this node. The host program or level 3 agents can connect their JAM node to a remote node, typically using IP-based AMP links and the `DIR.IP(proto://host:port)` destination direction.

| Operation(s) | Description |
| --- | --- |
| `moveto(dir)` | Send this agent to new destination node specified by *dir*. |
| `link(dir)` | Test a link to a node or returns current link information. |
| *dir* ∈ `DIR` | Link destination direction object |

Table 6-10\. Agent mobility operations; link directions are defined below.

```
[](#cb31-1)type DIR = {
[](#cb31-2)  NORTH, SOUTH,
[](#cb31-3)  WEST,  EAST,
[](#cb31-4)  LEFT,  RIGHT,
[](#cb31-5)  UP,    DOWN,
[](#cb31-6)  ORIGIN,
[](#cb31-7)  NW, NE, SW, SE,
[](#cb31-8)  BACKWARD,
[](#cb31-9)  FORWARD,
[](#cb31-10)  OPPOSITE,
[](#cb31-11)  // Assuming:  z-> x     N
[](#cb31-12)  //            |        W+E  U(+z)/D(-z)
[](#cb31-13)  //            v y       S
[](#cb31-14)  DELTA: function (addr) → {tag:"DIR.DELTA",delta:addr},
[](#cb31-15)  // Only for link? operation
[](#cb31-16)  RANGE: function (r) → {tag:"DIR.RANGE",radius:r}, 
[](#cb31-17)  // Address a node (identifier name) directly
[](#cb31-18)  NODE: function (node) → {tag:"DIR.NODE",node:node},
[](#cb31-19)  // Patterns: %:Node names; *:URLs
[](#cb31-20)  IP:function (addr) → {tag:"DIR.IP",ip:addr},
[](#cb31-21)  // Path can contain filters, 
[](#cb31-22)  // e.g. range /distance[0-5], /distance[5], .. 
[](#cb31-23)  // or a pattern for a set of destinations, e.g., /node*
[](#cb31-24)  // or a hopping array [dest1,dest2,..]
[](#cb31-25)  // type of path = string | string array
[](#cb31-26)  PATH:function (path) → {tag:"DIR.PATH",path:path},
[](#cb31-27)  CAP:function (cap) → {tag:"DIR.CAP",cap:cap}
[](#cb31-28)}
```

Definition 6-2\. Possible link and destination directions used by the connect, move-to, and link operations. The first set is used only in mesh-like networks (primarily in virtual node networks like in the simulator)

A simple moving agent is shown in Ex. [6-9](#5_agentjs-api.xhtml_agexmove1). The identifier names of the current IP-linked nodes are returned by the `link(DIR.IP('%'))` function call. A node is randomly chosen, and the agent migrates to the new node in the activity *move*, and back to its root node in the activity *back*.

```
[](#cb32-1)function ag() {
[](#cb32-2)  this.goto=null;
[](#cb32-3)  this.root=null;
[](#cb32-4)  this.act = {
[](#cb32-5)    check: () => {
[](#cb32-6)      this.root=myNode();
[](#cb32-7)      var links=link(DIR.IP('%'));
[](#cb32-8)      if (links && links.length) 
[](#cb32-9)        this.goto=random(links);
[](#cb32-10)      else sleep(500);
[](#cb32-11)    },
[](#cb32-12)    move: () => {
[](#cb32-13)      moveto(DIR.NODE(this.goto))
[](#cb32-14)    },
[](#cb32-15)    back: () => {
[](#cb32-16)      moveto(DIR.NODE(this.root)) 
[](#cb32-17)    },
[](#cb32-18)    end: () => {
[](#cb32-19)      log('Terminating');
[](#cb32-20)      kill();
[](#cb32-21)    },
[](#cb32-22)  }
[](#cb32-23)  this.trans = { 
[](#cb32-24)    check:() => { 
[](#cb32-25)     return this.goto?'move':'check' },
[](#cb32-26)    move:'back',
[](#cb32-27)    back:'end' }
[](#cb32-28)  this.next = 'check';
[](#cb32-29)}
```

Example 6-9\. An agent visiting a neighbour node and returning to its root node.

## Machine Learning

The fusion of agent and machine learning models creates learning agents. The ML module part of JAM provides a broad range of machine learning algorithms, including reinforcement learning. The ML module provides the algorithms. Most (but not all) models used by the algorithms are pure non-cyclic data objects that are mobile, i.e., the models can be carried by migrating agents and further processed on another node.

An agent (with at least privilege level 1) can access the ML module through the `ml` root object. The type signature of the ML module is shown in Def. [6-3](#5_agentjs-api.xhtml_agentjsml). The ML module consists of data analysis functions (*stats* object) and a set of generic ML operations, primarily: *learn*, which immediately creates an ML model from data (e.g., in the case of decision trees), *train*, which applies training to an already created model (e.g., ANN), and *predict*, which applies a trained model to new data. Some models can be updated (e.g., the Reinforcement Learner) by the *update* operation. There is a large set of ML algorithms covered by the generic operations, which can be selected by the `ml.ML` entries.

```
[](#cb33-1)type ml = { action: [Function: action],
[](#cb33-2)  classify: [Function: classify],
[](#cb33-3)  compact: [Function: compact],
[](#cb33-4)  depth: [Function: depth],
[](#cb33-5)  evaluate: [Function: evaluate],
[](#cb33-6)  info: [Function: info],
[](#cb33-7)  learn: [Function: learn],
[](#cb33-8)  learner: [Function: learn],
[](#cb33-9)  noise: [Function: noise],
[](#cb33-10)  preprocess: [Function: preprocess],
[](#cb33-11)  print: [Function: print],
[](#cb33-12)  similarity: [Function: similarity],
[](#cb33-13)  stats: 
[](#cb33-14)   { analyze: [Function: analyze],
[](#cb33-15)     entropy: [Function: entropy],
[](#cb33-16)     entropyN: [Function: entropyN],
[](#cb33-17)     entropyEps: [Function: entropyEps],
[](#cb33-18)     entropyTEps: [Function: entropyTEps],
[](#cb33-19)     entropyT: [Function: entropyT],
[](#cb33-20)     features: [Function: features],
[](#cb33-21)     gainEps: [Function: gainEps],
[](#cb33-22)     maxGainEps: [Function: maxGainEps],
[](#cb33-23)     mostCommon: [Function: mostCommon],
[](#cb33-24)     partition: [Function: partition],
[](#cb33-25)     partitionEps: [Function: partitionEps],
[](#cb33-26)     partitionUniqueEps: [Function: partitionUniqueEps],
[](#cb33-27)     splitEps: [Function: splitEps],
[](#cb33-28)     unique: [Function: unique],
[](#cb33-29)     uniqueEps: [Function: uniqueEps],
[](#cb33-30)     utils: 
[](#cb33-31)      { best: [Function: best],
[](#cb33-32)        bestNormalize: [Function: bestNormalize],
[](#cb33-33)        column: [Function: pluck],
[](#cb33-34)        log2: [Function: log2],
[](#cb33-35)        prob: [Function: prob],
[](#cb33-36)        relax: [Function: relax],
[](#cb33-37)        select: [Function: select],
[](#cb33-38)        selectEps: [Function: selectEps],
[](#cb33-39)        sort: [Function: sort],
[](#cb33-40)        stat: [Object],
[](#cb33-41)        without: [Function: without],
[](#cb33-42)        wrap: [Function: wrap] } },
[](#cb33-43)  test: [Function: test],
[](#cb33-44)  update: [Function: update],
[](#cb33-45)  // supported model/algorithm types
[](#cb33-46)  ML: 
[](#cb33-47)   { ANN: 'ann',         C45: 'c45',
[](#cb33-48)     CNN: 'cnn',         ICE: 'ice',
[](#cb33-49)     DTI: 'dti',         ID3: 'id3',
[](#cb33-50)     KMN: 'kmeans',      KNN: 'knn',
[](#cb33-51)     KNN2: 'knn2',       MLP: 'mlp',
[](#cb33-52)     RF: 'rf',           RL: 'rl',
[](#cb33-53)     SLP: 'slp',         SVM: 'svm',
[](#cb33-54)     TXT: 'txt',         EUCL: 'euclidean',
[](#cb33-55)     PEAR: 'pearson',    DPAgent: 'DPAgent',
[](#cb33-56)     TDAgent: 'TDAgent', DQNAgent: 'DQNAgent' },
[](#cb33-57)  predict: [Function: classify],
[](#cb33-58)  train: [Function: learn],
[](#cb33-59)  best: [Function: best] }
```

Definition 6-3\. The type signature of the AgentJS Machine Learning module

Some selected models and algorithms are presented in the next sub-sections.

### Decision Tree

There are different decision tree learners (see Def. [6-4](#5_agentjs-api.xhtml_dttmpl) and [6-5](#5_agentjs-api.xhtml_dtitmpl)), mainly C45, ID3, and a confidence interval decision tree model DTI based on interval arithmetic. To process input variables with a noise interval [x-εx+ε], interval arithmetic is used. Values with overlapping intervals are considered equal and do not contribute to an information gain. The noise (variable variance or standard deviation) values must be provided by the user. Either one value is provided for all input variables or one value for each input variable (array of ε values).

```
[](#cb34-1)xy=[{a:..,b:,..,..,y:..},{...},...]
[](#cb34-2)model = ml.learn({
[](#cb34-3) algorithm:ml.ML.C45, // ID3
[](#cb34-4) data:xy,
[](#cb34-5) target:'y',
[](#cb34-6) features:['a','b',..]
[](#cb34-7)})
[](#cb34-8)result = ml.classify(model,xy[0]) 
```

Definition 6-4\. C45/ID3 template (input variables can be numbers, strings, or Booleans; output variables are always strings)

```
[](#cb35-1)x=[[...],[...],..]
[](#cb35-2)y=['a','b',..]
[](#cb35-3)model = ml.learn({
[](#cb35-4)  algorithm:ml.ML.DTI,
[](#cb35-5)  x:x, 
[](#cb35-6)  y:y,
[](#cb35-7)  eps:number // or [e1,e2,...]
[](#cb35-8)});
```

Definition 6-5\. Basic DTI template (input variables may only be numbers, output variable is always a string type)

### Multi-layer Perceptron

The MLP model (see Def. [6-6](#5_agentjs-api.xhtml_mlptmpl)) is a fully connected neural network with hidden layers. The model is portable (mobile) and can be carried by mobile agents. The model can be trained on creation using the `ml.learner` function at once or iteratively using the *ml.train* function. Training of MLP models can be time-consuming and should be split into multiple activity runs (otherwise the activity processing can be terminated by the scheduler). The return of the training function delivers the current *loss* value and the time consumed by the training run. More information can be found in [STA09].

```
[](#cb36-1)x=[[...],[...],..]
[](#cb36-2)xo=[{...},{...},..]
[](#cb36-3)y=['a','b',..]
[](#cb36-4)model = ml.learner({
[](#cb36-5)        x:x, // alternative: xo,
[](#cb36-6)        y:y,
[](#cb36-7)        features:['x1','x2',...],
[](#cb36-8)        labels:['a','b',...],
[](#cb36-9)        hidden_layers : [4,4,5],
[](#cb36-10)        algorithm:ml.ML.MLP,
[](#cb36-11)        normalize:true,
[](#cb36-12)        bipolar:true,
[](#cb36-13)        verbose:1
[](#cb36-14)      });
[](#cb36-15)result = ml.train(model,{
[](#cb36-16)  epochs:1000,
[](#cb36-17)}) // -> { time, epochs, loss }
[](#cb36-18)result = ml.classify(model,x[0]) 
```

Definition 6-6\. Basic MLP template

### Support Vector Machine

The Support Vector Machine (SVM) is a binary classificator, although, it can be used for regression problems, too. Multi-label classification is established with a set of *n* binary classifiers for *n* different target variable classes. The SVM model is portable, too, and can be carried by mobile agents or inherited by child agents. The SVM can use different kernels, e.g., polynomial or "rbf". Details of the algorithm and its parameters can be found at [https://github.com/karpathy/svmjs](https://github.com/karpathy/svmjs). The basic SVM template for creating a trained model is shown in Def. [6-7](#5_agentjs-api.xhtml_svmtmpl). The input data does not need to be normalized.

```
[](#cb37-1)x=[[number,...],[...],..]
[](#cb37-2)y=[number �� {-1,1},..]
[](#cb37-3)// Binary SVM
[](#cb37-4)var model = ml.learn({
[](#cb37-5)    algorithm : ml.ML.SVM,
[](#cb37-6)    x : x,
[](#cb37-7)    y : y,
[](#cb37-8)
[](#cb37-9)    C : number, 
[](#cb37-10)    // default : 1.0\. C in SVM.
[](#cb37-11)    tol : number, 
[](#cb37-12)    // default : 1e-4\. Higher tolerance --> 
[](#cb37-13)    //                 Higher precision
[](#cb37-14)    max_passes : number, 
[](#cb37-15)    // default : 20\. Higher max_passes -->
[](#cb37-16)    //               Higher precision
[](#cb37-17)    alpha_tol : number, 
[](#cb37-18)    // default : 1e-5\. Higher alpha_tolerance --> 
[](#cb37-19)    //                 Higher precision
[](#cb37-20)
[](#cb37-21)    //kernel : { type: "polynomial", c: 1, d: 5}
[](#cb37-22)    kernel : { type: "rbf", sigma:0.5 }
[](#cb37-23)});
[](#cb37-24)result = ml.classify(model,x[0])
[](#cb37-25)// Multiclass SVM
[](#cb37-26)x=[[number,...],[...],..]
[](#cb37-27)y=['A','B',..]
[](#cb37-28)var model = ml.learn({
[](#cb37-29)    algorithm : ml.ML.SVM,
[](#cb37-30)    x : x,
[](#cb37-31)    y : y,
[](#cb37-32)    labels:['A','B',..],
[](#cb37-33)
[](#cb37-34)    threshold:boolean, 
[](#cb37-35)    // false:no threshold function on output; 
[](#cb37-36)    // highest value of svms is winner
[](#cb37-37)    ..
[](#cb37-38)}
[](#cb37-39)// classify returns {value:string,prob:number}[] arrays
[](#cb37-40)var winner = ml.stats.utils.best(
[](#cb37-41)  ml.classify(model,x[0])
[](#cb37-42))
```

Definition 6-7\. Basic SVM template

### Reinforcement Learner

The Reinforcement Learner (RL) is closely related to the concept of the adaptive behaviour of agents. The RL trainer needs an environment with helper functions. The state is a numerical value as well as the reward. More information can be found in [KAP15]. The action itself is not visible to the RL and is considered symbolic. The model is portable (pure data) and can be carried by mobile agents. A basic RL template is shown in Def. [6-8](#5_agentjs-api.xhtml_rltmpl). It is made up of an environment with some pre-defined functions and an update loop that repeatedly performs the *action*, *nextState*, *reward*, and *update* sequences.

```
[](#cb38-1)actions = ['a','b',..]
[](#cb38-2)env = {
[](#cb38-3)  // return allowed actions in current state
[](#cb38-4)  allowedActions : (state) => { 
[](#cb38-5)  },
[](#cb38-6)  // state transition functioin
[](#cb38-7)  nextState : (state,action) => {
[](#cb38-8)    return state
[](#cb38-9)  },
[](#cb38-10)  getNumStates : () => { return number},
[](#cb38-11)  getMaxNumActions : () => { return number},
[](#cb38-12)  // compute the reward of the state transitions and action
[](#cb38-13)  reward : (state,action,nextstate) => {
[](#cb38-14)    return number
[](#cb38-15)  },
[](#cb38-16)}
[](#cb38-17)model = ml.learn({
[](#cb38-18)  algorithm   : ml.ML.RL,
[](#cb38-19)  kind        : ml.ML.TDAgent,
[](#cb38-20)  actions     : actions,
[](#cb38-21)  // specs
[](#cb38-22)  // function learning rate
[](#cb38-23)  alpha       : 0.1, 
[](#cb38-24)  // learning rate for smooth policy update
[](#cb38-25)  beta        : 0.2, 
[](#cb38-26)  // initial epsilon for epsilon-greedy policy, [0, 1)
[](#cb38-27)  epsilon     : 0.2, 
[](#cb38-28)  // discount factor, [0, 1)
[](#cb38-29)  gamma       : 0.5, 
[](#cb38-30)  // eligibility trace decay, [0,1). 0 = no eligibility traces
[](#cb38-31)  lambda      : 0, 
[](#cb38-32)  // number of planning steps per iteration. 0 = no planning
[](#cb38-33)  planN       : 5, 
[](#cb38-34)  replacing_traces : true,
[](#cb38-35)  smooth_policy_update : false,
[](#cb38-36)  update : 'qlearn',  // 'qlearn' or 'sarsa'
[](#cb38-37)  environment : env
[](#cb38-38)})
[](#cb38-39)while () {
[](#cb38-40)  action = ml.action(model,state);
[](#cb38-41)  next = env.nextState(state,action);
[](#cb38-42)  reward = env.reward(next)
[](#cb38-43)  ml.update(model,reward)
[](#cb38-44)  state = next
[](#cb38-45)}
```

Definition 6-8\. Basic RL template

# JAM for Users and Programmers

The core JAM modules, entirely programmed in JavaScript, can be embedded in any application programs capable to process at least the ECMAscript 2015 standard. To ease programming and agent deployment, the core modules are encapsulated in a library providing a unified API. In addition to the core library used for development of custom applications, there are pre-built application programs:

1.  JAM shell (command line and Web browser versions);
2.  Mobile JAM App (Cordova and Web browser versions);
3.  JAM Web laboratory (Web browser);
4.  SEJAM (node-webkit and Web browser versions).

The following section introduce the use of and programming with the library and the programs. The JAM shell *jamsh* is the main programming and deployment platform. There is a JAM library version for command line applications (using node.js) and for the Web browser, with nearly the same API.

## JAM Library

The library version of *JAM* contains a full agent processing VM with the *AIOS* as the central component, enabling embedding of *JAM* in any host application, including Web HTML pages. A public API is used to create and control *JAM* node instances. Each instance is an object that provides a set of API methods to control the JAM instance and to connect the instance to other nodes. There are two slightly different versions of the *jamlib* targeting:

1.  Server side and terminal versions that support node.js [NOD22], jerryscript [JER22], and quickjs [QUI22];
2.  Client-side version that works with any browser that supports JS processing and Cordova-based apps for smartphones.

A JAM object instance is created by calling the `Jam` constructor function, shown in the code template in Def. [7-1](#6_jam-for-users-and-programmers.xhtml_jamlibdef1). A selection of JAM library object methods (instantiated by the *Jam* constructor function) is shown in Tables [7-1](#6_jam-for-users-and-programmers.xhtml_jamlibmeth1) and [7-2](#6_jam-for-users-and-programmers.xhtml_jamlibmeth2).

```
[](#cb39-1) 1: var JAM = require('jamlib.js');
[](#cb39-2) 2: // Browser: <script src="jamlib.browser.js">
[](#cb39-3) 3: // Create a JAM instance with a virtual world 
[](#cb39-4) 4: // containing one initial virtual node
[](#cb39-5) 5: var jam    = JAM.Jam({}), // Browser: JAMLIB.
[](#cb39-6) 6:     DIR    = jam.DIR;
[](#cb39-7) 7: jam.init();
[](#cb39-8) 8: jam.locate(); // start multi-stage geolocation
[](#cb39-9) 9: // Start the JAM scheduler loop
[](#cb39-10)10: jam.start();
[](#cb39-11)11: // Define an agent constructor function
[](#cb39-12)12: function foo(p) { 
[](#cb39-13)13:   this.x=p; 
[](#cb39-14)14:   this.act={..}; 
[](#cb39-15)15:   this.trans={..}; 
[](#cb39-16)16:   .. }
[](#cb39-17)17: // Compile the agent constructor
[](#cb39-18)18: jam.compileClass(foo,{verbose:1});
[](#cb39-19)19: // Instantiate agents from class constructor
[](#cb39-20)20: // with specific AIOS level
[](#cb39-21)21: var a1 = jam.createAgent('foo',[args],1);
[](#cb39-22)22: var a2 = jam.createAgent('foo',[args],1);
[](#cb39-23)23: // Create AMP HTTP port (communication endpoint)
[](#cb39-24)24: jam.createPort(DIR.IP('http://localhost:*'))
[](#cb39-25)25: // Connect to external node
[](#cb39-26)26: jam.connectTo(DIR.IP('http://ag-0.de:30002?secure=12:..'))
```

Definition 7-1\. JAM node instantiation and agent creation using the JAM library

The *compileClass* function creates and installs the sandbox-restricted agent constructor functions for each privilege level with a different operational AIOS function set. The *createAgent* function instantiates an agent from the already sandbox-restricted agent class constructors with a specific parameter set and a specific AIOS level (here 1).

The AIOS can be easily extended using the *extend* method, e.g., by adding natural language processing or logic solver APIs.

| Method | Parameter | Description |
| --- | --- | --- |
| `addClass` | *name*, *constructor*, *env* | Create sandbox constructors and add agent class to the JAM world. |
| `addNode` | *nodeDesc*: {x,y,id?} | Add a new node to the world. Assumption: 2D mesh-grid network with (x,y) coordinates. The root node has position {x=0,y=0} |
| `analyze` | *ac*, *options* | Analyze agent class template in text or object form |
| `compileClass` | *name*, *constructor*, *options* | Analyse and compile an agent class constructor function and add it to the world class library |
| `connectNodes` | *nodes*: {x,y} [] | Connect logical nodes (virtual link) |
| `connected` | *dir*, *nodeid*? | Check connection status of a link |
| `createAgent`, `createAgentOn` | (*nodeid*), *ac*, *args*, *level*, *className*, *parent*? | Create and start an agent from class ac with arguments |
| `createPort` | *dir*, *options*, *nodeid* | Create a physical communication port |
| `disconnect` | *dir*, *nodeid* | Disconnect remote endpoint |
| `extend` | *level*, *name*, *funcOrObj*, *argn* | Extend the AIOS agent API |
| `info` | *kind*, *id* | Get info about nodes, agents, and the host platform |
| `kill` | *id*, *nodeid* | Kill agent with specified id ("*": kill all agents on node or current node) |
| `locate` | *nodeid*, *callback*, *options* | Try to locate this node (based on network connectivity) and get geospatial position |
| `inp`, `mark`, `out`, `rd`, `ts` | - | Tuple space operation applied to current node |
| `saveSnapshot`, `saveSnapshotOn` | *agentid*, *nodeid*, .. | Take an agent process snapshot executed currently on given node (returned as string or saved in file) |
| `setCurrentNode` | *nodeid* | Set current v-JAM node |
| `signal` | *to*, *sig*, *arg*, *broadcast* | Send a signal to a specific agent or broadcast |

Table 7-1\. Selection of JAM library operational methods

| Method | Parameter | Description |
| --- | --- | --- |
| `init` | *callback* | Create and initialize node(s)/world, add optional TS provider/consumer, create physical network connections |
| `schedule` | - | Force a scheduler run immediately, as normally executed by the jam service loop, required if there was external agent management, e.g., by sending signals |
| `start0`, `start`, `stop` | *callback* | Start or stop JAM (0: without scheduler loop for single stepping) |
| `step` | *steps*, *callback* | Stepping the scheduler loop |

Table 7-2\. JAM library control methods

The JAM run-time supports two scheduling modes: Free running and single stepping. In free running mode, the scheduler determines the next schedule loop execution time based on pending events and ready agents (with a pending transition). In single step mode, only a fixed number of scheduler loop runs will be processed. This feature is used for debugging and simulation. The scheduler can only calculate the next loop execution time on events originating from agents (e.g., by calling the *sleep* operation). Externally introduced events require a forced scheduler run (by using the *schedule* operation).

The following Ex. [7-1](#6_jam-for-users-and-programmers.xhtml_jamlibweb) shows the embedding of the JAM library in an HTML page. The browser version of the JAM library is accessible via the global `JAMLIB` object.

```
[](#cb40-1) 1: <html>
[](#cb40-2) 2: <head>
[](#cb40-3) 3: <script src="jamlib.browser.js"></srcipt>
[](#cb40-4) 4: </head>
[](#cb40-5) 5: <body>
[](#cb40-6) 6: <script>
[](#cb40-7) 7: /* Object { Aios: Object, 
[](#cb40-8) 8:             Comp: Object, Esprima: Object, 
[](#cb40-9) 9:             Io: Object, Jam: function, 
[](#cb40-10)10:             Json: Object, 
[](#cb40-11)11:             environment: Object, 
[](#cb40-12)12:             options: Object }
[](#cb40-13)13: */
[](#cb40-14)14: var jam    = JAMLIB.Jam({}),
[](#cb40-15)15:     DIR    = jam.DIR;
[](#cb40-16)16: jam.Aios.Mobi.options.debug.move=1;
[](#cb40-17)17: jam.init();
[](#cb40-18)18: jam.locate(); // Start multi-stage geolocation
[](#cb40-19)19: // Start the JAM scheduler loop
[](#cb40-20)20: jam.start();
[](#cb40-21)21: jam.extend([1,2,3],'DOM',function (cmd,tag,content) {
[](#cb40-22)22:   switch (cmd) {
[](#cb40-23)23:     case 'agent': return navigator.userAgent;
[](#cb40-24)24:     case 'get': return document.getElementById(tag);
[](#cb40-25)25:   }
[](#cb40-26)26: },[2,3])
[](#cb40-27)27: if (document.URL.indexOf('https')==0) {
[](#cb40-28)28:   jam.createPort(DIR.IP('https://localhost:*'))
[](#cb40-29)29:   jam.connectTo(DIR.IP('https://ag-0.de:30001?secure=12:..'))
[](#cb40-30)30: } else {
[](#cb40-31)31:   jam.createPort(DIR.IP('http://localhost:*'))
[](#cb40-32)32:   jam.connectTo(DIR.IP('http://ag-0.de:30002?secure=12:..'))
[](#cb40-33)33: }
[](#cb40-34)34: function foo(opts) {
[](#cb40-35)35: ...
[](#cb40-36)36: }
[](#cb40-37)37: jam.compileClass(foo,{verbose:1});
[](#cb40-38)38: var foody = jam.createAgent('foo',{},2);
[](#cb40-39)39: </body>
[](#cb40-40)40: </html>
```

Example 7-1\. Basic usage of the JAM library (Browser version) embedded in an HTML Web pageExercise 7-1\. Web Page with JAM

1.  Start a *jamsh* instance on your computer (or any other computer on your network) by executing a script that creates an HTTP port and starts JAM: `port(DIR.IP('http://localhost:4567')); start()`. Read the next section, too.
2.  Use the above example code template. Replace the *connectTo* URL with the port number of your Jamsh instance. Create a simple notification agent that is created on page opening. The notification agent should sample the browser navigator agent string (via a `DOM("agent")` call), finally migrating to the shell node. The agent should print (log) the sampled sensor.
3.  Extend the shell script with a collector agent that waits for tuple messages containing the navigator agent strings (e.g., `inp(["BROAGENT",_],..)`. Each notification agent delivers its sampled sensor value via the tuple space (e.g., `out(["BROAGENT",v]`). The collector agent should report each new delivered sensor sample, finally creating statistics of the samples (percentage of occurence of a specific operating system, browser software, and so on).

Commonly, the embedded JAM node connects via AMP to an external public JAM node. Note that only HTTP and HTTPS are supported protocols, which must be supported by the remote node via respective ports. Additionally, if the Web page is loaded via HTTP, the HTTP must be used for AMP, too, otherwise HTTPS (mixed HTTP/HTTPS requests with respect to the page origin are commonly rejected by the browser), shown in lines 27-33 in Ex. [7-1](#6_jam-for-users-and-programmers.xhtml_jamlibweb).

Note that the Web page installs a sleep hack (`HackTimer.js` [TRU22] embedded in the `jamlib.browser.js` file). Web pages and timers are throttled and delayed by the browser program if the page is not visible, e.g., by switching the browser tab or just by hiding the browser window. This applies both to desktop and mobile devices. This leads to a shutdown of the JAM logic, which causes a lot of time-out issues. The HackTimer moves critical timers to a WebWorker context that will typically not be throttled by the browser. Alternatively, the JAM VM can be executed in a WebWorker, requiring some additional WebWorker logic.

A JAM instance on a Web page is only alive as long as the Web page is opened. After closing the page, the JAM state is lost, including all its agents. One potential solution to overcome this limitation is the migration of JAM to service workers. Service workers are executed independently of the root Web page. Typically, after closing the Web page, the service worker can run for up to 30 seconds until it is stopped. After the same Web page is opened again (same URL), the service worker is restarted. To create a snapshot of JAM, all agents must be serialized (process snapshot like for migration). The node snapshot requires at least the serialization of the tuple space content and the agent class constructor dictionary. The serialized code and data can be stored permanently (or temporarily) in the Web storage of the Web browser.

## JAM Shell

The JAM shell (`jamsh`) is a command line API for JAM basically providing a REPL and script wrapper for the JAM library. It provides a typical script-based programming interface to the underlying agent machine, easing the creation and control of agents, composing JAM networks and connecting JAM nodes, and so on. JAM scripts can be either loaded and processed directly from a file and/or by typing commands in the REPL shell. Agent class constructors can be loaded from files, compiled from functions, or interpreted from any text representation. There is a simplified and restricted Web version of the JAM shell, too, basically with restrictions due to connectivity (HTTP only) and missing watchdog protection.

### Shell Commands

Shell commands, either provided by the shell command line or executed in a script file, are summarized in Tab. [7-3](#6_jam-for-users-and-programmers.xhtml_jamshcmd). Most functions and procedures are directly related to the AIOS and *jamlib* API.

| Command(s) | Description |
| --- | --- |
| `add(x,y)` | Add a new logical (virtual) node |
| `agent(id,proc?)` | Returns the agent object (or process) |
| `agents()` | Get all agents (id list) of current node |
| `args` | Script arguments |
| `ask(question,choices)` | Ask a question and read answer. Available only in script mode. |
| `array`, `assign`, `contains`, `concat`, `copy`, `empty`, `filter`, `last`, `merge`, `neg`, `object`, `pluck`, `random`, `select`, `without` | Array, matrix, object, and math functions |
| `Capability`, `Port`, `Private` | Create a security capability object, port, and private field |
| `clock(milli), time()` | Return system time (ms or hh:mm:ss format using the clock function) |
| `cluster(desc)` | Create a worker process cluster |
| `config(options)`, `configs` | Configure JAM. Options: print, printAgent, TSTMO, .., and return configuration of JAM AIOS |
| `connect({x,y},{x,y})`, `connect(to)`, `disconnect({x,y},{x,y})`, `disconnect(to)`, `connected(to)` | Connect two logical nodes (DIR.NORTH...), connect to a physical node, disconnect, and check a connection to specified destination. |
| `compile(f,options)`, `open(file)` | Compile an agent class constructor function; open and compile agent class file; |
| `create(ac, args, level,node)`, `kill(id)` | Create an agent from class @ac with given arguments @args and @level optionally on @node (return agent id); kill an agent |
| `extend(level,name,argn)` | Extend the AIOS for one or more privilege levels |
| `http`, `https` | HTTP and HTTPS client and server objects supporting get, GET (JSON), put, PUT (JSON), and server operations. |
| `info(what,id)` | Return node information object ('node', 'version', 'host') |
| `inp(p,all)`, `mark(t,tmo)`, `out(t)`, `provider(cb)`, `rd(p,all)`, `rm(p,all)`, `test(p)` | Read and remove (a) tuple(s) from the tuple space (non-blocking); store a timeout-limited tuple; store a tuple in the current node TS; installation of a tuple provider and consumer handler; read a tuple from the TS; remove tuples; test for tuple(s); |
| `later(tmo,cb)` | Execute a function later. If the function returns a true value, the next timer is started. |
| `node(id)`, `nodes`, `name`, `world` | Get or set current v-node; return all v-node ids; return name of current node; return current world object |
| `on(ev,handler)` | Install an event handler. Events: "agent+","agent-","signal+","signal","link+","link-","exit" |
| `port(dir, options:{proto,secure}, node)` | Create a new physical communication port |
| `setlog(flag,val)` | Enable or disable logging features |
| `signal(t,sig,arg)` | Send a signal to specified agent |
| `sleep(milli)` | Suspend entire shell for seconds |
| `start()`, `stop()` | Start and stop JAM scheduler (and other services) |
| `uniqid(options)` | Return a random name |
| `utime()` | Return high resolution system time in nanoseconds |

Table 7-3\. Common JAM shell commands

A subset of the shell commands are available to agents, too, e.g., tuple space operations or the ML module *ml*. But there are no blocking operations (except *ask*). All asynchronous operations require a callback function.

### Ports and Links

A link between two (physical) nodes requires the setup of a communication port using the `port` operation. Typically, IP networks are used to establish JAM node links. At least one node needs a static IP port. A link is established by using the `connect` operation, shown in Def. [7-2](#6_jam-for-users-and-programmers.xhtml_jamshports).

```
[](#cb41-1)// Node A
[](#cb41-2)┌ var sport = Port.ofString('12:34:56:78')
[](#cb41-3)│ port(DIR.IP('http://localhost:4567'))
[](#cb41-4)│ // with a secure port, two alternative formats
[](#cb41-5)│ port(DIR.IP('http://localhost:5567?secure=12:..'))
[](#cb41-6)└ port(DIR.IP('http://localhost:6567'),{secure:sport})
[](#cb41-7)// Node B
[](#cb41-8)┌ port(DIR.IP('http://localhost:*'))
[](#cb41-9)│ connect(DIR.IP('http://localhost:4567'));
[](#cb41-10)│ // with secure port
[](#cb41-11)└ connect(DIR.IP('http://localhost:5567?secure=12:..'));
```

Definition 7-2\. Creation of IP ports and establishment of links between nodes. Ports can be protected by capability ports or by any string secret key

Instead, using HTTP for AMP communication, UDP and TCP can be used as well. The protocol can be directly set by the direction IP URL, e.g., `port(DIR.IP('udp://localhost:4567'))`. Note that Web browsers only support HTTP communication. A JAM shell can act as an agent relay node just by creating IP ports publicly visible. Any JAM node with Internet connectivity can connect to this node via AMP the *connect* operation. JAM nodes can be connected by (level-3) agents, too, using the *connectTo* operation.

Ports can be configured with a set of parameters changing the internal data flow and control, as shown in Def. [7-3](#6_jam-for-users-and-programmers.xhtml_ampportsprotos). The AMP ports can be unicast or multicast.A multicast port supports multiple links from remote node ports, and multiple links to this port. IP ports are typically multicast ports. In addition, AMP ports can be unidirectional or bidirectional.

```
[](#cb42-1) 1: port(DIR.IP('udp://...'),{
[](#cb42-2) 2:   secure?:string,
[](#cb42-3) 3:   oneway?:boolean,       // default:false
[](#cb42-4) 4:   multicast?:boolean,    // default:true
[](#cb42-5) 5:   snd?:{address,port},   // fixed destination 
[](#cb42-6) 6:   verbose?:number
[](#cb42-7) 7: })
[](#cb42-8) 8: port(DIR.IP('tcp://...'),{
[](#cb42-9) 9:   // Default for a link: pair of 
[](#cb42-10)10:   // uni-directional ad-hoc TCP sessions
[](#cb42-11)11:   keepAlive?:boolean,    // true:permanent TCP sessions 
[](#cb42-12)12:   sharedSocket?:boolean, // implies keepAlive
[](#cb42-13)13:   multicast?:boolean,    // default:true, 
[](#cb42-14)14:                          // false for NORTH,...
[](#cb42-15)15:   oneway?:boolean,       // default:false
[](#cb42-16)16:   secure?:string,
[](#cb42-17)17:   snd?:{address,port},   // fixed destination 
[](#cb42-18)18:   verbose?:number
[](#cb42-19)19: })
[](#cb42-20)20: port(DIR.IP('http://...'),{
[](#cb42-21)21:   keepAlive?:boolean,    // true:permanent TCP sessions 
[](#cb42-22)22:   secure?:string,
[](#cb42-23)23:   verbose?:number
[](#cb42-24)24: })
[](#cb42-25)25: port(DIR.IP('https://...'),{
[](#cb42-26)26:   keepAlive?:boolean,    // true:permanent TCP sessions 
[](#cb42-27)27:   pem: {
[](#cb42-28)28:     key:string,
[](#cb42-29)29:     cert:string,
[](#cb42-30)30:   },
[](#cb42-31)31:   secure?:string,
[](#cb42-32)32:   verbose?:number
[](#cb42-33)33: })
```

Definition 7-3\. Port configuration for different protocols

### Agent Classes

An agent constructor function can be compiled from an embedded function definition, a function definition loaded from a source file, or from a text string containing the code, as shown in Ex. [7-2](#6_jam-for-users-and-programmers.xhtml_exjamshcomp).

```
function ac (p) { 
  this.v=ε; 
  this.act={..}; 
  this.trans={..}; 
  this.on={..}; 
  this.next='..' }
compile(ac,{verbose:true});
// Alternatively read acf from file
// myclass.js contains: function myclass(p) {..}
open('myclass.js',true);
```

Example 7-2\. Compiling of an agent constructor function

The `compile(ac, name?, options?)` function compiles the sandbox-restricted constructor functions for all AIOS privilege levels into an internal library. Constructor functions can also be loaded directly from a file by using the `open(file,verbose?)` function. An agent class may only contain one named constructor function. The *compile* function uses a modified Esprima JS analyzer reflecting specific AgentJS features and that is applied to the agent constructor function. Analysis results can be displayed by setting the options attribute *verbose*.

The *compile* function (JAM shell API) or the *compileClass* function from the JAM library adds each new compiled agent constructor function to a dictionary, which can be accessed by all virtual nodes of a JAM instance. The same happens using the *open* statement. All the agent classes contained in the dictionary can be immediately used for agent creation.

### Physical Clusters

The JAM shell can be used to easily create worlds consisting of virtual or physical JAM nodes connected by virtual circuit links or IP-AMP links. Physical JAM nodes are grouped into clusters and can be created from a root JAM shell instance.

Each JAM node is a world container containing at least one virtual node with its own process tables and tuple space databases. Additional virtual nodes can be added to the JAM world. Virtual nodes in one world can be connected via virtual channel links with a two-dimensional mesh-grid network structure. Communication (agent migration and signal propagation) is supported via North, South, West, and East communication ports. The virtual node network is primarily used for simulation (see Sec. [SEJAM]) and virtualization of networks. The *jamsh* program provides direct support for virtual JAM networks, as shown in Def. [7-4](#6_jam-for-users-and-programmers.xhtml_jamshvn). Each node is identified by its logical position in the 2D world (*x*,*y*). The initial root node is at position (0,0). Commonly, the world and root name are the same (but, initially, the world name is always in uppercase letters).

```
[](#cb44-1)// Create virtual 2x2 node network
[](#cb44-2)var node2 = add({x:1,y:0}),
[](#cb44-3)    node3 = add({x:1,y:1}),
[](#cb44-4)    node4 = add({x:0,y:1});
[](#cb44-5)// unidirectional links!
[](#cb44-6)connect({x:0,y:0},{x:1,y:0})
[](#cb44-7)connect({x:1,y:0},{x:1,y:1})
[](#cb44-8)connect({x:1,y:1},{x:1,y:0})
[](#cb44-9)connect({x:1,y:0},{x:0,y:0})
[](#cb44-10)function foo() {
[](#cb44-11)  this.act = {
[](#cb44-12)    foo : () => {
[](#cb44-13)      // migrate in virtual network
[](#cb44-14)      var dirs = [DIR.NORTH,DIR.SOUTH,
[](#cb44-15)                  DIR.EAST,DIR.WEST],
[](#cb44-16)          goto=null;
[](#cb44-17)      iter(dirs, (dir) => {
[](#cb44-18)        if (!this.goto && link(dir)) 
[](#cb44-19)          this.goto=dir;
[](#cb44-20)      })
[](#cb44-21)      if (goto) moveto(goto); 
[](#cb44-22)    }
[](#cb44-23)  }
[](#cb44-24)}
```

Definition 7-4\. Creation of virtual node networks processed by the same physical node in the JAM shell

In contrast to virtual node networks, physical clusters consist of independent JAM node instances connected via IP-based communication channels (using AMP). The JAM shell supports the creation of JAM clusters directly, as shown in Def. [7-5](#6_jam-for-users-and-programmers.xhtml_jamshclusters). Again, nodes are arranged in a two-dimensional mesh grid. A cluster creates a set of IP-AMP ports. There are external and internal ports. Internal ports are used to connect the nodes directly via directional links, i.e., using North, South, West, and East ports. External (not directional) ports support connections from outside, e.g., using HTTP from Web browsers. Note that the root JAM node executing the shell script is not the first node in the cluster! Therefore, the root node must connect to one of the cluster nodes via an external port.

A physical cluster is created by the JAM shell by using the `cluster` operation, defining the grid network (rows and columns), the AMP IP ports and protocols, base ports for the AMP IP ports for each link class (p2p, multi), a poll interval to check for cluster node state, and an initial shell command to be executed by each cluster worker (*todo*), shown in Def. [7-5](#6_jam-for-users-and-programmers.xhtml_jamshclusters). The internode connections are arranged in a two-dimensional mesh-grid. Agent migration inside the cluster uses the directional links `DIR.NORTH`, `DIR.EAST`, and so on, depending on the node position.

Agents can migrate between cluster nodes by using the *moveto* operation with cartesian directions with respect to the neighbourhood of the agent's node, e.g., `DIR.NORTH`. Each cluster node creates public IP ports (starting with the IP port number *port0*, e.g., 11001) and private directed links (North, South, West, East), starting with IP port *port1*, e.g., 10001.

```
[](#cb45-1)// Create physical 2x2 node cluster network
[](#cb45-2)var workers = cluster({
[](#cb45-3)  connect:true,
[](#cb45-4)  rows:2,
[](#cb45-5)  cols:2,
[](#cb45-6)  port0:11001, // First internal IP port
[](#cb45-7)  port1:10001, // First external IP port
[](#cb45-8)  portn:100,   // Increment
[](#cb45-9)  proto:['http','udp'],
[](#cb45-10)  poll:number, // worker poll interval in ms
[](#cb45-11)  todo:'config({log:{node:true}});start()',
[](#cb45-12)  verbose:0,
[](#cb45-13)});
[](#cb45-14)workers.start()
[](#cb45-15)// Connect to first cluster node
[](#cb45-16)var p1=port(DIR.IP('udp://localhost:12000'));
[](#cb45-17)later(500,() => {
[](#cb45-18)  connect(DIR.IP('udp://localhost:10002'))
[](#cb45-19)});
[](#cb45-20)function foo () {
[](#cb45-21)  this.act = {
[](#cb45-22)    tofirst : () => {
[](#cb45-23)      // find first IP-connected cluster node
[](#cb45-24)      var connected=link(DIR.IP('%')),
[](#cb45-25)          goto=null;
[](#cb45-26)      if (connected && connected.length) 
[](#cb45-27)        goto=DIR.NODE(connected[0]);
[](#cb45-28)      if (goto) moveto(goto);
[](#cb45-29)    },
[](#cb45-30)    // migrate inside cluster
[](#cb45-31)    // EAST -> SOUTH -> WEST -> NORTH -> ..
[](#cb45-32)    toright : () =>  {
[](#cb45-33)      moveto(DIR.EAST)
[](#cb45-34)    }
[](#cb45-35)}
[](#cb45-36)// Create an agent that migrate from this node 
[](#cb45-37)// to the first cluster node
[](#cb45-38)create(...)
```

Definition 7-5\. Operational template to create physical JAM cluster networks using the JAM shell

The cluster is created and controlled by an initial JAM shell instance (not being part of the cluster network). Agents can be created on this controller instance. The agents can migrate to a node of the cluster if the controller instance has a link to one of the public ports of a cluster node. This is shown in the following Ex. [7-3](#6_jam-for-users-and-programmers.xhtml_jamshclustersag).

```
[](#cb46-1)function circulator(maxhop) {
[](#cb46-2)  this.maxhop=maxhop;
[](#cb46-3)  this.hops=0;
[](#cb46-4)  this.last=null;
[](#cb46-5)  this.goto=null;
[](#cb46-6)  this.act = {
[](#cb46-7)    start: () => { log('Start on '+myNode()); 
[](#cb46-8)                       sleep(1000); },
[](#cb46-9)    move : () => {
[](#cb46-10)      var next;
[](#cb46-11)      // Find directed links between cluster nodes
[](#cb46-12)      if (link(DIR.EAST)) next=DIR.EAST;
[](#cb46-13)      else if (link(DIR.SOUTH)) next=DIR.SOUTH;
[](#cb46-14)      else if (link(DIR.WEST)) next=DIR.WEST;
[](#cb46-15)      else if (link(DIR.NORTH)) next=DIR.NORTH;
[](#cb46-16)      // still on controller node?
[](#cb46-17)      else if (link(DIR.IP('%'))) 
[](#cb46-18)        next = DIR.NODE(link(DIR.IP('%'))[0]); 
[](#cb46-19)      log(next)
[](#cb46-20)      this.goto=next;
[](#cb46-21)      if (next) moveto(next);
[](#cb46-22)    },
[](#cb46-23)    hello : () => { this.hops++; 
[](#cb46-24)                    log('I am on '+myNode()) },
[](#cb46-25)    end   : () => { log('END'); kill() },
[](#cb46-26)  }
[](#cb46-27)  this.trans = {
[](#cb46-28)    start : move,
[](#cb46-29)    move  : () => { return this.goto?hello:end },
[](#cb46-30)    hello : () => { return this.hops<this.maxhop?
[](#cb46-31)                           move:end } 
[](#cb46-32)  }
[](#cb46-33)  this.next='start';
[](#cb46-34)} 
[](#cb46-35)compile(circulator,{verbose:false});
[](#cb46-36)later(1000, () => {
[](#cb46-37)  // connect to node (0,0), don't use http!!!!
[](#cb46-38)  port(DIR.IP('udp://localhost:10000'));
[](#cb46-39)  // 0,0 node, udp port
[](#cb46-40)  connect(DIR.IP('udp://localhost:10002')); 
[](#cb46-41)})
[](#cb46-42)later(1500, () => {
[](#cb46-43)  // Start agent here; it will migrate 
[](#cb46-44)  // to cluster node (0,0)
[](#cb46-45)  create('circulator',4);
[](#cb46-46)})
```

Example 7-3\. Using the JAM shell to inject agents by extending code from Def. [7-5](#6_jam-for-users-and-programmers.xhtml_jamshclusters). A simple circulating agent is created and started on the JAM shell control instance (starting and controlling the cluster, but not being part of the cluster network).

### Virtual Worlds

Virtual worlds can be constructed by using the JAM shell with only a few operations, as shown in Def. [7-6](#6_jam-for-users-and-programmers.xhtml_jamshvirt). Although, there is no speed-up that can be achieved by using virtual worlds (in contrast, to clusters), virtual worlds allow testing of agent mobility in a container world.

```
[](#cb47-1)// 1\. Create new Nodes (root node exists alreays
[](#cb47-2)var nodes = [{x:1,y:0},{x:1,y:1},{x:0,y:1}].map(add);
[](#cb47-3)// 2\. Connect nodes with virtual circuit links
[](#cb47-4)[{x1:0,y1:0,x2:1,y2:0},
[](#cb47-5) {x1:1,y1:0,x2:1,y2:1},
[](#cb47-6) {x1:1,y1:1,x2:0,y2:1},
[](#cb47-7) {x1:0,y1:1,x2:0,y2:0}].map((link) => {
[](#cb47-8) connect({x:link.x1,y:link.y1},{x:link.x2,y:link.y2})
[](#cb47-9)});
```

Definition 7-6\. Creation of linked virtual JAM node worlds by the JAM shell. The main JAM instance creating the world is part of the virtual network (root node at logical position 0,0)

Finally, an example of a simple circulating agent is shown in Ex. [7-4](#6_jam-for-users-and-programmers.xhtml_jamshvirtag), slightly changed from the IP-based cluster example. The agent must prevent it from going back in the opposite direction from which it arrived, here achieved by checking the opposite direction by applying the `DIR.OPPOSITE` function to the current migration direction (stored in `this.goto`, line 12).

```
[](#cb48-1) 1: function circulator(maxhop) {
[](#cb48-2) 2:   this.maxhop=maxhop;
[](#cb48-3) 3:   this.hops=0;
[](#cb48-4) 4:   this.last=null;
[](#cb48-5) 5:   this.goto=null;
[](#cb48-6) 6:   this.act = {
[](#cb48-7) 7:     start: () => { 
[](#cb48-8) 8:       log('Start on '+myNode()); 
[](#cb48-9) 9:       sleep(1000); 
[](#cb48-10)10:     },
[](#cb48-11)11:     move : () => {
[](#cb48-12)12:       var next,back=this.goto?
[](#cb48-13)13:                     DIR.opposite(this.goto):'';
[](#cb48-14)14:       if (link(DIR.EAST) && DIR.EAST!=back) 
[](#cb48-15)15:         next=DIR.EAST;
[](#cb48-16)16:       else if (link(DIR.SOUTH) && DIR.SOUTH!=back) 
[](#cb48-17)17:         next=DIR.SOUTH;
[](#cb48-18)18:       else if (link(DIR.WEST) && DIR.WEST!=back) 
[](#cb48-19)19:         next=DIR.WEST;
[](#cb48-20)20:       else if (link(DIR.NORTH) && DIR.NORTH!=back) 
[](#cb48-21)21:         next=DIR.NORTH;
[](#cb48-22)22:       log(next)
[](#cb48-23)23:       this.goto=next;
[](#cb48-24)24:       if (next) moveto(next);
[](#cb48-25)25:     },
[](#cb48-26)26:     hello : () => { 
[](#cb48-27)27:       this.hops++; 
[](#cb48-28)28:       log('I am on '+myNode()) 
[](#cb48-29)29:     },
[](#cb48-30)30:     end   : () => { log('END'); kill() },
[](#cb48-31)31:   }
[](#cb48-32)32:   this.trans = {
[](#cb48-33)33:     start : move,
[](#cb48-34)34:     move  : () => { return this.goto?hello:end },
[](#cb48-35)35:     hello : () => { return this.hops<this.maxhop?move:
[](#cb48-36)36:                                                  end } 
[](#cb48-37)37:   }
[](#cb48-38)38:   this.next='start';
[](#cb48-39)39: } 
[](#cb48-40)40: compile(circulator,{verbose:false});
[](#cb48-41)41: create('circulator',4);
```

Example 7-4\. A simple circulating agent is created and started on the root JAM shell instance

### AIOS Extension

The AgentJS AIOS, i.e., the AgentJS API for agents for the respective four privilege levels, can be easily extended. The host application can directly control agents via AIOS extension functions, as shown in Def. [7-7](#6_jam-for-users-and-programmers.xhtml_jamshextapi). Any number of arguments that can be passed to extension functions is supported. Each agent with an AIOS containing the extension function can call the extension function in activities, transition rule functions, and signal handler functions. There are synchronous and computational functions, and asynchronous functions with agent process control.

Simple computational functions can be added to the AgentJS AIOS for all or specific levels by using the `extend` function and by providing the AIOS level/levels, the new function name in the AIOS, and optionally the number of expected arguments (required only for the agent compiler to check code). New functions added to the AIOS can provide agent callback support. The callback functions will not be called in the agent object context (default case), i.e., the *this* object does not point to the agent object.

Additionally, the extension function may not start asynchronous function calls with callbacks (like `setInterval`) that could be called later outside the agent activity in which the extension function was called. Additional logic is required. Direct agent process control is possible in the extension function via the global `Aios.current.process` variable. The process object supports the *suspend*, *wakeup*, and *kill* methods. Asynchronous extension functions can send a signal to the calling agent process, too. A signal can be added to the process object's *signals* list attribute and by emitting a schedule event for this node (by the *node* attribute of the process).

In any out-of-flow processing of an asynchronous extension function, the state of the agent must be checked by checking the *kill* and *dead* process object attributes first.

```
[](#cb49-1) 1: extend : function (level:number|number[],
[](#cb49-2) 2:                    name:string,
[](#cb49-3) 3:                    function,
[](#cb49-4) 4:                    argn?:number|number[])
[](#cb49-5) 5: 
[](#cb49-6) 6: // 1\. New pure computational and
[](#cb49-7) 7: //    synchronous extension function
[](#cb49-8) 8: function computation(data,callback) {
[](#cb49-9) 9:   // callback has no agent object context
[](#cb49-10)10:   callback(ε(data)); 
[](#cb49-11)11:   return ε(data)
[](#cb49-12)12: }
[](#cb49-13)13: // 1b. Calling a callback function in its agent context
[](#cb49-14)14: function computation(data,callback) {
[](#cb49-15)15:   var pro = Aios.current.process;
[](#cb49-16)16:   // callback is executed in the current 
[](#cb49-17)17:   // agent object context
[](#cb49-18)18:   pro.callback(callback,ε(data));
[](#cb49-19)19:   return ε(data)
[](#cb49-20)20: }
[](#cb49-21)21: // 2\. Asynchronous extension function with
[](#cb49-22)22: //    agent control (suspend/wakeup)
[](#cb49-23)23: function control(callback) {
[](#cb49-24)24:   // save calling agent process
[](#cb49-25)25:   var pro = Aios.current.process;
[](#cb49-26)26:   // Suspend agent
[](#cb49-27)27:   pro.suspend(0);
[](#cb49-28)28:   // Asynchronous function with
[](#cb49-29)29:   // callback that is called outside 
[](#cb49-30)30:   // of this function
[](#cb49-31)31:   asynchronous(() => {
[](#cb49-32)32:     // Important: check agent state before proceed!
[](#cb49-33)33:     if (pro.kill || pro.dead) return;
[](#cb49-34)34:     // wake-up agent process
[](#cb49-35)35:     pro.callback(callback,arg);
[](#cb49-36)36:     pro.wakeup();
[](#cb49-37)37:   });
[](#cb49-38)38: }
[](#cb49-39)39: // 3\. Asynchronous extension function with
[](#cb49-40)40: //    agent control (signal).
[](#cb49-41)41: //    Agent must provide a signal handler, i.e.,
[](#cb49-42)42: //    this.on = { 'SIGNAL': function () {..} }
[](#cb49-43)43: function signal(sig,arg,..) {
[](#cb49-44)44:   var pro = Aios.current.process;
[](#cb49-45)45:   asynchronous(() => {
[](#cb49-46)46:     // Check agent state first!
[](#cb49-47)47:     if (pro.kill || pro.dead) return;
[](#cb49-48)48:     pro.signals.push([sig,arg]);
[](#cb49-49)49:     // Fire schedule event for this node
[](#cb49-50)50:     Aios.emit('schedule',pro.node);
[](#cb49-51)51:   });
[](#cb49-52)52: }
[](#cb49-53)53: // Add to AIOS level 1
[](#cb49-54)54: extend(1,'computation',foo,2);
[](#cb49-55)55: // Add to all AIOS levels
[](#cb49-56)56: extend([0,1,2,3],'computation',foo,[1,2]);
[](#cb49-57)57: // The computation function can now be used 
[](#cb49-58)58: // by all agents
[](#cb49-59)59: extend([2,3],'control',control,1);
[](#cb49-60)60: // The control function can now be used by 
[](#cb49-61)61: // all level-2 and level-3 agents
[](#cb49-62)62: extend([1,2,3],'signal',signal,2);
```

Definition 7-7\. JAM shell AIOS extension API and programming templates

## JAM Web Laboratory

The JAM Web laboratory is a self-contained HTML-JS application for the Web browser using the browser version of the JAM shell, providing basically the same API as the terminal command line version. The JAM laboratory provides shell, editor, monitor, and report windows (see Fig. [7-1](#6_jam-for-users-and-programmers.xhtml_jamlab)). Single agents can be debugged or terminated by a tree-based agent explorer. Code text can be loaded and saved on the local file system via a tiny helper service *wex* executed on the local computer, or alternatively via the Web browser file dialogue. Communication between the browser (e.g., an editor shell) and *wex* is performed via JSON HTTP RPC requests. In addition to local filesystem services, *wex* provides shell and proxy services, too.

![#jamlab](images/5cd2b093-7dfc-4b15-9e64-5aaa00134560.png)Figure 7-1\. The software architecture of the Web browser JAM laboratory and the wex service that provides local filesystem access

The JAM instance can be processed in an isolated Web worker process, preventing the blocking of the GUI. In addition, multiple physical JAM instances can be started and controlled via the GUI. An initial shell is created in the top-level JS instance, but additional WebWorker shells can be created by using the "plus" button on the top button bar. Each shell window provides direct access to the underlying JAM shell. An agent code editor can be opened. The agent editor is used to create one agent class constructor function. The editor window provides buttons to compile the constructor (information shown in the shell window) and to create agents from this class constructor. Agent arguments and privilege levels can be set in the editor set-up menu. Agent output is initially displayed in the shell console, too. By opening a monitor window (from the shell button bar), agent messages using the `log` statement are redirected to this window.

All created JAM shells can be connected to external JAM nodes. The link information is entered in the main set-up menu. The connection and disconnection of AMP links can be controlled by using the main button bar (link and unlink buttons), too. Note that initially created shells are not activated for agent processing (scheduler loop is initially disabled). This must be done first by using the main buttons (play and stop buttons). The buttons and their operations are explained in Fig. [7-2](#6_jam-for-users-and-programmers.xhtml_jamlabbuts).

![#jamlabbuts](images/bd50b601-d113-40c5-8e2f-f81fc26c3633.png)Figure 7-2\. JAM Web laboratory windows and buttons

The performance of agent processing with JAM depends on the supplied JS VM. Both SpiderMonkey and Google's V8 engines deliver sufficient performance. The V8 performance in the browser is comparable with that of the V8 engine embedded in node.js, as shown in Tab. [8-1](#6_jam-for-users-and-programmers.xhtml_perfhostvm) in the performance evaluation chapter.

Each editor window is connected to a JAM shell, and the code in each editor defines one agent class (its name is derived from the constructor function name). An unlimited number of agents can be created by each editor window. An agent class constructor function must be re-compiled after each change.

A simple "hello world" agent requires only a few lines of code:

* * *

```
[](#cb50-1)function hello (options) {
[](#cb50-2)  this.world=options.world;
[](#cb50-3)  this.child=null;
[](#cb50-4)  this.act = {
[](#cb50-5)    a1: () => {
[](#cb50-6)      log('Hello '+this.world); 
[](#cb50-7)      send(me(),'SIGUSR1') 
[](#cb50-8)    },
[](#cb50-9)    a2: () => {
[](#cb50-10)      this.child=fork({
[](#cb50-11)        world:reverse(this.world)
[](#cb50-12)      }) 
[](#cb50-13)    },
[](#cb50-14)    a3: () => {
[](#cb50-15)      log('End '+this.world);
[](#cb50-16)      kill()
[](#cb50-17)    } 
[](#cb50-18)  }
[](#cb50-19)  this.trans = {
[](#cb50-20)    a1:a2,
[](#cb50-21)    a2:a3
[](#cb50-22)  }
[](#cb50-23)  this.on = {
[](#cb50-24)    SIGUSR1 : () => { log('GOT SIGNAL') }
[](#cb50-25)  }
[](#cb50-26)  this.next = a1
[](#cb50-27)} 
```

* * *

The agent consists of three activities with an unconditional transition chain until the end state is reached. Before the agent can be started, you must enter the following agent argument in the editor set-up:

```
[](#cb51-1){
[](#cb51-2)  world : 'Joe'
[](#cb51-3)}
```

The first activity *a*[1] will use the world variable and will send a custom signal `SIGUSR1` to himself (the signal handler should output `GOT SIGNAL`). The second activity, *a*[2] forks a child agent with a reversed world string. The last activity finally terminates the agent. Note that if the agent is terminated not explicitly, it will persist until a platform's given lifetime quota is reached, eventually killing the agent by the platform.

The console output of an agent run should look like:

```
[](#cb52-1)17:25:33:59 [qiqaqika@17:25:33:59] Hello Joe
[](#cb52-2)17:25:33:60 [qiqaqika@17:25:33:60] GOT SIGNAL
[](#cb52-3)17:25:33:60 [sirenuke@17:25:33:60] End eoJ
[](#cb52-4)17:25:33:60 [qiqaqika@17:25:33:60] End Joe
```

In the shell window setup, you can set different logging options like time or agent identifier fields, which are added to each logging output line.

Exercise 7-2\. Web Agents (2)

1.  Start a JAM shell on your computer. Create an HTTP AMP port service. Start the scheduler loop: `port(DIR.IP('http://localhost:4567')); start()`. Connect the JAM laboratory (must be loaded from the local filesystem or via HTTP!) to this JAM shell.
2.  Create an agent that forks a child agent. The child agent should migrate to the JAM shell node. Both agents should send PING signals periodically to each other. If an agent (parent or child) does not receive PING messages any more, it should terminate.

## JAM Mobile App

There is mobile App version providing a full JAM instance with a dedicated GUI. The GUI is page-based (see Fig. [7-3](#6_jam-for-users-and-programmers.xhtml_jamapp)) and consists of configuration and network set-up, network management (connecting of the JAM node), agent management, and life information pages displaying all available sensors, and a chat dialogue page. There is a pure HTML-CSS-JS and a Cordova framework version.

The basic HTML version can be used in any Web browser on mobile and desktop computers. On mobile devices, the basic HTML version provides access to device sensors. The location of the device can be requested via GPS sensing (if available) and/or via the public IP address resolved by an external IP-GEO database and by using the Mozilla location service (optional).

The JAM App can be configured. It can connect to one or more remote JAM nodes using HTPP or HTTPS. The links can be configured in the setup section. Note that HTTP or HTTPS are only supported if the JAM App was loaded from the local filesystem or with the same protocol from a remote Web server. HTTPS can be restricted by browser settings if loaded from local filesystem. An adjustment of browser settings can sometimes be required.

A root agent can be loaded from a Web server or can be embedded already in the mobile App (a single self-contained HTML file or a multi-file archive). Additional agents can be loaded from a Web server and started. There is a JAM logging page collecting all agent and JAM messages. The chat dialogue can be accessed via an extended AIOS API by the agents directly (with sufficient rights). The agents can access the device sensors via the tuple space. The sensor information page lists all available sensors and their names used as the first key element of the sensor tuples (provided by a provider function).

![#jamapp](images/b31eec7c-79de-4381-98cd-c8a5535bef6a.png)Figure 7-3\. (Top) Software architecture of the Web browser / Cordova JAM App (Bottom) Some example pages

The mobile App is used for mobile crowdsensing (MCS) applications as well as for education. The Web browser version supports currently the following sensors (accessible by agents via the tuple space):

1.  Browser information (BENGINE, OS, BVERSION, JSVERSION)
2.  Time (CLOCK, TIME, DATE)
3.  Public IP address (IP)
4.  Geospatial location based on public IP address and additional services (GEO, LOCATION, LOCATION5), optionally using GPS (GEO5, LOCATION5)
5.  Depending on additional browser security settings (configuration and necessity to load the Web page via HTTPS):
    *   Acceleration (ACCEL, ACCELH, ACCELA0)
    *   Orientation (ORIENT)
    *   Light (LIGHT)

The Cordova (Android) version always provides access to internal sensors (acceleration, gyroscope, light, and so on).

Exercise 7-3\. Web Agents (2)

1.  Start a JAM shell on your computer. Create an HTTP AMP port service. Start the scheduler loop: `port(DIR.IP('http://localhost:4567')); start()`. Connect the JAM laboratory and the JAM app (must be loaded from the local filesystem or via HTTP!) to this JAM shell.
2.  Create an agent that forks a child agent. The child agent should migrate to the JAM shell node. From this relay node, it should search for unknown nodes, i.e., JAM App nodes. If it finds a new node, it should migrate to this node and collect some sensor values. The agent should finally return to its root node (laboratory in the Web browser), finally printing (logging) the sampled sensors.

# Performance

The JAM is typically processed by modern JS VMs like node.js/V8 or SpiderMonkey. These JS VMs can achieve native code performance of about 20-50%, mostly by applying just-in-time (JIT) native code compilation of already compiled Bytecode (the most common JS VM intermediate format). Although JAM agents are written in JavaScript and processed by the underlying JS VM (pseudo VM in VM architecture), there is nearly no performance degradation in the processing of agents. The tasks with the highest computational costs are the creation of agents and migration, both requiring full code-to-text serialization and text-to-code back deserialization. Fortunately, agent creation (not forking) requires this process only once applied to a reusable agent constructor function.

## JavaScript VM

JAM performance is inherently bound to the underlying JS VM performance. In Tab. [8-1](#7_performance.xhtml_perfhostvm), results for different JS VMs and host platforms using a normalized dhrystone benchmark test are shown. The dhrystone benchmark utilizes an average mix of operations typical for real-world software. i.e., object creation and destruction, array and string operations, and function calls. Different JS VMs are compared, although, JAM basically runs out of the box only on *node.js* and *jx*, a multithreaded *node.js* derivative optimized for JAM (especially native agent process watchdog support) based on the *jx-core* project. Note that the measured performance (except for the native code baseline) depends on VM settings like the garbage collector (GC) run-time settings. The GC interrupts the main JS control flow, lowering the benchmark performance. But GC interference occurs in any application program and this is a central part of the computational performance and average memory requirements.

| JS VM | Host | dhrystones/s | Memory |
| --- | --- | --- | --- |
| C/native | x86 i5-4310U, 2GHz, 8GB | 23000k | - |
| quickjs-2019 | x86 i5-4310U, 2GHz, 8GB | 142k | 2MB |
| quickjs-2019 | Raspberry Pi Zero, Arm, 1GHz, 1GB | 9k | 1MB |
| jerryscript-2017 | x86 i5-4310U, 2GHz, 8GB | 32k | 1MB |
| node.js-8 | x86 i5-4310U, 2GHz, 8GB | 6800k | 28MB |
| node.js-8 | Raspberry Pi Zero, Arm, 1GHz, 1GB | 220k | 28MB |
| node.js-10 | x86 i5-4310U, 2GHz, 8GB | 8000k | 30MB |
| jx (node.js-0.10.4) | x86 i5-4310U, 2GHz, 8GB | 7000k | 18MB |
| V8 (Chromium 90) | x86 i5-4310U, 2GHz, 8GB | 7450k | - |
| SpiderMonkey (Gecko FF 78) | x86 i5-4310U, 2GHz, 8GB | 5330k | - |

Table 8-1\. Comparison of different JS VMs and host platforms using the normalized dhrystone benchmark test [WEI84]

Note that node.js and the V8 core engine were optimized for the x86 processor architecture and therefore underperform on the Arm processor architecture. Besides the computational power, the memory requirements (base memory required for the VM itself and JAM) are another important parameter in the deployment of (tiny) embedded systems like the Raspberry Pi Zero. The VM performance is about 4 times slower than the native (C) code performance of the benchmark test program. Node.js with the V8 core engine with native code JIT compilation outperforms the low-resource pure Bytecode-based quickjs engine. But SpiderMonkey delivers similar results compared with V8!

## Agent class compilation and agent creation

The experiment was performed with the *jamsh* program to evaluate the time required to compile agent class constructor functions and to create agents by them using the following code:

```
[](#cb53-1)function foo(p) { .. }
[](#cb53-2)N=1000;
[](#cb53-3)t0=time()
[](#cb53-4)for (var i = 0;i<N;i++)
[](#cb53-5)  compile(foo,{verbose:false});
[](#cb53-6)t1=time()
[](#cb53-7)print((t1-t0)/N,'ms/compile')
[](#cb53-8)N=100
[](#cb53-9)t0=time()
[](#cb53-10)for (var i = 0;i<N;i++) 
[](#cb53-11)  create('foo',{..});
[](#cb53-12)t1=time()
[](#cb53-13)print((t1-t0)/N,'ms/create')
[](#cb53-14)var aid = create('foo',{..}),
[](#cb53-15)    agobj = agent(aid);
[](#cb53-16)print(Aios.Code.size(agobj))
```

The results are shown in Tab. [8-2](#7_performance.xhtml_perfagcreat). The compile time can be basically neglected because an agent class constructor must only be compiled once (per node). The creation of agents is fast enough (at least on modern computer hardware) compared with a typical average agent creation rate (about 1/s-10/s).

| Operation | Parameter | Time / Aux. |
| --- | --- | --- |
| compile | function | 0.8 ms |
| create | { string[16], number } | 0.09 ms |
| size | agent | Ser. code: 365 Bytes |

Table 8-2\. JAM (jamsh) performance: Agent sandbox-restricted transformation and creation (Host: x86 i5-4310U, 2GHz, 8GB, jx/node.js 0.10.40)

## Migration

Firstly, a 2 × 2 virtual JAM node mesh-grid network was created. The experiment was performed with *jamsh* and the following test code:

```
[](#cb54-1)function foo(p) {
[](#cb54-2)  ..
[](#cb54-3)  this.act = {
[](#cb54-4)    start : ..
[](#cb54-5)    percept : () => {
[](#cb54-6)      this.goto=null; 
[](#cb54-7)      var dirs = [DIR.NORTH,DIR.SOUTH,..]
[](#cb54-8)      iter(dirs, () => {
[](#cb54-9)        if (!this.goto && link(dir))
[](#cb54-10)          this.goto=dir;
[](#cb54-11)      })
[](#cb54-12)    },
[](#cb54-13)    move : () => {
[](#cb54-14)      this.hops--;
[](#cb54-15)      moveto(this.goto)
[](#cb54-16)    },
[](#cb54-17)    end : ..
[](#cb54-18)  }
[](#cb54-19)  this.trans = {
[](#cb54-20)    start:percept,
[](#cb54-21)    percept : () => this.goto && this.hops?move:end,
[](#cb54-22)    move : percept
[](#cb54-23)  }
[](#cb54-24)}
[](#cb54-25)var node2 = add({x:1,y:0}),
[](#cb54-26)    node3 = add({x:1,y:1}),
[](#cb54-27)    node4 = add({x:0,y:1});
[](#cb54-28)// unidirectional links!
[](#cb54-29)connect({x:0,y:0},{x:1,y:0})
[](#cb54-30)connect({x:1,y:0},{x:1,y:1})
[](#cb54-31)connect({x:1,y:1},{x:1,y:0})
[](#cb54-32)connect({x:1,y:0},{x:0,y:0})
[](#cb54-33)
[](#cb54-34)compile(foo,{verbose:false});
[](#cb54-35)var N=1000
[](#cb54-36)create('foo',{data:'..',hops:N});
[](#cb54-37)start()
```

The second experiment was performed with a physical 2 × 2 node mesh-grid cluster using directional UDP links and the following code:

```
[](#cb55-1)function foo(p) {
[](#cb55-2)  ..
[](#cb55-3)  this.act = {
[](#cb55-4)    start : () => {
[](#cb55-5)      // goto cluster node(0,0)
[](#cb55-6)      var connected=link(DIR.IP('%'))
[](#cb55-7)      if (connected && connected.length) 
[](#cb55-8)        this.goto=DIR.NODE(connected[0]); 
[](#cb55-9)    },
[](#cb55-10)    percept : () => {
[](#cb55-11)      this.goto=null; 
[](#cb55-12)      // follow ring
[](#cb55-13)      var dirs = [DIR.EAST,DIR.SOUTH,DIR.WEST,DIR.NORTH];
[](#cb55-14)      var next = dirs[this.index];
[](#cb55-15)      if (link(next)) {
[](#cb55-16)        this.goto=next;
[](#cb55-17)        this.index=(this.index+1)%4;
[](#cb55-18)      }
[](#cb55-19)    },
[](#cb55-20)    move : () => {
[](#cb55-21)      this.hops--;
[](#cb55-22)      moveto(this.goto)
[](#cb55-23)    },
[](#cb55-24)    end : ..
[](#cb55-25)  }
[](#cb55-26)  this.trans = {
[](#cb55-27)    start   : () => this.goto?'move':'percept',
[](#cb55-28)    percept : () => this.goto && this.hops?'move':'end',
[](#cb55-29)    move    : 'percept'
[](#cb55-30)  }
[](#cb55-31)}
[](#cb55-32)var workers = cluster({
[](#cb55-33)  connect:true,
[](#cb55-34)  rows:2,
[](#cb55-35)  cols:2,
[](#cb55-36)  port0:11001,
[](#cb55-37)  port1:10001,
[](#cb55-38)  portn:100,
[](#cb55-39)  proto:['http','udp'],
[](#cb55-40)  poll:2000,
[](#cb55-41)  todo:'start()',
[](#cb55-42)  verbose:0,
[](#cb55-43)});
[](#cb55-44)workers.start()
[](#cb55-45)// Connect to cluster node (0,0)
[](#cb55-46)var p1=port(DIR.IP('udp://localhost:12000'));
[](#cb55-47)later(500,() => {
[](#cb55-48)  connect(DIR.IP('udp://localhost:10002'))
[](#cb55-49)});
[](#cb55-50)compile(foo,{verbose:false});
[](#cb55-51)var N=1000
[](#cb55-52)later(3000,() => {
[](#cb55-53)  create('foo',{data:..,hops:N});
[](#cb55-54)})
```

| Operation | Parameter | Time / Aux. |
| --- | --- | --- |
| moveto | Virtual Link¹ | 0.5 ms / hop |
| moveto | Physical UDP Link² | 6.0 ms / hop |
| size | agent¹ | Ser. code: 730 Bytes |
| size | agent² | Ser. code: 946 Bytes |

Table 8-3\. JAM (jamsh) performance: Agent migration (Host: x86 i5-4310U, 2GHz, 8GB, jx/node.js 0.10.40)

The results in Tab. [8-3](#7_performance.xhtml_perfagmig) contain average times for agent process migration. The migration includes agent data and code serialization, the transfer of the serialized code to the next node, and finally the deserialization and process creation on the new node. The migration between virtual nodes is as fast as agent creation, whereas agent migration between physical nodes is 10 times slower, i.e., the overhead of AMP and the communication network is significant.

## Communication

Communication is performed between a parent and a child agent created by forking. The child agent migrates to another node (virtual or physical). Note that the agents in communication experiments use a ping-pong flow with signal handlers and activity blocking, i.e., agent scheduling is included in the communication times.

The first signal experiment used the following code skeleton using two agents on two different nodes (virtual or physical):

```
[](#cb56-1)function foo(p) {
[](#cb56-2)  ..
[](#cb56-3)  this.act = {
[](#cb56-4)    start : () => {
[](#cb56-5)      this.child=fork({parent:me(),goto:DIR.EAST});
[](#cb56-6)    },
[](#cb56-7)    move : () => {
[](#cb56-8)      moveto(this.goto);
[](#cb56-9)    },
[](#cb56-10)    ping : () => {
[](#cb56-11)      this.count--;
[](#cb56-12)      if (this.parent) send(this.parent,'PING',time());
[](#cb56-13)      else send(this.child,'PING',time());
[](#cb56-14)    },
[](#cb56-15)    pong : () => { sleep() },
[](#cb56-16)    wait : () => { sleep() }, 
[](#cb56-17)    end  : () => {  kill() },
[](#cb56-18)  }
[](#cb56-19)  this.trans = {
[](#cb56-20)    start : () => { return this.goto?'move':'wait' },
[](#cb56-21)    wait : () => { this.count--; 
[](#cb56-22)                   this.time=time(); return ping },
[](#cb56-23)    move : ping,
[](#cb56-24)    ping : pong,
[](#cb56-25)    pong : () => { return this.count?'ping':'end' },
[](#cb56-26)  }
[](#cb56-27)  this.on = {
[](#cb56-28)    PING : (arg,from) => {
[](#cb56-29)      send(from,'PONG',time())
[](#cb56-30)      if (this.child && this.count==this.N) wakeup()
[](#cb56-31)    },
[](#cb56-32)    PONG : (arg,from) => {
[](#cb56-33)      wakeup()
[](#cb56-34)    },
[](#cb56-35)  }
[](#cb56-36)  ...
```

The second agent is forked from the first one. The tuple space communication can only be executed between agents on the same JAM node. Again, two agents are used in the test set-up. Results are shown in Tab. [8-4](#7_performance.xhtml_perfagcomm). Signal sending is as fast as tuple space communication. Remote signal propagation is affected by the communication overhead, too, approximately 30 times slower.

| Operation | Parameter | Time / Aux. |
| --- | --- | --- |
| send | signal, virtual nodes | 0.1 ms |
| send | signal, physical nodes | 3.5 ms |
| out,inp | one node | 0.03 ms |

Table 8-4\. JAM (jamsh) performance: Agent communication times using signals and tuples, including agent scheduling times (Host: x86 i5-4310U, 2GHz, 8GB, jx/node.js 0.10.40)

# Simulation with SEJAM

Agent-based simulation is commonly used to simulate a sub-set of the real world with entities posing simplified behaviour and interaction models. The simulation aims to compute aggregate variables on a global level and emergent behaviour as a result of the interacting entities. Graphical simulation commonly assigns visual shapes and positions to agents in a two- or three-dimensional graphical world.

An entity, here represented by an agent, is defined by its behaviour model *m*[beh], which is commonly adapted by a parameter set *p*, i.e., *m*[beh](*p*). Different parameter settings result in different behaviour. For example, a parameter can determine the initial position of an agent in the simulation world, another can define the moving speed, direction, and so on. Parameters can affect the decision-making of agents, i.e., affect the run of an agent (sequence of agent states).

The selection of appropriate parameter settings is a challenge. Most simulations of real-world environments and entity interactions are inaccurate (on a time and spatial scale) due to inappropriate parameter sets, oversimplified behavior, and a low number of entities in the simulation compared to the real-world situation.

The coupling of simulation with the real world in real time (or at least on a snapshot basis) can improve the outcome of simulation significantly. MCS can be used to derive suitable parameter settings of simulation agents, creating digital twins from real-world entities (humans, machines, vehicles, and so on).

A digital twin is derived from a pre-defined agent behaviour *m*[beh] and a parameter set *p* that is derived from real world sensor data *s*, collected from a sampling process *S*, delivering a sub-set of the real world state *e* at a specific spatial position (or area) *x*,*y* at a specific time (or time range) *t*, e.g, from a survey:

| ![image-placeholder](images/ee0b2ad2-e88c-49ff-a5e4-943786cc7f18.png) | (9-1) |

The SEJAM simulator is a graphical two-dimensional world on top of the JAM platform, introduced in the next sections. The fact that SEJAM uses JAM enables migration of mobile agents between the simulation and real-world JAM nodes, e.g., mobile platforms like smartphones.

## Concept and Architecture

The Simulation Environment for JAM (SEJAM) is a graphical extension on top of the JAM platform to support agent-based simulation (ABS) using the same AgentJS programming as used in agent-based computation (ABC). Moreover, ABS and ABC can be combined, connecting SEJAM with external JAM nodes. Agents in simulation can migrate between "virtual" and real worlds seamlessly. The basic SEJAM architecture and concept are shown in Fig. [9-1](#8_simulation-with-sejam.xhtml_sejamconcept). A typical example of combining ABS with ABC is simulation with data from real environments using mobile crowd sensing, e.g., as described in [BOS18C].

Graphical shapes in the 2D simulation world are coupled to virtual JAM instances as part of the virtual node world of JAM. A visual shape is typically assigned to one agent, e.g., an agent representing a digital twin of a human or a machine. But an unlimited number of agents can be processed by one virtual node.

There are basically two different subclasses of agents used in the simulation:

1.  ABS cells are physical agents that represent physical entities (humans, machines, animals, and resources).
2.  Computational agents that serve as ABC cells in simulation and in the real world for distributed computation.

Both agent subclasses are processed by the same JAM instance. But physical agents are bound to their virtual node and cannot migrate. Additionally, they can access a NetLogo-like simulation programming interface, e.g., supporting the *ask* operator to explore agents in the spatial neighbourhood in the simulation world [BAN15].

A physical agent consists of a v-JAM node and one body agent always bound to this node. Physical agents can perform any computation and communicate with other v-JAM nodes. They can create computational agents that are capable of migrating to other v-JAM nodes of physical agents or external nodes. For example, a physical node can define a multicast port (used in simulation, only) with a visual shape of a circle with a specific radius. If two physical nodes have overlapping communication circles, the AIOS `link(DIR.PATH('%')` function will return the neighbour node's node name.The physical agent can create a computational agent that is then capable of migrating to the neighbouring node.

![#sejamconcept](images/ea150a1b-2c96-469b-8443-e0eb6148aba5.png)Figure 9-1\. SEJAM concept and architecture: A graphical simulation world on top of a JAM node instance

## Simulation Model and API

SEJAM extends the AIOS of JAM with additional functions related to the simulation world and model. SEJAM creates the simulation world from a simulation model containing world and agent descriptions.

### Simulation World

The simulation model is typically one JS (JSON-like) file containing the model object and the agent class constructor functions with its visual descriptors. Alternatively and for the sake of readability, the agent class constructor functions can be loaded from separate files containing the (named) agent class constructor functions, as shown in Def. [9-1](#8_simulation-with-sejam.xhtml_sejammo). Examples of agent classes are shown in Chapter [9-4](#8_simulation-with-sejam.xhtml_sec_example_5). Besides generic two-dimensional graphical worlds, different pre-defined world architectures can be used:

1.  A mesh-grid consists of a two-or three-dimensional connected grid of v-JAM nodes with neighbourhood connectivity (computational agents only), basically used to study distributed data processing and communication systems (see Def. [9-2](#8_simulation-with-sejam.xhtml_sejammomesh)). Network v-JAM odes are connected with von-Neumann neighbourhood nodes, providing DIR.NORTH, DIR.SOUTH, DIR.WEST, and DIR.EAST directional communication links.

2.  A patch-grid world consists of a two-dimensional Cartesian map of patches supporting physical agents (i.e., a container of a coupled v-JAM with one agent and a visual shape). A patch can be populated with one or more agents. Agents can move freely to different patch positions together with their container. A NetLogo-like API is provided that can be used by physical and world agents (see Def. [9-1](#8_simulation-with-sejam.xhtml_sejammo)).

```
[](#cb57-1) 1: {
[](#cb57-2) 2:   name:string,
[](#cb57-3) 3:   // Definition of agent classes
[](#cb57-4) 4:   agents : {
[](#cb57-5) 5:     classname: {
[](#cb57-6) 6:       behaviour : (..) => { .. } |
[](#cb57-7) 7:                   open(filename.js),
[](#cb57-8) 8:       visual : { shape, width, height, fill, .. }
[](#cb57-9) 9:     ..
[](#cb57-10)10:   },
[](#cb57-11)11:   // some passive resources in the 2D simulation world
[](#cb57-12)12:   resources : { 
[](#cb57-13)13:     classname : (id,x,y,w,h) => {
[](#cb57-14)14:       return { id, class, visual }
[](#cb57-15)15:     },
[](#cb57-16)16:     .. 
[](#cb57-17)17:   },
[](#cb57-18)18:   // dynamic node constructors, mainly for physical
[](#cb57-19)19:   // agent nodes and the world node
[](#cb57-20)20:   nodes : {
[](#cb57-21)21:     classname : (x,y) => {
[](#cb57-22)22:       return { id, x, y, visual, ports }
[](#cb57-23)23:     },
[](#cb57-24)24:     ..
[](#cb57-25)25:   },
[](#cb57-26)26:   // Definition of the world
[](#cb57-27)27:   world : {
[](#cb57-28)28:     init : {
[](#cb57-29)29:       // create specific agents
[](#cb57-30)30:       agents : {
[](#cb57-31)31:         classname : (nodeid) => { 
[](#cb57-32)32:           return { level, args } 
[](#cb57-33)33:         },
[](#cb57-34)34:       }
[](#cb57-35)35:     },
[](#cb57-36)36:     // create special nodes
[](#cb57-37)37:     map : () => {
[](#cb57-38)38:       return [
[](#cb57-39)39:          // graphical position 
[](#cb57-40)40:         model.nodes.world(52,52), 
[](#cb57-41)41:       ]
[](#cb57-42)42:     },
[](#cb57-43)43:     // resources
[](#cb57-44)44:     resources : (model) => {
[](#cb57-45)45:       // using model.resources.classname functions
[](#cb57-46)46:       return {} []
[](#cb57-47)47:     }, 
[](#cb57-48)48:     // if there is a NetLogo patchgrid world
[](#cb57-49)49:     patchgrid : {
[](#cb57-50)50:       rows, cols, width, height, floating?
[](#cb57-51)51:     },
[](#cb57-52)52:   },
[](#cb57-53)53:   // simulation parameter
[](#cb57-54)54:   parameter? : { .. },
[](#cb57-55)55: }
```

Definition 9-1\. Basic template of a SEJAM2 simulation model supporting the patch-grid architecture

The patch-grid world is used in conjunction with the NetLogo API that can be used by physical agents and the world agent. A patch-grid is a discretized 2D world with equally sized patches. Most operations use the logical path coordinates instead of the graphical pixel coordinates (used otherwise). Instead of logical or pixel coordinates, the world and the visual shapes can be referenced by geospatial coordinates using `gps:{latitude, longitude, height}` values (e.g., in the visual node descriptors). A geo-graphical coordinates mapping function is required.

The simulation commonly uses one central world agent (agent class "world") to control the simulation globally and centrally. The world agent has full access to the JAM and SEJAM APIs including database and file system access.

The agent simulation world can be coupled with a multi-body physics simulator (CANNON, see [BOS19A] for details).

```
[](#cb58-1) 1: { 
[](#cb58-2) 2:   ..
[](#cb58-3) 3:   world : {
[](#cb58-4) 4:     init: {
[](#cb58-5) 5:       agents: {
[](#cb58-6) 6:         node:function (nodeId,position) {
[](#cb58-7) 7:           // Create on each node a node agent,
[](#cb58-8) 8:           // return respective agent parameters!
[](#cb58-9) 9:           // If no agent should be created on the
[](#cb58-10)10:           // respective node, undefined must be returned!
[](#cb58-11)11:           if (nodeId!='world')
[](#cb58-12)12:             return {level:2,args:[
[](#cb58-13)13:               {x:position.x,y:position.y,z:position.z,
[](#cb58-14)14:                model:model,
[](#cb58-15)15:                verbose:0,
[](#cb58-16)16:               }]}
[](#cb58-17)17:         },
[](#cb58-18)18:         world: function(nodeId) {
[](#cb58-19)19:           if (nodeId=='world') return 
[](#cb58-20)20:             {level:3,args:[{model:model}]};
[](#cb58-21)21:         }
[](#cb58-22)22:       }
[](#cb58-23)23:     },
[](#cb58-24)24:     meshgrid : {
[](#cb58-25)25:       // y-axis
[](#cb58-26)26:       rows:8,
[](#cb58-27)27:       // x-axis
[](#cb58-28)28:       cols:5,
[](#cb58-29)29:       //z-axis
[](#cb58-30)30:       levels:3,
[](#cb58-31)31: 
[](#cb58-32)32:       matrix:[[0,0],[250,0], [500,0]],
[](#cb58-33)33: 
[](#cb58-34)34:       node: {
[](#cb58-35)35:         // Node ressource visual object
[](#cb58-36)36:         visual : {
[](#cb58-37)37:           shape:'rect',
[](#cb58-38)38:           width:30,
[](#cb58-39)39:           height:30,
[](#cb58-40)40:           fill: {
[](#cb58-41)41:             color:'green',
[](#cb58-42)42:             opacity: 0.5
[](#cb58-43)43:           }
[](#cb58-44)44:         },
[](#cb58-45)45:         filter: function (pos) {
[](#cb58-46)46:           // Node filter to create irregular networks
[](#cb58-47)47:           return 
[](#cb58-48)48:         },
[](#cb58-49)49:       },
[](#cb58-50)50:       // Link port connectors
[](#cb58-51)51:       port: {
[](#cb58-52)52:         type:'unicast',
[](#cb58-53)53:         place: function (node) { return [
[](#cb58-54)54:           {x:-15,y:0,id:'WEST',,
[](#cb58-55)55:           {x:15,y:0,id:'EAST'},
[](#cb58-56)56:           {x:0,y:-15,id:'NORTH'},
[](#cb58-57)57:           {x:0,y:15,id:'SOUTH'},
[](#cb58-58)58:           {x:-15,y:-15,id:'UP'},
[](#cb58-59)59:           {x:15,y:15,id:'DOWN'}
[](#cb58-60)60:         ]},
[](#cb58-61)61:         visual: {
[](#cb58-62)62:           shape:'rect',
[](#cb58-63)63:           fill: {
[](#cb58-64)64:             color:'black',
[](#cb58-65)65:             opacity: 0.5
[](#cb58-66)66:           },
[](#cb58-67)67:           width: 5,
[](#cb58-68)68:           height: 5
[](#cb58-69)69:         } 
[](#cb58-70)70:       },
[](#cb58-71)71:       // Connections between nodes 
[](#cb58-72)72:       // (with virtual port connectors)
[](#cb58-73)73:       link : {
[](#cb58-74)74:         // Link resource visual object
[](#cb58-75)75:         connect: function (node1,node2,port1,port2) {
[](#cb58-76)76:           return true},
[](#cb58-77)77:         type:'unicast',   // unicast multicast
[](#cb58-78)78:         visual: {
[](#cb58-79)79:           shape:'rect',
[](#cb58-80)80:           fill: {
[](#cb58-81)81:             color:'#888',
[](#cb58-82)82:             opacity: 0.5
[](#cb58-83)83:           },
[](#cb58-84)84:           width: 2
[](#cb58-85)85:         }
[](#cb58-86)86:       }
[](#cb58-87)87:     } 
[](#cb58-88)88:   }
[](#cb58-89)89: }
```

Definition 9-2\. Mesh-grid world architecture defining a communication network with von-Neumann neighbourhood connectivity consisting of v-JAM nodes processing computational agents

The difference between the mesh-grid communication network supporting computational agents only and the patch-grid world supporting physical (and computational) agents is shown in Fig. [9-2](#8_simulation-with-sejam.xhtml_simuworlds).

![#simuworlds](images/e8db453d-f441-4b2f-844b-5ca6c7720722.png)Figure 9-2\. Difference between the mesh-grid (a) and patch-grid world (b)

### NetLogo API

SEJAM provides a NetLogo-like API for physical agents. NetLogo is a widely used agent-based simulation environment for studying complex dynamic systems. Details of NetLogo simulations can be found in [WIL15]. The API is summarized in Tab. [9-1](#8_simulation-with-sejam.xhtml_sejamnetlogoapi) and can be accessed by the *net* module extension. If arrow functions are supplied, the `this` agent self-reference is not available. Instead, an additional callback function argument provides the agent object self-reference. There are different simulation object classes: Agents, resources, and patches, which can be handled by the `net.ask` function.

| Operation | Parameter | Description |
| --- | --- | --- |
| `net.create` | `agent-`*agentclass*, *number*, *callback*(*self*,*index*)? | Creates a set of agents. Each created agent can be configured by the callback function using the *self* function parameter pointing to the agent object. |
| `net.setxy` | [*x*, *y*] | Set patch position of agent. |
| `net.ask` | `agent` or `agent-`*agentclass*, [*x*, *y*], *callback*(*self*)? | Returns all agents at grid position (*x*,*y*) and optionally iterates over all agent objects with a callback function. |
| `net.ask` | `agent` or `agent-`*agentclass*, *radius*:number or `*`, *callback*(*self*)? | Returns all agents around current agent position in given radius or all. |
| `net.ask` | `resource` or `resource-`*class*, .. | Returns all matching resources |
| `net.ask` | `patch`, .. | Returns all matching patches |
| `net.ask` | *objclass* or *objclass*`-`*class*, `{x,y,w,h}` or `{x0,y0,x1,y1}`, *callback*(*self*)? | Returns all objects of given object class in given bounding box. |
| `net.set` | `color` or `shape`, *value* | Set visual shape colour or shape (`circle`, `rect`, `triangle`) |

Table 9-1\. SEJAM NetLogo-like API for physical agents

## Software

There are two nearly identical versions of the *sejam2* simulation environment:

1.  A *node-webkit* version with full access to operating system services and networking;
2.  A Web browser version with limited access to operating system services.

The original *sejam* simulator was a terminal and command line implementation using *ncurses* for a textual 2D world visualization.

## Example

A complete example of a simple simulation model is shown in Chapter [9-4](#8_simulation-with-sejam.xhtml_sec_example_5). The simulation model consists of:

1.  The patch-grid world that offers the NetLogo API (code in Sec. [13-1](#12_examples.xhtml_sec_sejam2_simulation_model_0));
2.  Computational world agent (code in Sec. [13-2](#12_examples.xhtml_sec_simulation_world_agent_1));
3.  Physical agents moving around the simulation world at random and changing the colour of their nodes based on crowd neighbourhood perception (code in Sec. [13-3](#12_examples.xhtml_sec_physical_random_walker_agent_2)).

The use-case section [Mobile Crowd Sensing with JAM] will elaborate on a more complex example using additional computational agents providing simulation-real world coupling (code see Sections [13-4](#12_examples.xhtml_sec_computational_explorer_agent_3) and [13-5](#12_examples.xhtml_sec_computational_micro_survey_agent_4)).

The following Fig. [9-3](#8_simulation-with-sejam.xhtml_sejamdemoex) shows a snapshot of the SEJAM2 simulation program executing the previous simulation model. A zoomed view shows the two-dimensional graphic world of the simulation. The circles around mobile nodes (bodies) of physical agents is a radio link that is used by a computational agent processed on the vJAM node of the physical agent. If there are two nodes with overlapping circles, the vJAM platforms are coupled by a virtual link. Computational agents can migrate between such connected vJAM nodes.

![#sejamdemoex](images/62786190-ae27-4cfe-b6e1-23e5a6a9598d.png)Figure 9-3\. SEJAM2 GUI window (node-webkit version) with an example worldExercise 9-1\. Simulation of Random Walker Agents

1.  Open the `sekam2web.html` file in your Web browser, start optionally the `wex` file service on your computer (using node.js, i.e., `node wex`)
2.  Load the simulation model from Sec. [13-1](#12_examples.xhtml_sec_sejam2_simulation_model_0). There are three agent classes loaded from separate files (requires *wex*): *world* (see Sec. [13-2](#12_examples.xhtml_sec_simulation_world_agent_1)), *foo* (physical random walker agent, see Sec. [13-3](#12_examples.xhtml_sec_physical_random_walker_agent_2)), and *explorer* (computational agent that migrates between physical agent nodes, see Sec. [13-4](#12_examples.xhtml_sec_computational_explorer_agent_3)). The simulation model file and the agent model files must be in the same folder.
3.  If the simulation model was successfully loaded, create a simulation world (simulation control panel: ☆)
4.  Start the simulation (play button in the simulation control panel) and observe the movement of agents and the creation of explorer agents. Open the agent log window and evaluate the agent messages.
5.  When is a new explorer agent created?
6.  What is the goal of the explorer agent?
7.  What determines the migration path? Give examples.
8.  Stop the simulation. Select a physical agent, then its node, and finally a computational explorer agent (if present). Explore each agent in the left inspector window.
9.  What is shown in the inspector window? Continue the simulation and observe the position body variable of the agent (agent root object in the inspector must be closed and re-opened to refresh).

The next chapter will introduce the coupling of the simulator with the real world. Only minor changes of the MAS must be performed to achieve augmented simulations with digital twins.

# Introduction to Augmented Simulation

Augmented simulation means the fusion of real and virtual worlds, creating "Augmented Virtuality" by using the previously introduced mobile JAM agents. The central feature is the agent duality of physical (simulation) and computational agents given by one unified agent programming model.

## Simulation of Socio-Technical Systems

If we consider sociotechnical systems, a rich set of interfaces occurs. They are characterized by interactions between

*   Human-Human (initiated by a human)
*   Human-Machine (initiated by a human)
*   Machine-Human (initiated by a machine, e.g., a chatbot)
*   Machine-Machine (initiated by a machine)

The simulation of social ensemble behaviour requires the simplification of interactions and individual behaviour. Commonly, simulations are performed with less than 1000 entities (humans, machines, and so on) in a sandbox world with limited model variance. Agent-based Modelling (ABM) is a suitable behaviour model for simulation, provided by JAM, too.

## Augmented Virtuality

Simulation worlds are virtual and commonly closed and rely on artificial sensory information generated by the simulator program or using data collected off-line (→ traditional field studies, see Fig. [10-1](#9_introduction-to-augmented-simulation.xhtml_augvirt)). A new simulation paradigm providing augmented virtuality is required to make simulation more general and suitable for real-world deployment and understanding.

![#augvirt](images/e5dbdf8d-c0af-48bc-babf-32bf0baae60f.png)Figure 10-1\. Transition from field studies and isolated simulations to extended simulations combining real and virtual worlds

> Crowd Sensing and social data mining integration in simulation worlds is the central key methodology for creating realistic simulations and simulation output that is aligned with real-world observations!

This means, the simulation world interacts with real world environments, humans, machines, and other virtual worlds in real-time using

*   **Agents** that can represent artificial humans, bots, machines, and many more;
*   **Agents** that can be used for distributed mobile computing → real world sensor data and digital twins from crowd sensing.

Multiple virtual worlds can be connected by the augmented virtuality approach. Each virtual world can be considered as a world and a model part, e.g., dividing a country into terrestrial units (towns), or living worlds into home, outdoor, and working areas. Multiple virtual worlds can be simulated independently and in parallel with a significant speedup (see [BOS21B] for details). This leads to a hybrid architecture with virtual and physical world fusion performed by the mobile agents and JAM networks, as shown in Fig. [10-2](#9_introduction-to-augmented-simulation.xhtml_multiworlds).

![#multiworlds](images/56c1ca44-ab70-404e-bd7a-6cb935462eb9.png)Figure 10-2\. Multiple simulations and real worlds

The next chapter [Mobile Crowdsensing with JAM] will introduce a simple simulation example with source code in Chapter [9-4](#8_simulation-with-sejam.xhtml_sec_example_5).

## Challenges

There are numerous challenges with the augmented simulation method, mainly time- and space-scale issues.

### Time

Different time scales in real and virtual worlds lead to several issues:

*   Simulation of distributed computing is much slower than Distributed Computing;
*   Simulation is discrete (processed step-wise) with respect to the time scale;
*   Interaction (reactivity) of entities and their behaviour models are different in virtual and real worlds.

There is a short-term versus long-term issue:

*   A simulation is typically run over a short time period (a window with defined start and end points).
*   Real-world environments with human-machine interaction do not have a well-defined beginning or end point for long-term execution.

Simulation can rely on a pre-analysis using Big Data. But Big Data poses strongly uncorrelated variables from different sources and therefore has low information strength.

### Space

We have different spatial scales in real and virtual worlds with basically three different spatial models, illustrated in Fig. [10-3](#9_introduction-to-augmented-simulation.xhtml_areas):

1.  Real and virtual worlds cover non-overlapping areas;
2.  Real and virtual worlds cover overlapping areas;
3.  Real world areas are mapped onto a virtual world.

![#areas](images/169b38b1-5442-4daa-8166-9d7e5367ccce.png)Figure 10-3\. Real and virtual (simulation) spatial areas and their correlation

### Surveys and Human-in-the-Loop

In addition to the collection of environmental sensor data, partially publicly available, e.g., crowd and traffic flows, temperature distributions, weather, and news, people can be used to provide information for adjusting and calibrating model parameters. Micro or full surveys can be used to get specific information for the behavioural models of agents in the simulation, finally creating digital twins of humans. The digital twin concept is not limited to humans. Digital twins can be created from devices and machines but require different parameter estimation approaches and measuring techniques.

Using the digital twin concept, the simulation world can be enriched by more variance and temporal calibrated agent behaviour. Humans (and the real world) are included in the simulation loop. On the one hand, people provide input for the simulation. On the other hand, simulation results can be passed back to the users as well (output). The simulation model and the agent models can be updated periodically by MCS, as shown in Fig. [10-4](#9_introduction-to-augmented-simulation.xhtml_simuextsurv).

![#simuextsurv](images/08487382-4eee-4e56-8ecd-708b7ad21c64.png)Figure 10-4\. Humans and real sensors as continuous input for simulation worlds

# Mobile Crowdsensing with JAM

An extended use case deploying mobile agents in an ad-hoc mobile crowdsensing (MCS) framework should demonstrate the suitability and scalability of the JAM architecture and its software. JAM, with its unified and universal agent platform, supports:

*   Mobile crowdsensing (ABC) that is used to sample environmental and user data at a microscale level;
*   Tight coupling of simulation (ABS) with real world interaction (human-in-the-loop);
*   Incremental data collection by software agents synchronising the simulation with real world data;
*   Simulation snapshots and forking enable prediction of future world evolution (of system aggregate variables, e.g., infection rates).

The data collection process using mobile agents can be used independently of simulation experiments for the collection of surveys using a dedicated version of the JAM App (Browser version) customized for non-technical end-users, as discussed in the next section.

## Surveys

The stand-alone mobile crowd sensing framework deploys the following nodes:

1.  The root node, which uses either the JAM Web browser laboratory, a dedicated Web application built with the JAM library (Web version), or the JAM shell from the command line to plan and master the survey and analyze the data.
2.  Stationary JAM shell relay nodes with a public internet connection and database access;
3.  Mobile Apps with embedded JAM and chat dialog (Web browser and Android App versions).

The survey is typically a static or dynamic question tree. A typical survey consists of about 10-20 questions. The survey can be provided as a dialogue snippet table with survey dialogue descriptors. A descriptor is a functional data object that describes the type of a dialogue entry (message, question) and possible answers, e.g., a choice list or a numeric interval. Questions can be dynamic by providing conditional resolution functions instead of static content. Finally, the dialogue entry can be activated by a conditional function. The conditions are based on answers from other dialogue snippets and sensor data, e.g., geospatial position or time.

A typical dialogue snippet descriptor is shown in Def. [11-1](#10_mobile-crowdsensing-with-jam.xhtml_dialoguedesc). A snippet can be optionally activated by a *cond* function that returns a Boolean value (false discards the snippet). All dialogue snippets in the dialogue table array have a unique tag string that is used to create a map table associating the tag name with its entry. The dialogue map table is passed to all conditional functions in a dialogue snippet. The dialogue table can be easily carried by mobile agents. The answers to questions are stored in the dialogue snippet entries, used at survey time, e.g., for conditional activations of snippets. A *next* function can be used to branch to the next entry (returning the tag name), otherwise the next index entry in the table array is processed.

```
[](#cb59-1) 1: type survey = {
[](#cb59-2) 2:   author : string,
[](#cb59-3) 3:   date   : string,
[](#cb59-4) 4:   dialogue : dialogSnippet [],
[](#cb59-5) 5:   stamp? : string | string [],
[](#cb59-6) 6:   user?  : string | string [],
[](#cb59-7) 7:   node?  : string | string []
[](#cb59-8) 8: }
[](#cb59-9) 9: type dialogSnippet = 
[](#cb59-10)10: {
[](#cb59-11)11:   tag : string | number,
[](#cb59-12)12:   message : string | 
[](#cb59-13)13:             function (dialogMap) → string 
[](#cb59-14)14: } |
[](#cb59-15)15: {
[](#cb59-16)16:   tag : string | number,
[](#cb59-17)17:   question : string | 
[](#cb59-18)18:              function (dialogMap) → string,
[](#cb59-19)19:   choices? : string [],
[](#cb59-20)20:   range?   : number [],
[](#cb59-21)21:   type : 'text'|'number',
[](#cb59-22)22:   answer? : string|number,
[](#cb59-23)23:   cond? : function (dialogueMap) → boolean,
[](#cb59-24)24:   next? : function (dialogueMap) → string
[](#cb59-25)25: }
[](#cb59-26)26: type dialogMap = { $tag : dialogSnippet }
```

Definition 11-1\. Type signature of typical dialogue snippet descriptors and a complete survey

The dialogue processor logic is rather simple, and a sketch algorithm is shown in Alg. [11-1](#10_mobile-crowdsensing-with-jam.xhtml_dialogueproc). The dialogue processor is typically executed by a client survey agent. A survey can be repeated with different users and/or on different nodes by mobile survey agents. Answers can then be stored in the snippet entries with an array or returned and sent to a remote database agent that collects finished surveys. Each function of a dialogue snippet can access its current entry via the `this` variable. The dialogue processor binds the entry on function call.

```
[](#cb60-1) 1: function process (survey) {
[](#cb60-2) 2:   var map = {}, current=survey.dialog[0], 
[](#cb60-3) 3:       index = 0;
[](#cb60-4) 4:   for (var i in survey.dialog) {
[](#cb60-5) 5:     map[survey.dialogue[i].tag]=survey.dialog[i];
[](#cb60-6) 6:     map[survey.dialogue[i].index=i;
[](#cb60-7) 7:   }
[](#cb60-8) 8:   while (current) {
[](#cb60-9) 9:     if (!current.cond || 
[](#cb60-10)10:         current.cond.call(current,map)) {
[](#cb60-11)11:       if (current.message) {
[](#cb60-12)12:         Message  (typeof current.message=='function'?
[](#cb60-13)13:                   current.message.call(current,map)
[](#cb60-14)14:                   :current.message);
[](#cb60-15)15:       } else if (current.question) {
[](#cb60-16)16:         Question (typeof current.question=='function'?
[](#cb60-17)17:                   current.question.call(current,map)
[](#cb60-18)18:                   :current.question,
[](#cb60-19)19:                   current);
[](#cb60-20)20:       }
[](#cb60-21)21:     }
[](#cb60-22)22:     if (current.next) {
[](#cb60-23)23:       current=map[typeof current.next=='function'?
[](#cb60-24)24:                   current.next.call(current,map)
[](#cb60-25)25:                   :current.next];
[](#cb60-26)26:       index = current.index;
[](#cb60-27)27:     } else {
[](#cb60-28)28:       index++;
[](#cb60-29)29:       current=survey.dialog[index];
[](#cb60-30)30:     } 
[](#cb60-31)31:   }
[](#cb60-32)32: }
```

Algorithm 11-1\. Dialogue processor logic

In principle, only one survey agent class is required using sub-classing of behaviour and replication (based on divide & conquer distribution). The root survey agent gets the survey description and forks a child agent that migrates from the root node to a publicly reachable relay node. This agent acts as a local collector instance and stays on the relay node and waits for new connections from (mobile or desktop) JAM nodes that could potentially provide the required chat dialogue environment controlled by a chat moderator agent. If a new node is found, a new child agent is forked to migrate to the new node. Either this is a node with a chat environment and the survey agents processes the survey, or it terminates, or it returns to the relay node. The waiting collector agent will recognize a time-out. If the survey was performed before a time-out, the reply is either carried by the mobile agent back to the relay node, or sent back by a signal (the collector agent is the parent of the mobile survey agent and hence known by its identifier name).

If the collector agent has serviced the survey for a specific time or enough replies have arrived, it will either return to the root node with the collected survey database, or send the database via a signal to the root agent (which is the parent of this agent).

The entire distributed three-stage survey processing is shown in Fig. [11-1](#10_mobile-crowdsensing-with-jam.xhtml_distsurv3).

![#distsurv3](images/db08ddb3-98f9-4251-9dc0-fb8ce017d175.png)Figure 11-1\. Distributed three-stage survey processing using one super survey agent class. The red and green agents provide subclass behaviour of the blue super agent class.

## Geolocation

An important sensor in mobile crowdsensing is the geographical position (usually given in polar coordinates with longitude (lon) and latitude (lat)). In addition to the physical geographical position, the location context is of interest (location description such as street name and city). The current geographical position of a mobile device such as a smartphone is usually obtained directly by means of radio waves and GPS.

The direct derivation of the position via the Internet device address is difficult because usually only the location of the Internet service provider (ISP) can be determined. But from crowdsensing of collective information and fusion with usage data (such as frequent page views with location reference, DNS usage, etc.), a more precise location of the publicly visible IP address is carried out.

JAM uses a multi-step procedure to determine the location of its host platform:

1.  Using the public IP address and an Internet Service Provider (ISP) database (accuracy between 10-500 km) and using the ISP database server http:\ip-api.com (Attention: Ad blockers in Web browsers prevent access to this database service). This geolocation does not use data from tracking and tracing (no crowdsensing), but can be highly inaccurate on mobile cellular networks!

2.  Using the public IP address and a localization service from Mozilla https:\location.services.mozilla.com (accuracy about 10 km, except in mobile cellular networks). This service uses data from its own crowdsensing (collective average value data, probably not personalized) to determine the user position (latitude and longitude) and [https://api.opencagedata.com](https://api.opencagedata.com) to determine the place context (place, country).

3.  If GPS is available and usable, as well as the HTML5 GeoLocation service in the WEB browser (GPS of the device is also used via this), precise geospatial localization can be performed (accuracy of about 1 m outdoors). It does not commonly work indoors!

The resolved node location can be accessed by the `info('node')` operation and using the *location* field of the return object. All sensed and resolved location services are provided by the *location* field: *geo* (using IP address), *geo5* (using GPS), *gps*, and *gps5*.

## MCS-based Surveys

The MCS-based survey is a classical participatory survey, in contrast, to the micro-survey used in the augmented simulation, discussed in the next section.

The survey is designed in advance. The survey participants use a customized JAM App for the Web browser on smartphones (hiding the technical details of JAM and starting with the chat dialogue page). The Web browser version has the advantage of a low threshold to participate and a higher utility for the user since there is no software that must be installed.

The survey agent is generic and gets it survey on creation. The survey agent is started on the surveyor node (e.g., JAM laboratory or shell).

So the root node starts with the definition of the survey. Here, for example, a simple survey among students about their age and food preferences:

```
[](#cb61-1)survey = {
[](#cb61-2)  author : 'Student',
[](#cb61-3)  date : Date.now(),
[](#cb61-4)  dialog : [
[](#cb61-5)    {sensors : ['LOCATION','LOCATION5','GEO',
[](#cb61-6)                'GEO5','TIME'],
[](#cb61-7)    {message : 'Food Survey'},
[](#cb61-8)    {tag:'QA', 
[](#cb61-9)     question: 'How old are you?',
[](#cb61-10)     range:[1,99], step:1 },
[](#cb61-11)    {tag:'QF', 
[](#cb61-12)     question: 'What foods do you eat?',
[](#cb61-13)     choices: ['Vegetarian',
[](#cb61-14)                           'Vegan',
[](#cb61-15)                           'Meat',
[](#cb61-16)                           'Fish'],
[](#cb61-17)     cond: function (dialog) {
[](#cb61-18)       return dialog.QA.answer>=18
[](#cb61-19)     }},
[](#cb61-20)    {tag:'QL', 
[](#cb61-21)     question: 'Name your favorite dish:' },
[](#cb61-22)    {message:'Thank you!'},
[](#cb61-23)  ],
[](#cb61-24)}
```

In addition to the dialogue, sensors are sampled, e.g., the current location of the user or the ambient light intensity. The platform provides a unified API to access sensors by an agent (commonly the tuple space).

The basic survey agent behaviour is shown in Alg. [11-2](#10_mobile-crowdsensing-with-jam.xhtml_mcssurv). It consists of network exploration and survey processing via a chat dialogue.

```
 1:  1: Save root node id (root)
 2:  2: Current is node
 3:  3: Create the dialogue processor map; dialogMap
 4:  4: All answers are store in sensors={$nodeid:{..}}
 5:  5: if goto then
 6:  6:   moveto(goto)
 7:  7: end
 8:  8: if on root node then
 9:  9:   waitfor relay := link(..) ≠ ∅
10: 10:   fork({goto:relay})
11: 11: if on relay node (node≠root) then
12: 12:   Save relay node id (relay)
13: 13:   while time < surveytime do
14: 14:     Get all linked nodes
15: 15:     ∀ node' ∈ linked ∧ node' ∉ visited do
16: 16:       Add node' to visited 
17: 17:       fork({goto:node'})
18: 18:     done
19: 19:     sleep
20: 20:   done
21: 21: if on chat node (node≠root≠relay∧∃chat) then
22: 22:   Save chat node id (chat)
23: 23:   Acquire chat session token
24: 24:   index := 1, next := dialog[1]
25: 25:   while next do
26: 26:     if next.cond ∧ next.cond(dialogMap) = false then
27: 27:       next = Next(dialogMap,index,next)
28: 28:       continue
29: 29:     end
30: 30:     if next.message then
31: 31:       if next.message is function then
32: 32:         text = next.message(dialogMap)
33: 33:       else
34: 34:         text = next.message
35: 35:       end
36: 36:       Message(text)
37: 37:     else if next.sensor(s) then
38: 38:       ∀ sensor ∈ next.sensors do 
39: 39:         sensors[node]2-5:=Sample(sensor)
40: 40:       done
41: 41:     else if next.question then
42: 42:       if next.question is function then
43: 43:         text = next.question(dialogMap)
44: 44:       else
45: 45:         text = next.question
46: 46:       end
47: 47:       Question(text,options)
48: 48:       answer = Answer(question)
49: 49:       sensors[node][next.tag]=answer
50: 50:     end
51: 51:     next = Next(dialogMap,index,next)
52: 52:   done
53: 53:   Go back to relay: moveto(relay)
54: 54: end
55: 55: if node≠root≠relay∧ then
56: 56:   Go back to relay: moveto(relay)
57: 57: end
```

Algorithm 11-2\. Basic survey-explorer agent behaviour

## Web Crawling

Another important task in MCS is Web crawling and Web scraping (see [ENG22] for details). Web scraping collects data from Web pages (the page content is the sensor), assuming the Web pages contain relevant and potentially dynamic data, e.g., daily updated statistics. But user interaction and even the pure visit of a page by a user can be utilized in MCS. In Sec. [7-1](#6_jam-for-users-and-programmers.xhtml_sec_jam_library_0) and in Chapter [9-4](#8_simulation-with-sejam.xhtml_sec_example_5) Sec. [13-8](#12_examples.xhtml_sec_web_page_with_jam_7) mobile agents are used to collect user data and its interaction with a Web page. Opening the Web page creates a JAM instance and a data collector agent that forks a child agent that migrates to an external relay JAM node. The parent-child agent pair is a temporary and loosely coupled data connection. The child agent will store collected data in the tuple space, which is consumed by another delivery agent and delivered to a data sink node (surveyor). This is a four-agent path principle, shown in Fig. [11-2](#10_mobile-crowdsensing-with-jam.xhtml_4agpath).

The data source and data sink sides are totally independent and exchange data only over the node tuple space, shown in Alg. [11-3](#10_mobile-crowdsensing-with-jam.xhtml_4agpathalg). The child and parent agents communicate by using signal messages. The parent agent will send ping messages periodically to the child agent. If the child agent does not receive new ping messages, it will terminate (lost parent). This approach can sense user data like geolocation and browser information as well as dynamic Web page content based on user interaction or user preferences (Web scraping), as shown in Chapter [9-4](#8_simulation-with-sejam.xhtml_sec_example_5) Sec. [13-8](#12_examples.xhtml_sec_web_page_with_jam_7). The JAM AIOS can be extended with a DOM access wrapper function, enabling direct access of the DOM content by agents (including modification of the page content). Note that Web scraping typically operates on Web pages not under the control of the surveyor, in contrast, to the approach presented here, where JAM code is injected into the page (i.e., it is a kind of reverse Web crawling).

![#4agpath](images/13a0681e-5e95-4533-8800-209be491ad9d.png)Figure 11-2\. A rendezvous of two parent-child agent pairs to pass information collected by a Web page (data source) to a surveyor (data sink).

```
 1:  1: (a) Data Source
 2:  2: ───────────────
 3:  3: 
 4:  4: waitfor relay := link(..) ≠ ∅
 5:  5: fork({goto:relay})
 6:  6: if goto then
 7:  7:   moveto(goto)
 8:  8: end
 9:  9: if parent then
10: 10:   while not timeout do
11: 11:     send(child,'PING')
12: 12:     sleep
13: 13:   done
14: 14:   kill()
15: 15: end
16: 16: if child then
17: 17:   while alive do
18: 18:     Collect data
19: 19:     send(parent,'DATA',data)
20: 20:     sleep
21: 21:   done
22: 22:   kill()
23: 23: end
24: 24: on 'PING' do
25: 25:   Update alive
26: 26: done
27: 27: on 'DATA' do
28: 28:   mark(data)
29: 29: done
30: 30: 
31: 31: (b) Data Sink
32: 32: ─────────────
33: 33: 
34: 34: waitfor relay := link(..) ≠ ∅
35: 35: fork({goto:relay})
36: 36: if goto then
37: 37:   moveto(goto)
38: 38: end
39: 39: if parent then
40: 40:   while not timeout do
41: 41:     send(child,'PING')
42: 42:     sleep
43: 43:   done
44: 44:   kill()
45: 45: end
46: 46: if child then
47: 47:   while alive do
48: 48:     inp(data)
49: 49:     send(parent,'DATA',data)
50: 50:     sleep
51: 51:   done
52: 52:   kill()
53: 53: end
54: 54: on 'PING' do
55: 55:   Update alive
56: 56: done
57: 57: on 'DATA' do
58: 58:   Store new data record in data base
59: 59: done
```

Algorithm 11-3\. Basic agent behaviour for two parent-child agent pairs performing a rendezvous to pass information collected by a Web page (data source) to a surveyor (data sink)

## Augmented Simulation

The basic concept relies on long-term longitudinal data mining combining MCS, modelling, and simulation [BOS21C]. The principle system architecture is shown in Fig. [11-3](#10_mobile-crowdsensing-with-jam.xhtml_mcsconcept). In addition, details can be found in [BOS17B] and [BOS18C] where MCS is integrated into the agent-based simulation using SEJAM.

The mobile crowd sensing and simulation framework deploys the following nodes:

1.  The root node with a SEJAM instance;
2.  Stationary JAM relay nodes with a public internet port and access to database services;
3.  Web browser JAM nodes embedded in Web pages;
4.  Mobile Apps with embedded JAM and chat dialogue (Web browser and Android App versions).

The behaviour model *beh* of physical simulation agents is parametrized with the parameter set *p*, i.e., *beh*=*beh*(*p*). The parameter set is either static with a-priori values (or calculated from previous data analysis), or dynamic with values derived from user micro-surveys and/or collected sensor data *X* performed by mobile survey agents, finally creating digital twins. The aim is to derive global aggregate variables *Y* from sensor input *X*. *Y* can be measured from simulations runs or predicted by data-driven machine models *M*(*X*) using ML methodologies. If the input data *X* is produced by the simulation, the predictive model is a surrogate model.

![#mcsconcept](images/7ba245c0-2a9e-4b4d-91e8-d4a4f8ba22ab.png)Figure 11-3\. Unified agent methodology for longitudinal data mining, complex systems modelling, and simulation

## MAS for Augmented Simulation

The augmented simulation MAS consists of:

1.  A world agent controlling the simulation and managing data in SQL databases;
2.  Computational survey explorer agents that are created by the world agent;
3.  A static set of physical agents modelling simple social and networking behaviour based on a-priori model parameter sets;
4.  A dynamic set of physical digital twin agents with model parameter settings based on micro surveys and created by the world agent via the explorer agent feedback.

The survey agents are started in the simulation world and migrate to a public relay JAM node. Mobile devices (smartphones) using the mobile JAM App are connected to the same relay node (ad-hoc). The explorer agent stays on the relay for a specific time and watches for new connections. If there is a new connection, a child agent is forked and sent to the remote node. The child explorer agent tries to find a chat agent. If the chat agent is found, the micro survey is delegated to the chat agent. The explorer agent waits for a specific time for a response (by the user propagated by the chat agent). Communication with the chat agent is performed via the tuple space.

A simplified version of the MAS is shown in Chapter [9-4](#8_simulation-with-sejam.xhtml_sec_example_5) in Sections [13-1](#12_examples.xhtml_sec_sejam2_simulation_model_0), [13-2](#12_examples.xhtml_sec_simulation_world_agent_1), [13-3](#12_examples.xhtml_sec_physical_random_walker_agent_2), and [13-5](#12_examples.xhtml_sec_computational_micro_survey_agent_4).

# Summary

The JavaScript Agent Machine (JAM) is a universal and highly portable agent processing platform using an advanced VM architecture. JAM is entirely programmed in JavaScript (JS) and can be executed on any JS VM engine, e.g., *node.js* or *SpiderMonkey* as part of a Web browser. The agents are programmed in AgentJS, a sub-set of JS, and executed in a masked and constrained environment directly by the underlying JS VM. The performance of the agent code execution is only limited by the JS VM. Although the agent is executed directly by the JS VM, JAM monitors the agent processing and limits, e.g., the processing time. Native code VM modules (mostly the watchdog module) can further improve the overall performance.

The agent behaviour is composed of activities and transitions between activities based on the body variables of the agent. JAM agents are mobile processes that can migrate their process snapshot, including their code, between different JAM nodes, regardless of the node interconnectivity. JAM supports virtualization on different levels, including agent communication. JAM can be deployed in Web-based and Internet environments like the IoT. JAM addresses ABS as well as ABC, combined in the SEJAM simulator.

Major fields of application are general distributed computing on the Internet and Web, simulation, sensor processing in distributed sensor networks, and mobile crowd sensing. The Agent Management Port (AMP) protocol enables loosely coupled connections between JAM nodes using a wide range of communication protocols.

# Examples

A simplified version of the MCS-MAS is shown in this chapter, combining ABS with ABC performing MCS to create digital twins in the simulation world from survey results. Although, printed source code is not very handy, the agent code is very compact and it is worth studying the AgentJS API and its usage. An extended version of the survey agent supporting dialogue flows can be used stand-alone to perform MCS only. Finally, Web crawling is demonstrated with a simple Web page.

## SEJAM2 Simulation Model

A simple SEJAM2 simulation model is shown in Ex. [13-1](#12_examples.xhtml_sejamex1). The model is composed of three different agent models (a world agent controlling the simulation, a physical simulation agent, and a computational agent), defined in the *agents* section in lines 3-42\. Each agent class is associated with a code behaviour and a visual shape. The agent code is loaded from separate files by the `open` function and assigned to the *behaviour* attribute. Visual properties are assigned to the *visual* attribute. Basic visual shapes are rectangles, circles (ellipses), and triangles. Colour and line attributes can be specified.

Agents require v-JAM nodes for execution, typically associated with a visual shape and a position in the simulation world, defined in the *nodes* section in lines 47-107\. Finally, the simulation world (here the pre-defined patch-grid) is defined in lines 116-146, including initialization and mapping functions. The *map* function returns a list of node descriptor structures. The *init* object is primarily used to create an initial static set of agents (here only the world agent). Each entry in the *init.agents* field specifies an agent class name that must be defined in the *agents* section. Typically, agents are created dynamically by the world agent at simulation time. Resources, e.g., streets or traffic signs, can be created by the *resources* function (not used here).

The world node creates a physical AMP communication endpoint (only possible in the node-webkit SEJAM version), defined in lines 48-52 and 71-73\. It is used to connect the simulation world (the automatically created world node, more specifically) with external JAM nodes. The link enables agents to migrate between simulation and real-world nodes. Computational agent examples can be found in Sec. [13-5](#12_examples.xhtml_sec_computational_micro_survey_agent_4)

Agents from the *foo* agent class create virtual wireless radio communication ports which can be used to link neighbouring nodes (*port* entry in 90-103 lines ). Overlapping radio circles establish a virtual ad-hoc connection and enable the linking of nodes (automatically done by the simulator program). The communication radius is given by the visual shape radius.

An optional user-defined parameter section is defined in lines 108-116 (not interpreted by the simulator). All initialization and mapping functions can access the model object directly.

The patch-grid world itself is defined in lines 135-145, mainly defining the grid and patch sizes. The *floating* parameter is commonly set true.

```
[](#cb64-1)  1: {
[](#cb64-2)  2:   name:'Random Walk Simulation',
[](#cb64-3)  3:   agents : {
[](#cb64-4)  4:     world : {
[](#cb64-5)  5:       behaviour:open('world.js'),
[](#cb64-6)  6:       visual:{
[](#cb64-7)  7:           shape:'circle',
[](#cb64-8)  8:           width:10,
[](#cb64-9)  9:           height:10,
[](#cb64-10) 10:           fill: {
[](#cb64-11) 11:             color:'green',
[](#cb64-12) 12:             opacity: 0.0
[](#cb64-13) 13:           }
[](#cb64-14) 14:       } 
[](#cb64-15) 15:     },
[](#cb64-16) 16:     foo : {
[](#cb64-17) 17:       behaviour : open('agent.js'),
[](#cb64-18) 18:       visual:{
[](#cb64-19) 19:           shape:'circle',
[](#cb64-20) 20:           width:4,
[](#cb64-21) 21:           height:4,
[](#cb64-22) 22:           fill: {
[](#cb64-23) 23:             color:'blue',
[](#cb64-24) 24:             opacity: 0.0
[](#cb64-25) 25:           }
[](#cb64-26) 26:       },
[](#cb64-27) 27:       type:'physical', 
[](#cb64-28) 28:     },
[](#cb64-29) 29:     explorer : {
[](#cb64-30) 30:       behaviour : open('explorer.js'),
[](#cb64-31) 31:       visual:{
[](#cb64-32) 32:           shape:'circle',
[](#cb64-33) 33:           width:4,
[](#cb64-34) 34:           height:4,
[](#cb64-35) 35:           x:-8,y:-8,
[](#cb64-36) 36:           fill: {
[](#cb64-37) 37:             color:'green',
[](#cb64-38) 38:             opacity: 0.0
[](#cb64-39) 39:           }
[](#cb64-40) 40:       }
[](#cb64-41) 41:     },
[](#cb64-42) 42:   },
[](#cb64-43) 43:   resources : {
[](#cb64-44) 44: 
[](#cb64-45) 45:   },
[](#cb64-46) 46:   nodes: {
[](#cb64-47) 47:     world: function (x,y) {
[](#cb64-48) 48:         var phy={type:'physical',
[](#cb64-49) 49:                  ip:'*',
[](#cb64-50) 50:                  to:model.parameter.ip+':'+
[](#cb64-51) 51:                     model.parameter.ipport,
[](#cb64-52) 52:                  proto:model.parameter.proto};
[](#cb64-53) 53:         return {
[](#cb64-54) 54:           id:'world',
[](#cb64-55) 55:           x:x, // patch position
[](#cb64-56) 56:           y:y,
[](#cb64-57) 57:           visual : {
[](#cb64-58) 58:             shape:'icon',
[](#cb64-59) 59:             icon:'world',
[](#cb64-60) 60:             label:{
[](#cb64-61) 61:               text:'World',
[](#cb64-62) 62:               fontSize:14
[](#cb64-63) 63:             },
[](#cb64-64) 64:             width:20,
[](#cb64-65) 65:             height:20,
[](#cb64-66) 66:             fill: {
[](#cb64-67) 67:               color:'black',
[](#cb64-68) 68:               opacity: 0.5
[](#cb64-69) 69:             }
[](#cb64-70) 70:           },
[](#cb64-71) 71:           ports : {
[](#cb64-72) 72:             phy:phy
[](#cb64-73) 73:           }
[](#cb64-74) 74:         }
[](#cb64-75) 75:     },
[](#cb64-76) 76:     foo : function (x,y,id) {
[](#cb64-77) 77:         return {
[](#cb64-78) 78:           id:id,
[](#cb64-79) 79:           x:x, // patch position
[](#cb64-80) 80:           y:y,
[](#cb64-81) 81:           visual : {
[](#cb64-82) 82:             shape:'rect',
[](#cb64-83) 83:             width:10,
[](#cb64-84) 84:             height:10,
[](#cb64-85) 85:             fill: {
[](#cb64-86) 86:               color:'yellow',
[](#cb64-87) 87:               opacity: 0.5
[](#cb64-88) 88:             }
[](#cb64-89) 89:           },
[](#cb64-90) 90:           port: {
[](#cb64-91) 91:             type:'multicast',
[](#cb64-92) 92:             status: function (nodes) {
[](#cb64-93) 93:               // Filter out nodes, e.g., beacons only?
[](#cb64-94) 94:               return nodes;
[](#cb64-95) 95:             },
[](#cb64-96) 96:             visual: {
[](#cb64-97) 97:               shape:'circle',
[](#cb64-98) 98:               radius : 30,
[](#cb64-99) 99:               line: {
[](#cb64-100)100:                 color: 'grey'
[](#cb64-101)101:               }
[](#cb64-102)102:             }
[](#cb64-103)103:           },
[](#cb64-104)104: 
[](#cb64-105)105:         } 
[](#cb64-106)106:     }
[](#cb64-107)107:   },
[](#cb64-108)108:   parameter : {
[](#cb64-109)109:     ip:'ag-0.de',
[](#cb64-110)110:     ipport:10002,
[](#cb64-111)111:     proto:'udp',
[](#cb64-112)112:     phy:true,
[](#cb64-113)113:     speed: 0.2,
[](#cb64-114)114:     randomness: 0.1,
[](#cb64-115)115:   },
[](#cb64-116)116:   world : {
[](#cb64-117)117:     init: {
[](#cb64-118)118:       agents: {
[](#cb64-119)119:         world: function(nodeId) {
[](#cb64-120)120:           if (nodeId=='world') 
[](#cb64-121)121:             return {level:3,args:{verbose:1}};
[](#cb64-122)122:         }
[](#cb64-123)123:       }
[](#cb64-124)124:     },
[](#cb64-125)125:     // special nodes
[](#cb64-126)126:     map : function () {
[](#cb64-127)127:       return [
[](#cb64-128)128:           model.nodes.world(25,25),  // patchgrid position 
[](#cb64-129)129:       ]
[](#cb64-130)130:     },
[](#cb64-131)131:     // resources
[](#cb64-132)132:     resources : function () {
[](#cb64-133)133:       return []
[](#cb64-134)134:     },
[](#cb64-135)135:     patchgrid : {
[](#cb64-136)136:       rows : 50,
[](#cb64-137)137:       cols : 50,
[](#cb64-138)138:       // geometrical width and height of patch in pixels
[](#cb64-139)139:       width : 10, 
[](#cb64-140)140:       height : 10,
[](#cb64-141)141:       // physical agents are containers 
[](#cb64-142)142:       // <logical v-node, behavioural agent>
[](#cb64-143)143:       floating : true, 
[](#cb64-144)144: 
[](#cb64-145)145:     }
[](#cb64-146)146:   }
[](#cb64-147)147: }
```

Example 13-1\. Example of a SEJAM2 simulation model

## Simulation World Agent

The world agent of a simulation (always level 3) is responsible for controlling the simulation. It creates an initial set of agents, monitors simulation aggregate variables, and loads and saves data. The world agent creates an explorer survey agent that migrates to an external relay JAM node. Mobile devices (smartphones) using the JAM App connect to the relay, too. The survey agent collects some user data and returns the result back to the world agent, which creates digital twin agents (random walk agents with a parameter set derived from the survey). The current simulation model (as defined in the previous section) can be accessed via the generic *simu* module and by calling the *model* function (line 7). The activity *percept* first checks for connected external JAM nodes. Secondly, it asks for all agents (nodes) of class *foo* and calculates an average (centre of mass) position from all nodes. Thirdly, it tests the presence of a survey reply tuple delivered by the survey agent. If a survey answer is found, a new digital twin agent is created with agent parameters derived from the survey results. Finally, a new instance of the survey explorer agent is created.

```
[](#cb65-1) 1: function world(p) {
[](#cb65-2) 2:  this.modelSim=null;
[](#cb65-3) 3:  this.survey=null;
[](#cb65-4) 4:  this.act = {
[](#cb65-5) 5:   start : () => {
[](#cb65-6) 6:    log('World is started.');
[](#cb65-7) 7:    this.modelSim = simu.model();
[](#cb65-8) 8:    sleep(500)
[](#cb65-9) 9:   },
[](#cb65-10)10:   wait : () => {
[](#cb65-11)11:     sleep(500)
[](#cb65-12)12:   },
[](#cb65-13)13:   percept : () => {
[](#cb65-14)14:    var nodes = link(DIR.IP('%'));
[](#cb65-15)15:    log('Connected? '+nodes);
[](#cb65-16)16:    var avgpos,n=0;
[](#cb65-17)17:    net.ask('agents-foo','*', (agent,node) => {
[](#cb65-18)18:     if (!avgpos) avgpos=copy(agent.pos);
[](#cb65-19)19:     else {
[](#cb65-20)20:      avgpos.x+=agent.pos.x;
[](#cb65-21)21:      avgpos.y+=agent.pos.y;
[](#cb65-22)22:     }
[](#cb65-23)23:     agent.speed=this.modelSim.parameter.speed;
[](#cb65-24)24:     agent.randomness=this.modelSim.parameter.randomness; 
[](#cb65-25)25:     n++
[](#cb65-26)26:    })
[](#cb65-27)27:    avgpos.x/=n;
[](#cb65-28)28:    avgpos.y/=n;
[](#cb65-29)29:    log('Center of mass: ',avgpos,n);
[](#cb65-30)30:    // return from survey agent?
[](#cb65-31)31:    if (test(['SURVEY','What kind of person are you?',_,_])) {
[](#cb65-32)32:     var t = inp(['SURVEY','What kind of person are you?',_,_]);
[](#cb65-33)33:     if (t[2]) {
[](#cb65-34)34:      var answer = t[2][4],
[](#cb65-35)35:          from  = t[2][1];
[](#cb65-36)36:      var s=0.1,r=0.1;
[](#cb65-37)37:      switch (answer) {
[](#cb65-38)38:       case 'quiet': s=0.05; r=0.05; break;
[](#cb65-39)39:       case 'restless': s=0.1; r=0.2; break;
[](#cb65-40)40:       case 'prudent': s=0.2; r=0.05; break;
[](#cb65-41)41:       case 'risky': s=0.5; r=0.2; break;
[](#cb65-42)42:      }
[](#cb65-43)43:      // create digital twin based on parameter set
[](#cb65-44)44:      net.create('agents-foo',1, (agent,index) => {
[](#cb65-45)45:       while (true) {
[](#cb65-46)46:        var x=random(0,49),y=random(0,49);
[](#cb65-47)47:        if (net.ask('agents-foo',[x,y]).length==0) { 
[](#cb65-48)48:         net.setxy(x,y)
[](#cb65-49)49:         break
[](#cb65-50)50:        } 
[](#cb65-51)51:        agent.speed=s;
[](#cb65-52)52:        agent.randomness=r;
[](#cb65-53)53:        net.set('shape','triangle');
[](#cb65-54)54:      })
[](#cb65-55)55:     }
[](#cb65-56)56:     // start new survey agent
[](#cb65-57)57:     this.survey=create('survey',{},1);
[](#cb65-58)58:    }
[](#cb65-59)59:   },
[](#cb65-60)60:   init : () => {
[](#cb65-61)61:    // NetLogo API
[](#cb65-62)62:    net.create('agents-foo',20, (agent) => {
[](#cb65-63)63:     while (true) {
[](#cb65-64)64:      var x=random(0,49),y=random(0,49);
[](#cb65-65)65:      if (net.ask('agents-foo',[x,y]).length==0) { 
[](#cb65-66)66:       net.setxy(x,y)
[](#cb65-67)67:       break
[](#cb65-68)68:      }
[](#cb65-69)69:     } 
[](#cb65-70)70:    })
[](#cb65-71)71:    // create survey agent
[](#cb65-72)72:    this.survey=create('survey',{},1);
[](#cb65-73)73:   }
[](#cb65-74)74:  }
[](#cb65-75)75:  this.trans = {
[](#cb65-76)76:   start   : init,
[](#cb65-77)77:   init    : wait,
[](#cb65-78)78:   wait    : percept,
[](#cb65-79)79:   percept : wait,
[](#cb65-80)80:  }
[](#cb65-81)81:  this.next = 'start';
[](#cb65-82)82: }
```

Example 13-2\. Example SEJAM2 world agent (world.js)

## Physical Random Walker Agent

The physical simulation agent performs a random walk in the simulation world. The speed and randomness parameters determine the walking behaviour. If an agent finds another agent in the neighbourhood it will change its colour to red, otherwise to blue. This is done in the activity *percept*. The *move* activity sets a new position of the agent if there is no other agent on the destination patch and if the position is inside the world bounding box. The walking direction is randomly changed from time to time in the activity *percept* (lines 26-32).

In addition to the random walking behaviour, computational explorer agents are created that can migrate to neighbouring nodes (lines 35-46).

```
[](#cb66-1) 1: function foo(p) {
[](#cb66-2) 2:  this.position = null;
[](#cb66-3) 3:  this.neighbors = [];
[](#cb66-4) 4:  this.goto=null;
[](#cb66-5) 5:  this.speed=p.speed||0.1;
[](#cb66-6) 6:  this.randomness=p.randomness||0.1;
[](#cb66-7) 7:  this.act = {
[](#cb66-8) 8:   start : () => {
[](#cb66-9) 9:    this.position = simu.position();
[](#cb66-10)10:    log('Agent is started  @ '+
[](#cb66-11)11:        this.position.x+','+this.position.y)
[](#cb66-12)12:   },
[](#cb66-13)13:   wait : () => {
[](#cb66-14)14:    sleep(200) // simulation steps
[](#cb66-15)15:   },
[](#cb66-16)16:   percept: () => {
[](#cb66-17)17:    // NetLogo API
[](#cb66-18)18:    var self=this,crowd=0;
[](#cb66-19)19:    this.position = simu.position();
[](#cb66-20)20:    net.ask('agents-foo',2, (agent,node) => {
[](#cb66-21)21:     if (agent.agent==self.id) return;
[](#cb66-22)22:     var dist = Math.max(1,distance(node.position,
[](#cb66-23)23:                                    self.position));
[](#cb66-24)24:     crowd += (1/dist);
[](#cb66-25)25:    })
[](#cb66-26)26:    if (crowd>0.1) net.set('color','red');
[](#cb66-27)27:    else net.set('color','blue');
[](#cb66-28)28:    if (random(0,1,0.1)<this.randomness) {
[](#cb66-29)29:     var dx = random([-1,0,1]),
[](#cb66-30)30:         dy = random([-1,0,1]);
[](#cb66-31)31:     this.goto={
[](#cb66-32)32:       x:dx,
[](#cb66-33)33:       y:dy
[](#cb66-34)34:     };
[](#cb66-35)35:    }
[](#cb66-36)36:    // Virtual wireless communication: 
[](#cb66-37)37:    // simulated ad-hoc v-JAM connectivity..
[](#cb66-38)38:    var neighbors=link(DIR.PATH('*'));
[](#cb66-39)39:    // Some new nodes?
[](#cb66-40)40:    iter(neighbors, (node) => {
[](#cb66-41)41:     if (!contains(this.neighbors,node)) {
[](#cb66-42)42:      log('New neighbor node '+node);
[](#cb66-43)43:      this.neighbors.push(node);
[](#cb66-44)44:      create('explorer',{
[](#cb66-45)45:        goto:node,
[](#cb66-46)46:        root:myNode(),
[](#cb66-47)47:      },1); /* only level 1-2 agents are mobile! */
[](#cb66-48)48:     }
[](#cb66-49)49:    }) 
[](#cb66-50)50:   },
[](#cb66-51)51:   move: () => {
[](#cb66-52)52:    // NetLogo API
[](#cb66-53)53:    if (random(0,1,0.1)>this.speed) return;
[](#cb66-54)54:    var dx = this.goto.x,
[](#cb66-55)55:        dy = this.goto.y;
[](#cb66-56)56:    if (this.position.x+dx<0 || 
[](#cb66-57)57:        this.position.x+dx>49) dx=0;
[](#cb66-58)58:    if (this.position.y+dy<0 || 
[](#cb66-59)59:        this.position.y+dy>49) dy=0;
[](#cb66-60)60:    // check new place occupancy
[](#cb66-61)61:    var x = this.position.x+dx,
[](#cb66-62)62:        y = this.position.y+dy;
[](#cb66-63)63:    if (net.ask('agents-foo',[x,y]).length==0)
[](#cb66-64)64:     net.setxy(x,y);
[](#cb66-65)65:   },
[](#cb66-66)66:  }
[](#cb66-67)67:  this.trans = {
[](#cb66-68)68:   start:wait,
[](#cb66-69)69:   wait:percept,
[](#cb66-70)70:   percept:() => { return this.goto?move:wait },
[](#cb66-71)71:   move: wait,
[](#cb66-72)72:  }
[](#cb66-73)73:  this.next = 'start';
[](#cb66-74)74: }
```

Example 13-3\. Example of a simple physical simulation agent with random walk behaviour (agent.js)

## Computational Explorer Agent

The following example of a simple computational explorer agent should only demonstrate the migration of this agent between different v-JAM nodes of the simulation world (using virtual *PATH* links only available in simulation). The destination node's identifier name is passed via the constructor parameter. The links between nodes are created dynamically by the simulator program (see simulation model). The explorer agent is created by the previously introduced physical random walker agent.

The explorer agent migrates to the destination node (activity *start*), senses the current clock in the destination node and its position in activity *percept*, goes back to its root node in activity *goback*, finally delivers the sensor results in activity *deliver*.

```
[](#cb67-1) 1: function explorer(p) {
[](#cb67-2) 2:  this.goto=p.goto;
[](#cb67-3) 3:  this.root=p.root;
[](#cb67-4) 4:  this.sensor=null;
[](#cb67-5) 5:  this.act = {
[](#cb67-6) 6:   start: () => {
[](#cb67-7) 7:    log('Explorer started. Destination: '+this.goto);
[](#cb67-8) 8:    if (link(DIR.PATH(this.goto))) {
[](#cb67-9) 9:     log('Going to '+this.goto); 
[](#cb67-10)10:     moveto(DIR.PATH(this.goto));
[](#cb67-11)11:    } else { log('No path to '+this.goto); this.goto=null };
[](#cb67-12)12:   },
[](#cb67-13)13:   percept : () => {
[](#cb67-14)14:    log('I am arrived on '+myNode());
[](#cb67-15)15:    this.sensor={time:clock(),pos:info('node').position};
[](#cb67-16)16:    this.goto=null;
[](#cb67-17)17:   },
[](#cb67-18)18:   goback : () => {
[](#cb67-19)19:    if (link(DIR.PATH(this.root))) {
[](#cb67-20)20:     this.goto=this.root;
[](#cb67-21)21:     log('Going to '+this.goto);
[](#cb67-22)22:     moveto(DIR.PATH(this.goto));
[](#cb67-23)23:    } else sleep(50);
[](#cb67-24)24:   },
[](#cb67-25)25:   deliver : () => {
[](#cb67-26)26:    log('I am back on '+myNode()+' with sensor '+this.sensor);
[](#cb67-27)27:   },
[](#cb67-28)28:   end : () => {
[](#cb67-29)29:    log('Terminating.');
[](#cb67-30)30:    kill()
[](#cb67-31)31:   }
[](#cb67-32)32:  }
[](#cb67-33)33:  this.trans = {
[](#cb67-34)34:   start:() => { return this.goto?percept:end },
[](#cb67-35)35:   percept : goback,
[](#cb67-36)36:   goback  : () => { return this.goto?deliver:goback },
[](#cb67-37)37:   deliver : end,
[](#cb67-38)38:  }
[](#cb67-39)39:  this.next='start'
[](#cb67-40)40: }
```

Example 13-4\. An example of a simple computational explorer agent (explorer.js)

## Computational Micro-survey Agent

The following more complex survey explorer agent features path travelling over external relay JAM nodes (public servers). The explorer agent tries to find mobile nodes with a chat agent (detected by the presence of a *CHAT* tuple). If the explorer agent stays on a mobile node with a chat agent (assuming a human user is available for questions), the agent will submit messages and questions to the chat agent via the local tuple space. The survey waits for a limited time on the answer, provided via the tuple space, too. In this version, the survey agent only visits one mobile node. It can be easily extended to visit multiple mobile nodes all connected to the relay node. The code of the chat moderator agent is shown in Sec. [13-7](#12_examples.xhtml_sec_chat_moderator_agent_6).

The chat agent (with direct access to the mobile App chat dialogue) processes client requests received via the tuple space. There are basically three different requests: Messages without an answer; questions with selection from choices `{choices: [A,B,C,..], mutual?}`; and numerical and text input with a question `{type: 'text' | 'number', default?, value?: number | string}`.

The activity trace of the agent starts with the *search* activity. The *search* activity searches for externally connected nodes. If the *relay* body variable is not set, it will select the first found node and migrate to this node (assuming it is a relay node). If the agent is already on the relay node, it selects another node (not the root origin node) to migrate to it. If no more nodes are found, it initiates the *goback* activity.

If the agent has found a node with a chat agent by testing the `CHAT` tuple in the *percept* activity, it will open a chat session and request a time-limited session token in the *sessionOpen* activity. If this was successful, the activity *ask* will ask his question and wait for a response from the chat agent or a time-out. After asking, it closes the session in the activity *sessionClose* and migrates back to the relay node via the *goback* activity. After the relay node reaches its destination, it goes back to its root node. Finally, the survey result is delivered in the *deliver* activity by inserting a `SURVEY` tuple in the local tuple space.

```
[](#cb68-1)  1: function survey (options) {
[](#cb68-2)  2:  this.root=null;  // start
[](#cb68-3)  3:  this.relay=null; // relay
[](#cb68-4)  4:  this.visited=[]; // all visited nodes
[](#cb68-5)  5:  this.chat=null;  // current chat node
[](#cb68-6)  6:  this.answer=null;
[](#cb68-7)  7:  this.token=null; // chat session token
[](#cb68-8)  8:  this.timeout=10000;
[](#cb68-9)  9:  this.goback=false; // return to root?
[](#cb68-10) 10: 
[](#cb68-11) 11:  this.act = {
[](#cb68-12) 12:   init: () => {
[](#cb68-13) 13:    this.root=myNode()
[](#cb68-14) 14:   },
[](#cb68-15) 15:   percept: () => {
[](#cb68-16) 16:    if (test(['CHAT',_])) {
[](#cb68-17) 17:     // Found chat agent and chat app
[](#cb68-18) 18:     this.chat=myNode()
[](#cb68-19) 19:    }
[](#cb68-20) 20:   },
[](#cb68-21) 21:   search: () => {
[](#cb68-22) 22:    var connected=link(DIR.IP('%'))
[](#cb68-23) 23:    if (connected.length==1 && !this.relay) {
[](#cb68-24) 24:     // from root to relay
[](#cb68-25) 25:     this.relay=connected[0];
[](#cb68-26) 26:     moveto(DIR.NODE(this.relay))
[](#cb68-27) 27:    } else if (myNode() == this.relay) {
[](#cb68-28) 28:     // from relay to user device
[](#cb68-29) 29:     connected=filter(connected, (node) => {
[](#cb68-30) 30:      return (node != this.root) && 
[](#cb68-31) 31:              !contains(this.visited,node)
[](#cb68-32) 32:     })
[](#cb68-33) 33:     var next=random(connected);
[](#cb68-34) 34:     if (next) {
[](#cb68-35) 35:      moveto(DIR.NODE(next))
[](#cb68-36) 36:     } else {
[](#cb68-37) 37:      this.goback=true;
[](#cb68-38) 38:     }
[](#cb68-39) 39:    } else if (connected.length) {
[](#cb68-40) 40:     // from user back to relay
[](#cb68-41) 41:     this.visited.push(myNode())
[](#cb68-42) 42:     // Going back to relay
[](#cb68-43) 43:     moveto(DIR.NODE(connected[0]))
[](#cb68-44) 44:    } else sleep(500);
[](#cb68-45) 45:   },
[](#cb68-46) 46:   sessionOpen :  () => { 
[](#cb68-47) 47:    // get a session token
[](#cb68-48) 48:    mark(['CHAT-SESSION',me(),60000],this.timeout);
[](#cb68-49) 49:    this.token=null;
[](#cb68-50) 50:    inp.try(this.timeout,['CHAT-TOKEN',me(),_], (reply) => {
[](#cb68-51) 51:     if (reply) this.token=reply[2];
[](#cb68-52) 52:     else rm(['CHAT-SESSION',me(),60000]);
[](#cb68-53) 53:    });
[](#cb68-54) 54:   },
[](#cb68-55) 55:   sessionClose : () => {
[](#cb68-56) 56:    mark(['CHAT-SESSION',me(),0],this.timeout); 
[](#cb68-57) 57:   },
[](#cb68-58) 58:   ask : () => {
[](#cb68-59) 59:    // micro survey
[](#cb68-60) 60:    out(['CHAT-MESSAGE',me(),this.token,
[](#cb68-61) 61:         'Hello from the doctor from star '+this.root])
[](#cb68-62) 62:    out(['CHAT-QUESTION',me(),this.token,
[](#cb68-63) 63:         'What kind of person are you?',{
[](#cb68-64) 64:         choices:['quiet',
[](#cb68-65) 65:                  'restless',
[](#cb68-66) 66:                  'prudent',
[](#cb68-67) 67:                  'risky'],mutual:true}])
[](#cb68-68) 68:    // wait for answer or timeout
[](#cb68-69) 69:    inp.try(30000,['CHAT-ANSWER',me(),
[](#cb68-70) 70:           this.token,'What kind of person are you?',_], 
[](#cb68-71) 71:           (t) => {
[](#cb68-72) 72:             this.answer=t;
[](#cb68-73) 73:           })
[](#cb68-74) 74:   },
[](#cb68-75) 75:   goback: () => {
[](#cb68-76) 76:    var next;
[](#cb68-77) 77:    if (myNode() == this.relay) {
[](#cb68-78) 78:     if (link(DIR.NODE(this.root))) next=this.root 
[](#cb68-79) 79:    } else if (myNode() == this.chat) {
[](#cb68-80) 80:     if (link(DIR.NODE(this.relay))) next=this.relay 
[](#cb68-81) 81:    }
[](#cb68-82) 82:    if (next) moveto(DIR.NODE(next));
[](#cb68-83) 83:     else kill()
[](#cb68-84) 84:   },
[](#cb68-85) 85:   deliver : () => {
[](#cb68-86) 86:    // Deliver the survey result
[](#cb68-87) 87:    out(['SURVEY','What kind of person are you?',
[](#cb68-88) 88:         this.answer,this.chat])
[](#cb68-89) 89:   },
[](#cb68-90) 90:   end : () => {
[](#cb68-91) 91:    kill()
[](#cb68-92) 92:   }
[](#cb68-93) 93:  }
[](#cb68-94) 94:  this.trans = {
[](#cb68-95) 95:   init : search,
[](#cb68-96) 96:   search : () => { return this.goback?goback:percept},
[](#cb68-97) 97:   percept : () => { return this.chat?sessionOpen:search },
[](#cb68-98) 98:   sessionOpen : () => { return this.token?ask:goback },
[](#cb68-99) 99:   ask : sessionClose,
[](#cb68-100)100:   sessionClose : goback,
[](#cb68-101)101:   goback : () => { return myNode()!=this.root?goback:deliver },
[](#cb68-102)102:   deliver : end
[](#cb68-103)103:  }
[](#cb68-104)104:  this.next = init
[](#cb68-105)105: }
```

Example 13-5\. An example of a full-featured computational explorer and survey agent (survey.js) that performs MCS on mobile platforms meets a chat agent with a user interface. It is assumed that the node origin as well as the JAM App are connected to an external relay node.

## Universal Survey Agent

This universal survey agent is used to perform a distributed participatory survey with a dialogue snippet database introduced in Sec. [11-1](#10_mobile-crowdsensing-with-jam.xhtml_sec_surveys_0). The agent utilizes a divide-and-conquer strategy to reach multiple mobile user platforms using relay nodes. In the following code Ex. [13-6](#12_examples.xhtml_surveyex1), only the relevant activities *arrived* and *ask* are shown. The *ask* activity provides the interface to the chat agent and chat dialogue. Different question formats (choice list, number selection, free text) are supported. Finally, this activity collects values from platform sensors via the tuple space. The actual sensor values are delivered by a platform tuple space provider function.

```
[](#cb69-1) 1:  this.token=null;
[](#cb69-2) 2:  // sensors collect sensor data and survey answers
[](#cb69-3) 3:  // {$nodeid:{$answertag:*,$sensor:*}
[](#cb69-4) 4:  this.sensors={};
[](#cb69-5) 5:  this.index=0;
[](#cb69-6) 6:  this.dialog=options.dialog;
[](#cb69-7) 7:  this.dialogMap=null;
[](#cb69-8) 8:  this.dialogNext=null;
[](#cb69-9) 9:  this.act = {
[](#cb69-10)10:   ..
[](#cb69-11)11:   arrived : () => {
[](#cb69-12)12:    this.node = myNode();
[](#cb69-13)13:    this.index = 0;
[](#cb69-14)14:    this.dialogNext=this.dialog[0];
[](#cb69-15)15:    this.sensors[this.node]={}
[](#cb69-16)16:   },
[](#cb69-17)17:   ask: () => {
[](#cb69-18)18:    var self=this, next=this.dialogNext;
[](#cb69-19)19:    if (next.message) {
[](#cb69-20)20:     var msg=typeof next.message == 'function'?
[](#cb69-21)21:             next.message(this.dialogMap):
[](#cb69-22)22:             next.message;
[](#cb69-23)23:     mark(['CHAT-MESSAGE',me(),this.token,msg],this.timeout);
[](#cb69-24)24:    } else if (next.question) {
[](#cb69-25)25:     var msg=typeof next.question == 'function'?
[](#cb69-26)26:             next.message(this.dialogMap):
[](#cb69-27)27:             next.message;
[](#cb69-28)28:     if (next.choices)
[](#cb69-29)29:      mark(['CHAT-QUESTION',me(),this.token,
[](#cb69-30)30:            msg,{choices:next.choices}],this.timeout);
[](#cb69-31)31:     else
[](#cb69-32)32:      mark(['CHAT-QUESTION',me(),this.token,
[](#cb69-33)33:            msg,{
[](#cb69-34)34:             type:next.range?'number':'text',
[](#cb69-35)35:             range:next.range,
[](#cb69-36)36:             value:next.value,
[](#cb69-37)37:           }],this.timeout)
[](#cb69-38)38:      inp.try(this.timeout,[
[](#cb69-39)39:       'CHAT-ANSWER',
[](#cb69-40)40:       me(),
[](#cb69-41)41:       this.token,
[](#cb69-42)42:       next.question,_],
[](#cb69-43)43:       (reply) => {
[](#cb69-44)44:        next.answer =
[](#cb69-45)45:        this.sensors[this.node][next.tag] =
[](#cb69-46)46:         reply && reply[4] && 
[](#cb69-47)47:         (next.range?Number(reply[4]):reply[4]));
[](#cb69-48)48:        if (!reply || reply[4]==undefined) { /*stop*/ 
[](#cb69-49)49:         if (!this.survey.dialog[this.survey.dialog.length-1]
[](#cb69-50)50:             .question)
[](#cb69-51)51:          this.index=this.survey.dialog.length-1;
[](#cb69-52)52:         else 
[](#cb69-53)53:          this.index=-1; 
[](#cb69-54)54:        }
[](#cb69-55)55:       })
[](#cb69-56)56:    } else if (next.sensors) {
[](#cb69-57)57:     iter(next.sensors, (sensor) => {
[](#cb69-58)58:      // sensors if available are provided via 
[](#cb69-59)59:      // tuple space provider function
[](#cb69-60)60:      // serviced by the host platform
[](#cb69-61)61:      var sample = inp.try(0,['SENSOR',sensor,_]);
[](#cb69-62)62:      if (sample) this.sensors[this.node]2-5=sample;
[](#cb69-63)63:     }) 
[](#cb69-64)64:    }
[](#cb69-65)65:   }
```

Example 13-6\. An example of a generic survey agent performing distributed surveys based on a divide-and-conquer strategy

## Chat Moderator Agent

The chat moderator agent can only be used on the JAM App (Cordova or Web browser version jamapp.html). A survey agent that wants to talk with the user via the chat moderator must initiate a session (optionally with a access key) to get a session token. A session token is only granted for a specific time interval. The basic code of the chat moderator agent accessing an extended AIOS API (`message`, `question`, `notify`, `beep`) via the App is shown in Ex. [13-7](#12_examples.xhtml_sejamex6) and the JAM App chat dialogue in Fig. [13-1](#12_examples.xhtml_jamapp1).

The client and moderator agent communicate entirely over the tuple space without knowing each other. Chat and user agents communicate entirely over the tuple space via four tuple patterns:

* * *

```
[](#cb70-1)// From requesting agent to chat moderator:
[](#cb70-2)['CHAT-MESSAGE',from,token,message]
[](#cb70-3)['CHAT-NOTIFY',from,token,message]
[](#cb70-4)['CHAT-QUESTION',from,token,question,action]
[](#cb70-5)['CHAT-SESSION',from,time]
[](#cb70-6)// From moderator to requesting agent
[](#cb70-7)['CHAT-ANSWER',from,token,question,answer]
```

* * *

The chat agent waits for a new session request in the activity *process*. If a session is opened, it waits for questions and messages from the current client agent. All communication is performed anonymously via the tuple space. Answers from the users are replied to via the tuple space too.

![#jamapp1](images/58aa5ee5-fd2e-42e5-9409-08c5164be34e.png)Figure 13-1\. The JAM App chat dialogue is controlled by the chat moderator agent (page view)

The initialization activity *init* stores a tuple `[’CHAT’,this.idn]` (line 26) to publish its service for chat user agents. The moderator agent is a long-time running agent, and must negotiate an extended run and lifetime (lines 24-25). The *talk* activity gets in touch with the user (of the App) to ask him for participation in the chat. Only if the user has granted participation, the moderator agent process chat agent requests. The *process* activity processes requests from chat agents via tuple exchange using the *alt.try* operation. After a chat agent successfully negotiates a session, the moderator will process questions and message tokens. Because there is a platform limit of tuple lifetime, the *refresh* activity refreshes the service publishing tuple periodically. Finally, the *dodialog* activity passes question and message tokens to the chat API of the App and waits for a response from the user.

```
[](#cb71-1)  1: function chat(options) {
[](#cb71-2)  2:  // remember delay time
[](#cb71-3)  3:  this.remember     = 2000;
[](#cb71-4)  4:  // on or off
[](#cb71-5)  5:  this.state        = 'off';
[](#cb71-6)  6:  this.busy         = false;
[](#cb71-7)  7:  // Current survey session? -> {from:string,stamp:number}
[](#cb71-8)  8:  this.session      = null;
[](#cb71-9)  9:  this.token        = 1001;
[](#cb71-10) 10:  this.sessionTime  = 60000;
[](#cb71-11) 11:  // last chat dialog action
[](#cb71-12) 12:  this.last         = 0;
[](#cb71-13) 13:  // Default question-response timeout
[](#cb71-14) 14:  this.timeout      = 40000;
[](#cb71-15) 15:  // pending dialog requests
[](#cb71-16) 16:  this.dialogs      = [];
[](#cb71-17) 17:  this.idn          = 0;
[](#cb71-18) 18: 
[](#cb71-19) 19:  this.act = {
[](#cb71-20) 20:   // Initialize the moderator agent
[](#cb71-21) 21:   init :  () => {
[](#cb71-22) 22:    var t;
[](#cb71-23) 23:    this.busy   = false;
[](#cb71-24) 24:    negotiate('CPU',10000000);
[](#cb71-25) 25:    negotiate('LIFE',1000000);
[](#cb71-26) 26:    this.idn=random(1000000); out(['CHAT',this.idn]);
[](#cb71-27) 27:   },
[](#cb71-28) 28: 
[](#cb71-29) 29:   // Get feedback from user: chilling to chatting?
[](#cb71-30) 30:   talk: () => {
[](#cb71-31) 31:    message('Moderator','Hello, I am '+me()+', 
[](#cb71-32) 32:            your moderator :-)');
[](#cb71-33) 33:    // Blocking operation (with timeout)
[](#cb71-34) 34:    this.state=null;
[](#cb71-35) 35:    this.busy=true;
[](#cb71-36) 36:    question('Moderator','What would you like to do?',[
[](#cb71-37) 37:       {text:'Chilling',value:'off'},
[](#cb71-38) 38:       {text:'Answer questions', value:'on'} 
[](#cb71-39) 39:     ], (res) => {
[](#cb71-40) 40:      this.state=res;
[](#cb71-41) 41:      if (this.verbose) log('[CHAT] Got answer '+res+'.')
[](#cb71-42) 42:      if (res=='on') {
[](#cb71-43) 43:       notify('Now I will mediate questions from agents!');
[](#cb71-44) 44:       message('Moderator',
[](#cb71-45) 45:               'Now I will mediate questions from agents!');
[](#cb71-46) 46:       message('Moderator',
[](#cb71-47) 47:               'Hope you will answer their questions!'); 
[](#cb71-48) 48:      }
[](#cb71-49) 49:      this.busy=false;
[](#cb71-50) 50:     });
[](#cb71-51) 51:   },
[](#cb71-52) 52: 
[](#cb71-53) 53:   process: () => {
[](#cb71-54) 54:    alt.try(500,[
[](#cb71-55) 55:      ['CHAT-MESSAGE',_,_,_],
[](#cb71-56) 56:      ['CHAT-NOTIFY',_,_,_],
[](#cb71-57) 57:      ['CHAT-QUESTION',_,_,_,_],
[](#cb71-58) 58:      ['CHAT-SESSION',_,_],
[](#cb71-59) 59:    ], (t) => {
[](#cb71-60) 60:     if (this.session && this.session.stop<time()) 
[](#cb71-61) 61:       this.session=null;
[](#cb71-62) 62:     if (t) switch (t[0]) {
[](#cb71-63) 63:      case 'CHAT-MESSAGE':
[](#cb71-64) 64:       if (!this.session || 
[](#cb71-65) 65:           this.session.from!=t[1] ||
[](#cb71-66) 66:           this.session.token!=t[2]) return log(t);
[](#cb71-67) 67: 
[](#cb71-68) 68:       this.dialogs.push({
[](#cb71-69) 69:        message: t[3],
[](#cb71-70) 70:        from:    t[1] 
[](#cb71-71) 71:       }); 
[](#cb71-72) 72:       break;
[](#cb71-73) 73: 
[](#cb71-74) 74:      case 'CHAT-NOTIFY':
[](#cb71-75) 75:       if (!this.session || 
[](#cb71-76) 76:           this.session.from!=t[1] ||
[](#cb71-77) 77:           this.session.token!=t[2]) return log(t);
[](#cb71-78) 78: 
[](#cb71-79) 79:       notify(t[3]);
[](#cb71-80) 80:       beep();
[](#cb71-81) 81:       break;
[](#cb71-82) 82: 
[](#cb71-83) 83:      case 'CHAT-QUESTION': 
[](#cb71-84) 84:       if (!this.session || 
[](#cb71-85) 85:           this.session.from!=t[1] ||
[](#cb71-86) 86:           this.session.token!=t[2]) return log(t);
[](#cb71-87) 87: 
[](#cb71-88) 88:       this.dialogs.push({
[](#cb71-89) 89:        question: t[3],
[](#cb71-90) 90:        from:     t[1],
[](#cb71-91) 91:        options:  t[4]
[](#cb71-92) 92:       }); 
[](#cb71-93) 93:       break;
[](#cb71-94) 94: 
[](#cb71-95) 95:     case 'CHAT-SESSION': 
[](#cb71-96) 96:      if (!this.session && t[2]>0) {
[](#cb71-97) 97:       this.session = {
[](#cb71-98) 98:        token :  this.token++,
[](#cb71-99) 99:        from  : t[1],
[](#cb71-100)100:        stamp : time(),
[](#cb71-101)101:        start : time(),
[](#cb71-102)102:        stop  : time()+Math.min(this.sessionTime,t[2])
[](#cb71-103)103:       };
[](#cb71-104)104:       mark(['CHAT-TOKEN',this.session.from,
[](#cb71-105)105:                          this.session.token],1000);
[](#cb71-106)106:      } else if (this.session && t[2]==0 && 
[](#cb71-107)107:                 this.session.from==t[1]) {
[](#cb71-108)108:       this.session=null; 
[](#cb71-109)109:      }
[](#cb71-110)110:      break;
[](#cb71-111)111:     }
[](#cb71-112)112:    });
[](#cb71-113)113:   },
[](#cb71-114)114: 
[](#cb71-115)115:   refresh : () => {
[](#cb71-116)116:    // refresh our chat tuple
[](#cb71-117)117:    if (!ts(['CHAT',this.idn],600000)) {
[](#cb71-118)118:     out(['CHAT',this.idn]);
[](#cb71-119)119:    } 
[](#cb71-120)120:   },
[](#cb71-121)121:   // process a doalog snippet
[](#cb71-122)122:   dodialog: () => {
[](#cb71-123)123:    var action;
[](#cb71-124)124:    if (this.busy) return;
[](#cb71-125)125:    var d=this.dialogs.shift();
[](#cb71-126)126:    if (d.message) {
[](#cb71-127)127:     this.busy=true;
[](#cb71-128)128:     message(d.from,d.message);
[](#cb71-129)129:     this.busy=false;
[](#cb71-130)130:    } else if (d.question) {
[](#cb71-131)131:     this.busy=true;
[](#cb71-132)132:     if (d.options.choices && d.options.mutual) 
[](#cb71-133)133:       action = d.options.choices;
[](#cb71-134)134:      else if (d.options.choices && !d.options.mutual) {
[](#cb71-135)135:       action = {
[](#cb71-136)136:        placeholder : 'Select',
[](#cb71-137)137:        multipleselect : true,
[](#cb71-138)138:        value : '',
[](#cb71-139)139:        button : {
[](#cb71-140)140:         icon: 'check',
[](#cb71-141)141:         label: 'OK'
[](#cb71-142)142:        },
[](#cb71-143)143:        options:d.options.choices
[](#cb71-144)144:       };
[](#cb71-145)145:      } else {
[](#cb71-146)146:       action = {
[](#cb71-147)147:        size:         14,
[](#cb71-148)148:        value:        d.options.value||'', 
[](#cb71-149)149:        sub_type:     d.options.type || 'text',
[](#cb71-150)150:        placeholder:  d.options.default||'' 
[](#cb71-151)151:       };
[](#cb71-152)152:      }
[](#cb71-153)153:      question(d.from,d.question,action, (res) => {
[](#cb71-154)154:        mark(['CHAT-ANSWER',
[](#cb71-155)155:              d.from,
[](#cb71-156)156:              this.session.token,
[](#cb71-157)157:              d.question,
[](#cb71-158)158:              res],10000);
[](#cb71-159)159:        this.busy=false;
[](#cb71-160)160:       },min(this.timeout,d.options.timeout||
[](#cb71-161)161:                          this.timeout));
[](#cb71-162)162:      }
[](#cb71-163)163:   },
[](#cb71-164)164: 
[](#cb71-165)165: 
[](#cb71-166)166:   remember: () => {
[](#cb71-167)167:    this.busy=false; 
[](#cb71-168)168:    sleep(this.remember) 
[](#cb71-169)169:   },
[](#cb71-170)170: 
[](#cb71-171)171:   end: () => {
[](#cb71-172)172:    kill()
[](#cb71-173)173:   }
[](#cb71-174)174:  }
[](#cb71-175)175: 
[](#cb71-176)176:  this.trans = {
[](#cb71-177)177:   init:talk,
[](#cb71-178)178:   talk: () => { 
[](#cb71-179)179:    return this.state=='on'?refresh:remember 
[](#cb71-180)180:   },
[](#cb71-181)181:   process: () => { 
[](#cb71-182)182:    if (this.dialogs.length) return dodialog;
[](#cb71-183)183:    else return refresh 
[](#cb71-184)184:   },
[](#cb71-185)185:   refresh : process,
[](#cb71-186)186:   remember: talk,
[](#cb71-187)187:   dodialog: refresh,
[](#cb71-188)188:  }
[](#cb71-189)189: 
[](#cb71-190)190:  this.next=init
[](#cb71-191)191: }
```

Example 13-7\. An example of a chat moderator agent (chat.js) that services MCS on platforms using the mobile JAM App

## Web Page with JAM

The Web page shown in Ex. [13-8](#12_examples.xhtml_sejamex7) provides an eye-catcher (animated GIF image) with a weird comic scene. The user should visit the page as long as possible to keep the experiment online. A JAM node is created under the hood and a data delivery agent is created on it. The JAM node connects via AMP to an external public relay node. Note that only HTTp and HTTPS are supported protocols, which must be supported by the relay node via respective ports. Additionally, if the Web page is loaded via HTTP, the HTTP protocol must be used for AMP, too, otherwise HTTPS (mixed HTTP/HTTPS requests are commonly denied by the browser).

The delivery agent forks a child agent that migrates to a relay node. The parent-child pair communicates via signals. The parent agent initially sends user data (location information, browser agent, etc.). A text field on the Web page should be used to answer a fake question. The text input of the user is sent to the child agent via a signal, too. The child agent stores received data tuples in the tuple space of the relay node. The parent agent sends PING messages periodically. If the child agent does not receive PING messages, it will terminate.

This Web page is used in conjunction with a data collector agent (see Ex. [13-9](#12_examples.xhtml_sejamex8)) that forks a child agent that migrates to the relay node, too. The collector agent consumes the data tuples stored by the delivery agent. Again, a parent-child pair is used that transmits data via signals.

Note that the Web page installs a sleep hack (`HackTimer.js` embedded in the `jamlib.browser.js` file). Web pages are throttled by the browser program if not visible. This leads to a shutdown of the JAM logic, which causes a lot of time-out issues. The HackTimer moves critical timers to a WebWorker context that will typically not be throttled. Alternatively, the JAM Vm can be executed in a WebWorker, requiring some additional WebWorker logic.

The Web page includes the JAM library in line 3\. A script tag inside the HTML body (lines 11-164) is the core logic to instantiate the JAM node and the collector agent, which is embedded, too. After the JAM instance is created, it must be initialized and the JAM scheduler loop must be started. To get geolocation information, the *locate* method is called. It performs a multi-stage IP-based and GPS-based (if available) geospatial location using external services (like Mozilla), too. After the collector agent starts, this script is done, and JAM and its agents are operating in the "background".

```
[](#cb72-1)  1: <html>
[](#cb72-2)  2: <head>
[](#cb72-3)  3: <script src="jamlib.browser.js"></script>
[](#cb72-4)  4: </head>
[](#cb72-5)  5: <body>
[](#cb72-6)  6: <img src="proxy-image.gif"/>
[](#cb72-7)  7: <p>
[](#cb72-8)  8: Tell daddy what's wrong here and win a prize ..
[](#cb72-9)  9: </p>
[](#cb72-10) 10: <textarea id="tellhim">???</textarea>
[](#cb72-11) 11: <script>
[](#cb72-12) 12: /* Object { Aios: Object, 
[](#cb72-13) 13:             Comp: Object, Esprima: Object, 
[](#cb72-14) 14:             Io: Object, Jam: function, 
[](#cb72-15) 15:             Json: Object, 
[](#cb72-16) 16:             environment: Object, 
[](#cb72-17) 17:             options: Object }
[](#cb72-18) 18: */
[](#cb72-19) 19: var jam    = JAMLIB.Jam({}),
[](#cb72-20) 20:     DIR    = jam.DIR;
[](#cb72-21) 21: jam.init();
[](#cb72-22) 22: // Start multi-stage geolocation
[](#cb72-23) 23: jam.locate((loc,err) => {
[](#cb72-24) 24:   // location is resolved
[](#cb72-25) 25:   // inject tuple and schedule
[](#cb72-26) 26:   // wake-up sleeping foo agent
[](#cb72-27) 27:   jam.out(['LOCATION',loc]);
[](#cb72-28) 28:   jam.schedule();
[](#cb72-29) 29: }, {verbose:1}); 
[](#cb72-30) 30: // Start the JAM scheduler loop
[](#cb72-31) 31: jam.start();
[](#cb72-32) 32: jam.extend([1,2,3],'DOM', (cmd,tag,content) => {
[](#cb72-33) 33:   switch (cmd) {
[](#cb72-34) 34:     case 'agent': return navigator.userAgent;
[](#cb72-35) 35:     case 'get': return document.getElementById(tag);
[](#cb72-36) 36:   }
[](#cb72-37) 37: },[2,3])
[](#cb72-38) 38: if (document.URL.indexOf('https')==0) {
[](#cb72-39) 39:   jam.createPort(DIR.IP('https://localhost:*'))
[](#cb72-40) 40:   jam.connectTo(DIR.IP('https://ag-0.de:30001'+
[](#cb72-41) 41:                        '?secure=12:..'))
[](#cb72-42) 42: } else {
[](#cb72-43) 43:   jam.createPort(DIR.IP('http://localhost:*'))
[](#cb72-44) 44:   jam.connectTo(DIR.IP('http://ag-0.de:30002'+
[](#cb72-45) 45:                        '?secure=12:..'))
[](#cb72-46) 46: }
[](#cb72-47) 47: function foo(opts) {
[](#cb72-48) 48:   this.data=[];
[](#cb72-49) 49:   this.root=null;
[](#cb72-50) 50:   this.relay=null;
[](#cb72-51) 51:   this.goto=opts.goto||'';
[](#cb72-52) 52:   this.state=0;
[](#cb72-53) 53:   this.child=null;
[](#cb72-54) 54:   this.last=null;
[](#cb72-55) 55:   this.lastTime=0;
[](#cb72-56) 56:   this.location=null;
[](#cb72-57) 57:   this.alive=0;
[](#cb72-58) 58:   this.act = {
[](#cb72-59) 59:     start : () => {
[](#cb72-60) 60:       if (this.goto)
[](#cb72-61) 61:         moveto(DIR.NODE(this.goto));
[](#cb72-62) 62:       else
[](#cb72-63) 63:         this.root=myNode();
[](#cb72-64) 64:       if (!this.state) this.state=1;
[](#cb72-65) 65:       // wait for location resolved
[](#cb72-66) 66:       if (!this.goto) 
[](#cb72-67) 67:         rd.try(30000,["LOCATION",_],
[](#cb72-68) 68:           (t) => {
[](#cb72-69) 69:            log(t)
[](#cb72-70) 70:            if (t) this.location=t[1];
[](#cb72-71) 71:         })
[](#cb72-72) 72:     },
[](#cb72-73) 73:     spy : () => {
[](#cb72-74) 74:       if (!this.relay) {
[](#cb72-75) 75:         var nodes = link(DIR.IP('%'));
[](#cb72-76) 76:         if (nodes.length) this.relay=nodes[0];
[](#cb72-77) 77:       }
[](#cb72-78) 78:       if (this.relay && this.state==1)  {
[](#cb72-79) 79:         this.state=2;
[](#cb72-80) 80:         var data = copy(info('node')),
[](#cb72-81) 81:             agent = DOM('agent');
[](#cb72-82) 82:         data.agent = agent;
[](#cb72-83) 83:         data.stamp = time();
[](#cb72-84) 84:         this.data.push(data);
[](#cb72-85) 85:         this.child=fork({goto:this.relay})
[](#cb72-86) 86:         this.alive=time()
[](#cb72-87) 87:       }
[](#cb72-88) 88:       if (this.relay && this.state==2 && 
[](#cb72-89) 89:           (time()-this.alive)>10000)  {
[](#cb72-90) 90:         // Lost child agent, not responding
[](#cb72-91) 91:         var nodes = link(DIR.IP('%'));
[](#cb72-92) 92:         if (nodes.length) this.relay=nodes[0];
[](#cb72-93) 93:         else this.relay=null;
[](#cb72-94) 94:         if (this.relay) {
[](#cb72-95) 95:           // Creating new agent
[](#cb72-96) 96:           this.child=fork({goto:this.relay,data:[]})
[](#cb72-97) 97:           this.alive=time()
[](#cb72-98) 98:         }
[](#cb72-99) 99:       }
[](#cb72-100)100:       var tellhim = DOM('get','tellhim');
[](#cb72-101)101:       if (tellhim.value != this.last && 
[](#cb72-102)102:           tellhim.value.length > 5) {
[](#cb72-103)103:         this.last=tellhim.value;
[](#cb72-104)104:         this.lastTime=time()
[](#cb72-105)105:       } else if (this.last && this.lastTime && 
[](#cb72-106)106:                  (time()-this.lastTime) > 10000 && 
[](#cb72-107)107:                  this.child) {
[](#cb72-108)108:         var data = {
[](#cb72-109)109:           id:this.root,
[](#cb72-110)110:           stamp:time(),
[](#cb72-111)111:           answer:this.last
[](#cb72-112)112:         }
[](#cb72-113)113:         // send child agent a message
[](#cb72-114)114:         send(this.child,'DATA',[data])
[](#cb72-115)115:         this.lastTime=0
[](#cb72-116)116:       }
[](#cb72-117)117:       if (this.child) 
[](#cb72-118)118:         send(this.child,'PING');
[](#cb72-119)119:       sleep(1000)
[](#cb72-120)120:     },
[](#cb72-121)121:     go : () => {
[](#cb72-122)122:       log('Go to '+this.goto);
[](#cb72-123)123:       moveto(DIR.NODE(this.goto));
[](#cb72-124)124:     },
[](#cb72-125)125:     deliver : () => {
[](#cb72-126)126:       // Deliver new data
[](#cb72-127)127:       mark(['WEBSPY',
[](#cb72-128)128:             this.data],
[](#cb72-129)129:             12*60*60*1000);
[](#cb72-130)130:       timer.add(1000,
[](#cb72-131)131:                 'CHECKPOINT',
[](#cb72-132)132:                 null,
[](#cb72-133)133:                 true);
[](#cb72-134)134:       sleep()
[](#cb72-135)135:     }
[](#cb72-136)136:   }
[](#cb72-137)137:   this.trans = {
[](#cb72-138)138:     start : spy,
[](#cb72-139)139:     spy : () => { return this.goto?go:spy },
[](#cb72-140)140:     go : deliver
[](#cb72-141)141:   }
[](#cb72-142)142:   this.on = {
[](#cb72-143)143:     'DATA': (arg,from) => {
[](#cb72-144)144:       // Got DATA
[](#cb72-145)145:       log(arg)
[](#cb72-146)146:       mark(['WEBSPY',arg],12*60*60*1000);
[](#cb72-147)147:     },
[](#cb72-148)148:     PING : () => {
[](#cb72-149)149:       this.alive=time();
[](#cb72-150)150:     },
[](#cb72-151)151:     CHECKPOINT : () => {
[](#cb72-152)152:       // Check child state
[](#cb72-153)153:       send(myParent(),'PING');
[](#cb72-154)154:       if ((time()-this.alive)>10000) {
[](#cb72-155)155:         log('Terminate. No parent!');
[](#cb72-156)156:         kill()
[](#cb72-157)157:       }
[](#cb72-158)158:     }
[](#cb72-159)159:   }
[](#cb72-160)160:   this.next='start';
[](#cb72-161)161: }
[](#cb72-162)162: jam.compileClass(foo,{verbose:1});
[](#cb72-163)163: var foody = jam.createAgent('foo',{},2);
[](#cb72-164)164: </script>
[](#cb72-165)165: </body>
[](#cb72-166)166: </html>
```

Example 13-8\. A Web page with embedded JAM and a "spy" agent that forwards user information to a relay JAM node.

In the following Ex. [13-9](#12_examples.xhtml_sejamex8) a data collector agent is presented. It implements an improved agent-pair that exchanges alive messages (ping and pong principle) with each other. The whole agent class consists of parent and child activities. If the child agent did not receive a ping message from its parent within a given time interval, it will terminate, assuming the parent terminated. The child agent periodically sends pong messages to his parent to signal that he is still alive (line 46 in activity *collectData*). If the parent agent did not receive a pong message from his child agent recently, it will create a new child agent. Based on internal parameter settings, JAM nodes decide how long an agent may exist (and run) on the node. After a time limit is reached, the agent will be terminated (garbage collected). The agent can negotiate a higher lifetime, but this is not necessary with the dynamic approach presented here. The delivery agent embedded in the Web page can apply this approach, too.

A timer is started that sends a notification signal to its agent (line 50 in activity *waitForData*). On each received notification signal, the parent agent will send a ping signal to its child agent (directly in the signal handler, line 81). If he did not received a ping message from his child agent, it will create a new one (lines 82-91).

```
[](#cb73-1) 1: // JAM shell script
[](#cb73-2) 2: // Data collector
[](#cb73-3) 3: // Connect to relay server on ag-0.de
[](#cb73-4) 4: port(DIR.IP('http://localhost:*'),{verbose:0})
[](#cb73-5) 5: connect(DIR.IP('http://ag-0.de:30002?secure=12:..'));
[](#cb73-6) 6: extend([1,2,3],'inspect',function (o) {
[](#cb73-7) 7:   return inspect(o,_,16)
[](#cb73-8) 8: },[1])
[](#cb73-9) 9: verbose(3)
[](#cb73-10)10: function collector () {
[](#cb73-11)11:   this.data = [];
[](#cb73-12)12:   this.collectTime = 1*60*60*1000;
[](#cb73-13)13:   this.alive = 0;
[](#cb73-14)14:   this.relay=null;
[](#cb73-15)15:   this.root=null;
[](#cb73-16)16:   this.child=null;
[](#cb73-17)17:   this.goto='';
[](#cb73-18)18:   this.act = {
[](#cb73-19)19:     start : () => {
[](#cb73-20)20:       log('Start')
[](#cb73-21)21:       this.root=myNode()
[](#cb73-22)22:     },
[](#cb73-23)23:     waitconnect : () => {
[](#cb73-24)24:       var nodes = link(DIR.IP('%'))
[](#cb73-25)25:       // first node must be the relay
[](#cb73-26)26:       if (nodes.length) {
[](#cb73-27)27:         this.relay=nodes[0];
[](#cb73-28)28:         this.alive=time();
[](#cb73-29)29:         log('Forking child agent..')
[](#cb73-30)30:         this.child=fork({goto:this.relay});
[](#cb73-31)31:       } else sleep(1000); 
[](#cb73-32)32:     },
[](#cb73-33)33:     goto : () => {
[](#cb73-34)34:       log('Go to '+this.relay);
[](#cb73-35)35:       moveto(DIR.NODE(this.relay));
[](#cb73-36)36:     },
[](#cb73-37)37:     arrived : () => {
[](#cb73-38)38:       // Arrived on destination
[](#cb73-39)39:       this.alive = time();
[](#cb73-40)40:     },
[](#cb73-41)41:     collectData : () => {
[](#cb73-42)42:       // Collecting new data
[](#cb73-43)43:       var data = inp.try(0,['WEBSPY',_],true);
[](#cb73-44)44:       if (data) send(myParent(),'DATA',data);
[](#cb73-45)45:       send(myParent(),'PING');
[](#cb73-46)46:       sleep(1000)
[](#cb73-47)47:     },
[](#cb73-48)48:     waitForData : () => {
[](#cb73-49)49:       timer.add(1000,'NOTIFY',0,true);
[](#cb73-50)50:       sleep(this.collectTime);
[](#cb73-51)51:     },
[](#cb73-52)52:     end : () => {
[](#cb73-53)53:       log('Terminate.')
[](#cb73-54)54:       kill()
[](#cb73-55)55:     }
[](#cb73-56)56:   }
[](#cb73-57)57:   this.trans = {
[](#cb73-58)58:     start : waitconnect,
[](#cb73-59)59:     waitconnect : () => {
[](#cb73-60)60:       if (this.goto) return goto;
[](#cb73-61)61:       return this.relay?waitForData:waitconnect
[](#cb73-62)62:     },
[](#cb73-63)63:     goto:arrived,
[](#cb73-64)64:     arrived : collectData,
[](#cb73-65)65:     collectData : () => {
[](#cb73-66)66:       return time()-this.alive < 10000?
[](#cb73-67)67:              collectData:end
[](#cb73-68)68:     },
[](#cb73-69)69:     waitForData : end
[](#cb73-70)70:   }
[](#cb73-71)71:   this.on = {
[](#cb73-72)72:     'DATA': (data,from) => {
[](#cb73-73)73:       iter(data,(rec) => { log(inspect(rec[1]))})
[](#cb73-74)74:       this.data.push(data)
[](#cb73-75)75:     },
[](#cb73-76)76:     'PING': () => {
[](#cb73-77)77:       this.alive=time();
[](#cb73-78)78:     },
[](#cb73-79)79:     'NOTIFY': () => {
[](#cb73-80)80:       send(this.child,'PING');
[](#cb73-81)81:       if ((time()-this.alive)>10000) {
[](#cb73-82)82:         var nodes = link(DIR.IP('%'));
[](#cb73-83)83:         this.relay=nodes[0];
[](#cb73-84)84:         if (this.relay) {
[](#cb73-85)85:           // Starting new child agent, 
[](#cb73-86)86:           // old not responding..')
[](#cb73-87)87:           this.child=fork({goto:this.relay,
[](#cb73-88)88:                            next:'goto'});
[](#cb73-89)89:         } else log('No connection to relay.');
[](#cb73-90)90:       }
[](#cb73-91)91:     }
[](#cb73-92)92:   }
[](#cb73-93)93:   this.next = 'start'
[](#cb73-94)94: }
[](#cb73-95)95: compile(collector,{verbose:true})
[](#cb73-96)96: var master = create('collector',{},1);
[](#cb73-97)97: start()
```

Example 13-9\. The data collector agent that is created by the JAM shell.

# References

| [ALV18] | O. Alvear, C. T. Calafate, J.-C. Cano, and P. Manzoni, *Crowdsensing in Smart Cities: Overview, Platforms, and Environment Sensing Issues*, Sensors, vol. 18, no. 460, 2018. |
| [BAD11] | C. Bădică, Z. Budimac, H.-D. Burkhard, and M. Ivanović, *Software Agents: Languages, Tools, Platforms*, Advances in Formal Languages, Modeling and Applications, vol. 8, no. 2, 2011. |
| [BAN15] | A. Banos, C. Lang, N. Marilleau, *Agent-based Spatial Simulation with NetLogo*, Volume 1 I. Elsevier Ltd, 2015. |
| [BAR14] | A. R. Bar and M. Maheswaran, *Confidentiality and Integrity in Crowdsourcing Systems*. Springer Cham Heidelberg NewYork Dordrecht London, 2014 |
| [BEL05] | Bellifemine, F., Bergenti, F., Caire, G., & Poggi, A. *JADE—a java agent development framework*, in Multi-agent programming (pp. 125-147), 2005 Springer, Boston, MA |
| [BOS13A] | S. Bosse, *Intelligent Microchip Networks: An Agent-on-Chip Synthesis Framework for the Design of Smart and Robust Sensor Networks*, Proceedings of the SPIE 2013, Microtechnologie Conference, Session EMT 102 VLSI Circuits and Systems, 24-26 April 2013, Alpexpo/Grenoble, France, SPIE, 2013, DOI:10.1117/12.2017224. |
| [BOS14A] | S. Bosse, *Distributed Agent-based Computing in Material-Embedded Sensor Network Systems with the Agent-on-Chip Architecture*, IEEE Sensors Journal, Special Issue MIS, 2014, DOI: 10.1109/JSEN.2014.2301938. |
| [BOS14B] | S. Bosse, Armin Lechleiter, *Structural Health and Load Monitoring with Material-embedded Sensor Networks and Self-organizing Multi-Agent Systems*, Procedia Technology, Proceeding of the SysInt 2014 Conference, 2-4 July 2014, Bremen, Germany, 2014, DOI:10.1016/j.protcy.2014.09.039. |
| [BOS15A] | S. Bosse, *Design and Simulation of Material-Integrated Distributed Sensor Processing with a Code-Based Agent Platform and Mobile Multi-Agent Systems*s, Sensors (MDPI), 15 (2), pp. 4513-4549, 2015, DOI:10.3390/s150204513 |
| [BOS15B] | S. Bosse, *A Unified Distributed Computing Framework with Mobile Multi- Agent Systems and Virtual Machines for Large-Scale Applications: From the Internet-of-Things to Sensor Clouds*, Annals of Computer Science and Information Systems Volume 6, Position Papers of the 2015 Federated Conference on Computer Science and Information Systems (FEDCSIS), Lodz, Poland, 13 - 16 Sep, 6, 2015, DOI:10.15439/2015F252. |
| [BOS16A] | S. Bosse, *Mobile Multi-Agent Systems for the Internet-of-Things and Clouds using the JavaScript Agent Machine Platform and Machine Learning as a Service*, The IEEE 4th International Conference on Future Internet of Things and Cloud , 22-24 August 2016, Vienna, Austria, 2016, 2016, DOI:10.1109/FiCloud.2016.43 |
| [BOS16B] | S. Bosse, A. Lechleiter, *A hybrid approach for Structural Monitoring with self-organizing multi-agent systems and inverse numerical methods in material-embedded sensor networks*, Mechatronics, (2016), DOI:10.1016/j.mechatronics.2015.08.005 |
| [BOS17A] | S. Bosse, *Incremental Distributed Learning with JavaScript Agents for Earthquake and Disaster Monitoring*, International Journal of Distributed Systems and Technologies (IJDST), (2017), IGI-Global, Vol. 8, Issue 4, DOI: 10.4018/IJDST.2017100103 |
| [BOS17B] | S. Bosse, E. Pournaras, *An Ubiquitous Multi-Agent Mobile Platform for Distributed Crowd Sensing and Social Mining*, FiCloud 2017: The 5th International Conference on Future Internet of Things and Cloud, Aug 21, 2017 - Aug 23, 2017, Prague, Czech Republic |
| [BOS17C] | S. Bosse, D. Lehmhus, *Towards Large-scale Material-integrated Computing: Self-Adaptive Materials and Agents*, IEEE 2nd International Workshops on Foundations and Applications of Self Systems (FASW), DOI: 10.1109/FAS-W.2017.123, 18-22 September 2017, University of Arizona, Tucson, AZ |
| [BOS18A] | S. Bosse, *Unified Distributed Sensor and Environmental Information Processing with Multi-Agent Systems: Models, Platforms, and Technological Aspects*, ISBN 9783746752228 (Hardcover), ISBN 9783746759470 (Softcover), epubli, 2018 |
| [BOS18B] | S. Bosse, *Smart Micro-scale Energy Management and Energy Distribution in Decentralized Self-Powered Networks Using Multi-Agent Systems*, FedCSIS Conference, 6th International Workshop on Smart Energy Networks & Multi-Agent Systems, 9-12.9.2018, Posznan, Poland, 2018 |
| [BOS18C] | S. Bosse, U. Engel, *Augmented Virtual Reality: Combining Crowd Sensing and Social Data Mining with Large-Scale Simulation Using Mobile Agents for Future Smart Cities*. Proceedings, Volume 4, ECSA-5 5th International Electronic Conference on Sensors and Applications 15–30 November, 2018 DOI 10.3390/ecsa-5-05762 |
| [BOS19A] | S. Bosse, D. Lehmhus, *Material-integrated cluster computing in self-adaptive robotic materials using mobile multi-agent systems*, Cluster Computing, doi 10.1007/s10586-018-02894-x, Volume 22, Number 3, pp. 1017-1037, 2019 ISSN 1386-7857 |
| [BOS19B] | S. Bosse, U. Engel, *Real-time Human-in-the-loop Simulation with Mobile Agents, Chat Bots, and Crowd Sensing for Smart Cities*, Sensors (MDPI), 2019, doi: 10.3390/s19204356 |
| [BOS19C] | S. Bosse, U. Engel, *Combining Crowd Sensing and Social Data Mining with Agent-based Simulation using Mobile Agents towards Augmented Virtuality*, Proc. of the Social Simulation Conference, 24-27.9.2019, Mainz, Germany |
| [BOS20A] | S. Bosse, *Self-organising Urban Traffic control on micro-level using Reinforcement Learning and Agent-based Modelling*, Proc. of the SAI IntelliSys Conference, 3-4.9.2020, Amsterdam, Netherlands, 2020 |
| [BOS21A] | S. Bosse, *Distributed Serverless Chat Bot Networks using mobile Agents: A Distributed Data Base Model for Social Networking and Data Analytics*, 13th International Conference on Agents and Artificial Intelligence (ICAART), Online, Worldwide, 4-6-2.2021 |
| [BOS21B] | S. Bosse, *Parallel and Distributed Agent-based Simulation of large-scale socio-technical Systems with loosely coupled Virtual Machines*, Proc. of the SIMULTECH Conference 2021, International Conference on Simulation and Modeling Methodologies, Technologies and Applications, 7-9.7.2021, Online |
| [BOS21C] | S. Bosse, Long-term Longitudinal data collection and analysis in highly dynamic systems using mobile Crowd Sensing and mobile Agents, 9th European Congress of Methodology EAM 2021, 21-23.7.2021, Valenica, Spain |
| [BRA13] | D. C. Brabham, *Crowdsourcing*. MIT Press, 2013 |
| [CAO12] | J. Cao and S. K. Das, Eds., *Mobile agents in networking and distributed computing*. John Wiley & Sons, 2012. |
| [DAM13] | K. H. van Dam, I. Lukszo, and N. Zofia, Eds., *Agent-Based Modelling of Socio-Technical Systems*, Springer Berlin, 2013. |
| [ENG22] | S. Bosse, L. Dahlhaus, U. Engel, *Web data mining: collecting textual data from web pages using R*, in: Handbook of computational social science ; Volume 2: Data science, statistical modelling, and machine learning methods, Editors U. Engel et al., 2022, Routledge ISBN 9781032111391 DOI |
| [GEL85] | D. Gelernter, *Generative communication in Linda*, ACM Transactions on Programming Languages and Systems (TOPLAS), vol. 7, no. 1, pp. 80-112, 1985. |
| [HAR05] | G. M. P. O’Hare, D. Marsh, A. Ruzzelli, and R. Tynan, *Agents forWireless Sensor Network Power Management*, in Parallel Processing, 2005\. ICPP 2005 Workshops. International Conference Workshops on, 2005. |
| [JAM22] | S. Bosse, *JavaScript Agent Machine (JAM)*, software repository, accessed 20.7.2022, https://github.com/bsLab/jam, |
| [JER22] | Jerryscript, https://jerryscript.net and https://github.com/jerryscript-project/jerryscript, on-line, accessed 20.7.2022 |
| [KAP15] | A. Karpathy, *Reinforcement Learning Agents in Javascript*, https://github.com/karpathy/reinforcejs, accessed 1.1.2022 |
| [LEB13] | J.-F. Lebraty and K. Lobre-Lebraty, *Crowdsourcing - One Step Beyond*. JohnWiley & Sons, Inc., 2013 |
| [MUE96] | Jörg P. Müller, *The Design of Intelligent Agents - A Layered Approach*, LNAI 1177\. Springer Berlin, 1996. |
| [MUL90] | S. J. Mullender and G. van Rossum, *Amoeba: A Distributed Operating System for the 1990s*, IEEE Computer, vol. 23, no. 5, pp. 44-53, 1990. |
| [NOD22] | Node\.js, https://nodejs.org, on-line, accessed 20.7.2022 |
| [QUI22] | F. Bellard, QuickJs, https://bellard.org/quickjs and https://github.com/bellard/quickjs, on-line, accessed 20.7.2022 |
| [STA09] | A. Avati, *CS229: Machine Learning, Simplified SMO Algorithm*, Stanford University, 2009, http://cs229.stanford.edu/materials/smo.pdf |
| [TRU22] | R. Tushov, https://github.com/turuslan/HackTimer, accessed 1.7.2022 |
| [UHR09] | A. M. Uhrmacher and D. Weyns, Eds., *Multi-agent systems: simulation and applications*, CRC Press, 2009. |
| [WEI84] | Weicker, R.P., *Dhrystone: a synthetic systems programming benchmark*. Communications of the ACM, 27(10), pp.1013-1030, 1984 |
| [WIL15] | U. Wilensky, W. Rand, *An Introduction to Agent-Based Modeling Modeling Natural, Social, and Engineered Complex Systems with NetLogo*. MIT Press, 2015 |

# Index