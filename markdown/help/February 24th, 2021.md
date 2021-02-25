- [[Conor]]
    - 17:43 - 17:52
        - Proving that we can have a nested Table / Grid Structure using just [[roam/css]]
            - Steps::
                - For each of the cases 
                    - Decide what needs to be represented, and what each block represents
                - Create a basic table layout
                    - Options::
                        - Rows first - each block is a column below
                            - Screenshot
                                - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fhelp%2Fj6BhKA9GjD.png?alt=media&token=1720cc07-5d79-4271-bf9b-e83e8f441d2a)
                            - Example::  [[.conor-table]]
                                - Row 1
                                    - A #.a
                                        - B#.a
                                            - C #.a
                                                - D
                                                - E
                                - 
                                - Row 2  
                                    - A
                                        - B 
                                            - C
                                                - D 
                                                - This
                                -  
                                    -  
                                        -  
                                            - 
    - 17:52 - 18:09
        - Copy "Example::  [[.conor-table]]" and create some custom CSS to display this as a table
            - ![](https://firebasestorage.googleapis.com/v0/b/firescript-577a2.appspot.com/o/imgs%2Fapp%2Fhelp%2FRj_CdeqTdz.png?alt=media&token=83b88678-1856-4449-992e-941ab25b0c5d)
            - ```css
.conor-table .rm-block__children {
  display: contents;
  
}

.conor-table > .rm-block__children .rm-block {
  display: grid;
  grid-template-columns: repeat(6, 100px);
  grid-template-rows: 100px;
}

.conor-table {
  border: 2px solid grey;
  width: 50vw;
}

.conor-table .rm-block {
  border: 0.5px solid grey;
flex: 1 1 60px;
}``` [*](((wef_Hru74)))
            - 
    - 18:11 - 18:20
        - [[Adam]] is making the assertion that 
            - We are __Sacrificing__ a block in order to represent rows in a table - and that this is enough of a problem that we would have to have a schema change in order to use tables
                - Correction::
                    - He thinks you could not represent [this table](((djGTZ4M8o))) - without 
        - 18:19
            - {{[[drawing]]}}
            - {{[[drawing]]}}
            - 
- [[Adam]]
    - "Copy "Example::  [[.conor-table]]" and create some custom CSS to display this as a table"
