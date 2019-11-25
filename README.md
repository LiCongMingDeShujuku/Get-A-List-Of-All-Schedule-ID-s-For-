![CLEVER DATA GIT REPO](https://raw.githubusercontent.com/LiCongMingDeShujuku/git-resources/master/0-clever-data-github.png "李聪明的数据库")

# 获取代理作业的所有计划ID列表 Agent JOBS
#### Get A List Of All Schedule ID’s For SQL Agent Jobs
**发布-日期: 2015年09月14日 (评论)**


## Contents

- [中文](#中文)
- [English](#English)
- [SQL Logic](#Logic)
- [Build Info](#Build-Info)
- [Author](#Author)
- [License](#License) 


## 中文
这里有一些可以显示所有作业中的所有计划ID的快速SQL逻辑。如果你在整个过程中有多个具有相同目的的代理作业，并且你需要修改所有这些作业的计划，这会很有用。获取计划ID将允许你批量更新计划。


## English
Here’s some quick SQL Logic to show you all the schedule ID’s across all your Jobs. This will help if you have multiple  across the enterprise that have the same purpose, and you need to modify the schedule across them all. Getting the Schedule ID will allow you to do a mass update of the schedules.

---
## Logic
```SQL
use master;
set nocount on
 
select
sj.name
,   sjs.step_id
,   sjs.step_name
,   sjsched.schedule_id
from
msdb..sysjobs sj join msdb..sysjobsteps sjs on sj.job_id = sjs.job_id join msdb..sysjobschedules sjsched on sj.job_id = sjsched.job_id order by
sj.name
,   sjs.step_id asc


```



[![WorksEveryTime](https://forthebadge.com/images/badges/60-percent-of-the-time-works-every-time.svg)](https://shitday.de/)

## Build-Info

| Build Quality | Build History |
|--|--|
|<table><tr><td>[![Build-Status](https://ci.appveyor.com/api/projects/status/pjxh5g91jpbh7t84?svg?style=flat-square)](#)</td></tr><tr><td>[![Coverage](https://coveralls.io/repos/github/tygerbytes/ResourceFitness/badge.svg?style=flat-square)](#)</td></tr><tr><td>[![Nuget](https://img.shields.io/nuget/v/TW.Resfit.Core.svg?style=flat-square)](#)</td></tr></table>|<table><tr><td>[![Build history](https://buildstats.info/appveyor/chart/tygerbytes/resourcefitness)](#)</td></tr></table>|

## Author

- **李聪明的数据库 Lee's Clever Data**
- **Mike的数据库宝典 Mikes Database Collection**
- **李聪明的数据库** "Lee Songming"

[![Gist](https://img.shields.io/badge/Gist-李聪明的数据库-<COLOR>.svg)](https://gist.github.com/congmingshuju)
[![Twitter](https://img.shields.io/badge/Twitter-mike的数据库宝典-<COLOR>.svg)](https://twitter.com/mikesdatawork?lang=en)
[![Wordpress](https://img.shields.io/badge/Wordpress-mike的数据库宝典-<COLOR>.svg)](https://mikesdatawork.wordpress.com/)

---
## License
[![LicenseCCSA](https://img.shields.io/badge/License-CreativeCommonsSA-<COLOR>.svg)](https://creativecommons.org/share-your-work/licensing-types-examples/)

![Lee Songming](https://raw.githubusercontent.com/LiCongMingDeShujuku/git-resources/master/1-clever-data-github.png "李聪明的数据库")

