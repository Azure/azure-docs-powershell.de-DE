---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/powershell/module/az.policyinsights/start-azpolicycompliancescan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Start-AzPolicyComplianceScan.md
ms.openlocfilehash: db51cfdf499fcf3d6c81f47d977978a6ff4bf8cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101937488"
---
# Start-AzPolicyComplianceScan

## SYNOPSIS
Löst eine Richtlinienkonformitätsauswertung für alle Ressourcen in einem Abonnement oder einer Ressourcengruppe aus.

## SYNTAX

```
Start-AzPolicyComplianceScan [-ResourceGroupName <String>] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet Start-AzPolicyComplianceScan** startet eine Richtlinienkonformitätsauswertung für ein Abonnement oder eine Ressourcengruppe. Für alle Ressourcen in diesem Bereich wird der Compliancestatus anhand aller zugewiesenen Richtlinien ausgewertet.

## BEISPIELE

### Beispiel 1: Starten einer Compliancescans im Abonnementbereich
```
PS C:\> Start-AzPolicyComplianceScan
```

Mit diesem Befehl wird eine Richtlinienkonformitätsauswertung für das aktive Abonnement gestartet.

### Beispiel 2: Starten einer Compliancescans im Ressourcengruppenbereich
```
PS C:\> Start-AzPolicyComplianceScan -ResourceGroupName "myRG"
```

Mit diesem Befehl wird eine Richtlinienkonformitätsauswertung für die Ressourcengruppe "myRG" im aktiven Abonnement gestartet.

### Beispiel 3: Starten sie eine Compliance-Überprüfung, und warten Sie, bis sie im Hintergrund abgeschlossen ist
```
PS C:\> $job = Start-AzPolicyComplianceScan -AsJob
PS C:\> $job | Wait-Job
```

Mit diesem Befehl wird eine Richtlinienkonformitätsauswertung für das aktive Abonnement gestartet. Er wartet, bis die Überprüfung abgeschlossen ist.

## PARAMETER

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
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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
Geben Sie True zurück, wenn der Befehl erfolgreich abgeschlossen wurde.

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
Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.

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
Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### System.String

## AUSGABEN

### System.Boolean

## NOTIZEN

## VERWANDTE LINKS
