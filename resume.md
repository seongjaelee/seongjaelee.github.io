---
layout: page
title: Resume
lang: en
date: 2024-10-24
last_modified_at: 2024-10-24
summary: Resume of Seongjae Lee, a machine learning software engineer in Seattle.
tags: [resume,Seongjae Lee,Seong Jae Lee,Google Maps]
---

## Seongjae Lee

- A software engineer interested in:
  - building and maintaining reliable machine learning pipelines, and
  - building a development environment promoting flexible and rapid ML research.
- seongjae@gmail.com
- [LinkedIn](https://www.linkedin.com/in/seongjae-lee-23028359/)
- [GitHub](https://github.com/seongjaelee)

## Skills
- **Programming Experience**: C++, Python, Google BigQuery, TypeScript, Java, C#, JavaScript, Dart, HTML/CSS
- **Frameworks and Tools**: Vertex AI, Google Dataflow, TFX, TensorFlow, Jupyter Notebook, pandas, AngularJS, AngularDart, GWT, jQuery, HavokAI, OpenGL
- **Languages**: English, Korean

## Experience
- **Senior Software Engineer**, Traffic AI, Geo, Google, Seattle (2018–Present)
  - Developed, launched, maintained, and decommissioned ML models for traffic prediction.
  - Built and maintained ML pipelines encompassing training, evaluation, deployment, serving, logging, tooling, and monitoring.
  - Improved ML models by adding input features, enhancing data quality, addressing discrepancies between training and serving data/code, and optimizing model architectures.
  - Monitored, investigated, and resolved model quality regressions.
  - Maintained and optimized batch pipelines processing petabytes of data on Google Dataflow.
  - Mainly used C++, Google BigQuery, Python, Google Dataflow, TFX, Vertex AI, Tensorflow, Jupyter Notebook, and pandas.
- **Software Engineer**, Cloud Endpoints, Google, Seattle (2017–2018)
  - Developed scalable web pages and components for managing service quotas and usages in AngularJS, JavaScript, TypeScript, and Java.
  - Built a scalable web page that visualizes API usages for +1000 hierarchical projects.
- **Software Engineer**, AdWords DoubleClick Search, Google, Seattle (2014–2017)
  - Developed scalable web pages and components for ads bidding strategy and bidding state monitoring in GWT, AngularDart, and Java.
  - Designed and developed a budget optimization feature.
  - Built a backend batch job building monthly invoices for customers.
- **Research Assistant**, [Center for Game Science](https://centerforgamescience.org/), University of Washington (2013–2014)
  - Built a ML model predicting individual player behaviors from play history in different educational games without game-specific domain models.
- **Game Developer**, [NCSOFT](https://kr.ncsoft.com/en/index.do), Seoul (2010–2013)
  - Developed a massively multiplayer online role-playing game (MMORPG).
  - Built a client-side game library handling pathfinding and character animation.
  - Built and refined tools for character animators and game map designers.
- **Research Assistant**, [Graphics and Imaging Laboratory](https://grail.cs.washington.edu/), University of Washington (2007–2010)
  - Researched controlling biped characters with mocap animation data.
  - Used reinforcement learning and inverse reinforcement learning (IRL) to learn data-based biped character controllers.
- **Intern**, Microsoft Research, Redmond (Summer of 2008)
  - Built an animation framework for avatars in a virtual world.
- **Research Assistant** of [Professor Amy Greenwald](http://cs.brown.edu/people/faculty/amy/), Brown University (2005–2007)
  - Worked on trading agents design and analysis.
  - Won in the annual [Trading Agent Competition (TAC)](https://strategicreasoning.org/trading-agent-competition/) with our agent RoxyBot in 2006.
  - Used integer linear programming (ILP) to model competitors, predict bidding prices, and compute the best bidding strategy.
- **Research Assistant**, [Center for Computation & Visualization](https://ccv.brown.edu/), Brown University (Summer of 2006)
  - Worked on visualization and user interface for CAVE(CAVE Automatic Virtual Environment), a virtual environment using 3D glasses.

## Selected Projects

### Model Modernization (2023-Present)

This project focused on modernizing a complex machine learning system with over ten years of legacy layers of models, as the interdependency has been slowing down making improvements on any component. The goal was to consolidate numerous entangled layers of models into a single deep learning model, without sacrificing quality. I joined this 3-year-old six-person team to improve the model to match the performance of the existing production system, and productionize it. We achieved a partial launch in 2024, reducing system complexity, accelerating model development cycle, while improving ETA quality. I am currently working on launching the model globally and decommissioning the old systems.

My contributions include:

- Reducing discrepancies between training and serving data and code.
- Introducing critical model input features previously used in legacy models.
- Prioritizing the direction of future model research.
- Building an online model evaluation pipeline.
- Improving the model training pipeline with a focus on scalability and reliability.
- Investigating and resolving quality regressions.

### Graph Neural Network Model (2018-2021)

This project, conducted in collaboration with DeepMind, focused on enhancing Google Maps ETA predictions using Graph Neural Networks applied to frequently visited predefined road networks. I joined this 2-year-old three-person team to improve and productionize the model. We achieved a global launch in 2020, which reduced inaccurate ETA trips by up to 50% in heavily congested urban areas. This project is detailed further in the associated [blog post][2] and [research paper][1].

My contributions include:

- Enhancing the model with new features.
- Investigating and resolving quality regressions.
- Building and maintaining the model training pipeline.
- Implementing model serving on existing servers.
- Designing, executing, and analyzing experiments.
- Setting up quality monitoring.
- Building and maintaining an automated ML pipeline for periodic model retraining and deployment.

[1]: https://arxiv.org/abs/2108.11482
[2]: https://deepmind.com/blog/article/traffic-prediction-with-advanced-graph-neural-networks

## Education
- University of Washington, Seattle
  - Ph.D. student in Computer Science and Engineering (did not finish)
  - Master in Computer Science and Engineering
- Brown University
  - Bachelor of Science in Mathematics and Computer Science
  - Magna cum laude, Honors in Computer Science
- Seoul National University
  - Electrical and Computer Engineering (did not finish)

## Publications
- Austin Derrow-Pinion, Jennifer She, David Wong, Oliver Lange, Todd Hester, Luis Perez, Marc Nunkesser, Seongjae Lee, Xueying Guo, Brett Wiltshire, Peter W. Battaglia, Vishal Gupta, Ang Li, Zhongwen Xu, Alvaro Sanchez-Gonzalez, Yujia Li, and Petar Veličković. (2021)
  ETA Prediction with Graph Neural Networks in Google Maps.
  Proceedings of the 30th ACM International Conference on Information & Knowledge Management (CIKM 2021)
  [[arxiv.org]](https://arxiv.org/abs/2108.11482)
- Seong Jae Lee, Yun-En Liu and Zoran Popović. (2014)
  Learning Individual Behavior in an Educational Game: A Data-Driven Approach.
  Proceedings of 7th International Conference on Educational Data Mining (EDM 2014)
  [[paper:pdf]][p-edm]
- Seong Jae Lee and Zoran Popović. (2010)
  Learning Behavior Styles with Inverse Reinforcement Learning.
  ACM Transactions on Graphics Vol. 29 Num. 3 (SIGGRAPH 2010)
  [[paper:pdf]][p-irl-pdf] [[webpage]](http://grail.cs.washington.edu/projects/learning-behavior-styles/)
- Yongjoon Lee, Seong Jae Lee and Zoran Popović. (2009)
  Compact Character Controllers. ACM Transactions on Graphics Vol. 28 Num. 5 (SIGGRAPH Asia 2009)
  [[paper:pdf]][p-ccc-pdf] [[webpage]](http://grail.cs.washington.edu/projects/trans-graph/s2009/)
- Amy Greenwald, Seong Jae Lee and Victor Naroditskiy. (2008)
  Bidding Heuristics for Simultaneous Auctions: Lessons from TAC Travel.
  AAAI-08 Workshop on Trading Agent Design and Analysis.
  [[webpage]](https://www.aaai.org/Library/Workshops/2008/ws08-12-001.php)
- Seong Jae Lee. (2007)
  Comparison of Bidding Algorithms in Simultaneous Auctions.
  Bachelor of Science Honors Thesis.
  [[paper:pdf]][p-thesis-pdf] [[presentation:pdf]][p-thesis-ppt]
- Seong Jae Lee, Amy Greenwald, Victor Naroditskiy. (2007)
  RoxyBot-06: An (SAA)² TAC Travel Agent.
  International Joint Conferences on Artificial Intelligence.
  [[paper:pdf]][p-ijcai-pdf] [[presentation:pdf]][p-ijcai-ppt]
- Marc ten Bosch, Seong Jae Lee. (2006)
  Restricted Coloring Using Saliency-Based Image Segmentation.
  SIGGRAPH 2006, Poster.
  [[abstrct:pdf]][p-siggraph-pdf]
- Amy Greenwald, Seong Jae Lee and Victor Naroditskiy. (2006)
  Heuristics for the Deterministic Bidding Problem: Lessons from TAC Travel. Tech Report CS-06-15, Computer Science Department, Brown University [[webpage]](https://cs.brown.edu/research/pubs/techreports/reports/CS-06-15.html)

[p-edm]: /assets/resume/learning%20individual%20behavior.pdf
[p-irl-pdf]: http://grail.cs.washington.edu/projects/learning-behavior-styles/learning%20behavior%20styles.pdf
[p-ccc-pdf]: http://grail.cs.washington.edu/projects/trans-graph/s2009/compact-character-controllers.pdf
[p-thesis-pdf]: /assets/resume/07.thesis.pdf
[p-thesis-ppt]: /assets/resume/07.thesis.presentation.pdf
[p-ijcai-pdf]: /assets/resume/07.ijcai.roxybot.pdf
[p-ijcai-ppt]: /assets/resume/07.ijcai.roxybot.presentation.pdf
[p-siggraph-pdf]: /assets/resume/06.siggraph.segmentation.abstract.pdf
[p-siggraph-poster]: /assets/resume/06.siggraph.segmentation.poster.pdf
