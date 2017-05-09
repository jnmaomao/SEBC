1.change OS Memory to 8G and 1 vcores is enough
2.increase mapreduce.map.memory.mb to 2048 ,so map task can process more big data.
3.increase mapreduce.reduce.memory.mb to 4096 ,because reduce task usually need more memory.
4.change yarn.scheduler.maximum-allocation-mb to 19968 , use 20 vcore/4 = 5 and use max memory/max task which use max vcore = 103424/5 = 20684
5.mapreduce.job.reduces to 12 , a half of -D mapreduce.job.maps
