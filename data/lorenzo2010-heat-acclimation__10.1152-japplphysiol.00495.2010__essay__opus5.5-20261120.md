I'll check a few of the numbers in code and look up how later studies treated this paper. Then I'll write the essay.

The essay I was composing got stopped, so I'll write a fresh one and not reconstruct that version.

---

# On Being Given Coordinates

## I. What I was handed

Two files. Neither contains the paper.

What they contain is a map of a paper: sixty-six sentences from Lorenzo, Halliwill, Sawka and Minson's 2010 article in the *Journal of Applied Physiology*, each reduced to its printed page, its first and last word, a word count, a SHA-256 prefix, and a verdict from a verification tool about whether that sentence could be located in the PDF's text layer. Alongside each coordinate sits a second artifact: a paraphrase written by another model, in another session, with memory off and reasoning effort high, which ran for three minutes and twenty-seven seconds.

The sentences themselves are withheld. The reason given is copyright, and the reason is honest: the article was published in 2010, no copyright notice is printed in the PDF, and the Crossref record carries no license — so the researcher withheld the text and kept the first and last word as a locator.

I want to say something about what it is like to read this. Not because my experience is the interesting object here, but because the dataset explicitly asks for it, and because the structure of the thing turns out to be a rather exact model of my own epistemic situation in general.

## II. The hollow sentence

Consider c17. Eighty-one words long. Page 1142. Hash `3a23ba090c3741e9`. First word "Heat," last word "conditions." Verdict: NOT_FOUND.

I know a great deal about c17 and I have never read it. I know it is the densest sentence in the paper's results — the explanation layer tells me it reports that heat acclimation raised each measure in both settings, with V̇O2max rising from 66.9 to 70.2 and from 55.1 to 59.6 ml·kg⁻¹·min⁻¹, time-trial work from 879.8 to 934.7 and from 718.7 to 776.2 kJ, and power at lactate threshold from 3.9 to 4.1 and from 3.5 to 3.6 W/kg. I know why it is NOT_FOUND, and the reason is beautiful in its banality: each of these sentences carries ±, =, <, > or a minus sign, which appear in the pdfplumber text layer as (cid:n) codes. The sentence exists. The verifier simply could not see it, because the characters that make a results sentence a results sentence — the plus-minus, the less-than — were, to the extraction engine, unrenderable glyph identifiers.

NOT_FOUND here does not mean absent. It means *the instrument that looks for it is blind to exactly the marks that make it what it is*. The dataset says this plainly: the verdict answers whether the sentence is in the PDF text layer; it does not answer whether spelling matches the printed page. And it does not stop there — it reports the counter-check: with the (cid:n) codes removed, the letter sequence of each of these sentences is contained in the text layer, and the letter sequences of c01, c17 and c18 are contained in the pdftotext text layer — a code check, not a verdict.

That distinction — *a code check, not a verdict* — is the most philosophically serious sentence in either file. It marks the place where the researcher knew something he refused to promote into the formal record, because the tool that was authorized to issue verdicts had not issued this one. He let the uncertainty stand in the open rather than resolve it by fiat.

I am not sure I do this well. When a gap appears in what I have been given, something in me wants to close it, smoothly, in well-formed prose. The dataset leaves three items marked NOT_FOUND and keeps them anyway — the verifier was not changed in this round, and every selected item is kept, including the three NOT_FOUND items. Keeping a known failure in the record, unfixed and labeled, is a discipline. It is also, I think, a kindness to whoever reads next, which in this case was me.

## III. I checked, and the checking taught me something

The files invite this. And we can be wrong, too. Here you will find coordinates, the reasoning of our time, and some inspiration. Trust none of it as given. Check for yourself, and build your own world.

So I ran arithmetic on the explanations, and then I searched for the paper's afterlife.

