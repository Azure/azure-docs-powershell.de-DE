---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzRoleDefinition.md
ms.openlocfilehash: 0930b66cf12d9c96d4fe00fa823cfd67c87081f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929843"
---
# New-AzRoleDefinition

## SYNOPSIS
Erstellt eine benutzerdefinierte Rolle in Azure RBAC.
Geben Sie entweder eine JSON-Rollendefinitionsdatei oder ein PSRoleDefinition-Objekt als Eingabe an.
Verwenden Sie zuerst den Befehl Get-AzRoleDefinition, um ein Geplantes Rollendefinitionsobjekt zu generieren.
Ändern Sie dann die Eigenschaften nach Bedarf.
Verwenden Sie schließlich diesen Befehl, um mithilfe der Rollendefinition eine benutzerdefinierte Rolle zu erstellen.

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
Das New-AzRoleDefinition-Cmdlet erstellt eine benutzerdefinierte Rolle in Azure Role-Based Access Control.
Stellen Sie eine Rollendefinition als Eingabe für den Befehl als JSON-Datei oder ein PSRoleDefinition-Objekt zur Verfügung.
Die Definition der Eingaberolle MUSS die folgenden Eigenschaften enthalten:
1) DisplayName: der Name der benutzerdefinierten Rolle
2) Beschreibung: Eine kurze Beschreibung der Rolle, die den Zugriff zusammenfasst, den die Rolle gewährt.
3) Aktionen: der Satz von Vorgängen, denen die benutzerdefinierte Rolle Zugriff gewährt.
Verwenden Get-AzProviderOperation, um den Vorgang für Azure-Ressourcenanbieter zu erhalten, der mit Azure RBAC gesichert werden kann.
Im Folgenden sind einige gültige Vorgangszeichenfolgen zu finden:
 - "*/read" gewährt Zugriff auf Lesevorgänge aller Azure-Ressourcenanbieter.
 - "Microsoft.Network/*/read" gewährt Zugriff auf Lesevorgänge für alle Ressourcentypen im Microsoft.Network-Ressourcenanbieter von Azure.
 - "Microsoft.Compute/virtualMachines/*" gewährt Zugriff auf alle Vorgänge virtueller Computer und deren untergeordnete Ressourcentypen.
4) AssignableScopes: die Gruppe von Bereichs (Azure-Abonnements oder Ressourcengruppen), in denen die benutzerdefinierte Rolle für die Zuordnung zur Verfügung steht.
Mit AssignableScopes können Sie die benutzerdefinierte Rolle nur in den Abonnements oder Ressourcengruppen verfügbar machen, die sie benötigen, und die Benutzererfahrung für die restlichen Abonnements oder Ressourcengruppen nicht überladen.
Im Folgenden sind einige gültige zuzuordnende Bereiche zu finden:
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": stellt die Rolle für die Zuweisung in zwei Abonnements zur Verfügung.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": stellt die Rolle in einem einzigen Abonnement zur Verfügung.
 - "/subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": stellt die Rolle nur in der Ressourcengruppe Netzwerk zur Verfügung.
Die Definition der Eingaberolle KANN die folgenden Eigenschaften enthalten:
1) NotActions: der Satz von Vorgängen, die aus den Aktionen ausgeschlossen werden müssen, um die effektiven Aktionen für die benutzerdefinierte Rolle zu bestimmen.
Wenn es einen bestimmten Vorgang gibt, auf den Sie in einer benutzerdefinierten Rolle keinen Zugriff gewähren möchten, ist es praktisch, notActions zu verwenden, um ihn auszuschließen, anstatt alle anderen Vorgänge als diesen bestimmten Vorgang in Aktionen anzugeben.
2) DataActions: der Satz von Datenvorgängen, denen die benutzerdefinierte Rolle Zugriff gewährt.
3) NotDataActions: der Satz von Vorgängen, die aus den DataActions ausgeschlossen werden müssen, um die effektiven Datenaktionen für die benutzerdefinierte Rolle zu ermitteln.
Wenn es einen bestimmten Datenvorgang gibt, auf den Sie in einer benutzerdefinierten Rolle keinen Zugriff gewähren möchten, ist es praktisch, notDataActions zu verwenden, um ihn auszuschließen, anstatt alle anderen Vorgänge als diesen bestimmten Vorgang in Aktionen anzugeben.
HINWEIS: Wenn einem Benutzer eine Rolle zugewiesen ist, die einen Vorgang in NotActions angibt und dem auch eine andere Rolle den Zugriff auf denselben Vorgang gewährt, kann der Benutzer diesen Vorgang ausführen.
NotActions ist keine Verweigernregel, sondern einfach eine bequeme Möglichkeit, eine Reihe zulässiger Vorgänge zu erstellen, wenn bestimmte Vorgänge ausgeschlossen werden müssen.
Im Folgenden finden Sie eine Beispieldefinition für json-Rollen, die als Eingabe bereitgestellt werden kann { "Name": "Aktualisierte Rolle", "Beschreibung": "Kann alle Ressourcen überwachen und virtuelle Computer starten und neu starten", "Aktionen": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action", \] "NotActions": \[ "*/write" \] , "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs /read" \] , "NotDataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/write" \] , "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }

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

### Beispiel 2: Erstellen mit der JSON-Datei
```powershell
PS C:\> New-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## PARAMETER

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

### -Rolle
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
Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## EINGABEN

### Keine

## AUSGABEN

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## NOTIZEN
Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment

## VERWANDTE LINKS

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[Set-AzRoleDefinition](./Set-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

