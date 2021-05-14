# Neural mechanisms of decision-making
**What is decision-making?** DM is a deliberative volountary process that results in the selection of an action, based on sensory information about the environment and the agent's internal state.

The decision can be controlled by stimulus called **reinforcers**: rewards and punishment.
From a psychological point of view we have to map the sensory input into a decision, taking into account the environment.

Decisions are inherently probabilistic and non-deterministic:
* Agents make inconsistent choices (i.e. sometimes we can choose sub-optimal decision);
* Agents make choices without fully know the consequences (i.e. we choose with uncertainty);
* External and internal signals are corrupted by noise.

Many modern decision theories consider the choice process, including deliberations and estimation of competing outcomes as instrinsically random, stochastic. Within an evolutionary framework, it's possible to show that being stochastic may augment the chances of survival and reproductive success, in the changing, uncertain and dangerous environments that characterized homo sapiens evolution.

There are two main kind of DM:
* **Perceptual DM**: agents select action A or B, based on weak or noisy external signals (i.e. you saw A or B?);
* **Value-based DM**: agents select action A or B, based on their subjective preference or value (i.e. you prefer A or B?).

Source of uncertainty changes:
* **Perceptual DM**: it's the identity of the stimulus that is uncertain, not the value of the associated action (uncertainty at sensory level);
* **Value-based DM**: it's the value of its associated action that is uncertain, not the identity of the stimulus.
<center>  <img  src=https://i.ibb.co/zHPqmXs/dm.png  width="500px"  />  </center>

*Note*: there's should be some consistency in what you prefer, some kind of transitivity.

## Value-based decision-making
Humans continuosly engage behaviours that entail a choice (i.e. different goods, select an investment, choose a mate, etc...). This kind of DM, known as value-based (or preferential, or economic), describes **choices guided by our preferences or values**.

It comprises five basic processes:
1. **Representation**: the available options (states) and actions, internal (i.e. hunger level) and external (i.e. threat level) factors, are identified;
2. **Valuation**: a value is assigned to different alternatives;
3. **Choice**: values are compared and then the highest one is selected;
4. **Outcome**: desirability of the consumed outcomes is measured;
5. **Learning**: feedback signals updates the relevant processes to improve the quality of next decision.
<center>  <img  src=https://i.ibb.co/JqdLGTK/choice.png  width="600px"  />  </center>

*Note*: usually are binary decision.

### Value vs. reward
The value of an option is the total amount of reward an agent can expect to accumulate over the future, from that state (expected reward, an internal prediction), while reward refers to the immediate advantage given from a state

*Example*: a state might always yield a low immediate reward but still have a high value because it's regularly followed by other states that yield high rewards.

Ideally choices are made based on value (foresightedness, frontal cortex usually helps with this).

### Utility
Utility is a subjective measure of satisfaction that a consumer obtains from the consumption of the choice, that varies from individual to individual, according to each individual's preference.
It's inferred directly from behaviour and neural representations of this function are are assumed to reflect behavioural preferences.

#### Alternative definitions
A further approach define values in terms of motivating properties of a stimulus from instrumental action: the degree to which an animal is prepared to work - to obtain a stimulus - relates to the degree to which the animal finds that stimulus desiderable (i.e. is it worth going to work to earn money?).

Under situations, behaviours can become **habits**, and an **action can be selected to obtain a good that is not actually preferred by the animal**. 

Both the *revealed preference* and *work motivation* definitions of value, would yield an inference that this particular good has high value for the animal, because it's reflected in the action-selection behaviour (i.e. I don't like drugs but I want them). However, once the good is obtained as result of the habitual actions, the animal won't actually consume the good.

### Reward functions
Obtaining primary rewards (i.e. food, liquid and sex) is critical to our survival, so rewards drive many of our behavioural and cognitive processes. Rewards can produces:
* Hedonic consequences (subjective pleasure);
* Assigning motivatonal value to goals, so that the organism can select among numerous behavioural options and determine what level of resources to put toward obtaining a specific goal (wanting);
* Learning cues that predict reward availability (pavlovian conditioning) and actions that permit its consumption (instrumental conditioning).

