---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: f3fb2377fd78db4b330afd39a8691f958597f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93479810"
---
# Sync-AzureAnalysisServicesInstance

## Synopsis

Synchronisiert eine angegebene Datenbank auf der angegebenen Instanz des Analysis Services-Servers mit allen Abfrage dezentralen Instanzen in der aktuell angemeldeten Umgebung, wie in Add-AzureAnalysisServicesAccount Befehl angegeben.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-Passthru]
```

## Beschreibung

Das Sync-AzureAnalysisServicesInstance-Cmdlet synchronisiert eine angegebene Datenbank auf der angegebenen Instanz des Analysis Services-Servers mit allen Abfrage-dezentralen Instanzen in der aktuell angemeldeten Umgebung, wie in Add-AzureAnalysisServicesAccount Befehl angegeben.

## Beispiele

### Beispiel 1

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

Dieser Befehl synchronisiert die Datenbank mit dem Namen "SalesOrders" auf dem Server "Contoso" im Umgebungs westus.asazure.Windows.net, vorausgesetzt, der Benutzer hat sich mit Add-AzureAnalysisServicesAccount Befehl bei dieser Umgebung angemeldet.

## Parameter

### -Instanz

Name der Analysis Services-Serverinstanz, die neu gestartet werden soll

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Datenbank

Identität der zu synchronisierenden Datenbank

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru

Wenn Sie dies angeben, wird true zurückgegeben, wenn der Befehl erfolgreich war.

```yaml
Type: Switch
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### System. Boolean

## Notizen

Alias: Sync-AzureAsInstance

## Verwandte Links
