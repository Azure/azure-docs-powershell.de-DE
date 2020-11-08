---
external help file: ''
Module Name: Az.ConnectedMachine
online version: https://docs.microsoft.com/en-us/powershell/module/az.connectedmachine/update-azconnectedmachineextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ConnectedMachine/help/Update-AzConnectedMachineExtension.md
ms.openlocfilehash: 95334b4f67685183e499518b068f1003f5bb6547
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009290"
---
# Update-AzConnectedMachineExtension

## Synopsis
Der Vorgang, um die Erweiterung zu erstellen oder zu aktualisieren.

## Syntax

### UpdateExpanded (Standard)
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-AutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>] [-Publisher <String>]
 [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>] [-Type <String>]
 [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### Aktualisieren
```
Update-AzConnectedMachineExtension -MachineName <String> -Name <String> -ResourceGroupName <String>
 -ExtensionParameter <IMachineExtensionUpdate> [-SubscriptionId <String>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentity
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity>
 -ExtensionParameter <IMachineExtensionUpdate> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### UpdateViaIdentityExpanded
```
Update-AzConnectedMachineExtension -InputObject <IConnectedMachineIdentity> [-AutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]
 [-Publisher <String>] [-Setting <IMachineExtensionUpdatePropertiesSettings>] [-Tag <Hashtable>]
 [-Type <String>] [-TypeHandlerVersion <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## Beschreibung
Der Vorgang, um die Erweiterung zu erstellen oder zu aktualisieren.

## Beispiele

### Beispiel 1: Aktualisieren einer Erweiterung
```powershell
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
            Settings = @{
                commandToExecute = "ls -l"
            }
        }
PS C:\> Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

Aktualisiert eine Erweiterung auf einem bestimmten Computer.

### Beispiel 2: Aktualisieren einer Erweiterung mit dem über die Pipeline angegebenen Speicherort
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -Settings @{
                commandToExecute = "ls -l"
            }

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

Aktualisiert eine bestimmte Erweiterung, die über die Pipeline übergeben wird.
Hier verwenden wir die Erweiterung, die über die Pipeline übergeben wurde, um uns zu helfen, zu ermitteln, welche Erweiterung wir betreiben möchten, und wir spezifizieren, was wir über die normalen Parameter (wie) ändern möchten. `-Settings`

### Beispiel 3: Aktualisieren einer Erweiterung mit Erweiterungs Parametern, die über die Pipeline angegeben werden
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $splat = @{
            ResourceGroupName = "connectedMachines"
            MachineName = "linux-eastus1_1"
            Name = "customScript"
        }
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension @splat

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

Aktualisiert eine bestimmte Erweiterung, die über die Pipeline übergeben wird.
Hier verwenden wir die Erweiterung, die über die Pipeline übergeben wird, um die Änderungen bereitzustellen, die wir für die Erweiterung vornehmen möchten.
Der Speicherort der Erweiterung wird nicht über die Pipeline abgerufen, sondern über die normalerweise angegebenen Parameter (durch den splat-Parameter).

### Beispiel 4: Verwenden eines Erweiterungsobjekts als Speicherort und Parameter für die Aktualisierung
```powershell
PS C:\> $extToUpdate = Get-AzConnectedMachineExtension -ResourceGroupName connectedMachines -MachineName linux-eastus1_1 -Name customScript
PS C:\> # Update the settings on the object that will be used via the pipeline
PS C:\> $extToUpdate.Setting.commandToExecute = "ls -l"
PS C:\> $extToUpdate | Update-AzConnectedMachineExtension -ExtensionParameter $extToUpdate

Name         Location ProvisioningState
----         -------- -----------------
customScript eastus   Succeeded
```

Aktualisiert eine bestimmte Erweiterung, die über die Pipeline übergeben wird.
Hier verwenden wir die Erweiterung, die über die Pipeline übergeben wurde, um uns zu helfen, die Erweiterung zu ermitteln, auf der wir arbeiten möchten.
Darüber hinaus verwenden wir die Parameter des Extension-Objekts, um anzugeben, was aktualisiert werden soll.

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
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
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
Beschreibt eine Aktualisierung der Computererweiterung.
Informationen zu Konstrukten finden Sie unter Abschnitt "Notizen" für extensionparameter-Eigenschaften und Erstellen einer Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdate
Parameter Sets: Update, UpdateViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ForceRerun
Die erzwungene Aktualisierung des Erweiterungs Handlers, auch wenn die Erweiterungskonfiguration nicht geändert wurde.

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Inputobject
Zu Erstell-Parameter des Parameters, lesen Sie den Abschnitt "Notizen" für Inputobject-Eigenschaften, und erstellen Sie eine Hashtabelle.

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.IConnectedMachineIdentity
Parameter Sets: UpdateViaIdentity, UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -MachineName
Der Name des Computers, auf dem die Erweiterung erstellt oder aktualisiert werden soll.

```yaml
Type: System.String
Parameter Sets: Update, UpdateExpanded
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
Parameter Sets: Update, UpdateExpanded
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
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesProtectedSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
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
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
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
Parameter Sets: Update, UpdateExpanded
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
Type: Microsoft.Azure.PowerShell.Cmdlets.ConnectedMachine.Models.Api20200802.IMachineExtensionUpdatePropertiesSettings
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
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
Parameter Sets: Update, UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### -Tag
Ressourcenkategorien

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Typ
Gibt den Typ der Erweiterung an; ein Beispiel ist "CustomScriptExtension".

```yaml
Type: System.String
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
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
Parameter Sets: UpdateExpanded, UpdateViaIdentityExpanded
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

### Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtensionUpdate

### Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. IConnectedMachineIdentity

## Ausgaben

### Microsoft. Azure. PowerShell. Cmdlets. ConnectedMachine. Models. Api20200802. IMachineExtension

## Notizen

Aliase

komplexe Parameter Eigenschaften

Wenn Sie die unten beschriebenen Parameter erstellen möchten, erstellen Sie eine Hashtabelle mit den entsprechenden Eigenschaften. Wenn Sie Informationen zu Hashtabellen erhalten, führen Sie Get-Help about_Hash_Tables aus.


Extensionparameter <IMachineExtensionUpdate> : Beschreibt eine Computer Erweiterungs Aktualisierung.
  - `[Tag <IUpdateResourceTags>]`: Ressourcenkategorien
    - `[(Any) <String>]`: Gibt an, dass einer Eigenschaft dieses Objekt hinzugefügt werden kann.
  - `[AutoUpgradeMinorVersion <Boolean?>]`: Gibt an, ob die Erweiterung eine neuere Nebenversion verwenden soll, wenn eine zur Bereitstellungszeit verfügbar ist. Nach der Bereitstellung werden die Erweiterungen jedoch nur dann untergeordnete Versionen aktualisiert, wenn Sie erneut bereitgestellt werden, auch wenn diese Eigenschaft auf true festgelegt ist.
  - `[ForceUpdateTag <String>]`: Die erzwungene Aktualisierung des Erweiterungs Handlers, auch wenn sich die Erweiterungskonfiguration nicht geändert hat.
  - `[ProtectedSetting <IMachineExtensionUpdatePropertiesProtectedSettings>]`: Die Erweiterung kann entweder protectedSettings oder protectedSettingsFromKeyVault oder überhaupt keine geschützten Einstellungen enthalten.
  - `[Publisher <String>]`: Der Name des Erweiterungs Handlers Publisher.
  - `[Setting <IMachineExtensionUpdatePropertiesSettings>]`: JSON-formatierte öffentliche Einstellungen für die Erweiterung.
  - `[Type <String>]`: Gibt den Typ der Erweiterung an; ein Beispiel ist "CustomScriptExtension".
  - `[TypeHandlerVersion <String>]`: Gibt die Version des Skript Handlers an.

Inputobject <IConnectedMachineIdentity> : Identity-Parameter
  - `[ExtensionName <String>]`: Der Name der Computererweiterung.
  - `[Id <String>]`: Ressourcen Identitäts Pfad
  - `[Name <String>]`: Der Name der hybridmaschine.
  - `[ResourceGroupName <String>]`: Der Name der Ressourcengruppe.
  - `[SubscriptionId <String>]`: Abonnement Anmeldeinformationen, die das Microsoft Azure-Abonnement eindeutig identifizieren. Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.

## Verwandte Links

