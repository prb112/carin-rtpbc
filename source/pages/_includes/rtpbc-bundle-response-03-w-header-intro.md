### Example RTPBC response scenario using FHIR messaging
In this example:
* the client is a patient application
* the server is the patient's insurer (specifically, the party that manages the patient's pharmacy benefit)
* the response is returned as a Bundle containing a ClaimResponse and supporting resources, in response to a Claim.$submit operation

Content:
* the requested medication is Prozac 10mg capsule, 60 capsules, and the requested pharmacy is Hometown Drug. Adjudication returned in the ClaimResponse.item composite
* the .item contains patient costs for the requested drug and pharmacy combination
* the .addItem composite holds an alternative fulfilment (the requested drug at a different pharmacy). Adjudication is returned in the ClaimResponse.addItem composite
* a pharmacy Organization resource describes the alternative pharmacy option identified by the processor
* summary coverage information (e.g., Covered, Covered but requiring PA) is returned in the .processNote element - linked to the particular item using the processNote.number field

<br/>


<div><img src="https://www.frankmckinney.com/carin-rtpbc/rtpbc-bundle-response-03-1-bundle.png" alt="bundle"></div>

<div><img src="https://www.frankmckinney.com/carin-rtpbc/rtpbc-bundle-response-03-2-message-header.png" alt="message-header"></div>

<div><img src="https://www.frankmckinney.com/carin-rtpbc/rtpbc-bundle-response-03-3-claim-response.png" alt="claimresponse"></div>

<div><img src="https://www.frankmckinney.com/carin-rtpbc/rtpbc-bundle-response-03-4-patient.png" alt="patient"></div>

<div><img src="https://www.frankmckinney.com/carin-rtpbc/rtpbc-bundle-response-03-5-organization-pharmacy.png" alt="organization-pharmacy"></div>

<br/>