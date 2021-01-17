---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 8916b35da467fb16fd3802b726a7e105093b1c7a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459272"
---
# New-AzRoleDefinition

## SYNOPSIS
Erstellt eine benutzerdefinierte Rolle in Azure RBAC.
Geben Sie entweder eine JSON-Rollendefinitionsdatei oder ein "PSRoleDefinition"-Objekt als Eingabe an.
Verwenden Sie zunächst den Befehl Get-AzRoleDefinition, um ein grundlegendes Rollendefinitionsobjekt zu generieren.
Ändern Sie dann die Eigenschaften nach Bedarf.
Verwenden Sie zum Schluss diesen Befehl, um mithilfe der Rollendefinition eine benutzerdefinierte Rolle zu erstellen.

## SYNTAX

### InputFileParameterSet
```
New-AzRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das New-AzRoleDefinition erstellt eine benutzerdefinierte Rolle in Azure Role-Based Access Control.
Geben Sie eine Rollendefinition als Eingabe für den Befehl als Eine -JSON-Datei oder ein PSRoleDefinition-Objekt an.
Die Definition der Eingaberolle MUSS die folgenden Eigenschaften enthalten:
1) DisplayName: der Name der benutzerdefinierten Rolle
2) Beschreibung: Eine kurze Beschreibung der Rolle, die den Zugriff zusammenfasst, den die Rolle gewährt.
3) Aktionen: die Gruppe von Vorgängen, denen die benutzerdefinierte Rolle Zugriff gewährt.
Verwenden Get-AzProviderOperation, um den Vorgang für Azure-Ressourcenanbieter zu erhalten, die mit Azure RBAC gesichert werden können.
Im Folgenden finden Sie einige gültige Vorgangszeichenfolgen:
 - "*/read" gewährt Zugriff auf Lesevorgänge aller Azure-Ressourcenanbieter.
 - "Microsoft.Network/*/read" gewährt Zugriff auf Lesevorgänge für alle Ressourcentypen im Microsoft.Network-Ressourcenanbieter von Azure.
 - "Microsoft.Compute/virtualMachines/*" gewährt Zugriff auf alle Vorgänge virtueller Computer und deren untergeordnete Ressourcentypen.
4) AssignableScopes: Die Gruppe von Bereiche (Azure-Abonnements oder Ressourcengruppen), in denen die benutzerdefinierte Rolle für die Zuweisung zur Verfügung steht.
Mithilfe von "AssignableScopes" können Sie die benutzerdefinierte Rolle nur in den Abonnements oder Ressourcengruppen verfügbar machen, die sie benötigen, und die Benutzererfahrung für die restlichen Abonnements oder Ressourcengruppen nicht überladen.
Im Folgenden finden Sie einige gültige zuzuordnende Bereiche:
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": macht die Rolle für Die Zuweisung in zwei Abonnements verfügbar.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": Macht die Rolle zur Zuweisung in einem einzigen Abonnement verfügbar.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": macht die Rolle nur in der #A0 für Zuordnungen verfügbar.
Die Definition der Eingaberolle KANN die folgenden Eigenschaften enthalten:
1) NotActions: die Gruppe von Vorgängen, die von den Aktionen ausgeschlossen werden müssen, um die effektiven Aktionen für die benutzerdefinierte Rolle zu bestimmen.
Wenn es einen bestimmten Vorgang gibt, auf den Sie in einer benutzerdefinierten Rolle keinen Zugriff gewähren möchten, ist es praktisch, ihn mit NotActions auszuschließen, anstatt alle Anderen als diesen speziellen Vorgang in "Aktionen" anzugeben.
2) DataActions: die Gruppe von Datenvorgängen, für die die benutzerdefinierte Rolle Zugriff gewährt.
3) NotDataActions: die Gruppe von Vorgängen, die von dataActions ausgeschlossen werden müssen, um die effektiven Datenaktionen für die benutzerdefinierte Rolle zu bestimmen.
Wenn es einen bestimmten Datenvorgang gibt, auf den Sie in einer benutzerdefinierten Rolle keinen Zugriff gewähren möchten, ist es praktisch, notDataActions zu verwenden, um ihn auszuschließen, anstatt alle Anderen als diesen speziellen Vorgang in "Aktionen" anzugeben.
HINWEIS: Wenn einem Benutzer eine Rolle zugewiesen ist, die einen Vorgang in NotActions angibt, und einem Benutzer, dem auch eine andere Rolle zugewiesen ist, der Zugriff auf denselben Vorgang gewährt wird, kann der Benutzer diesen Vorgang ausführen.
NotActions ist keine Verweigernregel, sondern einfach eine bequeme Möglichkeit, eine Reihe zulässiger Vorgänge zu erstellen, wenn bestimmte Vorgänge ausgeschlossen werden müssen.
Es folgt eine json-Beispiel-Rollendefinition, die als Eingabe bereitgestellt werden kann { "Name": "Aktualisierte Rolle", "Beschreibung": "Kann alle Ressourcen überwachen und virtuelle Computer starten und neu starten", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action", \] "NotActions": \[ "*/write", \] "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read", \] "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write", \] "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxx" \] }

## BEISPIELE

### Beispiel 1: Erstellen mit PSRoleDefinitionObject
```powershell
PS C:\> $role = Get-AzRoleDefinition -Name "Virtual Machine Contributor"

PS C:\> $role.Id = $null
PS C:\> $role.Name = "Virtual Machine Operator"
PS C:\> $role.Description = "Can monitor, start, and restart virtual machines."
PS C:\> $role.Actions.RemoveRange(0,$role.Actions.Count)
PS C:\> $role.Actions.Add("Microsoft.Compute/*/read")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/start/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/restart/action")
PS C:\> $role.Actions.Add("Microsoft.Compute/virtualMachines/downloadRemoteDesktopConnectionFile/action")
PS C:\> $role.Actions.Add("Microsoft.Network/*/read")
PS C:\> $role.Actions.Add("Microsoft.Storage/*/read")
PS C:\> $role.Actions.Add("Microsoft.Authorization/*/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/read")
PS C:\> $role.Actions.Add("Microsoft.Resources/subscriptions/resourceGroups/resources/read")
PS C:\> $role.Actions.Add("Microsoft.Insights/alertRules/*")
PS C:\> $role.Actions.Add("Microsoft.Support/*")
PS C:\> $role.AssignableScopes.Clear()
PS C:\> $role.AssignableScopes.Add("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")

PS C:\> New-AzRoleDefinition -Role $role
```

### Beispiel 2: Erstellen mit einer JSON-Datei
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden

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

### -InputFile
Dateiname, der eine einzelne json-Rollendefinition enthält.

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Role
Rollendefinitionsobjekt.

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## HINWEISE
Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment

## LINKS ZU VERWANDTEN THEMEN

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[Set-AzRoleDefinition](./Set-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

