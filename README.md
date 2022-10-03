# node.js_patika_odev3
const http = require("http");

const server = http.createServer((req,res) => {
    const url = req.url;
    if(url === "/"){
        res.writeHead(200,{"Content-Type":"text/html"});
        res.write("<h1>index sayfasina hosgeldiniz</h1>");
    }else if(url === "/about"){
        res.writeHead(200,{"Content-Type":"text/html"});
        res.write("<h1>about sayfasina hosgeldiniz</h1>");
        
    }else if (url === "/contact"){
        res.writeHead(200,{"Content-Type":"text/html"});
        res.write("<h1>contact sayfasina hosgeldiniz</h1>");
      
    }else{
        res.writeHead(200,{"Content-Type":"text/html"});
        res.write("<h1>404 page not found</h1>");
        
    }
    
    res.end();
})

const port = 5000;
server.listen(port, ()=> {
    console.log(`sunucu port ${port}  da çalişti`);
})
