---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/new-Azstorageaccountmanagementpolicyfilter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountManagementPolicyFilter.md
ms.openlocfilehash: 3e4cc41bf67eaef505cdeb1e33f84753f20650a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826687"
---
# New-AzStorageAccountManagementPolicyFilter

## Synopsis
Erstellt ein ManagementPolicy-Regelfilter Objekt, das in New-AzStorageAccountManagementPolicyRule verwendet werden kann.

## Syntax

```
New-AzStorageAccountManagementPolicyFilter [-PrefixMatch <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet **New-AzStorageAccountManagementPolicyFilter** wird ein ManagementPolicy-Regelfilter Objekt erstellt, das in New-AzStorageAccountManagementPolicyRule verwendet werden kann.

## Beispiele

### Beispiel 1: erstellt ein ManagementPolicy-Regelfilter Objekt, fügt es dann einer Verwaltungsrichtlinien Regel hinzu und legt es auf ein Speicherkonto
```
PS C:\>$filter = New-AzStorageAccountManagementPolicyFilter -PrefixMatch blobprefix1,blobprefix2
PS C:\>$filter 

PrefixMatch                BlobTypes  
-----------                ---------  
{blobprefix1, blobprefix2} {blockBlob}

PS C:\>$action = Add-AzStorageAccountManagementPolicyAction -BaseBlobAction Delete -daysAfterModificationGreaterThan 100
PS C:\>$rule = New-AzStorageAccountManagementPolicyRule -Name Test -Action $action -Filter $filter
PS C:\>$policy = Set-AzStorageAccountManagementPolicy -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount" -Rule $rule
```

Mit diesem Befehl wird ein ManagementPolicy-Regelfilter Objekt erstellt. Fügen Sie es dann einer Verwaltungsrichtlinien Regel hinzu, und legen Sie es auf ein Speicherkonto.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -PrefixMatch
Ein Array von Zeichenfolgen für Präfixe, die übereinstimmen sollen.
Eine Präfixzeichenfolge muss mit einem Containernamen beginnen.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. Management. Storage. Models. PSManagementPolicyRuleFilter

## Notizen

## Verwandte Links
