prima-core-libs
===============

Core libraries by the PRImA Research Lab

## Branches
* **[dev](https://github.com/maxnth/prima-core-libs/tree/dev)**

  dev branch for testing. Has the following branches merged
    * [feature/ComposedBlockType](https://github.com/maxnth/prima-core-libs/tree/feature/ComposedBlockType)
    * [feature/TextRegionTypeTags](https://github.com/maxnth/prima-core-libs/tree/feature/TextRegionTypeTags)
    * [feature/fontColor](https://github.com/maxnth/prima-core-libs/tree/feature/fontColor)
    * [feature/margins](https://github.com/maxnth/prima-core-libs/tree/feature/margins)
    * [stringMaps](https://github.com/maxnth/prima-core-libs/tree/stringMaps)
* **[feature/AdvancedTags](https://github.com/maxnth/prima-core-libs/tree/feature/AdvancedTags)**

  Experimental branch adding the LayoutTags proposed by [ALTO](https://altoxml.github.io/documentation/use-cases/tags/ALTO_tags_usecases.html)
* **[feature/ComposedBlockType](https://github.com/maxnth/prima-core-libs/tree/feature/ComposedBlockType)**

  Adds the PAGE XML region type to created ComposedBlockType-Elements (akin to IllustrationBlock-Elements)
* **[feature/TextRegionTypeTags](https://github.com/maxnth/prima-core-libs/tree/feature/TextRegionTypeTags)**

Adds OtherTag-Elements for PAGE XML text region types

* **[feature/fontColor](https://github.com/maxnth/prima-core-libs/tree/feature/fontColor)** 

Add support for converting textColour attributes to ALTO FONTCOLOR attributes

* **[feature/marginWOprintspace](https://github.com/maxnth/prima-core-libs/tree/feature/marginWOprintspace)**

Implements ALTO margin elements (TopMargin, BottomMargin, LeftMargin, RightMargin) for PAGE XML files without an explicitly specified PrintSpace-ELement. Builts on top of [feature/margins](https://github.com/maxnth/prima-core-libs/tree/feature/margins)

* **[feature/margins](https://github.com/maxnth/prima-core-libs/tree/feature/margins)**

ALTO margin elements (TopMargin, BottomMargin, LeftMargin, RightMargin) for PAGE XML files with an explicitly specified PrintSpace-ELement. Everything outside of the PrintSpace is considered to be inside the Margin. 

* **[stringMaps](https://github.com/maxnth/prima-core-libs/tree/stringMaps)**

Small code refactoring, replacing somewhat verbose if blocks (containing duplicates) with maps.
