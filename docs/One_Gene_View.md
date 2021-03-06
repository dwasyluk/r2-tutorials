<a id="one_gene_view"> </a>

One Gene View
=============


*Analyze the expression levels of a single gene within a dataset*


Scope
-----

-   Use R2 to investigate the expression levels of all samples from a
    specific dataset.
-   In this example the expression levels of the MYCN gene will be used.
-   Adjust several parameters in the advanced settings panel to get a
    better insight in the expressions levels or adapt your
    graphic layout.
-   In R2, the samples are annotated with e.g clinical data, each group
    of annotated data is called a “Track” in R2. These tracks can be
    used to filter data in all types of analyses R2 is offering.
-   A separated info panel in the one-gene expression level screen
    provides different types of analyses based on the expression level
    of the chosen gene.
-   Most of the mRNA expression datasets are generated with Affymetrix
    profiling arrays. In general these arrays use more than one so
    called probeset to measure the expression level of one single gene.
    With a separated module “Transcript view”, the details of the
    probesets can be studied.





Step 1: Selecting a gene
---------------

1.  Use “Single Dataset” in field 1 and make sure that the “Tumor
    Neuroblastoma public - Versteeg - 88 - MAS5.0 - u133p2” dataset is
    selected in field 2.
2.  Choose “View a gene” in field 3.
3.  Type MYCN and click ‘next’.


![Figure 1: R2 Single geneselection](_static/images/OneGene_singleselect.png "Figure 1: Single geneselection")

[**Figure 1: Single geneselection**](_static/images/OneGene_singleselect.png)


 ---------------
 ![](_static/images/R2d2_logo.png)**Click on "all news" to see previous R2 updates**
  
 ---------------





Step 2: Probesets for a gene
---------------

1.  In many cases more than one probeset is reported for each gene. In
    this example, there are 5 probesets annotated for the MYCN gene. By
    default, the probeset with the highest average present signal (APS)
    is selected. This APS signal is simply the average of all samples
    that are considered to express a selected gene (have a
    present call). Occasionally other probesets assigned to the same
    gene could be of interest depending on the structure of the gene
    (for example a potential splice variant). Also realize that the most
    informative probeset is re-determined in every dataset, sometimes
    resulting in a different probeset as the choice of R2. The
    expression levels are by default converted to log2 values.
	  	
	![Figure 2: By default the probeset with the highest expression level is selected](_static/images/OneGene_Adjust.png "Figure 2: By default the probeset with the highest expression level is selected")
	
	[**Figure 2: By default the probeset with the highest expression level is selected**](_static/images/OneGene_Adjust.png) 
    
2.  It could be that for a specific graphical representation not all
    the (default) tracks need to be represented in a graph. To add or
    skip tracks, click on the Track Display section and select the
    appropriate tracks.
3.  In the adjustable settings screen use the pre-defined default
    settings and click ‘next’.

----------
 ![](_static/images/R2d2_logo.png)**Did you know that a reporter with an exclamation marks is an indication there may be something wrong with the reporter (e.g. bad design)**      

 ![](_static/images/OneGene_Probeset.png)                  

> *Hovering over the exclamation mark will inform you on what may be the    
 issue with a specific reporter (probeset).Reportes with an issue will    
 not be used to represent a gene in searches where hugoonce is used.     
 Hovering over the name of a gene will display concise gene information,  
 such as alternative names for the current gene. In case you are not      
 searching with an official NCBI genesymbol, R2 will also search the      
 alternative names to find your gene of interest.*  

----------



Step 3: Plotting Gene expression 
---------------

1.  R2 generates a YY-graph Figure 3 from the MYCN expression levels of
    all samples with expression levels ordered from left (low) to
    right (high). Hovering over the dots reveals additional annotation
    that R2 has stored for the focused sample.
