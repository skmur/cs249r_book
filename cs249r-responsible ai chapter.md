[[Responsible AI]{.underline}](#responsible-ai)

> [[Introduction]{.underline}](#introduction)
>
> [[Definition]{.underline}](#definition)
>
> [[Key Principles and
> Concepts]{.underline}](#key-principles-and-concepts)
>
> [[Transparency and
> Explainability]{.underline}](#transparency-and-explainability)
>
> [[Fairness, Bias, and
> Discrimination]{.underline}](#fairness-bias-and-discrimination)
>
> [[Privacy and Data
> Governance]{.underline}](#privacy-and-data-governance)
>
> [[Safety and Robustness]{.underline}](#safety-and-robustness)
>
> [[Accountability and
> Governance]{.underline}](#accountability-and-governance)
>
> [[Cloud ML vs. Edge ML vs.
> TinyML]{.underline}](#cloud-ml-vs.-edge-ml-vs.-tinyml)
>
> [[Summary]{.underline}](#summary)
>
> [[Explainability]{.underline}](#explainability)
>
> [[Fairness]{.underline}](#fairness)
>
> [[Safety]{.underline}](#safety)
>
> [[Accountability]{.underline}](#accountability)
>
> [[Governance]{.underline}](#governance)
>
> [[Privacy]{.underline}](#privacy)
>
> [[Technical Aspects]{.underline}](#technical-aspects)
>
> [[Detecting and Mitigating Bias \[Lead:
> Alex\]]{.underline}](#detecting-and-mitigating-bias-lead-alex)
>
> [[Preserving Privacy]{.underline}](#preserving-privacy)
>
> [[Machine Unlearning]{.underline}](#machine-unlearning)
>
> [[Adversarial Examples and
> Robustness]{.underline}](#adversarial-examples-and-robustness)
>
> [[Building Interpretable
> Models]{.underline}](#building-interpretable-models)
>
> [[Monitoring Model
> Performance]{.underline}](#monitoring-model-performance)
>
> [[Implementation Challenges]{.underline}](#implementation-challenges)
>
> [[Organizational and Cultural Structures\
> \[sonia\]]{.underline}](#organizational-and-cultural-structures-sonia)
>
> [[Obtaining Quality and Representative
> Data]{.underline}](#obtaining-quality-and-representative-data)
>
> [[Difficulty Balancing Accuracy and Other
> Objectives]{.underline}](#difficulty-balancing-accuracy-and-other-objectives)
>
> [[Increased Cost and Complexity of
> Models]{.underline}](#increased-cost-and-complexity-of-models)
>
> [[Lack of Standards and Best
> Practices]{.underline}](#lack-of-standards-and-best-practices)
>
> [[Ethical Considerations in AI Design
> \[sonia\]]{.underline}](#ethical-considerations-in-ai-design-sonia)
>
> [[AI Safety/value alignment]{.underline}](#ai-safetyvalue-alignment)
>
> [[Autonomous Systems and Control \[and
> Trust\]]{.underline}](#autonomous-systems-and-control-and-trust)
>
> [[Economic Impacts on Jobs, Skills,
> Wages]{.underline}](#economic-impacts-on-jobs-skills-wages)
>
> [[Scientific Communication and AI
> Literacy]{.underline}](#scientific-communication-and-ai-literacy)
>
> [[Case Studies]{.underline}](#case-studies)
>
> [[Conclusion]{.underline}](#conclusion)

# Responsible AI

As machine learning models grow across various domains, these algorithms
have the potential to perpetuate historical biases, breach privacy, or
enable unethical automated decisions if developed without thoughtful
consideration of their societal impacts. Even systems created with good
intentions can ultimately discriminate against certain demographic
groups, enable surveillance, or lack transparency into their behaviors
and decision-making processes. As such, machine learning engineers and
companies have an ethical responsibility to proactively ensure
principles of fairness, accountability, safety, and transparency are
reflected in their models to prevent harm and build public trust. This
involves adopting technical approaches such as testing for biases,
building interpretable models that can explain their reasoning, as well
as governance practices like establishing oversight boards and
conducting impact assessments. By exploring machine learning through an
ethical lens, the field can work toward developing systems that better
align with human values and societal priorities. This chapter provides
an overview of responsible and ethical methods and principles that are
crucial knowledge for machine learning, as algorithms exert greater
influence over various aspects of society. Adopting such considerations
into the machine learning development lifecycle will be vital for
reducing potential detriments from these increasingly ubiquitous
technologies.

**Learning objectives**

-   

## Introduction

Machine learning models are increasingly used to automate decisions in
high-stakes social domains like healthcare, criminal justice, and
employment. However, without deliberate care, these algorithms can
perpetuate biases, breach privacy, or cause other harm. For instance, a
loan approval model solely trained on data from high-income
neighborhoods could disadvantage applicants from lower-income areas.
This motivates the need for responsible machine learning - creating
fair, accountable, transparent, and ethical models.

Several core principles underlie responsible ML. Fairness ensures models
do not discriminate based on gender, race, age, and other attributes.
Explainability enables humans to interpret model behaviors and improve
transparency. Robustness and safety techniques prevent vulnerabilities
like adversarial examples. Rigorous testing and validation help reduce
unintended model weaknesses or side effects.

Implementing responsible ML presents both technical and ethical
challenges. Developers must grapple with defining fairness
mathematically, balancing competing objectives like accuracy vs
interpretability, and securing quality training data. Organizations must
also align incentives, policies, and culture to uphold ethical AI.

This chapter will equip readers to critically evaluate AI systems and
contribute to developing beneficial and ethical machine learning
applications by covering the foundations, methods, and real-world
implications of responsible ML. The responsible ML principles discussed
are crucial knowledge as algorithms mediate more aspects of human
society.

### Definition

Responsible AI is about developing AI that positively impacts society
under human ethics and values. There is no universally agreed-upon
definition of \"responsible AI,\" but here is a summary of how it is
commonly described. Responsible AI refers to designing, developing, and
deploying artificial intelligence systems in an ethical, socially
beneficial way. The core goal is to create trustworthy, unbiased, fair,
transparent, accountable, and safe AI.

While there is no canonical definition, responsible AI is generally
considered to encompass principles such as:

-   **Fairness:** Avoiding biases, discrimination, and potential harm to
    > certain groups or populations

-   **Explainability:** Enabling humans to understand and interpret how
    > AI models make decisions

-   **Transparency:** Openly communicating how AI systems operate, are
    > built, and are evaluated

-   **Accountability:** Having processes to determine responsibility and
    > liability for AI failures or negative impacts

-   **Robustness:** Ensuring AI systems are secure, reliable and behave
    > as intended

-   **Privacy:** Protecting sensitive user data and adhering to privacy
    > laws and ethics

Putting these principles into practice involves technical techniques,
corporate policies, governance frameworks, and moral philosophy. There
are also ongoing debates around defining ambiguous concepts like
fairness and determining how to balance competing objectives.

## Key Principles and Concepts

### Transparency and Explainability

Machine learning models are often criticized as mysterious \"black
boxes\" - opaque systems where it\'s unclear how they arrived at
particular predictions or decisions. For example, an AI system called
[[COMPAS]{.underline}](https://doc.wi.gov/Pages/AboutDOC/COMPAS.aspx)
used to assess criminal recidivism risk in the U.S. was found to be
racially biased against black defendants. Still, the opacity of the
algorithm made it difficult to understand and fix the problem. This lack
of transparency can obscure biases, errors, and deficiencies.

Explaining model behaviors helps engender trust from the public and
domain experts and enables identifying issues to address.
Interpretability techniques like LIME, Shapley values, and saliency maps
empower humans to understand and validate model logic. Laws like the
EU\'s GDPR also mandate transparency, which requires explainability for
certain automated decisions. Overall, transparency and explainability
are critical pillars of responsible AI.

### Fairness, Bias, and Discrimination 

ML models trained on historically biased data often perpetuate and
amplify those prejudices. Healthcare algorithms have been shown to
disadvantage black patients by underestimating their needs (@obermeyer2019dissecting). Facial
recognition needs to be more accurate for women and people of color.
Such algorithmic discrimination can negatively impact people\'s lives in
profound ways.

Different philosophical perspectives also exist on fairness - for
example, is it fairer to treat all individuals equally or try to achieve
equal outcomes for groups? Ensuring fairness requires proactively
detecting and mitigating biases in data and models. However, achieving
perfect fairness is tremendously difficult due to contrasting
mathematical definitions and ethical perspectives. Still, promoting
algorithmic fairness and non-discrimination is a key responsibility in
AI development.

### Privacy and Data Governance

Maintaining individuals\' privacy is an ethical obligation and legal
requirement for organizations deploying AI systems. Regulations like the
EU\'s GDPR mandate data privacy protections and rights like the ability
to access and delete one\'s data.

However, maximizing the utility and accuracy of data for training models
can conflict with preserving privacy - modeling disease progression
could benefit from access to patients\' full genomes but sharing such
data widely violates privacy.

Responsible data governance involves carefully anonymizing data,
controlling access with encryption, getting informed consent from data
subjects, and collecting the minimum data needed. Honoring privacy is
challenging but critical as AI capabilities and adoption expand.

### Safety and Robustness 

Putting AI systems into real-world operation requires ensuring they are
safe, reliable, and robust, especially for human interaction scenarios.
Self-driving cars from Uber and Tesla have been involved in deadly
crashes due to unsafe behaviors.

Adversarial attacks that subtly alter input data can also fool ML models
and cause dangerous failures if systems are not resistant. Deepfakes
represent another emerging threat area.

Promoting safety requires extensive testing, risk analysis, human
oversight, and designing systems that combine multiple weak models to
avoid single points of failure. Rigorous safety mechanisms are essential
for the responsible deployment of capable AI.

### Accountability and Governance

When AI systems eventually fail or produce harmful outcomes, there must
be mechanisms to address resultant issues, compensate affected parties,
and assign responsibility. Both corporate accountability policies and
government regulations are indispensable for responsible AI governance.
For instance, [[Illinois\' Artificial Intelligence Video Interview
Act]{.underline}](https://www.ilga.gov/legislation/ilcs/ilcs3.asp?ActID=4015&ChapterID=68)
requires companies to disclose and obtain consent for AI video analysis,
promoting accountability.

Without clear accountability, even harms caused unintentionally could go
unresolved, furthering public outrage and distrust. Oversight boards,
impact assessments, grievance redress processes, and independent audits
promote responsible development and deployment.

## Cloud ML vs. Edge ML vs. TinyML

While these principles broadly apply across AI systems, certain
responsible AI considerations are unique or pronounced when dealing with
machine learning on embedded devices versus traditional server-based
modeling. Therefore, we present a high-level taxonomy comparing
responsible AI considerations across cloud, edge, and tinyML systems.

### Summary

The table below summarizes how responsible AI principles manifest
differently across cloud, edge, and tinyML architectures and how core
considerations tie into their unique capabilities and limitations. Each
environment\'s constraints and tradeoffs shape how we approach
transparency, accountability, governance, and other pillars of
responsible AI.

\| Principle \| Cloud ML \| Edge ML \| TinyML \|

\|-\|-\|-\|-\|

\| Explainability \| Complex models supported \| Lightweight required \|
Severe limits \|

\| Fairness \| Broad data available \| On-device biases \| Limited data
labels \|

\| Privacy \| Cloud data vulnerabilities \| More sensitive data \| Data
dispersed \|

\| Safety \| Hacking threats \| Real-world interaction \| Autonomous
devices \|

\| Accountability \| Corporate policies \| Supply chain issues \|
Component tracing \|

\| Governance \| External oversight feasible \| Self-governance needed
\| Protocol constraints \|

### Explainability

For cloud-based machine learning, explainability techniques can leverage
significant compute resources, enabling complex methods like SHAP values
or sampling-based approaches to interpret model behaviors. For example,
[[Microsoft\'s
InterpretML]{.underline}](https://www.microsoft.com/en-us/research/uploads/prod/2020/05/InterpretML-Whitepaper.pdf)
toolkit provides explainability techniques tailored for cloud
environments.

However, edge ML operates on resource-constrained devices, requiring
more lightweight explainability methods that can run locally without
excessive latency. Techniques like LIME (@ribeiro2016should) approximate model explanations
using linear models or decision trees to avoid expensive computations,
which makes them ideal for resource-constrained devices. But LIME
requires training hundreds to even thousands of models to generate good
explanations, which is often infeasible given edge computing
constraints. In contrast, saliency-based methods are often much faster
in practice, only requiring a single forward pass through the network to
estimate feature importance. This greater efficiency makes such methods
better suited to edge devices with limited compute resources where
low-latency explanations are critical.

Embedded systems poses the most significant challenges for
explainability, given tiny hardware capabilities. More compact models
and limited data make inherent model transparency easier. Explaining
decisions may not be feasible on high-size- and power-optimized
microcontrollers. [[DARPA\'s Transparent
Computing]{.underline}](https://www.darpa.mil/program/transparent-computing)
program aims to develop extremely low overhead explainability,
especially for tinyML devices like sensors and wearables.

### Fairness

For cloud machine learning, vast datasets and computing power enable
detecting biases across large heterogeneous populations and mitigating
them through techniques like re-weighting data samples. However, biases
may emerge from the broad behavioral data used to train cloud models.
Amazon\'s Fairness Flow framework helps assess cloud ML fairness.

Edge ML relies on limited on-device data, making analyzing biases across
diverse groups harder. But edge devices interact closely with
individuals, providing an opportunity to adapt locally for fairness.
[[Google\'s Federated
Learning]{.underline}](https://blog.research.google/2017/04/federated-learning-collaborative.html)
distributes model training across devices to incorporate individual
differences.

TinyML poses unique challenges for fairness with highly dispersed
specialized hardware and minimal training data. Bias testing is
difficult across diverse devices. Collecting representative data from
many devices to mitigate bias has scale and privacy hurdles. [[DARPA\'s
Assured Neuro Symbolic Learning and Reasoning
(ANSR)]{.underline}](https://www.darpa.mil/news-events/2022-06-03)
efforts are geared toward developing fairness techniques given extreme
hardware constraints.

### Safety

For cloud ML, key safety risks include model hacking, data poisoning,
and malware disrupting cloud services. Robustness techniques like
adversarial training, anomaly detection, and diversified models aim to
harden cloud ML against attacks. Redundancy and redundancy can help
prevent single points of failure.

Edge ML and TinyML interact with the physical world, so reliability and
safety validation are critical. Rigorous testing platforms like
[[Foretellix]{.underline}](https://www.foretellix.com/) synthetically
generate edge scenarios to validate safety. TinyML safety is magnified
by autonomous devices with limited supervision. TinyML safety often
relies on collective coordination - swarms of drones maintain safety
through redundancy. Physical control barriers also constrain unsafe
tinyML device behaviors.

In summary, safety is crucial but manifests differently in each domain.
Cloud ML guards against hacking, edge ML interacts physically so
reliability is key, and tinyML leverages distributed coordination for
safety. Understanding the nuances guides appropriate safety techniques.

### Accountability

Cloud ML\'s accountability centers on corporate practices like
responsible AI committees, ethical charters, and processes to address
harmful incidents. Third-party audits and external government oversight
promote cloud ML accountability.

Edge ML accountability is more complex with distributed devices and
supply chain fragmentation. Companies are accountable for devices, but
components come from various vendors. Industry standards help coordinate
edge ML accountability across stakeholders.

With TinyML, accountability mechanisms must be traced across long,
complex supply chains of integrated circuits, sensors, and other
hardware. TinyML certification schemes help track component provenance.
Trade associations should ideally promote shared accountability for
ethical tinyML.

### Governance 

For cloud ML, organizations institute internal governance like ethics
boards, audits, and model risk management. But external governance also
oversees cloud ML, like regulations on bias and transparency such as the
[[AI Bill of
Rights]{.underline}](https://www.whitehouse.gov/ostp/ai-bill-of-rights/),
[[General Data Protection Regulation
(GDPR)]{.underline}](https://gdpr-info.eu/), and [[California Consumer
Protection Act (CCPA)]{.underline}](https://oag.ca.gov/privacy/ccpa).
Third-party auditing supports cloud ML governance.

Edge ML is more decentralized, requiring responsible self-governance by
developers and companies deploying models locally. Industry associations
coordinate governance across edge ML vendors. Open software helps align
incentives for ethical edge ML.

With tinyML, extreme decentralization and complexity make external
governance infeasible. TinyML relies on protocols and standards for
self-governance baked into model design and hardware. Cryptography
enables the provable trustworthiness of tinyML devices.

### Privacy

For cloud ML, vast amounts of user data are concentrated in the cloud,
creating risks of exposure through breaches. Differential privacy
techniques add noise to cloud data to preserve privacy. Strict access
controls and encryption protect cloud data at rest and in transit.

Edge ML moves data processing onto user devices, reducing aggregated
data collection but increasing potential sensitivity as personal data
resides on the device. Apple uses on-device ML and differential privacy
to train models while minimizing data sharing. Data anonymization and
secure enclaves protect on-device data.

TinyML distributes data across many resource-constrained devices, making
centralized breaches unlikely and challenging for scale anonymization.
Data minimization and using edge devices as intermediaries help tinyML
privacy.

So, while cloud ML must protect expansive centralized data, edge ML
secures sensitive on-device data, and tinyML aims for minimal
distributed data sharing due to constraints. While privacy is vital
throughout, techniques must match the environment. Understanding nuances
allows for selecting appropriate privacy preservation approaches.

## Technical Aspects

### Detecting and Mitigating Bias \[Lead: Alex\]

There has been a large body of work demonstrating that machine learning
models can exhibit bias, from underperforming for people of a certain
identity to making decisions that limit groups\' access to important
resources (@buolamwini2018genderShades).

Ensuring fair and equitable treatment for all groups affected by machine
learning systems is crucial as these models increasingly impact people's
lives in areas like lending, healthcare, and criminal justice. We
typically evaluate model fairness by considering "subgroup
attributes"---attributes unrelated to the prediction task that capture
identities like race, gender, or religion.

For example, in a loan default prediction model, subgroups could include
race, gender, or religion. When models are trained naively to maximize
accuracy, they often ignore subgroup performance. However, this can
negatively impact marginalized communities.

To illustrate, imagine a model predicting loan repayment where the
plusses (+'s) represent repayment and the circles (O's) represent
default in the figure below. The optimal accuracy would be correctly
classifying all of Group A while misclassifying some of Group B's
creditworthy applicants as defaults. If positive classifications allow
access loans, Group A would receive many more loans---which would
naturally result in a biased outcome.

![](vertopal_8b55cd460b0a41b2b53e2bf707e13be8/media/image3.png){width="4.314260717410324in"
height="1.9635422134733158in"}

Alternatively, correcting the biases against Group B would likely
increase "false positives" and reduce accuracy for Group A. Or, we could
train separate models focused on maximizing true positives for each
group. But this would require explicitly using sensitive attributes like
race in the decision process.

As we see, there are inherent tensions around priorities like accuracy
versus subgroup fairness, and whether to explicitly account for
protected classes. Reasonable people can disagree on the appropriate
tradeoffs. And constraints around costs and implementation options
further complicate matters. Overall, ensuring the fair and ethical use
of machine learning involves navigating these complex challenges.

Thus, fairness literature has proposed three main *fairness metrics* for
quantifying how fair a model performs over a dataset (@hardt2016equality). Given a model h, a
dataset D consisting of (x,y,s) samples, where x is the data features, y
is the label, and s is the subgroup attribute, where we assume there are
simply two subgroups a and b, we can define the following.

1.  **Demographic Parity** asks how accurate a model is for each
    > subgroup. In other words,\
    > P(h(X) = Y \| S = a) = P(h(X) = Y \| S = b)

2.  **Equalized Odds** asks how precise a model is on positive and
    > negative samples for each subgroup.\
    > P(h(X) = y \| S = a, Y = y) = P(h(X) = y \| S = b, Y = y)

3.  **Equality of Opportunity** is a special case of equalized odds that
    > asks how precise a model is on positive samples only. This is
    > relevant in cases such as resource allocation where we care about
    > how positive (ie resource allocated) labels are distributed across
    > groups. For example, we care that an equal proportion of loans are
    > given to both men and women.\
    > P(h(X) = 1 \| S = a, Y = 1) = P(h(X) = 1 \| S = b, Y = 1)

Note: these definitions often take a narrow view of considering binary
comparisons between two subgroups. Another thread of fair machine
learning research focusing on *multicalibration* and *multiaccuracy*
considers the interactions between an arbitrary number of identities,
acknowledging the inherent intersectionality of individual identities in
the real world (@hebert2018multicalibration).

Before making any technical decisions in developing an unbiased ML
algorithm we need to understand the context surrounding our model. Who
will this model make decisions for? Who is represented in the training
data? Who is represented and who is missing at the table of engineers,
designers, and managers? What sort of long-lasting impacts could this
model have? For example, will it impact the financial security of an
individual at a generational scale such as determining college
admissions or admitting a loan for a house? What historical and
systematic biases are present in this setting, and are they present in
the training data the model will generalize from? Understanding the
social, ethical and historical background of a system is critical to
prevent harm and should inform decisions throughout the model
development lifecycle.

After understanding the context, there are a wide array of technical
decisions one can make to remove bias. First, one must decide what
fairness metric is the most appropriate criterion to optimize for. Next,
there are generally three main areas where one can intervene to debias
an ML system. First, *preprocessing* is when one balances a dataset to
ensure fair representation, or even increases the weight on certain
underrepresented groups to ensure the model performs well on them.
Second, *in processing* attempts to modify the training process of an ML
system to ensure it prioritizes fairness. This can be as simple as
adding a fairness regularizer (@lowy2021fermi), to training an ensemble of models and
sampling from them in a specific manner (@agarwal2018reductions). Finally, *post processing*
debiases a model after the fact, taking a trained model and modifying
its predictions in a specific manner to ensure fairness is preserved (@alghamdi2022beyond, @hardt2016equality).

The breadth of existing fairness definitions and debiasing interventions
underscores the need for thoughtful assessment before deploying ML
systems. As ML researchers and developers, responsible model development
requires proactively educating ourselves on the real-world context,
consulting domain experts and end-users, and centering harm prevention.
Rather than seeing fairness considerations as a box to check, we must
deeply engage with the unique social implications and ethical trade offs
around each model we build. Every technical choice about datasets, model
architectures, evaluation metrics and deployment constraints embeds
values. By broadening our perspective beyond narrow technical metrics,
carefully evaluating tradeoffs, and listening to impacted voices, we can
work to ensure our systems expand opportunity rather than encode bias.
The path forward lies not in an arbitrary debiasing checklist but in a
commitment to understanding and upholding our ethical responsibility at
each step.

### Preserving Privacy

Recent incidents have demonstrated how AI models can memorize sensitive
user data in ways that violate privacy. For example, as shown below in
Figure XXX, Stable Diffusion's art generations were found to mimic
identifiable artists' styles and replicate existing photos, concerning
many closely (@carlini2023extracting). These risks are amplified with personalized ML
systems deployed in intimate environments like homes or wearables.
Imagine if a smart speaker uses our conversations to improve the quality
of service to end users who genuinely want it. Still, others could
violate privacy by trying to extract what the speaker "remembers."

![](vertopal_8b55cd460b0a41b2b53e2bf707e13be8/media/image5.png){width="6.5in"
height="3.5951629483814522in"}

*Figure XXX: Diffusion models memorize individual training examples and
generate them at test time.*

Adversaries can train models to detect if specific training data
influenced a target model. For example, Membership Inference Attacks
train a secondary model which learns to detect a change in the target
model's outputs when making inference over data it was trained on versus
not trained on (@shokri2017membership,). TinyML devices are especially vulnerable because they
are often personalized on user data and are deployed in even more
intimate settings such as the home.

To combat these issues, private machine learning, as mentioned in
[Chapter 15: Security and Privacy](https://harvard-edge.github.io/cs249r_book/privacy_security.html), has evolved to establish safeguards
against adversaries. Techniques like differential privacy add
mathematical noise during training to obscure individual data points'
influence on the model. Popular methods like DP-SGD (@abadi2016deep) also clip
gradients to limit what the model leaks about the data. Still, some
argue users should also be able to delete the impact of their data after
the fact.

### Machine Unlearning

With ML devices personalized to individual users and then deployed to
remote edges without connectivity, a challenge arises---how can models
responsively "forget" data points after deployment? If a user requests
their personal data be removed from a personalized model, the lack of
connectivity makes retraining infeasible. Thus, efficient on-device data
forgetting is necessary but poses hurdles.

Initial unlearning approaches faced limitations in this context.
Retraining models from scratch on the device to forget data points
proves inefficient or even impossible, given the resource constraints.
Fully retraining also requires retaining all the original training data
on the device, which brings its own security and privacy risks. Common
machine unlearning techniques \[?\] for remote embedded ML systems fail
to enable responsive, secure data removal.

However, newer methods show promise in modifying models to approximately
forget data \[?\] without full retraining. While the accuracy loss from
avoiding full rebuilds is modest, guaranteeing data privacy should still
be the priority when handling sensitive user information ethically. Even
slight exposure to private data can violate user trust. As ML systems
become deeply personalized, efficiency and privacy must be enabled from
the start---not afterthoughts.

Recent policy discussions which include the [[European Union's General
Data]{.underline}](https://gdpr-info.eu)

[[Protection Regulation (GDPR)]{.underline}](https://gdpr-info.eu), the
[[California Consumer Privacy Act
(CCPA)]{.underline}](https://oag.ca.gov/privacy/ccpa),

the [[Act on the Protection of Personal Information
(APPI)]{.underline}](https://www.dataguidance.com/notes/japan-data-protection-overview),
and Canada's proposed

[[Consumer Privacy Protection Act
(CPPA)]{.underline}](https://blog.didomi.io/en-us/canada-data-privacy-law),
require the deletion of private information. These policies coupled with
AI incidents like Stable Diffusion memorizing artist data have
underscored the ethical need for users to delete their data from models
after training.

The right to remove data arises from privacy concerns around
corporations or adversaries misusing sensitive user information. Machine
unlearning refers to removing the influence of specific points from an
already-trained model. Naively this involves full retraining without the
deleted data. However, for ML systems personalized and deployed to
remote edges, connectivity constraints often make retraining infeasible.
If a smart speaker learns from private home conversations, retaining
access to delete that data is important.

Although limited, methods are evolving to enable efficient
approximations to retraining for unlearning. By modifying models
inference-time, they can mimic \"forgetting\" data without full access
to training data. However, most current techniques are restricted to
simple models, still have resource costs, and trading some accuracy.
Though methods are evolving, enabling efficient data removal and
respecting user privacy remains an imperative for responsible TinyML
deployment.

~~Recently, voices in policy, as well as academics, have pointed out
that users should have the right to remove their data from a model.
Recent examples of Stable Diffusion memorizing real images and art
styles have highlighted additional security vulnerabilities in~~
~~models. Furthermore, users may feel uncomfortable with a corporation
having access to their private data. In the sphere of TinyML,
personalized edge devices may retain behavior based on previous user
patterns that a consumer wants removed. Because of this, the field of
*machine unlearning* has evolved, seeking to provide methods to make
models "forget" user~~ ~~information. Naively, unlearning can be
achieved by retraining a model without the data a user requested to
forget. However, in many settings, it is infeasible to retrain with
every new user request, such as large language models, as well as
deployed edge devices. If an edge device is deployed without access to
the internet or its training data, it is important that there are
inference-time techniques to modify a model behavior to act as if it
hadn't seen a piece of data. Although limited, there are a few methods
which seek to achieve efficient approximations to retraining, although
to achieve theoretical guarantees, they are generally limited to convex
models and require large storage requirements of inverted Hessian~~
~~matrices. However, these methods shed promising light on efficient
methods to ensure the responsible development of tiny machine learning
models with mechanisms to delete user data and protect user privacy even
after deployment.~~

### Adversarial Examples and Robustness 

Machine learning models, especially deep neural networks, have a
well-documented Achilles heel: they often break when even tiny
perturbations are made to their inputs
(https://arxiv.org/abs/1312.6199). This surprising fragility highlights
a major robustness gap that threatens real-world deployment in
high-stakes domains. It also opens the door for adversarial attacks
designed to deliberately fool models.

Machine learning models can exhibit a surprising brittleness - minor
input tweaks can cause shocking malfunctions, even in state-of-the-art
deep neural networks (https://arxiv.org/abs/1312.6199). This
unpredictability around out-of-sample data underscores gaps in model
generalization and robustness. Given the growing ubiquity of ML, it also
enables adversarial threats that weaponize models' blindspots.

Deep neural networks demonstrate an almost paradoxical dual nature -
human-like proficiency in training distributions coupled with extreme
fragility to tiny input perturbations (https://arxiv.org/abs/1312.6199).
This adversarial vulnerability gap highlights gaps in standard ML
procedures and threats to real-world reliability. At the same time, it
can be exploited: attackers can find model-breaking points humans
wouldn\'t perceive.

![](vertopal_8b55cd460b0a41b2b53e2bf707e13be8/media/image2.png){width="4.28125in"
height="1.28125in"}

\[image source:
[[https://www.microsoft.com/en-us/research/blog/adversarial-robustness-as-a-prior-for-better-transfer-learning/]{.underline}](https://www.microsoft.com/en-us/research/blog/adversarial-robustness-as-a-prior-for-better-transfer-learning/)\]

This fragility has real-world impacts: lack of robustness undermines
trust in deploying models for high-stakes applications like self-driving
cars or medical diagnosis. Moreover, the vulnerability leads to security
threats: attackers can deliberately craft adversarial examples that are
perceptually indistinguishable from normal data but cause model
failures.

For instance, past work shows successful attacks that trick models for
tasks like NSFW detection
\[https://openaccess.thecvf.com/content_ECCV_2018/papers/Arjun_Nitin_Bhagoji_Practical_Black-box_Attacks_ECCV_2018_paper.pdf\],
malware classification \[https://ieeexplore.ieee.org/document/6638293\],
ad-blocking \[https://arxiv.org/abs/1811.03194\], and speech recognition
\[https://www.usenix.org/system/files/conference/usenixsecurity16/sec16_paper_carlini.pdf\].
While errors in these domains already pose security risks, the problem
extends beyond IT security: recently adversarial robustness has been
proposed as an additional performance metric by approximating worst-case
behavior.

The surprising model fragility highlighted above casts doubt on
real-world reliability and opens the door to adversarial manipulation.
This growing vulnerability underscores several needs. First, principled
robustness evaluations are essential for quantifying model
vulnerabilities before deployment. Approximating worst-case behavior
surfaces blindspots. Second, effective defenses across domains must be
developed to close these robustness gaps. With security on the line,
developers cannot ignore the threat of attacks exploiting model
weaknesses. Moreover, for safety-critical applications like self-driving
vehicles and medical diagnosis, we cannot afford any fragility-induced
failures. Lives are at stake. Finally, the research community continues
mobilizing rapidly in response. Interest in adversarial machine learning
has exploded as attacks reveal the need to bridge the robustness gap
between synthetic and real-world data. Conferences now commonly feature
defenses for securing and stabilizing models.

In recent years, research interest has rapidly grown around improving
model robustness to perturbations and new threat types. However, most
solutions still incur significant accuracy or performance costs. Three
main approaches have emerged:

**Gradient masking** defenses aim to construct models with obscured or
misleading gradients that cannot be exploited to optimize adversarial
examples. For instance, some techniques train models to have locally
smooth loss landscapes around training data. This makes it
mathematically difficult for attack algorithms to identify input
perturbations that lead to misclassifications.

However, gradient masking has significant downsides: it can severely
damage model representational capacity and trainability on clean data.
Adversarially trained models require readable gradients to learn robust
features. In effect, while gradient masking has shown limited success in
deterring attacks, the accuracy and convergence tradeoffs often outweigh
the defensive benefits. More work is still needed to reconcile
obfuscation with robust optimization
\[[[https://arxiv.org/pdf/1412.5068.pdf]{.underline}](https://arxiv.org/pdf/1412.5068.pdf),
[[https://dl.acm.org/doi/abs/10.1145/3052973.3053009]{.underline}](https://dl.acm.org/doi/abs/10.1145/3052973.3053009),
[[https://ojs.aaai.org/index.php/AAAI/article/view/11504]{.underline}](https://ojs.aaai.org/index.php/AAAI/article/view/11504),
[[https://proceedings.mlr.press/v80/athalye18a.html]{.underline}](https://proceedings.mlr.press/v80/athalye18a.html)\].

**Robust optimization defenses** augment standard training to promote
model stability in neighborhoods around training data. Popular
techniques include injecting adversarial examples into the loss \[?\],
adding regularization terms to enforce smoothness constraints \[?\], or
modifying architecture to add uncertainty \[?\]. The goal is to ensure
high confidence in correct predictions within a small epsilon ball
around inputs
\[[[https://proceedings.mlr.press/v80/wong18a/wong18a.pdf]{.underline}](https://proceedings.mlr.press/v80/wong18a/wong18a.pdf),
[[https://arxiv.org/abs/1706.06083]{.underline}](https://arxiv.org/abs/1706.06083)\].
Effectively, this trains models to resist common perturbation tactics.

However, robust optimization has significant costs: generating
adversarial training data is computationally expensive, converging these
models is much slower, and accuracy on clean test data often decreases
\[[[https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9926085]{.underline}](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9926085)\].
Moreover, as attacks grow more advanced, maintaining robustness to new
threat models requires continuous augmentation with adversarial data.
This ongoing arms race presents scaling challenges. So, while
adversarial training improves resilience it has efficiency and precision
tradeoffs. As research continues, reconciling these tensions remains an
open challenge.

While promising start, prevailing methods present clear tradeoffs
between computational overhead, clean accuracy, and reliable defense
across threat models. Tensions persist around efficiency, precision, and
generalizability. As research momentum continues building, resolving
these robustness barriers remains imperative for securing
mission-critical systems.

**Adversarial example detection** offers a complementary approach -
instead of robustifying models; it tries to spot perturbed inputs and
abstain from prediction. Typically, this involves training secondary
classifier networks to identify statistical anomalies in embeddings or
pixel space. Well-crafted perturbations often introduce detectable
artifacts that deviation from natural image properties
\[[[https://dl.acm.org/doi/abs/10.1145/3128572.3140444]{.underline}](https://dl.acm.org/doi/abs/10.1145/3128572.3140444)\].
However, adversarial detection has downsides as well: building these
sub-networks imposes additional inference costs, and attackers can still
find adversarial inputs that evade detection. The approach also
sidesteps improving model robustness itself.

Despite growing research, adversarial robustness remains an open
challenge due to inherent tensions. Gains in resilience often impose
accuracy losses, inefficient training processes, or generalization gaps
against evolving threats. These issues become more acute for large
language models. Sophisticated linguistic attacks exploit blindspots,
and adversarial training scales poorly. Worryingly, poisoning techniques
can embed backdoors during development.

However, for ML systems deployed at the edge and in embedded systems in
particular, adversarial robustness merits priority despite its costs.
Edge devices deployed widely in uncontrolled, real-world environments
demand resilience against distribution shifts. Users inevitably stress
test systems in ways developers didn\'t anticipate. While approximating
all possible use cases with adversarial examples may be infeasible,
controlled robustness evaluations can surface hidden fragility. This
enables patching weaknesses through augmented data and constraints.

---

~~In recent years, there has been significant growth in research that
aims to address this by ensuring that models are robust to a variety of
perturbations and threat models. However, research in this area is still
nascent, and most solutions incur significant model accuracy and
performance tradeoffs. The most commonly studied and adopted methods
include gradient masking/obfuscation, robust optimization/adversarial
training, and adversarial example detection.~~

-   ~~**Gradient masking methods** aim to alter or construct models such
    > that their gradients are not useful for attackers and cannot be
    > used to optimize for adversarial examples. Often, gradient
    > masked/obfuscated models have loss functions that are locally
    > smooth around the input data, making it difficult for adversarial
    > algorithms to find directions to exploit for the generation of
    > adversarial examples.
    > \[[[https://arxiv.org/pdf/1412.5068.pdf]{.underline}](https://arxiv.org/pdf/1412.5068.pdf),
    > [[https://dl.acm.org/doi/abs/10.1145/3052973.3053009]{.underline}](https://dl.acm.org/doi/abs/10.1145/3052973.3053009),
    > [[https://ojs.aaai.org/index.php/AAAI/article/view/11504]{.underline}](https://ojs.aaai.org/index.php/AAAI/article/view/11504),
    > [[https://proceedings.mlr.press/v80/athalye18a.html]{.underline}](https://proceedings.mlr.press/v80/athalye18a.html)\]~~

-   ~~**Robust optimization methods** generally propose new optimization
    > functions that have additional regularization terms, certification
    > bounds, adversarial examples in the objective function, or modify
    > the model to add uncertainty in the model layers such that the
    > model is robust to an epsilon-ball of samples around each input
    > point
    > \[[[https://proceedings.mlr.press/v80/wong18a/wong18a.pdf]{.underline}](https://proceedings.mlr.press/v80/wong18a/wong18a.pdf),
    > [[https://arxiv.org/abs/1706.06083]{.underline}](https://arxiv.org/abs/1706.06083)\].
    > This also makes it difficult for attackers to find adversarial
    > examples near input samples, and models ideally become robust to
    > most perturbations that are small enough that they are not
    > visible. These methods often require that the developer consider
    > and simulate the adversarial examples that different attackers and
    > threat models can generate via iterative projected gradient
    > descent and then update their models to be robust to those
    > examples. Note that this process is unfortunately much slower than
    > simply training models with ERM loss
    > \[[[https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9926085]{.underline}](https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=9926085)\]
    > and frequently results in a decrease in predictive performance as
    > well.~~

-   ~~**Adversarial example detection** **methods** take an alternative
    > approach and attempt to identify adversarial examples before model
    > prediction, rather than trying to make models robust to them. This
    > is generally done by finding statistical outliers or training
    > separate sub-networks that can distinguish between perturbed and
    > normal images.
    > \[[[https://dl.acm.org/doi/abs/10.1145/3128572.3140444]{.underline}](https://dl.acm.org/doi/abs/10.1145/3128572.3140444)\].~~

~~As mentioned earlier, this field is still developing and current
proposed solutions often have significant limitations. As such, open
problems in adversarial robustness include the direct tradeoff between
robustness and accuracy, the high training time and cost for adversarial
optimization methods, and the constantly evolving nature of adversaries
and threat models. These problems are often exacerbated in the case of
large language models, as adversaries can construct adversarial hard
prompts, soft prompts, and instructions, and can also poison data
\[[[https://arxiv.org/abs/2307.14692]{.underline}](https://arxiv.org/abs/2307.14692),
[[https://arxiv.org/pdf/2302.10149]{.underline}](https://arxiv.org/pdf/2302.10149.pdf)\],
and adversarial training can be prohibitively costly given the size of
these models.~~

~~Robustness is particularly relevant in many TinyML applications
because edge devices are deployed in such large scales in highly
variable real-world settings. Oftentimes, people may be using their
devices and models in settings completely different from how they were
developed, and as such the developers of TinyML systems need to ensure
that their systems are robust to these unforeseen changes. While
adversarial robustness is likely a much harder task than this real world
robustness, optimizing for the worst-case scenario is a straightforward
method to address the problem. However, it is important to note that the
downsides of adversarial robustness, mainly the computational overhead,
are particularly relevant in TinyML applications, which are already
resource constrained.~~

### Building Interpretable Models

As models are deployed more frequently in high-stakes settings,
practitioners, developers, and downstream end-users, as well as
increasing regulation, have highlighted the need for explainability in
machine learning. The goal of many interpretability and explainability
methods are to provide practitioners with more information about either
the overall behavior of models or the behavior given a specific input,
such that users can decide whether or not the output or prediction of a
model is *trustworthy.* Such analysis can help developers debug models
and improve performance by pointing out biases, spurious correlations,
and failure modes of models. In cases where models are able to surpass
human performance on a task, interpretability can help users and
researchers to better understand relationships in their data and
patterns that may previously have been unknown. There are many classes
of methods in explainability/interpretability, including: post hoc
explainability, inherent interpretability, and mechanistic
interpretability.

**Post hoc explainability methods** typically explain the output
behavior of a black-box model on a specific input. Popular methods
include counterfactual explanations, feature attribution methods, and
concept-based explanations. **Counterfactual explanations**, also
frequently referred to as algorithmic recourse, take the form of "If X
had not occurred, Y would not have occurred"
\[[[https://arxiv.org/pdf/1711.00399.pdf]{.underline}](https://arxiv.org/pdf/1711.00399.pdf)\].
If we consider a person applying for a bank loan and a model rejecting
their application, they may ask their bank for recourse, or how they
need to change to be eligible for a loan. A counterfactual explanation
would tell them which features they need to change and by how much such
that the model's prediction changes. **Feature attribution methods** aim
to highlight the input features important/necessary for prediction. For
a computer vision model, this would mean highlighting the individual
pixels that contributed most to the predicted label of the image. Note
that these methods do not explain *how* those pixels/features impact the
prediction, only that they do. Common methods include input gradients,
GradCAM
\[[[https://arxiv.org/abs/1610.02391]{.underline}](https://arxiv.org/abs/1610.02391)\],
SmoothGrad
\[[[https://arxiv.org/abs/1706.03825]{.underline}](https://arxiv.org/abs/1706.03825)\],
LIME
\[[[https://arxiv.org/abs/1602.04938]{.underline}](https://arxiv.org/abs/1602.04938)\],
and SHAP
\[[[https://papers.nips.cc/paper_files/paper/2017/file/8a20a8621978632d76c43dfd28b67767-Paper.pdf]{.underline}](https://papers.nips.cc/paper_files/paper/2017/file/8a20a8621978632d76c43dfd28b67767-Paper.pdf)\].
**Concept based explanations** aim to explain model behavior and outputs
using a pre-defined set of semantic concepts (e.g., the model recognizes
scene class \`\`bedroom\'\' based on the presence of concepts
\`\`bed\'\' and \`\`pillow\'\'), with recent work showing that users
often prefer these explanations to attribution and example based
explanations because they "resemble human reasoning and explanations"
\[[[https://arxiv.org/abs/2303.15632]{.underline}](https://arxiv.org/abs/2303.15632),
[[https://dl.acm.org/doi/abs/10.1145/3544548.3581001]{.underline}](https://dl.acm.org/doi/abs/10.1145/3544548.3581001)\].
Popular concept based explanation methods include TCAV
\[[[https://proceedings.mlr.press/v80/kim18d.html]{.underline}](https://proceedings.mlr.press/v80/kim18d.html)\],
Network Dissection
\[[[https://openaccess.thecvf.com/content_cvpr_2017/html/Bau_Network_Dissection_Quantifying_CVPR_2017_paper.html]{.underline}](https://openaccess.thecvf.com/content_cvpr_2017/html/Bau_Network_Dissection_Quantifying_CVPR_2017_paper.html)\],
and interpretable basis decomposition
\[[[https://openaccess.thecvf.com/content_ECCV_2018/html/Antonio_Torralba_Interpretable_Basis_Decomposition_ECCV_2018_paper.html]{.underline}](https://openaccess.thecvf.com/content_ECCV_2018/html/Antonio_Torralba_Interpretable_Basis_Decomposition_ECCV_2018_paper.html)\].
Note that these methods are extremely sensitive to the size and quality
of the concept set, and that there exists a tradeoff between the
accuracy and faithfulness of these methods and their interpretability or
understandability to humans
\[[[https://arxiv.org/pdf/2207.09615.pdf]{.underline}](https://arxiv.org/pdf/2207.09615.pdf)\].

I**nherently interpretable models** are constructed such that their
explanations are part of the model architecture and are thus naturally
faithful, which sometimes makes them preferable to post-hoc explanations
applied to black-box models, especially in high-stakes domains where
transparency is imperative
\[[[https://arxiv.org/pdf/1811.10154]{.underline}](https://arxiv.org/pdf/1811.10154.pdf)\].
Often, these models are constrained so that the relationships between
input features and predictions are easy for humans to follow (linear
models, decision trees, decision sets, k-NN models), or they obey
structural knowledge of the domain, such as monotonicity
\[[[https://www.jmlr.org/papers/volume17/15-243/15-243.pdf]{.underline}](https://www.jmlr.org/papers/volume17/15-243/15-243.pdf)\],
causality, or additivity
\[[[https://www.jstor.org/stable/2991772]{.underline}](https://www.jstor.org/stable/2991772),
[[https://dl.acm.org/doi/abs/10.1145/2487575.2487579]{.underline}](https://dl.acm.org/doi/abs/10.1145/2487575.2487579)\].
More recent works have relaxed the restrictions on inherently
interpretable models, using black-box models for feature extraction and
using a simpler inherently interpretable model for classification,
allowing for faithful explanations that relate high-level features to
prediction. Examples of this include Concept Bottleneck Models
\[[[https://arxiv.org/pdf/2007.04612]{.underline}](https://arxiv.org/pdf/2007.04612.pdf)\],
which predict a concept set c that is passed into a linear classifier,
and ProtoPNets
\[[[https://arxiv.org/abs/1806.10574]{.underline}](https://arxiv.org/abs/1806.10574)\],
which dissect inputs into linear combinations of similarities to
prototypical parts from the training set.

**Mechanistic interpretability** methods seek to reverse engineer neural
networks, often analogized to how one might reverse engineer a compiled
binary or how neuroscientists attempt to decode the function of
individual neurons and circuits in brains. Most research in mechanistic
interpretability views models as a computational graph
\[[[https://proceedings.neurips.cc/paper_files/paper/2021/file/4f5c422f4d49a5a807eda27434231040-Paper.pdf]{.underline}](https://proceedings.neurips.cc/paper_files/paper/2021/file/4f5c422f4d49a5a807eda27434231040-Paper.pdf)\],
and circuits are subgraphs with distinct functionality

\[[[https://arxiv.org/abs/2211.00593]{.underline}](https://arxiv.org/abs/2211.00593)\].
Current approaches to extracting circuits from neural networks and
understanding their functionality rely on human manual inspection of
visualizations produced by circuits
\[[[https://doi.org/10.23915/distill.00024.001]{.underline}](https://doi.org/10.23915/distill.00024.001),
[[https://arxiv.org/pdf/2304.14997]{.underline}](https://arxiv.org/pdf/2304.14997)\].
Alternative approaches build sparse autoencoders that encourage neurons
to encode disentangled interpretable features
\[[[https://transformer-circuits.pub/2023/monosemantic-features/index.html]{.underline}](https://transformer-circuits.pub/2023/monosemantic-features/index.html)\].
This field is much newer than existing areas in explainability and
interpretability, and as such most works are generally exploratory
rather than solution oriented. There are many open problems in
mechanistic interpretability, including the polysemanticity of neurons
and circuits, the inconvenience and subjectivity of human labeling, and
the exponential search space for identifying circuits in large models
with billions or trillions of neurons.

As methods for interpreting and explaining models progress, it is
important to note that humans overtrust and misuse interpretability
tools
\[[[https://www-personal.umich.edu/\~harmank/Papers/CHI2020_Interpretability.pdf]{.underline}](https://www-personal.umich.edu/~harmank/Papers/CHI2020_Interpretability.pdf)\]
and that a user's trust in a model due to an explanation can be
independent of the correctness of the explanations
\[[[https://arxiv.org/pdf/1911.06473.pdf]{.underline}](https://arxiv.org/pdf/1911.06473.pdf)\].
As such, it is necessary that aside from assessing the
faithfulness/correctness of explanations, researchers must also ensure
that interpretability methods are developed and deployed with a specific
user in mind, and that user studies are performed to evaluate their
efficacy and usefulness in practice. Furthermore explanations should be
tailored with the expertise of the user in mind, as well as the task
they are using the explanation for, and the corresponding minimal amount
of information required for the explanation to be useful to prevent
information overload.

While interpretability/explainability are popular areas in machine
learning research, very few works study their intersection with TinyML
and edge computing. Given that a significant application of TinyML is
healthcare, which often requires high transparency and interpretability,
it is important that existing techniques are tested for scalability and
efficiency with respect to edge devices. Many methods rely on extra
forward and backward passes, and some even require extensive training of
proxy models, all of which would likely be infeasible on
microcontrollers that are resource constrained. That being said,
explainability methods can be highly useful in the *development* of
models for edge devices, as they can give insights into how input data
and models can be compressed and how representations may change post
compression. Furthermore, many interpretable models are often smaller
than their black-box counterparts, which could have additional benefits
in TinyML applications.

### Monitoring Model Performance

While developers may train models such that they seem adversarially
robust, fair, and interpretable before deployment, it is imperative that
both the users and the owners of the model continue to monitor the
model's performance and trustworthiness during the model's full
lifecycle. In practice, data is frequently changing, which can often
result in distribution shifts. These distribution shifts can have
profound impacts on both the vanilla predictive performance of the model
as well as its trustworthiness (fairness, robustness, and
interpretability) on real world data. Furthermore, definitions of
fairness also frequently change with time, such as what society
considers a protected attribute, and the expertise of the users asking
for explanations may change as well. To ensure that models keep up to
date with such changes in the real world, developers must continually
evaluate their model on current and representative data and standards,
and update models when necessary.

## Implementation Challenges

### Organizational and Cultural Structures \[sonia\]

![](vertopal_8b55cd460b0a41b2b53e2bf707e13be8/media/image1.png){width="5.416666666666667in"
height="3.2708333333333335in"}

While innovation and regulation are often seen as having competing
interests, a number of countries have found it necessary to provide
oversight as AI systems expand into more sectors \[[[Human-Centered AI,
Chapter 8 "Government Interventions and
Regulations"]{.underline}](https://academic-oup-com.ezp-prod1.hul.harvard.edu/book/41126/chapter/350465542)\].
Among these are:

-   Canada's [[Responsible Use of Artificial
    > Intelligence]{.underline}](https://www.canada.ca/en/government/system/digital-government/digital-government-innovations/responsible-use-ai.html)

-   The European Union's [[General Data Protection Regulation
    > (GDPR)]{.underline}](https://gdpr-info.eu/)

-   The European Commission's [[White Paper on Artificial Intelligence:
    > a European approach to excellence and
    > trust]{.underline}](https://commission.europa.eu/publications/white-paper-artificial-intelligence-european-approach-excellence-and-trust_en)

-   The UK's Information Commissioner's Office and Alan Turing
    > Institute's [[Consultation on Explaining AI Decisions
    > Guidance]{.underline}](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/artificial-intelligence/explaining-decisions-made-with-artificial-intelligence/#:~:text=This%20co%2Dbadged%20guidance%20by,the%20individuals%20affected%20by%20them.)

### Obtaining Quality and Representative Data

Responsible AI design must occur at all stages of the pipeline,
including data collection. This begs the question; what does it mean for
data to be high-quality and representative? Consider the following
scenarios that *hinder* the representativeness of data:

-   **Subgroup imbalance.** This is likely what comes to mind when
    > hearing the phrase "representative data." Subgroup imbalance means
    > that the dataset contains relatively more data from one subgroup
    > than another. This imbalance can negatively affect the downstream
    > ML model, by causing it to overfit to a subgroup of people while
    > having poor performance on another. One example consequence of
    > subgroup imbalance is racial discrimination in facial recognition
    > technology
    > \[[[https://sitn.hms.harvard.edu/flash/2020/racial-discrimination-in-face-recognition-technology/]{.underline}](https://sitn.hms.harvard.edu/flash/2020/racial-discrimination-in-face-recognition-technology/)\];
    > commercial facial recognition algorithms have up to 34% worse
    > error rates on darker-skinned females than lighter-skinned males.
    > Note that data imbalance goes both ways, and subgroups can also be
    > harmfully *overrepresented* in the dataset. For example, the
    > Allegheny Family Screening Tool (AFST) is used to predict the
    > likelihood that a child will eventually be removed from a home
    > \[[[https://www.alleghenycountyanalytics.us/wp-content/uploads/2018/10/17-ACDHS-11_AFST_102518.pdf]{.underline}](https://www.alleghenycountyanalytics.us/wp-content/uploads/2018/10/17-ACDHS-11_AFST_102518.pdf)\].
    > The AFST produces disproportionate scores for different subgroups,
    > one of the reasons being that it is trained on historically biased
    > data, sourced from juvenile and adult criminal legal systems,
    > public welfare agencies, and behavioral health agencies and
    > programs
    > \[https://www.aclu.org/the-devil-is-in-the-details-interrogating-values-embedded-in-the-allegheny-family-screening-tool#4-2-the-more-data-the-better\].

-   **Target outcomes that cannot be quantified.** This occurs in
    > applications where the ground-truth label *cannot be measured* or
    > is *difficult to represent* in a single quantity. For example, an
    > ML model in a mobile wellness application may want to predict
    > individual stress levels. The true stress labels themselves are
    > impossible to obtain directly, and must be inferred from other
    > biosignals, such as heart rate variability and user's
    > self-reported data. In these situations, noise is built into the
    > data by design, making this a challenging ML task.

-   **Distribution shift.** Data may no longer be representative of a
    > task if a major external event causes the source of the data to
    > change drastically. The most common way to think about
    > distribution shift is with respect to time; for example, data on
    > consumer shopping habits that was collected pre-covid may no
    > longer be representative of consumer behavior today. Another form
    > of distribution shift is that caused by transfer. For example, in
    > applying a triage system that was trained on data from one
    > hospital to another, distribution shift may occur if the two
    > hospitals are very different.

**Gathering more data.** A reasonable solution for many of the above
problems with non-representative or low-quality data is to collect more;
we can collect more data targeting an underrepresented subgroup or
collect more data from the target hospital to which our model might be
transferred. However, there are also reasons that gathering more data is
an inappropriate or infeasible solution for the task at hand.

-   *Data collection can be harmful.* This is the *paradox of exposure*,
    > the situation in which those that stand to significantly gain from
    > their data being collected are also those that are put at risk by
    > the collection process (Data Feminism, Chapter 4). For example,
    > collecting more data on non-binary individuals may be important
    > for ensuring fairness of the ML application, but also put them at
    > risk, depending on who is collecting the data and how (whether the
    > data is easily identifiable, contains sensitive content, etc).

-   *Data collection can be costly.* In some domains, such as in
    > healthcare, obtaining data can be costly in terms of time and
    > money.

-   *The data collection process itself can be biased.* For example,
    > Electronic Health Records are a huge data-source for ML driven
    > healthcare applications. Issues of subgroup representation aside,
    > the data itself may be collected in a biased manner. For example,
    > negative language ("nonadherent", "unwilling") is
    > disproportionately used on black patients \[Himmelstein, G.,
    > Bates, D., & Zhou, L. (2022). Examination of stigmatizing language
    > in the electronic health record. *JAMA Network Open*, *5*(1),
    > e2144967-e2144967\].

**Other ways to ensure and improve data quality.**

We conclude with several additional strategies for maintaining data
quality: improving understanding of the data, data exploration, and
intr. Firstly, fostering a deeper understanding of the data is crucial.
This can be achieved through the implementation of standardized labels
and measures of data quality, such as in the [[Data Nutrition
Project]{.underline}](https://datanutrition.org/). Directly
collaborating with organizations responsible for the data collection can
help ensure that the data is interpreted correctly. Second, employing
effective tools for data exploration, such as . Furthermore,
establishing a feedback loop within the ML pipeline is essential for
understanding the real world implications of the data. Metrics, such as
fairness measures, allow us to define "data quality" in the context of
the downstream application; improving fairness may directly improve the
quality of the predictions that the end users receive.

### Difficulty Balancing Accuracy and Other Objectives

Though accuracy is the most popular evaluation metric on a machine
learning system, it is by no means the *only metric*, especially when
considering responsible AI. Other metrics that have been discussed
throughout the chapter-- including fairness, adversarial robustness, and
explanabililty-- can come into tension with accuracy when being
optimized. For example, one form of explainability is an *inherently
interpretable model*, such as a linear model with meaningful features.
By design, these models are simple enough to be analyzed by humans and
therefore less capable of expressing complex trends in the data, which
in turn, may negatively impact accuracy.

How do we know when it is worth trading-off accuracy for other
objectives such as fairness? Every (useful) ML system is situated in a
social context (in broader terms, the synthesis of technology and
society is referred to as a sociotechnical system). Therefore, every
design decision made for the ML system, such as the objective function,
can be made while considering the sociotechnical system. There are
design frameworks for analyzing how ML design choices will interface
with the broader social system. One such framework is Value Sensitive
Design \[https://vsdesign.org/\], in which the values of direct and
indirect stakeholders of the system are formalized. The *tensions*
between these values are also highlighted by VSD, and can be used to
inform the choice of objective.

### Increased Cost and Complexity of Models

### Lack of Standards and Best Practices

-   No regulation?

-   Multiple methods, all with different answers, no one knows what to
    > use

    -   No good benchmarks for \[fairness/interpretability/robustness\]
        > performance

## 

## 

## Ethical Considerations in AI Design \[sonia\]

In this section, we present an introductory survey of some of the many
ethical issues at stake in the design and application of AI systems and
diverse frameworks for approaching these issues, including those from AI
safety, Human-Computer Interaction (HCI), and Science, Technology, and
Society (STS).

### AI Safety/value alignment

In 1960, Norbert Weiner wrote, "'if we use, to achieve our purposes, a
mechanical agency with whose operation we cannot interfere
effectively... we had better be quite sure that the purpose put into the
machine is the purpose which we really desire" \[[[Some Moral and
Technical Consequences of Automation \|
Science]{.underline}](https://www.science.org/doi/10.1126/science.131.3410.1355)\].
In recent years, as the capabilities of deep learning models have
achieved, and sometimes even surpassed human abilities, the issue of how
to create AI systems that act in accord with human intentions instead of
pursuing unintended or undesirable goals, has become a source of concern
\[[[Human-Compatible Artificial
Intelligence]{.underline}](https://people.eecs.berkeley.edu/~russell/papers/mi19book-hcai.pdf);
[[Artificial Intelligence, Values, and
Alignment]{.underline}](https://link.springer.com/article/10.1007/s11023-020-09539-2);
[[Aligning AI With Shared Human
Values]{.underline}](https://arxiv.org/abs/2008.02275)\]. Within the
field of AI safety, a particular goal concerns "value alignment," or the
problem of how to code the "right" purpose into machines
\[[[Human-Compatible Artificial
Intelligence]{.underline}](https://people.eecs.berkeley.edu/~russell/papers/mi19book-hcai.pdf)\].
Present AI research assumes we know the objectives we want to achieve
and "studies the ability to achieve objectives, not the design of those
objectives."

![](vertopal_8b55cd460b0a41b2b53e2bf707e13be8/media/image4.png){width="3.0781255468066493in"
height="2.358419728783902in"}

*"The formal problem F to be solved by the machine in this case is a
game-theoretic one: to maximize human future-life preferences subject to
its initial uncertainty as to what they are, in an environment that
includes human participants. Furthermore, although the future-life
preferences are hidden variables, they're grounded in a voluminous
source of evidence, namely, all of the human choices ever made."*
\[[[Human-Compatible Artificial
Intelligence]{.underline}](https://people.eecs.berkeley.edu/~russell/papers/mi19book-hcai.pdf),
pg. 8\]

The absence of this alignment can lead to a number of AI safety issues,
as have been document in a variety of deep learning models
\[[[Specification gaming: the flip side of AI
ingenuity]{.underline}](https://deepmind.google/discover/blog/specification-gaming-the-flip-side-of-ai-ingenuity/)\].
A common feature of systems that optimize for an objective, is that
variables not directly included in the said objective may be set to
extreme values to help optimize for that objective, leading to issues
that have been characterized as specification gaming, reward hacking,
etc. in reinforcement learning (RL). In recent years, a particularly
popular implementation of RL has been models pre-trained using
self-supervised learning and fine-tuned using reinforcement learning
from human feedback (RLHF) \[[[Deep Reinforcement Learning from Human
Preferences]{.underline}](https://papers.nips.cc/paper_files/paper/2017/hash/d5e2c0adad503c91f91df240d0cd4e49-Abstract.html)\].
\[[[The alignment problem from a deep learning
perspective]{.underline}](https://arxiv.org/abs/2209.00626)\] argue that
by rewarding models for appearing harmless and ethical, while also
maximizing useful outcomes, RLHF could encourage the emergence of three
problematic properties: situationally-aware reward hacking where
policies exploit human fallibility to gain high reward, misaligned
internally-represented goals that generalize beyond the RLHF fine-tuning
distribution, and power-seeking strategies. Similarly, \[[[Concrete
Problems in AI Safety]{.underline}](https://arxiv.org/abs/1606.06565)\]
outline six concrete problems for AI safety, including avoiding negative
side effects, avoiding reward hacking, scalable oversight for aspects of
the objective that are too expensive to be frequently evaluated during
training, safe exploration strategies that encourage creativity but
while preventing harms, and robustness to distributional shift in unseen
testing environments.

### Autonomous Systems and Control \[and Trust\]

The consequences of autonomous systems that act independently of human
oversight, and often outside of human judgment, have been well
documented across a number of different industries and use cases. Most
recently, the The California Department of Motor Vehicles suspended
Cruise's deployment and testing permits for its autonomous vehicles
citing "unreasonable risks to public safety" \[[[California DMV suspends
Cruise\'s self-driving car permits, effective
immediately]{.underline}](https://www.cnbc.com/2023/10/24/california-dmv-suspends-cruises-self-driving-car-permits.html)\].
One such accident occurred when a vehicle struck a pedestrian who
stepped into a crosswalk after the stoplight had turned green, and the
vehicle was allowed to proceed \[[[Federal regulators open probe into
Cruise after pedestrian injury
reports]{.underline}](https://www.cnbc.com/2023/10/17/cruise-under-nhtsa-probe-into-autonomous-driving-pedestrian-injuries.html)\].
In 2018, a pedestrian crossing the street with her bike was killed when
a self-driving Uber car, which was operating in autonomous mode, failed
to accurately classify her moving body as an object to be avoided
\[[[Uber\'s self-driving operator charged over fatal
crash]{.underline}](https://www.bbc.com/news/technology-54175359)\].
Autonomous systems beyond self-driving vehicles are also susceptible to
such issues, with potentially graver consequences, as remotely-powered
drones are already reshaping warfare \[[[Human-machine teams driven by
AI are about to reshape
warfare]{.underline}](https://www.reuters.com/technology/human-machine-teams-driven-by-ai-are-about-reshape-warfare-2023-09-08/)\].
While such incidents bring up important ethical questions regarding who
should be held responsible when these systems fail \[[[Who Is
Responsible When Autonomous Systems Fail? - Centre for International
Governance
Innovation]{.underline}](https://www.cigionline.org/articles/who-responsible-when-autonomous-systems-fail/)\],
they also highlight the technical challenges of giving full control of
complex, real-world tasks to machines.

At its core, there is a tension between human and machine autonomy.
Engineering and computer science disciplines have tended to focus on
machine autonomy. For example, as of 2019, a search for the word
"autonomy" in the Digital Library of the Association for Computing
Machinery (ACM) reveals that of the top 100 most cited papers, 90% are
on machine autonomy ([[Supporting Human Autonomy in AI Systems: A
Framework for Ethical
Enquiry]{.underline}](https://link.springer.com/chapter/10.1007/978-3-030-50585-1_2)).
In an attempt to build systems for the benefit of humanity, these
disciplines have taken without question increasing productivity,
efficiency, and automation as primary strategies for benefiting
humanity. These goals put machine automation at the forefront, often at
the expense of the human. This approach suffers from inherent
challenges, as noted since the early days of AI through the Frame
problem and qualification problem, which formalizes the observation that
is impossible to specify all the preconditions needed for a real-world
action to succeed \[[[EPISTEMOLOGICAL PROBLEMS OF ARTIFICIAL
INTELLIGENCE]{.underline}](https://www-formal.stanford.edu/jmc/epistemological.pdf)\].
These logical limitations have given rise to mathematical approaches
such as Responsibility-sensitive safety (RSS) \[[[On a Formal Model of
Safe and Scalable Self-driving
Cars]{.underline}](https://arxiv.org/pdf/1708.06374.pdf)\] which is
aimed at breaking down the end goal of an automated driving system
(namely safety) into concrete and checkable conditions that can be
rigorously formulated in mathematical terms. The goal of RSS is that
those safety rules guarantee ADS safety in the rigorous form of
mathematical proofs. However, such approaches tend towards using
automation to the problems of automation and are susceptible to many of
the same issues.

Another approach to combating these issues is to turn the focus towards
the human-centered design of interactive systems that incorporate human
control. \[[[Value-sensitive
design]{.underline}](https://dl.acm.org/doi/10.1145/242485.242493)\]
described three key design factors for a user interface that impact
autonomy, including system capability, system complexity,
misrepresentation, and fluidity. A more recent model, called METUX (A
Model for Motivation, Engagement, and Thriving in the User Experience)
leverages insights from Self-determination Theory (SDT) in Psychology to
identifies six distinct spheres of technology experience that contribute
to the design systems that promote wellbeing and human flourishing
\[[[Designing for Motivation, Engagement and Wellbeing in Digital
Experience]{.underline}](https://www.frontiersin.org/articles/10.3389/fpsyg.2018.00797/full)\].
SDT defines autonomy as acting in accordance with one's goals and
values, which is distinct from the use of autonomy as simply a synonym
for either independence or being in control \[Soenens et al. 2007;
[[Self-determination theory and the facilitation of intrinsic
motivation, social development, and
well-being]{.underline}](https://psycnet.apa.org/record/2000-13324-007?doi=1)\].
\[[[Supporting Human Autonomy in AI Systems: A Framework for Ethical
Enquiry]{.underline}](https://link.springer.com/chapter/10.1007/978-3-030-50585-1_2)\]
elaborates on METUX and its six "spheres of technology experience" in
the context of AI-recommender systems. They propose these spheres --
Adoption, Interface, Tasks, Behavior, Life, and Society -- as a way of
organizing thinking and evaluation of technology design in order to
appropriately capture contradictory and downstream impacts on human
autonomy when interacting with AI systems.

### Economic Impacts on Jobs, Skills, Wages

A major concern of the current rise of AI technologies is widespread
unemployment. As AI systems' capabilities expand, many fear that these
technologies will cause an absolute loss of jobs as they replace current
workers and overtake alternative employment roles across industries.
However, changing economic landscapes at the hands of automation are not
new, and historically, have been found to reflect patterns of
*displacement* rather than replacement \[[[Human-Centered AI, Chapter 4
"Will Automation, AI, and Robots Lead to Widespread
Unemployment?"]{.underline}](https://academic-oup-com.ezp-prod1.hul.harvard.edu/book/41126/chapter/350464056)\].
In particular, automation usually lowers costs and increases quality,
which greatly increases access and demand. The need to serve these
growing markets pushes production, which in turn creates new jobs.
Further, studies have found that attempts to achieve "lights-out"
automation -- productive and flexible automation with a minimal number
of human workers -- have been unsuccessful. Attempts to do so have led
to what the MIT Work of the Future taskforce has termed "zero-sum
automation", in which process flexibility is sacrificed for increased
productivity \[[[A Smarter Strategy for Using
Robots]{.underline}](https://hbr.org/2023/03/a-smarter-strategy-for-using-robots)\].
The taskforce propose a "positive-sum automation" approach in which
flexibility is increased by designing technology that strategically
incorporates humans where they are very much needed: making it easier
for line employees to train and debug robots; using a bottom-up approach
to identifying what tasks should be automated; and choosing the right
metrics for measuring success \[[[The Work of the Future: Building
Better Jobs in an Age of Intelligent
Machines]{.underline}](https://workofthefuture-mit-edu.ezp-prod1.hul.harvard.edu/wp-content/uploads/2021/01/2020-Final-Report4.pdf)\].
However, the optimism of the high-level outlook does not preclude
individual harms, especially to those whose skills and jobs will be
rendered obsolete by automation. Public and legislative pressure as well
as corporate social responsibility efforts will need to be directed to
create policies that share the benefits of automation with workers and
result in higher minimum wages and benefits \[[[Human-Centered AI,
Chapter 4 "Will Automation, AI, and Robots Lead to Widespread
Unemployment?"]{.underline}](https://academic-oup-com.ezp-prod1.hul.harvard.edu/book/41126/chapter/350464056)\].

### Scientific Communication and AI Literacy

A 1963 survey of 3000 North American adults\' beliefs about the
\"electronic thinking machine\" revealed two primary perspectives of the
early computer: the \"beneficial tool of man\" perspective and the
\"awesome thinking machine\" perspective. The attitudes contributing to
the \"awesome thinking machine\" view in this and other studies,
revealed a characterization of computers as "intelligent brains, smarter
than people, unlimited, fast, mysterious, and frightening" \[[[The myth
of the awesome thinking
machine]{.underline}](https://dl-acm-org.ezp-prod1.hul.harvard.edu/doi/abs/10.1145/255950.153587)\].

These fears highlight an easily overlooked component of responsible AI,
especially amidst the rush to commercialize such technologies:
scientific communication that accurately communicates the capabilities
*and* limitations of these systems, while providing transparency about
the limitations of experts' knowledge about these systems. As AI systems
capabilities continue to expand beyond most people's comprehension,
there is a natural tendency to assume the kinds of apocalyptic worlds
painted by our media. This is in part due to the apparent difficulty of
assimilating scientific information, even in technologically advanced
cultures, which leads to the products of science being perceived as
magic - "understandable only in terms of what it did, not how it worked"
\[[[Science and Technology in Popular
Culture]{.underline}](https://www.jstor.org/stable/20026900?seq=2)\].

While tech companies should be held responsible for limiting grandiose
claims and not falling into cycles of hype, research studying scientific
communication, especially with respect to (generative) AI, will also be
useful in tracking and correcting public understanding of these
technologies. An analysis of the Scopus scholarly database found that
such research is scarce, with only a handful of papers mentioning both
"science communication" and "artificial intelligence" \[[[The Notorious
GPT: science communication in the age of artificial
intelligence]{.underline}](https://jcom.sissa.it/article/pubid/JCOM_2202_2023_Y02/#X0-Brauseetal2023)\].
Research that exposes the perspectives, frames, and images of the future
that are promoted by academic institutions, tech companies,
stakeholders, regulators, journalists, NGOs and others will also help to
identify potential gaps in AI literacy among adults \[[[Handbook of
Critical Studies of Artificial
Intelligence]{.underline}](https://www.e-elgar.com/shop/gbp/handbook-of-critical-studies-of-artificial-intelligence-9781803928555.html)\].
Increased focus on AI literacy from all stakeholders, or the "a set of
competencies that enables individuals to critically evaluate AI
technologies, communicate and collaborate effectively with AI, and use
AI as a tool online, at home, and in the workplace" \[[[What is AI
Literacy? Competencies and Design
Considerations]{.underline}](https://dl.acm.org/doi/10.1145/3313831.3376727)\]
will be an important tool in helping people whose skills are rendered
obsolete by AI automation \[[[AI Literacy: Definition, Teaching,
Evaluation and Ethical
Issues]{.underline}](https://asistdl.onlinelibrary.wiley.com/doi/10.1002/pra2.487);
[[Artificial intelligence literacy in higher and adult education: A
scoping literature
review]{.underline}](https://www.sciencedirect.com/science/article/pii/S2666920X2200056X)\].

*"But even those who never acquire that understanding need assurance
that there is a connection between the goals of science and their own
welfare, and above all, that the scientist is not a man altogether apart
but one who shares some of their own value."* (Handlin, 1965)

## Case Studies

\- Examples demonstrating responsible AI principles

\- Lessons learned from real-world systems

## Conclusion

\- Key takeaways on achieving responsible AI

\- Future outlook and areas for advancement