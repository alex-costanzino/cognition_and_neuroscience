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
<center>  <img  src=https://i.ibb.co/9GJmJGs/diffusion.png  width="500px"  />  </center>

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

*Note*: reward value evaluation in human seems to be in the amygdala and orbifrontal cortex.

### Validation circuitry
Neurons sensitive to reward value are widespread in the brain. 
Satiation of the animal reduces the reward responses in orbifrontal cortex, suggesting that the **responses reflect the rewarding functions of the objects** rather than their teaste. Infact, taste responses are found in the primary guustatory area and are insensitive to satiation.

## Value computation in OFC
*Orbitofrontal cortex* (OFC) is specialized for reward processing. It contains a high frequency of neurons that show selective responses to delivery of food and liquid rewards, and other OFC neurons respond to cues that predict rewards. This activity discriminates between reward and no reward, preferred and non-preferred rewards.

OFC has a key role in integrating multiple signals for the decision-makign process.

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
<center>  <img  src=https://i.ibb.co/gFcD2P3/uno.png  width="500px"  />  </center>

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
<center>  <img  src=https://i.ibb.co/ZBDn7b9/brain-areas.png  width="400px"  />  </center>

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

### Prediction and predition learnign during value learning
In both types of conditioning learning is based on a comparison between reward actually obtained and the reward expected on the basis of previous learning. 
The difference between these two quantities is known as **prediction error**: if the difference is large the predictions did not match observations, and more learning is needed. More formally: $$\delta_t = r_t - V_t$$
where:
* $r_t$ is the reward obtained;
* $V_t$ is the value expected.

The animal updates the prediction in the direction of the prediction error, to reduce it. Hence, in the next trial: $$V_{t+1} = V_t + \alpha \delta_t$$
where $\alpha$ is the **learning rate**, a parameter in $[0,1]$, that determines the size of the update step.

Learning is proportional to the prediction error $\delta$, that is larger at the start of the training, since the reward is unexpected, and gets smaller as the training progresses and the reward is correctly predicted.

**Rescorla-Wagner learning rule**: a prediction error is generated when outcome differs from its prediction. In Pavlovian and instrumental conditioning, a prediction error that leads to a change in prediction, leads to a behavioural change. Otherwise, if there is a match, no prediction error is generated.

### Temporal difference learning
Rescorla-Wagner model suffers from two major difficulties:
* Doesn't extend to high-order conditioning;
* Doesn't take into account sensitivity of conditioning to different temporal relations between the conditional and unconditional stimuli.

To overcome these two problems, **Sutton** and **Barto** suggested the **temporal difference learning rule** as a model of prediction learning in Pavlovian conditioning, an extension that takes into account the timing of different events, solving both problems.

In TD learning the agent's goal is to estimate the values of different states or situations, in terms of future rewards or punishments that they predict.

It considers a dynamic process, in which different states $S$ follow one another according to some predefined probability distribution $P(S_t+1|S_t)$, and rewards are observed at each state with probability $P(r|S)$. 
A useful quantity to predict in such a situation is the **expected sum of all future rewards**, given the current state $S_t$, namely the value $V(S_t) = P(r|S_t) + \gamma \sum_{S_{t+1}} P(S_t+1|S_t) V(S_{t+1})$.

The discount rate $\gamma$ was first introduced in order to ensure that the sum of future rewards is finite, however, it also aligns well with the fact that **humans and animals prefer earlier rewards to later ones**.

This scheme suffers of one major problem: it requires knowledge of the dynamics of the environment in order to compute the TD prediction error. Unreasonable for Pavlovian conditioning.

In a model-free case, where we cannot assume knowledge of the dynamics, it's the environment itself that supply this information: everytime that an animal is in a situation that corresponds to $S_t$ it can sample: 
* The reward probability in this state;
* The probabilities of transitions from this state to another.

As it experiences different states repeatedly the animal obtain samples and updates the estimated values according to these samples, eventually leading to the correct predictive values: $$\delta_t = r_t + \gamma V(S_{t+1}) - V(S_t))$$

### Dopinamergic system
There is strong evidence that dopaminergic system is the major neural substrate of reward and reinforcement for both natural rewards and addictive drugs.
<center>  <img  src=https://i.ibb.co/YXhXRG0/vfzsdfdf.png  width="400px"  />  </center>

