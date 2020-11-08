---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: D866554F-78B0-4691-BA06-F625F9B0DFC8
online version: ''
schema: 2.0.0
ms.openlocfilehash: 366941504c020910735015e3d8b282af376d54d9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006083"
---
# Publish-AzureWebsiteProject

## Synopsis
Veröffentlichen eines Visual Studio-Webprojekts auf einer Microsoft Azure-Website mithilfe von WebDeploy

## Syntax

### ProjectFile
```
Publish-AzureWebsiteProject -ProjectFile <String> [-Configuration <String>] [-ConnectionString <Hashtable>]
 [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### Paket
```
Publish-AzureWebsiteProject -Package <String> [-ConnectionString <Hashtable>] [-Tokens <String>]
 [-SetParametersFile <String>] [-SkipAppData] [-DoNotDelete] [-Name <String>] [-Slot <String>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Beschreibung
Veröffentlichen eines Visual Studio-Webprojekts auf einer Microsoft Azure-Website mithilfe von WebDeploy
Sie kann entweder ein WebDeploy-Paket übernehmen und direkt veröffentlichen, oder Sie können ein Visual Studio-Webprojekt erstellen, das Projekt erstellen und veröffentlichen.
Außerdem können die Verbindungszeichenfolgen im Web.config während der Veröffentlichung ersetzt werden.

## Beispiele

### Beispiel 1
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -Configuration Debug
```

Erstellen Sie ein Visual Studio-Webprojekt mit der Konfiguration "Debuggen" (Bedeutung verwenden Sie Web.Debug.config), und veröffentlichen Sie auf einer Microsoft Azure-Website mithilfe von WebDeploy.

### Beispiel 2
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1.zip
```

Veröffentlichen Sie eine ZIP-Datei für WebDeploy-Pakete auf einer Microsoft Azure-Website mit WebDeploy.

### Beispiel 3
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -Package .\WebApplication1
```

Veröffentlichen eines WebDeploy-Paketordners auf einer Microsoft Azure-Website mithilfe von WebDeploy

### Beispiel 4
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -ConnectionString @{ DefaultConnection = "my connection string" }
```

Erstellen Sie ein Visual Studio-Webprojekt, überschreiben Sie die Verbindungszeichenfolge "DefaultConnection" in Web.config, und veröffentlichen Sie Sie mithilfe von WebDeploy auf einer Microsoft Azure-Website.

### Beispiel 5
```
PS C:\> Publish-AzureWebsiteProject -Name site1 -ProjectFile .\WebApplication1.csproj -DefaultConnection "my connection string"
```

Erstellen Sie ein Visual Studio-Webprojekt, überschreiben Sie die Verbindungszeichenfolge "DefaultConnection" in Web.config, und veröffentlichen Sie Sie mithilfe von WebDeploy auf einer Microsoft Azure-Website.
Beachten Sie, dass-DefaultConnection ein dynamischer Parameter ist, der durch Analyse Web.config hinzugefügt wird.

## Parameter

### -Konfiguration
Die Konfiguration, die zum Erstellen des Visual Studio-Webanwendungsprojekts verwendet wird.

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConnectionString
Die für die Bereitstellung zu verwendenden Verbindungszeichenfolgen.

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DoNotDelete
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name der Website.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Paket
Der WebDeploy-Paketordner für die ZIP-Datei des Visual Studio-Webanwendungsprojekts, das veröffentlicht werden soll.

```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Profil
Gibt das Azure-Profil an, von dem dieses Cmdlet liest.
Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Projectdatei
Das zu veröffentlichende Visual Studio-Webanwendungsprojekt.

```yaml
Type: String
Parameter Sets: ProjectFile
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Setparameterdatei
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SkipAppData
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Der Name des Website Steckplatzes.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tokens
```yaml
Type: String
Parameter Sets: Package
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureWebsite](./Get-AzureWebsite.md)

[Neu – AzureWebsite](./New-AzureWebsite.md)

[Remove-AzureWebsite](./Remove-AzureWebsite.md)

[Satz-AzureWebsite](./Set-AzureWebsite.md)


