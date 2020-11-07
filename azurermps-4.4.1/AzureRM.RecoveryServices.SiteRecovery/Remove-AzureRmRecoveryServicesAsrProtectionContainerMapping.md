---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping.md
ms.openlocfilehash: 3d26a5285fbe96c0e77c56819567e21820cddf4f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663545"
---
# Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping

## Synopsis
Löscht die angegebene Azure Site Recovery Protection-Container Zuordnung.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -InputObject <ASRProtectionContainerMapping>
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping** löscht die angegebene Zuordnung des angegebenen Azure Site Recovery Protection-Containers.

## Beispiele

### Beispiel 1
```
PS C:\> $currentJob = Remove-AzureRmRecoveryServicesAsrProtectionContainerMapping -ProtectionContainerMapping $ProtectionContainerMapping
```

Startet das Löschen der angegebenen Schutzcontainer Zuordnung und gibt den ASR-Auftrag zurück, der zum Nachvollziehen des Vorgangs verwendet wird.

## Parameter

### -Force
Erzwingen Sie, dass der Befehl ausgeführt wird, ohne dass eine zusätzliche Warnung bereitgestellt wird.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Das Eingabeobjekt für das Cmdlet: das Container Zuordnungsobjekt für ASR-Schutz, das dem zu löschenden Schutzcontainer entspricht.

```yaml
Type: ASRProtectionContainerMapping
Parameter Sets: (All)
Aliases: ProtectionContainerMapping

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Bestätigen
Geben Sie an, ob eine Bestätigung erforderlich ist. Legen Sie den Wert des Confirm-Parameters auf $false fest, um die Bestätigung zu überspringen.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, ohne das Cmdlet tatsächlich auszuführen.

```yaml
Type: SwitchParameter
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

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRProtectionContainerMapping

## Ausgaben

### Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob

## Notizen

## Verwandte Links

[Get-AzureRmRecoveryServicesAsrProtectionContainerMapping](./Get-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)

[Neu – AzureRmRecoveryServicesAsrProtectionContainerMapping](./New-AzureRmRecoveryServicesAsrProtectionContainerMapping.md)
