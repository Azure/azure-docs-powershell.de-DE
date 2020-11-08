---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: F29E0B9C-2479-44FB-B196-EAF97B69E6A6
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/get-azoperationalinsightsworkspacemanagementgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Get-AzOperationalInsightsWorkspaceManagementGroup.md
ms.openlocfilehash: 1579308aed29a4d42cddfeec6f01c71c72c06c6f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165085"
---
# Get-AzOperationalInsightsWorkspaceManagementGroup

## Synopsis
Ruft Details zu Verwaltungsgruppen ab, die mit einem Arbeitsbereich verbunden sind.

## Syntax

```
Get-AzOperationalInsightsWorkspaceManagementGroup [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzOperationalInsightsWorkspaceManagementGroup** " listet die Verwaltungsgruppen auf, die mit einem Arbeitsbereich verbunden sind.

## Beispiele

### Beispiel 1: Abrufen von Verwaltungsgruppen nach Arbeitsbereichsnamen
```
PS C:\>Get-AzOperationalInsightsWorkspaceManagementGroup -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace"
```

Dieser Befehl ruft die Verwaltungsgruppen für den Arbeitsbereich mit dem Namen myworkspace in der Ressourcengruppe mit dem Namen ContosoResourceGroup ab.

### Beispiel 2: Abrufen von Verwaltungsgruppen mithilfe der Pipeline
```
PS C:\>Get-AzOperationalInsightsWorkspace -ResourceGroupName "ContosoResourceGroup" -Name "MyWorkspace" | Get-AzOperationalInsightsWorkspaceManagementGroup
```

Dieser Befehl verwendet das Get-AzOperationalInsightsWorkspace-Cmdlet, um den Arbeitsbereich mit dem Namen myworkspace abzurufen, und übergibt dann den Arbeitsbereich an das aktuelle Cmdlet, das die Verwaltungsgruppen für diesen Arbeitsbereich abruft.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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
Gibt den Arbeitsbereichsnamen an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen einer Azure-Ressourcengruppe an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. OperationalInsights. Models. PSManagementGroup

## Notizen

## Verwandte Links

[Azure-Cmdlets für operationelle Einblicke](./Az.OperationalInsights.md)

[Get-AzOperationalInsightsWorkspace](./Get-AzOperationalInsightsWorkspace.md)


