---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: b136f5194bdc7e0f4b4dfc969564d7ef8476d9bf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290843"
---
# Set-AzConnectedMachineExtension

## SYNOPSIS
Der Vorgang zum Erstellen oder Aktualisieren der Erweiterung.

## SYNTAX

### UpdateExpanded (Standard)
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### Update
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## BESCHREIBUNG
Der Vorgang zum Erstellen oder Aktualisieren der Erweiterung.

## BEISPIELE

### Beispiel 1: Festlegen einer Erweiterung auf einem Computer
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

Legt eine Erweiterung auf einem Computer fest.

### Beispiel 2: Festlegen einer Erweiterung mit Erweiterungsparametern, die über die Pipeline angegeben werden
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

Dadurch wird eine Erweiterung mit den Erweiterungsparametern festgelegt, die von dem über die Pipeline übergebenen Objekt bereitgestellt werden.
Dies ist ideal, wenn Sie die Parameter eines Computers übernehmen und auf einen anderen Computer anwenden möchten.

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

### -AutoUpgradeMinorVersion
Gibt an, ob für die Erweiterung eine neuere Nebenversion verwendet werden soll, wenn eine zur Bereitstellungszeit verfügbar ist.
Nach der Bereitstellung wird mit der Erweiterung jedoch nur dann ein Upgrade von Nebenversionen bereitgestellt, wenn diese erneut bereitgestellt werden, auch wenn diese Eigenschaft auf "true" festgelegt ist.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
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

### -ExtensionParameter
Beschreibt eine Computererweiterung.
Informationen zum Erstellen finden Sie im Abschnitt NOTES zu #A0 und zum Erstellen einer Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ExtensionType
Gibt den Typ der Erweiterung an. Beispiel: "CustomScriptExtension".

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ForceRerun
Die Art und Weise, wie der Erweiterungshandler zum Aktualisieren gezwungen werden sollte, auch wenn sich die Erweiterungskonfiguration nicht geändert hat.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Location
Der geo-Standort, an dem sich die Ressource befindet

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -MachineName
Der Name des Computers, auf dem die Erweiterung erstellt oder aktualisiert werden soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Der Name der Computererweiterung.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
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

### -ProtectedSetting
Die Erweiterung kann entweder geschützteSettings oder protectedSettingsFromKeyVault oder überhaupt keine geschützten Einstellungen enthalten.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesProtectedSettings
Parameter Sets: UpdateExpanded
Aliases: ProtectedSettings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Publisher
Der Name des Herausgebers des Erweiterungshandlers.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
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
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Einstellung
Json formatierte öffentliche Einstellungen für die Erweiterung.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionPropertiesSettings
Parameter Sets: UpdateExpanded
Aliases: Settings

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SubscriptionId
Abonnementanmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren.
Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.

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

### -Tag
Ressourcentags.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -TypeHandlerVersion
Gibt die Version des Skripthandlers an.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
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
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension

## AUSGABEN

### Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtension

## HINWEISE

ALIASE

KOMPLEXE PARAMETEREIGENSCHAFTEN

Erstellen Sie zum Erstellen der unten beschriebenen Parameter eine Hashtabelle mit den entsprechenden Eigenschaften. Um Informationen zu Hashtabellen zu erhalten, führen Sie Get-Help about_Hash_Tables.


<IMachineExtension>EXTENSIONPARAMETER: Beschreibt eine Computererweiterung.
  - `Location <String>`: Der geo-Standort, an dem sich die Ressource befindet
  - `[Tag <ITrackedResourceTags>]`: Ressourcentags.
    - `[(Any) <String>]`: Dies gibt an, dass diesem Objekt beliebige Eigenschaften hinzugefügt werden können.
  - `[AutoUpgradeMinorVersion <Boolean?>]`: Gibt an, ob für die Erweiterung eine neuere Nebenversion verwendet werden soll, wenn eine zur Bereitstellungszeit verfügbar ist. Nach der Bereitstellung wird mit der Erweiterung jedoch nur dann ein Upgrade von Nebenversionen bereitgestellt, wenn diese erneut bereitgestellt werden, auch wenn diese Eigenschaft auf "true" festgelegt ist.
  - `[ForceUpdateTag <String>]`: Wie der Erweiterungshandler zum Aktualisieren gezwungen werden sollte, auch wenn sich die Erweiterungskonfiguration nicht geändert hat.
  - `[MachineExtensionType <String>]`: Gibt den Typ der Erweiterung an. Beispiel: "CustomScriptExtension".
  - `[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Die Erweiterung kann entweder geschützteSettings oder protectedSettingsFromKeyVault oder überhaupt keine geschützten Einstellungen enthalten.
  - `[Publisher <String>]`: Der Name des Herausgebers des Erweiterungshandlers.
  - `[Setting <IMachineExtensionPropertiesSettings>]`: Json formatierte öffentliche Einstellungen für die Erweiterung.
  - `[TypeHandlerVersion <String>]`: Gibt die Version des Skripthandlers an.

## LINKS ZU VERWANDTEN THEMEN

