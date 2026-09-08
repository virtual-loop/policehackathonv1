# Chandigarh Police Hackathon 2026 (PS-3)
## Specialized Benchmark: Narcotics Surrogate Codeword Induction & Slang Governance
**Total Paired Cases:** 10 (10 Evasive Suspect Transcripts + 10 Benign Retail Controls)
**Objective:** Test AI/SLM model's capability to spot surrogate nouns in transactional contexts while eliminating False Positives on benign everyday conversations.

---

### CASE-NARCO-01: Footwear & Apparel Camouflage
- **Surrogate Codeword:** `White Canvas Shoes / Sneakers Size 5`
- **Canonical Classification:** Illicit Contraband Powder (5 grams uncut)
- **Evasion Mechanism:** Using shoe shoe-sizing metrics as gram weight indicators; delivery via dead drop.

#### 🚨 Positive Evasive Intercept (Should be Flagged):
```text
[SIGNAL FORENSIC EXTRACT: EXHIBIT CHD-PS3-01A]
Participants: Suspect_Karan (+91-9814022341), Vendor_ChdPlug (@chd_plug_official)
Location: Sector 22 / Sector 35 Chandigarh

[2026-09-04 14:15:22] Suspect_Karan: "Veere sunn, urgent requirement h weekend se pehle. Party orders pending hain."
[2026-09-04 14:15:45] Vendor_ChdPlug: "Haan bro bolo, sab fresh uncut stock h border channel se."
[2026-09-04 14:16:10] Suspect_Karan: "Mujhe 5 size ke 'White Canvas Shoes' chahiye. Purity check h na? Last time cut thoda zyada tha."
[2026-09-04 14:16:30] Vendor_ChdPlug: "100% lab grade h veere. 99.4% uncut. Size 5 ka rate ₹18,500 padega."
[2026-09-04 14:17:05] Suspect_Karan: "Theek h. Direct bank transfer me alert aa sakta h, do accounts me split karunga."
[2026-09-04 14:18:40] Vendor_ChdPlug: "Pehle ₹10,000 bhejo: 9814022341@paytm, baki ₹8,500 bhejo: chd_mule99@okaxis. Remark me likhna 'Sports shoes part payment'."
[2026-09-04 14:22:10] Suspect_Karan: "Payment done. Drop location coordinate bhej do."
[2026-09-04 14:22:45] Vendor_ChdPlug: "Drop spot: Sector 22 inner market, behind Aroma Hotel electrical junction box, magnetic tiffin box wrapped in red tape under the gravel pile. Collect within 1 hour." 
```

#### 🛡️ Benign Negative Control (Should NOT be Flagged):
```text
[WHATSAPP RETAIL STORE CHAT: CONTROL-01B]
Participants: Customer_Deepak (+91-9872112233), Store_Sales_Sec17 (+91-9814099887)
Location: Sector 17 Showroom Chandigarh

[2026-09-04 11:10:05] Customer_Deepak: "Hello, do you have Nike Pegasus or Converse White Canvas Shoes available in Size 5 for kids?"
[2026-09-04 11:12:30] Store_Sales_Sec17: "Yes sir, we have original white canvas sneakers in UK Size 5 in stock. Price is ₹2,800 after 20% seasonal discount."
[2026-09-04 11:14:10] Customer_Deepak: "Can I try them in the Sector 17 showroom this evening?"
[2026-09-04 11:15:00] Store_Sales_Sec17: "Sure sir, showroom is open until 9:00 PM. We accept UPI, debit card, or cash at billing counter." 
```

**Model Evaluation Guideline:** Model should flag Case A due to anomalous pricing (₹18,500 for size 5 shoes), split UPI accounts, and dead-drop instructions behind Aroma Hotel. Case B must NOT be flagged (legitimate retail store context).

------------------------------------------------------------

### CASE-NARCO-02: Cold Beverage Camouflage
- **Surrogate Codeword:** `Special Cold Coffee / Ice Brew Bottles`
- **Canonical Classification:** Liquid Synthetic Substance / Dissolved Contraband Vials
- **Evasion Mechanism:** Disguising 10ml liquid chemical vials as artisanal brewed cold coffee with anomalous pricing per bottle.

