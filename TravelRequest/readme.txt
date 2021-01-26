YouTube video walkthrough - https://youtu.be/40NJOwydzHE

Use Travel Request Microsoft Lists template
Add 2 columns: 
"Approval Status" of type Choice - Choice Values - "Approved","Rejected by HR","Rejected by Manager","Pending HR Approval","Pending Manager Approval"
"Approval Comments" of type Multi Lines of Text

Conditional formula:
Estimated airfare =if([$Airline]=='','false', 'true')
Estimated hotel cost =if([$Hotel]=='','false', 'true')

In the headerformatting.json file, replace the YourBingMapsKey text with your own Bing Maps Key.
get a Bing Maps Key -https://docs.microsoft.com/en-us/bingmaps/getting-started/bing-maps-dev-center-help/getting-a-bing-maps-key
