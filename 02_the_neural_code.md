# The neural code
The brain has a general specialized structure. The mechanism behind cognition, neuroscience and brain anatomy inspired biologically AIs to modelling intelligent functions.

## The brain anatomy
The central nervous system (CNS) is organized into four parts:
* Spinal cord;
* Brain stem;
* Cerebellum;
* Cerebrum.
<center>  <img  src=https://i.ibb.co/WPrZ4Yn/Cattura.png  width="400px"  />  </center>

The Peripheral Nervous System (PNS), it's the set of sensory cells that are located over the body and are needed to send information to the CNS.

### Cerebrum
The cerebrum is the most central part, divide into four regions:
* **Occipital lobe**: in the back of the head, for visual processing;
* **Parietal lobe**: in the upper part of the brain, for somatosensory processing and multisensory integration;
* **Frontal lobe**: in the front of the head, for motor control and planning;
* **Temporal lobe**: on the side of the brain, for auditory processing and language comprehension.
Moreover, in the inside there is the **limbic lobe** that handle emotional processing.
<center>  <img  src=https://teenbraintalk.files.wordpress.com/2017/02/four-lobes-of-the-brian.jpg?w=640  width="600px"  />  </center>

The brain is also divided in two different hemispheres, that commuicate through the **corpus callosum**. Each hemisphere deals with specific specialized functions.

Some other components are:
* **Corticospinal tract**: is a white matter motor pathway starting at the cerebral cortex that terminates on lower motor neurons and interneurons in the spinal cord, controlling movements of the limbs and trunk;
* **Somatosensory system**: a complex system of sensory neurons and neural pathways that responds to changes at the surface or inside the body. The axons of sensory neurons connect with, or respond to, various receptor cells. These sensory receptor cells are activated by different stimuli that carries information;
* **Auditory and visual system**: sound and visual processing.

**Anatomical orientation**: divided into four main directions, dorsal, ventral, caudal, rostral, but since we are on two feet the definition can be ambigous, so we use mostly orientation planes.
<center>  <img  src=https://s3-us-west-2.amazonaws.com/courses-images/wp-content/uploads/sites/102/2016/03/29181203/Anatomical_Directions.png  width="400px"  />  </center>

**Brain size and evolution**: since the first hominids the size of the brain increased, but the structure became more complex too, with more convolutions and folds. Folds provide a larger surface (cortex) in the same space.

### Artificial neural networks
Computing systems vaguely inspired by biological neural networks.
Each node - an artificial neuron - losely models a biological neuron, while each connection models a synapse, allowing communication between nodes.
Each artificial neuron can receive signals, and in turn send signals when threshold is reached.
These neurons are aggregated into functional layers like in human brains.
Neural networks learn: they can be trained to learn an association between an input and a result. This association can be stored to inform next associations. Any discrepancy, from the expected previous association, represents an errir which will be used to adjust the prediction.
Propagation functions regulates the way the neural nodes communicate: we have mostly feedforward, but also recurrent networks (bayesian learning).

### Neurons
The neuron is a discrete cell and is the primary computational unit of the nervous system.
Our bodies are composed of trillions of cells, enclosed by a membrane. Neurons are special types of cells, responsible for rapid communication between sensory cells, muscle cells and the brain.
Neurons have same structure of other cells, but they're specialized to send and receive messages, as electrochemical processes.

There are three main processing types:
* **Sensory**: from PNS to CNS;
* **Motor**: from CNS to PNS;
* **Interneurons**: located within CNS. They can be local (form circuits with nearby neurons) or relay (connect different circuits of local neurons). Relay neurons are essential for learning, perceiving, deciding etc...
<center>  <img  src=https://ib.bioninja.com.au/_Media/types-of-neurons_med.jpeg  width="600px"  />  </center>

There are three main anatomical types:
* **Bipolar**: one axon, one dendritic tree. Usually sensory;
* **Unipolar**: one stalk that splits, both outside the CNS with dendrites, and inside the CNS with terminal buttons. Usually sensory;
* **Multipolar**: one axon, many dendritic trees, most common in CNS.
<center>  <img  src=https://qbi.uq.edu.au/files/27928/types-of-neurons-QBI.jpg  width="600px"  />  </center>

