---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 160cff39918691c310de6931cd57cb415774d7e6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843439"
---
# Get-AzPolicyAssignment

## Synopsis
Ruft Richtlinienzuweisungen ab.

## Syntax

### DefaultParameterSet (Standard)
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### NameParameterSet
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### IncludeDescendentParameterSet
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### IdParameterSet
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet " **Get-AzPolicyAssignment** " ruft alle Richtlinienzuweisungen oder bestimmte Aufgaben ab.
Identifizieren Sie eine Richtlinien Aufgabe, die nach Name und Bereich oder nach ID abgerufen werden soll.

## Beispiele

### Beispiel 1: Abrufen aller Richtlinienzuweisungen
```
PS C:\> Get-AzPolicyAssignment
```

Mit diesem Befehl werden alle Richtlinienzuweisungen abgerufen.

### Beispiel 2: Abrufen einer bestimmten Richtlinienzuweisung
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

Der erste Befehl ruft eine Ressourcengruppe mit dem Namen "ResourceGroup11" ab, indem der Get-AzResourceGroup cmdletand in der $ResourceGroup-Variablen speichert.
Der zweite Befehl ruft die Richtlinienzuweisung mit dem Namen "PolicyAssignment07" für den Bereich ab **, den die Eigenschaft "** Eigenschaften" von $ResourceGroup identifiziert.

### Beispiel 3: Abrufen aller einer Verwaltungsgruppe zugewiesenen Richtlinienzuweisungen
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

Der erste Befehl gibt die ID der zu abfragenden Verwaltungsgruppe an.
Der zweite Befehl ruft alle Richtlinienzuweisungen ab, die der Verwaltungsgruppe mit der ID "mymanagegroup" zugewiesen sind.

## Parameter

### -ApiVersion
Gibt die Version der zu verwendenden Ressourcenanbieter-API an.
Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ID
Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuweisung an, die dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -IncludeDescendent
Bewirkt, dass in der Liste der zurückgegebenen Richtlinienzuweisungen alle Aufgaben im Zusammenhang mit dem angegebenen Bereich eingeschlossen werden, einschließlich derer aus übergeordneten Bereichen und aus untergeordneten Bereichen.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IncludeDescendentParameterSet
Aliases:

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
Type: System.Management.Automation.ActionPreference
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
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name
Gibt den Namen der Richtlinien Aufgabe an, die dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinitionId
Gibt die ID der Richtliniendefinition für die Richtlinienzuweisungen an, die dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Pre
Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.

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
Gibt den Bereich an, auf dem die Richtlinie für die Aufgabe angewendet wird, die dieses Cmdlet erhält.

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IncludeDescendentParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Neu – AzPolicyAssignment](./New-AzPolicyAssignment.md)

[Remove-AzPolicyAssignment](./Remove-AzPolicyAssignment.md)

[Satz-AzPolicyAssignment](./Set-AzPolicyAssignment.md)


