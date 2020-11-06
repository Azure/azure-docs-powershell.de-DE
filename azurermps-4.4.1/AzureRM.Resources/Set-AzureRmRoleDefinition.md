---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 115A7612-4856-47AE-AEE4-918350CD7009
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Set-AzureRmRoleDefinition.md
ms.openlocfilehash: 9f5927905e492fd93998e12f97a97a0380755905
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496926"
---
# Set-AzureRmRoleDefinition

## Synopsis
Ändert eine benutzerdefinierte Rolle in Azure RBAC.
Stellen Sie die geänderte Rollendefinition entweder als JSON-Datei oder als PSRoleDefinition bereit.
Verwenden Sie zuerst den Befehl Get-AzureRmRoleDefinition, um die benutzerdefinierte Rolle abzurufen, die Sie ändern möchten.
Ändern Sie dann die Eigenschaften, die Sie ändern möchten.
Speichern Sie die Rollendefinition schließlich mit diesem Befehl.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### InputFileParameterSet
```
Set-AzureRmRoleDefinition -InputFile <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### RoleDefinitionParameterSet
```
Set-AzureRmRoleDefinition -Role <PSRoleDefinition> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## Beschreibung
Das Set-AzureRmRoleDefinition-Cmdlet aktualisiert eine vorhandene benutzerdefinierte Rolle in Azure Role-Based Zugriffssteuerung.
Stellen Sie die aktualisierte Rollendefinition als Eingabe für den Befehl als JSON-Datei oder als PSRoleDefinition-Objekt bereit.
Die Rollendefinition für die aktualisierte benutzerdefinierte Rolle muss die ID und alle anderen erforderlichen Eigenschaften der Rolle enthalten, auch wenn Sie nicht aktualisiert werden: DisplayName, Description, Actions, AssignableScopes.
Notacts ist optional.

Im folgenden wird ein Beispiel für eine aktualisierte Role-Definition-JSON für Set-AzureRmRoleDefinition

{"ID": "52a6cc13-ff92-47a8-a39b-2a8205c3087e", "Name": "aktualisierte Rolle", "Beschreibung": "kann alle Ressourcen überwachen und virtuelle Maschinen starten und neu starten", "Aktionen": \[ "*/Read", "Microsoft. ClassicCompute/VirtualMachines/Restart/Aktion", "Microsoft. ClassicCompute/VirtualMachines/Start/Aktion" \] "AssignableScopes": \[ "/Subscriptions/4004a9fd-d58e-48dc-aeb2-4a4aec58606f" \] }

## Beispiele

### --------------------------Update mit PSRoleDefinitionObject--------------------------
```
PS C:\> $roleDef = Get-AzureRmRoleDefinition "Contoso On-Call"
          PS C:\> $roleDef.Actions.Add("Microsoft.ClassicCompute/virtualmachines/start/action")
          PS C:\> $roleDef.Description = "Can monitor all resources and start and restart virtual machines"
          PS C:\> $roleDef.AssignableScopes = @("/subscriptions/eb910d4f-edbf-429b-94F6-d76bae7ff401", "/subscriptions/a846d197-5eac-45c7-b885-a6227fe6d388")

          PS C:\> New-AzureRmRoleDefinition -Role $roleDef
```

### --------------------------Erstellen mit JSON-Datei--------------------------
```
PS C:\> Set-AzureRmRoleDefinition -InputFile C:\Temp\roleDefinition.json
```

## Parameter

### -Eingabefeld
Der Dateiname mit einer einzelnen JSON-Rollendefinition, die aktualisiert werden soll.
Schließen Sie nur die Eigenschaften ein, die in der JSON aktualisiert werden sollen.
Die ID-Eigenschaft ist erforderlich.

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
Rollen Definitionsobjekt, das aktualisiert werden soll

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

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### PSRoleDefinition
Der Parameter "Role" akzeptiert den Wert vom Typ "PSRoleDefinition" aus der Pipeline.

## Ausgaben

### Microsoft. Azure. Commands. resources. Models. Authorization. PSRoleDefinition

## Notizen
Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung

## Verwandte Links

[Get-AzureRmProviderOperation](./Get-AzureRmProviderOperation.md)

[Get-AzureRmRoleDefinition](./Get-AzureRmRoleDefinition.md)

[Neu – AzureRmRoleDefinition](./New-AzureRmRoleDefinition.md)

[Remove-AzureRmRoleDefinition](./Remove-AzureRmRoleDefinition.md)