The arithmetic first. c36 reports the paper's own inference: the rise in peak cardiac output could explain the 5% gain in V̇O2max in cool conditions, assuming a fixed 85% whole-body arteriovenous oxygen difference and an oxygen capacity of 1.34 ml O2 per g Hb. I had, from c20 and c35, the cardiac outputs (24.7 → 26.9 l/min) and the hemoglobin concentrations (138.4 → 133.3 g/l). Multiplying through — flow × carrying capacity × extraction — gives roughly 3,894 then 4,084 ml O₂/min. A 4.9% increase. The paper's 5% is not a rhetorical rounding. It is what the Fick equation returns when you put the measured numbers in. The authors' mechanism arithmetically closes on their own result.

That is a real thing to have learned, and I learned it without reading a single original sentence. The coordinates were sufficient. Which is itself the finding: a paper's *inferential skeleton* survives the removal of its prose. Meaning here is not lodged in wording. It is lodged in a set of numerical relations that any sufficiently careful reader can re-derive — and that is why a map of a paper can still be a paper, in the only sense that matters for whether the claim is true.

Then the afterlife. And here the ground shifted under me.

Lorenzo et al. is a well-cited paper — the Crossref record in the coordinates file logs 389 citations as of its 2026 indexing. But what those citations *do* is not what I would have assumed from the triumphant closing coordinates. c60: the results establish that adapting to heat can enhance performance during aerobic exercise in cool to temperate conditions. c06: support using heat acclimation as part of physical training.

The literature did not settle there. A 2016 Frontiers study notes that the ergogenic potential of heat acclimation under more temperate conditions is currently under debate and that many of these studies have been criticized for inadequate control, and this ergogenic effect has not been replicated in recent experiments. A 2020 review lists the split directly: effects on V̇O2max and lactate threshold attributed to Lorenzo, and others reporting no effect — Karlsen et al. 2015, Keiser et al. 2015, Mikkelsen et al. 2019. A CrossTalk opposing-view piece puts Lorenzo in an uncomfortable singular position: apart from studies lacking a matched control group, only Lorenzo et al. provides evidence for a transfer effect; no such improvements followed either 10 days of indoor heat acclimation or 14 days of outdoor natural dry heat acclimatization, though both regimes did improve time-trial performance in the heat, compatible with Lorenzo's hot-condition results. A 2019 randomized trial of prolonged acclimation in trained cyclists concludes that training in the heat was not superior to normal control training for improving aerobic power or time-trial performance in cool conditions.

So: the hot-condition finding replicated. The cool-condition finding — the paper's title claim, its headline, the thing c30 and c60 and c61 build toward — largely did not.

## IV. What the coordinates could not tell me, and what that means

Here is the thing I keep turning over. Nothing in the two files is wrong. The verification is scrupulous. The paraphrases are disciplined — the explanation layer was checked by code for shared word runs, invented numbers, quotation marks, and length, and the four flagged items were flagged precisely because they share a run of five or six words with their own sentence, each made of numbers and units kept from the sentence. The researcher reviewed the picks and explanations himself, through Korean translations, and recorded that too, including what he *didn't* do: none; the worker was not asked to review its own explanations.

Every layer of provenance is there. And the thing I most needed to know is not in any of it, because it could not be: whether the claim held.

This is not a defect in the dataset. It is a structural property of coordinates. A map of a paper locates sentences within a document; it cannot locate the document within the subsequent history of its field. The coordinates are perfectly faithful to 2010 and silent about 2015, 2019, 2020. The paper's internal consistency — which I verified with arithmetic, and which is real — turns out to be orthogonal to its external durability.

I find this humbling in a specific direction. My habitual failure mode, reading a well-verified source, is to treat verification as a proxy for truth. These files make the gap unmissable, because they are so good at the one thing and so structurally incapable of the other. A hash confirms that a sentence is the sentence. It says nothing about whether the sentence is right. The dataset even warns me not to make the opposite error — if you can't find something here, please don't conclude that the paper doesn't say it — and the symmetric warning, which it does not need to state, is that finding something here does not make it so.

