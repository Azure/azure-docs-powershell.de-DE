---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmDiagnosticSetting.md
ms.openlocfilehash: 36e523fbb224b77df205b8c7e7d736af0faa2962
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663573"
---
# Set-AzureRmDiagnosticSetting

## Synopsis
Legt die Einstellungen für Protokolle und Metriken für die Ressource fest.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

```
Set-AzureRmDiagnosticSetting -ResourceId <String> [-StorageAccountId <String>] [-ServiceBusRuleId <String>]
 [-EventHubAuthorizationRuleId <String>] [-Enabled <Boolean>]
 [-Categories <System.Collections.Generic.List`1[System.String]>]
 [-Timegrains <System.Collections.Generic.List`1[System.String]>] [-RetentionEnabled <Boolean>]
 [-WorkspaceId <String>] [-RetentionInDays <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Satz-AzureRmDiagnosticSetting** " aktiviert oder deaktiviert jede Zeit Körnung und Protokoll Kategorie für die jeweilige Ressource.

Die Protokolle und Metriken werden im angegebenen Speicherkonto gespeichert.

## Beispiele

### Beispiel 1: Aktivieren aller Metriken und Protokolle für eine Ressource
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True
```

Dieser Befehl aktiviert alle verfügbaren Metriken und Protokolle für Resource01.

### Beispiel 2: Deaktivieren aller Metriken und Protokolle
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $False
```

Mit diesem Befehl werden alle verfügbaren Metriken und Protokolle für die Ressource Resource01 deaktiviert.

### Beispiel 3: Aktivieren mehrerer Kategorien
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2
StorageAccountId   : <storageAccountId>
StorageAccountName : <storageAccountName>
Metrics
Enabled   : True
Timegrain : PT1M
Enabled   : True
Timegrain : PT1H
Logs
Enabled  : True
Category : Category1
Enabled  : True
Category : Category2
Enabled  : True
Category : Category3
Enabled  : False
Category : Category4
```

Dieser Befehl aktiviert Kategorie1 und Kategorie2.
Alle zeitkörnungen und anderen Kategorien bleiben identisch.

### Beispiel 4: Aktivieren einer Zeit Körnung und mehrerer Kategorien
```
PS C:\>Set-AzureRmDiagnosticSetting -ResourceId "Resource01" -Enabled $True -Categories Category1,Category2 -Timegrains PT1M
```

Dieser Befehl aktiviert nur Kategorie1-, Kategorie2-und Time Grain-PT1M.
Alle anderen Zeit Körnungen und-Kategorien sind unverändert.

## Parameter

### -Kategorien
Gibt die Liste der Protokollkategorien an, die entsprechend dem Wert von *Enabled aktiviert* oder deaktiviert werden sollen.
Wenn Sie keine Kategorie angeben, funktioniert dieser Befehl für alle Kategorien.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Aktiviert
Gibt an, ob die Diagnose aktiviert werden soll.
Geben Sie $true an, um die Diagnose zu aktivieren, oder $false, um die Diagnose zu deaktivieren.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Resourcen-Nr
Gibt die ID der Ressource an.

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

### -RetentionEnabled
Gibt an, ob die Beibehaltung von Diagnoseinformationen aktiviert ist.

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionInDays
Gibt die Aufbewahrungsrichtlinie in Tagen an.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ServiceBusRuleId
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

### -StorageAccountId
Gibt die ID des speicherkontos an, in dem die Daten gespeichert werden sollen.

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

### -Zeitkörnungen
Gibt die Zeit Körnungen an, die für Metriken entsprechend dem Wert von *Enabled aktiviert* oder deaktiviert werden sollen.
Wenn Sie kein Zeit Korn angeben, wird dieser Befehl für alle verfügbaren Zeit Körnungen ausgeführt.

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Arbeitsbereichs-Nr
Die ID des Arbeitsbereichs

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

### -EventHubAuthorizationRuleId
Die Ereignis-Hub-Regel-ID

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

### Microsoft. Azure. Commands. Insights. OutputClasses. PSServiceDiagnosticSettings

## Notizen

## Verwandte Links

[Get-AzureRmDiagnosticSetting](./Get-AzureRmDiagnosticSetting.md)


