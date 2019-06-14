DevSecOps: The First Step is the Hardest

	Developing functional and secure software is a complex and resource intensive process. Often projects attempt to take shortcuts or buy add-on solutions to the end product when security should have been incorporated from the beginning. I am going to discuss how to start applying strong security practices in order to create more robust applications. 

	Successful development teams tailor their Software Development Lifecycle (SDLC) to meet the demands of DevOps processes. This allows code to be pushed into production several times per day. However, security will lag behind such a schedule, becoming a roadblock. 

	In a perfect world, every deployment would be fully validated by security and evaluated as both individual pieces and integrations within the overall application. That is not a feasible objective, even on small applications. The time needed to conduct such an in-depth analysis would push the delivery of the application well past any reasonable deadline. 

	When security is involved in the SDLC, it is often in the form of a scan run at the end of the development cycle or as an assessment during the final sprint before the code is deployed. Performed in this manner, the results cannot be properly analyzed. Any significant findings would be exceptionally difficult to resolve before deploying, assuming it were possible to modify the application at that point. Misaligned development cycles and last minute changes can cause the worst case scenario: security analysis being performed on an application that no longer represents the code base. 

	Much like DevOps is aided by tooling, DevSecOps is best augmented by specific tools to satisfy coverage. These do not replace strong security practices and analysis, but are intended to produce quick results and identify low hanging fruit issues during early phases of software development. 

	One of the first security tools to apply is a static code analyzer. This should not be a robust tool. For java applications, it is more effective to begin with SonarQube for fast initial results than with HP Fortify. Although Fortify will do a better job of mapping an application and following the paths its parameters take, it is slow with high false positive rates. SonarQube searches the code base for known insecure strings, rather than perform a deep dive on how data travels within the application. This can give developers feedback when they commit code in the time it takes to get a cup of coffee. 

	Initial static analysis should be used as a first gateway to iteratively reduce the number of identified findings and track a team's overall progression. This is used in local developer environments such that code cannot be committed without some security review. 

	Project teams should be designed to build on established successes, such as reducing the overall number of findings by 0.1% or resolving 10 minutes of technical debt with every commit. Setting these measurable goals will track the team's progress and establish processes to reduce an application's overall security risks. This initial step will work best if developers understand and work to resolve discovered findings, rather than sending scan results to a separate security team or attempting to suppress these issues.

	Development teams are often penalized for writing insecure code through annual review metrics or extra work to resolve findings. This makes the security teams become perceived as an enemy. An unintentional side effect is that developers and security resources stop working together for the same goals. Instead of working to understand an application, security may spend a large portion of an assessment fighting to get the application working without support from developers.

	Successful DevSecOps programs require project mindsets to change in terms of security. Project teams, objectives, and metrics should be designed to incorporate security. Rather than use metrics to point fingers at who developed insecure code, tie developer objectives to reducing the number of vulnerabilities. This encourages developers to learn how to write secure code and gives them ownership of resolving potential risks. 

	Developers should strive to resolve security issues within the code or reach out to a security champion to pull resources. Likewise, security teams should strive to include specific coding and configuration remediations along with their findings. 

	A security team member should be involved from a project's outset in an open communication format by actively participating in planning meetings and prioritizing features to develop. This one change helps identify potential issues and insecurities, specifically with early threat modeling efforts or by establishing where security gaps may reside.
	
	Application coding decisions, such as what content to log, require a balance between various teams. More information being logged is essential when debugging an issue or when piecing events together following an incident. However, decisions of what to log, how to protect log data, and the length of time the log data will be stored requires collaboration among business owners, developers, and the security team. Logging too much can lead to the disclosure of sensitive information, which is its own security incident. Logging too little inhibits troubleshooting efforts or information gathering during forensics. This, and many similar conversations must be discussed among the various teams throughout the SDLC and cannot be done properly if various teams are set in silos. 

	DevSecOps doesn't just happen. It requires skilled team members working collectively toward the same goals. Rather than apply a robust security solution, work iteratively and build on small successes. This can be lightweight tools with fast feedback loops, but ultimately is derived from support across the project to develop better code and applications. 





