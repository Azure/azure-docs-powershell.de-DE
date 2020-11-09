---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301072"
---
# Get-AzTemplateSpec

## Synopsis
Abrufen oder Auflisten von Vorlagen Spezifikationen

## Syntax

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

## Beschreibung
Dieses Cmdlet kann verwendet werden, um Vorlagen Spezifikationen in einer Abonnement-oder Ressourcengruppe aufzulisten oder eine bestimmte Vorlagenspezifikation nach Name oder ID abzurufen. Wenn Sie eine bestimmte Vorlagenspezifikation nach Name/ID abrufen, kann eine bestimmte Version optional abgerufen werden, indem Sie über den Parameter **-Version** einen Versionsnamen angeben. Wenn **-Version** verwendet wird, sind nur die spezifischen Versionsdetails in * enthalten *. Versionen* des zurückgegebenen Vorlagen Spezifikations Objekts. Wenn beim Abrufen einer Vorlagenspezifikation nach Name/ID keine bestimmte Version angegeben ist, sind alle Versionen in der * enthalten *. Versions* -Eigenschaft des zurückgegebenen Objekts.

**Hinweis** : Wenn Sie alle Vorlagen Spezifikationen innerhalb eines Abonnements oder einer Ressourcengruppe auflisten, werden die einzelnen Vorlagen Spezifikationen "zurückgegeben *. Versions "* -Eigenschaft ist *null*. Versionsinformationen werden nur berücksichtigt, wenn-Name oder-Resourcen-Parameter bereitgestellt werden (z. b.: Sie fordern eine bestimmte Vorlagenspezifikation/-Version an).

## Beispiele

### Beispiel 1: Auflisten von Vorlagen Spezifikationen im aktuellen Abonnement
```powershell
PS C:\> Get-AzTemplateSpec
```

Listet alle Vorlagen Spezifikationen im aktuellen Abonnement auf.

### Beispiel 2: Auflisten von Vorlagen Spezifikationen in einer Ressourcengruppe
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

Listet alle Vorlagen Spezifikationen in der Ressourcengruppe "myRG" des aktuellen Abonnements auf.

### Beispiel 3: Abrufen der Vorlagenspezifikation (mit allen Versionen) nach Name
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

Ruft Informationen zur Vorlagenspezifikation mit dem Namen "MyTemplateSpec" innerhalb der Ressourcengruppe "myRG" ab.

**Hinweis** : alle Versionen der Vorlage spec sind in der " *. Versions* "-Eigenschaft des Rückgabe Objekts.

### Beispiel 4: Abrufen der Vorlagenspezifikation (bestimmte Version) nach Name
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

Ruft Informationen zur Version "v 1.0" der Vorlagenspezifikation mit dem Namen "MyTemplateSpec" innerhalb der Ressourcengruppe "myRG" ab.

**Hinweis** : die *". Versions "* -Eigenschaft des zurückgegebenen Objekts enthält nur die angeforderte bestimmte Version.

### Beispiel 5: Abrufen der Vorlagenspezifikation (mit allen Versionen) nach Ressourcen-ID
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

Ruft Informationen zur Vorlagenspezifikation mit dem Namen "MyTemplateSpec" innerhalb der Ressourcengruppe "myRG" des Abonnement- \{ subId ab \} .

**Hinweis** : alle Versionen der Vorlage spec sind in der " *. Versions* "-Eigenschaft des Rückgabe Objekts.

### Beispiel 6: Abrufen der Vorlagenspezifikation (bestimmte Version) nach Ressourcen-ID
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

Ruft Informationen zur Version "v 1.0" der Vorlagenspezifikation mit dem Namen "MyTemplateSpec" innerhalb der Ressourcengruppe "myRG" des Abonnement- \{ subId ab \} .

**Hinweis** : die *". Versions "* -Eigenschaft des zurückgegebenen Objekts enthält nur die angeforderte bestimmte Version.

## Parameter

### -DefaultProfile
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.

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

### -Resourcen-Nr
Die vollqualifizierte Ressourcen-ID der Vorlagenspezifikation. Beispiel:/Subscriptions/{subId}/resourceGroups/{rgName}/Providers/Microsoft.Resources/templateSpecs/{templateSpecName}

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
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).

## Eingaben

### System. String

## Ausgaben

### Microsoft. Azure. Commands. ResourceManager. Cmdlets. SdkModels. PSTemplateSpec

## Notizen

## Verwandte Links
