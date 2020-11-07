---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: 23392f77c9315cee2bf8b1b8369febbc2281c6ff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846080"
---
# Get-AzEventGridTopicType

## Synopsis
Ruft die Details zu den vom Azure-Ereignis Raster unterstützten Thementypen ab.

## Syntax

```
Get-AzEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Ruft die Details der Thementypen ab, die vom Azure-Ereignis Raster unterstützt werden.
Wenn der Name des Thementyps angegeben wird, werden Details zu diesem Thementyp zurückgegeben.
Wenn der Name des Thementyps nicht angegeben ist, werden Details zu allen Thementypen zurückgegeben.
Wenn IncludeEventTypes angegeben wird, werden Informationen zu Ereignistypen, die von den einzelnen Thementypen unterstützt werden, in der Antwort berücksichtigt.

## Beispiele

### Beispiel 1
```powershell
PS C:\> Get-AzEventGridTopicType
```

Ruft eine Liste der Thementypen ab.

### Beispiel 2
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

Ruft Informationen zum StorageAccounts-Thementyp ab.

### Beispiel 3
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

Ruft Informationen zum StorageAccounts-Thementyp ab, einschließlich der Ereignistypen, die von StorageAccounts unterstützt werden.

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
EventGrid Topic Type Name.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
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

### Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfoListInstance

### Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfo

## Notizen

## Verwandte Links
