---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/powershell/module/az.accounts/get-azaccesstoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Get-AzAccessToken.md
ms.openlocfilehash: 5fcd81dcfc69f020a4e17e0858abfca0edaba405
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929128"
---
# Get-AzAccessToken

## SYNOPSIS
Unformatiertes Zugriffstoken erhalten. Stellen Sie bei Verwendung von -ResourceUrl sicher, dass der Wert der aktuellen Azure-Umgebung zu entsprechen hat. Sie können auf den Wert von `(Get-AzContext).Environment` verweisen.

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

### Beispiel 1 Unformatiertes Zugriffstoken für ARM Endpunkt
```powershell
PS C:\> Get-AzAccessToken
```

Zugriffstoken des ResourceManager-Endpunkts für das aktuelle Konto erhalten

### Beispiel 2 Unformatiertes Zugriffstoken für AAD-Diagrammendpunkt
```powershell
PS C:\> Get-AzAccessToken -ResourceTypeName AadGraph
```

Zugriffstoken des AAD-Diagrammendpunkts für das aktuelle Konto

### Beispiel 3 Unformatiertes Zugriffstoken für AAD-Diagrammendpunkt
```powershell
PS C:\> Get-AzAccessToken -Resource "https://graph.windows.net/"
```

Zugriffstoken des AAD-Diagrammendpunkts für das aktuelle Konto

## PARAMETER

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
Optional: Typname neu erstellen, unterstützte Werte: AadGraph, AnalysisServices, Arm, Attestation, Batch, DataLake, KeyVault, OperationalInsights, ResourceManager, Synapse. Standardwert ist Arm, wenn nicht angegeben.

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
Ressourcen-URL für das Token, das Sie anfordern, z. B. ' http://graph.windows.net/ '.

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
Optionale Mandanten-ID. Verwenden Sie die Mandanten-ID des Standardkontexts, wenn sie nicht angegeben ist.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Keine

## AUSGABEN

### System.String

## NOTIZEN

## VERWANDTE LINKS
