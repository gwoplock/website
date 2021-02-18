---
title: "The 2021 Texas power outage is a nation wide problem"
date: 2021-02-18T08:17:36-06:00
draft: false
description: "History is bound to repeat itself and it has almost every year"
categories: "Electricity"
tags: ["Texas"]
---

Let me preface this with an explanation. Over the last few days I read online people saying that Texas' power outages had been caused by Texas being on its own grid... deregulation... Not following national standards...  had Texas been connected to the Eastern Interconnection or the Western Interconnection none of this would have happened. But not one post shows any evidence or requirements that backed up these claims. So, I went looking for proof and instead of finding requirements, I found a nationwide problem with winterization. As an aside I am not an expert in the grid or electricity, I am a software developer, and this is my best interpretation of the requirements I could find. 

Let's start off with how the electrical grid works in the US. The grid is made up of 3 interconnections: the Eastern Interconnection, the Western Interconnection, and the Texas Interconnect. Each of these interconnections operate in (near) isolation with their own frequency, voltage, and phase. There are several high voltage DC interconnects (HVDC or DC-DC) between them. In each of these interconnections there is at least one grid operators, for example ERCOT in Texas. These grid operators manage the generation and load of their interconnection, acting as almost as an electric clearing house. They are also responsible for keeping voltage and frequency within range and directing distributors (like ONCOR in north Texas) to shed load during Electrical Emergency Alerts (EEA). An important thing to note for later, from the best I can tell the different grid operators in the Eastern Interconnect share power in a "non-firm, as-available basis". 

What happened in Texas, starting 12:30 AM February 15. The long and short of it is an estimated 34GW of generation went offline in about 2 hours[1]. Looking at ERCOT's tweets [2,3,4], generation was starting to have an issue at 00:17:45 and some load needed to be shed so ERCOT issued the first EEA (EEA1). In the February EEA tools document[5] EEA1 can open up around 1.6GW of "peeker" generation and importation from the Eastern and Western Interconnections. But by 1:12:06 that wasn't enough and additional load had to be shed.  A second EEA was issued (EEA2) shedding another 1.6GW. But just a few minutes later the house came crashing down and at 1:25:40 the third EEA (EEA3) was issued. In addition to starting rolling blackouts to shed most of the load it also allowed for other actions to free .1-.2GW of load. 

The 34GW of generation lost was from every fuel source used. Most of it was frozen-off natural gas (gas) wells, some of it was frozen wind turbines, solar panels that had snow on them and even a nuclear plant had to go offline due to issues with feedwater pressure sensing issues related to the cold. 
What do the North American Electric Reliability Corporation (NERC) standards say about protecting any of these sources? Not much. 

Let's start by looking at the least complex, wind turbines. On September 12, 2012 NERC published a Lesson Learned document in regards to Texas's issues with some of the wind farms freezing in extreme winter weather[6]. According to the document the event that was predicted over a week beforehand brought 4 days of low temperature, high winds and wind chills, ice and snow that limited the generation facility to just 25% of capacity. The facility did have a SOP for icing conditions that was implemented. However, the facility never defined it's minimum operating temperature. When lightning knocked out some of the sensing equipment, the turbines had to be stop for safety. The repair crews couldn't immediately get to the turbines and they had to sit, this gave the oil a chance to cool and partly freeze. When the turbines were returned to service, they tripped back off due to high oil pressure. Eventually after working with the manufacturer they were able to safely heat the oil and restart the turbines. One of the big lessons from this was to install cold weather packs for wind turbines and watch the oil temperature. You'd think that would solve future outage, but no, in 2019 in the midwestwind turbines failed due to exceptionally low temperatures, around -21. Again the cold weather package hadn't been installed and was one of the root causes of the failure[7].

The nuclear plant's sensing problems had happened before too. Although it wasn't a nuclear plant, there are several documented cases on NERC's website citing cold weather and sensor issues [8,9]. This repeated in Texas (2011) and in the south east (2018)[10]. 

Let's discuss natural gas next. It appears that most of the issues in the problematic natural gas fired facilities was due to low gas supplies. In 2012 NERC warned of the interconnectivity of natural gas and electric[11]. Natural gas coming out of the ground has a naturally high water content. This water can freeze the extraction equipment during sub-freezing weather in improperly winterized wells creating what is know as a freeze-off. businesses, residential customers, and powerplants all run off the same supply, once wells start freezing off the supply dwindles for all. Natural gas companies prioritize residential customers as needed and will cut businesses and powerplants. This obviously creates issues in electrical generation. 

In this latest case, much of the gas generation loss was due to under pressure conditions at the generation site. When generation sites detect this kind of fault, they are taken offline for safety. Not only is this what happened this year, but it has happened many, many times before

The most resent case I could find was 2018 in the south east[10]. Starting on January 18, 2018 a large area in the south east US experienced unusually cold weather. This caused 183 generation facilities to go offline or operate with greatly reduced output. At the peak there was nearly 30GW of production lost. This caused several grid operators to issue EEAs and begin rolling blackouts. In the "event area" 14% of the failures could be directly attributed to the cold weather. And another 30% could be indirectly linked to weather, including mechanical failures know to happen in cold weather and gas supply issues. NERC found that more than 33% of the failed powerplants didn't have a winterization plan. 

Why didn't these plants have a winterization plan? Because it wasn't required[10,12].

This wouldn't be so bad if this wqs the first time it happened, it wasn't even the second time it happened. In 2014 a polar vortex hit the US. bringing temperatures well below normal. During this event 55% of the outages were at gas power plants and in all 90GW of generation was lost[13]. 

