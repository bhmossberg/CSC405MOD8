# CSC405MOD8

**CSC405 Computer Graphics, CSU Global (Winter 2026, Session A). Module 8: From Geometry to Pixels (Implementation and Rasterization)**

Painter's algorithm vs Z-buffer.

## Enabling Objectives

By the end of this module, you will be able to:

1. Describe basic implementation strategies.
2. Define the four major tasks.
3. Examine clipping.
4. Define rasterization.
5. Describe polygon rasterization.

## Readings

**Required**

- Gordon, V. S., & Clevenger, J. (2021). Computer graphics programming in OpenGL with Java (3rd ed.). Mercury Learning.
  - Chapter 2
    - Section 2.1.5: Rasterization
    - Section 2.1.6: Fragment Shader
    - Section 2.1.7: Pixel Operations
  - Chapter 4
    - Section 4.9: Combatting Z-Fighting Artifacts
    - Section 4.11.3: Back-Face Culling
  - Chapter 8: Shadows

**Recommended**

- Akenine-Möller, T., Haines, E., & Hoffman, N. (2022). Real-time rendering (4th ed.). A K Peters / CRC Press.
  - Chapter 23: Graphics Hardware — https://learning-oreilly-com.csuglobal.idm.oclc.org/library/view/real-time-rendering-fourth/9781351816144/xhtml/ch23.xhtml
- Fabre, J., Castillo, C., Rodriguez-Pardo, C., & Lopez-Moreno, J. (2026). Fast voxelization and level of detail for microgeometry rendering. The Visual Computer, 42(8), 311. https://arxiv.org/pdf/2604.13191

## Assignment: Module 8: Portfolio Project

Portfolio Project (200 Points)

The Portfolio Project has three parts:


### Part 1 — Milestone Updates (from Module 5)

Based on instructor feedback, update your Module 5 Interactive Viewer in Java with JOGL. Additionally, implement at least one advanced interactivity feature. Examples: allow users to select and highlight parts of a complex object using ray-picking; switch between displayed models; toggle between shaders; switch between perspective and orthographic projection; or load a model from disk using a small OBJ loader (Section 6.3 in the textbook). Submit the updated source files and screenshots with your final submission.


### Part 2 — Lessons Learned Reflection

Write a two-page reflection that discusses the key lessons you took from the course. Reflect on how these lessons apply to a real-world problem or specific real application (game engines, scientific visualization, AR/VR, data visualization, animation pipelines, etc.). How will you use the OpenGL concepts going forward?


### Part 3 — Final Program: Hidden-Surface Removal

Study the Hidden-Surface Removal problem in Section 4.9 (“Combating Z-Fighting Artifacts”) and Section 4.11.3 (“Back-Face Culling”) of Gordon & Clevenger (2021). Then implement the Painter’s Algorithm in Java with JOGL — sort your scene’s polygons back-to-front along the view axis each frame and render in that order, with the OpenGL depth test disabled. Compare the output to the same scene rendered with the depth test enabled (the Z-buffer algorithm). Discuss in one paragraph how Painter’s algorithm and the Z-buffer algorithm differ, and the cases in which Painter’s algorithm fails (intersecting polygons, cyclical occlusion).


### Submission Guidelines

Provide a 2 paragraph program overview, including:

Description of the primitives you used.

Screenshots of your working program (both Painter’s and Z-buffer side by side).

Adequate inline comments in your source code.

Your paper must be formatted according to APA guidelines in the CSU Global Writing Center (available in the left-hand navigation panel).

Assemble all of the requirements into a single ZIP file before submission.

Refer to the rubric below for more details about how you will be graded for this assignment.

As a reminder, there are no late submissions for Module 8 - everything must be submitted by the last day of the term.

