# Contributing

These tutorials are built by the OpenSceneGraph community. To contribute please read the following instructions:

Each tutorial should have its own folder, which contain the tutorial text in written in markup as well as the full compilable source code and CMakeList file. 
From the main document in the root folder there should be a link to the markup file in the tutorial folder:


## Markup

These tutorials uses [Markdeep](https://casual-effects.com/markdeep) as its format. The motivation for using this format is its superiour source code formatting compared to standard GitHub markdown. More information regarding the Markdeep formatting can be found here: [Markdeep feature demo](https://casual-effects.com/markdeep/features.md.html)

## Template documents

There is a folder named *tutorial_template* containing both template markup file as well as template CMake file. Please use these as a base for any new tutorials.

[Tutorial template](tutorial_template/tutorial_template.md.html)


## CMake

These tutorials uses CMake for generating build files, just as OpenSceneGraph it self. 

## Source code

Source code should be written in C++98 for maximum compiler compability. The code should be indented with 4 spaces (not tabs), to conform with the style of OpenSceneGraph.

Any models or textures used in the tutorials should be available in the OpenSceneGraph-Data repository.

## License

By committing code and/or tutorials to this repository you agree to publish these under the MIT license (for source code) and Creative Commons Attribution 4.0 International (for tutorial text).

