---
dg-publish: true
title: CASN Meeting & Sprint Notes
participants: Shristi Shrestha, Summer Dann, Natalie Ray, Nash Mahmoud, Rachel Veron (Blanco Institute)
---
# Meeting pre-notes

**Test dashboard:** https://casn-bfc18.web.app/

- CTE enrollments at `/schools/cte-enrollments`
	- Displays students' enrollment in different regions by different career clusters. You have to select a career cluster, for now, to see how different regions are doing within that cluster. 
	- We have the highest number of job openings in `health` career sector. 
	- **For example**: Within the `digital technology` career cluster, we have more student enrollments in the regions 1 and 2, followed by 4 and 7. Regions 5, 6, and 8 have fewer than 50 student enrollments
	- The data was collected from the LCTCS Perkins CTE enrollment PowerBI dashboard. The source data is basically a CSV file where each row is a student taking part in a specific program course in a school. We just aggregated the data to count by regions for each career cluster. 
	- Let me know if you want to look at the data yourself. It's a big file of around 15-20MB. The dashboard has summarized data only. 

- Labor Market at `/market/whos-hiring` 
	- displays number of unique job postings in different regions by different career clusters. You have to select a career cluster, for now, to see how different regions are doing within that cluster. 
	- We have the highest number of job openings in `health` career sector. 
	- **For example**: Within the `digital technology` career cluster , we have more job postings in the Region 2, followed by regions 1, 4, and 9. The rest of the regions are not doing so well; they have fewer than 20 jobs openings in this career cluster. 
	- The data was collected from the LA works site. We collected the data in September, which had the data for August of 2026. 

- Analytics at `/analytics/whos-hiring`
	- In this page, we want to display how different regions are doing in terms of both job openings and the number of students enrollment in a given cluster. **For example**: 
		- We have the highest number of job openings in `health` career sector. 
		- In this career sector, if we are looking at the `number of jobs openings per student`, we have more jobs in the regions 9 and 5, followed by region 6. Region 2, that's us is not doing that well. 
		- In contrast, if we are looking at `the number of students enrolled per job opening`, we have more students competing for the same job in the regions 8 and 3, followed by region 2. Region 6 and 5 have fewer students that are competing for the job openings in the health sector.  

- **Things to clarify**
	- There are `four types of timestamps` for data being display
		- When the data was collected exactly. This depends on site/organization who collected the  data. 
		- When the data was posted. This depends on site/organization who collected the  data. 
		- When we collected/downloaded the data.
	
	- `LCTCS` dataset has following characteristics
		- Each row represents a student taking part in a program course in a school. So, if the student has taken multiple courses, the data has multiple rows for such participation. 
		- A school may serve in different parishes that belong to different regions. The data does not specify which parish the schools serve. In my previous implementation, this created a conflict as to where the schools are in the nine regions. For now, I implemented a mapping, where BRCC belongs to region 2 (see [Dashboard: College to Region assignments](https://casn-bfc18.web.app/data-source/college_region_assignments)). Let me know if there are inaccuracies in the mapping. 
	- I have changed the color scheme for showing data intensity across the nine regions. I am using multiple shades of the same color, except for the light yellow color, because they all represent the same data metric like job openings, CTE student count. 
	
# In-Meeting Notes

- Rachel has data from **Blanco institute**
	- Data from degree completion. 
	- Classification of instruction program (CIP to SOC). Need for info on this. 
	- SIP from the academic to CIP to SOC is industry I think
	- https://www.laworks.net/LaborMarketInfo/LMI_OccAllProj.asp?years=20162026
		- job occupations' growth in ten years (since 2024)
	- Send `data access request` to her
	 - https://blancocenter.louisiana.edu/about-us/center-staff
	 - https://blancocenter.louisiana.edu/sites/blancocenter/files/Blanco%20Center%20-%20Linking%20Postsecondary%20Pathways%20-%202026.pdf
		 - Read this report and check if we can use any of their data (non PI) and contact her to get the data. 
