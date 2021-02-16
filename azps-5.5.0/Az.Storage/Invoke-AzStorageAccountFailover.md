---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100165721"
---
# Invoke-AzStorageAccountFailover

## SYNOPSIS
Ruft den Failover eines Speicherkontos auf.

## SYNTAX

### AccountName (Standard)
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### AccountObject
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Ruft den Failover eines Speicherkontos auf. Bei Verfügbarkeitsproblemen kann eine Failoveranforderung für ein Speicherkonto ausgelöst werden. Der Failover erfolgt vom primären Cluster des Speicherkontos zum sekundären Cluster für RA-GRS-Konten. Der sekundäre Cluster wird nach dem Failover primär.
Bitte beachten Sie die folgenden Auswirkungen auf Ihr Speicherkonto, bevor Sie den Failover starten: 1.1. Überprüfen Sie die Letzte Synchronisierungszeit mit GET BLOB Service Stats ( https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) , GET Table Service Stats ( und GET Queue Service Stats ( für Ihr https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) Konto). Dies sind die Daten, die verloren gehen können, wenn Sie den Failover initiieren.
2. Nach dem Failover wird der Speicherkontotyp in einen lokal redundanten Speicher (LRS) konvertiert. Sie können Ihr Konto so konvertieren, dass georedundanter Speicher (Geo redundant Storage, GRS) verwendet wird.
3. Sobald Sie GRS für Ihr Speicherkonto erneut aktivieren, repliziert Microsoft Daten in die neue sekundäre Region. Die Replikationszeit hängt von der Menge der zu replizierenden Daten ab. Beachten Sie, dass für das Bootstrap Bandbreitengebühren anfallen. https://azure.microsoft.com/en-us/pricing/details/bandwidth/

## BEISPIELE

### Beispiel 1: Aufrufen des Failover eines Speicherkontos
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

Dieser Befehl überprüft die letzte Synchronisierungszeit eines Speicherkontos und ruft dann den Failover des Kontos auf. Der sekundäre Cluster wird nach dem Failover primär. Da failover eine lange Zeit dauert, empfehlen Sie, ihn im Back-End mit dem Parameter "-Asjob" auszuführen, und warten Sie dann, bis der Auftrag abgeschlossen ist.

## PARAMETERS

### -AsJob
Ausführen des Cmdlets im Hintergrund

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

### -Force
Erzwingen des Failovers des Kontos

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

### -InputObject
Speicherkontoobjekt

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Name
Name des Speicherkontos.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Ressourcengruppenname.

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Confirm
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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

### -Waswenn
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
