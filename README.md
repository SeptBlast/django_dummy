# django_dummy

### <b>For Jekins test plz follow ellow steps </b>
---
</br>

## Configuring Jenkins
You need to install three required plugins:
- Violations plugin for parsing pylint reports.
- Cobertura plugin for showing the code coverage.
- Git plugin for source code management.

Install these plugins from Manage Jenkins -> Manage Plugins -> Available.

Start a new job with creating a free-style project via New Item:

![Create a new freestyle project](https://miro.medium.com/max/700/1*Q8lnuQc2k3_47k3OPLRnOg.png)
Create a new freestyle project

</br>
As our project is a git repository, select the Git option in the source code management.

![Source Code Management](https://miro.medium.com/max/700/1*elxt4-i4qlEATMSd2kZS1g.jpeg)
Source code management
</br></br>
Set build triggers.
![Build triggers](https://miro.medium.com/max/700/1*0yQ2LLWUWVP1b1UgMeT7XQ.png)
Build triggers
</br></br>
I choose to poll the repository on every hour. If there is a change, Jenkins will download it and do the tests.

Select Add build step -> Execute shell. Add commands to setup environment and the run tests command.

![Shell Commands](https://miro.medium.com/max/700/1*gEG-VN9IAtl46HQSat1IZg.png)
Execute shell
</br></br>
Select Add post-build action -> Publish Cobertura Coverage Report. Add Cobertura report location.

![Cobertura coverage report](https://miro.medium.com/max/700/1*4Reqaww4AuItc1urQs1otw.png)
Cobertura coverage report
</br></br>
Select Add post-build action -> Publish JUnit test result report. Add test result report location.

![JUnit](https://miro.medium.com/max/700/1*l_PcvYoMogkRJjwbz1JTEg.png)
JUnit test result report
</br></br>
Select Add post-build action -> Report Violations. Add locations of violations reports.
![Report Violation](https://miro.medium.com/max/700/1*SFTMfZmhHGV8KsyTNQIFbw.png)
Report violations
</br></br>
Results:
Press “Build Now” and see what you’ve got:
Code coverage report.
![Code Coverage](https://miro.medium.com/max/700/1*Pwi5M4Jzot8v7mCZi6ArLQ.png)
Code coverage report
</br></br>
Test result report.
![](https://miro.medium.com/max/700/1*WMFY3mKmwmtxl79WeHwARQ.png)
Test result report
</br></br>
Test result and code coverage graph.
![test result](https://miro.medium.com/max/503/1*6gDX38vRQTibL2RRz14_gg.png)
Test result and code coverage graph
</br></br>
Pep8 and pylint graph.
![pep8](https://miro.medium.com/max/700/1*ms6k5F3GA9L0pPS0IyfelQ.png)

Pep8 and pylint graph
</br></br>
Finished…..:)