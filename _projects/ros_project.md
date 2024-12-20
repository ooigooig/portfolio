---
layout: page
title: ROS-based competition car
description: For an educational robotics company, we need to develop a ROS-based competition robot to meet the needs of existing university/college courses.
img: assets/img/ros/homepage.png
importance: 7

giscus_comments: true
---

In this project, the content is organized into five main sections: ROS basics and control, OpenCV, laser and depth cameras, deep learning and voice control, and model training for autonomous driving.

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ros/ros_workspace.png" title="ros_workspace" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    In this workspace, many packages implemented by ROS are listed in the screenshot.
</div>

**ROS basics and control**

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ros/move.png" title="move" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    command to control by keyboard.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ros/move_rqt_graph.png" title="move_rqt_graph" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    rqt_graph for checking the correlation of topic and node.
</div>


**OpenCV**

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ros/opencv_simpleflow.png" title="opencv_simpleflow" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    it can implement many open source samples of opencv.
</div>


<div class="row justify-content-sm-center">
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/azure/kcf_image.png" title="kcf_image" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        {% include figure.liquid path="assets/img/azure/kcf_env.png" title="kcf_env" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    KCF tracker is a fast and robust object tracking algorithm that uses kernelized correlation filters and the Discrete Fourier Transform to efficiently follow objects in video frames.
</div>

**Laser**
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ros/laser_init.png" title="laser_init" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    The Robotic car can 'feel' the world now.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ros/mapping.png" title="mapping" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    mapping and navigation are the basic of ROS.
</div>

**depth cameras**

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ros/camera_init.png" title="camera_init" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    link the camera in the ros through node.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ros/depth_cam.png" title="depth_cam" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    depth camera on the way.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ros/ar_track.png" title="ar_track" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    AR code is implemented in the Rviz environment.
</div>



**deep learning and voice control**

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ros/yolo.png" title="yolo" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    YOLO3 implemented in the car by depth cam.
</div>

<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.liquid loading="eager" path="assets/img/ros/gesture.png" title="gesture" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    trained by own datasets through yolo pre-trained model.
</div>


****