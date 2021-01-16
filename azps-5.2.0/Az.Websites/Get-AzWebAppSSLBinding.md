---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: EE3D2BA0-32E7-4A37-BCAF-F0E8FAAC43CE
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppSSLBinding.md
ms.openlocfilehash: aaecb97932ffbd2d7f5a03e4eedebd47719c5b4f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371928"
---
# Get-AzWebAppSSLBinding

## SYNOPSIS
Ruft eine Azure Web App-Zertifikat-SSL-Bindung ab.

## SYNTAX

### S1
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-ResourceGroupName] <String> [-WebAppName] <String>
 [[-Slot] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### S2
```
Get-AzWebAppSSLBinding [[-Name] <String>] [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzWebAppSSLBinding"** ruft eine Secure Sockets Layer (SSL)-Bindung für eine Azure Web App ab.
SSL-Bindungen werden verwendet, um eine Web App einem hochgeladenen Zertifikat zuzuordnen.
Web Apps können an mehrere Zertifikate gebunden werden.

## BEISPIELE

### Beispiel 1: Erhalten von SSL-Bindungen für eine Web App
```
PS C:\>Get-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp"
```

Mit diesem Befehl werden die SSL-Bindungen für die Web App ContosoWebApp abgerufen, die der Ressourcengruppe "ContosoResourceGroup" zugeordnet ist.

### Beispiel 2: Verwenden eines Objektverweises zum Erhalten von SSL-Bindungen für eine Web App
```
PS C:\>$WebApp = Get-AzWebApp -Name "ContosoWebApp"
PS C:\> Get-AzWebAppSSLBinding -WebApp $WebApp
```

Die Befehle in diesem Beispiel erhalten auch die #A0 für die Web App ContosoWebApp. In diesem Fall wird jedoch anstelle des Web -App-Namens und des Namens der zugeordneten Ressourcengruppe ein Objektverweis verwendet.
Dieser Objektverweis wird durch den ersten Befehl im Beispiel erstellt, der **"Get-AzWebApp"** verwendet, um einen Objektverweis auf die Web App namens "ContosoWebApp" zu erstellen.
Dieser Objektverweis wird in einer Variablen mit dem Namen $WebApp.
Diese Variable und das **Cmdlet "Get-AzWebAppSSLBinding"** werden dann vom zweiten Befehl verwendet, um die SSL-Bindungen zu erhalten.

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen der SSL-Bindung an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, der das Zertifikat zugewiesen ist.
Sie können den Parameter *"ResourceGroupName"* und den Parameter *"WebApp" nicht* in demselben Befehl verwenden.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Slot
Gibt einen Bereitstellungsplatz für Web App an.
Um einen Bereitstellungsplatz zu erhalten, verwenden Sie das Get-AzWebAppSlot Cmdlet.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WebApp
Gibt eine Web App an.
Um eine Web App zu erhalten, verwenden Sie das Get-AzWebApp-Cmdlet.

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -WebAppName
Gibt den Namen der Web App an, aus der dieses Cmdlet SSL-Bindungen erhält.
Sie können den Parameter *"WebAppName"* und den Parameter *"WebApp"* nicht im gleichen Befehl verwenden.

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.WebApps.Models.PSSite

## AUSGABEN

### Microsoft.Azure.Management.WebSites.Models.HostNameSslState

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzWebAppSSLBinding](./New-AzWebAppSSLBinding.md)

[Remove-AzWebAppSSLBinding](./Remove-AzWebAppSSLBinding.md)

[Get-AzWebApp](./Get-AzWebApp.md)