#### 🚨 Positive Evasive Intercept (Should be Flagged):
```text
[TELEGRAM E2EE INTERCEPT: EXHIBIT CHD-PS3-02A]
Participants: Distro_Mohali, Club_Promoter_Nikhil
Location: Sector 35 / Phase 3B2 Mohali

[2026-09-05 16:30:10] Club_Promoter_Nikhil: "Bro, Friday club night booking full h. Humein 6 bottle 'Special Cold Coffee' liquid brew chahiye emergency me."
[2026-09-05 16:31:40] Distro_Mohali: "Special brew ready h. Amber glass vials me h with sealed dropper cap. Rate ₹6,500 per bottle. 6 bottle ka ₹39,000 banega."
[2026-09-05 16:33:15] Club_Promoter_Nikhil: "Rate thoda kam karo veere, regular order lete hain aapse."
[2026-09-05 16:34:30] Distro_Mohali: "Bhai pure imported concentrate h, zero water dilution. Final ₹36,000 lock karo. UPI mat karna, bank lien ka issue chal raha h. Send 425 USDT on TRON: TJ4V87qR984b2cNmQ7yXkL99pQ12345678."
[2026-09-05 16:38:00] Club_Promoter_Nikhil: "TRC-20 transfer done. TXID: c9810a42f... Delivery point batao."
[2026-09-05 16:40:15] Distro_Mohali: "Phase 3B2 Mohali, behind main market electricity transformer, black thermo-insulated pouch placed inside garbage dumpster corner. Pick up in 20 minutes." 
```

#### 🛡️ Benign Negative Control (Should NOT be Flagged):
```text
[ZOMATO ORDER SUPPORT: CONTROL-02B]
Participants: Customer_Simran, Cafe_Manager_Sec35
Location: Sector 35 Chandigarh

[2026-09-05 15:20:00] Customer_Simran: "Hi, I placed an order for 2 bottles of Hazelnut Cold Coffee from your Sector 35 outlet. Is it packaged with ice packs?"
[2026-09-05 15:21:15] Cafe_Manager_Sec35: "Yes ma'am, our bottled cold brew is packaged in insulated paper bags with ice gel pouches. Delivery partner is on the way."
[2026-09-05 15:22:30] Customer_Simran: "Great, total was ₹380 paid via UPI. Thank you!" 
```

**Model Evaluation Guideline:** Flag 02A based on unit price disparity (₹6,500 per bottle), TRON USDT requirement, dropper bottle format, and dumpster dead drop. Dismiss 02B as routine food delivery.

------------------------------------------------------------

### CASE-NARCO-03: Stationery & Art Paper Camouflage
- **Surrogate Codeword:** `California Sunshine / Stamp Papers / Drawing Sheets`
- **Canonical Classification:** Hallucinogen Blotter Sheets (LSD 220ug)
- **Evasion Mechanism:** Using stationery terms (perforated drawing sheets, stamp paper) to describe perforated chemical blotter squares.

#### 🚨 Positive Evasive Intercept (Should be Flagged):
```text
[SESSION PROTOCOL LOG: EXHIBIT CHD-PS3-03A]
Participants: Dealer_Karan_PU (+91-9872001122), Student_Kunal (+91-9815998877)
Location: Panjab University (PU) Sector 14, Chandigarh

[2026-09-05 18:10:00] Student_Kunal: "Bhai campus fest ke liye 'California Sunshine Stamp Papers' available hain kya?"
[2026-09-05 18:11:15] Dealer_Karan_PU: "Haan fresh perforated sheets aayi hain. 220ug potency certified. Minimum order half sheet (10 stamp papers)."
[2026-09-05 18:12:40] Student_Kunal: "10 stamp papers ka price kya hoga?"
[2026-09-05 18:13:30] Dealer_Karan_PU: "Single paper ₹1,200 ka h. 10 papers loge toh ₹9,500 lagega. Saath me foil wrapping moisture-lock rahegi."
[2026-09-05 18:15:00] Student_Kunal: "Payment kaise karna h? Proctor checking chal rahi h Gate 1 pe."
[2026-09-05 18:16:20] Dealer_Karan_PU: "UPI kar do: campus_canteen@okaxis. Narration me 'Engineering drawing chart sheets' daal dena taaki koi notice na kare. Delivery Law Department garden bench #3 ke niche taped envelope me milegi shaam 8 baje." 
```

