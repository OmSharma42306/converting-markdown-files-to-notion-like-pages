# Implemented this Like Exporting Markdown CSV from NOTION and Rendering Page on Website

## CODE :

 

```
    import { marked } from 'marked';
    import fs from "fs"
    const markdownFile = "./markdown/example.md";
    const outputHtml =  "./output/output.html"

    fs.readFile(markdownFile,'utf-8',(err,data) => {
        if(err) throw err;
        const htmlContent = marked(data);

        fs.writeFile(outputHtml,htmlContent,(err) => {
            if (err) throw err;
            console.log("Html file Created Successfully.")
        })
    })
```