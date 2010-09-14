# Apache Camel WebSite and Docs

This project creates the website for [Apache Camel](http://camel.apache.org/) and the HTML documentation using [Scalate](http://scalate.fusesource.com/). 

See [how the site works](http://scalate.fusesource.org/versions/snapshot/documentation/siteGen.html) along with how to [export Confluence](http://scalate.fusesource.org/versions/snapshot/documentation/siteGen.html#bootstrapping).

## Editing the live site

To edit templates and wiki files live on your computer and see the results immediately in your browser try

    mvn jetty:run
    open http://localhost:8080/    
    
As you hit save after editing a template, wiki file or a layout (which by default is in [src/main/webapp/WEB-INF/scalate/layouts/default.scaml](tree/master/src/main/webapp/WEB-INF/scalate/layouts/default.scaml)) you should be able to hit reload on the browser.

To avoid having to hit reload on the browser you can try [LiveReload](http://scalate.fusesource.org/versions/snapshot/documentation/siteGen.html#livereload) 

## Generating the static site

    mvn scalate:sitegen
    open target/sitegen/index.html
    
To deploy (if you [setup your maven project to deploy](http://scalate.fusesource.org/versions/snapshot/documentation/siteGen.html#deploy))

    mvn deploy
    
    