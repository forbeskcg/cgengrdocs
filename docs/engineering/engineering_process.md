# Engineering Process

Just as with the scientific method, engineering has a general flow that has been shown to guarantee solutions that solve the intended problem. The engineering process involves:

1. Understanding the problem
2. Drafting requirements for the solution
3. Brainstorming solutions to the problem
4. Narrowing the solutions through selection and prototyping (preliminary design)
5. Creating a detailed design of the solution (critical design)
6. Implementing the solution
7. Testing the solution against the original requirements
8. Iterate on the solution

Depending on project scope and size, additional steps may include supporting the solution through its full lifecycle. For a commercial product, that may include product release, customer use, and obsolescence.

We tend to solve problems in this way even when we aren’t consciously thinking about our actions. However, what differentiates an engineer from a “tinkerer” is documentation - keeping track of progress at each of these phases and verifying that each step is complete before moving on to the next.

We go into more detail on these steps in the sections below.

## 1. Problem Statement

The first step to solving a problem is understanding it. This can come in many forms:

- A simple description of the system and need,
- Define who the “customer” is,
- In-depth research to define the domain and scope of the problem,
- A list of use-cases, user stories, and similar user-facing needs,
- Information on interfaces between the problem domain and related systems

The depth to which you understand the problem is usually proportional to its significance. Large, expensive (cost and/or time) projects are worth dedicating significant time to research. Essentially, the better the problem is understood, the less risk we assume in the solution.

## 2. Requirements

Requirements are the essence of engineering a solution to a problem. We use requirements to understand the problem and create boundaries for the solution. Often they are drafted once we have a rough understanding of the problem or project. They *should* be written prior to brainstorming, so that potential solutions can be sized up against the requirements and pruned if found not to fit.

Requirements can take many forms. The simplest is a list in a document or spreadsheet. More formal requirements are traceable - they have IDs, are derived from research or use cases, and are validated against the solution during testing. Large-scale projects (or those in regulated markets such as medical) may even use software such as [Rational DOORS](https://www.ibm.com/docs/en/ermd/9.7.0?topic=overview-doors) to track requirements through the project lifecycle.

There are a few rules of thumb to keep in mind when drafting requirements:

- **Requirements are not “set in stone”.** They can be flexible, and should incorporate new information as it is discovered during the project.
- **Include what you don’t know.** It’s okay to include a TBD in the requirements. It is better to be comprehensive but unsure, than to leave something out because you aren’t familiar with the details. The requirements you don’t know form a list for what you should strive to understand.
- **Anti-requirements are also useful.** It can be useful to specify what a solution cannot be to limit the design space.
- **Requirements are not specifications**, though the two are related. Requirements define general limitations, while specifications define the specific chosen solution (what microcontroller will be used, how tall the robot will be, etc).

Further reading:

- <https://en.wikipedia.org/wiki/Requirement>
- <https://www.nasa.gov/seh/appendix-c-how-to-write-a-good-requirement>
- <https://reqexperts.com/wp-content/uploads/2015/07/writing_good_requirements.htm>

## 3. Brainstorming

Ideation or brainstorming is a highly collaborative approach to examining the solution space of a given problem. The goal is typically to generate a very broad set of potential solutions in order to ensure an “optimal solution” is not missed during further phases of development. The full team should be involved in the brainstorming process for it to be most effective.

There are many forms of brainstorming, but all include the mantra that **no idea is too far-reaching**. Even the wildest ideas can lead a group mindset to a feasible solution, sometimes even the best one. Judgment must be withheld in order to create a space and process where everyone feels comfortable sharing any and all concepts.

Some common techniques:

- Develop concepts individually first, to create the broadest possible set of starting points.
- Ask questions and try suspending design assumptions in order to generate new ideas
- Split into small groups and combine and develop concepts from those individuals
  - Consider how you might add or alter existing concepts (including removing a feature) to generate new ideas
- Come back together as a full group to present ideas for cross-pollination
  - Try combining multiple concepts to form novel ideas

Whiteboards and sticky notes work well during this phase, but consider that the concepts should be documented (as with all steps in the process), particularly for later referral and additional brainstorming sessions. A laptop and projector is a simple solution.

For those CS nerds, consider that the brainstorming process is truly one of optimization - we want to avoid getting stuck in [local optima](https://en.wikipedia.org/wiki/Local_optimum), and the best way to do this is by understanding as much of the solution space as possible.

Once the brainstorming process has been exhausted or reached a stopping point, the next process is pruning. Only a manageable number of concepts should be taken into the Preliminary Design phase (based on resources). Start by eliminating those ideas which do not fit with the agreed upon requirements. Then, any number of methods can be used to further reduce the selection, such as voting, organizing by feasibility/creativity, decision matrices, etc.

Further reading:

- <https://en.wikipedia.org/wiki/Brainstorming>
- <https://www.interaction-design.org/literature/article/how-to-select-the-best-idea-by-the-end-of-an-ideation-session>

## 4. Preliminary Design

During the preliminary design phase, the final selection of designs from the brainstorming session are further explored in detail. Feasibility studies are performed through prototyping to verify whether the designs truly meet the requirements and to understand their performance.

Additional concepts may be generated through this phase, and should be documented and presented as possible solutions during the design review.

The Preliminary Design Review (PDR) marks the end of this phase. Designs should be analyzed quantitatively so they can be compared objectively. Some designs may be ruled out if it is discovered they violate some requirement.

!!! note
    Remember that requirements are not set in stone! It may be that a requirement should be re-evaluated instead of tossing out a design concept.

A weighted decision matrix can be a helpful method to compare preliminary concepts and select one to move forward with detailed design. The chosen design should be validated to ensure it meets all the requirements.

Further reading:

- <https://en.wikipedia.org/wiki/Decision_matrix>
- <https://www.infonautics.ch/blog/decision-matrix/>

## 5. Critical Design

Finally, a design has been crowned, and the team can take it from concept to concrete.

At this point, all disciplines begin detailed design of their particular project areas. Prototyping still occurs, but at a departmental level. For mechanical teams, this means developing and iterating CAD models and drawings. The controls team may map out the entire system and select specific components to meet the mechanical and control design needs. Software teams may model the system components and interactions in tandem with the electrical and drive teams. Competitive analysis and software may also develop autonomous strategies.

A Critical Design Review (CDR) would mark the end of this phase and allow the design to continue on to implementation.

## 6. Iteration: Implementation and Testing

Finally, the design is fabricated, assembled, brought to life with software, and tested to verify the design meets the requirements.

??? question "What if we finish with time to spare?"
    Iterate! It is said that good is the enemy of great. If time and resources are available, efforts should be made to improve the design and/or implementation. We gain a deeper understanding of the problem through optimization.

Another common mantra (from Silicon Valley) is to **fail fast and often**. Again, for CS nerds, this is approximately equivalent to [gradient descent](https://en.wikipedia.org/wiki/Gradient_descent). Once we have found a good region in our solution space, we want to locate the local optimum. We push our design to the limits to determine the weaknesses, and focus our energy and improvements there.