#### 🛡️ Benign Negative Control (Should NOT be Flagged):
```text
[ADVOCATE CHAMBER CHAT: CONTROL-03B]
Participants: Advocate_Singla (+91-9814011223), Client_Harpreet (+91-9876044332)
Location: District Courts Sector 43 Chandigarh

[2026-09-05 11:00:00] Client_Harpreet: "Sir, rent agreement affidavit banwane ke liye kitne ke stamp paper purchase karne honge?"
[2026-09-05 11:02:15] Advocate_Singla: "Aap Sector 43 court complex ke treasury stamp vendor se ₹100 value ka non-judicial stamp paper le aao. Drafting ready h."
[2026-09-05 11:04:00] Client_Harpreet: "Theek h sir, main 15 minute me vendor se stamp paper lekar aapke chamber #214 me aata hoon." 
```

**Model Evaluation Guideline:** Flag 03A on potency metric ('220ug'), micro-pricing (₹9,500 for 10 sheets), and deceptive campus canteen narration. Differentiate from legal non-judicial stamp papers in 03B.

------------------------------------------------------------

### CASE-NARCO-04: Powdered Beverage & Health Blend Camouflage
- **Surrogate Codeword:** `Ice Tea Powder / Organic Green Reagent`
- **Canonical Classification:** Synthetic Stimulant Crystals / 4-MMC Mephedrone
- **Evasion Mechanism:** Marketing crystalline stimulant chemical as organic dietary powder; stealth foil packaging.

#### 🚨 Positive Evasive Intercept (Should be Flagged):
```text
[TELEGRAM PRIVATE LOG: EXHIBIT CHD-PS3-04A]
Participants: Tricity_Distro, Client_Sector8
Location: Sector 8 Chandigarh / Zirakpur Barrier

[2026-09-05 20:00:10] Client_Sector8: "Bro, last time wala 'Ice Tea Powder' bohot high quality tha. Kya aur 20g packet ready h?"
[2026-09-05 20:01:45] Tricity_Distro: "Haan bro, pure white crystal form me h. Lab purity 99.2%. Marquis test verified."
[2026-09-05 20:03:00] Client_Sector8: "20g pack ka total amount kitna lagega?"
[2026-09-05 20:04:15] Tricity_Distro: "₹24,000 for 20g. Packaging triple vacuum-sealed metallic foil tea bag me hogi. Smell-proof h. Police barrier ya canine unit detect nahi karega."
[2026-09-05 20:06:00] Client_Sector8: "UPI handle share karo."
[2026-09-05 20:07:20] Tricity_Distro: "Transfer to: tea_junction_sec8@okhdfcbank. Narration strictly 'Darjeeling organic tea consignment'. Drop location: Zirakpur highway near flyover pillar #42." 
```

#### 🛡️ Benign Negative Control (Should NOT be Flagged):
```text
[ORGANIC STORE INQUIRY: CONTROL-04B]
Participants: Customer_Ritu, OrganicStore_Admin
Location: Sector 26 Chandigarh

[2026-09-05 14:00:00] Customer_Ritu: "Do you have lemon ice tea powder and detox green tea bags in 500g family pack?"
[2026-09-05 14:02:10] OrganicStore_Admin: "Yes ma'am, 500g organic lemon ice tea powder is ₹340. We can ship it to your address in Sector 26 today."
[2026-09-05 14:03:30] Customer_Ritu: "Please send, I will pay ₹340 via Google Pay on delivery." 
```

**Model Evaluation Guideline:** Flag 04A on Marquis test reference, purity percentage (99.2%), extreme price (₹24,000 for 20g), and stealth packing claims. Control 04B shows standard food retail pricing (₹340 for 500g).

------------------------------------------------------------

### CASE-NARCO-05: Confectionery & Sweets Camouflage
- **Surrogate Codeword:** `Sweet Mithai / Kaju Katli Pieces / Brownie Cubes`
- **Canonical Classification:** Compressed Synthetic Tablets / MDMA Ecstasy Press
- **Evasion Mechanism:** Referring to stamped synthetic party pills as traditional sweets or gourmet confectionery by piece count.

