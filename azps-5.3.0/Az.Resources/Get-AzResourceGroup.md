---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 5B17A241-BF36-48A6-BC29-4C32C08F5F94
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azresourcegroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzResourceGroup.md
ms.openlocfilehash: 9c7c002861832da3e871b49f03753608ba48268d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459419"
---
# Get-AzResourceGroup

## SYNOPSIS
Ruft Ressourcengruppen ab.

## SYNTAX

### GetByResourceGroupName (Standard)
```
Get-AzResourceGroup [[-Name] <String>] [[-Location] <String>] [-Tag <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetByResourceGroupId
```
Get-AzResourceGroup [[-Location] <String>] [-Id <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "Get-AzResourceGroup"** ruft Die Azure-Ressourcengruppen im aktuellen Abonnement ab.
Sie können alle Ressourcengruppen erhalten oder eine Ressourcengruppe nach Name oder anderen Eigenschaften angeben.
Standardmäßig ruft dieses Cmdlet alle Ressourcengruppen im aktuellen Abonnement ab.
Weitere Informationen zu Azure-Ressourcen und -Ressourcengruppen finden Sie im New-AzResourceGroup-Cmdlet.

## BEISPIELE

### Beispiel 1: Erhalten einer Ressourcengruppe nach Name
```
PS C:\> Get-AzResourceGroup -Name "EngineerBlog"
```

Dieser Befehl ruft die Azure-Ressourcengruppe in Ihrem Abonnement mit dem Namen "EngineerBlog" ab.

### Beispiel 2: Alle Tags einer Ressourcengruppe erhalten
```
PS C:\> (Get-AzResourceGroup -Name "ContosoRG").Tags
```

Dieser Befehl ruft die Ressourcengruppe "ContosoRG" ab und zeigt die dieser Gruppe zugeordneten Tags an.

### Beispiel 3: Ressourcengruppen auf Der Grundlage eines Tags erhalten
```
PS C:\> Get-AzResourceGroup -Tag @{'environment'='prod'}
```

### Beispiel 4: Anzeigen der Ressourcengruppen nach Ort
```
PS C:\> Get-AzResourceGroup |
  Sort Location,ResourceGroupName |
  Format-Table -GroupBy Location ResourceGroupName,ProvisioningState,Tags
```

### Beispiel 5: Anzeigen der Namen aller Ressourcengruppen an einem bestimmten Speicherort
```
PS C:\> Get-AzResourceGroup -Location westus2 |
   Sort ResourceGroupName | 
   Format-Wide ResourceGroupName -Column 4
```

### Beispiel 6: Anzeigen der Ressourcengruppen, deren Namen mit WebServer beginnen
```
PS C:\> Get-AzResourceGroup -Name WebServer*
```

## PARAMETERS

### -ApiVersion
Gibt die vom Ressourcenanbieter unterstützte API-Version an.
Sie können eine andere Version als die Standardversion angeben.

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

### -ID
Gibt die ID der ressourcengruppe an, die sie erhalten soll.
Platzhalterzeichen sind nicht zulässig.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupId
Aliases: ResourceGroupId, ResourceId

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Gibt den Speicherort der Ressourcengruppe an, die sie erhalten soll.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Ressourcengruppe an, die sie erhalten soll. Dieser Parameter unterstützt Platzhalter am Anfang und/oder Ende der Zeichenfolge.

```yaml
Type: System.String
Parameter Sets: GetByResourceGroupName
Aliases: ResourceGroupName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### -Pre
Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.

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

### -Tag
Die Hashtabelle für das Tag zum Filtern von Ressourcengruppen.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: GetByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### System.Collections.Hashtable

## AUSGABEN

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceGroup

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[New-AzResourceGroup](./New-AzResourceGroup.md)

[Remove-AzResourceGroup](./Remove-AzResourceGroup.md)

[Set-AzResourceGroup](./Set-AzResourceGroup.md)

