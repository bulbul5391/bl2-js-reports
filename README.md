# bl2-js-report

<p align="center"><img src="https://bdprescription.com/npm-package/01.svg" height="200px" align="center" alt="JS Beautifier"></p>

<p align="center">💞️💞️💞️ BL2 JS REPORT 💞️💞️💞️</p>
<p align="center"><a href="#">
    <img alt="Join the chat" src="https://bdprescription.com/npm-package/JoinChat.svg"></a>
    <a href="https://www.linkedin.com/in/bulbulsarker/" target="_blank">
    <img alt="Linkedin Follow" src="https://bdprescription.com/npm-package/linkedins.svg">
  </a>
</p>  
<p align="center"><a href="#" target="_blank"><img alt="NPM stats" src="https://bdprescription.com/npm-package/install-01.png"></a></p>
  
## Installation

```
npm i bl2-js-report
```

## Uninstall

```
npm uninstall bl2-js-report
```

## 💞️ Basic Usage

## Add line in component file
```
import * as bl2Js from 'bl2-js-report';
```

## In html page
```
<button (click)="downloadPdf()" type="button">Download PDF</button>
```

## In js or ts file
```
downloadPdf() {
        this.data['fileName'] = 'save-file-name';
        this.data['templateName'] = 'ti-reports/Researcher-Profile-Information'; //file path       
        this.data['data'] = JSON.stringify(this.data);
        this.data['userDetails'] = JSON.stringify(this.userData);
        this.data['isInstitutional'] = JSON.stringify(this.isInstitutional);
        this.data['name'] = JSON.stringify(this.name);

        //Optional
        this.data['view'] = 0; // 0 = false or 1 = true
        this.data['print_r'] = 0; // 0 = false or 1 = true
        let actionUrl = `${reportBackend}/pdf-generate-post`;
        bl2Js(this.data, actionUrl);
    }
```