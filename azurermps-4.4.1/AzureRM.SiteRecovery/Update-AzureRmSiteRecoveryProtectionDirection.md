---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: A8C7BA18-4C67-46BA-9CCE-FC22E41465AE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryProtectionDirection.md
ms.openlocfilehash: 6103e9a820a80df7e89130f269296cd073283947
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481481"
---
# Update-AzureRmSiteRecoveryProtectionDirection

## Synopsis
Aktualisiert den Quell-und Zielserver zum Schutz eines Website Wiederherstellungsobjekts.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### ByPEObject (Standard)
```
Update-AzureRmSiteRecoveryProtectionDirection -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRPObject
```
Update-AzureRmSiteRecoveryProtectionDirection -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ByRPIObject
```
Update-AzureRmSiteRecoveryProtectionDirection -ReplicationProtectedItem <ASRReplicationProtectedItem>
 -Direction <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Update-AzureRmSiteRecoveryProtectionDirection** aktualisiert den Quell-und Zielserver zum Schutz eines Azure Site Recovery-Objekts nach Abschluss eines Commit-Failover-Vorgangs.

## Beispiele

## Parameter

### -Richtung
Gibt die Richtung des Commits an.
Die zulässigen Werte für diesen Parameter lauten wie folgt:

- PrimaryToRecovery
- RecoveryToPrimary

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: PrimaryToRecovery, RecoveryToPrimary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ProtectionEntity
Gibt das Schutz Entitätsobjekt an.

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -RecoveryPlan
Gibt ein Wiederherstellungsplan-Objekt an.

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ReplicationProtectedItem
```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: ByRPIObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
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

### ASRProtectionEntity
Der Parameter "ProtectionEntity" akzeptiert den Wert vom Typ "ASRProtectionEntity" aus der Pipeline.

### ASRRecoveryPlan
Der Parameter "RecoveryPlan" akzeptiert den Wert vom Typ "ASRRecoveryPlan" aus der Pipeline.

### ASRReplicationProtectedItem
Der Parameter "ReplicationProtectedItem" akzeptiert den Wert vom Typ "ASRReplicationProtectedItem" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. SiteRecovery. ASRJob

## Notizen

## Verwandte Links

