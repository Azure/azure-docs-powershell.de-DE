---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: aeda6548526c4ad12746ce90f1a030f85a0a8d2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918008"
---
# Set-AzCurrentStorageAccount

## SYNOPSIS
Ändert das aktuelle Speicherkonto des angegebenen Abonnements.

## SYNTAX

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

## BESCHREIBUNG
Das **Cmdlet Set-AzCurrentStorageAccount** ändert das aktuelle Azure Storage-Konto des angegebenen Azure-Abonnements in Azure PowerShell.
Das aktuelle Speicherkonto wird als Standard verwendet, wenn Sie auf Speicher zugreifen, ohne einen Namen für das Speicherkonto anzugeben.

## BEISPIELE

### Beispiel 1: Festlegen des aktuellen Speicherkontos
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

Mit diesem Befehl wird das Standardspeicherkonto für das angegebene Abonnement festgelegt.

## PARAMETER

### -Context
Gibt ein **AzureStorageContext-Objekt** für das aktuelle Speicherkonto an.
Verwenden Sie zum Abrufen eines Speicherkontextobjekts das New-AzStorageContext Cmdlet.

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
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Gibt den Namen des Speicherkontos an, das von diesem Cmdlet geändert wird.

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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

### System.String

## AUSGABEN

### System.String

## NOTIZEN

## VERWANDTE LINKS

[Set-AzStorageAccount](./Set-AzStorageAccount.md)


