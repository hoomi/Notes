###Basic Concepts of speech

1. There are no certain boundaries between units, or between words.

###Structure of Speech

1. <b>Phones</b>: Similar classes of sound in sequence of changing states

2. Phones can vary greatly depending on factors such as phone context, speaker style of speech

3. Coarticulation makes phones sound very different from their “canonical” representation

4. <b>Diphones</b>: parts of phones between two consecutive phones

5. A phone is usually divided into three or more regions of different nature - known as sub phonetic  units

6. Three sub phonetic -> <b>One</b>: It is related to the previous phone <b>Two</b>: It is the middle part which is usually stable <b>Three</b>: It the region before the subsequent phone

7. <b>Senone</b>: When phones are cosidered in a context, it is called a Senone    

8. <b>Subword</b>: Phones build "reduction-stable entities" similar to sylabus in words.

9. Subwords are usually used for vocabulary speech recognition

10. <b>Fillers</b>: Words and other non-linguistic sounds are called fillers

11.  <b>Utterances</b>: Fillers form utterances. They are seperated chunks of audio between pauses. They are not necessarily sentences

###Recognition process

Common way to recognize a speech:

1. Split a waveform into utterances using slinces
2. Recognize what is being said in each utterance

 <br/>

-	 <b>Concept of feature</b>: Each speech is usally divides into frame with length of typically 10 milliseconds. Then 39 numbers is extracted from each frame which is called <b> feature vector </b> . Selecting the feature vector is under active investigation

- <b>Concept of model</b>: It describes some mathematical object that gathers common attributes of the spoken word.
 
- <b>Hidden Markov  Model (HMM)</b>: It is the model of speech which describes the black-box communication channel.

- <b>Matching process</b> At any points we maintain best matching variants and extend them as time goes producing best matching variants for the next frame.

###Models
There are three models used in speech recognition:

1. <b>Acoustic Model</b>: It contains acoustic(mechnical waves) properties for each senone.There are context-independent models that contain properties (most probable feature vectors for each phone) and context-dependent ones (built from senones with context).

2. <b>Phonetic dictionary</b>: It contains a mapping from words to phones.

3. <b>Language Model</b> It is used to restrict word search. It defines which word could follow previously recognized words.  Most common language models used are n-gram language models-these contain statistics of word sequences-and finite state language models-these define speech sequences by finite state automation, sometimes with weights.

###Other Concepts Used
- <b>Lattice</b>: It is a directed graph that represents variants of the recognition. 
- <b>N-best lists </b>: They are like lattices but not as dense.
- <b>Word confusion networks (sausages) </b>: They are latices where the strict order of nodes is taken from lattice edges.
- <b> Speech databse </b>: A set of typical recording from  the task database. It is used to train, tune and test the decoding systems.
- <b> Text database </b>: Sample texts collected for language mode training and so on.

###What can be optimized

1. <b>Word Error Rate</b>: Let we have original text and recognition text of length of N words. From them the I words were inserted D words were deleted and S words were substituted Word error rate is:(It is usually measured in %)

		WER = (I + D + S) / N
2. <b>Accuracy</b>: It is almost the same is WER but it does not  count insertion

		Accuracy = (N - D - S) / N
3. <b>Speed</b>: Suppose the audio file was 2 hours and the decoding took 6 hours. Then speed is counted as 3xRT.

4. <b>ROC(Receiver Operating Charactersitics) graph</b>:A curve is a graphic that describes the number of false alarms vs number of hits, and tries to find optimal point where the number of false alarms is small and number of hits matches 100%.

 



