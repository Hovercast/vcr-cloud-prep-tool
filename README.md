~~~                                       ,,,                                      
                                ,,,,,,,,,,,,,,,,,                               
                           ,,,,,,,,,,,,,,,,,,,,,,,,,,                           
                       ,,,,,,,,,,,,           ,,,,,,,,,,,,                      
                   ,,,,,,,,,,,                    ,,,,,,,,,,,,                  
              .,,,,,,,,,,,                            .,,,,,,,,,,,              
          ,,,,,,,,,,,,               ,,,,,,                ,,,,,,,,,,,,         
      ,,,,,,,,,,,,               ,,,,,,,,,,,,,,,               ,,,,,,,,,,,,     
  ,,,,,,,,,,,                ,,,,,,,,,,,,,,,,,,,,,,,               .,,,,,,,,,,, 
 ,,,,,,,,               ,,,,,,,,,,,,         ,,,,,,,,,,,                ,,,,,,,,
,,,,,,              ,,,,,,,,,,,,,,,              ,,,,,,,,,,,,             ,,,,,,
 ,,,,,,,,,.     ,,,,,,,,,,,,,,,,,,,,,,,              ,,,,,,,,,,,,     ,,,,,,,,,,
   ,,,,,,,,,,,,,,,,,,,,      ,,,,,,,,.                    ,,,,,,,,,,,,,,,,,,,,  
       (,,,,,,,,,,,                            ,              ,,,,,,,,,,,(      
   ,,(((((((,,,,,,,,,,,,                   ,,,,,,,,,     .,,,,,,,,,,,((((((/,,  
 ,,,,,,,,*      ,,,,,,,,,,,,              ,,,,,,,,,,,,,,,,,,,,,,,     ,,,,,,,,,,
,,,,,,               ,,,,,,,,,,,              ,,,,,,,,,,,,,,               ,,,,,
 ,,,,,,,,                ,,,,,,,,,,,.       .,,,,,,,,,,,                ,,,,,,,,
  ,,,,,,,,,,,,               ,,,,,,,,,,,,,,,,,,,,,,,               ,,,,,,,,,,,. 
      ,,,,,,,,,,,,               .,,,,,,,,,,,,,.               ,,,,,,,,,,,,     
           ,,,,,,,,,,,                ,,,,,                ,,,,,,,,,,,          
               ,,,,,,,,,,,.                           ,,,,,,,,,,,,              
                   ,,,,,,,,,,,,                   ,,,,,,,,,,,,                  
                        ,,,,,,,,,,,           ,,,,,,,,,,,                       
                            ,,,,,,,,,,,,,,,,,,,,,,,,,                           
                                ,,,,,,,,,,,,,,,,,                               
                                       ,,,  

                           ~Hovercast VCR Prep Script~
~~~

### START HERE! Copy this code into Powershell (you may need to press enter at the end):
```
[Net.ServicePointManager]::SecurityProtocol = "tls12, tls11, tls" 
$ScriptWebArchive = "https://github.com/Hovercast/vcr-cloud-prep-tool/archive/master.zip"  
$LocalArchivePath = "$ENV:UserProfile\Downloads\vcr-cloud-prep-tool"  
(New-Object System.Net.WebClient).DownloadFile($ScriptWebArchive, "$LocalArchivePath.zip")  
Expand-Archive "$LocalArchivePath.zip" -DestinationPath $LocalArchivePath -Force  
CD $LocalArchivePath\vcr-cloud-prep-tool-master\ | powershell.exe .\HoverLoader.ps1  
```
