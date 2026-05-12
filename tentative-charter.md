# Tentative charter for INet4AI Research Group

**Internetworking Challenges for AI**

## Background

Generative AI systems are approaching a scalability limit in their development. Indeed, as mentioned in [1], the ever-growing size of large language model in terms of number of parameters to improve the quality of models' outcomes makes it infeasible to train such models in a single datacenter due to power density issues. To address such scalability issues, it becomes necessary to train those models beyond the realm of a single datacenter. 

Besides, as the adoption of services based on generative AI is ramping up, some distributed inference use cases associated with interactive applications ask for stringent quality of service levels in order to meet users demands. In particular, in conversational services, the latency to answer user request become an important factor to lower in order to keep the natural conversational flow of turn by turn chat interactions. Meeting those qualiy of service requirements can be addressed by using systems mixing powerful computing instances residing in cloud platforms with localized edge platforms, using heterogeneous and distributed systems.

At the same time, questions arise related to the governance and operational models of generative AI services, in particular due to data ownership and trustworthiness aspects. In the last few months, the bar to train or fine tune large language models has lowered: while a few months ago such operations were only accessible to large companies running dedicated infrastructure, the appearance of neocloud companies comoditizing access to shared GPU resources [2] or the development of training frameworks operating among heterogeneous clusters communicationg through the Internet raise new challenges regarding the operation of collective communications over heterogeneous, multi-stakeholder and widely distributed infrastructure. Some of those concerns can find a solution in federated learning systems, in which data ownership can be retained, and models are trained among several stakeholders. 

Those three observations have raised numerous questions in the IETF and IRTF communities to determine how the necessary distribution of generative AI systems beyond the realm of single datacenters in a multi-stakeholder, distributed infrastructure will impact the Internet at large. Besides, discussing the distribution of artificial intelligence training, fine tuning and inference at a global scale, potentially using a federated learning approach, is a key to address the concerning concentration of AI infrastructure and to move towards a more federated, decentralized and multi-stakeholder ecosystem.

## Main Objectives

This research group aim at discussing specific challenges associated with the operation of (generative) AI workloads over or alongside the Internet. In particular, it targets the following topics:
- Network resource management at regional scale
	- Suitable load balancing strategies
	- Adapting connection protocol to AI application distribution constraints 
	- Removing checkpointing needed at application level
	- Decentralized AI approach
	- Time-aware routing
- Latency sensitivity of generative AI traffic
	- Richer congestion signaling to tackle link heterogeneity issues
	- Enforcement of delay bounds at large scale
- Operating AI traffic over the Internet:
	- Revisit ALTO and CATS works under the lights of AI workload constraints 
	- Research on methods to adapt communication collectives to the network’s topology
- Security challenges of AI communications over the Internet
	- Low-latency and in-network computing-compatible security
	- Enablers for security mechanisms at application level
- In-network support (aggregation etc.)
- Optimizing agent communications over the Internet
	- (Trustworthy) translation between protocol realms for discovery, authentication and authorization
	- Exploring a departure from agent anthropomorphism to adopt agent-to-agent protocols accounting from their agentic nature

## Way of Working

As our objective is to foster discussions among people from the IETF / IRTF community who are interested in Internetworking Challenges for AI, we encourage research-oriented exchanges on the group's mailing list (net4ai@irtf.org). Besides, the research group plans to meet at least once per year at IETF meetings, and may hold additional meetings, either as standalone interim meetings, or co-located meetings at technical conferences and similar events. 

## References
1. A. Gherghescu *et al.*, *A Look Into Training Large Language Models on Next Generation Datacenters* https://arxiv.org/html/2407.12819v1
2. Mulani, Nikhil. "An Evolving AI Supply Chain." Available at SSRN 5628470 (2025).
