---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azcontextautosavesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzContextAutosaveSetting.md
ms.openlocfilehash: 193a1dab5bd08489740d0d95f65c6aad1ea85e43
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100167164"
---
# Get-AzContextAutosaveSetting

## SYNOPSIS
Anzeigen von Metadaten zum automatischen Speichern des Kontextfeatures, einschließlich Angaben dazu, ob der Kontext automatisch gespeichert wird und wo gespeicherte Kontext- und Anmeldeinformationen zu finden sind.

## SYNTAX

```
Get-AzContextAutosaveSetting [-Scope <ContextModificationScope>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Anzeigen von Metadaten zum automatischen Speichern des Kontextfeatures, einschließlich Angaben dazu, ob der Kontext automatisch gespeichert wird und wo gespeicherte Kontext- und Anmeldeinformationen zu finden sind.

## BEISPIELE

### Kontextspeichern von Metadaten für die aktuelle Sitzung
```
PS C:\> Get-AzContextAutosaveSetting

Mode             : Process
ContextDirectory : None
ContextFile      : None
CacheDirectory   : None
CacheFile        : None
Settings         : {}
```

Erfahren Sie mehr darüber, ob und wo der Kontext gespeichert wird.  Im vorstehenden Beispiel wurde das Feature "AutoAve" deaktiviert.

### Kontextspeichern von Metadaten für den aktuellen Benutzer
```
PS C:\> Get-AzContextAutosaveSetting -Scope CurrentUser

Mode             : CurrentUser
ContextDirectory : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
ContextFile      : AzureRmContext.json
CacheDirectory   : C:\Users\contoso\AppData\Roaming\Windows Azure Powershell
CacheFile        : TokenCache.dat
Settings         : {}
```

Erfahren Sie mehr darüber, ob und wo der Kontext für den aktuellen Benutzer standardmäßig gespeichert wird.  Beachten Sie, dass sich dies möglicherweise von den Einstellungen unterscheiden kann, die in der aktuellen Sitzung aktiv sind. Im vorstehenden Beispiel wurde das Feature "AutoSpeichern" aktiviert, und die Daten werden am Standardspeicherort gespeichert.

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -Scope
Bestimmt den Umfang von Kontextänderungen, z. B. ob Änderungen nur für den aktuellen Prozess oder für alle von diesem Benutzer gestarteten Sitzungen gelten.

```yaml
Type: Microsoft.Azure.Commands.Profile.Common.ContextModificationScope
Parameter Sets: (All)
Aliases:
Accepted values: Process, CurrentUser

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Common.Authentication.ContextAutosaveSettings

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