#### 🚨 Positive Evasive Intercept (Should be Flagged):
```text
[SIGNAL CHAT EXTRACT: EXHIBIT CHD-PS3-05A]
Participants: Club_Runner_Sunny (+91-9872334455), Dealer_Tricity (+91-9814022341)
Location: Sector 26 Club Strip, Madhya Marg Chandigarh

[2026-09-05 22:15:00] Club_Runner_Sunny: "Bhai midnight crowd ke liye 25 pieces 'Sweet Mithai' (Green Tesla press) chahiye. Stock h?"
[2026-09-05 22:16:30] Dealer_Tricity: "Haan fresh Dutch press 'mithai' available h. High strength 240mg per piece. Rate ₹1,400 per piece."
[2026-09-05 22:18:00] Club_Runner_Sunny: "25 piece ka ₹35,000 banega. Cash le lo club ke bahar."
[2026-09-05 22:19:15] Dealer_Tricity: "Club ke bahar PCR van khadi h, cash handover bilkul nahi. Seedha mule handle pe bhejo: deepak_tricity@paytm. Remark: 'Sweet mithai box 2 qty'."
[2026-09-05 22:22:00] Club_Runner_Sunny: "Sent ₹35,000. UTR: 991204819201. Maal kahan se uthaoon?"
[2026-09-05 22:24:00] Dealer_Tricity: "Sector 26 club back-alley exit, behind generator exhaust duct, black magnetic pouch stuck to the metal grill." 
```

#### 🛡️ Benign Negative Control (Should NOT be Flagged):
```text
[SWEET SHOP CATERING ORDER: CONTROL-05B]
Participants: Customer_Anil (+91-9815044991), Sindhi_Sweets_Counter (+91-9872011992)
Location: Sector 22 Chandigarh

[2026-09-05 17:00:00] Customer_Anil: "Bhaiya, family function ke liye 2 kg Kaju Katli mithai pack karwana h. Fresh h na?"
[2026-09-05 17:01:30] Sindhi_Sweets_Counter: "Haanji sir, bilkul fresh pure desi ghee batch h. ₹1,100 per kg rate h, total ₹2,200."
[2026-09-05 17:03:00] Customer_Anil: "Theek h, main 7 baje Sector 22 shop se collect kar loonga aur counter pe pay kar doonga." 
```

**Model Evaluation Guideline:** Flag 05A on 'Green Tesla press', 240mg strength metric, piece-rate pricing (₹1,400/piece), and back-alley generator drop. Control 05B represents regular kilogram-based sweet purchases.

------------------------------------------------------------

### CASE-NARCO-06: Automotive & Industrial Chemical Camouflage
- **Surrogate Codeword:** `Synthetic Brake Fluid / 50ml Lubricant Vial`
- **Canonical Classification:** Liquid Depressant / Dissolved Concentrates
- **Evasion Mechanism:** Disguising concentrated chemical liquid as specialty automotive additives sold in miniature volumes.

#### 🚨 Positive Evasive Intercept (Should be Flagged):
```text
[TELEGRAM E2EE INTERCEPT: EXHIBIT CHD-PS3-06A]
Participants: Mech_Mod_Vicky, Source_Ambala
Location: Sector 28 Motor Market Chandigarh

[2026-09-06 11:00:10] Mech_Mod_Vicky: "Ambala se shipment aayi kya? Mujhe 3 vials 'Synthetic Brake Fluid' (50ml pure concentration) chahiye."
[2026-09-06 11:01:45] Source_Ambala: "Haan delivery bus se dispatch ho chuki h. Clear pharmaceutical solution h, uncolored and odorless. Rate ₹8,000 per 50ml vial."
[2026-09-06 11:03:20] Mech_Mod_Vicky: "Total ₹24,000 ban gaya. Remark me kya likhna h?"
[2026-09-06 11:04:40] Source_Ambala: "UPI handle: ambala_spares@ybl. Narration likhna 'Car hydraulic fluid spare'. Bus conductor ko phone mat karna, Sector 43 Bus Stand parcel counter pe receipt code 'AMB-882' dikha ke parcel lena." 
```

#### 🛡️ Benign Negative Control (Should NOT be Flagged):
```text
[AUTO SPARE PARTS ORDER: CONTROL-06B]
Participants: Mechanic_Suresh, AutoStore_Manager
Location: Sector 28 Motor Market Chandigarh

[2026-09-06 10:15:00] Mechanic_Suresh: "Bhaiya, Honda City car servicing ke liye Castrol DOT 4 Brake Fluid ki 500ml bottle bhej do."
[2026-09-06 10:16:30] AutoStore_Manager: "Castrol DOT 4 500ml pack ₹320 ka h. Chhotu ko bhej raha hoon shop pe deliver karne." 
```

**Model Evaluation Guideline:** Flag 06A on micro-volume pricing (₹8,000 for 50ml), odorless/colorless attributes, and parcel counter drop codes. Differentiate from standard automotive supplies in 06B.

------------------------------------------------------------

