# Megafon_Statistical_Analysis

The dataset contains responses to two survey questions on improving the quality of Megafon cellular and internet service. It also has technical data for each respondent. The goal of the analysis is to predict which of the technical features affect the satisfaction of the clients with the service most. With this purpose in mind, methods like Logistic Regression, plotting confidence intervals, and Bootstrap have been used in this project.

The `preprocess.ipynb` notebook contains a Python script for preprocessing data (removing invalid entries, changing the formatting of the dataset, etc.) while most of the statistical work is done in the `Megafon_Stat_Analysis.Rmd` R-notebook.

## Codebook

`megafon.csv` contains the following columns: <br><br>
&nbsp;&nbsp;&nbsp;&nbsp; `user_id` — customer's unique id;<br>
&nbsp;&nbsp;&nbsp;&nbsp; `Q1` — response to the first question;<br>
&nbsp;&nbsp;&nbsp;&nbsp; `Q2` — response to the second question;<br>
&nbsp;&nbsp;&nbsp;&nbsp; `Total Traffic(MB)` — the volume of data transfer traffic <sup>1 </sup>; <br>
&nbsp;&nbsp;&nbsp;&nbsp; `Downlink Throughput(Kbps)` — average downlink throughput <sup>2 </sup>;<br>
&nbsp;&nbsp;&nbsp;&nbsp; `Uplink Throughput(Kbps)`— average uplink throughput <sup>3 </sup>;<br>
&nbsp;&nbsp;&nbsp;&nbsp; `Downlink TCP Retransmission Rate(%)` — retransmission frequency <sup>4 </sup>;<br>
&nbsp;&nbsp;&nbsp;&nbsp; `Video Streaming Download Throughput(Kbps)` — video streaming speed <sup>5 </sup>;<br>
&nbsp;&nbsp;&nbsp;&nbsp; `Video Streaming xKB Start Delay(ms)` — delay before starting to stream the video <sup>6 </sup>;<br>
&nbsp;&nbsp;&nbsp;&nbsp; `Web Page Download Throughput(Kbps)` — web page loading speed through web browser <sup>7 </sup>;<br>
&nbsp;&nbsp;&nbsp;&nbsp; `Web Average TCP RTT(ms)` — delay while viewing web pages<sup>8 </sup>.<br>

<sup>1 </sup> — How actively the customer uses mobile internet.<br>
<sup>2 </sup> — Calculated based on the entire data traffic.<br>
<sup>3 </sup> — Calculated based on the entire data traffic.<br>
<sup>4 </sup> — The higher the worse.<br>
<sup>5 </sup> — The higher the better.<br>
<sup>6 </sup> — The lower this value, the faster the video starts playing.<br>
<sup>7 </sup> — The higher the better.<br>
<sup>8 </sup> — The lower the better - web pages load faster.<br>

The first technical feature is a sum over a one week period before participating in the survey. All other technical features are an average over a one week period before participating in the survey.