All neurons tha produce dopamine (that is a neuromodulator, not a neurotransmitter) are deep in the brain, and then it goes into two major pathways:
* The one that originates from the *substantia nigra* (SNpc) and projects to the caudate-putamen, it's identified most strongly with **motor function** (most associated with action);
* The one that starts from the *ventral tegmental area* (VTA) and projects in two separate area of the frontal cortex, it's important for motivational function (less associated with action).

Dopamine neurons show phasic excitatory and inhibitory responses to different events, that can be interpreted as reward prediction error, similar to the one of Rescorla-Wagner.
The activation comes from **rewarding stimuli**: 
* About $75\%$ of dopamine neurons show phasic activation when animals touch a small piece of hidden food, or when drops of liquid are delivered to the mouth outside of any task. They do not discriminate between food and neurons (*identity*), but they distinguish rewards from non-rewards (*value*);
* Only $14\%$ of dopmine neurons show phasic activation whe avversive stimuli are administred (i.e. pain or electrical shock).

*Experiment*: a monkey puts the hand in a box (search task), touching something:
* Dopamine responses to touch of food, without any phasic stimuli predicting the reward;
* Differential response of dopamine neurons wrt touching a wire holding a piece of apple or an inedible object.

Dopamine neurons respond differentially to unpredicted objects of differing reward values, consistently with a prediction error signal: prediction error is positive when a reward is delivered but not expected.

*Note*: the dopamine neurons that fire with food are slow, like a metronome. Moreover they're food-invariant, they fire for food (*value*), not for the type (*identity*).

#### Activation by conditioned stimuli
About $55\% - 70\%$ of dopamine neurons are activated by visual and auditory *conditioned stimuli* (CS), that predicts rewards in various conditioned tasks. Only $10\%$ of dopamine neurons are activated by CS predicting avversive events.
* Before learning, a drop of appetitive juice occours in absence of prediction. Hence there is a **positive error** in the prediction: the **dopamine neuron is activated by an unpredicted occurence of juice**;
* After learning, the conditioned stimulus predicts reward, that comes according to the prediction. Hence there is **no error**: the **dopamine neuron is activated by the predicted reward**;
* After learning, the conditioned stimulus predicts reward, that fails to occour. Hence there is a **negative error** in the prediction: the **dopamine neuron is depressed exactly at the time when reward would have occoured**.
<center>  <img  src=https://i.ibb.co/k2pVLxb/vfzsdfdf.png  width="200px"  />  </center>

#### Activation during learning
The dopamine activation undergoes systematic changes during the progress of learning.
Primary rewards elicit neuronal activations during initial learning periods, which decrease progressively and are transfered to the conditioned, reward-predicting stimuli with increasing learning.

During a transient learning period, both rewards and conditioned stimuli elicit an activation.  
*Example*: a dopamine neuron that responds initially to a juice reward acquires a response to the CS after some trials, in which the CS is paired with the reward.

#### Prediction error signal is bidirectional
The neuronal response of dopamine neurons is bidirectional: 
* A reward that is unexpectedly delivered or is better than predicted elicits an activation (positive error);
* An expected reward that is omitted, or is worse than expected, induces a depression (negative error).
<center>  <img  src=https://i.ibb.co/0Jwj4ct/vsevevaev.png width="500px"  />  </center>

#### Coding of reward probability by dopamine neurons
Prediction error is modulated both by predictions (expected reward) as well as obtained rewards. 
*Experiment*: in one study, five different visual CS predicted delivery of reward with different probabilities $p$, ranging in steps of $0.25$ from certain delivery ($p=1$), to certain non-delivery ($p=0$). 

According to the Rescorla-Wagner and TD learning models, when the animal has learned the task, the prediction $V_t$ for each stimulus would indicate the average reward obtained for that stimulus (i.e. $1$ for the certain reward stimulus, $0.5$ for the stimulus rewarded $50\%$ of the time, and so on). 

Thus the prediction error for reward delivery would be zero for the always rewarded stimulus, and large for the never-rewarded stimulus, and something in between for the others. Indeed, **phasic dopamine responses** to a reward have this property, they **increase with the size of the prediction error** (or, equivalently, decrease with the degree of reward probability). 
<center>  <img  src=https://i.ibb.co/CWLyQZq/sfegg.png width="700px"  />  </center>

