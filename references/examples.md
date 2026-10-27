# Before and after

Each pair keeps the original ask as the floor and shows which axes did the stretching.

## 1. Fixing a bug (Altitude + Depth)

**Before:** "The checkout test fails sometimes. Can you fix it?"

**After:** "Checkout tests flake and I keep re-running CI by hand. Stop that from happening. Pull the last 60 days of CI results, rank tests by flake rate, reproduce the worst offender by running it 200 times, fix the root cause (no blind retries), and add a check that fails the build if any test's flake rate climbs above 0.5%. Target: no flaky failures across 1,000 consecutive runs. You decide when it's done by those runs, not by reading the diff. Tell me which access you need and ask before pushing anything."

## 2. A launch post (Range)

**Before:** "Write a blog post announcing our new export feature."

**After:** "The post exists so people who struggle with exporting try the feature within five minutes. Mine the last 90 days of support tickets for how customers describe the problem, write the post in those words, then run it past four passes: an editor who cuts a third, a skeptic who stops reading at the first vague claim, a fact-check against the product's actual behavior, and a headline test of ten variants judged by the skeptic. Give me the post and the evidence behind each claim. Don't publish anything."

## 3. Learning (Depth)

**Before:** "Explain how Kubernetes networking works."

**After:** "I want to debug my own cluster's networking in two weeks. Build me a small local cluster with deliberately broken networking in five different ways, hand them to me one at a time with only the symptoms, and check my diagnosis each time against what's really broken. Start from the packet path, not the abstractions. After each exercise, tell me what a platform engineer would have checked first."

## 4. Job search (Altitude + Range)

**Before:** "Polish my resume."

**After:** "I want interviews for product-analyst roles at mid-size SaaS companies. Gather 50 current postings, extract what they ask for and how they word it, find where my experience genuinely matches and where it doesn't, then tailor two versions of the resume. Have a recruiter-pass and a hiring-manager-pass attack each version and revise. Don't invent experience; list real gaps with a plan to close them. Target: each version matches at least 80% of the 'required' items across the postings, and I can defend every line in an interview."

## 5. When to keep it small

**Before:** "Write a short poem for my mom's 60th birthday. She loves gardening and terrible puns. Be ambitious!"

**After (ambition as craft):** Write it as a sonnet or another demanding form, make the puns structural rather than sprinkled, draft a few options and pick the strongest, and hand back one finished poem with at most a sentence or two of commentary. No research project, no validation tooling. The user asked for a poem.
