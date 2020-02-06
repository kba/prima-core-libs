prima-core-libs
===============

Core libraries by the PRImA Research Lab

## Branches
* **master**

Same codebase as [PRImA-Research-Lab:master](https://github.com/PRImA-Research-Lab/prima-core-libs). 

* **[dev](https://github.com/maxnth/prima-core-libs/tree/dev)**

  dev branch for testing. Has the following branches merged
    * [feature/ComposedBlockType](https://github.com/maxnth/prima-core-libs/tree/feature/ComposedBlockType)
    * [feature/TextRegionTypeTags](https://github.com/maxnth/prima-core-libs/tree/feature/TextRegionTypeTags)
    * [feature/fontColor](https://github.com/maxnth/prima-core-libs/tree/feature/fontColor)
    * [feature/margins](https://github.com/maxnth/prima-core-libs/tree/feature/margins)
    * [stringMaps](https://github.com/maxnth/prima-core-libs/tree/stringMaps)
* **[feature/AdvancedTags](https://github.com/maxnth/prima-core-libs/tree/feature/AdvancedTags)**

  Experimental branch adding the LayoutTags proposed by [ALTO](https://altoxml.github.io/documentation/use-cases/tags/ALTO_tags_usecases.html
  
  Example: 
  ```xml
      …
      <Tags>
        <LayoutTag ID="tag1" LABEL="Image"/>
        <LayoutTag ID="tag2" LABEL="Table"/>
        <LayoutTag ID="tag3" LABEL="Map"/> 
      </Tags>
      …
      <Illustration HEIGHT="36" HPOS="719" ID="r_0_1" TAGREFS="tag1" TYPE="ImageRegion"
          VPOS="427" WIDTH="52">
          <Shape>
              <Polygon POINTS="719,427 770,427 770,462 719,462"/>
          </Shape>
      </Illustration>
      <Illustration HEIGHT="50" HPOS="719" ID="r_0_1" TAGREFS="tag1" TYPE="ImageRegion"
          VPOS="427" WIDTH="52">
          <Shape>
              <Polygon POINTS="719,427 770,427 770,462 719,462"/>
          </Shape>
      </Illustration>
      …
      <ComposedBlock HEIGHT="86" HPOS="25" ID="r_200" TAGREFS="tag2" TYPE="TableRegion"
                  VPOS="475" WIDTH="376">
          <Shape>
              <Polygon POINTS="25,475 25,560 400,560 400,475"/>
          </Shape>
          <TextBlock HEIGHT="86" HPOS="25" ID="r_200_1" VPOS="475" WIDTH="376">
          …
      </ComposedBlock>
     …
    <Illustration HEIGHT="80" HPOS="719" ID="r_0_1" TAGREFS="tag3" TYPE="MapRegion"
          VPOS="427" WIDTH="52">
          <Shape>
              <Polygon POINTS="719,427 770,427 770,462 719,462"/>
          </Shape>
      </Illustration>
    …    
  ```
  
* **[feature/ComposedBlockType](https://github.com/maxnth/prima-core-libs/tree/feature/ComposedBlockType)**

  Adds the PAGE XML region type to created ComposedBlockType-Elements (akin to IllustrationBlock-Elements)
  
  Example:
  ```xml
      <ComposedBlock HEIGHT="86" HPOS="25" ID="r_200" TAGREFS="tag2" TYPE="TableRegion"
                  VPOS="475" WIDTH="376">
          <Shape>
              <Polygon POINTS="25,475 25,560 400,560 400,475"/>
          </Shape>
          <TextBlock HEIGHT="86" HPOS="25" ID="r_200_1" VPOS="475" WIDTH="376">
          …
      </ComposedBlock>
  ```
* **[feature/TextRegionTypeTags](https://github.com/maxnth/prima-core-libs/tree/feature/TextRegionTypeTags)**

Adds OtherTag-Elements for PAGE XML text region types

  Example:
  ```xml
       …
       <Tags>
          <OtherTag DESCRIPTION="PAGE XML text region type" ID="tag1" LABEL="page-number"/>
          <OtherTag DESCRIPTION="PAGE XML text region type" ID="tag2" LABEL="header"/>
      </Tags>
      …
      <TextBlock HEIGHT="36" HPOS="719" ID="r_1_1" TAGREFS="tag1" VPOS="427" WIDTH="52">
              <Shape>
                  <Polygon POINTS="719,427 770,427 770,462 719,462"/>
              </Shape>
              <TextLine HEIGHT="34" HPOS="720" ID="tl_1_1" LANG="de" STYLEREFS="ts1"
                  VPOS="428" WIDTH="50">
                  <Shape>
                      <Polygon POINTS="720,428 769,428 769,461 720,461"/>
                  </Shape>
                  <String CONTENT="26" HEIGHT="34" HPOS="720" ID="w_w1aab1b1b2b1b1ab1"
                      LANG="de" STYLEREFS="ts2" VPOS="428" WIDTH="50">
                      <Shape>
                          <Polygon POINTS="720,428 769,428 769,461 720,461"/>
                      </Shape>
                  </String>
              </TextLine>
          </TextBlock>
        …
        <TextBlock HEIGHT="33" HPOS="1044" ID="r_2_1" IDNEXT="r_4_1" TAGREFS="tag2"
            VPOS="442" WIDTH="228">
            <Shape>
                <Polygon POINTS="1044,442 1271,442 1271,474 1044,474"/>
            </Shape>
            <TextLine HEIGHT="31" HPOS="1045" ID="tl_2" LANG="de" STYLEREFS="ts3" VPOS="443"
                WIDTH="226">
                <Shape>
                    <Polygon POINTS="1045,443 1270,443 1270,473 1045,473"/>
                </Shape>
                <String CONTENT="II." HEIGHT="26" HPOS="1045" ID="w_w1aab1b3b2b1b1ab1"
                    LANG="de" STYLEREFS="ts3" VPOS="448" WIDTH="40">
                    <Shape>
                        <Polygon POINTS="1045,448 1084,448 1084,473 1045,473"/>
                    </Shape>
                </String>
                <String CONTENT="Abschnitt." HEIGHT="30" HPOS="1103"
                    ID="w_w1aab1b3b2b1b1ab9" LANG="de" STYLEREFS="ts3" VPOS="443"
                    WIDTH="168">
                    <Shape>
                        <Polygon POINTS="1103,443 1270,443 1270,472 1103,472"/>
                    </Shape>
                </String>
            </TextLine>
        </TextBlock>
        …
  ```

* **[feature/fontColor](https://github.com/maxnth/prima-core-libs/tree/feature/fontColor)** 

  Add support for converting textColour attributes to ALTO FONTCOLOR attributes

  Example:

  PAGEXML
  ```xml
        …
        <TextStyle textColour="red" fontFamily="Times New Roman" fontSize="8.5"/>
        …
  ```
  ALTO
  ```xml
        …
        <Styles>
          …
          <TextStyle FONTCOLOR="ff0000" FONTFAMILY="Times New Roman" FONTSIZE="8.5" ID="ts3"/>
          …
  ```

* **[feature/marginWOprintspace](https://github.com/maxnth/prima-core-libs/tree/feature/marginWOprintspace)**

  Implements ALTO margin elements (TopMargin, BottomMargin, LeftMargin, RightMargin) for PAGE XML files without an explicitly specified PrintSpace-ELement. Builts on top of [feature/margins](https://github.com/maxnth/prima-core-libs/tree/feature/margins)

* **[feature/margins](https://github.com/maxnth/prima-core-libs/tree/feature/margins)**

  ALTO margin elements (TopMargin, BottomMargin, LeftMargin, RightMargin) for PAGE XML files with an explicitly specified PrintSpace-ELement. Everything outside of the PrintSpace is considered to be inside the Margin. 

  Example:
  ```xml
  …
  <Page HEIGHT="2686" ID="p0" PAGECLASS="content" PHYSICAL_IMG_NR="0" WIDTH="1700">
      <TopMargin HEIGHT="376" HPOS="0" ID="TopMarginTypeID0" VPOS="0" WIDTH="1700"/>
      <LeftMargin HEIGHT="1772" HPOS="0" ID="LeftMarginTypeID0" VPOS="376" WIDTH="630"/>
      <RightMargin HEIGHT="1772" HPOS="1699" ID="RightMarginTypeID0" VPOS="376" WIDTH="3"/>
      <BottomMargin HEIGHT="538" HPOS="0" ID="BottomMarginTypeID0" VPOS="2148" WIDTH="1700"/>
      <PrintSpace HEIGHT="1772" HPOS="630" ID="PageSpaceTypeID0" VPOS="376" WIDTH="1071">
          <Shape>
              <Polygon POINTS="630,376 1700,376 1700,2147 630,2147"/>
          </Shape>
        …
  ```

* **[stringMaps](https://github.com/maxnth/prima-core-libs/tree/stringMaps)**

  Small code refactoring, replacing somewhat verbose if blocks (containing duplicates) with maps.
