---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmRoleDefinition.md
ms.openlocfilehash: 476555b271d58f8e594f0cae1422bcdde1fc46e5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663527"
---
# Remove-AzureRmRoleDefinition

## Synopsis
Löscht eine benutzerdefinierte Rolle in Azure RBAC.
Die zu löschende Rolle wird mit der ID-Eigenschaft der Rolle angegeben.
DELETE schlägt fehl, wenn vorhandene Rollenzuweisungen an der benutzerdefinierten Rolle vorgenommen wurden.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### RoleDefinitionIdParameterSet (Standard)
```
Remove-AzureRmRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RoleDefinitionNameParameterSet
```
Remove-AzureRmRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Remove-AzureRmRoleDefinition-Cmdlet löscht eine benutzerdefinierte Rolle in Azure Role-Based Zugriffssteuerung.
Stellen Sie den ID-Parameter einer vorhandenen benutzerdefinierten Rolle bereit, um diese benutzerdefinierte Rolle zu löschen.
Standardmäßig werden Sie von Remove-AzureRmRoleDefinition zur Bestätigung aufgefordert.
Verwenden Sie den Parameter Force, um die Eingabeaufforderung zu unterdrücken.
Wenn vorhandene Rollenzuweisungen an der zu löschenden benutzerdefinierten Rolle vorgenommen wurden, schlägt der Löschvorgang fehl.

## Beispiele

### --------------------------Beispiel 1--------------------------
```
Get-AzureRmRoleDefinition -Name "Virtual Machine Operator" | Remove-AzureRmRoleDefinition
```

### --------------------------Beispiel 2--------------------------
```
Remove-AzureRmRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## Parameter

### -Force
Wenn diese Einstellung eingestellt ist, wird keine Bestätigung angefordert, bevor die benutzerdefinierte Rolle gelöscht wird.

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

### -ID
Die ID der zu löschenden Rollendefinition

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Der Name der Rollendefinition, die gelöscht werden soll.

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PassThru
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

### -Scope
Rollen Definitionsbereich.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

## Ausgaben

### System. Boolean

## Notizen
Schlüsselwörter: Azure, azurerm, arm, Ressource, Verwaltung, Manager, Ressource, Gruppe, Vorlage, Bereitstellung

## Verwandte Links

[Neu – AzureRmRoleDefinition](./New-AzureRmRoleDefinition.md)

[Get-AzureRmRoleDefinition](./Get-AzureRmRoleDefinition.md)

[Satz-AzureRmRoleDefinition](./Set-AzureRmRoleDefinition.md)

