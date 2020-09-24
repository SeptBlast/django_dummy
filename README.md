# django_dummy

### <b>For Jekins test plz follow bellow steps </b>
---
</br>

## Configuring Jenkins
You need to install three required plugins:
- Violations plugin for parsing pylint reports.
- Cobertura plugin for showing the code coverage.
- Git plugin for source code management.

Install these plugins from Manage Jenkins -> Manage Plugins -> Available.

Start a new job with creating a free-style project via New Item:
</br>
![Create a new freestyle project](https://miro.medium.com/max/700/1*Q8lnuQc2k3_47k3OPLRnOg.png)
</br>Create a new freestyle project

</br>
As our project is a git repository, select the Git option in the source code management.
</br>

![Source Code Management](https://miro.medium.com/max/700/1*elxt4-i4qlEATMSd2kZS1g.jpeg)
</br>Source code management
</br>
</br>Set build triggers.
</br>

![Build triggers](https://miro.medium.com/max/700/1*0yQ2LLWUWVP1b1UgMeT7XQ.png)
</br>Build triggers
</br></br>
I choose to poll the repository on every hour. If there is a change, Jenkins will download it and do the tests.
</br>
Select Add build step -> Execute shell. Add commands to setup environment and the run tests command.
</br>

![Shell Commands](https://miro.medium.com/max/700/1*gEG-VN9IAtl46HQSat1IZg.png)
</br>Execute shell
</br></br>
Select Add post-build action -> Publish Cobertura Coverage Report. Add Cobertura report location.
</br>

![Cobertura coverage report](https://miro.medium.com/max/700/1*4Reqaww4AuItc1urQs1otw.png)
</br>Cobertura coverage report
</br></br>
Select Add post-build action -> Publish JUnit test result report. Add test result report location.
</br>

![JUnit](https://miro.medium.com/max/700/1*l_PcvYoMogkRJjwbz1JTEg.png)
</br>JUnit test result report
</br></br>
Select Add post-build action -> Report Violations. Add locations of violations reports.
</br>

![Report Violation](https://miro.medium.com/max/700/1*SFTMfZmhHGV8KsyTNQIFbw.png)
</br>Report violations
</br></br>
Results:
Press “Build Now” and see what you’ve got:
</br>Code coverage report.
</br>

![Code Coverage](https://miro.medium.com/max/700/1*Pwi5M4Jzot8v7mCZi6ArLQ.png)
</br>Code coverage report
</br></br>
Test result report.
</br>

![Test Result](https://miro.medium.com/max/700/1*WMFY3mKmwmtxl79WeHwARQ.png)
</br>Test result report
</br></br>
Test result and code coverage graph.
</br>

![test result](https://miro.medium.com/max/503/1*6gDX38vRQTibL2RRz14_gg.png)
</br>Test result and code coverage graph
</br></br>
Pep8 and pylint graph.
</br>

![pep8](https://miro.medium.com/max/700/1*ms6k5F3GA9L0pPS0IyfelQ.png)
</br>Pep8 and pylint graph
</br></br></br>
Finished…..:)