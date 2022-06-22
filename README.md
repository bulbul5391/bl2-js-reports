# bl2-js-reports

<p align="center"><img src="https://bdprescription.com/npm-package/01.svg" height="200px" align="center" alt="JS Beautifier"></p>

<p align="center">💞️💞️💞️ BL2 JS REPORT 💞️💞️💞️</p>
<p align="center"><a href="#">
    <img alt="Join the chat" src="https://bdprescription.com/npm-package/JoinChat.svg"></a>
    <a href="https://www.linkedin.com/in/bulbulsarker/" target="_blank">
    <img alt="Linkedin Follow" src="linkedin.svg" style="height: 13px; border: 1px solid #878ae5; padding: 3px; border-radius: 4px; ">
  </a>
</p>  
<p align="center"><a href="https://www.npmjs.org/package/js-beautify" target="_blank"><img alt="NPM stats" src="install.png"></a></p>
  
  ## Installation

  ```
npm i bl2-js-reports
```

## 💞️ Basic Usage

## Add line in component file
```
import * as bl2Js from 'bl2-js-reports';
```

## In html page
```
<button (click)="downloadPdf()" type="button">Download PDF</button>
```

## In js or ts file
```
downloadPdf($fileName = '') {
        this.data['fileName'] = $fileName;
        this.data['templateName'] = 'ti-reports/Researcher-Profile-Information';
        this.data['lng'] = localStorage.getItem("currentLang");
        this.data['data'] = JSON.stringify(this.data);
        this.data['userDetails'] = JSON.stringify(this.userData);
        this.data['isInstitutional'] = JSON.stringify(this.isInstitutional);
        this.data['name'] = JSON.stringify(this.name);
        let actionUrl = `${reportBackend}/pdf-generate-post`;
        bl2Js(this.data, actionUrl);
    }
```