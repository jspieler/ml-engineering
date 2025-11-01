# Group Project: Building an ML-enabled Product

## Overview
In this group project, you will enhance an existing web application with features powered by machine learning. The goal is to experience what it takes to move from a working ML model to a functioning product. You’ll consider not only how to integrate ML into an existing codebase, but also how to address product, usability, fairness, and scalability concerns.

**Learning goals:**

* Understand the scope of software engineering challenges when building an production system with ML components
* Identify technical and nontechnical challenges in deploying ML-powered features
* Reflect on user experience and risks introduced by ML components
* Develop awareness of issues such as explainability, fairness, and operational concerns

**A word on scope and difficulty:** You’ll work with an existing web application, [Moments](https://github.com/greyli/moments), a minimal Instagram clone built with Flask. Users can create accounts, upload and tag images, and comment on them. While the application is small, the codebase is non-trivial and uses multiple technologies: Flask, HTML templates, SQLAlchemy, wtforms, and pip-based dependency management.

We do not expect you to know all of these technologies already. You’ll learn by reading documentation, tutorials, and examples—just like professionals do when integrating ML into production systems. Even if the final code change is small, navigating and understanding where and how to make those changes is a core part of the learning experience.

This project consists of multiple tasks and a final report, which add up to a total of 36 points. Beyond that, the project is intentionally open-ended. You’ll implement three core features with minimal code, but high design impact. You can achieve full credit with a minimal implementation, as long as you identify its limitations and reflect on how it could be improved. You're also encouraged to go further if you want to experiment, explore better integrations, or apply advanced ideas.

## Tasks
In this assignment, you will use advances in machine learning for vision to improve accessibility and image search in an open source project named [Moments](https://github.com/greyli/moments). Moments is a demo implementation of a minimal Instagram clone in Python, created as example for a book on the flask library for Python. Users can create accounts and upload and share images, describe and tag images, and comment on images. While Moments is not a polished end-user product, it is a reasonable stand-in for a software product that may be used by end users while still having a reasonably small codebase. Moments does not currently use machine learning for any of its functionality.

Change the open source project to introduce at a minimum the following **three** features:

* Alternative text generation: Provide an automatically generated alternative text for images if users do not provide their own. In Moments you can use the existing description field or add a new mechanism to store the alternative text.
* Image search: Identify objects in images so that images can be searched with keywords. In Moments, you can use the existing functionality for tags or add a new hidden mechanism for storing identified objects.
* Think of another ML-enabled feature that Moments would benefit from and implement it.

You can use any existing ML models as part of your implementation, research or free or paid, remote APIs or local pretrained models. We do **not** recommend to train your own model.

### Task 1: Planning & Design
* Define how ML features will be integrated (diagram + explanation).
* UI decisions: Will alt-text be editable? When is it generated? How are tags stored?
* Identify at least three potential risks introduced by your features.
* Answer following questions:
  * What product benefit does each ML feature provide?
  * Where does ML sit in the system? What are its dependencies?

### Task 2: Model Integration
* Implement alt-text generation.
* Implement keyword tagging using object detection or zero-shot classification.
* Implement one other ML-enabled feature of your choice from which Moments could benefit.
* Include tests or examples of incorrect output and discuss limitations.
* Answer following questions:
  * What models did you choose and why?
  * What input/output formats do you use?
  * Are the models robust across different input types?
 
### Task 3: Responsible ML
* Evaluate how the system performs across different types of users or content for at least one feature (e.g., skin tone detection bias, stereotypes in captions).
* Include a basic audit of fairness/harms by identifying at least one harm for one feature, with one potential mitigation strategy.
* Offer a way for users to report/override model output.
* Answer following questions:
  * What kind of errors does your model make?
  * How might this affect users?
  * How explainable are your predictions?
  * Reflect on whether these failures stem from:
    * limitations of the training data,
    * limitations of the model itself, or
    * limitations of your integration.
 
### Task 4: Deployment & MLOps
* Describe how the system would scale (e.g., batching uploads, caching embeddings).
* Decide whether to use APIs (e.g., Replicate, HuggingFace Inference API) or run models locally.
* Include an example of monitoring or logging.
* Answer following questions:
  * What resources does your model need to run?
  * What metrics would you track to detect problems?
  * How would you update or replace your model?

## Submission
Commit all your code changes to your team's GitHub repository, but do not commit private credentials. Update instructions to install and run the system in the `README.md` file as necessary. For example, explain how to get an API token if needed or add additional libraries to `requirements.txt`.

Additionally, upload a short report to Moodle with the following content which also answers the questions of each task described before:

* **Github link:** Start the document with a link to your team's Github repository and the names of the team members.
* **Technical description (1 page max):** Briefly describe how you implemented the three features.
* **User interface design approach (1 page max):** Describe for each of the three features how the feature should interact with users (automate, prompt, organize, annotate, hybrid) and why. Justify your decision, considering forcefulness, frequency, value, and cost. If your implementation differs from the proposed approach, briefly explain how you would change your implementation if you had more time.
* **Harms (1 page max):** Discuss what possible harms you can anticipate from using machine learning for the features in the applications (e.g., safety, fairness). Identify at least one harm and discuss potential solutions to mitigate the harm. (You do **not** need to implement the solutions.)
* **Production challenges (1 page max):** Discuss any technical challenges you anticipate if you want to deploy this feature in production (e.g., scalability, operating costs) and how you would change your implementation if you expected millions of users. Identify at least one problem and discuss corresponding potential solutions. (You do **not** need to implement the solutions.)

Make sure your document is clearly structured, such that it is recognizable which answer belongs to which question.

Page limits are recommendations and not strictly enforced. You can exceed the page limit if there is a good reason. We prefer precise and concise answers over long and rambling ones.

Machine learning contributes a part to a larger application with many non-ML parts and system-level concerns. When designing the features, think about how you introduce the features into the existing open source application, whether they change the user interface, and when and how to call the ML models. Also consider whether the used ML models are really suitable for the task at hand and whether you foresee any risks of deploying these features in their current form and how to make them better. Finally, anticipate engineering issues that might occur if you wanted to scale the system to support millions of users and daily image uploads. Make sure you are discussing the overall application, not just the ML model.

Your discussions may reveal limitations of your implementation and make suggestions for improvements. Even if you point out serious flaws in your own implementation, you are not required to implement the improvements if your implementation already meets our minimal requirements.

## Grading
**Important:** Please read the grading specifications carefully. 

The project is worth **36 points** in total. We will assign credit as follows:

* 4p: The document is clearly structured, such that it is clear which text belongs to which question.
* 4p: We can install and run your implementation based on the descriptions in the README.md file (including instructions for dependencies and API credentials if needed).
* 2p: Most commits (>60%) are reasonably cohesive and contain reasonable commit messages. The code is generally reasonably well structured and understandable.
* 1p: No private credentials are committed to the GitHub repository, including its history.
* 3p: The document describes how alternative text generation is implemented, and we can find the corresponding implementation. A machine-learned model was used in the implementation. The application is functional in that it produces HTML with alt attributes containing alternative text for all images uploaded by users (excluding profile pictures). The alternative text is automatically generated by an ML model unless the alternative text is manually provided by the user.
* 3p: The document describes how image search is implemented, and we can find the corresponding implementation. A machine-learned model was used in the implementation. The application is functional to search for images uploaded by users with keywords that are matched objects in those images.
* 3p: The document describes why and how the third feature of your choice is implemented, and we can find the corresponding implementation. A machine-learned model was used in the implementation. The feature is functional.
* 4p: The document makes plausible recommendations of how to design the user interaction for the three new features. The recommendation is justified, and the justification considers forcefulness, frequency, value, and cost.
* 6p: The document makes a good faith attempt at discussing at least one possible harm. The discussion focuses on application-level concerns and the user experience. At least one potential harm with the current implementation is identified. At least one potential solution is discussed for each harm. All discussed harms and solutions are plausible in the context of the application.
* 6p: The document makes a good faith attempt at discussing production challenges. The discussion focuses on production issues such as scalability or operation costs. At least one potential problem with the current implementation is identified. At least one potential solution is discussed for each identified problem. All discussed problems and solutions are plausible in the context of the application.

## Technical Hints
Current browsers do not usually show the alternative text by default, not even as tool tip. There are several browser plugins and screen readers that can highlight them or you can simply inspect the produced HTML source.

There are many web APIs that provide object detection and image captioning features. You will typically have to sign up for an account. Most offer the API for free for a certain number of requests or offer trial periods -- this is sufficient to complete the assignment. Google and Microsoft also offer cloud credits for students that you may use. You can also consider using pretrained models locally. We do not recommend training your own model, as this would by far exceed the scope of this assignment. When we tested the assignment, we had good experiences with the Azure Computer Vision APIs.

For Moments, it is worth to gain a basic understanding of package management in Python with pip and of creating and running web applications that produce HTML pages with flask. If you are unfamiliar with HTML, the most basic tutorials are likely sufficient. The file blueprints/main.py contains the entry points for rendering different pages, including those for showing the photo listing, an individual photo, and for uploading photos. Moments uses an internal database to store objects in a format specified in models.py using SQLAlchemy; those objects are easily extensible without database knowledge. The uploaded files themselves are simply stored in a directory. The files in templates/main contain HTML templates used to generate the web pages by flask, where flask simply fills in the parts in double curly braces with the result of the code contained within. There are at least three <img> tags in these templates for showing user images without an alt attribute in the original implementation. Forms in Moments are generated with the library wtforms that abstracts from low-level HTML code.

The Moments code is a couple of years old now and you may run into dependency issues with newer Python or library versions. We expect that you are proficient to debug and fix these issues yourself. You might find it helpful to read the documentation of the affected libraries, upgrade libraries, or downgrade your local Python version.

Public APIs for ML models like Azure's Vision API usually have fairly decent documentation and code snippets in multiple languages to illustrate how to use them.

Never commit private credentials (such as API keys) to a public Git repository. A common strategy is to write credentials into a file (e.g., api.key), read the key from the file at runtime, add that file to the .gitignore file to avoid committing it accidentally, and add instructions to the README of how to obtain a key and how write it into a file. Alternatively it is common to pass API keys as environment variables. If you accidentally commit a key and push this to a public repository, you will need to revoke the key and create a new one; if you have not yet pushed the changes you can go the nontrivial route of rewriting the git history.
