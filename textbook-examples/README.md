# CSC405 Module 8 — Textbook Example Programs

Example code from Gordon, V. S., & Clevenger, J. (2021). Computer graphics programming in OpenGL with Java (3rd ed.). Mercury Learning and Information. Used for coursework study.

Official companion files were downloaded from the author’s page,
[Computer Graphics Programming in OpenGL with Java, 3rd Edition](https://athena.ecs.csus.edu/~gordonvs/textJ3E.html)
(`J3E_CompanionFiles.zip`). Each program folder is self-contained:
its `.java` sources, `.glsl` shaders, utility classes (`Utils.java`,
`Sphere.java`, `Torus.java`, `ImportedModel.java` as needed), and any
textures or models that program loads are copied into that folder.

**Assigned reading:** Chapter 2, Sections 2.1.5–2.1.7; Chapter 4, Sections 4.9 and 4.11.3; Chapter 8 (entire).

## Programs in this module

### Program8_1 — Shadow Mapping

- **Section:** 8.5 A Shadow Mapping Example
- **Official folder:** `Chapter_08_shadow/Prog8_1_shadowMapping`
- **Assets included:** `pyr.obj`

### Program8_2 — Percentage Closer Filtering (PCF)

- **Section:** 8.7.3 A Soft Shadow PCF Program
- **Official folder:** `Chapter_08_shadow/Prog8_2_softShadowsPCF`
- **Assets included:** `pyr.obj`

## Assigned sections without a numbered program

- Sections 2.1.5–2.1.7 (rasterization, fragment shader, pixel operations) are conceptual pipeline stages from Chapter 2. They have no unique numbered programs; Programs 2.1–2.2 in Module 1 introduce the pipeline as a whole.
- Sections 4.9 (Z-fighting) and 4.11.3 (back-face culling) have no numbered example programs. The book describes enabling glEnable(GL_CULL_FACE) / glCullFace(GL_BACK) and polygon-offset / depth settings as modifications, including adding back-face culling to Program 4.3 (in Module 5).
- Sections 8.1–8.4 and 8.6 develop the shadow-mapping algorithm and its artifacts, implemented in Programs 8.1 and 8.2.

## Compile and run

These programs use the official companion layout: Java sources and shaders live in a `code/` package (`package code;`), and textures or `.obj` models sit in the program folder (the working directory when you run). Shaders are loaded with paths such as `code/vertShader.glsl`.

You need **JDK 11**, **JOGL 2.4** (`jogl-all.jar`, `gluegen-rt.jar`, plus the native jars for your OS), and **JOML 1.10** (`joml-1.10.0.jar`) on the classpath. The textbook’s Appendix A (Windows) and Appendix B (macOS) cover installation. On Linux, put the jars in a `lib` directory (or any folder you prefer) and run the following from a program folder, for example `Program2_5`:

```bash
# Adjust these paths to where you keep the jars
CP="lib/jogl-all.jar:lib/jogl-all-natives-linux-amd64.jar:lib/gluegen-rt.jar:lib/gluegen-rt-natives-linux-amd64.jar:lib/joml-1.10.0.jar"

# Compile (from the program folder that contains the code/ directory)
javac -cp "$CP" code/*.java

# Run (also from that program folder, so shader and texture paths resolve)
java -cp "$CP:." \
  --add-exports java.base/java.lang=ALL-UNNAMED \
  --add-exports java.desktop/sun.awt=ALL-UNNAMED \
  --add-exports java.desktop/sun.java2d=ALL-UNNAMED \
  -Dsun.java2d.d3d=false -Dsun.java2d.uiScale=1 \
  code.Code
```

On Windows, use `;` instead of `:` in the classpath, and the official `compile.bat` / `run.bat` in each folder assume the JOGL and JOML jars are already on your global `CLASSPATH` (as the book’s setup appendix describes):

```bat
javac code/Code.java
java --add-exports java.base/java.lang=ALL-UNNAMED --add-exports java.desktop/sun.awt=ALL-UNNAMED --add-exports java.desktop/sun.java2d=ALL-UNNAMED -Dsun.java2d.d3d=false -Dsun.java2d.uiScale=1 code.Code
```

Programs that open a window need a display; compiling does not.


This `textbook-examples` folder contains **23** files.
