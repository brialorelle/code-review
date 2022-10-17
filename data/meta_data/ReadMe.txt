###########################################################
# THINGS+ NORMS & METADATA
###########################################################

GENERAL VARIABLES: 
- Word: THINGS concept noun
- uniqueID: unique concept ID
- subject_Nr: idenitifier for individual subjects
- N_ratings: number of ratings per object concept or image
- set_Nr: identifier for individual Amazon Mechanical Turk (AMT) HITs
- trial_Nr: identifier for individual trials in a specific HIT
- work_time: completion time (ms) of the trial
- work_time_mean: average completion time (ms) of the trials per object concept or image 
- work_time_SD: standard deviation of the average completion time per object concept or image
- age: age of the AMT worker
- gender: gender of the AMT worker

# ----------------------------------------------------------
"arousal_meanRatings.tsv"
- = Arousal ratings of the follow-up arousal experiment
- arousing_mean: mean arousal score (1 “very calming” to 7 “very arousing”)
- arousing_SD: Standard deviation of the mean arousal score
	
"objectProperties_meanRatings.tsv"
- = mean object property ratings per object concept (1 to 7), includes the deprecated arousal ratings 
- e.g. manmade_mean: mean manmadeness ratings per object concept
- e.g. manmade_SD: standard deviations of the mean manmadeness ratings
- TrialRating_SD: standard deviation of the ratings over all 11 items/properties 
	
"frequency_mat_manmade.tsv"; "frequency_mat_precious.tsv" "frequency_mat_heavy.tsv" etc. 
- = absolute rating frequencies of the object properties 
- e.g. pleasant_freq_1: how often the object was rated as 1 “very unpleasant”   
- .... 
- e.g. pleasant_freq_7: how often the object was rated as 7 “very pleasant” 

# ----------------------------------------------------------
"typicality_trialwise_wideFormat.tsv"
- = trial-wise results of the typicality task 
- category: higher-level category
- (NOTE: gorilla was mistakenly sampled as a member of the "food" category"

"typicality_objectwise_longFormat.tsv"
- = mean typicality ranks per members of all 53 categories
- typicality: mean typicality rank of the concept for the respective higher-level category
- (NOTE: Typicality ranks were inverted, so high scores represent high typicality and low scores low typicality)
- (NOTE2: mean typicality score of gorilla for "food" was removed)

# ----------------------------------------------------------
"category53_longFormat.tsv"
- membership associations for the 53 higher-level categories (long format)


"category53_wideFormat.tsv"
- membership associations for the 53 higher-level categories (wide format)
- 1 = member
- 0 = not a member

# ----------------------------------------------------------
"imageLabeling_imagewise.tsv"
- = results for all 26,107 images
- alternative_label: alternative spelling of the THINGS concept noun (e.g. "yo-yo" vs. "yo yo" vs. "yoyo")
- WordNet_Synonyms: Synonyms of the THINGS object noun derived from WordNet (Fellbaum, 1998)
- label1: participant generated labels for the prominent object depicted in each images 
- label1_moreEdit: additional corrections of label1, removal of over-specific labels e.g. ("green acorn" to "acorn", "shepherd dog" to "dog"). 
--- Note: we corrected labels which included the THINGS concept word 
- label2: labels for all other objects in the image (e.g. in the background)
- most_frequent_rating: most frequently used label by the participants (regardless if correct)
- naming_consistency: fraction of the most frequently used label 
- nameability: fraction of labels identical to the THINGS object noun
- recognizability: fraction of labels identical to the THINGS object noun or synonymous to the WordNet Synonym
- SE_nameability; SE_recognizability; SE_naming_consistency: Standard error of the scores	

"imageLabeling_objectwise.tsv"
- = results for the 1,854 object concepts (averaged over all images depicting the respective object)
- ... see above
- mean_ratingsPerImage: average number of responses per object concept (averaged over all images depicting the object)
- nameability_mean; recognizability_mean; consistency_mean: mean score (averaged over all image examples) 	
- nameability_SD; recognizability_SD; consistency_SD: standard devitaions of the mean scores	
- SE_nameability_mean; SE_recognizability_mean; SE_consistency_mean: standard errors of the eman scores

# ----------------------------------------------------------
"size_trialWise.tsv"
- = trial-wise size ratings
- WordContext: object nouns as they were depicted in the experiment (including contextual information for homonyms, e.g. bat (sports) vs. bat (animal))
- noSize: 1 = object has not size
- notKnow: 1 = worker does not know the object concept
- ratingLevel1: rating on Level1 of the rating-task (approximate size)
--- (NOTE: if value = None the worker indicated no size range (e.g. only clicked on the scale once)
- RangeStart: start point of the size range (0 to 520 units)
- RangeEnd: end point of the size range 
- RangeLength: Length of the size range (RangeEnd - RangeStart)
- Size: perceived size of the object concept (= mean point on the size range)

"size_meanRatings.tsv"
- = object-wise results, averaged over trials
-  ... see above
- N_noSize: number of trials in which the object was rated to have no size
- N_notKnow: number of trials in which the worker did not know the object
- N_noRange: number of trials in which the object had no range
- RangeStart_mean; RangeEnd_mean; RangeLength_mean: mean sart, end and length of the size range
- Size_mean: mean size rating of the object
- RangeStart_SD; RangeEnd_SD; RangeLength_SD; Size_SD: standard deviations