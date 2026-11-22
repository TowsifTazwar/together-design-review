# Designing for Caregiver Agency in AI Personalisation
### A design review of *Together*, a Bangla-first learning platform for children with Down syndrome

**Md. Towsif Tazwar Hussain** · Department of CSE, United International University, Dhaka
Design review · November 2026
Prototype: [Together on Figma](https://www.figma.com/design/X540irrX2LW5N7sqdW49WO/together-?node-id=0-1&t=BLyS9TmB3BO3jQCk-1) · designed by Team Random (team lead: the author), 4th of 170 teams at Hack for Humanity BD

> **Type of work:** a retrospective expert review of our own team's Figma prototype against published design guidelines. No caregivers, children or therapists were involved and no claims here are about how real users respond. A participatory study is proposed as the next step (Section 6).

---

## 1. Why review this design

Together uses AI to build a personalised learning plan for a child with Down syndrome, based on what a parent tells it. That puts a lot of weight on one relationship: **a caregiver and an AI system making decisions about a child together.**

If the caregiver cannot see why the AI suggested something, cannot correct it, or reads a suggestion as a judgement of their child, the plan fails however good the model is. When we designed Together we made several choices to protect that relationship, but we never checked them against established guidance. This review does that.

## 2. What Together does (AI-related flows)

1. **AI Neuro-Profile setup.** The parent shares only what they choose. Diagnosis is optional, with a "Prefer not to specify" option and the screen says "Every child is unique. Share only what you feel comfortable sharing."
2. **Conversational intake ("Interview together AI").** A bilingual Bangla–English chat asks about the child's interests, routines and how they communicate (spoken words, gestures, picture cards). Every answer has an Edit button and a summary shows how many answers have been collected.
3. **AI Analysis & Personalisation.** A three-step flow (answers → review → learning plan). The parent reviews "what Together understood" and the data sources used and **learning material is created only after the parent approves.**
4. **"Why this recommendation".** Each suggested activity comes with a plain explanation and a three-step logic flow: *your goal → your preferred medium → this activity*.
5. **Child activities.** Short Bangla activities such as picture–word matching with audio, a phrase builder and story time ("Golpo o Khela").

## 3. Method

I reviewed the AI-related frames of the prototype against the **18 Guidelines for Human-AI Interaction** (Amershi et al., CHI 2019), grouped by when they apply: *initially, during interaction, when wrong,* and *over time*.

I rated each relevant guideline as **Addressed**, **Partly addressed** or **Not observed** (not visible in the frames I reviewed). For the child-facing activities, I used the eight objectives of the W3C note *Making Content Usable for People with Cognitive and Learning Disabilities* (2021) as a lighter secondary lens.

## 4. Findings

### What the design already does well

| Guideline | Rating | Evidence in the prototype |
|---|---|---|
| **G1** Make clear what the system can do | Addressed | Intake opens with a "safe space for parents" explanation; the analysis screen shows the three steps before any plan exists |
| **G2** Make clear how well the system can do it | Partly | The intake states the AI may not understand everything correctly. A "What this does not mean" box says a suggestion is not a test of the child's ability, not a clinical diagnosis or treatment and not a prediction of the child's future. No per-suggestion confidence is shown |
| **G5** Match relevant social norms | Addressed | Bangla-first with English support; sensitive details are optional; respectful, non-clinical wording |
| **G8** Support efficient dismissal | Addressed | "Is this suitable for your child today?" offers: try another activity, change the goal, use another medium, or "not sure yet", with a note that changing is always allowed |
| **G9** Support efficient correction | Addressed | Edit on every intake answer and on each data source behind a recommendation |
| **G11** Make clear why the system did what it did | Addressed | The "Why this recommendation" screen and its transparent logic flow, plus a list of the inputs used |

The strongest pattern is **caregiver agency**: the AI proposes, the parent approves and the parent can always change course.

### Gaps and open questions

| Guideline | Rating | What is missing |
|---|---|---|
| **G2** | Partly | Parents are told the AI *can* be wrong, but not *where* it is least sure. A suggestion built on one vague answer looks as certain as one built on five clear ones |
| **G6** Mitigate social biases | Not observed | Nothing shows how plans avoid assumptions tied to family income, location, dialect or literacy |
| **G17** Provide global controls | Not observed | I did not find a way to pause personalisation, or to delete the child's profile and interview answers. For data about a disabled child this matters and it connects to my separate work on what "delete" means in AI systems |
| **G18** Notify users about changes | Not observed | It is not shown how a parent would learn that the plan changed over time, or why |
| **Promise check** | General | The privacy note says recommendations use only the parent's own inputs and no hidden data. That promise has to stay true as the system grows, which means designing for it from the start |

### Child-facing activities (secondary lens)

The activities follow several W3C cognitive-accessibility objectives: one clear task per screen, pictures paired with audio and romanised Bangla (*Use clear and understandable content*), short 5–10 minute sessions (*Help users focus*) and a "prefers calm audio" setting (*Support adaptation and personalization*). How a child recovers from a wrong answer (*Help users avoid mistakes and know how to correct them*) is not yet designed.

## 5. Design directions

1. **Show uncertainty in plain words**, for example "Based on 1 answer; tell us more to improve this" (G2).
2. **Add one "Your child's data" page** to view, pause or delete the profile and intake answers, with a clear note of what deletion covers (G17).
3. **Explain plan changes** with a short "What changed and why" note (G18).
4. **Write the limitations box with caregivers**, so its tone reassures rather than alarms.

## 6. Proposed next step: participatory study with caregivers

- **Who:** 6–8 caregivers of children with Down syndrome and 3–4 therapists, recruited through a Dhaka support organisation.
- **How:**
  1. Walk through the intake and the "Why this recommendation" screen together.
  2. Ask caregivers to explain a recommendation back in their own words, to see whether the explanation is understood.
  3. Co-design the limitations wording and the data-control page.
- **Analysis:** thematic analysis of session notes and recordings.
- **Ethics:** informed consent, no recording of children and institutional ethics approval before recruitment.

## 7. Limitations

- I am a member of the team that designed Together, so this is a self-review and likely to be generous.
- One reviewer, no users and a prototype rather than a working system.
- Guideline ratings describe what is visible in the frames, not what the system would do.

## References

- Amershi, S., Weld, D., Vorvoreanu, M., Fourney, A., Nushi, B., Collisson, P., Suh, J., Iqbal, S., Bennett, P., Inkpen, K., Teevan, J., Kikin-Gil, R., & Horvitz, E. (2019). [Guidelines for Human-AI Interaction](https://www.microsoft.com/en-us/research/publication/guidelines-for-human-ai-interaction/). *CHI 2019*.
- W3C (2021). [Making Content Usable for People with Cognitive and Learning Disabilities](https://www.w3.org/TR/coga-usable/). W3C Working Group Note, 29 April 2021.