#### Neural structure and activity
1. Dendrites receive information, they're covered in synapses;
2. The mebrane under the synapse has many receptors that detect neurotransmitters in the synaptic cleft;
3. Most dendirtes have spines, specialized structures that form one half of a synapse;
4. The soma integrated information;
5. The axon carries information (like a wire);
6. Axon differ from the soma since no protein synthesis take place here;
7. The terminal buttons (axon terminals) pass on the information;
8. The terminal buttons contain numerous small bubbles of membrane called synaptic vescicles, to attach to spines of other neurons;
9. Terminal buttons also contain numerous mitochondria, which indicates high energy demand.

So we have dendrites as input, soma for integration, axons for action potential propagation and terminal buttons as output. 
<center>  <img  src=https://images.saymedia-content.com/.image/t_share/MTc0MjM1NjA2MDg2MzI5ODUy/structure-of-a-neuron.png  width="600px"  />  </center>

**Dendrites and synaptic plasticity**: the formation of new and the removal of old spines is a near continuous process. It is hypothesized tha spine density underlies many behaviours, such as learning, memory and motivation.
Some connections are dominant and building up new connections is a challenge (maybe be i.e. stimulated by traumas).

**Soma**: it behaves like a signal processor. After a while of learning, a certain activity is done faster by the neuron. Inside the soma we found:
* **Cytosol**: intracellular fluid present inside the cells;
* **Organelles**;
* **Cytoplasm**: everything in the cell except the nucleus; 
* **Nucleus**: it contains DNA, and it's specific pattern is called gene expression. The product of gene expression is protein synthesis. The mRNA carries genetic informations to sites of protein synthesis in cytoplasm (proteins are assembled from amino acids). This process is called *translation*.

**Cytoplasm**
* Rough endoplasmic reticulum (ER): major site of protein synthesis;
* Smooth endoplasmic reticulum: site of lipid production, regulates internal concentration of substances;
* Golgi apparatus: sorts proteins and produces lysosomes that break down wastes;
* Mitochondrion: main energy source for the cell.

## The electrochemical brain
Dynamic properties of neurons are derived from the fact that brain is awash with electrically-charged chemicals that exert pressures on each other.
Intracellular and extracellular fluid is like seawater (a way to set a level of energy).
It's made up of atoms and molecules with net electrical charge.
Note: cations positively charged ions, anions negatively charged ions.

The membrane is a phospholipid bilayer, that is relatively impermeable. On it there are:
* **Ion channels**: gated-channel that can open and shut depending on the charge of the membrane, allowing some chemicals to pass through;
* **Ion pumps**: made of conjoined proteins, exchange one chemical for another.

There are two factors that influence the movement of ions:
* **Diffusion**: natural tendency for ions to disperse from high concentration to low concentration;
* **Electrostatic pressure**: force that causes oppositely charged ions to attract each other and viceversa, like magnets.

These forces (balanced in rest state) contributed by these ions give rise to the membrane potential:
* **Sodium** Na+ and **Chloride** Cl- that are mainly outside the cell;
* **Potassium** K+ that is mainly inside the cell;
* **Organic anions** A- that is *only* inside the cell.

### The axon membrane
At rest state, potassium K+ is found mostly inside the cell.
Diffusion would tend to push it out, but the outside of the cell (external membrane) is relatively positive and so the electrostatic pressure keeps it inside the cell.
At rest state, chloride Cl- is found mostly outside the cell.
Diffusion would tend to push it inside, but the inside of the cell (internal membrane) is already negatively charged and so the electrostatic pressure pushes it outside the cell.
<center>  <img  src=https://i.ibb.co/F65bGWH/1.png  width="600px"  />  </center>
At rest state, sodium Na+ is found mostly outside of the cell.
Both diffusion and electrostatic pressure would tend to push it inside the cell, but a third force, the sodium-potassium pump pushes the sodium Na+ out.

Being this pump asymmetric from the point of view of electrical charge, it turns out that the inside of the cell is negatively charged with respect to the outside and this difference of potential, called membrane (resting) potential, can be measured and it is almost $-70 mV$.
This potential is experimentally measured on giant squid axons (about half a millimeter) with a pair of electrodes. The potential refers to a stored-up source of energy.

A message travelling along an axon takes the form of a sudden change in this potential.
The basic currency of the electrochemical brain is the action potential (nerve impulse or spike), and it's the main facilitator of communication within and between the neurons.

### The action potential
To send a signal we have to cause a *depolarization* of the membrane. If it's too weak, it will start but it won't propagate: if the stimulus is at or above a certain threshold the action potential is triggered.
When it happens the membrane potential is suddendly reversed and the inside of the cell becomes positively charged (wrt the outside) and it's about $+40 mV$.
<center>  <img  src=https://i.ibb.co/cCQQsqJ/fva.png  width="400px"  />  </center>

