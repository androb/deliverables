--- 
title: Interview Guide for  {{ role }}
subtitle:  {{ company }}
author: Created by [Deliverables AI](https://github.com/androb/deliverables)
date: {{ today's date and time }}
--- 

# Interview Guide for {{ role }}

<thinking>Your thinking about the guide</thinking>

## About this Guide

<thinking>Your thinking about how to introduce this guide</thinking>

{{ About this guide in 4 paragraphs }}

### Interview Agenda

<thinking>Your thinking about the interview agenda</thinking>

{{ detailedInterviewAgendaAsMarkdown }}

### Competency Framework

<thinking>Your thinking about the competencies</thinking>

{{ competencyFrameworkDescription }}

{% for competency in competencies %}
{{ loop.index }}. **{{ competency[0] }}**: {{ competency[1] }}

{% endfor %}

## Job Description

{{ Job description provided by the user with the formatting cleaned up. Use bold for headings. Make sure there is a blank line before lists. }}

{% for jobdescriptionsection in jobdescription %}
** {{ jobdescriptionsection.heading }}

{{ jobdescriptionsection.content }}

{% endfor %}

{% for competency in competencies %}

## Competency {{ loop.index }}. **{{ competency.title }}**

<thinking>Your thinking about this section</thinking>

{{ competency.description }}

### Lead Question

<thinking>Your thinking about this section</thinking>

**&ldquo;{{ competency.leadQuestion }}&rdquo;** {{ competency.leadQuestionFollowup1 }} {{ competency.leadQuestionFollowup2 }} {{ competency.leadQuestionFollowup3 }}

&nbsp;

&nbsp;

_{{ competency.leadQuestionWhatToLookFor }}__

### Situational Scenario

<thinking>Your thinking about this section</thinking>

**&ldquo;{{ competency.detailedSituationalScenario }}&rdquo;**

&nbsp;

&nbsp;

_{{ competency.scenarioWhatToLookFor }}_

### Diving Deeper

<thinking>Your thinking about this section</thinking>

{% for question in competency.deepDiveQuestions %}
- &ldquo;{{ question }}&rdquo;
{% endfor %}

&nbsp;

&nbsp;

### Evaluation

| Rating 1 | Rating 2 | Rating 3 | Rating 4 | Rating 5 |
| -------- | -------- | -------- | -------- | -------- |
{% for evaluation in competency.evaluation %}
| {{ evaluation.Rating1 }} | {{ evaluation.Rating2 }} | {{ evaluation.Rating3 }} | {{ evaluation.Rating4 }} | {{ evaluation.Rating5 }} |
{% endfor %}

{% endfor %}

## Case Study

<thinking>Your thinking about this section</thinking>

{{ Clearly define a specific problem or challenge faced by the company. This should be relevant to the job role and require skills that are essential for the position. Include details such as financial constraints, time pressures, or resource limitations. Provide any necessary data, graphs, or additional resources that the candidate would need to analyze to solve the problem. This could include financial reports, market research, customer feedback, etc. List specific questions the candidate should address in their response. These might involve identifying the root cause of the problem, proposing a strategy, outlining potential risks, or suggesting metrics for success.Explain what a successful solution would look like. Include both qualitative and quantitative measures. Mention how the solution will impact the company, its employees, and its customers. Specify any guidelines or constraints the candidate should consider. This could include budget limits, brand guidelines, regulatory requirements, etc. If applicable, include considerations unique to the role. For a marketing position, this might involve brand positioning; for a technical role, specific technologies or methodologies. Detail the criteria on which the candidate’s solution will be evaluated. This helps ensure that the candidate's focus aligns with what the role demands.}}

## Candidate Q&A

<thinking>Your thinking about this section</thinking>

{{ Candidate Q&A introduction }}

{% for i in range(6) %}
**Q. {{ candidateQuestions[i].question }}**

A. {{ candidateQuestions[i].answer }}

{% endfor %}

## Candidate Evaluation

Complete the following scorecard for the Infrastructure Software Engineer role at Y Combinator. Refer to the evaluation guides for 
each competency to determine the candidate's score.

| Competency | Rating (1-5) | Interviewer Comments |
| --- | --- | --- |
{% for competency in competencies %}
| {{ competency.name }} |   |   |
{% endfor %}
| &nbsp; | | |
| **Total** |   |   |