---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
ms.openlocfilehash: 621fb15d3a83b7c704e5828d6541ad9d4404875c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501866"
---
# Get-AzureRmEventGridTopicType

## Synopsis
Ruft die Details zu den vom Azure-Ereignis Raster unterstützten Thementypen ab.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Get-AzureRmEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Ruft die Details der Thementypen ab, die vom Azure-Ereignis Raster unterstützt werden.
Wenn der Name des Thementyps angegeben wird, werden Details zu diesem Thementyp zurückgegeben.
Wenn der Name des Thementyps nicht angegeben ist, werden Details zu allen Thementypen zurückgegeben.
Wenn IncludeEventTypes angegeben wird, werden Informationen zu Ereignistypen, die von den einzelnen Thementypen unterstützt werden, in der Antwort berücksichtigt.

## Beispiele

### Beispiel 1
```
PS C:\> Get-AzureRmEventGridTopicType
```

Ruft eine Liste der Thementypen ab.

### Beispiel 2
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

Ruft Informationen zum StorageAccounts-Thementyp ab.

### Beispiel 3
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

Ruft Informationen zum StorageAccounts-Thementyp ab, einschließlich der Ereignistypen, die von StorageAccounts unterstützt werden.

## Parameter

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String
System. Management. Automation. Switchparameter

## Ausgaben

### System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfoListInstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]
Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfo

## Notizen

## Verwandte Links

