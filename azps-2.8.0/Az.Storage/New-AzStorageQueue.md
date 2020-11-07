---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E9500392-6BE1-46EC-9AF5-9234281025E6
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragequeue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageQueue.md
ms.openlocfilehash: df6f616aacb066ec17aa089b8d91226a5bd171b8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823899"
---
# New-AzStorageQueue

## Synopsis
Erstellt eine Speicherwarteschlange.

## Syntax

```
New-AzStorageQueue [-Name] <String> [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzStorageQueue** erstellt eine Speicherwarteschlange in Azure.

## Beispiele

### Beispiel 1: Erstellen einer Azure Storage-Warteschlange
```
PS C:\>New-AzStorageQueue -Name "queueabc"
```

In diesem Beispiel wird eine Speicherwarteschlange mit dem Namen "queueabc" erstellt.

### Beispiel 2: Erstellen mehrerer Azure Storage-Warteschlangen
```
PS C:\>"queue1 queue2 queue3".split() | New-AzStorageQueue
```

In diesem Beispiel werden mehrere Speicher Warteschlangen erstellt.
Sie verwendet die Split-Methode der .net-Zeichenfolgenklasse und übergibt dann die Namen in der Pipeline.

## Parameter

### -Context
Gibt den Azure-Speicherkontext an.
Sie können es mithilfe des New-AzStorageContext-Cmdlets erstellen.

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
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext

## Ausgaben

### Microsoft. WindowsAzure. Commands. Common. Storage. ResourceModel. AzureStorageQueue

## Notizen

## Verwandte Links

[Get-AzStorageQueue](./Get-AzStorageQueue.md)

[Remove-AzStorageQueue](./Remove-AzStorageQueue.md)


