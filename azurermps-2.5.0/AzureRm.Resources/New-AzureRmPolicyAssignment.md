---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: 6183d4b8da931836a1ec613c113b32c71871bbf2
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850267"
---
# New-AzureRmPolicyAssignment

## Synopsis
Erstellt eine Richtlinienzuordnung.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## Syntax

### DefaultParameterSet (Standard)
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### PolicyParameterObjectParameterSet
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### PolicyParameterStringParameterSet
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### PolicySetParameterObjectParameterSet
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### PolicySetParameterStringParameterSet
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Beschreibung
Das Cmdlet **New-AzureRmPolicyAssignment** erstellt eine Richtlinienzuordnung.
Geben Sie eine Richtlinie und einen Bereich an.

## Beispiele

### Beispiel 1: Richtlinienzuweisung auf Ressourcengruppen Ebene
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzureRmPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzureRMResourceGroup-Cmdlets ab und speichert Sie in der Variablen $ResourceGroup.
Der zweite Befehl ruft die Richtliniendefinition mit dem Namen VirtualMachinePolicy mithilfe des Get-AzureRmPolicyDefinition-Cmdlets ab und speichert Sie in der $Policy-Variablen.
Der endgültige Befehl weist die Richtlinie in $Policy auf der Ebene der Ressourcengruppe zu, die von der Eigenschaft " **Resourcen** " von $ResourceGroup identifiziert wurde.

### Beispiel 2: Richtlinienzuweisung auf Ressourcengruppen Ebene mit Richtlinienparameter Objekt
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzureRmLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzureRmPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzureRMResourceGroup-Cmdlets ab.
Der Befehl speichert das Objekt in der $ResourceGroup Variablen.
Der zweite Befehl ruft die integrierte Richtliniendefinition für zulässige Speicherorte mithilfe des Get-AzureRmPolicyDefinition-Cmdlets ab.
Der Befehl speichert das Objekt in der $Policy Variablen.
Der dritte und der vierte Befehl erstellen ein Objekt, das alle Azure-Bereiche mit "Ost" im Namen enthält.
Die Befehle Speichern dieses Objekt in der $AllowedLocations Variablen.
Der endgültige Befehl weist die Richtlinie in $Policy auf der Ebene einer Ressourcengruppe mithilfe des Richtlinienparameter Objekts in $AllowedLocations zu.
Die **Resourcen** -Eigenschaft von $ResourceGroup identifiziert die Ressourcengruppe.

### Beispiel 3: Richtlinienzuweisung auf Ressourcengruppen Ebene mit Richtlinienparameter Datei
Erstellen Sie eine Datei mit dem Namen _AllowedLocations.js_ im lokalen Arbeitsverzeichnis mit folgendem Inhalt.

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
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> New-AzureRmPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzureRMResourceGroup-Cmdlets ab und speichert Sie in der Variablen $ResourceGroup.
Der zweite Befehl ruft die integrierte Richtliniendefinition für zulässige Speicherorte mithilfe des Get-AzureRmPolicyDefinition-Cmdlets ab und speichert Sie in der $Policy-Variablen.
Der endgültige Befehl weist die Richtlinie in $Policy der Ressourcengruppe zu, die von der Eigenschaft " **Resourcen** " von $ResourceGroup mithilfe der Richtlinienparameter Datei AllowedLocations.jsauf aus dem lokalen Arbeitsverzeichnis festgelegt wurde.

### Beispiel 4: Richtlinienzuweisung mit einer verwalteten Identität
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzureRmPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity 
```

Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzureRMResourceGroup-Cmdlets ab und speichert Sie in der Variablen $ResourceGroup.
Der zweite Befehl ruft die Richtliniendefinition mit dem Namen VirtualMachinePolicy mithilfe des Get-AzureRmPolicyDefinition-Cmdlets ab und speichert Sie in der $Policy-Variablen.
Der endgültige Befehl weist die Richtlinie in $Policy der Ressourcengruppe zu. Eine verwaltete Identität wird automatisch erstellt und der Richtlinien Aufgabe zugewiesen.

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

### -AssignIdentity
Generieren Sie eine Azure Active Directory-Identität für diese Richtlinienzuweisung, und weisen Sie diese zu. Die Identität wird verwendet, wenn Bereitstellungen für "deployIfNotExists"-Richtlinien ausgeführt werden. Beim Zuweisen einer Identität ist ein Speicherort erforderlich.

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
Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement

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

### -Beschreibung
Die Beschreibung für die Richtlinienzuweisung

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
Gibt einen Anzeigenamen für die Richtlinienzuordnung an.

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

### -Standort
Der Speicherort der Ressourcen Identität der Richtlinienzuordnung. Dies ist erforderlich, wenn der-AssignIdentity-Schalter verwendet wird.

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

### -Metadaten
Die Metadaten für die neue Richtlinienzuordnung. Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.

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
Die nicht-Bereiche für die Richtlinienzuweisung.

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
Gibt eine Richtlinie als **PsPolicyDefinition** -Objekt an, das die Richtlinienregel enthält.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Policyparameter
Der Richtlinienparameter-Dateipfad oder die Richtlinienparameter-Zeichenfolge.

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
Das Richtlinienparameter-Objekt.

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
Das Richtliniensatz-Definitionsobjekt.

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
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
Wenn Sie beispielsweise einer Ressourcengruppe eine Richtlinie zuweisen möchten, geben Sie Folgendes an: `/subscriptions/` Abonnement-ID- `/resourcegroups/` Ressourcengruppenname

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

### -SKU
Eine Hashtabelle, die SKU-Eigenschaften darstellt. Standardmäßig ist die ﻿kostenlose SKU mit den Werten: `@{Name = 'A0'; Tier = 'Free'}` . Verwenden Sie die Werte:, um die Standard-SKU zu verwenden `@{Name = 'A1'; Tier = 'Standard'}` .

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable. Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## Eingaben

## Ausgaben

## Notizen

## Verwandte Links

[Get-AzureRmPolicyDefinition](./Get-AzureRmPolicyDefinition.md)

[Get-AzureRmPolicyAssignment](./Get-AzureRmPolicyAssignment.md)

[Remove-AzureRmPolicyAssignment](./Remove-AzureRmPolicyAssignment.md)

[Satz-AzureRmPolicyAssignment](./Set-AzureRmPolicyAssignment.md)


