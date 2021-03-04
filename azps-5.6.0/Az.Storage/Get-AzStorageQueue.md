---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: 2361196f2e8b904f2403aaf06118122931e83afd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101942064"
---
# Get-AzStorageQueue

## SYNOPSIS
Listet Speicherwarteschlangen auf.

## SYNTAX

### QueueName (Standard)
```
Get-AzStorageQueue [[-Name] <String>] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### QueuePrefix
```
Get-AzStorageQueue -Prefix <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Im **Get-AzStorageQueue-Cmdlet** werden Speicherwarteschlangen aufgeführt, die einem Azure Storage-Konto zugeordnet sind.

## BEISPIELE

### Beispiel 1: Auflisten aller Azure Storage-Warteschlangen
```
PS C:\>Get-AzStorageQueue
```

Dieser Befehl ruft eine Liste aller Speicherwarteschlangen für das aktuelle Speicherkonto ab.

### Beispiel 2: Auflisten von Azure Storage-Warteschlangen mit einem Platzhalterzeichen
```
PS C:\>Get-AzStorageQueue -Name queue*
```

Dieser Befehl verwendet ein Platzhalterzeichen, um eine Liste der Speicherwarteschlangen zu erhalten, deren Name mit der Warteschlange beginnt.

### Beispiel 3: Auflisten von Azure Storage-Warteschlangen mit dem Präfix "Warteschlangenname"
```
PS C:\>Get-AzStorageQueue -Prefix "queue"
```

In diesem Beispiel wird der *Parameter Präfix* verwendet, um eine Liste der Speicherwarteschlangen zu erhalten, deren Name mit der Warteschlange beginnt.

## PARAMETER

### -Context
Gibt den Azure-Speicherkontext an.
Sie können sie mithilfe des **Cmdlets New-AzStorageContext** erstellen.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt einen Namen an.
Wenn kein Name angegeben ist, ruft das Cmdlet eine Liste aller Warteschlangen ab.
Wenn ein vollständiger oder teilweiser Name angegeben ist, ruft das Cmdlet alle Warteschlangen ab, die dem Namensmuster entsprechen.

```yaml
Type: System.String
Parameter Sets: QueueName
Aliases: N, Queue

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -Prefix
Gibt ein Präfix an, das im Namen der Warteschlangen verwendet wird, die Sie erhalten möchten.

```yaml
Type: System.String
Parameter Sets: QueuePrefix
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## AUSGABEN

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue

## NOTIZEN

## VERWANDTE LINKS

[New-AzStorageQueue](./New-AzStorageQueue.md)

[Remove-AzStorageQueue](./Remove-AzStorageQueue.md)


