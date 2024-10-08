{% from "_course-" + course + "/weeklyTpTasks-fragment.md" import weekly_tp_themes with context %}

{% set admin_topics = [
  {level: 1, id: "courseOverview", title: course_pair + ": " + course_name, link: "courseOverview.html", alt: "Course Overview"},
  {level: 1, id: "usingThisWebsite", title: "Using this Website", link: "usingThisWebsite.html", highlight: "true", priority: 1},
  {level: 1, id: "courseExpectations", title: "Course Expectations", link: "courseExpectations.html", priority: 2},
  {level: 0, id: "courseStructure", title: "Course Structure"},
    {level: 2, id: "courseBriefings", title: "Course Briefing Videos", link: "courseBriefings.html", priority: 3},
    {level: 2, id: "weeklySchedule", title: "Weekly Schedule", link: "weeklySchedule.html", priority: 3},
    {level: 2, id: "lectures", title: "Weekly Briefings", link: "lectures.html", priority: 3},
    {level: 2, id: "tutorials", title: "Tutorials", link: "tutorials.html", priority: 2},
  {level: 1, id: "instructors", title: "Instructors", link: "instructors.html", priority: 4},
  {level: 1, id: "textbooks", title: "Textbooks", link: "textbooks.html", priority: 2},
  {level: 1, id: "programmingLanguages", title: "Programming Language", link: "programmingLanguages.html", priority: 2},
  {level: 1, id: "standardsAndConventions", title: "Standards/Conventions", link: "standardsAndConventions.html", priority: 2},
  {level: -1, id: "ip", title: "Individual Project (iP)"},
    {level: 2, id: "ip-overview", title: "iP (Individual Project): Overview", link: "ip-overview.html", priority: 2},
    {level: 2, id: "ip-w2", title: "iP: Week 2", link: "ip-w2.html", priority: 2},
    {level: 2, id: "ip-w3", title: "iP: Week 3", link: "ip-w3.html", priority: 2},
    {level: 2, id: "ip-w4", title: "iP: Week 4", link: "ip-w4.html", priority: 2},
    {level: 2, id: "ip-w5", title: "iP: Week 5", link: "ip-w5.html", priority: 2},
    {level: 2, id: "ip-w6", title: "iP: Week 6", link: "ip-w6.html", priority: 1},
    {level: 2, id: "ip-w7", title: "iP: Week 7", link: "ip-w7.html", priority: (4 if course == "CS2103" else 1)},
    {level: 2, id: "ip-w8", title: "iP: Week 8", link: "ip-w8.html", priority: 1},
    {level: 2, id: "ip-grading", title: "iP: Grading", link: "ip-grading.html", priority: 2},
  {level: -1, id: "project", title: "Team Project (tP)"},
    {level: 2, id: "tp-overview", title: "tP (team project): Overview", link: "tp-overview.html", priority: 2},
    {level: 2, id: "tp-expectations", title: "tP: Expectations", link: "tp-expectations.html", priority: 2},
    {level: 2, id: "tp-timeline", title: "tP: Timeline", link: "tp-timeline.html", priority: 3},
    {level: 2, id: "tp-constraints", title: "tP: Constraints", link: "tp-constraints.html", priority: 2},
    {level: 2, id: "tp-teams", title: "tP: Forming Teams", link: "tp-teams.html", priority: 2},
    {level: 2, id: "tp-w3", title: "tP Week 3: " + weekly_tp_themes.w3.name, link: "tp-w3.html", priority: 2},
    {level: 2, id: "tp-w4", title: "tP Week 4: " + weekly_tp_themes.w4.name, link: "tp-w4.html", priority: 3},
    {level: 2, id: "tp-w5", title: "tP Week 5: " + weekly_tp_themes.w5.name, link: "tp-w5.html", priority: 2},
    {level: 2, id: "tp-w6", title: "tP Week 6: " + weekly_tp_themes.w6.name, link: "tp-w6.html", priority: 2},
    {level: 2, id: "tp-w7", title: "tP Week 7: " + weekly_tp_themes.w7.name, link: "tp-w7.html", priority: 2},
    {level: 2, id: "tp-w8", title: "tP Week 8: " + weekly_tp_themes.w8.name, link: "tp-w8.html", priority: 3},
    {level: 2, id: "tp-w9", title: "tP Week 9: " + weekly_tp_themes.w9.name, link: "tp-w9.html", priority: 2},
    {level: 2, id: "tp-w10", title: "tP Week 10: " + weekly_tp_themes.w10.name, link: "tp-w10.html", priority: 2},
    {level: 2, id: "tp-w11", title: "tP Week 11: " + weekly_tp_themes.w11.name, link: "tp-w11.html", priority: 2},
    {level: 2, id: "tp-w12", title: "tP Week 12: " + weekly_tp_themes.w12.name, link: "tp-w12.html", priority: 3},
    {level: 2, id: "tp-w13", title: "tP Week 13: " + weekly_tp_themes.w13.name, link: "tp-w13.html", priority: 2},
    {level: 2, id: "tp-deliverables", title: "tP: Deliverables", link: "tp-deliverables.html", priority: 2},
    {level: 2, id: "tp-ped", title: "tP: Practical Exam Dry Run", link: "tp-ped.html", priority: 2},
    {level: 2, id: "tp-pe", title: "tP: Practical Exam", link: "tp-pe.html", priority: 2},
    {level: 2, id: "tp-grading", title: "tP: Grading", link: "tp-grading.html", priority: 2},
    {level: 2, id: "tp-supervision", title: "tP: Supervision/Guidance", link: "tp-supervision.html", priority: 2},
  {level: 1, id: "peerEvaluations", title: "Peer Evaluations", link: "peerEvaluations.html", priority: 2},
  {level: 1, id: "tools", title: "Tools", link: "tools.html", priority: 3},
  {level: 1, id: "exams", title: "Exams", link: "exams.html", priority: 2},
  {level: 1, id: "participation", title: "Participation Marks", link: "participation.html", priority: 2},
  {level: 1, id: "gradeBreakdown", title: "Grade Breakdown", link: "gradeBreakdown.html", priority: 2},
  {level: 0, id: "appendices", title: "Appendices"},
    {level: 2, id: "appendixA-principles", title: "Apdx A: Course Principles", link: "appendixA-principles.html", priority: 4},
    {level: 2, id: "appendixB-policies", title: "Apdx B: Course Policies", link: "appendixB-policies.html", priority: 1},
    {level: 2, id: "appendixC-faq", title: "Apdx C: FAQ", link: "appendixC-faq.html", priority: 1},
    {level: 2, id: "appendixD-help", title: "Apdx D: Getting Help", link: "appendixD-help.html", priority: 2},
    {level: 2, id: "appendixE-gitHub", title: "Apdx E: Using GitHub", link: "appendixE-gitHub.html", priority: 1},
    {level: 2, id: "appendixF-teamworkIssues", title: "Apdx F: Handling Team Issues", link: "appendixF-teamworkIssues.html", priority: 4}
]%}

