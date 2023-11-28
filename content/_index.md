---
# Leave the homepage title empty to use the site title
title:
date: 2022-10-24
type: landing

sections:
  - block: about.biography
    id: about
    content:
      title: Biography
      # Choose a user profile to display (a folder name within `content/authors/`)
      username: admin
  - block: features
    content:
      title: Skills
      items:
        - name: Software Development
          description: C++/C/Python, ROS, Simscape/Raisim/Mujoco, Pinocchio/OCS2/Acados/OSQP
          icon: laptop-code
          icon_pack: fas
        - name: Robotics & Control
          description: Kinematics, Dynamics, DCM, HZD, WBC, TSID, PID, LQR, MPC, TrajOpt, CLF
          icon: robot
          icon_pack: fas
        - name: Mechanical Design
          description: Solidworks, Ansys, VSA
          icon: gears
          icon_pack: fas
  - block: experience
    content:
      title: Experience
      # Date format for experience
      #   Refer to https://wowchemy.com/docs/customization/#date-format
      date_format: Jan 2006
      # Experiences.
      #   Add/remove as many `experience` items below as you like.
      #   Required fields are `title`, `company`, and `date_start`.
      #   Leave `date_end` empty if it's your current employer.
      #   Begin multi-line descriptions with YAML's `|2-` multi-line prefix.
      items:
        - title: Research Engineer
          company: ARX Robotics (Beijing) Co. Ltd.
          company_url: ''
          company_logo: arx
          location: Beijing, China
          date_start: '2023-06-01'
          date_end: ''
          description: |2-
              Controller design and hardware implementation of a miniature bipedal robot (ARX-6M)
        - title: Research Intern (Core member)
          company: DISCOVER Lab (Prof. Guyue Zhou), Institute for AI Industry Research (AIR), Tsinghua University
          company_url: 'https://air.tsinghua.edu.cn/en/info/1046/1196.htm'
          company_logo: air
          location: Beijing, China
          date_start: '2022-05-01'
          date_end: '2022-12-01'
          description: |2-
              * Lightweight asynchronous multi-threading modularized software system for robotic control usage
              * Controller development of a bipedal robot based on: HZD offline gait library / NMPC online footstep adaptation
        - title: Undergraduate Researcher
          company: Robotics Laboratory (Prof. Yuqing Chen), Xi'an Jiaotong-Liverpool University
          company_url: 'https://www.xjtlu.edu.cn/en/staff-details/staff/yuqing-chen'
          company_logo: xjtlu
          location: Suzhou, China
          date_start: '2021-04-01'
          date_end: '2023-03-01'
          description: |2-
              * Optimal control algorithm implementation
              * Robot hardware design and control
              * Variable stiffness actuator (VSA) design
        - title: Electronic Control Group Tech Leader
          company: XJTLU DJI RoboMaster Team (Prof. Chun Zhao & Prof Quan Zhang), GMaster
          company_url: ''
          company_logo: gmaster
          location: Suzhou, China
          date_start: '2019-09-01'
          date_end: '2021-09-01'
          description: |2-
            * Responsible for the motor controller quality in the competition
            * Vision servo system development
    design:
      columns: '1'
  - block: portfolio
    id: projects
    content:
      title: Projects
      filters:
        folders:
          - project
      # Default filter index (e.g. 0 corresponds to the first `filter_button` instance below).
      default_button_index: 0
      # Filter toolbar (optional).
      # Add or remove as many filters (`filter_button` instances) as you like.
      # To show all items, set `tag` to "*".
      # To filter by a specific tag, set `tag` to an existing tag name.
      # To remove the toolbar, delete the entire `filter_button` block.
      buttons:
        - name: All
          tag: '*'
        - name: Robots
          tag: RO
        - name: Optimal Control
          tag: OC
        - name: Mechanical Design
          tag: MD  
    design:
      # Choose how many columns the section has. Valid values: '1' or '2'.
      columns: '2'
      view: masonry
      # For Showcase view, flip alternate rows?
      flip_alt_rows: false
  - block: collection
    id: pubs
    content:
      title: Publications
      filters:
        folders:
          - publication
        exclude_featured: true
    design:
      columns: '2'
      view: citation
---
