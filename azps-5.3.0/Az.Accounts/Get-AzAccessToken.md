---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 696ae59cb5115181605b7e6e647e2eb7d2792fd8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471593"
---
# Get-AzAccessToken

## SYNOPSIS
Erhalten Sie das Token für den unformatierte Zugriff. Stellen Sie bei Verwendung von "-ResourceUrl" sicher, dass der Wert mit der aktuellen Azure-Umgebung übereinstimmen soll. Sie können auf den Wert von `(Get-AzContext).Environment` verweisen.

## SYNTAX

### KnownResourceTypeName (Standard)
```
Get-AzAccessToken [-ResourceTypeName <String>] [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### ResourceUrl
```
Get-AzAccessToken -ResourceUrl <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Zugriffstoken erhalten

## BEISPIELE

### Beispiel 1: Token für den unformatierte Zugriff für den ARM erhalten
```powershell
PS C:\> Get-AzAccessToken
```

Zugriffstoken des ResourceManager-Endpunkts für aktuelles Konto erhalten

### Beispiel 2: Token für den unformatierte Zugriff für den AAD-Diagrammendpunkt
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

Zugriffstoken des AAD -Diagrammendpunkts für aktuelles Konto erhalten

### Beispiel 3: Token für den unformatierte Zugriff für den AAD-Diagrammendpunkt
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

Zugriffstoken des AAD -Diagrammendpunkts für aktuelles Konto erhalten

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

### -ResourceTypeName
Optionaler Name des Typs "Neuausführen", unterstützte Werte: AadGraph, AnalysisServices, Arm, Nachweis, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse. Der Standardwert ist "Arm", wenn dieser nicht angegeben ist.

```yaml
Type: System.String
Parameter Sets: KnownResourceTypeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceUrl
Ressourcen-URL für das Token, für das Sie token anfordern, z. B. ' http://graph.windows.net/ '.

```yaml
Type: System.String
Parameter Sets: ResourceUrl
Aliases: Resource, ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TenantId
Optionale Mandanten-ID. Verwenden Sie die Mandanten-ID des Standardkontexts, wenn dieser nicht angegeben ist.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Keine

## AUSGABEN

### System.String

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
