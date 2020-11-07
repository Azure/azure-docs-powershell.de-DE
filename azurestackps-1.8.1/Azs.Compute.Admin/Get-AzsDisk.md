---
external help file: Azs.Compute.Admin-help.xml
Module Name: Azs.Compute.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b639a09789960393ac26d035a80157069dbaaa
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/15/2020
ms.locfileid: "93828344"
---
# Get-AzsDisk

## Synopsis
Gibt die Liste der verwalteten Datenträger zurück, die in der angegebenen Freigabe migriert werden können.

## Syntax

### Liste (Standard)
```
Get-AzsDisk [-Location <String>] [-Start <Int32>] [-SharePath <String>] [-Count <Int32>]
 [-UserSubscriptionId <String>] [-Status <String>] [<CommonParameters>]
```

### ResourceId
```
Get-AzsDisk -ResourceId <String> [<CommonParameters>]
```

### Erhalten
```
Get-AzsDisk [-Location <String>] -Name <String> [<CommonParameters>]
```

## Beschreibung
Gibt eine Liste von Datenträgern zurück.

## Beispiele

### --------------------------Beispiel 1--------------------------
```
$disks = Get-AzsDisk -location local
```

Gibt eine Liste der verwalteten Datenträger am lokalen Speicherort zurück.
Standardmäßig werden die ersten 100-Datenträger

### --------------------------Beispiel 2--------------------------
```
$disk = Get-AzsDisk -location local -name $DiskId
```

Besorgen Sie sich einen bestimmten verwalteten Datenträger.

## Parameter

### -Anzahl
Die maximale Anzahl von Datenträgern, die zurückgegeben werden sollen.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Standort
Der Speicherort der Ressource.

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Die Datenträger-GUID als Identität.

```yaml
Type: String
Parameter Sets: Get
Aliases: DiskId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Resourcen-Nr
Die Ressourcen-ID.

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SharePath
Die Quell Freigabe, zu der die Ressource gehört.

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Start
Der startIndex von Datenträgern in Query.

```yaml
Type: Int32
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Die Parameter des Datenträger Zustands.

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -UserSubscriptionId
Die Mandanten-Abonnement-ID, zu der die Ressource gehört.

```yaml
Type: String
Parameter Sets: List
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. AzureStack. Management. Compute. admin. Models. Disk

## Notizen

## Verwandte Links

