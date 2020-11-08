---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/invoke-Azstorageaccountfailover
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Invoke-AzStorageAccountFailover.md
ms.openlocfilehash: 05399377a679a1bb06216364e17b198397a467f5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178670"
---
# Invoke-AzStorageAccountFailover

## Synopsis
Ruft das Failover eines speicherkontos auf.

## Syntax

### Kontoname (Standard)
```
Invoke-AzStorageAccountFailover [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Kontoobject
```
Invoke-AzStorageAccountFailover -InputObject <PSStorageAccount> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Ruft das Failover eines speicherkontos auf. Bei Verfügbarkeitsproblemen kann eine Failover-Anforderung für ein Speicherkonto ausgelöst werden. Das Failover erfolgt vom primären Cluster des speicherkontos zu sekundärem Cluster für RA-GRS-Konten. Der sekundäre Cluster wird nach einem Failover Primär.
Bitte verstehen Sie die folgenden Auswirkungen auf Ihr Speicherkonto, bevor Sie das Failover initiieren: 1,1. Bitte überprüfen Sie die letzte Synchronisierungszeit mithilfe von Get BLOB Service stats ( https://docs.microsoft.com/en-us/rest/api/storageservices/get-blob-service-stats) , Abrufen von tabellendienst Statistiken ( https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.table.cloudtableclient.getservicestats?view=azure-dotnet) und Abrufen von Warteschlangendienst Statistiken ( https://docs.microsoft.com/en-us/dotnet/api/microsoft.windowsazure.storage.queue.cloudqueueclient.getservicestats?view=azure-dotnet) für Ihr Konto). Dies sind die Daten, die Sie möglicherweise verlieren, wenn Sie das Failover initiieren.
2. nach dem Failover wird der Typ Ihres speicherkontos in den lokal redundanten Speicher (LRS) konvertiert. Sie können Ihr Konto in die Verwendung von "Geo-redundant Storage (GRS)" umwandeln.
3. Nachdem Sie die GRS für Ihr Speicherkonto wieder aktiviert haben, repliziert Microsoft Daten in Ihre neue sekundäre Region. Die Replikationszeit ist abhängig von der zu replizierenden Datenmenge. Beachten Sie bitte, dass für den Bootstrap Bandbreiten Gebühren anfallen. https://azure.microsoft.com/en-us/pricing/details/bandwidth/

## Beispiele

### Beispiel 1: Aufrufen eines Failovers eines speicherkontos
```
PS C:\>$account = Get-AzStorageAccount -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -IncludeGeoReplicationStats
PS C:\>$account.GeoReplicationStats

Status LastSyncTime
------ ------------
Live   11/13/2018 2:44:22 AM

PS C:\>$job = Invoke-AzStorageAccountFailover -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount" -Force -AsJob
PS C:\>$job | Wait-Job
```

Mit diesem Befehl wird die letzte Synchronisierungszeit eines speicherkontos überprüft, anschließend wird der sekundäre Cluster nach einem Failover als primärer Cluster verwendet. Da ein Failover lange Zeit in Anspruch nimmt, empfehlen wir, es im Back-End mit-AsJob-Parameter auszuführen, und warten Sie, bis der Auftrag abgeschlossen ist.

## Parameter

### -AsJob
Ausführen eines Cmdlets im Hintergrund

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

### -Inputobject
Speicherkonto Objekt

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
Name des speicherkontos

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
Name der Ressourcengruppe.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount

## Notizen

## Verwandte Links
