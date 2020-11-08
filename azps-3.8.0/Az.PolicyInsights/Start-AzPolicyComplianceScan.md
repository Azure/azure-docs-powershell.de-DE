---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: cd173d17b0867fb5c635b77ee6c72847dc845cb7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003177"
---
# Start-AzPolicyComplianceScan

## Synopsis
Löst eine Richtlinien Konformitätsbewertung für alle Ressourcen in einem Abonnement oder einer Ressourcengruppe aus.

## Syntax

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Start-AzPolicyComplianceScan** startet eine Richtlinien Konformitätsbewertung für ein Abonnement oder eine Ressourcengruppe. Für alle Ressourcen innerhalb dieses Bereichs wird der Konformitätsstatus für alle zugewiesenen Richtlinien ausgewertet.

## Beispiele

### Beispiel 1: Starten einer Konformitätsüberprüfung im Abonnement Bereich
```
PS C:\> Start-AzPolicyComplianceScan
```

Mit diesem Befehl wird eine Richtlinien Konformitätsbewertung für das aktive Abonnement gestartet.

### Beispiel 2: Starten eines Konformitätsscans im Bereich der Ressourcengruppe
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

Mit diesem Befehl wird eine Richtlinien Konformitätsbewertung für die Ressourcengruppe "myRG" im aktiven Abonnement gestartet.

### Beispiel 3: Starten eines Konformitätsscans und abwarten des Abschlusses im Hintergrund
```
PS C:\> $job = Start-AzPolicyComplianceScan
PS C:\> $job | Wait-Job
```

Mit diesem Befehl wird eine Richtlinien Konformitätsbewertung für das aktive Abonnement gestartet. Der Vorgang wartet, bis die Überprüfung abgeschlossen ist.

## Parameter

### -AsJob
Führen Sie das Cmdlet im Hintergrund aus.

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PassThru
Gibt "true" zurück, wenn der Befehl erfolgreich abgeschlossen wurde.

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

### -ResourceGroupName
Name der Ressourcengruppe.

```yaml
Type: String
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
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### System. Boolean

## Notizen

## Verwandte Links
