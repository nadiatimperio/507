# Nadia Timperio's Log for English 507 

## Apr. 2/15
### Panel Presentation Notes

(Presentation PowerPoint slides posted in 507 repo.)

**Methods:**

Each project discussed in this panel has its own distinct methodology, but every project is similar in where the research questions originate from and what the methods lead to or "produce" in the end.  Every project uses computational methods to focus qualitative research – they all begin with a close reading of the text in question.  On the other side of the various computational methods, each one of us finished with two distinct, and yet intimately related, outcomes: a prototype and a literary analysis.  As we conducted our literary analyses using computers, we made contributions back into the critical conversation both through our literary analyses, as well as by producing some object that stands on its own.  Further, these "prototypes" are able to stand on their own by *showing* aspects of our arguments without the writer *telling* or mediating them.  

Lindsey’s network analysis of social relationships in Austen’s novels used CSV databases and Gephi, which is an open-source network analysis program.  She began with two CSVs: one for her nodes (listing the characters), and one for her edges (displaying the relationships between characters based on the degree to which each character demonstrated class mobility.  Then, she imported the CSVs into Gephi and *wizzbang*! The program produced visual networks.  Adam will speak more about the mystery behind the program in a bit.  Finally, Lindsey adapted colour on the visual, added labels, and segregated nodes manually.

In Adam’s investigation of Mitford’s sketches, he used KH Coder, a free software used for content analysis, text mining, or corpus linguistics.  While he also briefly experimented with Gephi, the ultimate choice to use KH Coder was determined by the usability of the software.  It was simple to the point that he could use it confidently with only a minimal step-by-step tutorial.  He imported the text file of the sketches, grabbed from Project Guttemberg, into KH Coder and directed the program to run pre-processing and analyze the text in terms or co-occurrence.

When I set out to conduct my study of emotion in Wright’s Native Son, I hoped that converting the text into "meaningful numbers" would provide me with some clear direction toward the passages of the text that supported my reading of the narrator as unreliably framing the central character as having a lack of emotional grounding.  I had planned to take direction from the sentences with the greatest net positive and negative sentiment values.  But, once I finally got the result I was looking for, I realized they weren’t quite what I was looking for...

Neal Caren, the sociologist who developed the script mine originated from, noted the major challenges in qualitative data analysis:
* collecting and managing the data
* turning the text into numbers of some sort
* analyzing the numbers

I adopted sociologist Neal Caron’s positive and negative sentiment dictionaries, which he had converted from a sentiment dictionary developed by sociologists at the University of Pittsburgh.  I chose these dictionaries because they are freely available and straightforward - the more positive words in a line, relative to the other words in that line, the higher the test scores on the positive sentiment scale.  The lists count the proportion of words that usually have a positive connotation and the proportion that have a negative one.  

Next, I adopted and edited Caren’s Python script to suit my research agenda.  While this type of analysis could be done using other programs, Python is a free and open-source programming language that emphasizes code readability.  Many people use Python, so there are lots of resources available, including online tutorials and scripts shared by other researchers.  

The majority of my script remained the same as Caren’s.  At the top of the script, you can see that I import some modules from Python’s repository – these are the same ones that he uses.  

One difference was that I manually downloaded the sentiment dictionaries and created the text file for *Native Son* locally, so my string linked to my desktop, and not to an online repository, as his did.

The default for this program is to examine each word on its own, following a "bag of words" model.  For example, the phrase "I had no fun" would produce a positive value, based on the word "fun". However, Caron's original script accounts for this, reading the lines contextually.

I initially organized my text file of "Book One" of Native Son according to sentences; I made manual line breaks following end punctuation (except those contained within quotation marks).  So essentially, every line within the text file is a sentence, or multiple sentences if it’s quoted dialogue.  But once I finally got my script up and running using this text file, the results were … not so helpful.  I expected that the sentences with the most positive and most negative net values would direct me to passages in the novel where the narrator was implicitly exhibiting some judgment of the main character’s emotionality.  But this was not the case. 

So I returned to my text file and reorganized it according to my initial close reading, pre-computation.  I made line breaks whenever the narrator made an explicit reference to the way Bigger, the main character, was feeling.  So for example (read example projected).

Running this text file produced more helpful results, since *these* values relayed the overall sentimental value *between* two emotions.

My methodology, as well as those of the other two projects led to the creation of both literary analysis and a digital prototype.  These methodologies all presented unique challenges and limitations on the type and size of questions we were able and comfortable asking, which Adam will discuss in greater detail.

**Conclusion:**

Anne Balsalmo's introduction to "Technicultural Innovation" reinforces this idea.  She argues for the importance of taking culture seriously throughout technological innovation.  Building on her connections between the cultural and the technological, we posit that our work examining the social relationships in literary texts is "innovative," and instrumental, in that we "create unique arrangements that provide the basis for a reorganization of the way things will be in the future."  Our method of reading literature through a digital lens has in effect accomplished this aim.  If, we make our prototypes publically available by publishing them alongside our literary analyses (presented in the form of the traditional academic essay), we effectively distribute a new way of organizing the text - a "reorganization" of the text that can serve to influence future research projects.  While it's every researcher's hope for one's work to be to be taken up by future critics and that one's arguments are agreed with – disagreed with, or built upon – it is our additional hope that our prototypes are also brought back into the critical conversation.  

##Mar. 24/15
### Log 8: Panel Abstract

**Panel Title:** Quantifying the Qualitative: Examining Relationships in Literary Texts

**Abstract:** How do we, as literary scholars, quantify relationships - which are inherently qualitative - in a text?  This question drives the research of all three projects comprising this panel: a social network analysis of Jane Austen’s novels, *Mansfield Park* and *Emma*; visualizing character co-occurrence in Mary Russell Mitford’s *Our Village*; and an algorithmic reading of Richard Wright’s *Native Son*.  This panel will discuss the parameters, methods, and limitations of such research.  Ultimately, we posit that leveraging computational methods to guide innovative literary analysis renders this work instrumental scholarship (i.e. work that replicable, referenceable, and extensible).

**Panelists:** Adam J. Kneeland, Lindsey Seatter, and Nadia Timperio

##Mar. 17/15
### Log 7: Working Prototype

**Argument:** My research engages Richard Wright’s infamous protest novel *Native Son* (1940) as a strategically constructed text that critiques the practices and consequences of institutionalized racism by mimicking participation in the Othering of a young black man.  The narrator’s descriptions of Bigger’s thoughts and actions “transform [his] consciousness in the very act of representing it” (Tanner 413).  Since the linguistic sophistication of the narrative voice echoes speech patterns of the white characters, I posit that Bigger’s story, relayed through the oppressor’s voice, does not communicate a reliable narrative, but instead suggests that Bigger’s inability to establish emotional grounding is responsible for his condemning acts of aggression.

**Discoverability:** My essay will be written in markdown and pushed to my GitHub account.  At this point, a text files of the positive and negative sentiment lists, the python script I'm using, and "Book One: Fear" from *Native Son* are discoverable, but I am hopeful that my request for a private educational account will be granted.  

**Works Cited**

Tanner, Laura. “Uncovering the Magical Disguise of Language: The Narrative Presence in Richard Wright's Native Son.” *Texas Studies in Literature and Language* 29.4 (1987): 412. Web. 15 Mar. 2015.

##Mar. 3/15
### Log 6: Abstract for the Final Essay
**Anger/Fear/Shame-Driven Violence: Examining the Role of Emotion in Richard Wright’s *Native Son***

This project examines the role emotion plays in Richard Wright’s *Native Son* (1940). Anti-hero Bigger Thomas displays little remorse for the violent crimes he commits. Wright’s unapologetic portrayal of Bigger has been read to suggest a systematic inevitability behind the young man’s acts of violence. I posit that Bigger’s inability to identify the social conditions imposed upon him and other African Americans by “White” America is reflected in the narration’s slippage between emotions. To explore potential consequences of Bigger’s emotional journey, this project analyzes all references to emotion in the first part of the novel: “Book One: Fear”. I use two major research strategies: (1) a close reading of emotion-laden descriptions, especially as they relate to Bigger’s actions and reactions to environmental elements, and (2) a quantitative analysis of both the references to emotion, and of the passages connecting these instances. I have encoded the novel’s first part and will conduct qualitative analysis in a text editor. This study takes up previously established parallels between Bigger’s psychological disorientation and larger social conditions that are responsible for his predicament, as well as the identification of Bigger’s disassociated sensibility. I synthesize and expand upon these claims by demonstrating how the narrator mirrors Bigger’s confusion through a muddled articulation of his emotional journey.  Every time one emotion slips into another, the narrator implicitly suggests that Bigger’s inability to establish emotional grounding is responsible for his condemning acts of aggression.

**Journal:** I will write my essay with the intention of submitting it to Modern Fiction Studies, a peer-reviewed journal committed to publishing articles that take “theoretical, historical, interdisciplinary, and cultural approaches” to analyzing modern fiction. In the recent past (since 1995), MFS has published articles on *Native Son*, which suggests that this journal facilitates a conversation I could insert myself into.

**Scope:** Since I am encoding the text manually, I have narrowed my computational analysis to the novel’s first part: “Book One: Fear.” This unfortunately excludes rich moments of slippage between emotions present in the second part of the novel (during this second book, Bigger attempts to lives in constant fear that his first crime will be discovered as he runs from his fate).

**Concerns:** How do I appeal to scholars who are new to media studies? If my method of reading the text *could* be conducted without encoding, how do I justify my methodology for a non-DH journal’s readership?

##Feb. 24/15
###Log 5: Workshop Reflection

I expressed to my peers the frustration and lack of clarity I felt regarding my project.  I relayed that my preliminary readings on affect theory had led me to a place of and my desire to drop that theoretical lens altogether.  They provided valuable insights, as detailed below:

Massa suggested I consult her bibliography as she has changed the focus of her project and is now working with emotions in modern American literature as well.  She also suggested I check out Matcher Drucker’s work and that I might want to consult some sentiment dictionaries.

Elizabeth and Matt both encouraged me to return to my initial instincts and to remain open to the possibility of engaging with affect theory.  Elizabeth suggested I explore how other literary scholars have engaged with affect theory in literary analysis (she specifically cited an article by Sylvan Thomson on Agnes Grey).  

## Feb. 16/15
### Log 4: Annotated Bibliography

**Elder, Matthew.** "Social Demarcation and the Forms of Psychological Fracture in Book One of Richard Wright's Native Son." *Texas Studies in Literature and Language* 52.1 (2010): 31-47. Web. 26 Jan. 2015.

Draws parallels between Bigger’s psychological disorientation and larger social conditions that are responsible for his predicament.  Elder’s understanding of Bigger informs my own interpretation of how the character’s psychological confusion manifests itself in his actions.

**Ellis, A J.** "Where Is Bigger's Humanity? Black Male Community in Richard Wright's Native Son." *Anq Lexington Ky* 15 (2002): 23-29. Web. 5 Feb. 2015.

Suggests Bigger’s “deeply emotional conversations with his homeboys” work to establish a black male community, which enables the men to “purge the psychic pain of urban blight.”  This investigation of urban homosocial spaces and recognition of a performed black male identity create an opportunity to discuss the space between Bigger’s environment and actions. 

**Fairfield, J.** "Deadly Discourses: Examining the Roles of Language and Silence in the Lynching of Emmett Till and Wright's Native Son." *The Arizona Quarterly* 63.4 (2007): 63-82. Web. 10 Feb. 2015.

Cites Bigger’s inability to engage in the “master language” of the white community as the primary determinant in securing his fate.  I will relate these concerns with language to Bigger’s inability to establish an emotional grounding.

**Hogue, W.L.** "Can the Subaltern Speak? a Postcolonial, Existential Reading of Richard Wright's Native Son." *The Southern Quarterly* 46.2 (2009): 9-39. Web. 26 Jan. 2015.

Dissects the previously established psychological portrait of Bigger using ideas from subaltran studies, post-colonial theory, psychoanalysis, and existentialism.  This interpretation of Bigger’s un/conscious desire for agency will inform my understanding of what happens between environmental factors and his reaction.

**Massumi, Brian.** *Parables for the Virtual: Movement, Affect, Sensation.* Durham, NC: Duke University Press, 2002. Print.

Claims cultural formations, such as the body and media, function on varying levels of sensation, beyond traditional rhetorical models.  Suggests affect remains autonomous from conscious perception, language, and emotion.  Following this, I posit that affect in *Native Son* is located in the passages between the narrator’s identifications of Bigger’s emotion.

**Matthews, Kadeshia L.** "Black Boy No More? Violence and The Flight from Blackness in Richard Wright's Native Son." *MFS: Modern Fiction Studies* 60.2 (2014): 276-297. Web. 10 Feb. 2015.

Questions the black subjectivity of the novel and suggests that Wright constructs gendered subjects, not racialized ones.  Will support a reading of the text that sees Wright’s project as racially inclusive; Bigger’s circumstances are representative of a greater community than exclusively those of African American men.

**Probyn, Elspeth.** “Writing Shame.” *The Affect Theory Reader.* Ed. Melissa Gregg and  Gregory J. Seigworth. Durham, NC: Duke University Press, 2010. 71-92. Print.

Defines "writing shame" as the author’s "affective, bodily feeling of betraying interest" (71).  Discusses implications of one’s writing that shame brings to the forefront.  Will inform a reading of the text that illuminates Wright’s motivation to create the character of Bigger Thomas.

**Tremaine, Louis.** "The Dissociated Sensibility Of Bigger Thomas In Wright's Native Son." *Studies In American Fiction* 14.1 (1986): 63-76. Web. 10 Feb. 2015.

Reads the novel as a “formal projection of Bigger’s struggle toward self-expression”  (63).  My research builds on Tremaine’s identification of Bigger’s “dissociated sensibility,” that is, “the conflict between experience and expression where there should be complementarity,” but instead, gives rise to acts of violence (64).

**Wright, Richard.** “How ‘Bigger’ Was Born.” *Native Son.* New York: Perennial Classics, 1998. 429-462. Print.

Explains Bigger as representative of many men with antisocial and violent tendencies, whom Wright witnessed.  Will inform a reading of the text as depicting a universal problem and indicative of broader social wrongs than that of one man.  Perhaps Bigger’s individual affectual experience is unimportant, considering Wright’s authorial agenda.

**--.** *Native Son*. New York: Perennial Classics, 1998. Print.

Unapologetic depiction of impoverished African American Bigger Thomas suggests systematic inevitability behind crimes he committs throughout the novel.  Bigger’s response to environmental influences and his inability to identify the social conditions responsible for his demise reflect his emotional stiltedness.  The narrator’s muddled attempt to articulate Bigger’s emotional journey will be analyzed through computational methods after having been encoded in markdown, with special attention paid to mentions of emotion.


## Feb. 3/15
### Log 3: Revised Thought Piece

I wish to conduct a study of affect in Richard Wright’s infamous protest novel, *Native Son* (1940).  Wright has been criticized for years as the main character, 20-year-old African American Bigger Thomas, living in Chicago’s South Side in the 1930s, shows little remorse for his violent actions.  Wright’s unapologetic portrayal of Bigger sheds light upon the systematic inevitability behind the crimes committed throughout the novel.  Likewise, Wright, though the narrative voice, makes no effort to apologize for Bigger’s crimes, but instead sheds light upon the systematic inevitability behind them.  Although Bigger’s crimes provide the action for the narrative, the real story rests in the way Bigger responds to environmental influences.  Bigger’s inability to identify the social conditions imposed upon African Americans by the dominant white society which have led to his demise reflects his emotional stiltedness.  Even at the end of the novel, Bigger is unable to explain the circumstances he was placed in which led to his demise – instead, a lawyer speaks on his behalf.  I wish to illustrate how this inability to articulate one’s emotions is prevalent throughout the entire piece through the narrator’s combination and conflation of Bigger’s self-unidentifiable emotions.

To accomplish this goal, I will transcribe the first part of the text, “Fear,” into a text editor with line breaks before and after every explicit mention of emotion.  Following transcription, the references to emotion could be pushed into a data sheet and read cumulatively, allowing me to study what comes in-between and to contextualize the connectors between emotions.  At this point, I will evaluate my findings and decide on the next step.  One course of action might be to produce a force directed graph, a type of network visualization.  This type of visualization will present the interconnectedness of emotions and signify which relationships are strongest based on thickness of connecting line.  Additionally, within this model, springs and charged particles will enable the more closely related emotions to appear in closer together than those that lack association in the text.  I will need to familiarize myself with the Gephi or D3.js to create a digital visualization.  Alternatively, structuring the text though references to emotion may be the full extent to which computers help me work through my question.  In transcribing the text in this way, I will be reading like an algorithm; my process will model a computation approach and so an actual algorithm might not be necessary.
 
Should I choose to produce a network visualization, a larger project would be to incorporate my the graph into a longform, media-rich narrative; my argument would be ideally communicated through the presentation of a visual aid alongside text.  Since my research aims to show the interconnectedness and interdependence of Bigger’s emotions, as the narrator attempts to define them, the employment of a network visualization is most appropriate.  Not only will the network make visible and therefore more easily digestible the argument I present, but it will also help me to realize varying strengths of relationships between emotions.  For example, I predict to find more frequent connections between “fear” and “anger” than between “shame” and “power,” which should provide insight into the characterization of Bigger Thomas. 

**Bibliography**

Wright, Richard. *Native Son*. New York: Perennial Classics, 1998. Print.

## Jan. 27/15
###Workshop: Think Piece Review

Nadia's comments appear in-text, *italicized*.

**Mahsae Badpour**

Umar Khayyam was a polymath, scientist, philosopher, and poet of the 11th century CE. Although Umar Khayyam's Rubā‘iyyāt have been admired in the Persian speaking world for many centuries, they have only been known in the West since the mid 19th century, when Edward FitzGerald rendered the Rubā‘iyyāt into English. In his Rubā‘iyyāt, Khayyam challenged religious doctrines and casts doubt on them. The paradox of his philosophies where he refers to God as the “Necessary Being” and his Rubā‘iyyāt in which he exhibits skepticism is the subject of my interest. I aim to shed light upon his ideas and philosophies in Rubā‘iyyāt to determine which philosophy and thought he leaned towards. What shall we call the ideas that Khayyam expresses in Rubā‘iyyāt; theological or philosophical?

The new media will help me search for the key concepts in Rubā‘iyyāt , gather data , and make a more efficient illustration with the use of audio and visual aids. There are a lot of religious, mythological allusions in this work that would be best demonstrated with the help of new media. Furthermore, the computation would be more rapid and precise than a normal close reading. Employing the new media will be of great assistance in comprehension and connecting of the concepts by engaging more of our senses. It will also illuminate the link between the allusions given in the text and Khayyam’s beliefs.  

*I understand that Khayyam's philosophical beliefs are informed by/expressed through mythological allusions; however, I'm unsure as to exactly how the audio and visual elements of the media-rich narrative will illuminate the links between his literary and philosophical texts in a way that citing them in writing would not.  Maybe an example here of a particular image that you think might be included in your project and a sentence or two on the connection would strengthen this Think Piece.  Thinking about the kinds of elements you will include in the media-rich narrative might help you to narrow the scope of your argument aswell.*

I would like to demonstrate the piece by a long form, media-rich narrative since it would allow me to guide the argument through visual elements. This method would allow me to make distinct and clear demonstration of the allusions and imagery mentioned in the poem in order to come up with the patterns linking them to Khayyam’s ideas. I intent to trace the various allusions and references in the work and then demonstrate them by either using a pre-existing visual media or creating 3D models. To expand the research I might portray the patterns and links between these images and his beliefs using graphs and network visualizations. 

The type of media that I will need to maser this recipe would be Scalar, CSS, and markdown.furthermore, D3.js, Python , and CityEngine. I intent to create a visually accessible piece that is both illuminating and educational.

*Interesting project, Mahsae!  What is most promising about this proposed project is your background in this area.  The wealth of knowledge you have regarding Persian language, literature, and mythology makes you an ideal scholar to complete this project.  My concern at this time is with the scope of the project.  You have indicated that FitzGerald translated ~70 quartets, but that you will also consult the original poems, as well as Khayyam’s philosophical papers; this seems like an overwhelming amount of texts to work with and so maybe, considering the timeline of this semester, the project's scope should be narrowed.  Along the same line, I think you have proposed too many projects.   I think that the construction of 3D models, graphs, network visualizations, and the longform, media-rich narrative seems like an ambitious project that one would have difficulty completing over the next two months.*


**Elizabeth Bassett**

Although Anne Brontë's Agnes Grey has often been referred to as having a simple narrative structure (Bell; Berry; Stolpa), Agnes' reference to her personal diary at the end of the novel makes clear that Agnes (the narrator) has written down two accounts of her life story, and also makes clear that the construction of her governess story is purposefully complex.

If a distinction is drawn between Agnes' public (governess) story and her private story, then Agnes Grey appears to be very deliberately constructed as an instructional novel that aims to inform readers of the stifling conditions of the governess occupation. The main question of this research is: How does the subtly complex narrative form of Agnes Grey reflect the tensions between the narrator's governess (public) self and her personal self?

Using computation to modify Brontë's original text and then close reading the digitally altered text could aid in emphasizing that Agnes' references to her separate and personal story are essential to the overall impact of her governess narrative. For example, deleting instances where Agnes interrupts her personal story would shed light on the narrative purpose of her interruptions.

Computation will allow me to rearrange Brontë's text, and to speculate about what her text would lack if the narrative interruptions were omitted. Juxtaposing the altered model with her original text will allow me to draw attention to the intricacies of Brontë's narrative in a way that extends the traditional close-reading methods used in earlier versions of the paper.

Based on Posner's article, I anticipate that I will use a media-rich narrative argument for my final seminar essay.

A media-rich narrative will allow me to present my final seminar essay in a form that is conducive to integrating images. Showing images of Brontë's original pages of text beside pages that have been digitally altered for this paper will aid with my analysis, as well as with how it is presented.

For this argument, I will need both a print copy of Agnes Grey (for me to read) as well as a digital copy (for me to manipulate). I will need to use a text editor as well as, perhaps, an image editor such as Photoshop. In addition, I will need to decide on a platform for presenting my project. As my decision to choose a media-rich narrative was informed by Matthew F. Delmont's project The Nicest Kids in Town, it seems likely that Scalar could be an appropriate platform.

*This sounds like a very strong project, Elizabeth.  It is obvious that your idea has been born out of thoughtful engagement with the text in question and so the problem, questions, and hypothesis all appear to be well thought out.  The relationship between the research question, how do the moments in which the narrator draws attention to her own self-subservience reflect the tension between her public and private self, and the choice of computation seems very tight.  The creation of a digitally modified text, in addition to serving your argument, will stand as a valuable resource to other scholars who wish to build off of your observations about the text.  The media-rich narrative makes sense too, considering you've already articulated the consequences of these hypothetical deletions in an earlier project. This also reassures me of the feasibility of this project, considering the time constraints.*

**Matt McBride**

Last semester, I worked on an essay exploring the relationship between Martin Heidegger’s Question Concerning Technology and the biblical fable the Tower of Babel. Specifically, I tried to show that the Babel story demonstrates Heidegger’s concept of “enframing,” and “Dasein.” I wanted go further and demonstrate how the different reactions to Babel throughout history demonstrate the same principle in a sort of art mirroring life mirroring theory.

Does Babel reflect Heidegger’s concepts of Dasein and Gestell, which in turn reflect the artistic interpretations of Babel throughout the ages, which in turn reflect et cetera?

Where new media can help address this question is in its own expression of the Babel story. It models the story of Babel with new concerns involved and a different medium from previous ages. In this sense, new media merely carries on the work of previous intepretations. However, I would hope that a new media project might be able to ask new questions of Gestell and project alternative endings to Babel.

I would like to build a text-based game either in Ruby or Python. At this stage, I’m still unsure of what question I’m trying to answer. I know that my game design would add to the examples of my argument, yet I won’t be able to know if it could produce another answer to the second half. A main feature of what Heidegger’s concepts and Babel have in common is an inevitability. That the structure of existence presupposes this. If I make a game that presupposes the same ending, will players inevitably play it out? Or will they figure out different ways of understanding it? And will it help me understand Heidegger’s concepts better?

My primary sources include the biblical story of Babel, Martin Heidegger’s Question Concerning Technology. I may use as secondary resources any critical articles that link the two although in my previous research I did not, so it is a matter of debate. For the tools, I will either use Ruby or Python to make the text-based game. My inspiration, A Dark Room used Ruby, so I may stick to that language.

*Exciting project, Matt!  What I understood of your Think Piece seems very interesting.  One research challenge I see at this time is the feasibility of addressing the second part of your question - how will you know whether or not players have resisted the structure by creating an alternative ending to Babel?  As we discussed in our group conversation, would you create a "Comments" section for participants to volunteer testimony of their experiences playing?  Is there some way of tracking game participation?  If the latter option is your choice, this might present a new technical challenge.  Another consideration I thought of after our group conversation concerns the participants in your study.  Have you considered the consequences of players' familiarity with Heidegger's Question Concerning Technology and/or with the story of Babel?  Is it preferable to have players who are or those you are not familiar with either/both of these concepts?  If this question of familiarity is relevant to your project's aims, how will you recruit players that are/are not familiar with these texts?*

### Log 2: Think Piece

<p> I wish to conduct a study of affect in Richard Wright’s infamous protest novel, *Native Son* (1940).  Wright has been criticized for years as the main character, 20-year-old African American Bigger Thomas, living in Chicago’s South Side in the 1930s, shows little remorse for his violent actions.  Wright’s unapologetic portrayal of Bigger sheds light upon the systematic inevitability behind the crimes committed throughout the novel.  Likewise, Wright, though the narrative voice, makes no effort to apologize for Bigger’s crimes, but instead sheds light upon the systematic inevitability behind them.  Although Bigger’s crimes provide the action for the narrative, the real story rests in the way Bigger responds to environmental influences.  Bigger’s inability to identify the social conditions imposed upon African Americans by the dominant white society which have led to his demise reflects his emotional stiltedness.  Even at the end of the novel, Bigger is unable to explain the circumstances he was placed in which led to his demise – instead, a lawyer speaks on his behalf.  I wish to illustrate how this inability to articulate one’s emotions is prevalent throughout the entire piece through the combination and conflation of emotions, as Bigger identifies them.

To accomplish this goal, I will produce a force directed graph, a type of network visualization.  Using identified emotions within the text as my dataset, this type of visualization will present the interconnectedness of emotions and signify which relationships are strongest based on thickness of connecting line.  Additionally, within this model, springs and charged particles will enable the more closely related emotions to appear in closer together than those that lack association in the text.  As Posner recommends, in order to produce this feature, I will need to familiarize myself with the D3.js, a JavaScript library used to create digital visualizations, and Python, a programming language used to manipulate data.  I will produce my own dataset by manually tracking and recording instances of affect within the novel. 

A larger project, which I hope to complete, would be to incorporate the visualization into a longform, media-rich narrative; my argument would be ideally communicated through the presentation of the visual aid alongside text.  Since my research aims to show the interconnectedness and interdependence of the various emotions, as Bigger understands them, the employment of a network visualization is most appropriate.  Not only will the network make visible and therefore more easily digestible the argument I present, but it will also help me to realize varying strengths of relationships between emotions.  For example, I predict to find more frequent connections between “fear” and “anger” than between “shame” and “power,” which should provide insight into the characterization of Bigger Thomas. 
 <p/>


**Bibliography**

Wright, Richard. *Native Son*. New York: Perennial Classics, 1998. Print.

## Jan. 20/15
### Log 1: After Hermes?

Although I, personally, am not persuaded by Alexander R. Galloway’s argument outlined in “Love of the Middle,” his contribution to Excommunication: Three Inquiries in Media and Mediation (2013), I believe his rhetorical style would prove effective for a specific, and likely his targeted, demographic: the traditional humanities scholar, well-versed in classical literature and Western philosophy.  Galloway proposes a theory of mediation through descriptions of mythological figures Hermes, Iris, and the Furies.  These figures are used to introduce and elucidate the dominant modes of contemporary critical discourse: exegesis, hermeneutics, symptomatics, immanence, and ‘furious’ communication.  All five of these critical approaches are aptly presented by Galloway as forms of mediation – intermediate action between two bodies.  At the climax of his essay, Galloway celebrates the “withering” of “hermeneutic interpretation and immanent iridescence” in exchange for the rise of “the system, the machine, the network” (62).  Not yet having explored the examples Galloway lists later in his piece, I can only speculate what critical scholarship might look like within this new culture.  I foresee the types of scholarship emerging from the “infuriation of distributed systems” to reflect a ‘new’ poststructuralist agenda (62).  Poststructuralists argue against the hermeneutic understanding that exercises such as ‘truth’ finding and meaning-making are legitimate pursuits.  Instead, they suggest that a sort of materiality or particular structure should constitute focus for analysis.  I posit this ascending “network” which Galloway enthusiastically speaks of could fulfill the role of a poststructuralist focus through which analysis could develop.  Why must images and texts experience a “tendential fall” while the machine rises (62)?  I suggest coexistence has the greater potential to be embraced by practitioners of critical inquiry, trained in the tradition of textual analysis, especially since this is the community whom I feel would respond most favourably to Galloway's argumentative style.