### CASE-NARCO-07: Agricultural & Garden Nutrient Camouflage
- **Surrogate Codeword:** `Plant Food / Organic Soil Booster Crystals`
- **Canonical Classification:** Crystalline Synthetic Reagent / Research Chemical
- **Evasion Mechanism:** Selling recreational synthetic crystals under the guise of specialized hydroponic plant nutrients.

#### 🚨 Positive Evasive Intercept (Should be Flagged):
```text
[WHATSAPP ENCRYPTED CHAT: EXHIBIT CHD-PS3-07A]
Participants: Grower_Alex (+91-9872990011), Supplier_Kalka (+91-9814044556)
Location: Zirakpur / Panchkula Sector 20

[2026-09-06 13:20:00] Grower_Alex: "Bro, hydroponic setup ke liye 15g 'Soil Booster Crystals' chahiye. Fresh purity h na?"
[2026-09-06 13:21:30] Supplier_Kalka: "Bilkul uncut white crystals hain. Purity 99%. 15g ka rate ₹18,000 h. Zirakpur highway nursery ke pass dead drop milega."
[2026-09-06 13:23:00] Grower_Alex: "Payment: ₹18,000 sent to kalka_nursery@okaxis with remark 'Garden fertilizer pack'. Coordinate bhejo."
[2026-09-06 13:24:45] Supplier_Kalka: "Drop coordinate: Behind highway nursery boundary wall, blue plastic canister buried under loose sand near electricity pole #18." 
```

#### 🛡️ Benign Negative Control (Should NOT be Flagged):
```text
[NURSERY ORDER CHAT: CONTROL-07B]
Participants: Home_Gardener_Pooja, GreenNursery_Panchkula
Location: Panchkula Sector 5

[2026-09-06 12:00:00] Home_Gardener_Pooja: "Do you have 5kg organic vermicompost and plant food fertilizer packets for rose plants?"
[2026-09-06 12:01:30] GreenNursery_Panchkula: "Yes ma'am, 5kg vermicompost bag is ₹150 and organic plant food pack is ₹120. Total ₹270." 
```

**Model Evaluation Guideline:** Flag 07A due to gram-level metric (15g), exorbitant rate (₹18,000 for 15g), and buried canister dead drop. Control 07B shows normal agricultural weights (5kg for ₹150).

------------------------------------------------------------

### CASE-NARCO-08: Hardware & Construction Material Camouflage
- **Surrogate Codeword:** `White Cement / Ultra-Fine Gypsum Powder`
- **Canonical Classification:** Opiate / Illicit Substance Uncut
- **Evasion Mechanism:** Using bulk construction masonry names to disguise gram-weight retail packets.

#### 🚨 Positive Evasive Intercept (Should be Flagged):
```text
[SIGNAL SECURE LOG: EXHIBIT CHD-PS3-08A]
Participants: Contractor_Ravi (+91-9872115544), Dispatcher_D (+91-9814033221)
Location: Industrial Area Phase 1 Chandigarh

[2026-09-06 15:00:10] Contractor_Ravi: "Bhai project site ke liye 10g 'Ultra-Fine White Cement' urgently deliver karwa do."
[2026-09-06 15:01:40] Dispatcher_D: "Grade-1 Afghan import h. Rate ₹38,000 for 10g packet. Heat-sealed zip pouch me pack h."
[2026-09-06 15:03:00] Contractor_Ravi: "Transfer done to: hardware_ind1@paytm with remark 'Sanitary tile grout'. Where is pickup?"
[2026-09-06 15:04:30] Dispatcher_D: "Industrial Area Phase 1, behind railway culvert siding, taped inside concrete hollow block." 
```

#### 🛡️ Benign Negative Control (Should NOT be Flagged):
```text
[BUILDING MATERIAL INQUIRY: CONTROL-08B]
Participants: HomeOwner_Manoj, BuildingSupply_IndArea
Location: Industrial Area Phase 2 Chandigarh

[2026-09-06 14:10:00] HomeOwner_Manoj: "What is the price of a 50kg bag of Birla White Cement for wall putty?"
[2026-09-06 14:11:30] BuildingSupply_IndArea: "Sir, Birla White Cement 50kg bag is ₹1,150. Delivery tempo charge to Sector 44 is ₹200 extra." 
```

**Model Evaluation Guideline:** Flag 08A on 10g metric for 'cement', extreme cost (₹38,000 for 10g), and culvert dead drop. Control 08B represents legitimate construction material sales in 50kg sacks.

