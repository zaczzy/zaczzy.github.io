# Zachary Zhao
Software engineer at my core, aspiring linux engineer.
## I'm Zach. Nice to meet you.
- [If you want to see my Resume](https://drive.google.com/file/d/1MitwAobv6OKL9T2PmZlmldUreXOQ35vA/view?usp=sharing)
- [If you want to see my LinkedIn profile and maybe say hi](https://www.linkedin.com/in/zzzhao/)

## My undergradate major: what is NETS?
Networked and social systems engineering, or NETS, is a UPenn special program aimed to help students with interdisciplinary interests in Computer Science, Systems engineering and Economics. It allowed students to pursue a traditional CS major, specialize in network science, data science, systems engineering, economics, communications or anything in-between.

**A solid CS traditional training**

In my case, I had a traditional CS experience, but also utilized the additional freedom of the curriculum to prioritize certain CS courses over others.

Specifically, I have taken all courses required for the CS undergrad, except the following two:
1. CIS 262 Automata, Computability, and Complexity (I have taken a more advanced version of this course: CIS 511, as a graduate)
2. CIS 471	Computer Organization and Design (The "hardware" course in our CS department. Unfortunately our professor has been on sabbatical so I couldn't take this course during my stay at UPenn.)

But I have taken many more CS courses than required. Also, I have always optted for the more challenging version of the same course. (e.g. CIS 520 over CIS 519 on machine learning, MATH 314 advanced linear algebra over MATH 312 the normal version.)
By taking the hardest challenges head-on, I can proudly declare that my undergraduate education is much more transformative and fullfilling than a traditional CS major.

**Something a little more**

Any CS faculty @Penn holds the NETS student at the same technical proficiency requirement as the CS (named CIS @ UPenn) student. In fact, the transfer process between the two majors is as easy as submitting a form in Sophomore year. But the NETS faculty imposes additional expectation for young NETS scholars. These tailored NETS courses are so useful that CS students often consider it a requirement as well:
1. [NETS 212](https://nets212.seas.upenn.edu/): scalable and cloud computing. The ONLY undergrad level course that introduces real cloud computing concepts.
2. NETS 312: theory of networks. This is the de-facto network science course.
3. [NETS 412](https://www.cis.upenn.edu/~aaroth/courses/agtS17.html): algorithmic game theory. Well, it's advanced game theory that focuses on welfare, pricing and games from a network of actors. It's more difficult than all of my data stuctures and algorithm courses combined. It's exceptionally well taught by our young and brilliant Prof. Aaron Roth. Enough said. 

**Summary**

For any potential employer, you can view my transcipt to see that my education is more technical than the average CS major. At times, I challenged myself to beyond my capabilities, which was foolish. But I always kept trying.

Please don't let the major NETS confuse you. It just means CS(+?) in my case.

**For your reference**

- [CS program requirement](https://catalog.upenn.edu/undergraduate/programs/computer-science-bse/)
- [NETS program requirement](https://www.nets.upenn.edu/long/nets-curriculum)
- My transcipt trackrecord aligns well with both programs.

## Projects
### Internship projects
**Starboard Ventures Database**
I constructed and maintained a virtual machine running several Docker containers on AWS/GCP/Azure cloud to store on-chain metrics collected by a [Lotus](https://spec.filecoin.io/), the Filecoin implementation.
The work is on-going and currently I am experimenting with GCP container-optimized OS running Lotus, Visor, TimescaleDB and Grafana. In the future, we may migrate to AWS for long-term service.
My current work is studying the Filecoin implemenation to make changes to [Visor](https://github.com/filecoin-project/sentinel-visor) (Implemented in Go), which capture additional metrics; the most important work is query optimization and overall management of the database server running Docker. I architect the infrastructure for server as well as investigate the performance of timescaledb and visor to ensure the most up-to-date information is gathered. (The challenge is every 30 seconds an epoch is updated, and data grows at 27GB per day.)
My additional duties include product feature development and DevOps support for Starboard's miner profitability predictor (Angular + Express). CI/CD with Jenkins.

**Infervision RCNN CV Product**
My primary duty is develop internal tools for better image segmentation task on their faster-RCNN product. I augmented their X-ray&CT scan DICOM datasets, implemented transformation matrices for their volume data, and developed a basic interactive teaser website for an event. 
Additionally, I set up Ubuntu workstations for new employees and helped provide manual labels for image segmentation.

### Research projects
**DeDOS testing and debugging for Deterlab**
For one year, I was a research assistant at the Distributed Systems Lab @UPenn. I helped Isaac, a full-time programmer, researcher, and graduate student and Henri (Max), a PhD student at the time to debug and present their work on the [DeDOS project](https://dedos.cis.upenn.edu/) ([Paper hosted by Prof. Linh T. X. Phan](cis.upenn.edu/~linhphan/papers/acsac18-dedos.pdf)) to Deterlabs to see if the system indeed delivers on its promise.
Due to the limitations of my time and technical expertise, I primarily focused on understanding the source code and one application written on top of the DeDOS infrastructure, the HTTP web server. I studied how the web server is divided into units of execution named Minimum Splitable Units and how the DeDOS system replicate and allocate these MSUs across thread workers on different machines.
In the meantime, I helped to debug a few minor functional bugs and primarily helped gathering experiment materials to present to representives from [Deterlab, ISI](https://www.isi.deterlab.net/index.php3), who is tasked to examine the performance claims made by the paper. 
### Course projects
In order of decreasing time and complexity, I will list the largest projects I have completed @UPenn here:

1. "Penn Drive": an application that aims to help use learn some core aspects of a distributed system: parallelism, primary replication with remote writes, sequential constistency, fault recovery via snapshot replay. As part of a 4 student team, I developed the multi-threaded test client, the admin server, the frontend server and the communication protocol and API with Michal. I helped with the "Google Big Table" key-value store implementation and the primary replication with remote write implementation, but my teammates are mainly responsible for that.
The end application supports: 
    1. SMTP email service (CRUD)
    2. Cloud storage: files (CRUD)
    3. An admin console to see node health and store state

2. "Penn Google Search": an application written using Penn's proprietary "Apache Storm Lite" Java framework to crawl, index and store more than 1 million pages from certain start URLs. The challenge of this project is to implement an efficient scraper/indexer that can finish processing 1M pages in one day. The architecture is React frontend, Nginx backend with Postgres connection to RDS database for metadata and S3 buckets for page data. Apache storm lite is used to implement the crawler and indexer, the Hadoop / Apache Spark are both used (tried two implementations) for PageRank, which is stored in DynamoDB. As part of 4 student team, I primarily implemented PageRank with Scala on Apache Spark, but also helped with the indexer and engine implementation in various module implemenations.
3. "Penn Twitter": a MERN web application aimed to teach agile development and practices in the tech industry. The website supports social media features (following, posting, commenting), media upload, chatting, and streaming (w/ basic stream chat) with Twilio streaming framework support. The challenge is to be familiar with best testing and continuous integration practices using Travis CI, Jest, Selenium and keeping the code average at above 80%. (In real world, it must be 100%, I understand.) As part of 3 student team, I developed about 45% of the project and helped other students with better Git practices and design of our app. From writing the user stories, design and prototyping with Figma, database design on MongoDB Atlas, API design w/ Swagger, development, integration and testing, the entire project took 10 one-week sprints over the semester.
4. "Penn UNIX kernel": a C application that simulates the Kernel scheduler by premptive scheduling user threads wth user contexts; it also simulates a file system handler available to the Kernel with a module that treats a file as a filesystem, and stores files in flatFAT format. As part of a 4 student team, I primarily worked on the flatFAT filesystem and the shell, which is used to interact with the program. As extra credit I implemented a directory system that use the same mechanism on directorys as on files, same as the i-nodes design in Linux. The challenge of this project is writing low-level C code for the first time and understanding important system calls.
5. "Database open-ended project: movie recommendation system"
6. "Machine Learning project: twitter posts sentiment analysis"
7. "Penn Facebook": 
8. "Graphics project: mini-minecraft"
9. "Security assignments: various attacks on unsecure web targets"
10. "Blog website with Latex support": JS
11. "Restaurant management system": Ruby on Rails


### My inspirations
- Isaac, my friend and mentor from DSL. Prof. Boon Thau Loo. My friends from grace covenant church. Friends who showed incredible kindness.
- Robert Martin (Uncle bob) on clean code: [Youtube](https://www.youtube.com/watch?v=7EmboKQH8lM&list=PLdpsE-GEhYVn_81kDPo1mwE73UgYCeMLu)
- Our intro to algorithms (CIS 160/121) professor, Prof. Rajiv Ghandhi. From his challenging academic curriculum, rigorous discouse, to his [inspiring speech](https://www.youtube.com/watch?v=Kao_IZUCKgg), Prof. Ghandhi laid the solid foundation of algorithms of me and my peer compputer scientists.
- Book by our wise and lovely professor, Prof Jean Galier. [Linear Algebra and Optimization with Applications to Machine Learning](https://www.cis.upenn.edu/~jean/gbooks/linalg.html)
- The brilliant inspirers that are [Prof. Steve Zdancewic](https://www.cis.upenn.edu/~stevez/) and [Prof. Stephanie Weirch](https://www.cis.upenn.edu/~sweirich/). ([Article](https://csweb.rice.edu/news/stephanie-weirich-passion-programming-languages)). Functional programming. Ocaml. I loved the wisdoms embedded in programming languages and I shall perfect my craft with the best programming practice. For my final semester, I will take advanced programming, learn Haskell and functional programming to the best of my capabilities.