2.  Underneath the X-axis, colored boxes are depicted, representing
    clinical information of the samples in so called "tracks". Again,
    hovering over them will reveal underlying data. For MYCN there is a
    clear relation between the expression levels and the tracks for
    “MYCN amplification” and “INSS-stage“. So these tracks underneath
    the image give a quick glance at some of the clinical parameters,
    defined for the dataset. It is also possible to define your own
    custom made tracks, or disable/adapt the settings for default tracks
    (further explained in “Adapting R2 to your needs")
	
	![Figure 3: YY plot MYCN expression](_static/images/OneGene_MYCN.png "Figure 3: YY plot MYCN expression")
	
	[**Figure 3: YY plot MYCN expression**](_static/images/OneGene_MYCN.png)

3.  Sometimes you get more insight by reviewing the expression levels
    with other transformations. Scroll down and transform the data
    (Figure 4), choosing “none”, in the ‘transformation’ pulldown menu
    and click adjust settings. In the “adjustable settings” panel, there
    are several other settings to adapt the graph R2 generates (like
    changing font sizes, or adding labels to the datapoints). 

----------
  ![](_static/images/R2d2_logo.png)**Did you know that the Adjustable Settings panel is also available in the previous screen**
  
> *Just scroll down the page*
  
----------

To highlight / mark specific samples in the graph you can enter the r2 sample ID’s in the field 'samples to mark' from the
‘adjustable settings’ box. Several marking options can be selected with the 'Mark method' that can be found in the 'More settings' tab (e.g: ‘epicenter’ and ‘arrow’).

To generate a graph of a subgroup of samples use the 'Select a track(subset)' Select pulldown from the 'sample filter' tab to select a specific group. These selections can be repeated a couple of times to build your ultimate selection. After every selection, you have to 
click the red ‘confirm’ link to fix the selection.


![Figure 4: Adjusting the graph settings](_static/images/OneGene_Marksample.png "Figure 4: Adjusting the graph settings")

[**Figure 4: Adjusting the graph settings**](_static/images/OneGene_Marksample.png)

Also multiple colors and different markings can be applied to the individual samples you want to highlight. Next to only indicate the samples, you maybe want to use multiple colors and the type of marking. In order to do so define the method within the ‘samples to mark’ box by adding another ‘:’ after the color representation. Defining this will overrule the default setting, and thus also enable the use of different markings within the same figure. So the skeleton for advanced usage is : ‘sample1,sample2:color1:method1;sample3,sample4:color2:method2’. For example: ‘“itcc0288:0000ff:dot;itcc0021:ff00ff:arrow;itcc0013,itcc0132:00ff00:epicenter”’ creates the markings as shown in the figure.


![Figure 5: Adjusting the sample mark layout](_static/images/one_gene_view_samplesmark.png "Figure 4: Adjusting the graph settings")

[**Figure 5: Adjusting the sample mark layout**](_static/images/one_gene_view_samplesmark.png)

>*R2 knows a couple of mark options, that you can make use of in the advanced prescriptions:* 
 - *'dot': places a thick border around the sample*
 - *'circle': Places a ring around the sample (diameter 9)*
 - *'circle_2': Places a ring around the sample (diameter 4)*
 - *'circle_3': Places a ring around the sample (diameter 1), effectively a thin border*
 - *'epicenter': Places a set of 3 rings descending in width around a sample*
 - *'arrow': Places a block arrow pointing to the sample*
 - *'triangle': Places a filled triangle under the sample*

>*Note: The dotsize does not scale with 'arrow' and 'triangle' method.*

---------------
 ![](_static/images/R2d2_logo.png)**Did you know that converting expression levels using the “transform” option can help you to gain additional insight.**                              

> *There are several data transformations available*                         
 -   *“none”: Raw untransformed expression values, as they are represented 
     in the R2 database.*                                                  
 -   *“2log”: logarithmic values with base of 2. Every increment           
     constitutes twice the amount.*                                        
 -   *“rank”: Data transformation in which numerical or ordinal values are 
     replaced by their rank when the data are sorted by expression. This  
     transformation is useful for non-parametric statistical tests.*       
 -   *“zscore”: 2log transformed data, centered around the average and     
     expressed as the number of standard deviations from the average.*     
 -   *“zscore\_nonlog”: raw intensity values, centered around the average  
     and expressed as the number of standard deviations from the average. This transformation is 	 useful when the intensities in R2 are not raw, but for example logfolds as is often the 	 	 case for aCGH data.*    
 -   *“mad/mad2log”: Median absolute deviation (on raw values, or log2     
     transformed values).*                                                 
 -   *“center/log2center”: Expression values centered around 0 (on raw     
     values, or log2 transformed values).*                                 
 -   *“zcore\_group”: Coverts the expression levels from the zscore within 
     a group (track). Applicable when e.g technical variation in          
     expression levels is expected. A possible reason could be when       
     samples from the same dataset originate from different centers.*      
     
---------------


Step 4: Probeset verification
---------------


Figure 5 lists for the various reporters of MYCN whether they are in
agreement with the genome position of MYCN reference sequence (RefSeq).
If all are stating “YES” then everything appears alright (from the
perspective of an automated assessment). For the MYCN reporters “NO”
indications indicate there may be an issue with it. Scroll down the page
and click on the “Tview” link in the reporter table.



![Figure 5: Probeset verification table](_static/images/OneGene_Probesettable.png "Figure 5: Probeset verification table")

[**Figure 5: Probeset verification table**](_static/images/OneGene_Probesettable.png)

1.  A new screen (or TAB in the browser) appears with TranscriptView.
    The Transcript view application depicts the alignment of expressed
    sequence tags (EST) and mRNA sequences to the human reference genome
    sequence (Fig 5). The strand orientation of these sequences are
    indicated by a color (green = positive strand, red = negative
    strand, blue = strand information is missing). The structure of the
    reference sequence has also been indicated. Furtermore, it has also
    aligned the sequences used to generate the reporters on the array
    (in the case of Affymetrix microarrays). This view can be used to
    inspect the quality of a reporter. Note that the reporter
    “242046\_at” is aligned to the genomic region of the MYCN reference
    sequence, but that it’s color is different from the rest (colored
    in red). In addition in this particular case the reporter is also
    located in the intronic (light shaded color) region which is also a
    reason not to pick a certain probeset. Indeed, if we compare the
    gene expression values of this reporter, then its expression is 60
    fold lower than R2's standard pick (22 vs 1,369). Below the ESTs the
    average gene expression of the individual probesets is illustrating
    that for this example the correct probeset is selected for analysis.
    NB: Currently probeset verification is only provided for various
    human Affymetrix array types.


![Figure 6: Color legend](_static/images/OneGene_Colorlegend.png "Figure 6: Color ")

[**Figure 6: Coloring represents type of transcript**](_static/images/OneGene_Colorlegend.png)

  
![Figure 7: MYCN reporters in Transcript view](_static/images/OneGene_Tview.png "Figure 7: MYCN reporters in Transcript view")

[**Figure 7: MYCN reporters in Transcript view**](_static/images/OneGene_Tview.png)



---------------
  ![](_static/images/R2d2_logo.png)***Did you know that you can browse the gene expression values along the genome***

> *Once you have entered the genome browser with an attached dataset (like above), you can also navigate to / zoom out any other region in the genome. This allows you to look at the neighboring genes in a single go.
  What can also be informative is the ability to separate the expression on the basis of a track. This can be achieved by selecting 'dataset\_track' from the sample dropdown in the middle panel. Finally, within the genome browser, the contents for a panel on the left side can be hidden from a view by setting the height to 0.*

---------------


Step 5: TranscriptView
----------------

1.  Close the TranscriptView TAB or go back to the MYCN 1-gene-view
    expression screen.
	
	![Figure 8:Left menu panel providing additional info (including link-out) and analyses options](_static/images/OneGene_menupanel.png "Figure 8:Left menu panel providing additional info (including link-out) andanalyses options")
	
	[**Figure 8:Left menu panel providing additional info (including link-out) and analyses options**](_static/images/OneGene_menupanel.png)
	
In the left upper menu-panel several options are available to provide
you with additional information sources of the MYCN gene and additional
analyses. KaplanScan and Time Series analyses will be discussed in
separate tutorials. GeneCards will redirect you to an overview on your
gene of interest composed of many different resources. ProbePlus, will
provide the sequences probed by the U133 Affymetrix platforms (Will not
be shown in other platforms).
Across datasets will generate an overview showing the average expression
of the gene of interest within all datasets of the same
platform/normalization scheme (provided that the normalization supports
dataset additions).


Clicking on pubsniffer opens a new screen showing a list of how times
your gene of interest is found within the NCBI Pubmed database in
combination with dataset keywords. Clicking on “outlink” redirects you
**to Pubmed Pub-reminer** which is a tool for PubMed query building and
literature mining.

---------------------------------------------------
  ![](_static/images/R2d2_logo.png)***Did you know that the [Pub-reminer](http://hgserver2.amc.nl/cgi-bin/miner/miner2.cgi) is a helpful tool for literature mining***

> *In the large amounts of medical literature, finding information tailored to your needs and interest is becoming more and more complex. Using the right keywords is essential for effective searches, but which ones should you use?
 Pub re-miner is a web-based tool that allows simple text-based query building and information gathering (mining) of the NCBI literature search engine PubMed.
 Pub re-miner presents its results, gathered from abstracts, in frequency tables of journals, authors and words, which can be included / excluded in an iterative fashion.
 Next to building efficient queries, Pub re-miner can also be helpful in other areas: selecting a journal for your current work (by scanning the most often used journals of similar research) Finding experts in a research area (by viewing the authors associated with your query) Determine the research interest of an author (by viewing the keywords associated with an author*

--------------------


Step 6: Adapting plot
---------------


1. To investigate the values R2 uses for graph generation click on
“Datatable” to unfold a table with the expression levels for all
samples.
	
	![Figure 9: Unfold the datatable](_static/images/OneGene_Datatable.png "Figure 9: Unfold the datatable")
	
	[**Figure 9: Unfold the datatable**](_static/images/OneGene_Datatable.png)
	
2. The “track display selection” section can be opened by clicking on it.
In here, you are able to toggle which tracks to display and/or hide
within the YY-plots. Do note that these selections are non-persistent
and will be forgotten as soon as you leave the xgeneview. Persistent,
changes to the tracks can be made via the ‘my settings’ menu item, which
is present in the main screen. Note that the adjustable settings panel
including the customize track parameters are available throughout R2.
	
	![Figure 10: Tick and drag tracks](_static/images/OneGene_trackdisplay.png)
	
	[**Figure 10: Tick and drag tracks**](_static/images/OneGene_trackdisplay.png "Figure 10: Tick and drag tracks")
	
3. Other convenient options are revealed by clicking the “more settings”
section. An extra panel unfolds which allows you to adapt your graph to
meet for example the requirements of a journal. The appearance of this
section will change depending on the kind of graph that you are
selecting.


![Figure 11: the extra settings Panel](_static/images/OneGene_Extrasettings_v1.png "Figure 11: the extra settings Panel")

[**Figure 11: the extra settings Panel**](_static/images/OneGene_Extrasettings_v1.png)



![Figure 12: Adapting a graph](_static/images/OneGene_Adapting.png "Figure 12: Adapting a graph")

[**Figure 12: Adapting a graph**](_static/images/OneGene_Adapting.png)

In Figure 12 sample annotation (“Annot Graph”) and legend (“Draw
Legend”) were added. The “Annot Graph” option, adds the information of a
selected track to the YY-plot. This can be helpful for the addition of
Sample labels, or cell line names etc. Annotations can be shown in 3
ways; just below/on top of the expression value, as a series below the
annotation tracks or at the values for those samples that haven been
marked. The size of the annotation scales with the setting of the
dotsize.The adjustable settings menu is available in most of the R2
modules where a one-or two gene view is generated.



![Figure13: Adapting annotationsize](_static/images/OneGene_Adapting2.png "Figure13: Adapting annotationsize")

[**Figure 13: Legend added**](_static/images/OneGene_Adapting2.png)



Step 7: View a gene in groups
---------------

 1. Thus far, we have been looking at the expression of MYCN ordered by the expression. From the current location, we can also inspect the MYCN expression sub divided in groups. To achieve this, we simply scroll to the end of the page and locate the dropdown box in the 'group separations section of the 'adjustable settings''. Here we can select a track to separate the cohort accordingly. Select 'inss' as a track and press the 'adjust' button at the end of the page. R2 has now separated the patients on the basis of the inss staging track in alphabetical order. 

![Figure14: View in Groups](_static/images/OneGene_ViewInGroups1.png "Figure14: Viewing a gene in groups")

[**Figure 14: View a gene in groups**](_static/images/OneGene_ViewInGroups1.png)

 2. The current representation is the most honest way of showing your data, as every single value is visible in the plot. We can also change the graphical representation of the data by selecting another graph type. Select 'boxplot' from the 'graphtype' dropdown and change 'color by' to 'color by track'. press the 'adjust' button again to change the view. We now obtain a boxplot image where the respective groups have been colored according to the groups. Adaptations to other graphtypes can be made in a similar way.

![Figure15: View in Groups boxplot](_static/images/OneGene_ViewInGroups2.png "Figure15: Viewing a gene in groups by boxplot")

[**Figure 15: View a gene in groups by boxplot**](_static/images/OneGene_ViewInGroups2.png)

-----------
  ![](_static/images/R2d2_logo.png)***Did you know that once you separate a dataset in more than 2 groups, R2 will identify the most significant pair?***

> *If you view a gene in groups within the one-gene-view view page and the number of sub-groups are greater than 2, then R2 will automatically perform a brute-force t-testing to identify the combination of 2 groups that have the most significant difference. Just click on the ‘T-test on combinations’ link underneath the image and gain insight into all the tested combinations. When the number of performed tests exceeds XX, R2 will list the XX most significant tests.*

----------




Step 8: Find best track separation with CliniSnitch
---------------

 1. We could wonder if our gene of interest associates even more with any annotation that is already available for the current dataset (like e.g. age group) than the example in the previous section. For such an analysis R2 has the CliniSnitch function. Within this functionality a brute force T-test is performed on every possible combination of subgroups within every annotation track. We can run a CliniSnitch analysis directly from the one-gene-view page by clicking on the Gene name under CliniSnitch in the left panel. Click on the ‘MYCN’ gene. 


![Figure16: CliniSnitch](_static/images/OneGene_CliniSnitch1.png "Figure16: CliniSnitch representation")

[**Figure 16: CliniSnitch result for MYCN**](_static/images/OneGene_CliniSnitch1.png)

 2. For every track, the most significant test will be highlighted. Every test can also be visualized by clicking on the combination label. Not surprisingly, we can see that MYCN expression is best separated by the MYCN amplification track. If we look at the ‘inss’ track, we can also see that nearly every test containing ‘st4’ has a significant value. Click on ‘st2 vs st4’ to inspect this further.
 3. We are now back in the 'one gene view', but our dataset has been restricted to only those patients that belong to either st2 or st4.




Final remarks / future directions
---------------------------------



Some of these functionalities have been developed recently. If you run
into any quirks or annoyances don't hesitate to contact r2 support
(r2-support@amc.uva.nl).





We hope that this tutorial has been helpful,The R2 support team.



