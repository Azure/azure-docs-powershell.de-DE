---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: 24c0140f4a1ba09111db0dacaa612c4a635493fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658755"
---
# Set-AzCurrentStorageAccount

## Synopsis
Ändert das aktuelle Speicherkonto des angegebenen Abonnements.

## Syntax

### UsingResourceGroupAndNameParameterSet (Standard)
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### UsingStorageContext
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzCurrentStorageAccount** " ändert das aktuelle Azure-Speicherkonto des angegebenen Azure-Abonnements in Azure PowerShell.
Das aktuelle Speicherkonto wird als Standard verwendet, wenn Sie auf den Speicher zugreifen, ohne einen Speicherkonto Namen anzugeben.

## Beispiele

### Beispiel 1: Einrichten des aktuellen speicherkontos
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

Dieser Befehl legt das Standardspeicher Konto für das angegebene Abonnement fest.

## Parameter

### -Context
Gibt ein **AzureStorageContext** -Objekt für das aktuelle Speicherkonto an.
Verwenden Sie zum Abrufen eines Speicherkontext Objekts das New-AzStorageContext-Cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UsingStorageContext
Aliases:

Required: True
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
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen des speicherkontos an, das von diesem Cmdlet geändert wird.

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt die Ressourcengruppe an, die das zu ändernde Speicherkonto enthält.

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext

### System. String

## Ausgaben

### System. String

## Notizen

## Verwandte Links

[Satz-AzStorageAccount](./Set-AzStorageAccount.md)


