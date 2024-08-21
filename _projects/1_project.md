---
layout: page
title: TTC - Hackathon
description: to solve the problem of assaulting operators and user experience.
img: assets/img/ttc-hackathon/ttchomepage.png
importance: 1
category: study 
giscus_comments: true
---
What we do: My team of six participated in a TTC hackathon, where the main task was to design a system and solution to address driver assaults and enhance the TTC user experience. During the competition, we interviewed TTC bus drivers about issues related to assaults in order to develop a solution for driver safety. For the user experience design, since I lost my laptop on a TTC bus a week before the event and discovered that TTC lacked an official lost-and-found process, we decided to address this problem.

How we do: We designed a system based on the Presto card, including an assault detection system and an official forum for users. In the assault detection system, when a passenger taps their Presto card, their photo is captured by a camera. If the passenger assaults the driver, the driver can press a button to trigger an emergency alert, allowing the police to track the vehicle using its location and TTC vehicle number. The official user forum includes a lost-and-found system that provides information about passenger rides. Within three hours of the ride (to prevent disturbance calls from affecting the driver’s operation), users can contact the specific vehicle. For example, I lost my laptop on TTC bus number 3422 last time.

    ---
    Technical requirements:
    1.Familiar with MERN(MongoDB,Express,React,Node.js)
    2.Familiar with Bootstrap.（design an passenger app and driver app）
    3.Familiar with Web API.
    4.Investigate with some passengers and TTC drivers.
    5.Knowledge of Git/GitHub
    ---

# Passenger Forum
If passengers want to immediately retrieve their lost items, they can use this web app to get in contact with drivers.
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/ttc-hackathon/ttchomepage.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    This screenshot is TTC passenger lost and found system, which has several functions, such as user information and fourm. In terms of user information, passengers tap the presto and the bus will be recorded, including bus number, bus contact phone number etc.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/ttc-hackathon/travel_record.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Within 3 hours(this is for preventing scam phone calls), passengers can contact with driver to get their lost items. Also, as we can see in the screenshot, it would show time remaining(time for you to contact drivers), bus number, bus contact phone number, and when did you get in bus.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/ttc-hackathon/signin1.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/ttc-hackathon/signin2.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    It is Sign in page.
</div>

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/ttc-hackathon/signup.png" title="example image" class="img-fluid rounded z-depth-1" %}
    </div>
</div>

<div class="caption">
    Sign up page, passenger should sign up the same email as presto card email, so that the information in presto will upload in the app automatically.
</div>

# driver system

This system is the one next to the driver's seat. He can use this brand new system to prevent passengers from assaulting him.

continuing...