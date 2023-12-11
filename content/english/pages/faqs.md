---
title: "FAQs"
# meta title
meta_title: ""
# meta description
description: "This is meta description"
# save as draft
draft: false
---

{{< accordion "How do I configure Dialpine Service?" >}}

- The day you setup the service with us, we created a new "Master Congiguration" event in Dialpine Calendar
- Look for : [MASTERT CONFIG - DO NOT DELETE - CAN MODIFY]
- Edit this event to reveal all the Dialpine Congigurations and edit accordingly.

{{< /accordion >}}

{{< accordion "How do I change my Office Name greeting thats announced to my customers ?" >}}

- Change "sStoreName": "Office Of So and So", with your office name
- example : 
- "sStoreName": "Office Of Sams Physical Therapy",

{{< /accordion >}}

{{< accordion "How do I configure my first and last appointment time" >}}

- Change --- "startTime": "08:00" --- with the time you want your first booking to start
- Change --- "iMinimumWorkHours": 10, --- with the time you want your first booking to end
- example : 
- A Start time of 8 and Minimum Work hours of 10 mean, your last booking shall end at 6 pm

{{< /accordion >}}

{{< accordion "How do I configure handling non english speakers ?" >}}

- After we play your office greeting, we ask the person "Press 1 for English, 2 for Other Languages"
- Change --- "OperatorLangs": "Other Languages", ---  
- Example : Change "Other Languages" to "Spanish",
- You would also need to chnage the Operator Number
- Change --- "OperatorNumber": "+13105551231", --- : Put your full Office number here so that Dialping can forward these calls.
{{< /accordion >}}

{{< accordion "Advanced : How do I configure 5 rooms with 3 doctors  ?" >}}

- Dialpine allows your to have more patients in office than there are doctors.
- Example : You may have 5 rooms and 3 doctors.
- These two settings give you the flexibility needed to configure bookings accordingly.
- "overlappSlots": 3,
- "overlappSlotsFacility": 5,
- Dialpine - out of the box - will allow 3 new bookings to start at the top of the hour
- However, it will also ensure there are never more that 5 patients occupying the rooms
- This is helpful when a doctor might spend 1 hour with the patient but keep the patient on Traction for 30mins to 60mins extra. In this case a room is still occupied but doctor is open to see other patients.

{{< /accordion >}}


{{< accordion "Advanced : How do I configure that some patients should always be seen by the Sr. Doctor  ?" >}}

- Dialpine assigns every patient "patcode", aka Patient Codes
- Every new patient is assigned a patcode of 0. This is visible and editable in Google Contact.
- Dialpine will ensure that at any given appointment time, there is only one patient with "patcode" of 0
- Dialpine also provides flexibilty that certain patients should always be seen by Sr. Doctor.
- To do so, your office will have to assign these patients with "patcode" of 5 in Google Contact.
- Dialpine is smart, it will always ensure that only one "New Patient" or "Serious Condition Patient" is give the same appointment.

{{< /accordion >}}

{{< accordion "What else can I configure ?" >}}

- "blackListNumCommaSep" : "+13105551232,+13105551233" :: Edit this to add certain number that Dialpine should block from ever reaching your operator or making bookings.
- "firstTimeCallerToOperator" : false :: Change this to true if you want the first call to always come to operator. This is helpful if you want to talk to these customers first.
- "sendNonApprovedToOperator": false, :: By default, Dialpine will allow call all callers to make a booking. If you ONLY want "Approved" callers to make a booking, then change this to true. This ads an additonal step where in your office staff will have to open the Google Contact of the caller and set the "auto_approved" flag to "yes". This is helpful if your office wants to approve certain patients after verifying their insurance.
- "slotDurationInMins": 30, ::  Default appointment time for the caller ( you can chnage this in Google Contacts)
- "daysAheadAllowed": 30, :: How many days of your calendar is open for Dialpine controller bookings.
- "insuranceCheckNeeded": false, :: Change this to true in case you want to ask a caller "If your insurance has changed" at regular intervals. Use below setting to change how long to wait before asking. 
- "insuranceCheckReminderDays": 30, :: Use this to in conjunction with above setting.

{{< /accordion >}}
