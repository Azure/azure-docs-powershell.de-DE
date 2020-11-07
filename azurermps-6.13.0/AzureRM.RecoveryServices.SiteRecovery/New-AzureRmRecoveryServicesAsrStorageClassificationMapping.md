---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/new-azurermrecoveryservicesasrstorageclassificationmapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/New-AzureRmRecoveryServicesAsrStorageClassificationMapping.md
ms.openlocfilehash: 6ab8102de0deb27c18c6e50f8d78db2f23a5155a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662665"
---
# New-AzureRmRecoveryServicesAsrStorageClassificationMapping

## Synopsis
Erstellt eine Zuordnung der ASR-Speicher Klassifikation im Recovery Services Vault.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name <String>
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmRecoveryServicesAsrStorageClassificationMapping** erstellt eine Speicher Klassifikation, die den Wiederherstellungsdienste-Tresor zugeordnet ist.

## Beispiele

### Beispiel 1
```
PS C:\> $currentJob = New-AzureRmRecoveryServicesAsrStorageClassificationMapping -Name $StrorageClassificationMappingName -PrimaryStorageClassification $PrimaryStorageClassification -RecoveryStorageClassification $RecoveryStorageClassification
```

Startet den Speicher Klassifizierungs Zuordnungs Erstellungsvorgang mit den angegebenen Parametern und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.

## Parameter

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

### -Name
Gibt einen Namen für die ASR-Speicher Klassifikations Zuordnung an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PrimaryStorageClassification
Gibt das primäre ASR-Speicher Klassifikations Objekt für die Zuordnung an.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecoveryStorageClassification
Gibt das Wiederherstellungs-ASR-Speicher Klassifikations Objekt für die Zuordnung an.

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRStorageClassification

## Ausgaben

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## Notizen

## Verwandte Links

[Get-AzureRmRecoveryServicesAsrStorageClassificationMapping](./Get-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)

[Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping](./Remove-AzureRmRecoveryServicesAsrStorageClassificationMapping.md)
