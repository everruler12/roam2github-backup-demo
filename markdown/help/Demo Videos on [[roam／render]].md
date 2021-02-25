- Basic Setup - and the templates to help you that you can copy over from help db
    - {{[[video]]: https://www.loom.com/share/19d190d5a1054669bf681e50d09e6b0d}}
    - Steps::
        - Hello World
            - [[roam/render]] Hello World #[[roam/templates]]
                - {{roam/render: ((7kVYGbMR2))}} 
                    - ```clojure
(defn my-component []
  [:h1 {:on-click #(js/alert "Hello World")} "Hello World"]
  )```
        - Counter with a local variable
            - [[roam/render]] Namespaces and useful functions #[[roam/templates]]
                - {{roam/render: ((l0AwfXNWX))}} 
                    - ```clojure
(ns starting-point-for-custom-roam
  (:require
   [reagent.core :as r]
   [datascript.core :as d]
   [roam.datascript.reactive :as dr]))```
                    - ```clojure
(defn counter [_]
  (let [*count (r/atom 1)]
    (fn [_]
      [:button
       {:draggable true
        :on-click (fn [evt] (swap! *count inc))}
       @*count])))```
        - # Accessing Roam Data
            - {{roam/render: ((kWQSWD-zX))}}
                - ```clojure
(ns starting-point-for-custom-roam
  (:require
   [reagent.core :as r]
   [datascript.core :as d]
   [roam.datascript.reactive :as dr]))```
                - ```clojure


(defn input-thing [x]
   [:div 	
   [:input {:value @x
              :on-change 
      (fn [e] 
         (reset! x (.. e -target -value)))}]
             ]
          )
```
                - ```clojure
(defn counter [_]
  (let [*count (r/atom 1)
        x (r/atom "TODO")]
    (fn [_]
      [:div 
       [input-thing x]
       (pr-str @x)
      [:button
       {:draggable true
        :on-click (fn [evt] (swap! *count inc))}
       @*count]])))```