In economic theories, decision-making corresponds to the selection of an action with maximum utility, while in reinforcement learning, actions are chosen probabilistically (i.e. softmax) on the basis of their value functions, and value functions are updated on the basis of the outcome.
<center>  <img  src=https://i.ibb.co/gvPqHJC/Cattura.png  width="500px"  />  </center>

### A computational model of value-based DM
*Mental experiment*: on every trial the subject is shown a consumption stimulus (i.e. tasty food), as well as the amount of effort required to get it (i.e. squeeze handgrip). 
The subject needs to decide of he wants to get the food in exchange for that effort, or get nothing but do not work (yes/no decision).

These tasks leads to psychometric choice (sigmoid) curves, that are consistent with the logistic choice model, and define the probability of choosing the food as a function of stimulus value (orange curve), and action cost (green curve), respectively.

The probability of saying yes increases with the subjective values of the consumption good, and decreases with the action costs (B).
<center>  <img  src=https://i.ibb.co/9GJmJGs/diffusion.png  width="600px"  />  </center>

**Drift diffusion model (DDM)**
The DDM assumes that decisions are made by a noisy and dynamic process that accumulates information over time (**sequential sampling model**) from a starting point, towards one of the two response criteria (boundaries). 
DDM separates the evidence entering the decision, from the decision criteria and from other, non-decision processes, such as stimulus encoding and response excution.
<center>  <img  src=https://i.ibb.co/nsRfYRr/drift.png  width="500px"  />  </center>

According to the DDM, a binary choice is made by dynamically integrating:
* Stimulus value ($SV$);
* Action cost ($AC$);
into an noisy *action value signal* ($AV$) that measures the estimated relative value of one action versus the other (yes/no).

The signal start to zero and evolves until a pre-specified barrier is crossed, according to:
$$R_{t+1} = R_t + \theta \bigl( \text{AV}(\text{Yes}) - \text{AV}(\text{No}) \bigr) + \varepsilon_0$$

In DDM, the decision is based on a sequence of observations (sequential sampling): after each acquisition, a decision variable is calculated from the evidence obtained up to that point, then, more evidence can be obtained or the process can be terminated with a decision.

In single models, information is accumulated as a single total: information in favour of one is evidence against the other. In race models, information favouring different responses is accumulated separately.

DDM models can account for the effects of changing stimuli or instructions, varying a single parameter for each:
* **Drift rate**: the rate of accumulation of information. Is determined by the quality of information extracted from the stimuli (i.e. if quality is poor, rate of accumulation is slower and decision takes longer);
* **Boundary separation**: decision criteria (amount of information needed for a response). Boundaries decreases to respond rapidly, increases to respond accurately.
<center>  <img  src=https://i.ibb.co/L0Z9yYf/Cattura.png  width="500px"  />  </center>

### Value signals in the brain
**State value**: corresponds to the rewards expected from a particular state of the animal's environment. Denoted by $S(t)$, it represents the average of action values functions weighted by the probability of taking each action in a given state.
**Action values**: corresponds to the rewards expected for taking a particual action in a particular state of the environment, and it's often denoted by $Q(s,a)$, where $s$ and $a$ refer to the state of the environment and the animal's action, respectively.

During decision-making, the state valued function changes from the weighted average of action valued for alternative choices, to the action value function for the chosen action (chosen value).

How to identify value signals?
* From the subject: liking ratings of BDM actions that provide a monetary and incentive compatible measure (questionaries);
* From the brain: values of signals are encoded either in single neurons or in clusters. The firing rate of these neurons, or the activity of such regions, should be proportional to the subject, and stimulus-specific.

