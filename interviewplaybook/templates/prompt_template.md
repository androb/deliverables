--- 
title: Interview Guide for  {{ role }}
subtitle:  {{ company }}
author: Created by [Deliverables AI](https://github.com/androb/deliverables)
date: {{ today's date and time }}
--- 

# Interview Guide for {{ role }}

<!-- Your thinking about the guide -->

## About this Guide

<!-- Your thinking about this section -->

{{ About this guide in 4 paragraphs }}

## Job Description

{{ Job description provided by the user with the formatting cleaned up. Use bold for headings. }}

## Interview Agenda

<!-- your_thinking -->

{{ detailedInterviewAgendaAsMarkdown }}

## Competency Framework

<!-- your_thinking -->

{{ competencyFrameworkDescription }}

{% for competency in competencies %}
{{ loop.index }}. **{{ competency[0] }}**: {{ competency[1] }}

{% endfor %}

{% for competency in competencies %}

## Competency {{ loop.index }}. **{{ competency.title }}**

{{ competency.description }}

### Lead Question

**&ldquo;{{ competency.leadQuestion }}&rdquo;** {{ competency.leadQuestionFollowup1 }} {{ competency.leadQuestionFollowup2 }}

&nbsp;

&nbsp;

_{{ competency.leadQuestionWhatToLookFor }}__

### Situational Scenario

**&ldquo;{{ competency.detailedSituationalScenario }}&rdquo;**

&nbsp;

&nbsp;

_{{ competency.scenarioWhatToLookFor }}_

### Diving Deeper

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

## Case Study / Role Play

<!-- your_thinking -->

{{ Three paragraphs describing a case study for candidates to role play and how to evaluate them. }}

## Candidate Q&A

<!-- your_thinking -->

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