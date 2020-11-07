---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Set-AzureRmCurrentStorageAccount.md
ms.openlocfilehash: 73680e82a9d898075e905d88bcc8602609a5612d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662879"
---
# Set-AzureRmCurrentStorageAccount

## Synopsis
Ändert das aktuelle Speicherkonto des angegebenen Abonnements.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### UsingResourceGroupAndNameParameterSet (Standard)
```
Set-AzureRmCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### UsingStorageContext
```
Set-AzureRmCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmCurrentStorageAccount** " ändert das aktuelle Azure-Speicherkonto des angegebenen Azure-Abonnements in Azure PowerShell.
Das aktuelle Speicherkonto wird als Standard verwendet, wenn Sie auf den Speicher zugreifen, ohne einen Speicherkonto Namen anzugeben.

## Beispiele

### Beispiel 1: Einrichten des aktuellen speicherkontos
```
PS C:\>Set-AzureRmCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

Dieser Befehl legt das Standardspeicher Konto für das angegebene Abonnement fest.

## Parameter

### -Context
Gibt ein **AzureStorageContext** -Objekt für das aktuelle Speicherkonto an.
Verwenden Sie zum Abrufen eines Speicherkontext Objekts das New-AzureStorageContext-Cmdlet.

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

## Ausgaben

## Notizen

## Verwandte Links

[Satz-AzureRmStorageAccount](./Set-AzureRmStorageAccount.md)


