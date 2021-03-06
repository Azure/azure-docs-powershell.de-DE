---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160009"
---
# Get-AzTemplateSpec

## SYNOPSIS
Ruft Vorlagenspezifikationen ab oder listet vorlagenspezifikationen auf

## SYNTAX

### ListTemplateSpecsParameterSet (Standard)
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### GetTemplateSpecByNameParameterSet
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### GetTemplateSpecByIdParameterSet
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## BESCHREIBUNG
Dieses Cmdlet kann verwendet werden, um Vorlagenspezifikationen in einer Abonnement-/Ressourcengruppe auflisten oder eine bestimmte Vorlagenspezifikation nach Name oder ID zu erhalten. Beim Abrufen einer bestimmten Vorlagenspezifikation nach Name/ID kann optional eine bestimmte Version abgerufen werden, indem über den Parameter **"-Version"** ein Versionsname angegeben wird. Wenn **"-Version"** verwendet wird, sind in * nur die jeweiligen Versionsdetails *vorhanden. Versionen* des zurückgegebenen Vorlagenspezifikationenobjekts. Wenn beim Abrufen einer Vorlagenspezifikation nach Name/ID keine bestimmte Version angegeben wird, sind alle Versionen im **vorhanden. Eigenschaft* "Versions" des zurückgegebenen Objekts.

**Hinweis:** Wenn Sie alle Vorlagenspezifikationen in einem Abonnement oder einer Ressourcengruppe auflisten, wird für jede zurückgegebene Vorlagenspezifikation *". Die Eigenschaft "Versionen"* ist *null.* Versionsinformationen sind nur enthalten, wenn die Parameter "-Name" oder "-ResourceId" bereitgestellt werden (z. B.: Sie fordern eine bestimmte Vorlagenspezifikation/Version an).

## BEISPIELE

### Beispiel 1: Listenvorlagenspezifikationen im aktuellen Abonnement
```powershell
PS C:\> Get-AzTemplateSpec
```

Listet alle Vorlagenspezifikationen im aktuellen Abonnement auf.

### Beispiel 2: Listenvorlagenspezifikationen in einer Ressourcengruppe
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

Listet alle Vorlagenspezifikationen in der Ressourcengruppe "myRG" des aktuellen Abonnements auf.

### Beispiel 3: Vorlagenspezifikation (mit allen Versionen) nach Name
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

Ruft Informationen zum Vorlagenspezifikationentyp "MyTemplateSpec" in der Ressourcengruppe "myRG" ab.

**Hinweis:** Alle Versionen der Vorlagenspezifikationen sind im "*enthalten. Versions*"-Eigenschaft des Rückgabeobjekts.

### Beispiel 4: Vorlagenspezifikation (bestimmte Version) nach Name
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

Ruft Informationen zur Version 'v1.0' des Vorlagenspezifikationen namens 'MyTemplateSpec' in der Ressourcengruppe 'myRG' ab.

**Hinweis:** Das *". Die Eigenschaft "Versionen"* des zurückgegebenen Objekts enthält nur die angeforderte Version.

### Beispiel 5: Vorlagenspezifikation (mit allen Versionen) nach Ressourcen-ID erhalten
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

Ruft Informationen zur Vorlagenspezifikation mit dem Namen "MyTemplateSpec" in der Ressourcengruppe "myRG" von \{ "subId" für Abonnements \} ab.

**Hinweis:** Alle Versionen der Vorlagenspezifikationen sind im "*enthalten. Versions*"-Eigenschaft des Rückgabeobjekts.

### Beispiel 6: Vorlagenspezifikation (bestimmte Version) nach Ressourcen-ID erhalten
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

Ruft Informationen zur Version 'v1.0' des Vorlagenspezifikationen namens 'MyTemplateSpec' in der Ressourcengruppe 'myRG' von subscription \{ subId \} ab.

**Hinweis:** Das *". Die Eigenschaft "Versionen"* des zurückgegebenen Objekts enthält nur die angeforderte Version.

## PARAMETERS

### -DefaultProfile
Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.

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

### -Name
Der Name der Vorlagenspezifikation.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Der Name der Ressourcengruppe.

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceId
Die vollqualifizierte Ressourcen-ID der Vorlagenspezifikation. Beispiel: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Die Version der Vorlagenspezifikation.

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

## AUSGABEN

### Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN
