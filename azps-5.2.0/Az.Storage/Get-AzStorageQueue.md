---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: C2EBCCF0-56CE-4D49-A138-74E52FC3A9AC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageQueue.md
ms.openlocfilehash: df4d31c1a90808e4d289cab60c5edf9785de1182
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290560"
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
Das **Cmdlet "Get-AzStorageQueue"** listet Speicherwarteschlangen auf, die einem Azure Storage-Konto zugeordnet sind.

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

In diesem Beispiel wird der *Präfixparameter* verwendet, um eine Liste der Speicherwarteschlangen zu erhalten, deren Name mit der Warteschlange beginnt.

## PARAMETERS

### -Context
Gibt den Azure -Speicherkontext an.
Sie können sie mit dem **Cmdlet "New-AzStorageContext"** erstellen.

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
Wenn ein vollständiger oder teilweiser Name angegeben wird, ruft das Cmdlet alle Warteschlangen ab, die dem Namensmuster entsprechen.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## AUSGABEN

### Microsoft.WindowsAzure.Commands.Common.Storage.ResourceModel.AzureStorageQueue

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzStorageQueue](./New-AzStorageQueue.md)

[Remove-AzStorageQueue](./Remove-AzStorageQueue.md)


