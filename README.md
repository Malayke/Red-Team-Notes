# 什么是红队？


The Red Team’s mission is to emulate the tactics, techniques, and procedures (TTPs) by adversaries.  The goals are to give real world and hard facts on how a company will respond, find gaps within a security program, identify skill gaps within employees, and ultimately increase their security posture.
> Kim, Peter. The Hacker Playbook 3: Practical Guide To Penetration Testing . Secure Planet.

我不太恰当的翻译和补充：

红蓝对抗是军事用语，红队作为对抗者其任务是模拟 [战术、技术和过程(TTPs)](https://blog.csdn.net/chenyulancn/article/details/79065169)。 使用真实世界的攻击手法（APT）对目标发起攻击，找出对方在安全防护上的缺陷，找出员工的技术缺陷，并最终提高他们的安全防护状况。

------

近几年随着 Red Team 建设的话题越来越流行，不管是甲方或者乙方都在极力的发展自己的 Red Teaming 能力，尤其是各个乙方都推出了自己的 Red Team服务，如：[FireEye](https://www.fireeye.com/content/dam/fireeye-www/services/pdfs/pf/ms/ds-red-team-for-security-operations.pdf)，他们的最终目的都是为甲方输出检验企业的Detection（识别）和Response（防御）能力，找到防御弱点进而优化防御系统和流程。

我们不禁要思考一下，到底什么样的企业才真的需要Red Team？当然，输出安全能力和服务的乙方不在讨论范围内，因为其最终是为了服务和支持甲方。根据我的观察和发现，目前大部分人很容易把 Red Team 和 Penetration Testing 弄混或者干脆混为一谈。其实**二者有共同点但也有本质上的不同**，简单做个比喻就是忍者(隐秘，快速，准确，一击即中)和海盗（强壮，贪婪，可以刚正面，一波高地）的区别，各有侧重和优劣，但侧重点不同，比如，Red Team类似忍者，侧重于精心准备（如：社会工程学等）收集信息进而绕过现有的防御体系（类似于APT）来检验防御和检测能力；而Penetration Testing则如同海盗，侧重于尽可能多地发现应用，系统，网络，设备等的漏洞，并利用其发现更深层或者复杂的漏洞从而来评估风险。所以，答案显而易见，一个企业只有拥有了基本的防御和检测的能力，并需要持续检测和改善这种能力时，Red Team就是很好地选择了。

那么，什么样的Red Team才算合格和有效呢？如前面所说，Red Team如同忍者去做暗杀，既然暗杀那么就需要一个详细的计划，如：目标是什么（暗杀对方头目），手段是什么（前期侦查对方大本营，守卫布局，对方头目的日常习惯和出现的场所，会不会功夫等），如何去执行（选择某个夜黑风高的晚上，众人都准备或者已经睡觉的时候，摸进对方大本营，提前隐藏在对方头目习惯出现的场所，等待其出现，再一刀毙命）。对应到Red Team就是，1）设置好这次行动目的是模拟偷取公司的客户资料；2）提前做好侦查看看公司都可能有哪些人会碰到这类数据，有哪些防御检测方式（如：反病毒，入侵检测，流量分析）；3）针对可能接触数据的人员做定向钓鱼攻击或者面对面的社工，安装专门制作的绕杀软的工具，利用常见的社交或者云存储网站来做C2，等待时机控制机器，获取必要的用户凭证，盗取客户资料，销毁痕迹，最终走人。因此，一个合格的Red Team，需要具备模拟攻击者入侵的各种能力，手段以及假想的目的。想要具备这种能力的一个最简单有效的方法，就是从现有的真实世界里发生的APT攻击活动中抽取TTP来模拟真实的threat actors，分类并总结他们曾今采用的手段，方法，技术和工具，然后加以优化和改进，最终结合每个Red Team活动的假想目的来模拟不同APT组织对于公司的入侵，以此来检测已有的防御和响应体系是否有效。

> 安全小飞侠，知识星球

------

Red Team mindset and focus on: 
* Vulnerabilities in Security not IT  
* Simulate Real World events  
* Live in a world of constant Red Team infections

Challenge the system…  Provide real data to prove security gaps.

> Kim, Peter. The Hacker Playbook 3: Practical Guide To Penetration Testing . Secure Planet. Kindle Edition. 

我不太恰当的翻译和补充：

红队的核心关注点：

* 发现安全防护上的漏洞，不是安全漏洞
* 模拟真实世界正在发生的攻击手法，也就是APT
* 生活在一个不断被红队感染的世界里

勇敢的去挑战，为提高安全防护水平提供真实的数据

------


