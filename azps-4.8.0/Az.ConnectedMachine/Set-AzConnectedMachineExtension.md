---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/set-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Set-AzConnectedMachineExtension.md
ms.openlocfilehash: b136f5194bdc7e0f4b4dfc969564d7ef8476d9bf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009301"
---
# Set-AzConnectedMachineExtension

## Synopsis
Der Vorgang, um die Erweiterung zu erstellen oder zu aktualisieren.

## Syntax

### UpdateExpanded (Standard)
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -Location <String> [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ExtensionType <String>]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionPropertiesSettings>] [-Tag <Hashtable>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### Aktualisieren
```
Set-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtension> [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## Beschreibung
Der Vorgang, um die Erweiterung zu erstellen oder zu aktualisieren.

## Beispiele

### Beispiel 1: Einrichten einer Erweiterung auf einem Computer
```powershell
PS C:\> $Settings = @{ "commandToExecute" = "powershell.exe -c Get-Process" }
PS C:\> Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName win-eastus1 -Location eastus -Publisher "Microsoft.Compute" -TypeHandlerVersion 1.10 -Settings $Settings -ExtensionType CustomScriptExtension

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

Legt eine Erweiterung auf einem Computer fest.

### Beispiel 2: Einrichten einer Erweiterung mit den über die Pipeline angegebenen Erweiterungs Parametern
```powershell
PS C:\> $otherExtension = Get-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName other
PS C:\> $otherExtension | Set-AzConnectedMachineExtension -Name custom -ResourceGroupName ContosoTest -MachineName important

Name   Location ProvisioningState
----   -------- -----------------
custom eastus   Succeeded
```

Dadurch wird eine Erweiterung mit den Erweiterungs Parametern festgelegt, die von dem über die Pipeline übergebenen Objekt bereitgestellt werden.
Das ist großartig, wenn Sie die Parameter eines Rechners angreifen und auf einen anderen Computer anwenden möchten.

## Parameter

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
Gibt an, ob die Erweiterung eine neuere Nebenversion verwenden soll, wenn eine zur Bereitstellungszeit verfügbar ist.
Nach der Bereitstellung werden die Erweiterungen jedoch nur dann untergeordnete Versionen aktualisiert, wenn Sie erneut bereitgestellt werden, auch wenn diese Eigenschaft auf true festgelegt ist.

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

### -Extensionparameter
Beschreibt eine Computererweiterung.
Informationen zu Konstrukten finden Sie unter Abschnitt "Notizen" für extensionparameter-Eigenschaften und Erstellen einer Hashtabelle.

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
Gibt den Typ der Erweiterung an; ein Beispiel ist "CustomScriptExtension".

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
Die erzwungene Aktualisierung des Erweiterungs Handlers, auch wenn die Erweiterungskonfiguration nicht geändert wurde.

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

### -Standort
Der Geo-Standort, an dem die Ressource wohnt

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

### -Nowait
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
Die Erweiterung kann entweder protectedSettings oder protectedSettingsFromKeyVault oder keine geschützten Einstellungen enthalten.

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
Der Name des Erweiterungs Handlers Publisher.

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
Mit JSON formatierte öffentliche Einstellungen für die Erweiterung.

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

### -Tag
Ressourcenkategorien.

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
Gibt die Version des Skript Handlers an.

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

### Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension

## Notizen

Aliase

komplexe Parameter Eigenschaften

Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften. Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.


Extensionparameter <IMachineExtension> : Beschreibt eine Computererweiterung.
  - `Location <String>`: Der Geo-Standort, an dem die Ressource wohnt
  - `[Tag <ITrackedResourceTags>]`: Ressourcenkategorien.
    - `[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.
  - `[AutoUpgradeMinorVersion <Boolean?>]`: Gibt an, ob die Erweiterung eine neuere Nebenversion verwenden soll, wenn eine zur Bereitstellungszeit verfügbar ist. Nach der Bereitstellung werden die Erweiterungen jedoch nur dann untergeordnete Versionen aktualisiert, wenn Sie erneut bereitgestellt werden, auch wenn diese Eigenschaft auf true festgelegt ist.
  - `[ForceUpdateTag <String>]`: Die erzwungene Aktualisierung des Erweiterungs Handlers, auch wenn sich die Erweiterungskonfiguration nicht geändert hat.
  - `[MachineExtensionType <String>]`: Gibt den Typ der Erweiterung an; ein Beispiel ist "CustomScriptExtension".
  - `[ProtectedSetting <IMachineExtensionPropertiesProtectedSettings>]`: Die Erweiterung kann entweder protectedSettings oder protectedSettingsFromKeyVault oder überhaupt keine geschützten Einstellungen enthalten.
  - `[Publisher <String>]`: Der Name des Erweiterungs Handlers Publisher.
  - `[Setting <IMachineExtensionPropertiesSettings>]`: JSON-formatierte öffentliche Einstellungen für die Erweiterung.
  - `[TypeHandlerVersion <String>]`: Gibt die Version des Skript Handlers an.

## Verwandte Links

