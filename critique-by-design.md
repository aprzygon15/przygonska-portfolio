| [home page](https://cmustudent.github.io/tswd-portfolio-templates/) | [data viz examples](dataviz-examples) | [critique by design](critique-by-design) | [final project I](final-project-part-one) | [final project II](final-project-part-two) | [final project III](final-project-part-three) |

# Rethinking Health Literacy: Redesigning KFF's Antibiotic Awareness Visualization
When I started browsing MakeoverMonday for a dataset to analyze, I knew I wanted to choose a topic with real-world public health impact. I stumbled across a dataset sourced from a Kaiser Family Foundation (KFF) publication titled "Data Note: Public Awareness Around Antibiotic Resistance." Specifically, I focused on Figure 6, which presented survey responses to a fundamental health question: "Can antibiotics cure viral infections?" (Correct answer: No, cannot be cured).


## Step one: the visualization

The original visualization was published by the Kaiser Family Foundation (KFF) as part of their public health awareness series on antibiotic resistance.

<img width="605" height="425" alt="KFF Figure 6 " src="https://github.com/user-attachments/assets/c29f3897-53f9-40fa-bd23-7b22b35373a0" />" 
- Source: KFF Data Note: Public Awareness Around Antibiotic Resistance
- Website url: https://www.kff.org/other-health/data-note-public-awareness-antibiotic-resistance/

## Step two: The critique
Step Two: The Critique
To evaluate Figure 6, I applied a comprehensive data visualization critique framework grounded in design principles from Stephen Few's Data Visualization Effectiveness Profile (a resource Storytelling with Data). I analyzed the original chart across five core dimensions: audience context, visual encoding, color semantics, typography, and data selection.

| Design Dimension | Score | Evaluation & Observations |
| :--- | :---: | :--- |
| **Truthfulness** | **9 / 10** | Accurately reflects KFF survey findings with a clear tone |
| **Completeness** | **8 / 10** | Captures essential demographic breakdowns across Education, Income, Gender, and Age tiers. |
| **Usefulness** | **7 / 10** | Highly relevant topic for healthcare professionals, public health advocates, and policymakers. |
| **Engagement** | **6 / 10** | Clear title at the top, but corporate branding treats the data as a static visual rather than a story |
| **Perceptibility** | **3 / 10** | Stacked bars force readers to slow down and perform mental calculations across segments to add to 100%. |
| **Aesthetics** | **3 / 10** | Blue palette makes distinguishing right from wrong confusing and relies heavily on the legend. |
| **Intuitiveness** | **2 / 10** | Readers miss the core takeaway unless they read the chart line by line |

The data itself was accurate and valuable, but the layout and brand-heavy coloring was hiding the key insights from anyone reading the chart out of context.

As someone who is frequently around healthcare professionals, the dataset itself caught my attention right away. The title at the top was clear, and the graphic had a boring tone you expect from an organization presenting objective facts. However, while I was able to read the graph, it required me to stop and really LOOK at it to make sense of what it was saying. I understand why the author used blue, it aligns with their company branding, but using two different shades of blue for the right and wrong answers was deeply confusing. It forced me to constantly check back and forth with the color key.

The primary audience for this graphic seems to be public health advocates, healthcare professionals, and policymakers. In its current form, I would kind of be helpful for that group. A busy professional or policymaker wouldn't be able to grasp the core takeaways in a matter of seconds, meaning manny people will completely miss the story the visual is trying to tell. The chart should be highlighting that higher education and income levels directly relates with knowing how antibiotics work, but instead, you are forced to read through the chart line by line just to reach that conclusion.

Moving into my redesign, I want to strip out the extra noise and focus directly on what drives health literacy! I moved on to watching Andy Kriebel's video using the same data. I found it interesting that the color scheme didn't seem to be much of a problem. I really liked the dual axis dot plot he created in the video, but after looking at it for a long time, it felt like it was not representative of the data. The circles don't "take up room" like a bar would to be more comparable in size. 

## Step three: Sketch a solution

When I began sketching a solution, I first stopped to really think about what I was looking to achieve. I decided to start in Datawrapper because it felt a lot less intimidating to dive into compared to more complex tools.

I went through and tested several different graph styles, and I ultimately chose a separated bar chart layout with clear spacing in between the rows rather than keeping the original stacked bar format. From there, I adjusted the colors to align with intuitive associations:

- Red represents incorrect answers ("Can cure").
- Green represents correct answers ("Cannot cure").
- Gray de-emphasizes uncertainty ("Don't know").

In KFF's original visual, the gray bar was actually what your eye was drawn to first simply because it stood out against the surrounding blues. By switching to green for the correct response, I aimed to leverage the Western cultural association that green signifies "correct."

I also deleted the color legend entirely because it felt redundant, much like the original figure on the KFF website. Instead of a separate key, I added clear column titles directly above each panel. This created a much smoother narrative flow from top to bottom.

Next, I brainstormed different titles by looking closely at the data to see what insight jumped out the most. The educational breakdown was the clearest pattern, so I reworked the headline to highlight education status.

As I worked deeper into Datawrapper, however, I began hitting frustrations with the tool's limitations:
- I wanted to reorder the main demographic categories so they would tell a more compelling, logical story.
- I wanted to reorder the subcategories (like education levels) into a progression that made sense.
- Because I wasn't used to using the software, I couldn't get to the level of micro-customization I wanted.

<img width="755" height="706" alt="DataWrapperDraft" src="https://github.com/user-attachments/assets/28e04bdd-b927-4b6c-9ab4-d2c084e81d4c" />
Ultimately, I walked into class with a draft I wasn't 100% in love with, but I knew exactly which elements were falling short and what needed to change in the next iteration.

## Step four: Test the solution

- "Is there anything that is too redundant in my graph?"
Peer 1: Felt that including the Age category was redundant and could be removed.
Peer 2: Agreed that Age was redundant and didn't add much value to the story.
Peer 3: Thought Age was interesting and suggested it didn't hurt to keeping it in.

- "What should the order of the colors/columns be?"
Peer 1: Recommended ordering from Green (Correct) $\rightarrow$ Gray (Uncertain) $\rightarrow$ Red (Incorrect).
Peer 2: Agreed that Green should come first, followed by Gray, then Red.
Peer 3: Initially leaned toward putting Red first, but eventually agreed that leading with Green created a better flow.

- "Is the title too poignant or overly focused on just one category?"
Peer 1: Loved the title, calling it catchy, and suggested moving Education to the top of the chart to align with it.
Peer 2: Agreed the title worked really well, and noted that the data labels should show percentage signs (%).
Peer 3: Thought the title was strong and that the overall draft was in great shape.

The first question about redundancy showed me something that I didn't see, so I had to go back and re-evaluate if age was something that was actually necessary in showing this graph. Between deciding to drop Age, needing to reorder the categories to match my title, and wanting  percentage signs on my bar labels, Datawrapper's limitations became overwhelming. Hearing this feedback put the nail in the coffin *wop wop wooOOoop* that I needed to give up on Datawrapper and move on to Tableau. 

## Step five: Build the Solution

Before committing to the final small-multiples bar chart, I wanted to test all feedback from my critique session. One group member had recommended redoing the entire visualization into pie charts. I experimented with a pie chart layout in Tableau, but I quickly realized it made comparative analysis much worse. Comparing angles and slices across eight different demographic groups and three response categories created extreme visual clutter. It confirmed my intuition that horizontal bar charts anchored to a shared baseline were the best choice for fast, accurate reading.

- Layout: I reorganized the demographic categories to place Education at the very top, directly supporting my headline hook ("Health Literacy Rates Double through the American Education System"). Viewers can immediately see the green bar jump from 26% (High school diploma or less) up to 65% (At least a college degree).

- Intuitive Color Semantics & Column Flow:
  -Green ("No, cannot be cured" (correct)): Positioned in the first column to immediately reward the eye with correct health literacy rates.
  -Gray ("Don't know enough to say"): Positioned in the middle panel to de-emphasize passive uncertainty without distracting from the main story.
-  Red ("Yes, can usually be cured"): Positioned in the final panel to isolate active misinformation.

-Proportional Context: I locked every paneled horizontal axis to a fixed 0%–100% range with explicit 25% tick marks. This ensures that a 26% bar in one row represents the exact visual proportion out of 100% as a 26% bar in another row.

- Percentage: Every bar features bold percentage text positioned right at the bar end, eliminating the need to trace gridlines down to an axis.

- Citation: I added a clear citation footer at the bottom linking directly back to KFF’s original 2019 study.

Overall, I am thrilled with how much cleaner, clearer, and more narrative-driven this final visualization turned out compared to the original KFF Figure 6. It tells a story in seconds without requiring the reader to dive into a dense article.

The one detail I wish I could change is the display of the main category headers (Education, Income, Gender). I wanted these labels to sit horizontally above their subcategories as section title rows rather than being rotated vertically on the far-left pane. I spent a lot of time tweaking Tableau settings trying to force horizontal title placement within a single paneled sheet, but Tableau’s default axis formatting made that layout difficult to execute.

Despite that minor formatting hiccup, moving away from stacked bars and blue branding completely transformed the graphic. The final design makes this a more accessible public health story.

<img width="998" height="599" alt="Health" src="https://github.com/user-attachments/assets/29360772-b510-42ab-8757-290e4b541801" />

## References

Andy Kriebel (Director). (2024, April 1). How ignorant are American men about antibiotics? [Video recording]. https://www.youtube.com/watch?v=VeSwnexUU4s

Data Visualization Effectiveness Profile. (n.d.). Retrieved September 17, 2026, from https://www.perceptualedge.com/articles/visual_business_intelligence/data_visualization_effectiveness_profile.pdf

kfflunnal. (2019, June 21). Data Note: Public Awareness Around Antibiotic Resistance. KFF. https://www.kff.org/other-health/data-note-public-awareness-antibiotic-resistance/

Martin, F. &. (2015, April 3). Design and Redesign. Medium. https://medium.com/@hint_fm/design-and-redesign-4ab77206cf9


## AI acknowledgements
I Googled help troubleshoot why the clickable links to my pages were not working properly, which is technically the AI tool called Gemini. 