The earliest report I could find was from the 2011 winter event in Texas[14]. A very strong cold front hit Texas (and other parts of the south central US) bringing temperatures below freezing for over 4 days and winds over 30 MPH. Leading up to the event, ERCOT and other grid operators in surrounding areas felt that there wouldn't be a need for rolling blackouts. At the beginning of the event ERCOT had 3.1GW of reserve, nearly 1GW over the minimum required. However, over the next 2 days ERCOT lost nearly 30GW of production in 193 generation facilities. ERCOT was able to stabilize the grid with rolling blackouts and the other EEA methods[5]. Other grids suffered problems as well, EPE (El Paso) and SRP (Arizona) lost nearly 1.4GW due to cold weather. Another issue in ERCOT's region was nearly 50% of the "black start" facilities were either down for scheduled maintenance or failed on startup. One of the main causes again was the loss of gas during this blackout period. 14.8 Bcf of natural gas production was lost due to freeze-offs, electrical outages (ironically) and customer curtailments. following the previous equivalent storm in 1989, the PUCT (Public Utility Commission of Texas) issued several recommendations and guidelines for winterization of power plants and gas wells. However, due to the infrequency of these storms the implementation lacked. With many of the same facilities that failed in 1989 also failed in 2011.  My guess is these same sites failed again in 2021. Interestingly the NERC found that it is quite possible that gas production in these unusually cold conditions may be impossible.

What has been done since 2011? Not a whole lot. A request for a new standard was issued to NERC in late 2012, however a few months later it was denied.[15] Also in 2012 NERC put out a set of guidelines for developing a plan for winter weather[16]. In 2017 NERC put out a special reliability report on the relationship between gas and electricity[17]. Finally, after the 2018 event NERC received another standard request that was approved[23], however it won't be finalized until late 2021[18,19,20]. 

From what I can see, ERCOT has more restrictive rules in their Generator Winter Weatherization Workshop than NERC[21]. All generation stations must have plans for emergencies, address abnormal weather, critical failure points, weather design limits, alternative fuels and testing[21,22]. ERCOT reports that there were 80 spot checks done in the 2019/2020 season with 71 being gas plants and 6 being black start gas plants. 23 had to improve and would be reinspected in early 2021 the rest passed.  

The issue of extreme cold weather and electrical outages is a national issue that needs to be addressed. However, after repeated failings it hasn't really been addressed. Hopefully with the new NERC requirements and the Texas legislature in session progress can be made.

---

[1] http://www.ercot.com/news/releases/show/225244  
[2] https://twitter.com/ERCOT_ISO/status/1361197991659503618  
[3] https://twitter.com/ERCOT_ISO/status/1361211669788176384  
[4] https://twitter.com/ERCOT_ISO/status/1361215084010352644  
[5] http://www.ercot.com/content/wcm/lists/219692/EEA_Tools_One_Pager_Winter_2021_2-13-2021.pdf  
[6] https://www.nerc.com/pa/rrm/ea/Lessons%20Learned%20Document%20Library/LL20120901_Wind_Farm_Winter_Storm_Issues.pdf  
[7] https://www.nerc.com/pa/rrm/ea/Lessons%20Learned%20Document%20Library/LL20200601_Unanticipated_Wind_Generation_Cutoffs_during_a_Cold_Weather_Event.pdf  
[8] https://www.nerc.com/pa/rrm/ea/Lessons%20Learned%20Document%20Library/LL20111001_Plant_Instrument_and_Sending_Equipment_Freezing_Due_to_Heat_Trace_and_Insulation_Failures.pdf  
[9] https://www.nerc.com/pa/rrm/ea/Lessons%20Learned%20Document%20Library/LL20110902_Adequate_Maintenance_and_Inspection_of_Generator_Freeze_Protection.pdf  
[10] https://www.ferc.gov/sites/default/files/2020-04/07-18-19-ferc-nerc-report.pdf  
[11] https://www.nerc.com/pa/rrm/ea/Lessons%20Learned%20Document%20Library/LL20120905_Gas_and_Electricity_Interdependency.pdf  
[12] https://www.nerc.com/comm/OC_Reliability_Guidelines_DL/Reliability_Guideline_Generating_Unit_Winter_Weather_Readiness_v3_Final.pdf  
[13] https://www.nerc.com/pa/rrm/ea/ColdWeatherTrainingMaterials/Polar_Vortex_Review_2014.pdf  
[14] https://www.ferc.gov/sites/default/files/2020-04/08-16-11-report.pdf  
[15] https://www.nerc.com/pa/Stand/Pages/Project2013-01_Cold_Weather.aspx  
[16] https://www.nerc.com/comm/OC_Reliability_Guidelines_DL/Reliability_Guideline_Generating_Unit_Winter_Weather_Readiness_v3_Final.pdf  
[17] https://www.nerc.com/pa/RAPA/ra/Reliability%20Assessments%20DL/NERC_SPOD_11142017_Final.pdf  
[18] https://www.nerc.com/pa/Stand/Project%20201906%20Cold%20Weather%20DL/EOP-011-2_Clean_01272021.pdf  
[19] https://www.nerc.com/pa/Stand/Project%20201906%20Cold%20Weather%20DL/IRO-010-4_Clean_01272021.pdf  
[20] https://www.nerc.com/pa/Stand/Project%20201906%20Cold%20Weather%20DL/TOP-003-5_Clean_01272021.pdf  
[21] http://www.ercot.com/content/wcm/key_documents_lists/210163/7._ERCOT_Weatherization_Workshop_2020_2021_Final.pdf  
[22] https://www.puc.texas.gov/agency/rulesnlaws/subrules/electric/25.53/25.53.pdf   
[23] https://www.nerc.com/pa/Stand/Project%20201906%20Cold%20Weather%20DL/2019-06_Cold_Weather_SAR_10042019.pdf  
[24] https://www.nerc.com/pa/Stand/Pages/Project%202019-06%20Cold%20Weather.aspx