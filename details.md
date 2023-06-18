# Indextr: Distributed Collective Knowledge Management (Scratchpad/Draft)
## Problems with existing content-publishing models (Wikipedia, Academic Journals etc)

- Linear and static: Content structure is generally linear, a byproduct of physical paper. 
- Journal Articles: Presented as factual because of peer review. Price to submit/read while the contributors/curators do work for free. Introduction content caters neither beginners (jargon, not truly an “introduction to the field”) or experts (introductions are typically similar, experts really want to “get to the point” because they already have a massive literature stack)
- Publications are biased for successful results
- Wikipedia: Single perspective. Topics rejected for not being important enough. Reviewing is “free” but they may be paid by other sources that are opaque to users.
- AI generated content: Though ChatGPT is only a few months old, it has exploded in popularity. It is amazing at generating textual content and is undoubtedly being used for writing long form content. However there are problems of reliability - it is confidently wrong. When asking about a specialized topic, it may provide a response that is coherent, but unverifiable by those unversed in the topic. It is also the perfect tool to “bloat” up ideas. A single bullet point can be expanded into a multi-paragraph article, seemingly coherent but ultimately vacant in content. Since AI is trained to cater toward average content, it is likely to propagate already popular paradigms while impeding novel perspectives that have yet to make ground. Additionally, as AI becomes more sophisticated, it is likely that is will become better  at sounding coherent to the general ne
- Wikipedia: Single perspective. Topics rejected for not being important enough. Reviewing is free but they may be paid by other sources that are opaque to users.

- Think about the already existing SEO programming tutorial filled with fluff but little relevance to actual content - this makes the situation even worse. Given that researchers are already burdened with too much new literature to read, it will be an even harder time to wade through
- Salami-slicing or seperating a single study into multiple papers to increase publication count will be an even easier task
- All major platforms are centralized points of failure

## The problem solving application: The Zettle-Wiki

- A Zettlekasten or “Slip-box” is a personalized way of storing notes that refer to other content. It emphasizes conciseness, links to other notes and references. Each note contains “A single piece of knowledge”, or “Knowledge that can be stored on an index card”

- A Wiki emulates the encyclopedia with long form articles with references

- A Zettle-Wiki.would be long form articles that are composed of index cards. This allows for articles to be composable and allow catering to different needs, multiple versions of articles. Experts can have their “Introduction to Genetics” and branch off various specialized links of applications, knowledge or research. Beginners can also have their own “Introduction to Genetics” that have content catered to their own knowledge base. Each note can refer to other notes for concepts, vocabulary, or outside references to break down the concept for any audience.

- AI generated content can now be constrained because ideas not only have references, but note the specific location where the knowledge is derived from. (e.g. Reference A. paragraphs 8 - 20)

## A rough overview:

### The social-network aspect: 

- The Zettle-Wiki is an interesting idea in of itself, but science/knowledge is ever changing and has multiple perspectives. How can we incorporate this?
- Distinguish between *Article Notes*, *Commentary Notes* and *Question Notes*. Article notes contain content that would belong to a standard wiki or journal article, just decomposed into index cards where knowledge is represented compactly. Other users can highlight sentences, and make commentary on the note. E.g “This sentence does not make sense”, “the interpretation of the resource is incorrect”, “this is correct but there are points missing” with their own references. Question notes may evoke others to answer, or write their own articles to answer a question.
- Note merge requests: An article may already exist, but a second user may think it is lacking in some crucial ways. The second author may say “you should incorperate these ideas” and propose a way of integrating the new knowledge within the note, or make their own note. If the original author agrees, a new note will be created allowing where there are now two authors. Content can be highlighted to indicate who is the author of what content.

- Content Discovery: to discourage vote manipulation, instead of likes there notes are ranked by the amount of commentary notes or incoming links. **This is a possible solution for large public relays or aggregated knowledge networks.**
  - An article stating nonsense low effort content or bad faith arguments such as "genetics are made from marshmellows. Reference: Me"  is not worth time and will likely be ignored.
  - Good faith arguments but faulty logic may have engagement by other authors who disagree and can make commentary notes showing why the logic/interpretation is wrong and link to other resources. The original author may not change their mind, but future readers can see the collective dialogue on such topics and even ask questions.

    
  - If this does not completely dissuade spam or bad faith content. Relays can also take action to remove or block users. A single group can exclusively publish to a relay and dissalow others from writing to it. The indextr client, through the use of multiple relays will generate a collective network from multiple relays and users can comment on articles even thoough they are not publishing to the same relay that an article is hosted on
    - Relay operators for the Zettle-Wiki can create a number of additional incentives for quality content:
    -  (1) Have users be paid to curate/organize content
    -  (2) Have authors "put skin in the game" for their content i.e. wage ~$5 that the content has quality. If it isn't the content is rejected and the wage is split among relay operators and curators
    - (3) Reject submissions but provide feedback on how to resubmit. Bad faith arguments should end up disappearing
    
- Index card-sized content. Makes knowledge compact and easily navigable. This now incentivizes multiple perspectives, negative and iterative results, all of which are important for the advancement of science and knowledge.
- Financial aspect. Users may tip the authors of the content they would like to see via micropayments. This incentives authors to write well and to continue writing. If a user wants to learn about *self sustainability* but has no knowledge of where to start, users can create bounties which will pay authors for new content. Optional zap splits with content creators, relay operators and individual client developers 
### Indextr interface
- ![](https://i.imgur.com/JQDDqjd.png)
- In the abstract: There user interface is to be minimal, and to hide functionality within layers
#### Description of Components
- Subject title
- Note title (e.g "Introduction")
- Note content (markdown-like syntax)
- Suggested Table of Contents: If an author creates a long form article, they can create the standard linear form article, but it must be split into notes, each containing a **single idea**. They can have before and after links to other notes within their suggested article. 
- Authors (toggled/hover functionality)
- Keyword Tags (toggled/hover functionality)
- References (toggled/hover functionality) Specificially note where in the reference the content is derived from "paragraph 4 - 10" etc. It is unadvisable to create a single note and have a reference to a 40 page article. This is in place because it shows the exact locations where the conclusions in this note are derived from.
- commentary-notes (toggle/hovered functionality)

##### Body content
- Like a regular wiki, notes can link to other links (word definitions, other internal/external references)

Layer toggles: 
- (1) External commentary notes: Some scale of agreement/disagreement that is beyond just "liking". Commentary notes can also have suggestions for the main note. This will help in ranking notes not by "likes" but by engagement
- (2)question notes (word "A" not defined, "unclear sentence", "wrong interpretation here", "bad reference" etc.) Suggesting other content be written, or have bounty incentives
- (3) author highlights: When toggled, the sentences that have been written by a specific author will be highlighted by a different color
### Commentary Notes
- When toggled, shows the complete list of "commentary notes" that are connected, organized by some "agree/disagree" spectrum.
- Each of these notes also retain the index card structure: Linking to other notes, should have references
- Commentary on specific content it is referring to. (Location in text, presentation of subject matter)
### Literature note
- Single line linking to one paper
- Commentary notes can link to this paper that can deconstruct the concepts and provide limitations/points of contention to the paper

## Specification of note "kinds" [see EVENT KINDS](https://github.com/nostr-protocol/nips#event-kinds)
### Article Note
### Commentary Note
### Question Note
### Flashcard
### Literature Note
 - Title
 - Author
 - Atomic reference (DOI, url, ISBN, etc) 
### Bounty Note
