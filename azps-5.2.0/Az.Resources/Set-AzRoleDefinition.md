---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleDefinition.md
ms.openlocfilehash: c68ad7def1b94796a020ffd29495e2b4c0b15a60
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307136"
---
# Set-AzRoleDefinition

## SYNOPSIS
Ändert eine benutzerdefinierte Rolle in Azure RBAC.
Geben Sie die geänderte Rollendefinition entweder als Eine -JSON-Datei oder als PSRoleDefinition an.
Verwenden Sie zunächst den Befehl Get-AzRoleDefinition, um die benutzerdefinierte Rolle abzurufen, die Sie ändern möchten.
Ändern Sie dann die Eigenschaften, die Sie ändern möchten.
Speichern Sie schließlich die Rollendefinition mit diesem Befehl.

## SYNTAX

### InputFileParameterSet
```
Set-AzRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
Set-AzRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das Set-AzRoleDefinition aktualisiert eine vorhandene benutzerdefinierte Rolle in Azure Role-Based Access Control.
Geben Sie die aktualisierte Rollendefinition als Eingabe für den Befehl als Eine -JSON-Datei oder ein PSRoleDefinition-Objekt an.
Die Rollendefinition für die aktualisierte benutzerdefinierte Rolle MUSS die ID und alle anderen erforderlichen Eigenschaften der Rolle enthalten, auch wenn sie nicht aktualisiert werden: "DisplayName", "Description", "Actions", "AssignableScopes".
NotActions, DataActions, NotDataActions sind optional.
Es folgt ein Beispiel mit aktualisierter Rollendefinition für Set-AzRoleDefinition { "Id": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "Aktualisierte Rolle", "Beschreibung": "Kann alle Ressourcen überwachen sowie virtuelle Computer starten und neu starten", "Actions": \[ "*/read", "Microsoft.ClassicCompute/virtualmachines/restart/action", "Microsoft.ClassicCompute/virtualmachines/start/action", \] "NotActions": \[ "*/write", \] "DataActions": \[ "Microsoft.Storage/storageAccounts/blobServices/containers/blobs/read", \] "NotDataActions": \[ "Microsoft.Storage/storageAccount": \] "AssignableScopes": \[ "/subscriptions/xxxxxxxx-xxxxxxxxxxxx" \] }

## BEISPIELE

### Beispiel 1: Aktualisieren mit PSRoleDefinitionObject
```powershell
PS C:\> $roleDef = Get-AzRoleDefinition "Contoso On-Call"
PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
PS C:\> $roleDef.AssignableScopes = @("/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx", "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx")
PS C:\> Set-AzRoleDefinition -Role $roleDef
```

### Beispiel 2: Erstellen mit einer JSON-Datei
```powershell
PS C:\> Set-AzRoleDefinition -InputFile C:\Temp\roleDefinition.json
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
Dateiname, der eine einzelne json-Rollendefinition enthält, die aktualisiert werden soll.
Schließen Sie nur die Eigenschaften ein, die im JSON aktualisiert werden sollen.
Die Eigenschaft "ID" ist "Required".

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Role
Zu aktualisierende Rollendefinitionsobjekt

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: RoleDefinitionParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## AUSGABEN

### Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition

## HINWEISE
Schlüsselwörter: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment

## LINKS ZU VERWANDTEN THEMEN

[Get-AzProviderOperation](./Get-AzProviderOperation.md)

[Get-AzRoleDefinition](./Get-AzRoleDefinition.md)

[New-AzRoleDefinition](./New-AzRoleDefinition.md)

[Remove-AzRoleDefinition](./Remove-AzRoleDefinition.md)

