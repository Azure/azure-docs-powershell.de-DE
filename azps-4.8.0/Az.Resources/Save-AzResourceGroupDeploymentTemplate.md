---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 8BB4AD6B-EBE3-442A-83E7-B77A31573208
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/save-azresourcegroupdeploymenttemplate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Save-AzResourceGroupDeploymentTemplate.md
ms.openlocfilehash: 7f630ddb538b51dd7403fd731dfed19f78b4c67e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166117"
---
# Save-AzResourceGroupDeploymentTemplate

## Synopsis
Speichert eine Bereitstellungsvorlage einer Ressourcengruppe in einer Datei.

## Syntax

```
Save-AzResourceGroupDeploymentTemplate -ResourceGroupName <String> -DeploymentName <String> [-Path <String>]
 [-Force] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **Save-AzResourceGroupDeploymentTemplate**  speichert eine Vorlage für die Ressourcengruppen Bereitstellung in einer JSON-Datei.

## Beispiele

### Beispiel 1: Speichern einer Bereitstellungsvorlage
```powershell
PS C:\>Save-AzResourceGroupDeploymentTemplate -DeploymentName "TestDeployment" -ResourceGroupName "TestGroup"
```

Dieser Befehl ruft die Bereitstellungsvorlage aus TestDeployment ab und speichert Sie als JSON-Datei im aktuellen Verzeichnis.

### Beispiel 2

Speichert eine Bereitstellungsvorlage einer Ressourcengruppe in einer Datei. automatisch

<!-- Aladdin Generated Example -->
```powershell
Save-AzResourceGroupDeploymentTemplate -DeploymentName 'TestDeployment' -Path <String> -ResourceGroupName 'TestGroup'
```

## Parameter

### -ApiVersion
Gibt die Version der zu verwendenden Ressourcenanbieter-API an.
Wenn keine Angabe erfolgt, wird die neueste API-Version verwendet.

```yaml
Type: System.String
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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Deploymentname
Gibt den Namen der Bereitstellung an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.

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

### -Path
Gibt den Ausgabepfad der Vorlagendatei an.

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

### -Pre
Gibt an, dass dieses Cmdlet Vorabversion-API-Versionen verwendet, wenn automatisch ermittelt wird, welche API-Version verwendet werden soll.

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

### -ResourceGroupName
Gibt den Namen der Ressourcengruppe an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
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
Default value: False
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### System. Management. Automation. PSObject

## Notizen

## Verwandte Links