There are two main kind of conduction:
* **Unmyelinated**: when a depolarizing stimulus is applied, an action potential is triggered. The magnitude of the action potential does not change, once it occours remains the same size even if it splits along different axons;
* **Myelinated**: in vertebrates most axons are myelinated (surrounded by myelinating glia, a layer of fat called *myelin sheat*), and there are gaps at regular intervals, called *nodes of Ranvier*. Magnitude of the AP does increase, the ions that need to be exchanged to fuel it cannot penetrate the sheat. The AP is regenerated at the nodes of Ranvier, hence we have a *saltatory conduction*.

**Pit-stop analogy**: every stop takes time but the car doesn't have to carry as much as fuel and therefore it travels faster. So, the saltatory conduction is economic and fast (like smoke signals).

## Neural coding
As a neuron can fire an action potential that has a definite value in magnitude, one can ask on what the threshold is based on, how the neuron can tell if a stimulus is weak or strong.
The variable took into consideration is the *rate of firing*: to a faster firing is related a more intense stimulus and viceversa.
Anyway, the rate cannot exceed a thousand firing per second, being the re-fractory period of $1 ms$ (computational capacity of the brain). The summation across neurons allows for a great range of stimulus levels to be encoded.
<center>  <img  src=https://i.ibb.co/L82V0j7/gfdssgbs.png  width="500px"  />  </center>

### Synaptic transmission
It's the way in which communication takes place between one neuron and another (linking between terminal buttons and spines). Can be electrical or chemical, and it's composed in three main parts:
* **Presynaptic** (terminal button): we can found mithocondria and vescicles that envelope neurotransmitters (NT);
* **Synaptic gap or cleft**: they're not physically attached, but there is extracellular fluid, in which the neurotransmitters diffuse;
* **Postsynaptic**: there are NTs receptors and ion channels. This stage can determine if the neuron fires or not (channels and receptors can stay closed for some reasons).

Generally the're one way (*prodromic*) but in some cases they can work on reverse.

**Release of a neurotransmitter**
When the action potential (AP) reaches the button, the voltage-dependent ion channels open. Hence, the calcium ions $Ca^{2+}$ enter and bind with the proteins, causing the vescicle to dock with the membrane.
Finally, vescicle opens and NTs are released (*exocytosis*).
<center>  <img  src=https://i.ibb.co/hs0Yx09/agbfdgvbzdafbg.png  width="600px"  />  </center>

Different receptors respond to different NTs. There are two main types of postsynaptic receptors:
* **Ionotropic** (excitatory): exterior portion contains binding sites for specific NTs. When the NT binds the channel opens, and the movement of ions changhes the charge across the membrane, propagating the potential;
* **Metabotropic** (inibitory): it's more complicate and indirect since it requires a second messenger. It leads to anatomycal changes and allows slower and more long-lasting effects (modulation).

**Post-synaptic potentials**
The two different kind of receptors lead to two types of potentials:
* **Depolarization**: excitatory post synaptic potentials (EPSPs), more positive;
* **Hyperpolarization**: inhibitory post synaptic potentials (IPSPs), more negative;

The process that occours depends on which NT-gated ion channels are activated:
* Glutamate: predominant excitatory NTs in the CNS;
* GABA: NTs released by inhibitory interneurons.

So, it's possible to influence the postsynaptic neurons with molecules (fire or not fire).

**Post-synaptic integration** 
Most CNS neurons receive thousands of synaptic inputs, that activate different combinations of ionotropic and metabotropic receptors. All incoming information is integrated by the cell with one result: AP or not AP. 
The rate of firing is determined by the relative excitatory-inhibitory activity at the synapses (activity counteraction, AP depends on the balance).

The integration depends on the level of plasticity of the system too.
Post-synaptic neuron is excited or inhibited depending on the precise combination of inputs:
* Excitatory or inhibitory NTs;
* Spatial and temporal summation.

Summation, which includes both spatial and temporal summation, is the process that determines whether or not an action potential will be generated by the combined effects of excitatory and inhibitory signals, both from multiple simultaneous inputs (spatial summation), and from repeated inputs (temporal summation). Depending on the sum total of many individual inputs, summation may or may not reach the threshold voltage to trigger an action potential.  

## Oscillatory fluctuations in the membrane potential
Neurons are never truly at rest, individual depolarizing events happen at all times and they add together in a cascade of events from synapse to synapse.
If many signals arrive at the same time, the aggregate effect of the depolarization will be much larger that if the same number of depolarizing signals arrive at different times (temporal summation).
Hyperpolarization contributes to the fluctuation of the membrane potential as well.

