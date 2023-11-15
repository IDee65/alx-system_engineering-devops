As a component of the ALX Software Engineering Program, we were assigned the intriguing task of crafting a postmortem using our imaginative and creative faculties.

According to Wikipedia, a postmortem or project post-mortem is a procedure employed to pinpoint the reasons behind a project failure or substantial business-impairing downtime, and to strategize preventive measures for the future. It can be likened to undergoing a medical checkup as a human and taking medications to either cure or prevent illness.

Postmortem Report Overview:

Issue Summary: On November 5, 2023, between 03:45 AM (UTC) and 11:30 AM (UTC), an unprecedented service disruption occurred, impacting our flagship messaging service. Communication for 30% of our user base was disrupted.

Root Cause: A misconfigured load balancer during routine maintenance triggered a cascading failure. This misconfiguration caused an uneven distribution of traffic, overwhelming some servers while leaving others underutilized.

Impact: The cascading failure affected the messaging service, disrupting communication for 30% of our user base.

Timeline:

Detection: Automated monitoring alerted the on-call engineer at 03:45 AM (UTC) to an unusual spike in error rates.
Investigation: Initial suspicion of a DDoS attack led to the discovery of a misconfiguration in the load balancer settings.
Misleading Paths: Early assumptions about database issues and network latency diverted attention from the actual misconfiguration.
Escalation: The incident was escalated to the system reliability team for its complexity.
Resolution: Immediate relief was achieved by rolling back the load balancer configuration. A comprehensive fix involved reconfiguring the load balancer to ensure proper request distribution.

Root Cause and Resolution:

Root Cause: Misconfigured load balancer settings causing uneven traffic distribution.
Resolution: Immediate relief through rollback and permanent fix by reconfiguring the load balancer, validated through extensive testing.
Corrective and Preventative Measures:

Improvements/Fixes:
Regular audits of critical infrastructure configurations.
Enhanced monitoring thresholds for load balancer performance.
Tasks:
Thorough review of load balancer configurations.
Improved documentation for load balancer maintenance.
Automated checks for load balancer configurations after updates.
Training sessions for the operations team on load balancer management best practices.
Conclusion: This incident emphasized the need for regular infrastructure audits and vigilant monitoring. The misconfiguration, while unintentional, significantly impacted user experience. Our commitment to continuous improvement involves not only resolving incidents promptly but also implementing measures to prevent recurrence. The outlined corrective actions aim to strengthen our systems for a more robust and resilient service.
