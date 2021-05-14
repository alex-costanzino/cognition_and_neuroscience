# Neural mechanisms of selective visual attention
In any moment, our visual system receives an overwhelming amount of information, but only a part of the total visual input can be used in the control of the behaviour. This happens due to our extremely limited capacity of visual processing and the high energy cost of neuronal activity.

Selective visual attention describes the **tendency to selectively process only a subset of sensory input** (i.e. only attended stimuli controls the behaviour), and is one of the most fundamental cognitive functions, for humans and other primates, whom vision is the dominant sense.

*Example*: change blindness. Observers fail to notice large changes to visual scenes when the change coincides with a brief visual disturbance. 

## Vision
Vision is the sense we most depend on in our daily lives.
It's used for:
* Object recognition;
* Guide movements.

These separate functions are mediate by at least two parallel and interacting pathways.

Vision is often incorrectly compared to the operation of a camera, but visual perception is actually an active and inferential process, that involves more than just the information provided to the retina: it's based on a generative model that actively predicts and explains sensory inputs based on past experiences (bayesian brain hypothesis).

### Hierarchy
Vision is **hierarchical**, it depends on processing the input signals through multiple stages of the visual pathway: visual input is first transduced in the retina, then conveyed through the thalamic nuclei (LGN), to the primary visual cortex (V1).

Then, cortical projections go forward from the primary visual cortex V1, to:
* Areas in the parietal lobe (*dorsal pathway*), concerned with visually guided movements;
* Areas in the temporal lobe (*ventral pathway*), concerned with object recognition.
<center>  <img  src=https://i.ibb.co/986DWFR/photo-2021-05-07-17-00-48.jpg  width="400px"  />  </center>

Vision is highly disturbed: the various object features (i.e. motion, depth, form, etc...) are experienced as unitary percept. The subjective unity is although achieved by multiple systems in the brains (distributed processing).

Information about each visual hemifield is processed in the contralateral visual pathway.

The axons of the retinal ganglion cells form the optic nerve, that extends to a midline crossing point, the optic chiasm.  
Beyond the optic chiasm, fibers from the temporal hemiretinas proceed to the ipsilateral hemisphere, whereas fibers from the nasal hemiretinas cross to the contralateral hemisphere.

Because the temporal hemiretina of one eyes sees the same visual hemifield as the nasal hemiretina of the other, the decussation of fibers at the chiasm ensures that all the information about each hemifield is processed in the visual pathway of the contralateral hemisphere.
<center>  <img  src=https://i.ibb.co/Hxx2X7q/Cattura.png  width="400px"  />  </center>

