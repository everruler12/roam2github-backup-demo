- 23:12 - 23:52
    - Let's test mindmap via [[roam/css]]
        - Iteratons
            - Step 1
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fhelp%2FEmJhviA4Hg.png?alt=media&token=3293b5b8-2ec0-47e6-8a3d-31f6ab1b5f19)
                    - Result of 
                        - ```css
.mindmap {
  display: flex;
  align-items: center;
  flex-direction: row;
}
.mindmap .rm-block__input {
  border: 1px solid grey;
}
.mindmap > .rm-block__self {
  flex-grow: 0.1;
}
.mindmap .rm-block__children .rm-block__controls {
opacity: 1;
  position: relative;
}


.mindmap:hover .rm-block__children .rm-block__controls {
opacity: 1;
}

.mindmap:hover .rm-block__children .rm-block__controls {
opacity: 1;
}

.mindmap > .rm-block__children {
   flex-grow: 1;
  margin: 12px 4px;
  padding: 8px 0px;
  border-top: 1px solid green;
  border-bottom: 1px solid green;
  border-left: 1px solid green;
}``` [*](((WD92x3LBi)))
            - Step 2 [css](((WD92x3LBi)))
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fhelp%2F23f6pfr2jN.png?alt=media&token=2c02e69e-dcfb-421b-a892-eb2209eabcfa)
                    - Result of::
                        - ```javascript

.mindmap .block-expand  {
  opacity: 1;
  background-color: green;
  height: 4px;
  align-self: center;
  min-width: 80%;
  margin-left: -4px;
}```
                            - at:: 23:23
            - Step 3
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fhelp%2FFyJHFi6Qtg.png?alt=media&token=bbea05f3-c690-4d2e-af9b-4eb1e28461c3)
                    - Result of::
                        - ```css
.mindmap {
  overflow: scroll;
}

.mindmap .rm-block__children .rm-block {
  display: flex;
  align-items: center;
  flex-direction: row;
}
.mindmap .rm-block__children .rm-block__input {
  border: 1px solid grey;
  padding: 8px;
}
.mindmap .rm-block__children .rm-block__self {
  flex-grow: 0.1;
}
.mindmap .rm-block__children .rm-block__children .rm-block__controls {
opacity: 1;
  position: relative;
}


.mindmap:hover .rm-block__children .rm-block__controls {
opacity: 1;
}

.mindmap:hover .rm-block__children .rm-block__controls {
opacity: 1;
}


.mindmap .rm-block__children .block-expand  {
  opacity: 1;
  background-color: green;
  height: 4px;
  align-self: center;
  min-width: 80%;
  margin-left: -4px;
}

.mindmap .rm-block__children .rm-multibar {
  opacity: 0;
}
.mindmap .rm-block__children .rm-block__children {
   flex-grow: 1;
  margin: 12px 4px;
  padding: 8px 0px;
 
}``` [*](((WD92x3LBi)))
                        - 
                    - 23:34
            - Final Result for now
                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fhelp%2Fqm2mj8zA-d.png?alt=media&token=58fa05d1-6754-4333-85cc-b21b021659df)
                    - Result of::
                        -  ```css
.mindmap {
  overflow: scroll;
}

.mindmap .rm-block__children .rm-block {
  display: flex;
  align-items: center;
  flex-direction: row;
}
.mindmap .rm-block__children .rm-block__input {
  border-left: 1px solid grey;
  border-top: 1px solid grey;
  border-bottom: 1px solid grey;
  padding: 8px;
}
.mindmap .rm-block__children .rm-block__self {
  flex-grow: 0.1;
}
.mindmap .rm-block__children .rm-block__children .rm-block__controls {
opacity: 1;
  position: relative;
}


.mindmap:hover .rm-block__children .rm-block__controls {
opacity: 1;
}

.mindmap:hover .rm-block__children .rm-block__controls {
opacity: 1;
}


.mindmap .rm-block__children .rm-block__children .block-expand  {
  opacity: 1;
  background-color: green;
  height: 4px;
  align-self: center;
  min-width: 80%;
  margin-left: -4px;
}

.mindmap .rm-block__children .rm-block__children {
   flex-grow: 1;
  margin: 12px 4px;
  padding: 8px 0px;
 
}``` [*](((WD92x3LBi)))
        - Workspace 
            - test
                - 
                    - #.mindmap
                        - This is not going to be quite right
                            - A "C"
                                - B
                                - C
                                - C
                                    - D
                                    - "B"
                                        - E
                                        - {{[[embed]]: ((dr7PdJAjs))}}
                                            - 
            - Editor
                - {{[[embed]]: ((WD92x3LBi))}}
            - #.mindmap
                - test
                    - X
                        - Y
                        - Z
                            - 
        - Testing with an embedded page or block
        - {{[[video]]: https://www.loom.com/share/a49deee0d918461ba7c26208056c188c}}
            - #.mindmap
                - {{[[embed]]: [[Roam White Paper]]}}
                - {{[[embed]]: [[It's Time To Build]]}}
            - #.mindmap
                - {{embed: [[How can we develop transformative tools for thought?]]}}
            - #.mindmap
                - {{[[embed]]: ((LDz19VdCH))}} 
