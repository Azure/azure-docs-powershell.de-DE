---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 63efc580cf47274363f04750dc6a3f8da93b6665
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357985"
---
# New-AzPolicyAssignment

## SYNOPSIS
Erstellt eine Richtlinienzuweisung.

## SYNTAX

### DefaultParameterSet (Standard)
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>]
 [-PolicySetDefinition <PsPolicySetDefinition>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyParameterObjectParameterSet
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicyParameterStringParameterSet
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetParameterObjectParameterSet
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### PolicySetParameterStringParameterSet
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## BESCHREIBUNG
Das **Cmdlet "New-AzPolicyAssignment"** erstellt eine Richtlinienzuweisung.
Geben Sie eine Richtlinie und einen Bereich an.

## BEISPIELE

### Beispiel 1: Richtlinienzuweisung auf Abonnementebene
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

Der erste Befehl ruft mithilfe des Cmdlets "Get-AzSubscription" ein Abonnement namens "Subscription01" ab und speichert es in der $Subscription Variable.
Der zweite Befehl ruft die Richtliniendefinition namens "VirtualMachinePolicy" mithilfe des cmdlets Get-AzPolicyDefinition ab und speichert sie in der $Policy Variable.
Der letzte Befehl weist die Richtlinie in $Policy auf der Ebene des Abonnements zu, das durch die Zeichenfolge des Abonnementbereichs identifiziert wird.

### Beispiel 2: Richtlinienzuordnung auf Ressourcengruppenebene
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

Der erste Befehl ruft eine Ressourcengruppe namens "ResourceGroup11" mithilfe des cmdlets Get-AzResourceGroup ab und speichert sie in der $ResourceGroup Variable.
Der zweite Befehl ruft die Richtliniendefinition namens "VirtualMachinePolicy" mithilfe des cmdlets Get-AzPolicyDefinition ab und speichert sie in der $Policy Variable.
Der letzte Befehl weist die Richtlinie in $Policy auf der Ebene der Ressourcengruppe zu, die durch die Eigenschaft **"ResourceId"** von "$ResourceGroup.

### Beispiel 3: Richtlinienzuordnung auf Ressourcengruppenebene mit Richtlinienparameterobjekt
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

Der erste Befehl ruft mithilfe des Cmdlets "ResourceGroup11" Get-AzResourceGroup Ressourcengruppe ab.
Der Befehl speichert dieses Objekt in der $ResourceGroup Variable.
Der zweite Befehl ruft die integrierte Richtliniendefinition für zulässige Speicherorte mithilfe des cmdlets Get-AzPolicyDefinition ab.
Der Befehl speichert dieses Objekt in der $Policy Variable.
Mit dem dritten und vierten Befehl wird ein Objekt erstellt, das alle Azure-Regionen mit "ost" im Namen enthält.
Die Befehle speichern dieses Objekt in der $AllowedLocations Variable.
Der letzte Befehl weist die Richtlinie in $Policy auf Ebene einer Ressourcengruppe mit dem Richtlinienparameterobjekt in der Gruppe $AllowedLocations.
Die **Eigenschaft "ResourceId"** von $ResourceGroup die Ressourcengruppe an.

### Beispiel 4: Richtlinienzuordnung auf Ressourcengruppenebene mit Richtlinienparameterdatei
Erstellen Sie eine Datei _namensAllowedLocations.jsim_ lokalen Arbeitsverzeichnis mit den folgenden Inhalten.

```
{
    "listOfAllowedLocations":  {
      "value": [
        "westus",
        "westeurope",
        "japanwest"
      ]
    }
}
```

```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

Der erste Befehl ruft eine Ressourcengruppe namens "ResourceGroup11" mithilfe des cmdlets Get-AzResourceGroup ab und speichert sie in der $ResourceGroup Variable.
Der zweite Befehl ruft die integrierte Richtliniendefinition für zulässige Speicherorte mithilfe des cmdlets Get-AzPolicyDefinition ab und speichert sie in der $Policy Variable.
Der letzte Befehl weist die Richtlinie in $Policy der Ressourcengruppe zu, die durch die Eigenschaft **"ResourceId"** von $ResourceGroup mithilfe der Richtlinienparameterdatei AllowedLocations.jsaus dem lokalen Arbeitsverzeichnis identifiziert wird.

### Beispiel 5: Richtlinienzuweisung mit verwalteter Identität
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

Der erste Befehl ruft eine Ressourcengruppe namens "ResourceGroup11" mithilfe des cmdlets Get-AzResourceGroup ab und speichert sie in der $ResourceGroup Variable.
Der zweite Befehl ruft die Richtliniendefinition namens "VirtualMachinePolicy" mithilfe des cmdlets Get-AzPolicyDefinition ab und speichert sie in der $Policy Variable.
Der letzte Befehl weist der Ressourcengruppe $Policy Richtlinie in der Gruppe zu. Eine verwaltete Identität wird automatisch erstellt und der Richtlinienzuweisung zugewiesen.

### Beispiel 6: Richtlinienzuweisung mit einer Erzwingungsmoduseigenschaft
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

Der erste Befehl ruft mithilfe des Cmdlets "Get-AzSubscription" ein Abonnement namens "Subscription01" ab und speichert es in der $Subscription Variable.
Der zweite Befehl ruft die Richtliniendefinition namens "VirtualMachinePolicy" mithilfe des cmdlets Get-AzPolicyDefinition ab und speichert sie in der $Policy Variable.
Der letzte Befehl weist die Richtlinie in $Policy auf der Ebene des Abonnements zu, das durch die Zeichenfolge des Abonnementbereichs identifiziert wird. Die Zuordnung wird mit dem Wert "EnforcementMode" von _"DoNotEnforce"_ festgelegt, d. h., der Richtlinieneffekt wird während der Ressourcenerstellung oder -aktualisierung nicht erzwungen.

## PARAMETERS

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

### -AssignIdentity
Generieren und zuweisen Sie eine Azure Active Directory-Identität für diese Richtlinienzuweisung. Die Identität wird beim Ausführen von Bereitstellungen für "deployIfNotExists"-Richtlinien verwendet. Der Standort ist erforderlich, wenn Sie eine Identität zuweisen.

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

### -Beschreibung
Beschreibung der Richtlinienzuweisung

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

### -DisplayName
Gibt einen Anzeigenamen für die Richtlinienzuweisung an.

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

### -EnforcementMode
Der Erzwingungsmodus für die Richtlinienzuweisung. Derzeit sind gültige Werte "Standard", "DoNotEnforce".

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyAssignmentEnforcementMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, DoNotEnforce

Required: False
Position: Named
Default value: Default
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Location
Der Speicherort der Ressourcenidentität der Richtlinienzuordnung. Dies ist erforderlich, wenn der Schalter "-AssignIdentity" verwendet wird.

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

### -Metadata
Die Metadaten für die neue Richtlinienzuweisung. Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.

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

### -Name
Gibt einen Namen für die Richtlinienzuordnung an.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NotScope
Dies sind keine Bereiche für die Richtlinienzuordnung.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyDefinition
Gibt eine Richtlinie als ein **"PsPolicyDefinition"-Objekt** an, das die Richtlinienregel enthält.

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyParameter
Der Dateipfad des Richtlinienparameters oder die Parameterzeichenfolge der Richtlinie.

```yaml
Type: System.String
Parameter Sets: PolicyParameterStringParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -PolicyParameterObject
Das Richtlinienparameterobjekt.

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterObjectParameterSet, PolicySetParameterObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -PolicySetDefinition
Das Richtliniensatzdefinitionsobjekt.

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
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

### -Scope
Gibt den Bereich an, für den die Richtlinie zugewiesen werden soll.
Wenn Sie beispielsweise einer Ressourcengruppe eine Richtlinie zuweisen möchten, geben Sie Folgendes an: Name der `/subscriptions/` Ressourcengruppe "Abonnement-ID". `/resourcegroups/`

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

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable. Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## EINGABEN

### System.String

### System.String[]

### System.Management.Automation.PSObject

## AUSGABEN

### System.Management.Automation.PSObject

## HINWEISE

## LINKS ZU VERWANDTEN THEMEN

[Get-AzPolicyDefinition](./Get-AzPolicyDefinition.md)

[Get-AzPolicyAssignment](./Get-AzPolicyAssignment.md)

[Remove-AzPolicyAssignment](./Remove-AzPolicyAssignment.md)

[Set-AzPolicyAssignment](./Set-AzPolicyAssignment.md)