At each stage of the processing hierarchy the neuronal response is governed by the receptive field (RF) properties of infividual cells. In the retina, LGN and V1, visual RFs have different properties and are measured in degrees of visual angles (they're like different layers of a neural network). 

### Receptive field (RF)
The term **receptive field** refers to the region of visual space where changes in luminance influence the activity of a single neuron. The RF of each neuron occupies a fixed retinal location, thus, when the eye moves, the RF moves a corresponding amount in visual space.
A given stimulus elicits the strongest response from the center of the RF, with response gradually declining as the stimulus is presented further away (bidimensional gaussian function).

The RF properties can be studied using single-unit extracellular recordings, with a fine-tipped metal electrode, inserted into the extracellular space. These signals are then amplified, filtered and analyzed. Since spikes (or APs) are all-or-none, most information is encoded in the brain as firing rate (i.e. number of AP in $1 ms$).
The primary goal of single-cell recording is to determine what experimental manipulations produce a consistent change in the firing rate of an isolated neuron.
The procedure is invasive, but guarantees high spatial and temporal resolution, and the possibility to differentiate excitation from inhibition.

<center>  <img  src=https://i.ibb.co/ky1vM9Y/Cattura.png  width="600px"  />  </center>

*Experiment*: monkey is required to maintain fixation and stimuli are presented at various positions in the visual field. The neuron fires vigorously only when the stimulus is presented in the upper-right quadrant of the screen.

Receptive fields are also hierarchical: each RF at one stage of the visual hierarchy is composed of input from many neurons of the previous stage, and the RF size increases along the visual hierarchy. Simple RFs are constructed from the convergence of LGN inputs with RFs aligned in visual space, complex RFs originate from the convergenve of simple cells with similar orientation preferences.

### Retinotopic maps
In early visual areas, the visual field is represented in retinotopic maps that preserve the spatial arrangments of inputs from the retina (**isomorphism**, neighbouring regions on the retina are represented in neighbouring regions on the higher levels). These maps are higly distorted since there is much more cortical tissue devoted to foveal rather than peripheral regions (**cortical magnification**). The amount of cortical area dedicated to inputs wrt each degree of visual space varies with eccentricity (**non-isometry**).

The central (foveal) part of the visual field commands the largest area of cortex (i.e. in V1 more cortex is dedicated to the central $10°$ of visual space than to all the rest). 

Spatial resolution varies systematically across the visual field, with the highest resolution at the focus of our gaze (at the fovea). The receptive fields for retinal ganglion cells that monitor portions of the fovea subtend approximately $0.1°$ (high resolution), whereas those in the visual periphery reach up to $10°$ (low resolution).

Cones are much more sparsely located in the periphery than in the center of the retina. More cortical space is dedicated to the central part of vision, where the receptive fields are smallest and the visual system has the greatest spatial resolution. Images presented in the periphery of a visual scene are processed more slowly and less accurately.

The central area, the fovea, is where vision (i.e., spatial acuity) is sharpest and corresponds to the center of gaze that we direct toward the objects of our attention. The density of photoreceptors, bipolar cells, and ganglion cells is highest at the fovea, thereby providing higher spatial resolution. A retinal ganglion cells near the fovea receives input from fewer receptors (mainly cones), covering a smaller area (smaller RF, higher resolution), while a ganglion farther from the fovea receives input from many more receptors (mainly rods), covering a larger area, hence ensuring a larger RF.

### Cells in LGN
RFs of retinal ganglion and LGN neurons are small ($<1°$), circular and with a center-surround organization. They can be:
* On-center, off-surround (light-sensitive);
* Off-center, on-surround (dark-sensitive).
<center>  <img  src=https://i.ibb.co/nncbLwJ/Cattura.png  width="500px"  />  </center>

They respond optimally to contrast, but are not selective for orientation.

### Simple cells in V1
In V1, neurons respond selectively to oriented bars or gratings. In simple cells. RFs have separate on/off subfields. Neurons have elongated RFs and respond to a narrow range of orientations, and different neurons respond optimally to distinct orientations. The orientation of the RF is thought to result from the alignment of the circular center-surround RFs of several LGN cells.
<center>  <img  src=https://i.ibb.co/yWFCy5w/Cattura.png  width="500px"  />  </center>

This selectivity is the first step in the brain's analysis of an object's form.

### Complex cells in V1
In complex cells on/off regions are superimposed, hence, every location in the receptive field responds both to white and black bars, and so, cells respond to lines or edges that traverses the RF along a prependicular axis (aperture problem).

Due to the lack of discrete on/off subfields, there is a constancy in the response to variations of stimulus (position invariance): they fire continuously as a line or edge stimulus traverses their RFs.
<center>  <img  src=https://i.ibb.co/z5QjNkf/Cattura.png  width="200px"  />  </center>

### Visual features
In addition to stimulus position, V1 neurons are selective for a number of attributes:
* **Orientation**: this selectivity must arise from computations that take place within cortex, because LGN responses are not selective for orientation;
* **Spatial frequency**: V1 neurons are typically sharply selective for the spatial frequency of a stimulus. Spatial frequency is best defined for a grating pattern, where frequency is the inverse of the distance between bars. This selectivity arises naturally from the shape of the receptive fields that have multiple on/off regions;
* **Direction**: cells in area V1 are commonly selective for direction of stimulus motion;
* **Temporal frequency**: is the inverse of the period between temporal oscillations between dark and light. V1 neurons typically prefer lower temporal frequencies than those that can drive LGN neurons; 
* **Disparity**: in animals with front-facing eyes, much of the visual field is covered jointly by both eyes. This poses a challenge as signals need to be integrated, but also an opportunity for computing binocular depth (stereoscopy). The signals from corresponding regions in the two eyes are kept separate in the LGN, and are combined in V1; 
* **Colour**: retinal ganglion cells respond along one of three cardinal directions (they're like colour channels). V1 neurons are also organized along cardinal directions.

The visual system use neurons with different RFs size to create a series of neural representations at different spatial scale (like a feature space).

Using *gratings*, at a sufficient low contrast, stimulus would appear uniform and unpatterned, while for higher constrast the pattern would be visible, hence there exists a contrast threshold.
Visual system contains sets of neurons tuned to different bar widths (sets of neurons channels).
Moreover, different spatial frequencies convey different information about a stimulus (i.e. in fusiform cortex, a visual area in the ventral pathway, neurons respond selectively to faces)

The *contrast sensitivity function* (CSF) describes how sensitive an observer is to sine wave gratings as a function of their spatial frequency. This is measured using a contrast detection experiment where one determines the minimum contrast to detect sine wave grating of different spatial frequencies.

If the sensitivity is high, the threshold is low. Humans are most sensitive for an intermediate range of spatial frequencies and less sensitive for both higher and lower frequencies.

### Neural models
* **Simple cells**: linear filtering (weighted sum of image intensities, weights from RFs) and then rectification (only part of the respones that is larger than a threshold is seen in the firing rate response);
* **Complex cells**: linear filtering by a number of RFs, rectification and then summation.
<center>  <img  src=https://i.ibb.co/4pWcZr0/Cattura.png  width="400px"  />  </center>

### Attention hierarchy
The brain analyzes a visual scene at three levels:
* **Low level**: local contrast and motion are discriminated;
* **Intermediate level**: uses low-level features to parse the visual image into surfaces and contours, to segregate of objects from background;
* **High level**: once a scene has been parsed, object is recognized (with ot without awareness) and it's matched with memories of shapes and their associated meanings.

### High-level visual processing
Beyond V1 lie the extrastriate areas, a set of higher-order visual areas that are also organized as neural maps of the visual field.
V1 constitutes the first level of cortical processing of visual information, and after activating area V1, visual information is transmitted over two major pathways:
* **Ventral pathway**: into the temporal lobe, carries information about what the stimulus is (object recognition);
* **Dorsal pathway**: into the parietal lobe, carries information about where the stimulus is (visuomotor integration).

All connections between cortical areas are reciprocal: each area sends information back to the areas from which it receives the input (feedback). This is an important feature of the connectivity between cortical areas.

The complexity of neural processing increases along each cortical pathway.
*Example*: V1 neurons respond to linear contrasts, V2 neurons respond to illusory contours, V4 neurons respond to the conjuction of elementary features (i.e. colour, shapes), IT neurons respond to complex stimuli (i.e. faces).

## Attention
There are two basic phenomenon that defines selective visual attwntion:
* **Limited processing capacity**: only a small amount of info available on the retina can be processed and used to control behaviour;
* **Selectivity**: ability to filter out unwanted or irrelevant information (one is aware of attendend stimuli and largely unaware of unattended ones).

Objects in the visual input compete for representation, attention biases competition toward information relevant to behaviour. Attended stimuli make demands on processing capacity, unattanded ones often don't.

**Competitive selection**: process that allows the neural representation with the highest signal strenght to control behaviour. 

The main two form of attention are:
* **Top-down** (endogenous, aware, volountary): selective visual processing due to an endogenously signal (i.e. instruction). Can be engaged explicitly to select one thing over another, as well as to follow a particular instructional set or general rule, but can be also guided by spatiotemporal regularities that are learned implicitly over time;
* **Bottom-up** (exogenous, unaware, automatic): selective processing that is generated by the physical properties of stimuli (i.e. brightness, colour, etc...). Allows novel or salient information to transiently interupted goal-directed behaviour.

Why the brain implements these mechanisms?
* Allow entrance of the selected perceptal inputs into the working memory and conscious perception;
* Move eyes toward the target (foveal analysis);
* Direct actions;
* Gate access of perceptual inputs to memory systems.

### Top-down visual attention
Competitive selection can be influenced by cognitive processes (top-down attention) through which task-relevant objects are selected by attention.

**Attentional template**: representation of the relevant object formed and held in the subject's working memory. It can be used to give a competetive advantage to those objects in the visual scene that match the description (creation of expectation).

We distinguish:
* **Object-based attention**: selection is based on non-spatial features (i.e. orientation, colour, shape, etc...);
* **Space-based attention**: selection is based on spatial location or direction.

Some kind of short-term description of the information currently needed must be used to control competitive bias in the visual system, such that inputs matching that description are favored in the visual cortex.
*Example*: you are given the task to attending and reporting the identity of a red stimulus. Following this instruction, a representation (attentional template) corresponding to the instruction is formed and mantained active in the working memory. The description serves to prime the cortical areas that encode red colour, such that the visual stimuli of this colour will be processed more efficiently and with priority wrt other colours.

There are two main paradigms to study attention:
* **Central cue paradigm**: used to examine space-based attention. Participant fixates on a central cross of a screen. Then a central informative cue is presented, indicating where the target is more likely to appear (correct $80\%$ of the times). **Target detection is faster and more accurate in the valid than in the invalid trials**
<center>  <img  src=https://i.ibb.co/3423pjV/agfdv.png  width="600px"  />  </center>

* **Feature parallel search** and **conjuction serial search**: employed for studying object-based attention. Participant is presented with a display that can contain a target stimulus amongst a variable number of distractor stimuli. Set size is variable and refers to the number of displayed items (distractors + target). The unique target is either present or absent. **Efficiency of search decreases as the similarity between target and distractors increases, and increases as the similarity among distractors increases**.
<center>  <img  src=https://i.ibb.co/Q8MXf4s/Cattura.png  width="600px"  />  </center>

The most efficient are searches  for a distinctive target amongst homogeneous distractors (pop-out target). In feature search, response times are independent of the number of distractors, while in conjuction search, response times increase linearly with the number of distractors.

### Neural correlates 
Selective visual attention increases visually-driven firing rates of neurons encoding the attending stimulus. This modulation is present as early as LGN and has been observed at nearly all levels along the ventral pathway of the visual system (V1, V2 and V4). There is also evidence that suggest that the magnitude of attentional enhancement increases as one ascends the visual hierarchy. Analogous modulatory effects of attention have been demonstrated in visual areas of the dorsal stream, such as MT and MST.

The study examined how **attention affected the orientation tuning of neurons in V1 and extrasriate area V4**. Monkeys performed a delayed match-to-sample task in which oriented stimuli were presented in the RF of the neuron. On some trials the animals were instructed to pay attention to those stimuli (inside RF) and on some other trials, they were instructed to pat attention to other stimuli (outside RF).
<center>  <img  src=https://i.ibb.co/28K4bgS/Cattura.png  width="400px"  />  </center>

Orientation-tuning curves were constructed from neuronal responses in two behavioural states: attendend and non-attended. Gaussians were fit to neuronal responses to twelve different orientations for each behavioural state.

Results showed attentional modulation of the amplitude of orientation-tuning curves in both areas V4 and V1 (with smaller effects), but there was little evidence for change in the width of tuning. The principal action of attention appeared to be a **multiplicative scaling of responses** (attention seems to work as a **gain factor**).
<center>  <img  src=https://i.ibb.co/VjqSD75/Cattura.png  width="500px"  />  </center>

Middle temporal area (MT) is crucial for perception of visual motion. MT neurons show direction tuning cuves (bell-shaped response profiles), depending on the direction of motion of the stimulus (on random dot pattern, a test for object-based detection).

Spatial attention modulates the responses of neurons selective to direction of motion in area MT and MST.
<center>  <img  src=https://i.ibb.co/Msxm582/Cattura.png  width="500px"  />  </center>

**Experiment 1: effect of spatial attention**
One RDP was presented inside the RF, while the other (distractor) was presented in the opposite hemifield. In a given trial, both RDPs moved in the same twelve possible directions.
The upper curve shows the response when the monkey was attending to the stimulus inside the receptive field, while the lower curve plots the responses when the monkey was attending to the stimulus outside the receptive field. This show an **increase in directional gain in the attended condition**.
<center>  <img  src=https://i.ibb.co/1L6dKyr/Cattura.png  width="600px"  />  </center>

**Experiment 2: effect of featural (non-spatial) attention**
The stimulus inside the receptive field always moved in the cell's preferred direction, the stimulus outside moved in either direction.

The first histogram compares responses of 131 cells to the stimulus inside the RF, when attention was on the preferred or anti-preferred direction outside the RF. The histogram is shifted to the right, indicating an **increased response when the stimulus moved in the cell's preferred direction**.

The second histogram compares responsed of cells to the stimulus inside the RF, when attention was on anti-preferred motion outside or the stimulus inside the RF. The histogram is shifted to the right, indicating an **increased response when the attended target was inside the RF**.
<center>  <img  src=https://i.ibb.co/9nh9bn9/Cattura.png  width="650px"  />  </center>

These results demonstrate a physiological correlate between the two kind of attention, by showing neuronal response modulations in the abscence of spatial shifts of attention.

Attending to a given direction: 
* Enhances the responses of neurons whose preferred direction aligns with the attended direction; 
* Reduces the responses of those neurons preferring the opposite direction.

Spatial-based and feature-based attention represent separate and summable processes that have a multiplicative effect on the neuronal respones.

Neuronal response modulations are not only obtained by manipulating the behavioural relevance of the stimuli, but enhancement effect can be achieved by changing stimulus contrast (non attentional, bottom-down effect).

Visual neurons typically produce increasing responses as a function of stimulus contrast, up to a plateau: the *constrast response function* (CRF) takes the form of an H-ration (sigmoid). It represents a sort of dynamic range.

Two alternative hypotheses can explain the effect of attention on the neuron response to a stimulus inside its RF:
* Hypothesis 1 - **response gain model**: the response is multiplied by a constant factor, and the effect of attention is maximum for the highest stimulus contrast. The CRF shifts upward;
* Hypothesis 2 - **contrast sensitivity gain model**: attention increases sensitivity to contrast, the effect of attention is macimum in the area of the curve where the response is most dynamic (steep, inflection point). The CRF shifts to left.
<center>  <img  src=https://i.ibb.co/Zd8FLP2/Cattura.png  width="600px"  />  </center>

#### Attention increases sensitivity of V4 neurons
*Experiment*: after the fixation cross appear in the center, two stimuli (sinusoidal gratings) are presented on the screen, one inside and the other outside the RF.
In separate blocks the animals paid attention on the stimulus inside (attend RF) or outside (attend away). The luminance of contrast was selected randomly from a set that spanned the whole dynamic range. 

It was so possible to compare neuronal responses to identical stimuli, with different attention (opposite hemifield).
<center>  <img  src=https://i.ibb.co/0QQqdZD/Cattura.png  width="600px"  />  </center>

Attention caused largest increases in firing rate to stimuli that were near the contrast-response threshold. Here, attention caused a $24\%$ increase in the average firing rate. As stimulus contrast increased, the effects of attention on the neuronal response decreased. 

The results support the hypothesis 2,  that **attention causes an increase in V4 neurons sensitivity but without substantial increase in the response to high-contrast stimuli**     . This increase in sensitivity is reflected in a leftward shift in the CRF. The largest changes in firing rate with attention were observed for stimuli that were within the dynamic range of the CRF.

#### Attention alters visual cortical receptive fields
Vision is limited by many factors, including the visual system spatial resolution (acuity), the ability to discriminate two nearby points in space.
This shifts in spatial attention results in enhanced visual processing at the attended location.

The idea that attention operates by changing the spatial selectivity of single neurons was suggested by **Moran** and **Desimone**, recording single V4 neurons in monkeys while they attended to one of two stimuli presented inside the RF:
* One of the two stimuli elicited a strong response from the neuron when presented alone (effective stimulus), while the other elicited a weak response when presented alone (non-effective stimulus); 
* When presented simultaneously (without attention) the response was an average;
* When attention was on one of the two stimuli, the response was primarily determined by the attended one: firing rate was enhanced when the preferred stimulus was attended, and reduced when the non-preffered stimulus was attended.

Neuron response is biased in favour of the attended stimulus, where influence of a unattended one was attenuated, as if the RF contracted arounf the stimulus.
<center>  <img  src=https://i.ibb.co/0Fy0XSq/Cattura2.png  width="600px"  />  </center>

*Note*: a red bar is an effective stimulus, while a green bar is ineffective (for V4).

#### Mechanisms of attention effects on receptive fields
Two input populations of neurons project to the neuron of interest (output neuron). 
* The input population responding to the stimulus preferred by the output neuron (purple) has predominantly excitatory connections (thick black line);
* The one responding to the non-preferred stimulus has predominantly inhibitory connections (thick grey line) to the output neuron. 

Attention strengthens the connections from the input population that responds to the attended stimulus, so that the response of the output neuron is dominated by the attended stimulus.
<center>  <img  src=https://i.ibb.co/mTMv3N7/uno.png  width="500px"  />  </center>

Attention changes the gain of inputs to the RF: the strength of the attentional influence (red dashed line) follows a gaussian distribution, with the strongest modulation at the attentional focus and weaker modulation elsewhere.

Multiplicative interaction of the baseline RF (blue solid line) and the attentional influence (red dashed line) results in a Gaussian RF profile (red solid line) that is narrower and shifted towards the attentional focus.
<center>  <img  src=https://i.ibb.co/xLF5v7z/uno.png  width="500px"  />  </center>

#### Model
To simulate the results of Moran & Desimone (1985) and Reynolds et al. (1999), a simple feedforward competitive neural network has been used, defined by 4 equations. 

Attention is assumed to increase the strength of synapses between the population activated by the attended stimulus (e.g., in V1 or V2) and the output cell (e.g., V4). 
Increasing the strength of the signal from the attended stimulus population causes it to have a greater influence on the total excitation and inhibition. Consequently, the response of the cell is driven toward the response that would be elicited if the attended stimulus were presented alone. 
<center>  <img  src=https://i.ibb.co/bd2vyGN/due.png  width="500px"  />  </center>

* Equations 1 and 2 describe the total excitatory $E$ and inhibitory $I$ inputs to the cell;
* Equation 3 describes how the firing rate of the output neuron $y$ changes over time. This equation was originally introduced by Grossberg (1973) to avoid neurons saturating their responses to strong inputs (e.g., high-contrast stimuli), while remaining sensitive to weak inputs. The first term $[(B - y)E]$ governs excitatory input. $B$ is the maximum response of the cell, therefore, $(B - y)$ is always positive. The second term $-yl$ governs inhibitory input. The third term $-Dy$ is a passive decay term;
* Equation 4 describes equilibrium response of the output neuron. 
 
#### Local field potential (LFP)
Selective attention can also enhance signal efficacy via synchrony among neuorons encoding the attended stimulus. In particular, it has been argued that high frequency synchronization ($\gamma$-band) of projection neurons with attention might lead to pronounced firing-rate changes at subsequent stages.

Fries et al. (2001) recorded neuron spikes and local field potentials LFPs simultaneously from multiple V4 sistes, with overlapping RFs. Spikes, LFPs and response histograms show stimulus-evoked responses but no clear effect on attention.

LPSs are low-frequency electrical potential recorded in depth (cortex or deep brain structures) with low impedance extracellular electrodes. The signal is then low-pass filtered.
LFPs sample relatively localized populations of neurons - smaller than EEG - but display the same type of oscillations during wake and sleep states.

APs have a limited participation in the genesis of EEG or LFP, that are instead generated by the synchronous post-synaptic potentials on the local population of neurons.

The LFP is believed to represent the summed and synchronized input into the observed area, as opposed to the spike data, which represents the output from the area.

In order to measure local neuronal synchronization, the spike-triggered average (STA) of the LFP was used. The STA is widely used to study the temporal relationship between a spike train and a simultaneously recorded continuous signal, such as LFP.  It represents the average LFP signal taken in a time window ($\pm 150ms$) around spike occurrences.
 
If spike times have a reliable temporal relation to the local neuronal activity (as measured by the LFP), then LFP fluctuations add up during the STA process. On the other hand, if spike times have no temporal relation to the activity of surrounding neurons, fluctuations in the LFP average out during STA, resulting in a flat STA.
 
To quantify the STA, the absolute power spectrum can be calculated, which gives the magnitude of all frequency components of the STA.
<center>  <img  src=https://i.ibb.co/R0zz3F3/Cattura.png  width="500px"  />  </center>


The STAs revealed oscillatory synchronization between spikes and LFP from two separate electrodes, both during the delay preceding the stimulus (figures E and F) and the stimulus period (figures H and I). 
* During the delay, the power spectra of the STAs (figure G) were dominated by frequencies below $17 Hz$. With attention, this low-frequency synchronization was reduced;
* During the stimulus period, there were two distinct bands in the power spectrum of the STAs (figure J), one below $10 Hz$ and another at $35 Hz$ to $60 Hz$. With attention, the reduction in low-frequency synchronization was maintained and, conversely, gamma-frequency synchronization was increased.  

In summary, attention increased gamma-frequency and reduced low-frequency synchronization of V4 neurons representing the behaviorally relevant stimulus. 
This held true even during the delay period and in the first few hundred milliseconds after response onset, when firing rates were not affected.
 
The observed changes in synchronization may enhance the impact of the affected neurons on postsynaptic targets. Gamma-frequency synchronization causes spikes to coincide within $10 ms$ (half the cycle length of $20 ms$), enhancing their impact on postsynaptic neurons . 
 
### Bottom-up visual attention
Neuorns at earliest stages of visual processing are tuned into simple features (i.e. lumiance, contrast, edge orientation, etc...), but processing becomes increasingly more specialized with the progression from low-level to high visual areas (i.e. corners, contours, shapes, etc...).

Early visual features are computed pre-attentively in a massively parallel manner across the entire visual field. Early stages of visual processing decompose the incoming visual input through an ensemble of feature-selective filtering processes.

Even though attention doesn't seem to be mandatory for early vision, it can modulate it. 
It has been hypotesized that the various feature maps feed into a uniqe *saliency map*, a 2d map whose activity topographically repsents visual saliency, irrespective of the feature dimension that makes the location salient.

This bias attention to focus onto the most salient location.

A saliency map can provide an efficient control strategy for the deployment of attention on the basis of bottom-up cues.
<center>  <img  src=https://i.ibb.co/rHkv9YC/Cattura.png  width="600px"  />  </center>

Visual targets composed of features that are dissimilar from sorrounding distractors are more salient and more easily located during search tasks (more variance, hence more information). These *pop-out* stimuli are believed to draw attention in a bottom-up manner (unaware), with search being driven via parallel (pre-attentive) processing.

Targets made up of a unique conjction of features are more difficult to locate and require longer times as the number of distractors increases.

*Experiment*: to study the impact of bottom-up (stimulus-driven) effects of salience on area V4 responses, visual stimuli are presented during a fixation task. The array stimuli were behaviourally irrelevant (no rewards) and there was no goal-driven basis (no top-down attention).

*Results*: V4 neurons exhibit enhanced responses to pop-out stimuli placed inside the RF. The magnitude of the popout modulation increased with the number of array items and the number of features that define the popout stimulus.
<center>  <img  src=https://i.ibb.co/FxLR7BQ/Cattura.png  width="600px"  />  </center>

## Causal control of visual attention
Gaze direction and the attention focus are often spatially aligned (**overt attention**), but it's also possible to attend to objects of interes in the cisual scene without shifting our gaze (**covert attention**).

### Relationship between saccade preparation and spatial attention
In 1886, **Ferrier** found out that removal of the *frontal eye field* (FEF) in one hemisphere can impar gaze shifts and spatial attention toward the contralesional (opposite) hemifield.
He hypothesized that the:
> "power of attention is initmately related to volitional movements of the head and eyes."

In 1980s, **Rizzolatti** proposed a premotor theory of attention, which states that same neural mechanisms are involved in directing spatial attention and saccade programming.

Later studies showed that visual detection and discrimination are facilitated at endpoints of saccades.

FEF neurons receive projections from most visual area, and projects to both brainstem saccade generator and SC. FEF also sends feedback projection to much of visual cortex, suggesting a pathway where saccade related signals can influence visual processing.
The visual responses of some FEF neurons are enhanced when the RF stimulus is used as a saccade target.
<center>  <img  src=https://i.ibb.co/r21R1SS/Cattura.png  width="600px"  />  </center>

#### Presaccadic visual enhancement
So, when a saccade is preparing there is a feedback to the visual cortex to enhance visual response. Visual activity, in several brain regions, is enhanced immediately before an animal targets a RF stimulus with a saccadic eye movement.

*Experiment*: the neuronal responses to a target visual stimulus presented inside the RF were enhanced when the animal prepared a saccada inside the RF wrt when fixation was mantained.
<center>  <img  src=https://i.ibb.co/Nj1B4wB/Cattura.png  width="600px"  />  </center>

#### Control of eye movements and spatial attention
Several studies have employed electrical microstimulation to investigate the role of gaze-control structures in the deployment of spatial attention.

*Intracortical microstimulation on visual attention*: monkey was trained to fixate a central spot and attend a peripheral target that could randomly dim. While monkey awaited the dimming, visual distractors were randomly flashed. The *motor field* signifies the location to which the eyes move during supra-threshold stimulation (inject enough current to make the eyes move).
<center>  <img  src=https://i.ibb.co/X3JX0P5/Cattura1.png  width="600px"  />  </center>

a. Individual saccade vectors obtained with supra-threshold stimulation at FEF site, illustrating how the motor field was mapped;
b. Open arrowhead indicated the subthreshold used during spatial attention task;
c. Luminance change detection obtained with and without microstimulation.

The subthreshold stimulation of the FEF, immediately before ($\approx 100 ms$) the appearence of the target, significantly improved the animal's performance in detecting the luminance change (sensitivity). The improvement was observed only if the target appears in the motor field.

*Note*: to have a motor field we have to consider a neuron that is capable to move (i.e. arm neuron, eye neuron, etc...)

*Subsequent study* by **Moore**, in 2003: examine functional interaction between saccadic preparation and visual cortical processing, by microstimulating sites in FEF and measurig its effect on the activity of neurons in extrastriate visual cortex V4.
Visual responses in V4 could be enhanced after a brief subthreshold stimulation of retinotopically corresponding sites in FEF sites. The enhancement was significantly increased by the presence of distracting stimuli (attentional competition).
Stimulation of FEF sistes with motor field not corresponding the RF of V4 neurons suppressed responses.

The results suggest that the gain of visual signal is modified according to the strenght of spatially corresponding eye movement commands.

