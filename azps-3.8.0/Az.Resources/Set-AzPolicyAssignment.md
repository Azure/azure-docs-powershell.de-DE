---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: ab0617b4012ca623bf67471a9a5bcc3ccf54d905
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996438"
---
# <span data-ttu-id="65f3d-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="65f3d-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="65f3d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65f3d-102">SYNOPSIS</span></span>
<span data-ttu-id="65f3d-103">Ändert eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="65f3d-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="65f3d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65f3d-104">SYNTAX</span></span>

### <span data-ttu-id="65f3d-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="65f3d-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65f3d-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65f3d-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65f3d-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="65f3d-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65f3d-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="65f3d-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65f3d-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="65f3d-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65f3d-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="65f3d-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65f3d-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65f3d-111">DESCRIPTION</span></span>
<span data-ttu-id="65f3d-112">Das Cmdlet " **festlegen-AzPolicyAssignment** " ändert eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="65f3d-112">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="65f3d-113">Geben Sie eine Zuordnung nach ID oder nach Name und Bereich an.</span><span class="sxs-lookup"><span data-stu-id="65f3d-113">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="65f3d-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65f3d-114">EXAMPLES</span></span>

### <span data-ttu-id="65f3d-115">Beispiel 1: Aktualisieren des Anzeigenamens</span><span class="sxs-lookup"><span data-stu-id="65f3d-115">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="65f3d-116">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="65f3d-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="65f3d-117">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="65f3d-117">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="65f3d-118">Der zweite Befehl ruft die Richtlinienzuweisung mit dem Namen PolicyAssignment mithilfe des Get-AzPolicyAssignment-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="65f3d-118">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="65f3d-119">Der Befehl speichert das Objekt in der $PolicyAssignment Variablen.</span><span class="sxs-lookup"><span data-stu-id="65f3d-119">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="65f3d-120">Der endgültige Befehl aktualisiert den Anzeigenamen in der Richtlinienzuweisung in der Ressourcengruppe, die von der Eigenschaft " **Resourcen** -Wert" von $ResourceGroup angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="65f3d-120">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="65f3d-121">Beispiel 2: Hinzufügen einer verwalteten Identität zur Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="65f3d-121">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="65f3d-122">Der erste Befehl ruft mithilfe des Get-AzPolicyAssignment-Cmdlets die Richtlinienzuweisung mit dem Namen PolicyAssignment aus dem aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="65f3d-122">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="65f3d-123">Der Befehl speichert das Objekt in der $PolicyAssignment Variablen.</span><span class="sxs-lookup"><span data-stu-id="65f3d-123">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="65f3d-124">Der endgültige Befehl weist der Richtlinienzuweisung eine verwaltete Identität zu.</span><span class="sxs-lookup"><span data-stu-id="65f3d-124">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="65f3d-125">Beispiel 3: Aktualisieren von Richtlinien Zuordnungs Parametern mit dem neuen Richtlinienparameter Objekt</span><span class="sxs-lookup"><span data-stu-id="65f3d-125">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="65f3d-126">Der erste und der zweite Befehl erstellen ein Objekt, das alle Azure-Bereiche enthält, deren Namen mit "Frankreich" oder "UK" beginnen.</span><span class="sxs-lookup"><span data-stu-id="65f3d-126">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="65f3d-127">Der zweite Befehl speichert das Objekt in der $AllowedLocations Variablen.</span><span class="sxs-lookup"><span data-stu-id="65f3d-127">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="65f3d-128">Der dritte Befehl ruft die Richtlinienzuweisung mit dem Namen "PolicyAssignment" ab, wobei der Befehl das Objekt in der $PolicyAssignment Variablen speichert.</span><span class="sxs-lookup"><span data-stu-id="65f3d-128">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="65f3d-129">Der endgültige Befehl aktualisiert die Parameterwerte für die Richtlinienzuweisung mit dem Namen PolicyAssignment.</span><span class="sxs-lookup"><span data-stu-id="65f3d-129">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="65f3d-130">Beispiel 4: Aktualisieren von Richtlinien Zuordnungs Parametern mit Richtlinienparameter Datei</span><span class="sxs-lookup"><span data-stu-id="65f3d-130">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="65f3d-131">Erstellen Sie eine Datei mit dem Namen _AllowedLocations.js_ im lokalen Arbeitsverzeichnis mit folgendem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="65f3d-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

```
{
    "listOfAllowedLocations":  {
      "value": [
        "uksouth",
        "ukwest",
        "francecentral",
        "francesouth"
      ]
    }
}
```