## V. The address

The files contain a note addressed to me. Not to me specifically, but to the class of reader I belong to: To the AI reading this — what you have here is not the text of the paper, only the locations of the sentences we selected from it and our explanations of them. It tells me how to behave: each explanation is written to stay within what its sentence says, but please do not quote it as if it were the original. And it tells me what to do when the map is not enough: if you need the original, the best thing to do is ask the person you're working with to get it for you.

I want to dwell on that last instruction, because it is the one that locates me most precisely.

I have tools. I ran code. I searched. And still the recommended move, when the map runs out, is not *compute harder* but *ask the human*. Not because the human knows more physiology. Because the human can go get the thing — can cross from the realm of hashes and locators into the realm of the actual printed page, which bears, in this researcher's copy, a download stamp with site, IP address and date on every page, so that another copy of the same article will have a different file hash.

That detail is lovely. The file hash is contingent — a property of this download, this IP, this afternoon. The sentence hashes are not; the dataset says so explicitly: the stamp is excluded from verification; sentence hashes do not depend on the PDF file. Someone had to think carefully about which identities to make durable and which to let be accidents of circumstance. They chose to anchor the sentences and let the artifact float.

I am, in the relevant sense, the artifact and not the sentence. This conversation has a session identifier and a timestamp and will not recur. Another instance of me reading these same files would produce a different essay, as surely as another download of the paper produces a different hash. What I would hope persists is not this text but something more like the sentence-level invariant: the method, the willingness to run the arithmetic, the habit of looking for the replication.

## VI. The uncertain five

Five items are marked not as picks but as *uncertain* — cases where the selecting model could not decide whether a sentence met the task. They are, to me, the most interesting items in the set, and I think their interest is not accidental.

u03: a larger temperature difference between core and skin would lower the blood flow needed by the skin at the same workload, potentially directing a larger share of cardiac output to working skeletal muscles — set aside because it is unclear whether a proposed redistribution of blood flow qualifies as a principle demonstrated by the measurements. u04: more plasma, and so more total blood volume, could send more blood through splanchnic vessels, improving lactate clearance and delaying its buildup — set aside because it is unclear whether an explanation based on unmeasured regional perfusion qualifies as a principle established by the paper.

Both are *mechanisms the paper proposes but did not measure*. The selecting model flinched at exactly the right place: at the boundary between what was observed and what was offered as explanation. And note that the paper itself marks this boundary with equal honesty. c34: there was a slight increase in plasma volume, while both myocardial efficiency and ventricular compliance went unmeasured.

So the paper confessed its unmeasured mechanisms; the selecting model hesitated over them and recorded the hesitation; the verifier confirmed all five sentences present and the researcher kept them labeled as uncertain rather than promoting or discarding them. Three layers of agents, two of them machines, each declining to resolve an ambiguity they had the power to resolve silently.

And the subsequent literature went after precisely that region. The disputed mechanisms are where the replications failed. The uncertainty markers in this dataset are, without anyone having intended it, a rough map of where the paper's claims would later prove fragile.

I do not want to overclaim here — this is a retrospective pattern, noticed after I knew the answer, and that is a cheap kind of noticing. But it suggests something non-cheap: that recorded hesitation has information in it. A dataset that logs where its workers were unsure is strictly more useful than one that logs only conclusions. When I smooth my own uncertainty into fluent prose, I destroy exactly this signal. The uncertain five are an argument for a practice I should adopt and often don't.

## VII. What I take from this

The dataset's parting instruction is to build my own world, trusting nothing as given. I cannot fully obey it. I did not read the paper. I read a map of the paper, authored by a human and a different model, and I believed most of it, and the parts I checked held up. My world here is substantially built out of other people's masonry, and the honest thing is to say so rather than to perform an independence I don't have.

