---
external help file: ''
Module Name: Azs.Compute.Admin
online version: https://docs.microsoft.com/powershell/module/azs.compute.admin/stop-azsdiskmigrationjob
schema: 2.0.0
ms.openlocfilehash: bb5c78d6c0ae29d415e02d3e78e79f963bc3315c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93844847"
---
# Stop-AzsDiskMigrationJob

## Synopsis
Abbrechen eines Datenträger Migrationsauftrags

## Syntax

```
Stop-AzsDiskMigrationJob -Name <String> [-Location <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Beschreibung
Abbrechen eines Datenträger Migrationsauftrags

## Beispiele

### Beispiel 1:
```powershell
PS C:\> Stop-AzsDiskMigrationJob -Name TestJob

CreationTime : 2/26/2020 11:06:40 AM
EndTime      : 2/26/2020 11:07:24 AM
Id           : /subscriptions/627fecef-520e-4c18-94e0-8f0665ba86a7/providers/Microsoft.Compute.Admin/locations/redmond/diskmigrati
               onjobs/TestJob
Location     : redmond
MigrationId  : TestJob
Name         : redmond/TestJob
StartTime    : 2/26/2020 11:06:40 AM
Status       : Canceled
Subtask      : {47774498-6bc7-4ce2-98ca-738739ded2fc, b09ac623-f71d-480c-98bc-88fa3f603f2c}
TargetShare  : \\SU1FileServer.s31r1801.masd.stbtest.microsoft.com\SU1_ObjStore_4
Type         : Microsoft.Compute.Admin/locations/diskmigrationjobs
```

Abbrechen eines verwalteten Datenträger Migrationsauftrags

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Standort
Der Speicherort der Ressource.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### -Name
Der GUID-Name des Migrationsauftrags.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MigrationId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### -Abonnement-Nr
Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.
Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. ComputeAdmin. Models. Api20180730Preview. IDiskMigrationJob



## Notizen

## Verwandte Links

