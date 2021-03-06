---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 8300B143-E322-419E-BC98-DBA56DD90A59
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermroledefinition
schema: 2.0.0
ms.openlocfilehash: bf3df91cc8b35ad2c61d277b12ad234a8034d207
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849484"
---
# New-AzureRmRoleDefinition

## Synopsis
Erstellt eine benutzerdefinierte Rolle in Azure RBAC.
Stellen Sie entweder eine JSON-Rollen Definitionsdatei oder ein PSRoleDefinition-Objekt als eingabebereit.
Verwenden Sie zuerst den Befehl Get-AzureRmRoleDefinition, um ein Baseline-Rollen Definitionsobjekt zu generieren.
Ändern Sie dann die Eigenschaften nach Bedarf.
Verwenden Sie abschließend diesen Befehl, um eine benutzerdefinierte Rolle mithilfe der Rollendefinition zu erstellen.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### InputFileParameterSet
```
New-AzureRmRoleDefinition [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
New-AzureRmRoleDefinition [-Role] <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das New-AzureRmRoleDefinition-Cmdlet erstellt eine benutzerdefinierte Rolle in Azure Role-Based Zugriffssteuerung.
Stellen Sie eine Rollendefinition als Eingabe für den Befehl als JSON-Datei oder als PSRoleDefinition-Objekt bereit.
Die Definition der Eingabe Rolle muss die folgenden Eigenschaften enthalten:
1) DisplayName: der Name der benutzerdefinierten Rolle
2) Beschreibung: eine kurze Beschreibung der Rolle, die den von der Rolle gewährten Zugriff zusammenfasst.
3) Aktionen: die Gruppe von Vorgängen, denen die benutzerdefinierte Rolle Zugriff gewährt.
Verwenden Sie Get-AzureRmProviderOperation, um den Vorgang für Azure-Ressourcenanbieter abzurufen, die mithilfe von Azure RBAC gesichert werden können.
Im folgenden sind einige gültige Vorgangs Zeichenfolgen enthalten:
 - "*/Read" gewährt Zugriff auf Lesevorgänge aller Azure-Ressourcenanbieter.
 - "Microsoft. Network/*/Read" gewährt Zugriff auf Lesevorgänge für alle Ressourcentypen im Microsoft. Network-Ressourcenanbieter von Azure.
 - "Microsoft. Compute/virtualMachines/*" gewährt Zugriff auf alle Vorgänge von virtuellen Computern und deren untergeordneten Ressourcentypen.
4) AssignableScopes: die Gruppe von Bereichen (Azure-Abonnements oder Ressourcengruppen), in denen die benutzerdefinierte Rolle für die Zuweisung zur Verfügung steht.
Mithilfe von AssignableScopes können Sie die benutzerdefinierte Rolle nur in den Abonnements oder Ressourcengruppen zur Verfügung stellen, die Sie benötigen, und nicht die Benutzeroberfläche für die restlichen Abonnements oder Ressourcengruppen überladen.
Im folgenden finden Sie einige gültige beschreibbar-Bereiche:
 - "/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e", "/Subscriptions/e91d47c4-76f3-4271-a796-21b4ecfe3624": stellt die Rolle in zwei Abonnements für die Zuweisung zur Verfügung.
 - "/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e": stellt die Rolle in einem einzigen Abonnement für die Zuweisung zur Verfügung.
 - "/Subscriptions/c276fc76-9cd4-44c9-99a7-4fd71546436e/resourceGroups/Network": stellt die Rolle für die Zuweisung nur in der Netzwerkressourcen Gruppe zur Verfügung.
Die Definition der Eingabe Rolle kann die folgenden Eigenschaften enthalten:
1) Notacts: der Satz von Vorgängen, der aus den Aktionen ausgeschlossen werden muss, um die effektiven Aktionen für die benutzerdefinierte Rolle zu ermitteln.
Wenn es einen bestimmten Vorgang gibt, dem Sie in einer benutzerdefinierten Rolle keinen Zugriff gewähren möchten, empfiehlt es sich, ihn mithilfe von notacts auszuschließen, anstatt alle Vorgänge außer diesem bestimmten Vorgang in Aktionen anzugeben.
2) Daten Aktionen: die Gruppe von Datenvorgängen, denen die benutzerdefinierte Rolle Zugriff gewährt.
3) NotDataActions: der Satz von Vorgängen, der aus den dataactions ausgeschlossen werden muss, um die effektiven dataactions für die benutzerdefinierte Rolle zu ermitteln.
Wenn es einen bestimmten Datenvorgang gibt, dem Sie in einer benutzerdefinierten Rolle keinen Zugriff gewähren möchten, empfiehlt es sich, NotDataActions zu verwenden, um ihn auszuschließen, anstatt alle anderen Vorgänge als diesen bestimmten Vorgang in Aktionen anzugeben.
Hinweis: Wenn einem Benutzer eine Rolle zugewiesen wird, die einen Vorgang in notacts angibt und auch einer anderen Rolle zugewiesen wurde, wird der Zugriff auf denselben Vorgang gewährt – der Benutzer kann diesen Vorgang durchführen.
Notacts ist keine Ablehnungsregel – es ist einfach eine bequeme Möglichkeit zum Erstellen einer Reihe von zulässigen Vorgängen, wenn bestimmte Vorgänge ausgeschlossen werden müssen.
Im folgenden finden Sie eine JSON-Beispielrollen Definition, die als Eingabe {"Name": "aktualisierte Rolle", "Beschreibung": "kann alle Ressourcen überwachen und virtuelle Maschinen starten und neu starten", "Aktionen": \[ " */Read", "Microsoft. ClassicCompute/VirtualMachines/Restart/Aktion"; "Microsoft. ClassicCompute/VirtualMachines/Start/Action" \] ; "notacts": \[ "* /Write" \] ; "Daten Aktionen": \[ "Microsoft. Storage/storageAccounts/blobServices/Container/BLOBs/Read" \] ; "NotDataActions": \[ "Microsoft. Storage/storageAccounts/blobServices/Container/BLOBs/Write" \] , "AssignableScopes": \[ "/Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" \] }

## Beispiele

### Erstellen mithilfe von PSRoleDefinitionObject
```
PS C:\> $role = Get-AzureRmRoleDefinition -Name "Virtual Machine Contributor"
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

          PS C:\> New-AzureRmRoleDefinition -Role $role
```

### Erstellen mit JSON-Datei
```
PS C:\> New-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Eingabefeld
Dateiname mit einer einzelnen JSON-Rollendefinition

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
Rollen Definitionsobjekt

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine

## Ausgaben

### Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition

## Notizen
Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung

## Verwandte Links

[Get-AzureRmProviderOperation](./Get-AzureRmProviderOperation.md)

[Get-AzureRmRoleDefinition](./Get-AzureRmRoleDefinition.md)

[Satz-AzureRmRoleDefinition](./Set-AzureRmRoleDefinition.md)

[Remove-AzureRmRoleDefinition](./Remove-AzureRmRoleDefinition.md)