This prediction can be tested using the usual neurophysiologic methods, to look for neurons or brain regions in which the measures of neural activity correlate with value signals.

### Stimulus value vs. stimulus identity
Difference found in neural activity in response to different outcomes, might reflect sensory properties (*identity*) instead of the underlying *value* of those outcomes (in which we are interested).
* One way to circumvent this problem is to use the manipulation of expected values (i.e. probability and magnitude of stimuli);
* Another way is to use **reversal task**: one option yields a monetary reward with some probability, while the other a monetary loss with some probability. After a while, contingencies are reverse.

### Reinforcer devaluation
Another approach to measuring neural responses to values is to measure activity to a particular outcome (or a cue, or an action associated with a given outcome), before and after introducing a change in the experienced utility (**reinforcer devaluation**, i.e. I test a subject when hungry and then when satiated).

Changes in activation, measured in response to the stimulus following the devaluation, can be assumed to be related to a **change in the reward-value of the associated outcome**.

### Slide 27,28,29

### Validation circuitry
Neurons sensitive to reward value are widespread in the brain. 
Satiation of the animal reduces the reward responses in orbifrontal cortex, suggesting that the **responses reflect the rewarding functions of the objects** rather than their teaste. Infact, taste responses are found in the primary guustatory area and are insensitive to satiation.

## Value computation in OFC
*Orbitofrontal cortex* (OFC) is specialized for reward processing. It contains a high frequency of neurons that show selective responses to delivery of food and liquid rewards, and other OFC neurons respond to cues that predict rewards. This activity discriminates between reward and no reward, preferred and non-preferred rewards.

Neural activity in the OFC plays a crucial role in the generation of expectancies concerning outcomes (important for prediction).

Neurons in the orbifrontal cortex encode economic values. Economic choice is the behavior observed when individuals select one among many available options.
*Experiment*: thirsty monkeys choos between two types of juice offered in different amounts. Behaviourally, a trade-off between juice type and juice quantity is observed (i.e. they preferred A over B, and chose A even in front of four times B).

Rarely, neuron responses depend on the spatial configuration of the offers, in contrast, the activity of most neurons varies significantly depending on the offer type.

Three types of neurons were found:
* **Chosen values neurons**: respones reflect economic values of juice that was chosen, rather than physical properties;
* **Offer value neurons**: responses reflect the value of one of the two juices alone
* **Taste neurons**: responses reflect the type of juice chosen by the monkey, independently of the amount.

Responses encoding the chosen value are particulary interesting, because they're indepent of the visuomotor contingencies of the task and also independent of the specifics of the good (juice type or amount). 

*Example*: in the case of chose value neuron, the firing rate would be the same whether the monkey chose one drop of A or four drops of B.

We can't explain this pattern based on the drinks volume (equal volumes of the drinks produce different firing rates), nor on the drinks taste (certain volumes of the drinks produce equal firing rates). We can explain it in terms of monkey **subjective preferences**, because when the monkey valuation of the drinks is the same, the neuronal firing rate is also equivalent. Hence, **OFC neurons are important for deriving the subjective value of an outcome**, and using them to guide choice behaviour.

### Temporal discounting
To behave optimally, agents must be able to compute the value of rewards that can take place arbitrarily far in the future. *Temporal discounting* (TD) refers to the decline in subjective value with increasing delays. It differs across individuals and is described by discount functions, well characterized by a hyperbolic function. 

Choosing between immediate and delayed monetary rewards involves comparing neutrally encoded subjective values. This encoding seems to take place in the *anterior cingulate cortex* (ACC).

### Effort-based decision-making
ACC and OFC lesions have distinct effects on how decision are made when both *reward* and *action cost* need to be considered in order to make decisions.

*Experiment*: rats choose between two arms of a T-maze, associated with different pellets and barriers.
<center>  <img  src=https://i.ibb.co/gFcD2P3/uno.png  width="700px"  />  </center>