{% set weekly_admin_topics = {
week1: [
  {faq_id: "whereIsEverything"},
  {topic_id: "tp-teams"},
  {topic_id: "textbooks"},
  {topic_id: "gradeBreakdown"},
  {faq_id: "tVsNonT"},
  {faq_id: "aPlus"}],
week2: [
  {policy_id: "policy-plagiarism"},
  {policy_id: "policy-reuse"},
  {policy_id: "policy-outsiderHelp"},
  {policy_id: "policy-followingInstructions"},
  {policy_id: "policy-techHelp"},
  {topic_id: "appendixA-principles"},
  {faq_id: "separateWebsite"},
  {faq_id: "slideFormat"}],
week3: [
  {policy_id: "policy-adminQuestions"},
  {topic_id: "tutorials"},
  {topic_id: "peerEvaluations"},
  {topic_id: "standardsAndConventions"},
  {topic_id: "tp-supervision"},
  {policy_id: "policy-teamSize"}],
week4: [
  {faq_id: "narrowProjectScope"},
  {faq_id: "favoriteTool"},
  {policy_id: "policy-publishingSubmissions"}],
week5: [
  {topic_id: "tp-grading"},
  {policy_id: "policy-workDistribution"},
  {policy_id: "policy-responseTime"},
  {faq_id: "beanCounting"}],
week6: [
  {topic_id: "appendixF-teamworkIssues"},
  {faq_id: "manySubmissions"},
  {faq_id: "cs2101Difference"}],
week7: [],
week8: [],
week9: [],
week10: [],
week11: [
  {topic_id: "exams"}],
week12: [],
week13: []
}%}