#### Ramp-like tonic dopamine signals enocde reward uncertainty
Some dopamine show a sustained increase in activity that grows from the onset of the conditioned stimulus to the expected time of reward. The peak of the sustained activation occurs at the **time of potential reward**, which corresponds to the **moment of greatest uncertainty**. 
Tonic responses were significantly larger at $p = 0.5$, but in general,  measures of uncertainty (variance, standard deviation, and entropy) are all maximal at $p = 0.5$.
 
Subjective reward uncertainty corresponds both to the **necessity of identifying more accurate predictors** , and to the **expectation of reward information in order to resolve uncertainty** (uncertainty is higher when we are xpecting the reward and it's extremely important to see if rewards arrives or not).

#### Dopamine neurons report an error in the temporal prediction of reward
Dopamine responses depend on event unexpectedness. 

The unexpectedness, however, is not limited to event occurrence (i.e. reward is delivered or omitted unexpectedly), but also includes the time of reward, as rewards elicit transient activations when they are delivered earlier or later than predicted, even though it is certain that the reward will eventually occur.
 
Moreover, dopamine neurons are depressed exactly at the time of the usual occurrence of reward when a predicted reward is omitted. The depression occurs even in the absence of any stimuli at the time of the omitted reward, indicating that the **depression does not constitute a simple neuronal response but reflects an expectation process based on an internal clock** tracking the precise time of predicted reward.  
<center>  <img  src=https://i.ibb.co/Qpm7tbc/sfegg.png width="500px"  />  </center>

#### Dopamine signal encodes model-based predictions
Standard model-free reinforcement learning occours through prediction errors derived from actually experienced outcomes.
However, individual also elarn about contexts, rules and task structures, called **models** of the world (cognitive map).

Knowledge derived from models can deeply affect the prediction in the neuronal prediction error computation, resulting in a more appropriate teaching signal, and so an enhanced learning.

Probably, the acquisition and updating of these models involves cortical signals (OFC) rather than dopamine ones. Dopamine responses seems to incorporate the predictive information from model once they're established.

*Experiment*: in a study, sequences of non-rewarded trials lead to higher reward probability with non-rewarded trials.
<center>  <img  src=https://i.ibb.co/hdw6H0T/trial.png width="500px"  />  </center>

The task was a memory-guided saccade task with four possible target positions, but reward was given to only one of these positions. A cue stimulus indicated the saccade goal. The task included consecutive sub-blocks of 4 trials each, with one trial for each direction. Within a sub-block, one out of four directions was associated with reward (reward probability $25\%$), while the other three directions were not rewarded. 

The task induced a specific profile of reward probability in relation to the preceding trials. The **probability of reward increased with the number of previous non-rewarded trials** (PNR, post reward trial number). 
Reward probability was the lowest ($p = 0.0625$), if the preceding trial was rewarded (PRN: 1). In contrast, reward probability was the highest ($p=1.0$), if six preceding trials were not rewarded (PRN: 7). 

Thus, the animal's reward prediction (e.g., reward expectancy) should increase after each unrewarded trial. As a consequence, positive prediction error (reward delivery) should decrease, and negative prediction error (reward omission) should increase after each non-rewarded trial. In line with this reasoning, dopamine neurons show decreasing activations to reward delivery (red line), and increasing depressions to reward omission (blue line), as the number of non-rewarded trials increases. 
<center>  <img  src=https://i.ibb.co/9WB8ZY9/trial.png width="300px"  />  </center>

Due to increasing reward prediction, later reward delivery induces increasingly weaker positive prediction errors, and reward omission elicits stronger negative prediction errors. In contrast, model-free reinforcement learning would only consider the past unrewarded trials and hence generate progressively decreasing reward prediction and an opposite, increasing pattern of prediction errors. 

The observed dopamine prediction error responses are not fully explained by the previous experience with reward (model-free learning) but incorporate predictions from the task structure (model of the world). 
Thus **dopamine neurons process prediction errors with both model-free and model-based reinforcement learning**. 

*Note*: in this task the animal is not deciding, but just moving.

*Experiment*: rat can learn model of environment (cognitive map, environement representation) and use it to plan flexibility. The rat was trained to find a food source located with a light. Then it was placed in the same starting position of a new maze, with the usual route blocked.

If the rats had formed only state-action associations, where behaviors were or were not reinforced (a policy), they would not have a spatial map to guide them and they would likely choose the path most similar to the one that had originally lead to food. 

In contrast, if the rats had formed something like a mental map of the original maze, they would know that the food was ahead and to the right, and should choose a path, which pointed in that direction. And this is exactly what the majority of them they did.

## Value systems
Humand and animal decisions are not governed by single unitary control, but rather by multiple valuation systems, which are sometimes in agreement, but often in conflict.
There are three values systems that enable organisms to use previous experience to predict biologically significant events, and select appropriate behaviour.
<center>  <img  src=https://i.ibb.co/W5wsY0R/gdsgav.png width="500px"  />  </center>

These systems can operate in the domain of rewards (*appetitive outcomes*) and punishments (*aversive otucomes*).

The distinction between model-free and model-based reinforcement learning algorithms corresponds to the distinction psychologists make between habitual and goal-directed control of learned behavioral patterns. 

Habits are behaviors triggered by appropriate stimuli and then performed more-or-less automatically. Goal-directed behavior, is purposeful in the sense that it is controlled by knowledge of the value of goals and the relationship between actions and their consequences. 

Habits are controlled by antecedent stimuli, whereas goal-directed actions are controlled by their consequences.

*Note*: with these three systems correspond a specific pathway in the brain. 

### Pavlovian system (stimulus-outcome associations)
Certain environmental events trigger innate reflexive behaviours, that provide an adaptive response to environmental challenges. Pavlovian system is a mechanism by which an animal can learn to make prediction about when and where biologically significant events are likely to occour, in particular to learn which stimuli tend to precede them.

Pavlovian cues allow the organism to predict and prepare behaviour in anticipation of behaviourally significant events, rather than responding in a reactive manner.
Although adaptive in many circumstances, Pavlovian behaviours are inflexible and stereotyped.

### Habitual systems (stimulus-response associations)
Habitual system learns associations between stimuli and responses. 
Such stimulus-response association are shaped by a reinforcement rule so that stimulus-response links leading to satisfaction are strengthened, whereas stimulus-response links leading to discomfort are weakened. 

Habitual system can learn, through a process of trial-and-error, a large number of actions, as long as sufficient training is provided and the environment is sufficiently stable. It works simply by repeating actions that were previously successful (satisfactory).

However, such a mechanism is incapable of evaluating novel actions.

It's model based, extremely flexible but expensive and prone to error at beginning.

### Goal-directed systems (action-outcome associations)
The goal-directed system chooses actions based on the expected value of the outcomes associated with those actions (need to know if the action is followed by an outcome and if I like/want it at the moment). 

A choice is goal directed if it depends on a representation of the action outcome contingency (i.e. knowledge that lever-pressing produces food) and on the outcome as a desired goal or incentive (that food is valuable). Otherwise it is seen as the product of some other influences, such as habitual or Pavlovian. 

A key basis for distinguishing goal-directed and habitual behaviors experimentally is examining whether organisms can flexibly adjust their actions following a change in the reward value of an associated outcome. 

*Experiment*
First, a hungry rat learns to lever-press for food. After, the rat is fed to satiety with the food (devaluation), in the sense that the rat will not eat it if presented. 
<center>  <img  src=https://i.ibb.co/KWtJjng/gdsgav.png width="500px"  />  </center>

In the test, the rat is offered the chance to work again on the lever associated with the now-devalued food (like an all-you-can-eat):
* If behavior were controlled by a goal-directed system, then animal would correctly decide not to press the lever (I don't need food anymore);
* If behavior were controlled by a habitual system (i.e. by past satisfaction upon pressing the lever, not current value of the food), the animal would decide to press the lever (I press for habit, like binge-eating).
 
The goal-directed system updates the value of an action as soon as the value of its outcome changes, whereas the habit system does not. 
Ultimately, the stimulus-response link will be unlearned (by new experience showing that the lever-press no longer produces satisfaction), but initially the mechanism will produce inappropriate behavior (habit).

**What determines which behaviour is observed after outcome evaluation?** One key-factor is the amount of training prior to devaluation. If animals are moderately trained on the task they maintain devaluation sensitivity, if they're over-trained their behaviour can become insensitive to devaluation, suggesting a shift from goal-directed to habital during the learning. 

### Methods for outcome revaluation
<center>  <img  src=https://i.ibb.co/QpPxSkW/asdada.png width="500px"  />  </center>

#### Difference between model-free and model-based decision strategies
*Experiment*: a rat navigates a maze with different outcomes at different end points. The rat starts at state $S_1$ and must choose either left or right. It must choose again at either $S_2$ or $S_3$, to turn left or right to harvest one outcome.
<center>  <img  src=https://i.ibb.co/qxHd5Tx/model.png width="400px"  />  </center>

There are two strategies to solve the sequential action selection problem:
* By learning a **model of the environment** (consisting of a state-transition model and a reward model, essentially a state–action–outcome tree), the rat can decide whether to turn L or R at $S_1$ by searching through the tree (simulating its next action choices) and finding the path with the highest overall utility. Crucially, the current motivational state of the rat defines the relevant mapping between outcomes and utilities (numbers in boxes), such that when hungry (yellow), the rat will find choice L optimal at $S_1$, but when thirsty (blue), it will prefer R. **Behavior is thus goal-directed**;
* By contrast, a **model-free strategy** relies on stored (cached) values in common currency for state–action pairs. These action values are estimates of the highest return the rat can expect for each action taken from each (nonterminal) state. Action selection simply involves choosing the action with the greatest cached value at the current state. Because the values are divorced from the identities of the outcomes produced by different actions, changes in the outcome–utility mapping (due to different motivation state, hunger or thirst) cannot be translated into appropriate changes in values.

However, the motivational state (hunger, $H$) can be stored as part of the state representation. In this way, action selection can be modified to match a different motivational mapping (e.g. relevant to thirst, $T$) if the set of (state, action) values relevant to that state $\{(T;S_1,R),(T;S_2,L),. . .\}$ has previously been learned.

Generally, when the environment of a model-free agent changes the way it reacts to the agent’s actions, the agent has to acquire new experience in the changed environment during which it can update its policy and/or value function. 

For a **model-free agent** to change the action its policy specifies for a state, or to change an action value associated with a state (or both), it has to move to that state, act from it, possibly many times, and experience the consequences of its actions.

A **model-based agent** can accommodate changes in its environment without this kind of "personal experience" with the states and actions affected by the change. A change in its model automatically (through planning) changes its policy.

### Actor/Critic architecture in the brain
The (external or internal) environment provides two signals to the system:
* $S$, indicating the current state or stimuli; 
* $r$ indicating the current reward. ù

The Actor comprises of a mapping between states $S$ and action policies $\pi(a|S)$ (through modifiable weights or associative strengths). Its ultimate output is an action which then feeds back into the environment and serves to (possibly) earn rewards and change the state of the environment.

The Critic comprises of a mapping between states $S$ and values $V$ (also through modifiable weights). The value of the current state provides input to a temporal difference (TD) module that integrates the value of the current state, the value of the previous state (indicated by the feedback arrow) and the current reward, to compute a prediction error signal. This signal is used to modify the mappings in both the Actor and the Critic.

<center>  <img  src=https://i.ibb.co/vd0PzQH/actor-critic.png width="500px"  />  </center>

In the Actor/Critic architecture the Critic stores and learns state values and uses these to compute prediction errors, by which it updates its own state values. 
These same prediction errors are also conveyed to the Actor who stores and learns an action selection policy. The Actor uses the Critic’s prediction error as a surrogate reinforcement signal with which it can improve its policy. 

In this particular division of labor, the “environment” sees only the output of the Actor, (i.e. the actions), however, rewards from the environment are only of interest to the Critic.

*Experiment*: free choice.
To explore Actor/Critic architecture in humans, *functional magnetic resonance imaging* (fMRI) data were collected from participants performing an instrumental and a Pavlovian conditioning tasks. The instrumental task was composed of two trial types: reward and neutral.

In the reward trials, participants had to choose between one of two stimuli: 
* One associated with a high probability (HP) of obtaining a juice reward (on 60% of occasions); 
* The other with a low probability of obtaining a juice reward (on 30% of occasions). 

In neutral trials, participants had to choose between two other stimuli associated with either a high (60%) or low (30%) probability of obtaining a neutral (unrewarding) solution.

The Pavlovian task was identical to the instrumental task (with both reward and neutral trials), except that the computer made the selection and the participant’s task was to indicate which stimulus had been chosen by the computer.

*Results*
* Participants found the fruit juice to be significantly more pleasant than the control tasteless;
* Participants chose the high-probability action significantly more often than the low-probability action in reward trials;
* In the second phase of the experiment, participants were faster to respond during reward trials than neutral trials. This provides a behavioral measure of learning, providing some evidence that participants did acquire the Pavlovian associations.

After the subtraction of the neutral condition in the fMRI we can see two main brain areas activated:
* **Dorsal striatum**: prediction error only in instrumental task;
* **Ventral striatum**: prediction error in both Pavlovian and instrumental task.

<center>  <img  src=https://i.ibb.co/8BV630N/actor-critic.png width="500px"  />  </center>

*Experiment*: forced choice, no alternatives.
<center>  <img  src=https://i.ibb.co/6sPbYqk/monkey.png width="500px"  />  </center>

Reference trials did not present the monkeys with a meaningful choice, and the particular prediction error reported by dopamine firing on presentation of an image simply corresponds to its associated reward probability. Monkeys adopted the common suboptimal choice strategy of **probability matching**, pursuing richer and poorer options in rough proportion to their relative worth. 

This behavior was fortuitous because it allowed Morris et al. (2006) to record the activity of dopamine neurons on decision trials in which the monkey ultimately chose either the richer or the poorer option. The comparison of one with the other, and with the firing patterns from the single-image reference trials, provides a window onto the decision process.

The central finding is that a **burst of dopaminergic responding at the outset of a decision trial nearly instantly reflects the average reward associated with the option that will ultimately be chosen**, even though the monkey cannot actually submit its decision until some seconds later. 

Indeed, the neural response to the presentation of a pair of images is nearly the same in average.
<center>  <img  src=https://i.ibb.co/sHfddZ8/boh.png width="500px"  />  </center>

There are three main possibilities:
* The first option (values are averaged over the choices $V_i$) would have been expected under the so-called actor-critic algorithm, which posits that a "critic" with no knowledge of the actions can track the average value of states; these values can, separately, be used as rewards to train an ‘actor’ that makes choices. 
* The second option, Q learning, in which the prediction error associated with a decision is determined by the Q value of the better option rather than the one actually chosen. This is a very clever idea, as it **decouples learning from the actual choice and allows optimal behavior to be acquired while exploring suboptimal alternatives**. However, this is evidently too clever for the dopamine cells, whose activity follows the reference activity for the action actually chosen. 
* The third option is the class of algorithms that acquire Q values using a prediction error that reflects the value of the chosen option. It is these so-called SARSA (state-action-reward-state-action) algorithms, that this study favors.

**Graphs in the red rectangle**
* **Top**: dopamine responses to conditioned stimulus in reference (empty circles) and decision (filled circles) trials, as a function of the action value (defined as the average probability ofreward following each action). 
* **Bottom**: dopamine responses to reward delivery in the rewarded decision trials.

### Why should the brain use two different controllers in parallel?
If the brain uses two controllers, how can it arbitrate between the two when they disagree? It has been proposed that the brain relies on a controller of each class in circumstances in which its predictions tend to be most accurate.

The brain might estimate this accuracy for the purpose of arbitration by tracking the relative uncertainty of the predictions made by each controller (when there is most variance in the prediction I can calculate the uncertainty).

One class of controller involves **model-free** approaches such as temporal-difference learning, which reflects the activity of dopamine neurons and their dorsolateral striatal projections. The other class involves **model-based** methods, which we has been identified with the prefrontal cortex system.
<center>  <img  src=https://i.ibb.co/0K1LLDp/boh.png width="600px"  />  </center>

Model-free learning (cached values) is computationally simple but comes at the cost of inflexibility: action and values are divorced from the outcomes themselves and so do not immediately change with the re-valuation of the outcome.

By contrast, model-based reinforcement learning method constructs predictions of long-run outcomes, not through cached storage, but rather on the fly. This involves exploring a branching set of possible future situations, a method also known as *tree search*. Search in deep trees can be **expensive in terms of memory and time** and can also be **error-prone**. However, that the predictions are constructed on the fly allows them to **react more quickly** to changed circumstances, as when outcomes are re-valued.
<center>  <img  src=https://i.ibb.co/V2nrLdM/bnhbvkhb.png width="400px"  />  </center>

**Early** in learning the planning process of a **model-based** system is **more trustworthy** because it chains together short-term predictions which can become accurate with less experience than long-term predictions of the model-free process (less sensitive to devaluation). 

But with **continued experience**, the **model-free process** becomes **more trustworthy** because planning is prone to making mistakes due to model inaccuracies and short-cuts necessary to make planning feasible, such as various forms of tree-pruning: the removal of unpromising search tree branches (less sensitive to devaluation).  

According to this idea one would expect a shift from goal-directed behavior to habitual behavior as more experience accumulates.