* Normal control rats stil opted for high reward option, despite the effort of the barrier;
* ACC lesions cause animals to always opt for the low reward option, not because they weren't able to make effortful action, but because they weren't able to **integrate together effort and reward information** like before.

These results imply that medial frontal cortex is important for allowing the animal to put more work to obtain greater rewards.

## Reinforcement learning
We learn by interacting with our environment. When an infant plays, it has no explicit teacher, but has a direct sensorimotor connection to her environment. Excercising this connection produces information about cause and effect and what to do in order to achieve goals.

Reinforcement learning is learning what to do (how to map states into action) to maximize reward: the learned is not told which action to take but must discover which actions yield the most reward by trying them.

Three different learning mechanism operate within the brain:
* **Unsupervised learning**: used by the brain to detect statistical regularities or inherent patterne hidden in the perceived environment;
* **Supervised learning**: some internal or external supervisor (teacher) supplies a desired output (correct answer) when the learner produces an output in response to a certain input pattern. Learning process is based on the minimization of the error;
* **Reinforcement learning**: aims at maximizing the value of action choices. The system that selects different actions is modified depending on the reward obtained. Agento and environment interacts continually.

These different mechanism operates in different areas of the brain:
<center>  <img  src=https://i.ibb.co/ZBDn7b9/brain-areas.png  width="600px"  />  </center>

The field of behavioural psychology focuses on the ability of animals to learn appropriate behaviour on the basis of the associated rewards or punishments. Animals and artificial systems face similar problems in learning how to optimizing their behaviour in the light of rewards and punishments.
The field is traditionally separated in:
* **Classical (or Pavolvian) conditioning**: reinforcers are delivered independently of any behavioural response emitted by the animal (prediction algorithm);
* **Instrumental (or operant) conditioning**: behavioural response of the animal determine what reinforcement is provided (control algorithm).

### Pavlovian learning
* **Unconditioned response** (UR): a response that doesn't have to be learned (autonomic reflex, i.e. pupil dilation);
* **Unconditioned stimulus** (US): stimulus that elicits a response (autonomic reflex) without any prior learning (i.e. smell of tasty food elicits salivation);
* **Conditioned response** (CR): learned response to a conditioned stimulus (i.e. ring of a bell elicits salivation);
* **Conditioned stimulus** (US): stimulus that elicits a response only after learning has taken place (i.e. ring of a bell indicates food is coming).

**Blocking**: occours when an animal fails to learn a conditioned response, when a potential conditioned stimulus is presented with another conditioned stimulus that was already used to produce that conditioned response (you don't need to learn something you already know).
<center>  <img  src=https://i.ibb.co/KXpgjBk/doggo.png  width="600px"  />  </center>

**High-order conditioning**: occours when a previously conditioned stimulus acts as as an unconditioned stimulus in conditioning another initially neutral stimulus (works as a sort of transitivity).
<center>  <img  src=https://i.ibb.co/svpDcs5/doggo.png  width="600px"  />  </center>
 
#### The Rescorla-Wagner model
The model postulates that **learning occours only when events violate expectations**
Two important assumptions:
1. Learning happens only when events are not predicted;
2. Predictions due to different stimuli are summed to form the total prediction in a trial.

Learning is driven by the discrepancy between what was predicted and what actually happened.

### Instrumental learning
In instrumental conditioning, learning depends on the consequences of behaviour: the delivery of a reinforcing stimulus is contingent on what the animal does, while in classical conditioning the reinforcers is delivered in any case.

**Law of effect**: generally known as learning by trial and error. In computational terms, describes an elementary way of combining search and memory (like searching with an heuristic).

Instrumental learning algorithms are:
* **Selectional**: try different alternatives and select among them comparing their consequences;
* **Associative**: alternatives found by selection are associated with particular situations to form agent's policy.

Reinforcement learning is not just finding actions that produce a lot of reward, but also connecting these actions to situations or states.

