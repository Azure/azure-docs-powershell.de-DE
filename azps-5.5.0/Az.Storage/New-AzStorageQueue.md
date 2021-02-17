---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: 1c3f258f4aecbeb492e0e60e274c5e702ae1a3f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164777"
---
# New-AzStorageQueue

## SYNOPSIS
Erstellt eine Speicherwarteschlange.

## SYNTAX

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzStorageQueue"** erstellt eine Speicherwarteschlange in Azure.

## BEISPIELE

### Beispiel 1: Erstellen einer Azure -Speicherwarteschlange
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

In diesem Beispiel wird eine Speicherwarteschlange namens "queueabc" erstellt.

### Beispiel 2: Erstellen mehrerer Azure -Speicherwarteschlangen
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

In diesem Beispiel werden mehrere Speicherwarteschlangen erstellt.
Sie verwendet die Split-Methode der .NET-Zeichenfolgenklasse und übergibt dann die Namen in der Pipeline.

## PARAMETERS

### -Context
Gibt den Azure -Speicherkontext an.
Sie können sie mithilfe des cmdlets New-AzStorageContext erstellen.

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
Gibt einen Namen für die Warteschlange an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Queue

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

[Get-AzStorageQueue](./Get-AzStorageQueue.md)

[Remove-AzStorageQueue](./Remove-AzStorageQueue.md)


