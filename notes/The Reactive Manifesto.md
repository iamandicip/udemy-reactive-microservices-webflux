# The Reactive Manifesto

> Organisations working in disparate domains are independently discovering patterns for building software that look the
> same. These systems are more robust, more resilient, more flexible and better positioned to meet modern demands.

Organisations working in disparate domains are independently discovering patterns for building software that look the
same. FThese systems are more robust, more resilient, more flexible and better positioned to meet modern demands.

These changes are happening because application requirements have changed dramatically in recent years. Only a few years
ago a large application had tens of servers, seconds of response time, hours of offline maintenance and gigabytes of
data. Today applications are deployed on everything from mobile devices to cloud-based clusters running thousands of
multi-core processors. Users expect millisecond response times and 100% uptime. Data is measured in Petabytes. Today's
demands are simply not met by yesterday’s software architectures.

We believe that a coherent approach to systems architecture is needed, and we believe that all necessary aspects are
already recognised individually: we want systems that are Responsive, Resilient, Elastic and Message Driven. We call
these Reactive Systems.

Systems built as Reactive Systems are more flexible, loosely-coupled
and [scalable](moz-extension://71991916-9a2b-4eac-a19f-60dc647f43f2/glossary#Scalability). This makes them easier to
develop and amenable to change. They are significantly more tolerant of failure and
when [failure](moz-extension://71991916-9a2b-4eac-a19f-60dc647f43f2/glossary#Failure) does occur they meet it with
elegance rather than disaster. Reactive Systems are highly responsive,
giving [users](moz-extension://71991916-9a2b-4eac-a19f-60dc647f43f2/glossary#User) effective interactive feedback.

### Reactive Systems are:

**Responsive:** The [system](moz-extension://71991916-9a2b-4eac-a19f-60dc647f43f2/glossary#System) responds in a timely
manner if at all possible. Responsiveness is the cornerstone of usability and utility, but more than that,
responsiveness means that problems may be detected quickly and dealt with effectively. Responsive systems focus on
providing rapid and consistent response times, establishing reliable upper bounds so they deliver a consistent quality
of service. This consistent behaviour in turn simplifies error handling, builds end user confidence, and encourages
further interaction.

**Resilient:** The system stays responsive in the face
of [failure](moz-extension://71991916-9a2b-4eac-a19f-60dc647f43f2/glossary#Failure). This applies not only to
highly-available, mission-critical systems — any system that is not resilient will be unresponsive after a failure.
Resilience is achieved by [replication](moz-extension://71991916-9a2b-4eac-a19f-60dc647f43f2/glossary#Replication),
containment, [isolation](moz-extension://71991916-9a2b-4eac-a19f-60dc647f43f2/glossary#Isolation)
and [delegation](moz-extension://71991916-9a2b-4eac-a19f-60dc647f43f2/glossary#Delegation). Failures are contained
within each [component](moz-extension://71991916-9a2b-4eac-a19f-60dc647f43f2/glossary#Component), isolating components
from each other and thereby ensuring that parts of the system can fail and recover without compromising the system as a
whole. Recovery of each component is delegated to another (external) component and high-availability is ensured by
replication where necessary. The client of a component is not burdened with handling its failures.

**Elastic:** The system stays responsive under varying workload. Reactive Systems can react to changes in the input rate
by increasing or decreasing the [resources](moz-extension://71991916-9a2b-4eac-a19f-60dc647f43f2/glossary#Resource)
allocated to service these inputs. This implies designs that have no contention points or central bottlenecks, resulting
in the ability to shard or replicate components and distribute inputs among them. Reactive Systems support predictive,
as well as Reactive, scaling algorithms by providing relevant live performance measures. They
achieve [elasticity](moz-extension://71991916-9a2b-4eac-a19f-60dc647f43f2/glossary#Elasticity) in a cost-effective way
on commodity hardware and software platforms.

**Message Driven:** Reactive Systems rely
on [asynchronous](moz-extension://71991916-9a2b-4eac-a19f-60dc647f43f2/glossary#Asynchronous) [message-passing](moz-extension://71991916-9a2b-4eac-a19f-60dc647f43f2/glossary#Message-Driven)
to establish a boundary between components that ensures loose coupling, isolation
and [location transparency](moz-extension://71991916-9a2b-4eac-a19f-60dc647f43f2/glossary#Location-Transparency). This
boundary also provides the means to
delegate [failures](moz-extension://71991916-9a2b-4eac-a19f-60dc647f43f2/glossary#Failure) as messages. Employing
explicit message-passing enables load management, elasticity, and flow control by shaping and monitoring the message
queues in the system and
applying [back-pressure](moz-extension://71991916-9a2b-4eac-a19f-60dc647f43f2/glossary#Back-Pressure) when necessary.
Location transparent messaging as a means of communication makes it possible for the management of failure to work with
the same constructs and semantics across a cluster or within a single
host. [Non-blocking](moz-extension://71991916-9a2b-4eac-a19f-60dc647f43f2/glossary#Non-Blocking) communication allows
recipients to only consume [resources](moz-extension://71991916-9a2b-4eac-a19f-60dc647f43f2/glossary#Resource) while
active, leading to less system overhead.

![](reactive-traits.svg)

Large systems are composed of smaller ones and therefore depend on the Reactive properties of their constituents. This
means that Reactive Systems apply design principles so these properties apply at all levels of scale, making them
composable. The largest systems in the world rely upon architectures based on these properties and serve the needs of
billions of people daily. It is time to apply these design principles consciously from the start instead of
rediscovering them each time.

[Source](https://www.reactivemanifesto.org/)