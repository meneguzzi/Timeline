# Timeline
**Convert Markdown timeline to Graphviz DOT**

![Example timeline](README.md.dot.svg)

Timeline converts parts of Markdown to Graphviz [DOT](https://en.wikipedia.org/wiki/DOT_%28graph_description_language%29 "Graph description language"):
- ``<!--class color-->`` to set following nodes class and color
- ``[node]: http://www.website.com "optional tooltip"`` to set node external link and tooltip
- ``## cluster`` to a cluster
- ``- [node] description`` to a node of the cluster

Node class, color, external link and tooltip are optional, but are expected to be defined before their respective nodes appear.
Edges between nodes of the same cluster are possible.
Nodes defined before the first cluster are considered free.
This README is actually a valid input, open the [raw](https://raw.githubusercontent.com/Maumagnaguagno/Timeline/master/README.md) file to see the links.

There are two implementations available.
The first one in Ruby reads a Markdown file and direction, ``README.md`` and ``LR`` by default, and outputs a DOT file.
This DOT file contains a graph representation of the timeline, which can be converted into an image format by Graphviz.
By using a combination of a HTML and SVG output one can obtain a static timeline page.
SVG output is recommended to take full advantage of links and tooltips, see the result [here](http://maumagnaguagno.github.io/Timeline/static.html).

```Shell
ruby timeline.rb README.md LR                   # Generate Left to Right DOT file
dot README.md.dot -O -T svg                     # Generate SVG file
```

The second one is implemented in JavaScript and focuses on client-side rendering with [d3-graphviz](https://github.com/magjac/d3-graphviz).
This removes the need to install any specific tools, while adding interactivity.
This version is able to read a Markdown file ([limited to GitHub](https://en.wikipedia.org/wiki/Cross-origin_resource_sharing)) and direction from an URL query, edit, display and download their content and graph, see the result [here](http://maumagnaguagno.github.io/Timeline).

```
https://maumagnaguagno.github.io/Timeline?from=https://maumagnaguagno.github.io/Timeline/README.md&dir=LR
```

Everything below is valid input for Timeline.

<!--class1 #ff8888-->
[IJCAI]: http://www.ijcai.org/ "International Joint Conference on Artificial Intelligence"
<!--class4 #ff88d1ff-->
[UAI]: http://auai.org/uai2017/index.php "Conference on Uncertainty in Artificial Intelligence"
[IROS]: http://www.iros.org/ "International Conference on Intelligent Robots and Systems"
<!--class1 #ff8888-->
[ECAI]: http://www.ecai2016.org/ "European Conference on Artificial Intelligence"
<!--class2 #88ff88-->
[IAT]: http://wibih.unomaha.edu/wi "International Conference on Intelligent Agent Technology"
<!--class4 #ff88d1ff-->
[SBGames]: http://sbgames.org/ "Simposio Brasileiro de Games e Entretenimento Digital"
[AIIDE]: http://aiide.org
[ICRA]: http://www.icra2017.org/ "International Conference on Robotics and Automation"
[SAC]: http://www.sigapp.org/sac/ "Symposium On Applied Computing"
<!--class1 #ff8888-->
[AAAI]: http://www.aaai.org/Conferences/conferences.php "Association for the Advancement of Artificial Intelligence"
<!--class2 #88ff88-->
[EUMAS]: http://eumas-at2016.webs.upv.es/EUMAS2016.html "European Conference on Multi-Agent Systems"
[ICAART]: http://www.icaart.org/ "International Conference on Agents and Artificial Intelligence"
[ICAPS]: http://www.icaps-conference.org/ "International Conference on Automated Planning and Scheduling"
[AAMAS]: http://www.ifaamas.org/ "International Conference on Autonomous Agents and Multiagent Systems"
<!--class1 #ff8888-->
[FLAIRS]: http://www.flairs.com/ "Florida Artificial Intelligence Research Society"
<!--class2 #88ff88-->
[KR]: http://www.kr.org/ "International Conference on Principles of Knowledge Representation and Reasoning"
[ICLP]: http://software.imdea.org/Conferences/ICLP2016/ "International Conference on Logic Programming"
<!--class3 #8888ff-->
[NeurIPS]: https://neurips.cc "Conference on Neural Information Processing Systems"
[ICML]: https://icml.cc "Conference on Neural Information Processing Systems"
[ICCV]: https://www.thecvf.com "International Conference on Computer Vision"
[CVPR]: https://www.thecvf.com "Conference on Computer Vision and Pattern Recognition"
[BMVC]: https://bmvc2020-conference.com "British Machine Vision Conference"

## January

- [IJCAI] Abstracts Submission
- [ICML] Abstracts

## February

<!-- - [IJCAI] Submission -->
- [ICML] Submission
- [UAI] Submission
- [KR] Abstracts Submission

## March

- [IROS] Submission
- [ICCV] Abstracts Submission

## April

- [IJCAI] Notification
- [ECAI] Submission
- [IAT] Submission
- [ICLP] Abstracts Submission
- [BMVC] Abstracts Submission
- [KR] Notification

## May

- [NeurIPS] Abstracts Submission
- [ICML] Notification
- [IAT] Notification

## June

- [ECAI] Notification
- [UAI] Notification
- [IROS] Notification
- [ICLP] Notification
- [AIIDE] Submission


## July

- [SBGames] Abstracts Submission
- [ICCV] Notification
- [BMVC] Notification
- [ICML] Conference
- [KR] Conference

## August

- [SBGames] Notification
- [IJCAI] Conference

## September

- [ICRA] Submission
- [SAC] Abstracts Submission
- [AAAI] Abstracts Submission
- [EUMAS] Submission
- [NeurIPS] Notification

## October

- [EUMAS] Notification
- [ICAART] Submission

## November

- [AAAI] Notification
- [SAC] Notification
- [ICAPS] Abstracts Submission
- [AAMAS] Abstracts Submission
- [FLAIRS] Submission
- [ICAART] Notification
- [CVPR] Abstracts Submission

## December

- [AAMAS] Notification

## January

- [ICRA] Notification
- [ICAPS] Notification
- [FLAIRS] Notification
- [AAAI] Conference

## February

- [CVPR] Notification

## May

- [AAMAS] Conference

## June

- [ICAPS] Conference