The final result is an ongoing fluctuation between depolarization and hyperpolarization in the dendritic membrane potential, that can be measured with electrodes in the extracellular space.
Given the high density of neurons that contribute to this fluctuation, what is recorded is actually the local field potential (LFP), that is the local region of cortex where dendrites are located (ensemble of neurons).

Despite the hundreds of thousand of individual channels, the LFP is often observed to fluctuate in a orderly oscillation.
Oscillations are so typical of the brain activity that they have been given names (they're typical of the biological systems in general).
Even if it's actually debated, oscillations seems to be associated with specific functions.
<center>  <img  src=https://ars.els-cdn.com/content/image/1-s2.0-S0301008220301337-gr1.jpg  width="600px"  />  </center>

**How can the brain orchestrate individual single channel events into a steady predictable up and down rhythm?**
The way neurons are wired up facilitate the oscillatory behaviour (brain mapping). In many pyramid cells, inhibitory input from interneurons tend to synapse near the base of the dendrite or even the soma, acting as a gate that allows or not depolarization (organized cluster of information).

Moreover, inhibitory interneurons tend to be wired to each other creating synchronized loops via axonal connections in addition to sending signal to pyramid cells. As a consequence, pyramid cells tend to receive *synchronized hyperpolarized activity*, facilitating rhytmic fluctuation on membrane potentials (organized and synchronized cluster of information).

For example, a consequence of, say receiving a synchronized delivery of hyperpolarizing GABA 40 times per second, is that the membrane potential of a pyramid cell will not actually remain at the steady -70mV but, more realistically, it will oscillate between $-90 mV$ and $-50 mV$.
Given that neuron is much more likely to fire when the threshold is at around $-50 mV$ than $-90 mV$, pyramid neurons have 40 windows per second in which they can fire.

There are two mechanism to maximize the actual and effective firing:
* Time the delivery of its own action potential during a depolarization phase of the membrane oscillations (at around $-50 mV$);
* Receive most depolarizing inputs from neighbour neurons at the same time to maximze chances to optimally depolarize and fire.

Synchronized activity of the membrane oscillations in different clusters of neurons is a critical factor in the smooth operations of the brain. 
At a local level there is a degree of synchrony between interneurons and pyramid cells, while across regions, oscillatory synchronization of ensembles neurons in necessary (and not guaranteed) for effective communication.

Synchronization between different parts of the brain is referred to as *phase synchronization*.

### Electroencephalography
It's a neuroscience's tool to measure oscillatory electrical activity in the human brain in a non-invasive way (at the level of the scalp).
* In 1875, **Richard Caton** studied electrical phenomena on the exposed cerebral hemispheres of rabbits and monkeys;
* In 1890, **Adolph Beck** investigated the spontaneous electrical activity of the brain of rabbits and dogs, in particular rythmic oscillations altered by light. He placed electrodes directly on the surface of the brain to test sensory stimulation and his observation of fluctuating brain activity led him to the conclusion of brain waves;
* In 1912, **Vladimir Pravdich-Neminsky** first succeded in study the first animal EEG, evoking a potential in the dog;
* In 1924, **Hans Berger** first recorded human brain waves, and in 1929 he first observed the alpha waves in the back of the brain. He's considered the father of EEG.

Differently from the electrocorticography (ECoG), which is an invasive tool as it must be placed under the skull, the EEG is made up of electrodes which are placed directly on the surface of the skull (neurons are far frome the surface, hence an amplifier is needed).

The EEG does not measure neither the AP nor the summation of APs, but it measures the summation of *post-synaptic potentials* (PSPs), that results from the combined activity of a large number of similarly oriented pyramidal neurons and requires synchronous activity between those cells.

EEG is used to find an *event related potential* (ERP), a recorder signal which can be associated to a conscious event (responde to stimuli).
Being the brain never at rest, its activity always produces some kind of background noise (EEG is never flat) which, however, almost annihilate itself, however, when a potential is synchronously fired between pyramid cells of the same area, the EEG can record a considerable anomaly in this background noise, resulting in a peak (and, eventually, in a subsequent bottom peak) in the PSPs.

**The alpha rhythm**
It was traditionally assumed that synchronous neural activity generating the alpha rhythm is associated with areas of the cortex that are not processing information (rest or idle state). This is wrong, alpha waves are associated with active inhibitory processes. 
