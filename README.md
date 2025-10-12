# Machine Learning Engineering: From Models to Products
Lecture at DHBW Ravensburg that covers how to build, deploy, assure, and maintain software products with machine-learned models. Includes the entire lifecycle from a prototype ML model to an entire system deployed in production. Covers also responsible AI (including safety, security, fairness, explainability) and MLOps. Heavily inspired by the great material of [Machine Learning in Production at CMU](https://github.com/mlip-cmu).

## Course Description
This course is designed for those who want to build real software products powered by machine learning, not just models or demos. We assume you already know how to train models or design prompts to generate predictions. But what does it take to turn those models into reliable, deployable products? How do you ensure their quality, scale them effectively, and maintain them in production?

## Learning Outcomes
After taking this course, among others, students should be able to

* analyze tradeoffs for designing production systems with ML-components, analyzing various qualities beyond accuracy such as operation cost, latency, updateability, and explainability
* plan for mistakes in ML components and implement production-quality systems that are robust to those mistakes
* design fault-tolerant and scalable data infrastructure for learning models, serving models, versioning, and experimentation
* ensure quality of the entire machine learning pipeline with test automation and other quality assurance techniques, including automated checks for data quality, data drift, feedback loops, and model quality
* build systems that can be tested and monitored in production and build robust deployment pipelines
* consider system-level requirements such as safety, security, privacy, fairness, and usability when building complex ML-enabled products
*  communicate effectively in interdisciplinary teams

## Logistics, Syllabus & Policies
The course uses Moodle for project submission, grading, discussion, questions, announcements, and supplementary documents. Github is used to coordinate group work. All public course material (assignments, slides, syllabus) can be found in the course’s GitHub repository.

### Prerequisites
The course does not have formal prerequisites, but we describe background knowledge that will help you be successful in the course. In a nutshell, we expect basic exposure to machine learning and basic programming skills, but do not require software engineering experience.

**Machine learning** (some experience recommended): if you have no prior experience or need a refresher, we recommend for example "Hands-On Machine Learning with Scikit-Learn, Keras, and TensorFlow" by Aurélien Géron or courses such as [MIT 6.S191: Introduction to Deep Learning](https://introtodeeplearning.com/) or [CS229: Machine Learning](https://cs229.stanford.edu/).

**Programming** (basic proficiency required): we expect basic fluency in a programming language like Python including the ability to install and learn libraries in that language and we expect that you will be able, on your own, to learn basic use of libraries like Flask to write a web service. 

### Exam
The course has no final written exam, but includes a group project, which focuses on building, deploying, evaluating, and maintaining an ML-enabled system. You will work on the project during an in-between the lectures and your final submission will be graded at the end of the course. The project description can be found [here](assignments/project.md).

### Policies

**Use of content generation AI tools and external sources:** We place no restrictions on the use of AI tools, such as ChatGPT, Co-Pilot, or Stable Diffusion. You may also reuse code from external sources, such as StackOverflow or tutorials. In any case, you will need to declare the use or source and you will be solely responsible for the correctness of the solution. You are also responsible for complying with any applicable licenses. If you use content generation tools, we encourage you to share your experience with us or the entire class.

**Academic honesty and collaboration:** We expect that group members collaborate with one another, but that groups work independently from other groups, not exchanging results with other groups. Within groups, we expect that you are honest about your contribution to the group's work. This implies not taking credit for others' work and not covering for team members that have not contributed to the team. 

Beyond that, the key guiding principle of academic honesty in this course is: _"You may not copy any part of a solution to a problem that was written by another student (in this or prior iterations of the class), or was developed together with another student, or was delegated to another person. You may not look at another student's solution, even if you have completed your own, nor may you knowingly give your solution to another student or leave your solution where another student can see it."_ Note that this implies that you cannot publicly post your solutions on GitHub. While the use of AI content generation tools is okay (see above) using the work from other students is not. Discussing challenges and solution strategies with others at a high level is okay, sharing code or text is not.

Any violation of this policy is cheating and will be reported. If you have any question about how this policy applies in a particular situation, ask us for clarification.

## Further Readings
If you are interested in diving deeper, here are some book and paper recommendations:

* Christian Kästner. Machine Learning in Production: From Models to Products. https://mlip-cmu.github.io/book/index.html
* Andriy Burkov. Machine Learning Engineering. https://mlebook.com/
* Hulten, Geoff. Building Intelligent Systems: A Guide to Machine Learning Engineering.
* Kiri L. Wagstaff. Machine Learning That Matters. https://arxiv.org/pdf/1206.4656


