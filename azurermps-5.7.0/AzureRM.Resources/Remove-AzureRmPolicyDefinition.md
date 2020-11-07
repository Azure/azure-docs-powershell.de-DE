---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: DEC01722-EB1A-45CE-BD30-9DB861718573
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/remove-azurermpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Remove-AzureRmPolicyDefinition.md
ms.openlocfilehash: 68c4f94ea4fee91c03ab0c65cbcba0f025c3c43b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662348"
---
# Remove-AzureRmPolicyDefinition

## Synopsis
Entfernt eine Richtliniendefinition.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### RemoveByPolicyDefinitionName (Standard)
```
Remove-AzureRmPolicyDefinition -Name <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### RemoveByPolicyDefinitionId
```
Remove-AzureRmPolicyDefinition -Id <String> [-Force] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Remove-AzureRmPolicyDefinition** entfernt eine Richtliniendefinition.

## Beispiele

### Beispiel 1: Entfernen der Richtliniendefinition nach Name
```
PS C:\>Remove-AzureRmPolicyDefinition -Name "VMPolicyDefinition"
```

Mit diesem Befehl wird die angegebene Richtliniendefinition entfernt.

### Beispiel 2: Entfernen der Richtliniendefinition nach Ressourcen-ID
```
PS C:\>$PolicyDefinition = Get-AzureRmPolicyDefinition -Name "VMPolicyDefinition" 
PS C:\> Remove-AzureRmPolicyDefinition -Id $PolicyDefinition.ResourceId -Force
```

Der erste Befehl ruft mithilfe des Get-AzureRmPolicyDefinition-Cmdlets eine Richtliniendefinition mit dem Namen VMPolicyDefinition ab.
Der Befehl speichert Sie in der $PolicyDefinition-Variablen.

Mit dem zweiten Befehl wird die Richtliniendefinition entfernt, die durch die Eigenschaft " **Resourcen** " von $PolicyDefinition identifiziert wurde.

## Parameter

### -ApiVersion
Gibt die Version der zu verwendenden Ressourcenanbieter-API an.
Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Gibt die vollqualifizierte Ressourcen-ID für die Richtliniendefinition an, die vom Cmdlet entfernt wird.

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Information
Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.

Die zulässigen Werte für diesen Parameter lauten wie folgt:

- Weiterhin
- Ignorieren
- Erkundigen
- SilentlyContinue
- Beenden
- Anhalten

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Gibt eine Informations Variable an.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Richtliniendefinition an, die vom Cmdlet entfernt wird.

```yaml
Type: String
Parameter Sets: RemoveByPolicyDefinitionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
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
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.
Das Cmdlet wird nicht ausgeführt.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

### Keine
Dieses Cmdlet akzeptiert keine Eingaben.

## Ausgaben

### System. Boolean

## Notizen

## Verwandte Links

[Get-AzureRmPolicyDefinition](./Get-AzureRmPolicyDefinition.md)

[Neu – AzureRmPolicyDefinition](./New-AzureRmPolicyDefinition.md)

[Satz-AzureRmPolicyDefinition](./Set-AzureRmPolicyDefinition.md)


