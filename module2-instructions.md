# MODULE 2 — TRADE ESSENTIALS: Full Enhanced Data

## INSTRUCTIONS FOR CLAUDE CODE

In `src/App.jsx`, find the current Module 2 placeholder (around line 394):

```
{ id: 'module-2', title: "Trade Essentials", subtitle: "Rules of Valid Transactions", icon: "🤝", color: "#d97706", difficulty: "Beginner", estimatedTime: "35 min", lessonCount: 3, lessons: [
  { id: 'l2-1', title: "Valid Sale", description: "Pillars & conditions", duration: "7 min", questions: [] },
]},
```

Replace it ENTIRELY with the following data. Keep the EXACT same JS object format used by Module 1 lessons. Each question needs: concept, question, type, options, correct, explanation, uiType. Some have visual objects too.

---

## REPLACEMENT MODULE 2 DATA

```javascript
{ id: 'module-2', title: "Trade Essentials", subtitle: "Rules of Valid Transactions", icon: "🤝", color: "#d97706", difficulty: "Beginner", estimatedTime: "90 min", lessonCount: 5,
  mascotMessage: "Time to learn what makes a sale actually valid — not just legal, but Islamically sound!",
  lessons: [
    // ═══════════════════════════════════════════════════════
    // LESSON 1 — Valid Sale: Pillars & Conditions
    // ═══════════════════════════════════════════════════════
    { id: 'lesson-2-1', title: "Valid Sale: Pillars & Conditions", description: "The five pillars every sale needs", duration: "12 min",
      questions: [
        // --- ZONE 1: WARM-UP (Q1-3) ---
        { concept: "A valid sale (bay') needs five pillars: (1) offer & acceptance, (2) lawful & specified subject matter, (3) known price, (4) ability to deliver, (5) absence of riba/gharar/maysir.\\nIf ANY pillar is missing, the contract is structurally defective -- not just poor practice, but invalid.\\nThe item must be owned or constructively possessed by the seller at the time of sale (exceptions: salam, istisna').\\n\\nThink of buying a car: you need to know the exact car (specified), agree the exact price (known), actually hand it over (deliverable), and both genuinely agree (consent).",
          question: "How many pillars does a valid Islamic sale (bay') require?",
          type: "multiple-choice", options: ["Three: buyer, seller, and price", "Five: offer & acceptance, specified subject, known price, deliverability, absence of riba/gharar/maysir", "Two: agreement and payment", "Four: subject, price, consent, and witnesses"], correct: 1,
          explanation: "Five pillars form the skeleton. Miss any one and the contract is structurally defective -- not just risky, but invalid. Witnesses are good practice but not a structural pillar. Payment timing is a term, not a pillar.",
          uiType: "mcq" },

        { concept: "A valid sale (bay') needs five pillars: (1) offer & acceptance, (2) lawful & specified subject matter, (3) known price, (4) ability to deliver, (5) absence of riba/gharar/maysir.\\nPrice must be known and fixed at contract -- 'we'll figure it out later' is gharar.\\nBoth parties must have legal capacity and give genuine consent (no coercion, no material deception).\\n\\nThink of an online marketplace listing: 'Price: TBD after inspection.' You can't form a binding contract with an open price.",
          question: "You're reviewing a contract for a second-hand camera on an online marketplace. Select the TWO elements that are non-negotiable for the sale to be valid.",
          type: "multi-select", options: ["The camera's condition and model are clearly specified", "The total price is known and agreed at contract", "The buyer and seller must live in the same city", "The listing must include at least five photos"], correct: [0, 1],
          explanation: "A valid sale requires a specified, identifiable subject (what exactly is being sold, in what condition) and a known price. Location proximity and photo count might be good practice, but they aren't pillars.",
          uiType: "sel2" },

        { concept: "A valid sale (bay') needs five pillars: (1) offer & acceptance, (2) lawful & specified subject matter, (3) known price, (4) ability to deliver, (5) absence of riba/gharar/maysir.\\nOne pillar is the ability to deliver. If the seller cannot actually transfer what they're selling, the sale fails on deliverability.\\n\\nThink of trying to sell a gym membership the gym says is non-transferable -- you don't have the right to hand it over.",
          question: "Complete the five pillars of a valid sale: (1) Offer & ______, (2) Lawful & specified subject, (3) Known price, (4) Ability to deliver, (5) Absence of riba, gharar & ______.",
          type: "multiple-choice", options: ["(1) silence, (5) profit", "(1) acceptance, (5) maysir", "(1) estimate, (5) delay", "(1) promise, (5) debt"], correct: 1,
          explanation: "Offer & acceptance (ijab wa qabul) forms the contractual tie. The fifth pillar blocks riba, gharar, AND maysir -- all three must be absent. A promise isn't acceptance; silence isn't consent; profit and delay aren't prohibited elements.",
          uiType: "fill" },

        // --- ZONE 2: BUILD (Q4-7) ---
        { concept: "A valid sale (bay') needs five pillars: (1) offer & acceptance, (2) lawful & specified subject matter, (3) known price, (4) ability to deliver, (5) absence of riba/gharar/maysir.\\nPrice must be known and fixed at contract -- 'we'll figure it out later' is gharar.\\n\\nA car dealership posts: 'Price to be confirmed after inspection.' You agree and pay a deposit. The buyer's obligation is undefined at the point of agreement.",
          question: "A car dealership posts: '2023 Toyota Camry, white, 18,000 km. Price: to be confirmed after inspection.' You agree to buy and pay a deposit. What is the structural issue?",
          type: "multiple-choice", options: ["No issue -- inspection-based pricing is standard commercial practice", "Price is unknown at contract -- a core pillar is missing, creating gharar", "The car must be brand new for the sale to be valid", "Only a documentation problem that can be fixed later"], correct: 1,
          explanation: "Price to be confirmed means the buyer's obligation is undefined at the point of agreement. That's a missing pillar -- known price -- not just poor UX. The deposit doesn't fix an unknown price. Inspection can happen before the sale is finalised, but you can't form a binding contract with an open price.",
          uiType: "spot" },

        { concept: "A valid sale (bay') needs five pillars: (1) offer & acceptance, (2) lawful & specified subject matter, (3) known price, (4) ability to deliver, (5) absence of riba/gharar/maysir.\\nOne pillar is the ability to deliver. If the item cannot actually be transferred, the sale is structurally defective.\\n\\nExample: a gym membership marked 'non-transferable' in the gym's terms. The seller cannot hand over what the contract doesn't allow.",
          question: "A friend wants to sell you his gym membership. The gym's terms explicitly state: 'Memberships are non-transferable.' Can this sale go ahead?",
          type: "multiple-choice", options: ["Yes -- a sale is between two people, the gym can't intervene", "No -- the subject matter is not deliverable; the seller can't transfer what the contract doesn't allow", "Yes, but only at a discounted price", "Only if the gym doesn't find out"], correct: 1,
          explanation: "One pillar of a valid sale is the ability to deliver. If the gym's terms prohibit transfer, the seller cannot actually hand over what they're selling. Discounts, secrecy, or the gym 'not finding out' don't create deliverability. The right to transfer simply doesn't exist here.",
          uiType: "mcq" },

        { concept: "A valid sale (bay') needs five pillars: (1) offer & acceptance, (2) lawful & specified subject matter, (3) known price, (4) ability to deliver, (5) absence of riba/gharar/maysir.\\nGenuine mutual consent (ridha) is foundational. A contract signed under duress or material coercion is defective because the seller's agreement isn't real.\\n\\nThink of a property developer threatening a small shop owner: 'Sell to me or I'll destroy your business.' A signed document doesn't equal valid consent.",
          question: "A property developer tells a shop owner: 'Sell me your unit at AED 400,000, or I'll make sure the municipality rezones your area and your business dies.' The shop owner signs. Is this sale valid?",
          type: "multiple-choice", options: ["Valid -- a signed contract is a signed contract regardless of context", "Invalid -- genuine consent (free from coercion) is a requirement for a valid sale", "Valid if the price is objectively fair for the area", "Only invalid if witnesses were present during the threat"], correct: 1,
          explanation: "Genuine mutual consent (ridha) is foundational. A contract signed under duress is defective because the seller's agreement isn't real. Fair price doesn't cure forced consent. Witness presence is about evidence, not about whether coercion occurred.",
          uiType: "mcq" },

        { concept: "A valid sale (bay') needs five pillars: (1) offer & acceptance, (2) lawful & specified subject matter, (3) known price, (4) ability to deliver, (5) absence of riba/gharar/maysir.\\nAll five pillars must be present simultaneously. Remove any one and the contract is structurally defective.\\n\\nThe five pillars work like a chain -- each link matters. A beautiful price means nothing if the subject is unspecified.",
          question: "True or False: A sale can still be valid if the price is fair, the item is described, and the buyer is happy -- even if the seller was coerced into selling.",
          type: "multiple-choice", options: ["True -- buyer satisfaction validates the sale", "False -- all five pillars must be met, including genuine consent from BOTH parties"], correct: 1,
          explanation: "ALL five pillars must be present. Coerced consent is not genuine consent, regardless of how satisfied the other party is. A fair price, a described item, and a happy buyer don't cure a fundamentally broken pillar.",
          uiType: "mcq" },

        // --- ZONE 3: STRETCH (Q8-10) ---
        { concept: "A valid sale (bay') needs five pillars: (1) offer & acceptance, (2) lawful & specified subject matter, (3) known price, (4) ability to deliver, (5) absence of riba/gharar/maysir.\\nSubstance over labels: what something IS matters more than what it's CALLED. A 'gift' with strings attached might actually be a defective sale.\\n\\nThink of a 'free trial' that auto-charges without clear disclosure -- the label says free, the substance says sale.",
          question: "A mobile app is listed as 'free' in the App Store. Once downloaded, it requires a AED 49.99 'activation fee' before any features work. No mention of this fee in the listing. Which pillar is compromised?",
          type: "multiple-choice", options: ["No pillar is compromised -- the fee is disclosed inside the app", "Known price -- the total cost was not known at the point of agreement to download", "Deliverability -- the app was delivered to the phone", "Absence of maysir -- the hidden fee is like gambling"], correct: 1,
          explanation: "The user agreed to download a 'free' app. The real cost (AED 49.99) was concealed. That's a price unknown at the point of the initial agreement -- gharar in the pricing. Delivery happened physically, but the contractual price was hidden. This isn't maysir (no chance element).",
          uiType: "spot" },

        { concept: "A valid sale (bay') needs five pillars: (1) offer & acceptance, (2) lawful & specified subject matter, (3) known price, (4) ability to deliver, (5) absence of riba/gharar/maysir.\\nIn Module 1 we learned that hiding defects corrupts consent and makes earnings haram.\\n\\nCross-reference: Lesson 1 (Module 1) -- truthful dealing is mandatory. Hiding defects or faking scarcity corrupts consent.",
          question: "A used car dealer resets odometers before listing cars for sale. The prices are fair for the mileage shown. The cars run fine. How many pillars are affected?",
          type: "multiple-choice", options: ["None -- the cars work and the prices are reasonable", "One -- the subject matter is misspecified (the true mileage is concealed)", "Two -- misspecified subject matter AND compromised consent (buyer's agreement is based on false information)", "Three -- add absence of riba"], correct: 2,
          explanation: "Two pillars are hit. The subject matter is not truly specified (fake mileage = buyer doesn't know what they're actually buying). And genuine consent is compromised (the buyer's 'yes' is based on false information). A 'fair' price based on fraudulent specs isn't actually fair. Riba isn't involved -- this is about deception, not interest.",
          uiType: "mcq" },

        { concept: "A valid sale (bay') needs five pillars: (1) offer & acceptance, (2) lawful & specified subject matter, (3) known price, (4) ability to deliver, (5) absence of riba/gharar/maysir.\\nThe adviser question: can you explain the pillars to someone else in a practical way?\\n\\nYour cousin wants to sell handmade jewellery on Instagram. What should you tell her?",
          question: "Your cousin is launching a handmade jewellery business on Instagram. She asks: 'What do I need to make sure each sale is valid from an Islamic perspective?' Give the best advice.",
          type: "multiple-choice", options: ["Just price your items fairly and you'll be fine -- Islam is flexible on commercial details", "Make sure each listing clearly specifies the item (materials, size), states the exact price, you actually have the item ready to ship, the buyer agrees before you charge, and there's no deception in your descriptions", "Get an Islamic finance certificate before selling anything", "Only sell to Muslims to keep it halal"], correct: 1,
          explanation: "The five pillars in plain language for a small business: describe your product honestly (specified subject), state the price clearly (known price), have it ready to ship (deliverable), get clear agreement before charging (offer & acceptance), and don't deceive in your descriptions (no gharar). She doesn't need a certificate -- she needs good practice.",
          uiType: "advise" }
      ]
    },

    // ═══════════════════════════════════════════════════════
    // LESSON 2 — Ownership & Possession (Asset-First Rule)
    // ═══════════════════════════════════════════════════════
    { id: 'lesson-2-2', title: "Ownership & Possession", description: "Don't sell what you don't own", duration: "12 min",
      questions: [
        // --- ZONE 1: WARM-UP (Q1-3) ---
        { concept: "Don't sell what you don't own or possess (hadith). This is a structural rule, not a guideline.\\nConstructive possession (warehouse receipt, title documents, control + risk transfer) can count when the seller truly bears the risk.\\nExceptions are structured contracts (salam, istisna'), not loopholes for anything you want to sell.\\n\\nThink of a dropshipper who lists products they've never touched -- they're selling someone else's inventory.",
          question: "True or False: You can sell an item you don't yet own as long as the buyer is willing to wait for delivery.",
          type: "multiple-choice", options: ["True -- buyer willingness covers the seller's lack of ownership", "False -- the seller must own or possess the item before concluding the sale (with structured exceptions like salam)"], correct: 1,
          explanation: "Ownership before sale is a structural requirement, not a preference. Buyer patience doesn't cure the seller's lack of ownership. Salam and istisna' are specific structured exceptions with their own strict rules -- they're not blanket permission to sell what you don't have.",
          uiType: "mcq" },

        { concept: "Don't sell what you don't own or possess (hadith). This is a structural rule, not a guideline.\\nThe test: does the seller carry real risk of loss on this asset right now? If not, they can't sell it.\\n\\nAn online reseller lists AirPods at AED 899. When a customer orders, the reseller only then buys from a supplier and ships directly. The reseller never owns or holds inventory.",
          question: "An online reseller lists AirPods on their store at AED 899. When a customer orders, the reseller buys from a supplier and ships directly to the customer. The reseller never holds inventory. What is the core issue?",
          type: "multiple-choice", options: ["No issue -- this is efficient supply chain management", "Selling before ownership or possession -- a structural defect", "Only a logistics problem that doesn't affect validity", "Fine as long as the customer receives the product"], correct: 1,
          explanation: "The reseller is finalising a sale for an item they neither own nor possess at the time of contract. Customer satisfaction, delivery speed, and logistics are commercial considerations -- but they don't fix the structural problem.",
          uiType: "mcq" },

        { concept: "Don't sell what you don't own or possess (hadith).\\nConstructive possession means: legal control, payment made, risk transferred. Physical holding isn't the only form of valid possession.\\n\\nAn electronics distributor paid in full, received title/invoice, goods insured under her name in the manufacturer's warehouse. Physical pickup next week.",
          question: "A distributor buys 500 laptops. She has paid in full, holds the title/invoice, and goods are insured under her name in the manufacturer's warehouse. Physical pickup is next week. Can she resell some units now?",
          type: "multiple-choice", options: ["Absolutely not -- she must physically hold every unit before selling any", "Generally yes -- she has constructive possession (legal control, payment made, risk transferred)", "Only if the buyer collects directly from the warehouse", "Only if the market price hasn't changed since purchase"], correct: 1,
          explanation: "The distributor has constructive possession: paid in full, holds title, insured under her name, bears the risk of loss. This level of control normally permits resale before physical pickup. What matters is: who controls the goods and who bears the risk?",
          uiType: "mcq" },

        // --- ZONE 2: BUILD (Q4-7) ---
        { concept: "In murabaha, the bank MUST own the asset before selling it to the customer.\\nThe sequence matters: identify -> bank acquires -> bank sells -> you pay.\\nOwnership must sit with the bank before the sale to you is executed.\\n\\nIf the bank sells before owning, it's not murabaha -- it's a loan dressed in sale language.",
          question: "Put a murabaha smartphone purchase in the correct sequence.",
          type: "multiple-choice", options: ["You pay -> Bank sells -> Bank buys -> You identify", "You identify the phone -> Bank purchases and owns it -> Bank sells to you at cost + markup -> You pay by schedule", "Bank sells -> You identify -> You pay -> Bank buys", "Bank buys -> You pay -> Bank sells -> You identify"], correct: 1,
          explanation: "The sequence matters: identify, then bank acquires, then bank sells, then you pay. Ownership must sit with the bank before the sale to you is executed. Skipping or reordering the ownership step collapses the structure into a personal loan with extra steps.",
          uiType: "mcq" },

        { concept: "In murabaha, the bank MUST own the asset before selling it to the customer.\\nThe sale price (cost + markup) is fixed and disclosed upfront.\\nCalling monthly payments 'interest' internally doesn't change substance, but it signals the institution may be treating it as a loan.\\n\\nA valid murabaha has two guardrails: (1) bank owns first, (2) total price fixed at contract.",
          question: "You're reviewing a bank's murabaha product for home appliances. Select ALL conditions that help keep the murabaha valid.",
          type: "multi-select", options: ["The bank actually buys and takes ownership of the appliance before selling it to the customer", "The sale price (cost + markup) is fixed and disclosed upfront", "The bank calls the monthly payments 'interest' in internal documents", "The bank sells from a catalogue of items it hasn't yet purchased"], correct: [0, 1],
          explanation: "Murabaha is only valid when the bank truly owns the asset and bears its risk before reselling, and when the final sale price is fixed at contract. Labelling payments as 'interest' internally signals loan treatment. Selling items not yet purchased is the exact ownership defect murabaha is supposed to avoid.",
          uiType: "sel2" },

        { concept: "The core test for possession (qabd) is risk. If the asset were destroyed right now, who takes the hit? If it's the seller, they have possession. If not, they're selling something they don't truly hold.\\n\\nReceipts are evidence but not the test. A good price is irrelevant to the possession question.",
          question: "What single question best tests whether a seller has valid possession?",
          type: "multiple-choice", options: ["Does the seller have a receipt for the item?", "Does the seller bear the real risk of loss on this asset right now?", "Did the seller negotiate a good purchase price?", "Is the buyer willing to wait for delivery?"], correct: 1,
          explanation: "The core test for possession (qabd) is risk. If the asset were destroyed right now, who takes the hit? Receipts are evidence but not the test. A good price is irrelevant. Buyer patience doesn't create seller possession.",
          uiType: "mcq" },

        { concept: "Don't sell what you don't own or possess.\\nSubstance over labels: a 'pre-order' system on Instagram where the seller takes payment, then buys from a supplier, is still selling before owning -- regardless of what it's called.\\n\\nThe label 'pre-order' doesn't create a salam structure. Salam has strict requirements (full prepayment, detailed specs, fixed delivery).",
          question: "A sneaker reseller takes orders on Instagram and only buys from Nike once customers have paid. She never holds inventory. She calls this 'pre-ordering.' Core defect?",
          type: "multiple-choice", options: ["No defect -- pre-ordering is a standard modern practice", "Selling without ownership or possession at time of sale", "Gharar only -- the sneakers might not arrive", "Only a delivery risk that insurance can cover"], correct: 1,
          explanation: "Completing a sale before owning or possessing the item is a structural defect. The label 'pre-order' doesn't create a valid salam structure. Pre-orders CAN be structured validly (e.g. salam with proper terms), but an Instagram sale with no ownership, no formal specs, and no salam structure doesn't qualify.",
          uiType: "spot" },

        // --- ZONE 3: STRETCH (Q8-10) ---
        { concept: "Don't sell what you don't own or possess.\\nEdge case: a tech wholesaler buys 1,000 tablets. Paid in full, holds commercial invoice and title, insurance in her name. Tablets are in the supplier's bonded warehouse awaiting customs clearance.\\n\\nThe question: is customs clearance a possession issue, or just an administrative step?",
          question: "A tech wholesaler buys 1,000 tablets. She has paid in full, holds title, and insurance is in her name. The tablets are in the supplier's bonded warehouse awaiting customs clearance. Can she resell some now?",
          type: "multiple-choice", options: ["Never -- must physically hold every unit and clear customs first", "Generally yes -- constructive possession (control, title, risk transferred) suffices even before customs clearance", "Only if the buyer visits the warehouse personally", "Only after customs clearance is complete"], correct: 1,
          explanation: "Constructive possession: legal control, title, full payment, and risk are all with the wholesaler. She can generally resell even before physical pickup. Customs clearance is an administrative step, not a possession question. What matters is who controls and bears the risk.",
          uiType: "mcq" },

        { concept: "Cross-reference Module 1: salam requires full prepayment, specified goods, fixed delivery date and location.\\nOwnership before sale is the rule. Salam is the structured EXCEPTION, not a loophole.\\n\\nThe difference between a valid salam and 'selling before owning' is the strictness of the structure.",
          question: "What is the key difference between a prohibited 'sell before you own' arrangement and a valid salam contract?",
          type: "multiple-choice", options: ["There is no difference -- both involve selling goods you don't have yet", "Salam has strict structural safeguards (full prepayment, detailed specs, fixed delivery) that remove the gharar; casual pre-selling has none of these", "Salam is only for food commodities, not manufactured goods", "The difference is just the label -- substance is the same"], correct: 1,
          explanation: "Salam exists precisely to allow future delivery -- but with strict guardrails that remove gharar: full prepayment, detailed specifications, and a fixed delivery date and place. Without these safeguards, selling before owning is prohibited because the buyer's risk is unmanaged.",
          uiType: "compare" },

        { concept: "Adviser question: your friend has just started a reselling business. He buys from wholesale sites and ships directly to customers without ever touching the products.\\nHow do you explain the problem and the fix?",
          question: "Your friend runs a dropshipping business. He buys from AliExpress when a customer orders on his Shopify store. He never touches the products. He asks: 'Is there an Islamic issue with this?' Best advice?",
          type: "multiple-choice", options: ["No issue -- dropshipping is just modern commerce and Islam adapts to new business models", "Yes -- you're selling before owning. Fix: either hold inventory, use a formal agency (wakala) arrangement where you're an agent not a seller, or structure it as salam with proper specs and prepayment", "Just relabel it as 'procurement service' and the problem disappears", "Only a problem if the customer complains about delivery delays"], correct: 1,
          explanation: "The structural issue is real: selling before owning. But there ARE fixes. Hold inventory (simplest). Or use a wakala (agency) structure where you're clearly an agent facilitating a purchase, not a seller. Or structure as salam with full specs. The fix isn't a label change -- it's a structural change.",
          uiType: "advise" }
      ]
    },

    // ═══════════════════════════════════════════════════════
    // LESSON 3 — Risk Before Profit (al-ghurm bil-ghunm)
    // ═══════════════════════════════════════════════════════
    { id: 'lesson-2-3', title: "Risk Before Profit", description: "No risk carried = no legitimate return", duration: "12 min",
      questions: [
        // --- ZONE 1: WARM-UP (Q1-3) ---
        { concept: "al-ghurm bil-ghunm / al-kharaj bil-daman: entitlement to gain follows exposure to loss.\\nNo risk carried = no legitimate return. If your 'profit' comes without any skin in the game, it looks like riba.\\n\\nThis principle is the backbone of Islamic commercial law. It shows up in every contract.",
          question: "Complete the principle: 'Entitlement to benefit follows ______.'",
          type: "multiple-choice", options: ["Seniority in the industry", "Liability (exposure to loss)", "Popularity of the product", "Duration of the investment"], correct: 1,
          explanation: "al-ghurm bil-ghunm: whoever carries the risk of loss earns the right to profit. Without liability, a 'return' resembles riba. Seniority, popularity, and duration don't generate entitlement by themselves -- risk does.",
          uiType: "fill" },

        { concept: "In ijarah (lease): the owner/lessor bears ownership risks and major maintenance. The lessee bears operating/usage costs and misuse liability.\\nIn a sale: risk passes to the buyer on delivery/acceptance.\\n\\nThink of leasing a car: if the transmission fails from normal wear, the lessor pays. If you crash it, you pay.",
          question: "In an ijarah (lease), who bears the cost of major maintenance from normal wear and tear?",
          type: "multiple-choice", options: ["The lessee -- they're the one using the asset daily", "The lessor (owner) -- major wear is an ownership risk", "Split 50/50 by default in Islamic leases", "Whoever has the higher income at the time"], correct: 1,
          explanation: "In ijarah, the lessor owns the asset and bears ownership-level risks, including major maintenance from normal wear. The lessee covers misuse damage and day-to-day running costs. Income levels are irrelevant -- the ownership structure determines liability.",
          uiType: "mcq" },

        { concept: "Risk -> return is not just a slogan. It's a diagnostic tool.\\nAsk: 'Who carries the risk of loss right now?' The answer tells you who has a legitimate claim to profit.\\n\\nIf nobody bears risk but someone earns a return, that return has no Islamic basis.",
          question: "Select the TWO statements that correctly reflect the risk-return principle.",
          type: "multi-select", options: ["A return without bearing any liability is perfectly acceptable in Islamic finance", "Profit belongs to the party bearing real liability for the asset", "A lessor earns rent because they own the asset and carry its structural risks", "The buyer always bears all risks, even before delivery"], correct: [1, 2],
          explanation: "Profit follows the party with liability. Rent follows the party with ownership risk. A return without liability is exactly what Islamic finance prevents. And the buyer doesn't bear pre-delivery risk unless the contract specifically assigns it.",
          uiType: "sel2" },

        // --- ZONE 2: BUILD (Q4-7) ---
        { concept: "In ijarah: lessor bears ownership costs (structural repairs, major wear, manufacturer servicing). Lessee bears usage costs (consumables, misuse damage, day-to-day running).\\n\\nThe split is based on ownership vs usage, not on who has the asset physically.",
          question: "You lease office equipment. This year's costs: (1) Compressor replacement from normal wear: AED 4,200. (2) Broken handle -- your employee dropped it: AED 350. (3) Annual manufacturer servicing: AED 1,100. (4) Toner and paper: AED 600. What is the LESSOR's total vs YOURS?",
          type: "multiple-choice", options: ["Lessor: AED 5,300 (compressor + servicing) | You: AED 950 (broken handle + consumables)", "Lessor: AED 4,200 | You: AED 2,050", "Everything is 50/50 = AED 3,125 each", "You pay everything -- it's in your office"], correct: 0,
          explanation: "Lessor bears ownership-level costs: compressor from normal wear (AED 4,200) + manufacturer servicing (AED 1,100) = AED 5,300. You bear misuse damage (dropped handle: AED 350) + consumables (toner/paper: AED 600) = AED 950. 'It's in your office' doesn't make everything your cost.",
          uiType: "calc", visual: { calcSteps: ["Lessor costs: AED [___] (compressor) + AED [___] (servicing) = AED [___]", "Your costs: AED [___] (broken handle) + AED [___] (consumables) = AED [___]"], factChips: ["Compressor (normal wear): AED 4,200", "Broken handle (employee): AED 350", "Annual servicing: AED 1,100", "Toner & paper: AED 600"] } },

        { concept: "In a sale: risk passes to the buyer on delivery/acceptance as per contract.\\nOnce you've received and accepted the item, damage or loss is on you.\\n\\nClicking 'buy' initiates the contract but doesn't transfer physical risk. The trigger is delivery + acceptance.",
          question: "You buy a washing machine online. The store dispatches it, and the delivery driver hands it to you at your door. You sign for it. At what point does risk of damage transfer to you?",
          type: "multiple-choice", options: ["When you first clicked 'buy' on the website", "On delivery and your acceptance as per contract", "Only after the first instalment payment clears", "Never -- the store always bears the risk for items it sold"], correct: 1,
          explanation: "Risk typically transfers on delivery and acceptance as defined in the contract. Clicking 'buy' initiates the contract but doesn't transfer physical risk. Payment timing doesn't itself move risk. The trigger is delivery + acceptance.",
          uiType: "mcq" },

        { concept: "al-ghurm bil-ghunm applies to investment too.\\nA 'guaranteed return' on an investment where the investor bears no risk = riba territory.\\n\\nIf your capital is guaranteed AND you earn a fixed return, who is actually bearing the risk? The other party -- and your 'profit' is really interest.",
          question: "An investment platform offers: 'Invest AED 50,000. Guaranteed 8% annual return. Principal fully protected.' How does the risk-return principle apply?",
          type: "multiple-choice", options: ["Compliant -- the platform is just generous with returns", "Non-compliant -- guaranteed return + protected principal means the investor bears zero risk, making the 'profit' structurally equivalent to riba", "Compliant if the platform labels it as 'profit sharing'", "Compliant as long as the underlying assets are halal"], correct: 1,
          explanation: "If your principal is guaranteed and your return is fixed, you bear zero risk. The 'profit' has no Islamic basis because it doesn't follow from liability. Labels like 'profit sharing' don't fix substance. Even halal underlying assets can't cure a riba structure.",
          uiType: "spot" },

        { concept: "The risk-return principle connects to Module 1: riba is a guaranteed surplus on money without risk.\\nA deposit that guarantees 4% return = riba. An equity investment where you share profits AND losses = legitimate.\\n\\nThe distinguishing factor is always: does the investor share in the downside?",
          question: "Two investments: (A) AED 100,000 in a mudarabah fund -- you get 70% of profits but could lose your capital. (B) AED 100,000 in a 'profit account' -- guaranteed 5% return, principal protected. Which follows risk-return principles?",
          type: "multiple-choice", options: ["Both are fine -- they both generate returns", "Only A -- the investor shares in both upside AND downside", "Only B -- it's safer and safety is a priority in Islam", "Neither -- all investments carry some form of riba"], correct: 1,
          explanation: "Investment A follows al-ghurm bil-ghunm: the investor can profit but also bears real loss risk. Investment B gives a guaranteed return with no downside -- that's structurally equivalent to interest on a deposit. Safety isn't the test; risk-sharing is.",
          uiType: "compare" },

        // --- ZONE 3: STRETCH (Q8-10) ---
        { concept: "Edge case: in some ijarah contracts, the lessee is made responsible for ALL maintenance -- including major structural repairs.\\nThis shifts ownership risk to the lessee while the lessor keeps the title. Is this consistent with ijarah principles?",
          question: "An Islamic bank's car lease (ijarah) contract states: 'The lessee is responsible for ALL maintenance, repairs, and insurance -- including engine and transmission failure.' Is this clause consistent with ijarah?",
          type: "multiple-choice", options: ["Yes -- the lessee is using the car, so they should cover everything", "No -- dumping ALL risk on the lessee while retaining ownership undermines the ijarah structure; the lessor must bear ownership-level risks", "Yes, as long as the rent is reduced to compensate", "Only problematic if the car is new"], correct: 1,
          explanation: "Ijarah splits risk by ownership vs usage. If ALL risk falls on the lessee but the lessor retains title and earns rent, the lessor is earning without bearing any liability -- violating al-ghurm bil-ghunm. Reduced rent doesn't fix a structural misallocation of risk.",
          uiType: "spot" },

        { concept: "Cross-reference: Module 1 Lesson 6 -- governance and screening. The risk-return principle also applies to Shariah-compliant fund structures.\\n\\nA fund manager who earns a fee regardless of performance bears no risk. A fund manager who shares in losses has skin in the game.",
          question: "A Shariah-compliant fund charges a 2% management fee annually regardless of performance, plus 20% of any profits. The manager bears no losses if the fund declines. Does this fee structure align with Islamic risk-return principles?",
          type: "multiple-choice", options: ["Fully aligned -- management fees are standard in Islamic finance", "The fixed fee is acceptable for management services, but the profit share without loss-sharing weakens the alignment -- ideally the manager should share in downside too", "Completely non-compliant -- all fees must be performance-based", "Aligned only if the fund invests in halal assets"], correct: 1,
          explanation: "A fixed fee for genuine management services can be justified as a service charge (ujrah). But a profit share (20% of upside) without any loss-sharing means the manager captures gains without risk. The ideal is skin in the game on both sides. Halal assets are necessary but don't fix the fee structure.",
          uiType: "mcq" },

        { concept: "Adviser question: your uncle wants to invest his retirement savings. He's been offered two options by his bank.\\nApply the risk-return principle to help him choose wisely.",
          question: "Your uncle (retiring next year) asks for advice on two bank offers: (A) 'Guaranteed Savings Account' -- 4.5% fixed return, capital protected. (B) 'Mudarabah Investment' -- projected 6-9% but capital at risk, profit/loss shared 70/30. Best advice?",
          type: "multiple-choice", options: ["Option A -- guaranteed returns are always better for retirees and Islam prioritises safety", "Explain that Option A is structurally interest (guaranteed return, no risk). Option B follows Islamic principles (shared risk). BUT -- given his age and retirement needs, suggest he explore low-risk Shariah-compliant alternatives (e.g. ijarah income funds) that balance compliance with capital preservation", "Option B only -- the higher return makes it the obvious Islamic choice", "Both are equally compliant -- just pick whichever pays more"], correct: 1,
          explanation: "The adviser skill: diagnose the structure (A is riba, B is legitimate) AND consider the person's circumstances. For a retiree, high-risk mudarabah may not be appropriate even though it's Shariah-compliant. The best advice points to compliant AND suitable alternatives.",
          uiType: "advise" }
      ]
    },

    // ═══════════════════════════════════════════════════════
    // LESSON 4 — Ribawi vs Non-Ribawi Exchanges
    // ═══════════════════════════════════════════════════════
    { id: 'lesson-2-4', title: "Ribawi vs Non-Ribawi Exchanges", description: "Know what's in the matrix and what's not", duration: "12 min",
      questions: [
        // --- ZONE 1: WARM-UP (Q1-3) ---
        { concept: "Ribawi goods (classical): gold, silver, dates, wheat, barley, salt. Currencies are treated like gold/silver.\\nSame-kind ribawi: must be EQUAL and IMMEDIATE. (gold-for-gold = equal weight, on the spot.)\\nDifferent-kind ribawi (same category): must be IMMEDIATE, but equality is not required. (gold-for-silver = spot, negotiated ratio OK.)\\n\\nNon-ribawi goods (cars, phones, clothes): don't carry the ribawi equality/spot rules, but still need a valid sale.",
          question: "Which of the following are NON-ribawi goods where the special equality/spot rules do NOT apply?",
          type: "multi-select", options: ["A used Tesla", "A designer handbag", "Gold bars", "UAE dirhams"], correct: [0, 1],
          explanation: "Cars and handbags are non-ribawi. The special equality and spot requirements don't apply. You still need a valid sale (known price, specified item, deliverability), but not the ribawi matrix rules. Gold bars and currencies (AED, USD) ARE ribawi.",
          uiType: "sel2" },

        { concept: "Same-kind ribawi: must be EQUAL and IMMEDIATE.\\nA 3g excess in a gold-for-gold swap = riba al-fadl, regardless of whether both parties are happy with the deal.\\n\\n'Close enough' doesn't exist in ribawi exchanges.",
          question: "Two jewellers swap 18k gold: one gives 50g, the other gives 47g. Both hand over on the spot. Verdict?",
          type: "multiple-choice", options: ["Compliant -- the amounts are close enough and both delivered on the spot", "Riba al-fadl -- same-kind ribawi exchanged at unequal weight, even though delivery was immediate", "Riba al-nasi'ah -- this is a timing defect", "Maysir -- the unequal swap is like gambling"], correct: 1,
          explanation: "Same-kind ribawi (gold for gold, same karat) must be equal in weight AND immediate. A 3g excess = riba al-fadl. 'Close enough' doesn't exist. There's no timing defect here (both on the spot), so it's not nasi'ah. And it's not chance-based, so not maysir.",
          uiType: "mcq" },

        { concept: "Different-kind ribawi: must be IMMEDIATE but equality is NOT required.\\nGold-for-silver, AED-for-USD: you can negotiate the ratio, but both sides must deliver on the spot.\\n\\nThink of a bureau de change: AED cash for EUR cash, both handed over at the counter = valid sarf.",
          question: "At a gold souk, you swap a 24k gold coin for a silver bar. You negotiate a ratio both sides accept. Both items handed over on the spot. Compliant?",
          type: "multiple-choice", options: ["Yes -- different-kind ribawi requires spot delivery, not equal weight", "No -- all precious metal swaps require equal weight", "Only compliant if a third party certifies the purity", "Only compliant if both items are investment-grade"], correct: 0,
          explanation: "Gold and silver are different ribawi categories. The rule: must be immediate (spot), but equality is not required. A negotiated ratio is fine as long as both sides hand over in the same sitting. Don't over-apply the equality rule -- it's for same-kind only.",
          uiType: "mcq" },

        // --- ZONE 2: BUILD (Q4-7) ---
        { concept: "Currency exchange (sarf): currencies are ribawi (treated like gold/silver).\\nAED-for-USD: different-kind ribawi = spot required, equality not required.\\n\\n10,000 AED at 3.67 AED/USD = USD 2,724.80. Both currencies delivered at the counter = valid sarf.",
          question: "You convert AED 10,000 to USD at a bureau de change. Rate: 3.67 AED/USD. You hand over AED 10,000 cash. The bureau gives you USD 2,724.80 on the spot. Is this exchange valid, and is the amount correct?",
          type: "multiple-choice", options: ["Valid and correct: 10,000 / 3.67 = approx. USD 2,724.80, both delivered on the spot", "Invalid -- the amounts aren't equal so it's riba al-fadl", "Valid only if you come back tomorrow for the USD", "Invalid -- all currency exchange is prohibited in Islam"], correct: 0,
          explanation: "AED and USD are different currencies (different-kind ribawi). Rule: must be immediate, equality not required. 10,000 / 3.67 = approx. USD 2,724.80 -- correct. Both delivered on the spot = valid sarf. Equality isn't required for different-kind. Coming back tomorrow would create nasi'ah.",
          uiType: "calc", visual: { calcSteps: ["AED [___] / Rate [___] = USD [___]", "Both delivered: [spot/deferred]?", "Same-kind or different-kind ribawi?"], factChips: ["AED 10,000 cash", "Rate: 3.67 AED/USD", "Both currencies: counter delivery"] } },

        { concept: "Same-kind ribawi: EQUAL and IMMEDIATE. Break either = riba.\\nA 100g vs 103g gold swap on the spot = 3g excess = riba al-fadl.\\n\\nThe size of the excess is irrelevant -- 3g or 0.3g, it's still fadl.",
          question: "Two traders swap 24k gold: Trader A gives 100g, Trader B gives 103g. Both hand over on the spot. Calculate the excess and classify the defect.",
          type: "multiple-choice", options: ["Excess: 3g. Riba al-fadl (same-kind, unequal spot exchange)", "Excess: 3g. Compliant because the amounts are close and delivery is immediate", "No excess -- different pieces of jewellery aren't 'same-kind'", "Excess: 3g. Riba al-nasi'ah (timing defect)"], correct: 0,
          explanation: "Same-kind ribawi (gold for gold, same karat): must be equal AND immediate. 100g vs 103g = 3g excess on the spot. That's riba al-fadl. 'Close enough' doesn't exist. It's not nasi'ah (both delivered now). Different pieces are still same-kind if same metal and karat.",
          uiType: "calc", visual: { calcSteps: ["Excess = [___]g - [___]g = [___]g", "Defect type: [fadl/nasi'ah/none]"], factChips: ["Trader A: 100g 24k gold", "Trader B: 103g 24k gold", "Both: spot delivery"] } },

        { concept: "The ribawi matrix is a diagnostic tool. Step 1: Are these ribawi goods? Step 2: Same-kind or different-kind? Step 3: Apply the rules.\\n\\nNon-ribawi exchanges (car for cash, phone for furniture) don't carry the special equality/spot rules -- but still need a valid sale.",
          question: "You trade your used iPhone (worth AED 2,000) for your colleague's used MacBook (worth AED 3,500). Both items handed over on the spot. Any ribawi issue?",
          type: "multiple-choice", options: ["Riba al-fadl -- the values are unequal", "No ribawi issue -- phones and laptops are non-ribawi goods; the ribawi equality rules don't apply", "Riba al-nasi'ah -- electronics exchanges must be deferred", "Gharar -- you can't swap electronics directly"], correct: 1,
          explanation: "Phones and laptops are non-ribawi. The special equality and spot rules don't apply. The unequal value is simply a negotiated barter -- perfectly fine for non-ribawi goods. You still need a valid sale (both agree, items specified), but not the ribawi matrix rules.",
          uiType: "mcq" },

        { concept: "Currency exchange (sarf) must be spot on both sides.\\nFixing the rate doesn't cure a delayed handover.\\n\\nA remittance app that locks today's rate but credits GBP in 3 business days has a timing defect: the handover itself must happen now.",
          question: "Currency exchange (sarf) must be ______ on both sides to be Sharia-compliant.",
          type: "multiple-choice", options: ["Collateralised with a third-party guarantee", "Spot / immediate on both sides", "Notarised by a Shariah board", "Equal in nominal value"], correct: 1,
          explanation: "In sarf, both currencies must be delivered on the spot. Any deferral on either side = riba al-nasi'ah. A fixed rate, collateral, or notarisation don't fix the timing requirement. The handover itself must happen now.",
          uiType: "fill" },

        // --- ZONE 3: STRETCH (Q8-10) ---
        { concept: "Edge case: a remittance app locks today's rate but one side is delivered today and the other in 3 business days.\\nSame-day settlement has stronger scholarly support than multi-day delays.\\n\\nClassical sarf = same sitting. Modern scholars discuss near-instantaneous electronic settlement.",
          question: "Two remittance options for sending GBP to your family. Option A: GBP credited in 2 hours (same business day). Option B: GBP credited in 3 business days. Both lock today's rate. Which better satisfies sarf requirements?",
          type: "multiple-choice", options: ["Both fine -- the rate is locked in both cases", "Option A -- near-immediate settlement has stronger scholarly support; Option B's 3-day delay is a clear deferral", "Option B -- locking the rate matters more than delivery speed", "Neither -- only physical cash exchange at a counter counts"], correct: 1,
          explanation: "Classical sarf = same sitting. Modern scholars discuss near-instantaneous electronic settlement as potentially satisfying this. 2 hours has stronger support than 3 days. Rate locking is not the same as delivery timing.",
          uiType: "compare" },

        { concept: "Cross-reference Module 1: the 'GoldRush' app scenario. Guaranteed return + no spot delivery + vague terms = layer cake of defects.\\nThe ribawi matrix helps you systematically classify the defect type.\\n\\nReal products often have MULTIPLE overlapping defects across the ribawi and non-ribawi rules.",
          question: "A new app offers: 'Deposit AED 5,000. We invest in gold on your behalf. Guaranteed 4% monthly return. Withdraw anytime.' Classify using the ribawi matrix.",
          type: "multiple-choice", options: ["Compliant -- gold is an Islamic asset and the return sounds reasonable", "Multiple defects: (1) Guaranteed return on gold = riba, (2) No spot delivery of gold to investor = potential nasi'ah, (3) 'We invest on your behalf' with no risk-sharing = not a valid mudarabah", "Only a gharar issue due to vague terms", "Compliant if the app has Shariah certification"], correct: 1,
          explanation: "Layer cake: guaranteed return (riba), no spot gold delivery (nasi'ah risk), 'investing on your behalf' with guaranteed outcome isn't mudarabah (no risk-sharing). Gold being halal as an asset doesn't cure structural defects. Certification doesn't fix substance.",
          uiType: "spot" },

        { concept: "Adviser question: your friend is starting a jewellery business and asks about the rules for exchanging gold with suppliers.\\nCan you explain the ribawi rules in practical terms?",
          question: "Your friend is opening a gold jewellery shop. She asks: 'Can I swap old gold pieces from customers for new ones from my stock?' What rules should she follow?",
          type: "multiple-choice", options: ["Swap freely -- it's her business and gold is halal", "Same-karat gold: must be equal weight and immediate. Different-karat gold: scholars differ (some treat as same-kind requiring equality, others allow exchange with a price adjustment). Safest: sell the old gold for cash, then use cash to buy new pieces (two separate transactions)", "Only swap if the customer pays extra in cash for any weight difference", "Gold-for-gold swaps are always prohibited in modern commerce"], correct: 1,
          explanation: "Same-kind ribawi (same karat gold) requires equal weight + spot. Different-karat gold has scholarly discussion. The safest practical route: two transactions -- sell old for cash, buy new with cash. This avoids the ribawi exchange entirely while serving the customer.",
          uiType: "advise" }
      ]
    },

    // ═══════════════════════════════════════════════════════
    // LESSON 5 — Price, Time & Credit Sales
    // ═══════════════════════════════════════════════════════
    { id: 'lesson-2-5', title: "Price, Time & Credit Sales", description: "Deferred payment is not interest", duration: "12 min",
      questions: [
        // --- ZONE 1: WARM-UP (Q1-3) ---
        { concept: "It's permissible to sell today at a higher fixed price payable later (deferred/credit sale), as long as the total price is fixed at contract.\\nA higher credit price is compensation for deferred payment, agreed as part of the SALE -- it's NOT interest on a loan.\\n\\nThink of a furniture store: 'AED 5,000 cash or AED 5,800 on 12 months.' Pick ONE price at contract.",
          question: "True or False: Selling an item at a higher price for deferred payment is the same as charging interest on a loan.",
          type: "multiple-choice", options: ["True -- any markup for time is interest by definition", "False -- a higher credit sale price fixed at contract is compensation for deferred payment within a sale, not interest on money lent"], correct: 1,
          explanation: "A credit sale price (fixed upfront) is NOT interest on a loan. The seller owns an asset, sells it at an agreed price, and the buyer pays over time. Riba is a guaranteed surplus on MONEY lent. Here, it's a sale price negotiation for a real asset. The distinction is substance, not labelling.",
          uiType: "mcq" },

        { concept: "NOT allowed: leaving two prices open ('Cash AED 9,000 / Credit AED 10,000 -- decide later'). Pick one at contract.\\nNOT allowed: increasing the amount after default as profit. Monetising arrears = riba territory.\\n\\nThe rule: one fixed price, agreed at signing. Not two options left open.",
          question: "A furniture store offers: 'This sofa is AED 5,000 cash or AED 5,800 on 12-month instalments -- let us know which one after delivery.' You agree and the sofa is delivered. What's the issue?",
          type: "multiple-choice", options: ["No issue -- both prices are transparently disclosed", "Non-compliant: the price is not fixed at contract (two prices left open after delivery = gharar)", "Only a documentation problem that can be fixed with a receipt", "Compliant as long as the buyer eventually chooses one price"], correct: 1,
          explanation: "You must fix ONE price at the point of contract. Having two prices open until after delivery means neither party knows the actual obligation -- that's gharar. Disclosure isn't the same as agreement. Consent 'later' doesn't fix a price that was undefined at contract.",
          uiType: "spot" },

        { concept: "A deferred sale at a higher fixed price is a credit sale, not a loan.\\nThe profit is part of the sale price negotiation, not a charge on money lent.\\n\\nAn appliance store sells you a fridge for AED 3,200 total on 8 monthly instalments. Cash price would have been AED 2,900. The AED 300 difference is part of the sale price, not interest.",
          question: "An appliance store sells a fridge for AED 3,200 total, payable in 8 monthly instalments of AED 400. Cash price: AED 2,900. No loan involved. Is this compliant?",
          type: "multiple-choice", options: ["No -- the AED 300 markup is interest in disguise", "Yes -- it's a sale at a fixed deferred price, not a loan with interest", "Only compliant if the label says 'no interest' on the receipt", "Only compliant if collateral is provided"], correct: 1,
          explanation: "A deferred sale price (fixed upfront) is not interest. The AED 3,200 is the agreed sale price -- the AED 300 is part of the sale price negotiation, not a charge on money lent. The store sold an asset at a known total price, payable in instalments. That's a credit sale.",
          uiType: "mcq" },

        // --- ZONE 2: BUILD (Q4-7) ---
        { concept: "Credit sale math: Total instalment price - Cash price = Markup. Markup / Cash price x 100 = Markup percentage.\\nMonthly instalment = Total price / Number of months.\\n\\nA phone shop sells a Samsung Galaxy: Cash AED 3,400. 12-month price: AED 3,720 total (fixed at contract).",
          question: "A phone shop: Cash price AED 3,400. 12-month instalment price: AED 3,720 (fixed at contract). What is the monthly instalment and the credit sale markup?",
          type: "multiple-choice", options: ["Monthly: AED 310 | Markup: AED 320 (9.4% of cash price)", "Monthly: AED 283.33 | Markup: AED 0 (it's interest-free)", "Monthly: AED 310 | Markup: AED 320 (this is riba)", "Cannot calculate without knowing the bank's base rate"], correct: 0,
          explanation: "Monthly: AED 3,720 / 12 = AED 310. Markup: AED 3,720 - AED 3,400 = AED 320 (320 / 3,400 = 9.4%). The markup is part of the agreed sale price, not interest on a loan. Bank rates are irrelevant -- this is priced as a sale.",
          uiType: "calc", visual: { calcSteps: ["Monthly = AED [___] / 12 = AED [___]", "Markup = AED [___] - AED [___] = AED [___]", "Markup % = [___] / [___] x 100 = [___]%"], factChips: ["Cash price: AED 3,400", "Instalment price: AED 3,720", "Term: 12 months"] } },

        { concept: "Late-payment clauses should be non-profit deterrents (charity/admin cost), not income for the seller.\\nAdding extra money to the debt as profit for being late = riba territory.\\nCompounding arrears (penalty interest that accrues more charges) mimics conventional interest.\\n\\nGenuine restructuring (same amount, clearer terms) and real at-cost admin fees can be acceptable.",
          question: "A customer bought a TV on 12-month instalments and missed three payments. Select the TWO practices that are NOT allowed as profit by the seller.",
          type: "multi-select", options: ["Adding extra money to the debt as profit for being late", "Compounding arrears (charging penalty interest that itself accrues more charges)", "Restructuring with the same principal and a clearer repayment schedule", "Sending reminders and charging documented, at-cost admin fees"], correct: [0, 1],
          explanation: "Monetising time on an unpaid debt as profit = riba territory. Compounding arrears mimics conventional interest. Genuine restructuring (same amount, clearer terms) and real at-cost admin fees can be acceptable -- they're not profit on the debt itself.",
          uiType: "sel2" },

        { concept: "Substance over labels: a car dealership selling at AED 45,000 on 24 months (cash price AED 42,000) with the total fixed at contract is a credit sale.\\nThe AED 3,000 difference is part of the sale price, not interest.\\n\\nThe test: was one fixed price agreed at contract for a real asset? If yes, it's a sale. If the price floats with time, it slides toward a loan.",
          question: "A car dealership sells you a used Honda for AED 45,000, payable in 24 monthly instalments of AED 1,875. Cash price was AED 42,000. Total price was fixed at contract. Is this a loan or a sale?",
          type: "multiple-choice", options: ["Loan with AED 3,000 interest disguised as a sale price", "Sale with a fixed deferred price -- the AED 3,000 is part of the agreed sale price, not interest on money", "Compliant only if the contract explicitly says 'no interest'", "Gharar -- there are two different prices being discussed"], correct: 1,
          explanation: "The total deferred sale price (AED 45,000) was fixed at contract. The AED 3,000 from cash price is part of the sale price negotiation, not interest on a loan. Monthly: 45,000 / 24 = AED 1,875. There aren't 'two prices' open -- one price (AED 45,000) was chosen at signing.",
          uiType: "calc", visual: { calcSteps: ["Monthly = AED [___] / 24 = AED [___]", "Credit markup = AED [___] - AED [___] = AED [___]"], factChips: ["Sale price: AED 45,000", "Cash price: AED 42,000", "Term: 24 months"] } },

        { concept: "NOT allowed: leaving the price open or floating. 'Market rate at delivery' or 'we'll adjust based on how long you take' slides from sale territory into loan territory.\\n\\nIn a compliant credit sale, the final price must be FIXED at the point of contract.",
          question: "In a compliant credit sale, the final price must be ______ at the point of contract.",
          type: "multiple-choice", options: ["Floating based on market conditions at delivery", "Fixed / known and agreed by both parties", "Estimated with room for later adjustment", "Indexed to the central bank rate"], correct: 1,
          explanation: "Fixing the price at contract is what separates a deferred sale from a loan charging interest. A floating, estimated, or indexed price means the buyer's obligation changes with time -- and that slides from sale territory into loan territory.",
          uiType: "fill" },

        // --- ZONE 3: STRETCH (Q8-10) ---
        { concept: "Edge case: an electronics store says 'AED 4,500 cash or AED 5,100 on credit. We'll lock in which price after you've taken the laptop home.'\\nTwo prices open until after delivery = gharar.\\n\\nYou can offer both BEFORE the sale, but one must be chosen and agreed at contract.",
          question: "An electronics store says: 'This laptop is AED 4,500 cash or AED 5,100 on credit. We'll lock in the price after you take it home.' Verdict?",
          type: "multiple-choice", options: ["Fine -- both options are transparently communicated upfront", "Non-compliant: price not fixed at contract (two prices left open after delivery = gharar)", "Only a marketing issue that doesn't affect the sale's validity", "Compliant as long as the customer verbally agrees to one option"], correct: 1,
          explanation: "The price must be fixed at the point of sale. Two prices open until after delivery = gharar. Transparency of options does not equal a fixed contract price. You can offer both options before, but one must be chosen and agreed at contract.",
          uiType: "spot" },

        { concept: "Cross-reference: Module 1 -- riba is a guaranteed surplus on money lent. A credit sale markup is profit on a SALE.\\nThe distinction matters: riba attaches to money (loans). Credit sale markup attaches to an asset (sale).\\n\\nIf you remove the asset and just lend money at a premium, you've crossed into riba.",
          question: "What is the fundamental difference between a credit sale markup and riba?",
          type: "multiple-choice", options: ["There is no difference -- both charge more for time", "A credit sale markup is profit on the sale of a REAL ASSET at a fixed price; riba is a surplus on MONEY LENT without an underlying asset or risk", "The difference is only in the label used on the contract", "Credit sale markup becomes riba if it exceeds 10%"], correct: 1,
          explanation: "The distinction is structural, not cosmetic. Credit sale: a real asset changes hands, the price is fixed, and the markup is part of the sale negotiation. Riba: money is lent and a surplus is guaranteed on the money itself. Remove the asset and the markup becomes interest. There's no percentage threshold.",
          uiType: "compare" },

        { concept: "Adviser question: a family member is buying furniture and the store offers cash or instalment pricing.\\nCan you explain the Islamic view clearly and practically?",
          question: "Your sister is buying a bedroom set. The store offers AED 12,000 cash or AED 13,800 on 18-month instalments. She asks: 'Isn't the extra AED 1,800 just interest with a different name?' Best response?",
          type: "multiple-choice", options: ["She's right -- any extra charge for time is interest, so she should only pay cash", "Explain: 'It's not interest. The store owns the furniture and is selling it to you at an agreed price. The AED 13,800 IS the sale price for deferred payment -- it's not a loan plus interest. The key: one fixed price agreed before you take delivery. If they leave both prices open after delivery, that's the problem.'", "Tell her it doesn't matter -- just pick whichever is more convenient", "The extra charge is a grey area that scholars disagree on, so avoid it entirely"], correct: 1,
          explanation: "The best advice explains WHY it's different from interest (asset sale vs money loan), WHAT makes it compliant (one fixed price at contract), and WHAT would make it problematic (two open prices, floating amounts). Don't just classify -- equip her to evaluate.",
          uiType: "advise" }
      ]
    }
  ]
},
```

This replaces the entire Module 2 object. Make sure to keep the comma after the closing `},` and ensure the rest of the file (quran-arabic, islamic-history modules) remains unchanged.
