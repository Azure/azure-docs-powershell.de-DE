---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/export-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
ms.openlocfilehash: ceba71f729de627e0e7231b9c295d0cad1ccc105
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663648"
---
# Export-AzureRmRedisCache

## Synopsis
Exportiert Daten aus Azure-a/a-Cache in einen Container.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Export-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Mit dem Cmdlet " **Export-AzureRmRedisCache** " werden Daten aus Azure-a/a-Cache in einen Container exportiert.

## Beispiele

### Beispiel 1: Exportieren von Daten
```
PS C:\>Export-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

Dieser Befehl exportiert Daten aus einer Azure-Member-Cache-Instanz in den Container, der von der SAS-URL angegeben wird.

## Parameter

### -Container
Gibt die Dienst-SAS-URL des Containers an, in dem dieses Cmdlet Daten exportiert. Sie können eine Dienst-SAS-URL mit den folgenden PowerShell-Befehlen generieren: $storageAccountContext = New-AzureStorageContext-StorageAccountName "Speicher Name"-StorageAccountKey "Schlüssel" $sasKeyForContainer = New-AzureStorageContainerSASToken-Name "Containername"-Berechtigung "rwdl"-Startzeit ([System. DateTime]:: jetzt). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5)-context $storageAccountContext-FullUri Export-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "cachename"-Präfix "blobprefix"-Container ($sasKeyForContainer)

```yaml
Type: System.String
Parameter Sets: (All)
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

### -Format
Gibt ein Format für das BLOB an.
Derzeit ist RDB das einzige unterstützte Format.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen eines Caches an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
Gibt an, dass dieses Cmdlet einen booleschen Wert zurückgibt, der angibt, ob der Vorgang erfolgreich ausgeführt wurde.
Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.

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

### -Prefix
Gibt ein Präfix an, das für BLOB-Namen verwendet werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an, die den Cache enthält.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Bestätigen
Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird. Das Cmdlet wird nicht ausgeführt.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

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

## Ausgaben

### System. Boolean

## Notizen
* Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Benutzer-Nr., Cache, Web, Webanwendung, Website

## Verwandte Links

[Importieren-AzureRmRedisCache](./Import-AzureRmRedisCache.md)

[Neu – AzureRmRedisCache](./New-AzureRmRedisCache.md)

[Remove-AzureRmRedisCache](./Remove-AzureRmRedisCache.md)

[Reset-AzureRmRedisCache](./Reset-AzureRmRedisCache.md)

[Satz-AzureRmRedisCache](./Set-AzureRmRedisCache.md)