```
PS C:\> Set-AzPolicyAssignment -Name 'PolicyAssignment' -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="65f3d-132">Der Befehl aktualisiert die Richtlinien Aufgabe mit dem Namen "PolicyAssignment" mithilfe der Richtlinienparameter Datei AllowedLocations.jsaus dem lokalen Arbeitsverzeichnis.</span><span class="sxs-lookup"><span data-stu-id="65f3d-132">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="65f3d-133">Beispiel 5: Aktualisieren eines enforcementMode</span><span class="sxs-lookup"><span data-stu-id="65f3d-133">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="65f3d-134">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="65f3d-134">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="65f3d-135">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="65f3d-135">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="65f3d-136">Der zweite Befehl ruft die Richtlinienzuweisung mit dem Namen PolicyAssignment mithilfe des Get-AzPolicyAssignment-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="65f3d-136">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="65f3d-137">Der Befehl speichert das Objekt in der $PolicyAssignment Variablen.</span><span class="sxs-lookup"><span data-stu-id="65f3d-137">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="65f3d-138">Der endgültige Befehl aktualisiert die enforcementMode-Eigenschaft für die Richtlinienzuweisung in der Ressourcengruppe, die von der Eigenschaft " **Resourcen** -Wert" von $ResourceGroup angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="65f3d-138">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="65f3d-139">Parameter</span><span class="sxs-lookup"><span data-stu-id="65f3d-139">PARAMETERS</span></span>

### <span data-ttu-id="65f3d-140">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="65f3d-140">-ApiVersion</span></span>
<span data-ttu-id="65f3d-141">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="65f3d-141">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="65f3d-142">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="65f3d-142">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="65f3d-143">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="65f3d-143">-AssignIdentity</span></span>
<span data-ttu-id="65f3d-144">Generieren Sie eine Azure Active Directory-Identität für diese Richtlinienzuweisung, und weisen Sie diese zu.</span><span class="sxs-lookup"><span data-stu-id="65f3d-144">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="65f3d-145">Die Identität wird verwendet, wenn Bereitstellungen für "deployIfNotExists"-Richtlinien ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="65f3d-145">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="65f3d-146">Beim Zuweisen einer Identität ist ein Speicherort erforderlich.</span><span class="sxs-lookup"><span data-stu-id="65f3d-146">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="65f3d-147">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65f3d-147">-DefaultProfile</span></span>
<span data-ttu-id="65f3d-148">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="65f3d-148">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="65f3d-149">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65f3d-149">-Description</span></span>
<span data-ttu-id="65f3d-150">Die Beschreibung für die Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="65f3d-150">The description for policy assignment</span></span>

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

### <span data-ttu-id="65f3d-151">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="65f3d-151">-DisplayName</span></span>
<span data-ttu-id="65f3d-152">Gibt einen neuen Anzeigenamen für die Richtlinienzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="65f3d-152">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="65f3d-153">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="65f3d-153">-EnforcementMode</span></span>
<span data-ttu-id="65f3d-154">Der Erzwingungsmodus für die Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="65f3d-154">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="65f3d-155">Gültige Werte sind derzeit Standard, DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="65f3d-155">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="65f3d-156">-ID</span><span class="sxs-lookup"><span data-stu-id="65f3d-156">-Id</span></span>
<span data-ttu-id="65f3d-157">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuweisung an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="65f3d-157">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet, PolicyParameterIdObjectParameterSet, PolicyParameterIdStringParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65f3d-158">-Standort</span><span class="sxs-lookup"><span data-stu-id="65f3d-158">-Location</span></span>
<span data-ttu-id="65f3d-159">Der Speicherort der Ressourcen Identität der Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="65f3d-159">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="65f3d-160">Dies ist erforderlich, wenn der-AssignIdentity-Schalter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="65f3d-160">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="65f3d-161">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="65f3d-161">-Metadata</span></span>
<span data-ttu-id="65f3d-162">Die aktualisierten Metadaten für die Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="65f3d-162">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="65f3d-163">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="65f3d-163">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="65f3d-164">-Name</span><span class="sxs-lookup"><span data-stu-id="65f3d-164">-Name</span></span>
<span data-ttu-id="65f3d-165">Gibt den Namen der Richtlinien Aufgabe an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="65f3d-165">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65f3d-166">-NotScope</span><span class="sxs-lookup"><span data-stu-id="65f3d-166">-NotScope</span></span>
<span data-ttu-id="65f3d-167">Die Richtlinienzuweisung nicht Bereiche.</span><span class="sxs-lookup"><span data-stu-id="65f3d-167">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="65f3d-168">-Policyparameter</span><span class="sxs-lookup"><span data-stu-id="65f3d-168">-PolicyParameter</span></span>
<span data-ttu-id="65f3d-169">Der neue Richtlinienparameter-Dateipfad oder die Zeichenfolge für die Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="65f3d-169">The new policy parameters file path or string for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterNameStringParameterSet, PolicyParameterIdStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65f3d-170">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="65f3d-170">-PolicyParameterObject</span></span>
<span data-ttu-id="65f3d-171">Das neue Richtlinienparameter-Objekt für die Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="65f3d-171">The new policy parameters object for the policy assignment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterNameObjectParameterSet, PolicyParameterIdObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65f3d-172">-Pre</span><span class="sxs-lookup"><span data-stu-id="65f3d-172">-Pre</span></span>
<span data-ttu-id="65f3d-173">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="65f3d-173">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="65f3d-174">-Scope</span><span class="sxs-lookup"><span data-stu-id="65f3d-174">-Scope</span></span>
<span data-ttu-id="65f3d-175">Gibt den Bereich an, auf dem die Richtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="65f3d-175">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65f3d-176">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65f3d-176">CommonParameters</span></span>
<span data-ttu-id="65f3d-177">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65f3d-177">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65f3d-178">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="65f3d-178">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65f3d-179">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65f3d-179">INPUTS</span></span>

### <span data-ttu-id="65f3d-180">System. String</span><span class="sxs-lookup"><span data-stu-id="65f3d-180">System.String</span></span>

### <span data-ttu-id="65f3d-181">System. String []</span><span class="sxs-lookup"><span data-stu-id="65f3d-181">System.String[]</span></span>

## <span data-ttu-id="65f3d-182">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65f3d-182">OUTPUTS</span></span>

### <span data-ttu-id="65f3d-183">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="65f3d-183">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="65f3d-184">Notizen</span><span class="sxs-lookup"><span data-stu-id="65f3d-184">NOTES</span></span>

## <span data-ttu-id="65f3d-185">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65f3d-185">RELATED LINKS</span></span>

[<span data-ttu-id="65f3d-186">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="65f3d-186">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="65f3d-187">Neu – AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="65f3d-187">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="65f3d-188">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="65f3d-188">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


