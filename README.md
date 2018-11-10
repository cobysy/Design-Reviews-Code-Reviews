#  Design Reviews &amp; Code Reviews
(keeping for posterity; from project I worked on in 2003-2005ish )

## The Art of the Review
The Old-Fashioned Way to Find Errors and Produce Quality Software

TOC
- [Design Reviews &amp; Code Reviews](#design-reviews--amp--code-reviews)
  * [The Art of the Review](#the-art-of-the-review)
    + [Software Reviews](#software-reviews)
    + [Review Results](#review-results)
    + [Different Types of Reviews](#different-types-of-reviews)
  * [Design Reviews](#design-reviews)
    + [Design Reviews](#design-reviews-1)
  * [Code Reviews](#code-reviews)
    + [Benefits](#benefits)
    + [What are you looking for?](#what-are-you-looking-for-)
    + [On-line Reference](#on-line-reference)
    + [What To Do and What *NOT* To Do](#what-to-do-and-what--not--to-do)
    + [Sin 1: Participants Don't Understand the Review Process](#sin-1--participants-don-t-understand-the-review-process)
    + [Sin 2: Reviewers Critique the Producer, Not the Product](#sin-2--reviewers-critique-the-producer--not-the-product)
    + [Sin 3: Reviews are Not Planned](#sin-3--reviews-are-not-planned)
    + [Sin 4: Review Meetings Drift into Problem Solving](#sin-4--review-meetings-drift-into-problem-solving)
    + [Sin 5: Reviewers Aren't Prepared](#sin-5--reviewers-aren-t-prepared)
    + [Sin 6: The Wrong People Participate](#sin-6--the-wrong-people-participate)
    + [Sin 7: Reviewers Focus on Style, Not Substance](#sin-7--reviewers-focus-on-style--not-substance)
  * [Checklists](#checklists)
    + [Why Use Checklists](#why-use-checklists)
    + [A Code Review Checklist](#a-code-review-checklist)
    + [More Reading on Code Reviews](#more-reading-on-code-reviews)
  * [Targeted Reviews](#targeted-reviews)
    + [Performance Review](#performance-review)
    + [The Seven Deadly Performance Sins](#the-seven-deadly-performance-sins)


### Software Reviews
* The origin of software reviews goes back to the 1970's and Fagan's (IBM) software inspection technique.
  * Manual examination of software work products (e.g. code, documentation, etc.) by developer's peers.
  * Impressive results: Raytheon, Motorola, BNR (aka Nortel), HP
  * But authors have had difficulty getting it going 

 * Reviews involve the reading of specification or design documents or the visual inspection of the source code by a team of qualified people

### Review Results
 * It is arguably one of the most powerful software quality practices
   * "... all software groups should become skilled in their application"
   * Capers Jones notes that "Formal code inspection are about twice as efficient as any known form of testing in finding deep and obscure programming bugs, are are the only known method to top 80 percent in defect-removal efficiency"

  * The main objectives are to
    * Find as many errors as possible
    * Improve the quality of the software
    * Familiarize designers/programmers with standards.

### Different Types of Reviews
  * __Review__
    * Complete and thorough evaluation.
  * __Walk-through__
    * Producers of reviewed material is present and guides progression of review (demo is a special case)
  * __Inspection__
    * Rapid, focusing on a few selected aspects, one at a time
  

## Design Reviews

### Design Reviews
* Reviewing a design is slightly different than reviewing code.
  * But, because design errors are associated with a higher cost than code errors, design review is very important.
* Designs have a subjective component that makes reviewing difficult.
  * Is it easiest to do when comparing one design to another.
  
## Code Reviews

### Benefits
* Improves consistency of coding styles.
* Provides cross-pollination of ideas and techniques among the programming team.
* Provides essential training in using standards for coding.
* Motivates programmers to produce better code.
* Shortens debugging phase.

* Programmers are forced to more clearly and completely document their code
* Code becomes more readable.
* Improves team confidence in the software being produced.
* Motivates programmers to produce better code before the review.

* Testing the code becomes easier.
* Misunderstandings about interface issues are caught earlier in the coding process.
* Code reviews typically find 30% to 70% of the logic design and coding errors in software.

### What are you looking for?
* Poor or sloppy coding style
  * Uninitialized variables
  * Meaningless or confusing variable names
  * Loops with poorly defined controls
  * Conditional statements with parts that cannot be reached during execution of the program
  * Poorly designed classes - usually too larger and thus not reusable

* Comments (or their absence)
  * Redundant, misleading, confused, out of date
  * Functionality and correctness
  * Does the code follow the design?
  * Logic errors
  * Mathematical/arithmetic errors
    * Dividing by zero, overflow, mixed-type computations
    
### On-line Reference
* Procedures for Peer Code Review
  ** http://www.computerinterfacedesign.com (website defunct)

### What To Do and What *NOT* To Do
__Reference__: Karl Wiegers, The Seven Deadly Sins of Software Reviews, Software Development, March, 1998

### Sin 1: Participants Don't Understand the Review Process
* __Problems__
  * What is the role of the reviewer?
  * What is being reviewed?
  * Establishing clear objectives
    * Drifting focus (solving problems, challenging programming style)
  * Team make-up
    * Size
    * Participants - good software engineers are not necessarily good software reviewers
  * Documentation format

* __Consequences__
  * Missed defects
  * Frustration
  * Unwillingness to participate in future reviews
 
* __Solutions__
  * Training (4-8 hours recommended)
    * Additional training for leaders
  * Written procedures (for formal and informal reviews)
  * Standard forms
  
### Sin 2: Reviewers Critique the Producer, Not the Product

* __Problems__
  * Personal assaults on skills and style of work product author
  * Confrontational style of raising issues

* __Consequences__
  * Developer feels beaten down, defensive and resistant to legitimate defensive
  * Reluctance to submit future products for review
  * Revenge when its time to review someone else's work

* __Solutions__
  * Establish the correct battle lines
    * Pit the developer abd peers against defects in work product
    * Not a chance to show how smart you are
  * Use collective wisdom insight, and experience of a group of peers to improve the quality of the group's products
  
  * Direct comments and critiques to product, rather than the authors
    * "They never explain why they use RMI" versus "The document is missing a rationalization for the choice of RMI"
    * "You forgot to initialize these variables" versus "I don't see where the variables were initialized"

  * If author is not present or participating then confrontational nature is reduced
    * Otherwise reviewers and authors should check their egos at the door
    * Author should participate as little as possible, and reviewers should know how to express criticisms in a non-confrontational manner

### Sin 3: Reviews are Not Planned

* __Problems__
  * Reviews are not part of the schedule
  * Treated as milestones (take zero time), rather than tasks (take time)
  
* __Consequences__
  * No time devoted to reviews
  * Potential participants don't have time available

* __Solutions__
  * Make reviews high priority
  * Include reviews in schedule
  * Estimate time required for individual preparation and reviewers, the meeting, and rework
  * Keep records of previous review times to predict future reviews
  * Review planned and scheduled

### Sin 4: Review Meetings Drift into Problem Solving

* __Problems__
  * Software developers are creative problem solvers by nature
    * The more challenging the better!
  * When faced with a problem we instantly begin thinking, *how would I do this*
     * The *born to code* syndrome often combined with coding withdrawal
  * This is not what we want during a technical review

* The biggest danger is us!*

* __Consequences__
  * Problem solving causes progress of examining the product to grind to a halt
  * Some people tune out
  * Can easily lead to reviewing the author (why would anyone in their right mind do this?)
  * Time runs out and reviewers skip over really serious problems

* __Solutions__
  * Remember that the primary purpose is to find defects in product (and should stop there)
  * The leader should evaluate progress and stop discussions concerning solutions
  * Sometimes you may encounter a show-stopper defect that puts the whole premise of the product into question
    * Do not solve the problem in the review
    * Document and send back for further action
  
### Sin 5: Reviewers Aren't Prepared

* __Problems__
  * You get the review documents at 7:45am for a meeting at 8:00am
  * People at the review meeting are seeing the document for the first time
  * Reviewers haven't bothered to review materials

* __Consequences__
  * Reviewers don't spot subtle errors
  * No questions are comments on the document
  * Some reviewers don't contribute

* __Solutions__
  * Group leader begins by collection preparation times
  * If prep-times are inadequate, meeting should be rescheduled

  * Recognize that time spent reviewing someone else's work will be paid back when they review your work
  * Review documents provided 48 hours in advance
    * Document describes the same product that you are working on
  * Reviewers are graded

### Sin 6: The Wrong People Participate

* __Problems__
  * Reviewers need appropriate skills and knowledge
  * Participants who only go to learn will not be likely to improve quality of product
  * Management participation may be bad if review results are linked to performance appraisals (reviewers might not want to make colleagues look bad)
  * Large review teams can be counter productive

* __Consequences__
  * Focus on trivial details (how sentences should be phrased)
  * Slow progress

* __Solutions__
  * Three to seven people is ideal
    * Reviewers should include author?
    * Author of predecessor or spec
    * User of the product
    * Only first level manager should be allowed to attend and only if author says its OK
  * Review management's stuff too
    * Design doc's grade will not depend on results of review
    * Reviewers' grades will depend on errors found

### Sin 7: Reviewers Focus on Style, Not Substance

* __Problems__
  * Review meetings turn into debates on style
  * Participants get heated up over indentation, brace positioning, variable scoping, comments, etc.

* __Consequences__
  * Substantive errors are overlooked
  * Logic errors, missing functionality

* __Solutions__
  * Adopt code standard and templates for documents
  * Use code reformatting tools to enforce standards so people can program the way they like
  * Be flexible and realistic about the style
  * Don't get hung up on minor issues

  * Don't impose your will on others
  * Respect individual differences
  * Preferences versus clarity

## Checklists

### Why Use Checklists
* Other professions rely on the use og checklists to insure safety, e.g. a pilot's preflight check
  * U.S. Navy reports that a study of accidents at ibe U.S. Air Force base found that before every accident, the preflight checklist had not been rigorously followed.

### A Code Review Checklist
* The following is a sample checklist for code reviews
  * By Patricia Mandl-Striegnitz (University of Stuttgart)
  * Available at http://www.informatik.uni-stuttgart.de/ifi/se/service/checklists/download/Review_code.html (defunct)

1. Has the design properly been translated into code?
2. Are there misspellings and typos?
3. Has proper use of language conventions been made?
4. Is there compliance with coding standards for language style, comments, etc.?

5. Are the incorrect or ambiguous comments?
6. Are comments useful or are they simply alibis for poor coding?
7. Are data types and data declarations proper?

8. Are physical constants correct?
9. Are there redundant operations for which there is no compensation benefit?
10. Has maintainability been considered?

11. Completeness
  * Are all referenced data defined, computed, or obtained from external source?
  * Are all defined data used?
  * Are all referenced subprograms defined?
  * Are all defined subprograms used?

12. Efficiency
  * All all non loop dependent computations kept out of loop?
  * Are all compound expressions defined once?
  * Are data grouped for efficient processing?
  * Are data indexed and referenced for efficient processing?

### More Reading on Code Reviews
* *A Case for Code Review* by John Stenersen on the website, Gamasutra, March 14, 200
* http://gamasutra.com/features/20000314/stenersen_01.htm (defunct)


## Targeted Reviews
An example of how you can use a code review to check for specific characteristics, specifically __performance__.

### Performance Review
* __Reference__
  * Profiling, Data Analysis, Scalability, and Magic Numbers, Part 2: Using Scalable Features and Conquering the Seven Deadly Performance Sins by Herb Marselas on Gamasutra, August 16, 2000
* http://gamasutra.com/features/20000816/marselas_01.htm (defunct)

### The Seven Deadly Performance Sins
1. __Executing dead or superfluous code__
  * Over the course of a long development cycle, a lot of code-based functionality is created, changed, and/or discarded.
  * Sometimes this code is not removed and continues to be executed
2. __Executing code too much__
  * An inappropriate data structure or logic thread may cause inefficiencies in the system
3. __Using inappropriate algorithms__  
  * An evening in the lab can save an hour in the library
4. __Encountering exceptional data__
  * Code is written based on assumptions about the data
    * The data is a certain type and will fall within certain limit or into certain sets
  * When data falls outside these expectations, an algorithm may start experiencing performance problems

5. __Inefficient memory usage__
  * Are the most appropriate data structures being used?
6. __Inefficient code__
  * Has the developer profiled the code or done unit testing using an optimization compiler?
7. __Other programs__
  * Will the environment, under which the code being reviewed will run, effect performance?




