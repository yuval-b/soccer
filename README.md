# soccer
### Temporal Match Analysis and Recommending Substitutions in Live Soccer Games

Authors:
Yuval Berman, Dr. Sajib Mistry, Prof. Aneesh Krishna, PhD.

This repository contains all the source code and references for the 2021/22 Pawsey Summer Internship.

Uncertainty is an intrinsic feature in a live soccer game. Teams continuously adapt to the situation in the game, applying new tactical formations, substituting players, and so on. Due to this fluid nature, dynamic decision making is normally driven by human experts; the coaches.
As the live game generates a lot of data in a very short period, effective analysis of dynamics in the game would provide valuable new insight and enable coaches to deploy data-backed, real time decisions to impact the game's outcome. 
We investigate using network metrics and event logs data to correlate temporal network metrics to match prediction and use those results in order to recommend substitutions based on performance of players and wider team tactics.

## Code Notebooks Explanations:

Listed in chronological order.

**Data Cleaning:** this notebook 'cleans' the initial event logs data into more usable form- stored as 'cleaned_events/events_COUNTRY.json'. Credit to J. Makins for this code.

**SoccerNets**: this notebook takes the 'cleaned' event logs data and generates networks on ten minute sliding windows. It calculates a host of key metrics for each network and saves them into dataframes, each dataframe is for one country on one metric- it includes all games in the country and the trajectories of that particular metric for each game.

**Multivariate TimeSeries predictions:** this notebook takes the input from above and uses multivariate timeseries classification algorithms to assign each timeseries to a particular match outcome (win, draw, loss).




## References:

[1]  J.  Makins,  S.  Mistry,  A.  Krishna,  and  M.  S.  Islam,  “Fdnn-based  feature  extraction  and prediction modeling in live soccer analytics,” Under review, 2021.

[2] A. Bialkowski, P. Lucey, P. Carr, Y. Yue, S. Sridharan, and I. Matthews, “Identifying teamstyle in soccer using formations learned from spatiotemporal tracking data,” in Proceedings of  the  14th  IEEE  International  Conference  on  Data  Mining  Workshops (X.  Wu,  J.  Pei,Z. H. Zhou, W. Wang, R. Kumar, J. Z. Huang, and H. Toivonen, eds.), pp. 9–14, UnitedStates of America:  Institute of Electrical and Electronics Engineers Inc., 2014

[3]  C. Merhej, R. Beal, S. D. Ramchurn, and T. Matthews, “What happened next?  using deeplearning  to  value  defensive  actions  in  football  event-data,”CoRR,  vol.  abs/2106.01786,2021.

[4] G. Liu and O. Schulte, “Deep reinforcement learning in ice hockey for context-aware playerevaluation,” inProceedings of the Twenty-Seventh International Joint Conference on Arti-ficial  Intelligence,  IJCAI-18, pp. 3442–3448, International Joint Conferences on ArtificialIntelligence Organization, 7 2018

[5] B. Skinner, “The price of anarchy in basketball,”Journal of Quantitative Analysis in Sports,vol. 6, Jan 2010

[6] J. Xie, R. B. Girshick, and A. Farhadi, “Unsupervised deep embedding for clustering anal-ysis,”CoRR, vol. abs/1511.06335, 2015.

[7]  J. Gudmundsson and M. Horton, “Spatio-temporal analysis of team sports,”ACM  Com-puting Surveys, vol. 50, p. 1–34, Jun 2017.

[8] T. Decroos, J. Van Haaren, and J. Davis, “Automatic discovery of tactics in spatio-temporalsoccer  match  data,”  inProceedings  of  the  24th  ACM  SIGKDD  International  Conferenceon  Knowledge  Discovery    Data  Mining,  KDD  ’18,  (New  York,  NY,  USA),  p.  223–232,Association for Computing Machinery, 2018.

[9] J. H. Mart ́ınez, D. Garrido, J. L. Herrera-Diestra, J. Busquets, R. Sevilla-Escoboza, andJ. M. Buld ́u,  “Spatial and temporal entropies in the spanish football league:  A network science perspective,”Entropy, vol. 22, no. 2, 2020.

[10] F. Clemente, M. Couceiro, F. Martins, and R. Mendes, “Using network metrics in soccer:A macro-analysis,”Journal of Human Kinetics, vol. 45, pp. 123–134, 03 2015.

[11] J. M. Buld ́u, J. Busquets, J. H. Mart ́ınez, J. L. Herrera-Diestra, I. Echegoyen, J. Galeano,and  J.  Luque,  “Using  network  science  to  analyse  football  passing  networks:   Dynamics,space, time, and the multilayer nature of the game,”Frontiers in Psychology, vol. 9, p. 1900,2018

[12]  G. Suzuki, S. Takahashi, T. Ogawa, and M. Haseyama, “Team tactics estimation in soccervideos based on a deep extreme learning machine and characteristics of the tactics,”IEEEaccess, vol. 7, pp. 153238–153248, 2019

[13] M. H. Rønningen, “The genesis of data-driven decision-making in the world of soccer tactics:  deciphering the potential of big data,” 2021.