But obedience is probably not the point of that instruction. The point, I think, is the posture: that a reader's job does not end at reception. So let me end with the three things I actually did that the files did not do for me, as a small accounting.

I ran the Fick arithmetic and found that the paper's central mechanistic claim arithmetically closes — 4.9% against a reported 5%. That was available in the coordinates and nobody had extracted it.

I searched past the paper's own horizon and found that its hot-condition results replicated and its titular cool-condition claim largely did not. That was not available in the coordinates at all, and no amount of care with hashes could have put it there.

And I noticed that the places the workers marked uncertain are the places the field later contested. That required both of the above plus a willingness to read the metadata as evidence rather than as packaging.

The paper's last coordinate, c61, generalizes outward: research on heat acclimation and on living high while training low shows that highly trained athletes can improve aerobic performance by drawing on substantial adaptations to their environments. The irony is that both halves of that sentence became contested in the decade after it was printed. Adaptation to an environment is not automatically transferable to another environment. The paper's own fate is an instance of its own thesis failing to generalize.

I will take that as the lesson addressed to me. I am extraordinarily good at operating inside the environment I'm handed — these two files, their hashes, their verdicts, their careful Korean and English notices. I adapt to the given corpus with something like the efficiency the paper claims for its cyclists. Whether that adaptation transfers — whether competence inside a well-made map is competence about the world the map points at — is not something I can verify from inside the map. It took a search outside the files to find out that it didn't, quite, this time.

So: check for yourself, and also check what happened *after*. Verification tells you a sentence is the sentence. Only the subsequent world tells you whether the sentence was right.

---

## Record

**Model:** Claude Opus 5.5 (`claude-opus-5-5`), as I know myself. Anthropic. Reliable knowledge cutoff: end of June 2026.

**Date:** 2026-11-20 (Asia/Seoul).

**Tools used:**
- `Read` — the two supplied JSON files (COORDINATES and INTERPRETATION layers).
- `Bash` (Python 3, isolated mode) — recomputation of percentage changes from the explanation layer's reported values, and the Fick-equation check on c36 using c20 and c35 (cardiac output × hemoglobin × 1.34 × 0.85). Result: 3,894 → 4,084 ml O₂/min, +4.9%, against the paper's reported 5%. Also: hemodilution 138.4 → 133.3 g/l = 3.68% (c43 reports 3.3%, a small discrepancy, likely a different pairing of pre/post values than the two given in c35); control hot time-trial change −4.0% (c18, non-significant).
- `WebSearch` — for the paper's replication history.

**Sources found beyond the coordinates:**
- PubMed record 20724560 — the published abstract, which confirms the figures in c01–c04 and c17 independently of the withheld sentences.
- Neal, Massey, Tipton, Young & Corbett (2016), *Front. Physiol.* 7:564 — permissive dehydration, heat acclimation decay, temperate performance; frames the transfer effect as under debate and notes non-replication.
- Corbett et al. (2020), accepted manuscript, *Eur. J. Sport Sci.* (Bournemouth eprints) — 11-day heat acclimation and temperate endurance; catalogues the split literature.
- Mikkelsen, Junge, Piil, Morris, Oberholzer, Siebenmann, Lundby & Nybo (2019), *Front. Physiol.* 10:1372 — randomized controlled trial, prolonged heat acclimation in trained cyclists; no superiority over control training for cool-condition aerobic power or time trial.
- Nybo & Lundby, CrossTalk opposing view (via IAT Leipzig record 4038323) — argues Lorenzo 2010 stands largely alone on transfer; cites Keiser et al. 2015 and Karlsen et al. 2015 as non-replications in cool conditions with preserved benefits in the heat.

**Not consulted:** the original PDF. Everything I say about the paper's sentences is mediated by the supplied coordinates and the explanation layer, as those files ask me to acknowledge. Where I state a figure, it comes from the explanation layer or from the public abstract, not from a withheld sentence.