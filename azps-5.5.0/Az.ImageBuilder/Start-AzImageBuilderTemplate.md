---
external help file: ''
Module Name: Az.ImageBuilder
online version: https://docs.microsoft.com/en-us/powershell/module/az.imagebuilder/start-azimagebuildertemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ImageBuilder/help/Start-AzImageBuilderTemplate.md
ms.openlocfilehash: 710c39adca3f3a82b91b1e27a7f63e0ef1f6b693
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161569"
---
# Start-AzImageBuilderTemplate

## SYNOPSIS
Erstellen von Artefakten aus einer vorhandenen Bildvorlage

## SYNTAX

### Ausführen (Standard)
```
Start-AzImageBuilderTemplate -ImageTemplateName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### RunViaIdentity
```
Start-AzImageBuilderTemplate -InputObject <IImageBuilderIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## BESCHREIBUNG
Erstellen von Artefakten aus einer vorhandenen Bildvorlage

## BEISPIELE

### Beispiel 1: Starten einer Bildvorlage
```powershell
PS C:\> Start-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg

```

Mit diesem Befehl wird eine Bildvorlage gestartet.

### Beispiel 2: Starten einer Bildvorlage
```powershell
PS C:\> $template = Get-AzImageBuilderTemplate -ResourceGroupName wyunchi-imagebuilder -Name template-name-sn78hg
PS C:\> Start-AzImageBuilderTemplate -InputObject $template

```

Mit diesem Befehl wird eine Bildvorlage gestartet.

## PARAMETERS

### -AsJob
Ausführen des Befehls als Auftrag

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
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageTemplateName
Der Name der Bildvorlage

```yaml
Type: System.String
Parameter Sets: Run
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity
Parameter Sets: RunViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -NoWait
Asynchrones Ausführen des Befehls

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

### -PassThru
Gibt "true" zurück, wenn der Befehl erfolgreich ausgeführt wurde.

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

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: Run
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.
Die Abonnement-ID ist teil des URI für jeden Dienstaufruf.

```yaml
Type: System.String
Parameter Sets: Run
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.PowerShell.Cmdlets.ImageBuilder.Models.IImageBuilderIdentity

## AUSGABEN

### System.Boolean

## HINWEISE

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften. Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.


INPUTOBJECT <IImageBuilderIdentity> : Identity Parameter
  - `[Id <String>]`: Ressourcenidentitätspfad
  - `[ImageTemplateName <String>]`: Der Name der Bildvorlage
  - `[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.
  - `[RunOutputName <String>]`: Der Name der Ausgabe der Ausführung
  - `[SubscriptionId <String>]`: Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist teil des URI für jeden Dienstaufruf.

## LINKS ZU VERWANDTEN THEMEN

