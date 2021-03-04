---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: 3a715e0c4c2540a0905035afabc15ef46caa32bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938760"
---
# Get-AzEventGridTopicType

## SYNOPSIS
Ruft die Details zu den Thementypen ab, die von Azure Event Grid unterstützt werden.

## SYNTAX

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Ruft die Details der von Azure Event Grid unterstützten Thementypen ab.
Wenn ein Thementypname angegeben wird, werden Details zu diesem Thementyp zurückgegeben.
Wenn kein Thementypname angegeben wird, werden Details zu allen Thementypen zurückgegeben.
Wenn IncludeEventTypes angegeben wird, werden Informationen zu Ereignistypen, die von jedem Thementyp unterstützt werden, in die Antwort einbezogen.

## BEISPIELE

### Beispiel 1
```powershell
PS C:\> Get-AzEventGridTopicType
```

Ruft eine Liste der Thementypen ab.

### Beispiel 2
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

Ruft Informationen zum Thematyp StorageAccounts ab.

### Beispiel 3
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

Ruft Informationen zum Thematyp StorageAccounts ab, einschließlich der von StorageAccounts unterstützten Ereignistypen.

## PARAMETER

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

### -IncludeEventTypeData
Wenn angegeben, enthält die Antwort die Ereignistypen, die von einem Thementyp unterstützt werden.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Name des EventGrid-Thementyps.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance

### Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo

## NOTIZEN

## VERWANDTE LINKS