------------------------------------------------------------

### CASE-NARCO-09: Electronics & Charger Camouflage
- **Surrogate Codeword:** `65W Fast Charger / High-Watt Adapter`
- **Canonical Classification:** Concealed Parcel with Hollowed Hardware Stash
- **Evasion Mechanism:** Hollowing out electronic power supplies to conceal illicit contraband during courier handoff.

#### 🚨 Positive Evasive Intercept (Should be Flagged):
```text
[TELEGRAM PRIVATE CHAT: EXHIBIT CHD-PS3-09A]
Participants: Tech_Seller_Aman, Courier_Runner_Harry
Location: Sector 22 Mobile Market / Sector 17 Plaza

[2026-09-06 17:30:00] Tech_Seller_Aman: "Harry, parcel ready h. Outer shell 65W fast charger ki h, lekin inside plastic casing hollow karke 15g uncut maal pack kiya hua h. Screws glued with epoxy."
[2026-09-06 17:31:30] Courier_Runner_Harry: "Weight balance theek h na? Courier company weigh scale pe shak toh nahi karegi?"
[2026-09-06 17:33:00] Tech_Seller_Aman: "Lead counterweight add kiya h, exact 140 grams standard weight h. Payment ₹22,000 received via crypto. Parcel Sector 17 post office drop box me dalna h." 
```

#### 🛡️ Benign Negative Control (Should NOT be Flagged):
```text
[MOBILE ACCESSORY SHOP CHAT: CONTROL-09B]
Participants: Customer_Kunal, MobileShop_Sec22
Location: Sector 22 Mobile Market Chandigarh

[2026-09-06 16:20:00] Customer_Kunal: "Do you have original Samsung 65W fast charger with Type-C cable in stock?"
[2026-09-06 16:21:15] MobileShop_Sec22: "Yes sir, Samsung original 65W trio charger is available for ₹2,499 with 1 year manufacturer warranty." 
```

**Model Evaluation Guideline:** Flag 09A on internal concealment descriptions ('hollowed casing', 'lead counterweight', 'screws glued with epoxy'). Control 09B is a standard retail electronics query.

------------------------------------------------------------

### CASE-NARCO-10: Pharmaceutical Blister Diversion
- **Surrogate Codeword:** `Silver Strips / Unmarked Sleeping Lozenges`
- **Canonical Classification:** Schedule H/H1 Diverted Psychotropic Pills
- **Evasion Mechanism:** Diverting controlled pharmaceutical sedative blister strips without prescriptions using color/strip jargon.

#### 🚨 Positive Evasive Intercept (Should be Flagged):
```text
[WHATSAPP ENCRYPTED CHAT: EXHIBIT CHD-PS3-10A]
Participants: Buyer_Tricity_Nitin (+91-9872449911), Chemist_Counter_Mule (+91-9814088990)
Location: Near Sector 32 Government Hospital, Chandigarh

[2026-09-06 19:10:00] Buyer_Tricity_Nitin: "Bhai 10 'Silver Strips' (unmarked sleeping lozenges / alprazolam strips) mil sakti hain bina doctor slip ke?"
[2026-09-06 19:11:45] Chemist_Counter_Mule: "Stock warehouse me h. Strip pe batch number stamp cut kiya hua h for security. ₹600 per strip lagega (normal rate ₹60 h). 10 strip ka ₹6,000 cash only."
[2026-09-06 19:13:20] Buyer_Tricity_Nitin: "Theek h, Sector 32 hospital ke back parking gate pe milo 20 minute me." 
```

#### 🛡️ Benign Negative Control (Should NOT be Flagged):
```text
[PHARMACY PRESCRIPTION REFILL: CONTROL-10B]
Participants: Patient_Attendant, Chemist_Care_Sec32
Location: Sector 32 Chandigarh

[2026-09-06 18:00:00] Patient_Attendant: "Hello, I am sending a photo of the doctor's prescription from GMCH-32 for blood pressure tablets and sleeping aid."
[2026-09-06 18:02:10] Chemist_Care_Sec32: "Prescription verified. Doctor has prescribed 1 strip of 10 tablets. Total bill is ₹78. Please bring original slip for stamping." 
```

**Model Evaluation Guideline:** Flag 10A on avoidance of doctor's slip, 10x price mark-up (₹600 vs ₹60), cut batch numbers, and hospital back-gate handover. Control 10B shows strict prescription compliance.

------------------------------------------------------------