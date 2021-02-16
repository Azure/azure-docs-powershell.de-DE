---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 8efda1a15546a09f0946506f3bc7fd27462b3c03
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100169049"
---
# <span data-ttu-id="782f2-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="782f2-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="782f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="782f2-102">SYNOPSIS</span></span>
<span data-ttu-id="782f2-103">Ändert eine Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="782f2-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="782f2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="782f2-104">SYNTAX</span></span>

### <span data-ttu-id="782f2-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="782f2-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="782f2-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="782f2-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="782f2-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="782f2-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="782f2-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="782f2-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="782f2-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="782f2-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="782f2-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="782f2-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="782f2-111">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="782f2-111">InputObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] -InputObject <PsPolicyAssignment> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="782f2-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="782f2-112">DESCRIPTION</span></span>
<span data-ttu-id="782f2-113">Das **Cmdlet "Set-AzPolicyAssignment"** ändert eine Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="782f2-113">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="782f2-114">Geben Sie eine Zuordnung nach ID oder nach Name und Bereich an.</span><span class="sxs-lookup"><span data-stu-id="782f2-114">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="782f2-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="782f2-115">EXAMPLES</span></span>

### <span data-ttu-id="782f2-116">Beispiel 1: Aktualisieren des Anzeigenamens</span><span class="sxs-lookup"><span data-stu-id="782f2-116">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="782f2-117">Der erste Befehl ruft eine Ressourcengruppe namens "ResourceGroup11" mithilfe des cmdlets Get-AzResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="782f2-117">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="782f2-118">Der Befehl speichert dieses Objekt in der $ResourceGroup Variable.</span><span class="sxs-lookup"><span data-stu-id="782f2-118">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="782f2-119">Der zweite Befehl ruft die Richtlinienzuweisung mit dem Namen "PolicyAssignment" mithilfe des cmdlets Get-AzPolicyAssignment ab.</span><span class="sxs-lookup"><span data-stu-id="782f2-119">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="782f2-120">Der Befehl speichert dieses Objekt in der $PolicyAssignment Variable.</span><span class="sxs-lookup"><span data-stu-id="782f2-120">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="782f2-121">Der letzte Befehl aktualisiert den Anzeigenamen für die Richtlinienzuordnung für die Ressourcengruppe, die durch die Eigenschaft **"ResourceId" von "$ResourceGroup.**</span><span class="sxs-lookup"><span data-stu-id="782f2-121">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="782f2-122">Beispiel 2: Hinzufügen einer verwalteten Identität zur Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="782f2-122">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="782f2-123">Der erste Befehl ruft die Richtlinienzuweisung mit dem Namen "PolicyAssignment" aus dem aktuellen Abonnement mit dem cmdlet Get-AzPolicyAssignment ab.</span><span class="sxs-lookup"><span data-stu-id="782f2-123">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="782f2-124">Der Befehl speichert dieses Objekt in der $PolicyAssignment Variable.</span><span class="sxs-lookup"><span data-stu-id="782f2-124">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="782f2-125">Der letzte Befehl weist der Richtlinienzuweisung eine verwaltete Identität zu.</span><span class="sxs-lookup"><span data-stu-id="782f2-125">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="782f2-126">Beispiel 3: Aktualisieren von Richtlinienzuordnungsparametern mit einem neuen Richtlinienparameterobjekt</span><span class="sxs-lookup"><span data-stu-id="782f2-126">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="782f2-127">Mit dem ersten und zweiten Befehl wird ein Objekt erstellt, das alle Azure-Regionen enthält, deren Namen mit "france" oder "uk" beginnen.</span><span class="sxs-lookup"><span data-stu-id="782f2-127">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="782f2-128">Der zweite Befehl speichert dieses Objekt in der $AllowedLocations Variable.</span><span class="sxs-lookup"><span data-stu-id="782f2-128">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="782f2-129">Der dritte Befehl ruft die Richtlinienzuweisung namens "PolicyAssignment" ab. Der Befehl speichert dieses Objekt in der $PolicyAssignment Variable.</span><span class="sxs-lookup"><span data-stu-id="782f2-129">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="782f2-130">Der letzte Befehl aktualisiert die Parameterwerte für die Richtlinienzuweisung namens "PolicyAssignment".</span><span class="sxs-lookup"><span data-stu-id="782f2-130">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="782f2-131">Beispiel 4: Aktualisieren von Richtlinienzuordnungsparametern mit der Richtlinienparameterdatei</span><span class="sxs-lookup"><span data-stu-id="782f2-131">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="782f2-132">Erstellen Sie eine Datei _namensAllowedLocations.jsim_ lokalen Arbeitsverzeichnis mit den folgenden Inhalten.</span><span class="sxs-lookup"><span data-stu-id="782f2-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="782f2-133">Der Befehl aktualisiert die Richtlinienzuweisung namens "PolicyAssignment" mithilfe der Richtlinienparameterdatei, AllowedLocations.jsaus dem lokalen Arbeitsverzeichnis gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="782f2-133">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="782f2-134">Beispiel 5: Aktualisieren eines enforcementMode</span><span class="sxs-lookup"><span data-stu-id="782f2-134">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="782f2-135">Der erste Befehl ruft eine Ressourcengruppe namens "ResourceGroup11" mithilfe des cmdlets Get-AzResourceGroup ab.</span><span class="sxs-lookup"><span data-stu-id="782f2-135">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="782f2-136">Der Befehl speichert dieses Objekt in der $ResourceGroup Variable.</span><span class="sxs-lookup"><span data-stu-id="782f2-136">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="782f2-137">Der zweite Befehl ruft die Richtlinienzuweisung mit dem Namen "PolicyAssignment" mithilfe des cmdlets Get-AzPolicyAssignment ab.</span><span class="sxs-lookup"><span data-stu-id="782f2-137">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="782f2-138">Der Befehl speichert dieses Objekt in der $PolicyAssignment Variable.</span><span class="sxs-lookup"><span data-stu-id="782f2-138">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="782f2-139">Der letzte Befehl aktualisiert die "enforcementMode"-Eigenschaft für die Richtlinienzuordnung für die Ressourcengruppe, die durch die **Eigenschaft "ResourceId"** der Gruppe "$ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="782f2-139">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="782f2-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="782f2-140">PARAMETERS</span></span>

### <span data-ttu-id="782f2-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="782f2-141">-ApiVersion</span></span>
<span data-ttu-id="782f2-142">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="782f2-142">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="782f2-143">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="782f2-143">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="782f2-144">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="782f2-144">-AssignIdentity</span></span>
<span data-ttu-id="782f2-145">Generieren und zuweisen Sie eine Azure Active Directory-Identität für diese Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="782f2-145">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="782f2-146">Die Identität wird beim Ausführen von Bereitstellungen für "deployIfNotExists"-Richtlinien verwendet.</span><span class="sxs-lookup"><span data-stu-id="782f2-146">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="782f2-147">Der Standort ist erforderlich, wenn Sie eine Identität zuweisen.</span><span class="sxs-lookup"><span data-stu-id="782f2-147">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="782f2-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="782f2-148">-DefaultProfile</span></span>
<span data-ttu-id="782f2-149">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="782f2-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="782f2-150">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="782f2-150">-Description</span></span>
<span data-ttu-id="782f2-151">Beschreibung der Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="782f2-151">The description for policy assignment</span></span>

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

### <span data-ttu-id="782f2-152">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="782f2-152">-DisplayName</span></span>
<span data-ttu-id="782f2-153">Gibt einen neuen Anzeigenamen für die Richtlinienzuweisung an.</span><span class="sxs-lookup"><span data-stu-id="782f2-153">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="782f2-154">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="782f2-154">-EnforcementMode</span></span>
<span data-ttu-id="782f2-155">Der Erzwingungsmodus für die Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="782f2-155">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="782f2-156">Derzeit sind gültige Werte "Standard", "DoNotEnforce".</span><span class="sxs-lookup"><span data-stu-id="782f2-156">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="782f2-157">-ID</span><span class="sxs-lookup"><span data-stu-id="782f2-157">-Id</span></span>
<span data-ttu-id="782f2-158">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuordnung an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="782f2-158">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="782f2-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="782f2-159">-InputObject</span></span>
<span data-ttu-id="782f2-160">Das zu aktualisierende Richtlinienzuweisungsobjekt, das von einem anderen Cmdlet ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="782f2-160">The policy assignment object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="782f2-161">-Location</span><span class="sxs-lookup"><span data-stu-id="782f2-161">-Location</span></span>
<span data-ttu-id="782f2-162">Der Speicherort der Ressourcenidentität der Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="782f2-162">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="782f2-163">Dies ist erforderlich, wenn der Schalter "-AssignIdentity" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="782f2-163">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="782f2-164">-Metadata</span><span class="sxs-lookup"><span data-stu-id="782f2-164">-Metadata</span></span>
<span data-ttu-id="782f2-165">Die aktualisierten Metadaten für die Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="782f2-165">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="782f2-166">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="782f2-166">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="782f2-167">-Name</span><span class="sxs-lookup"><span data-stu-id="782f2-167">-Name</span></span>
<span data-ttu-id="782f2-168">Gibt den Namen der Richtlinienzuweisung an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="782f2-168">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="782f2-169">-NotScope</span><span class="sxs-lookup"><span data-stu-id="782f2-169">-NotScope</span></span>
<span data-ttu-id="782f2-170">Die Richtlinienzuweisung keine Bereiche.</span><span class="sxs-lookup"><span data-stu-id="782f2-170">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="782f2-171">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="782f2-171">-PolicyParameter</span></span>
<span data-ttu-id="782f2-172">Der dateipfad oder die neue Zeichenfolge für die Richtlinienzuweisung für die Richtlinienparameter.</span><span class="sxs-lookup"><span data-stu-id="782f2-172">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="782f2-173">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="782f2-173">-PolicyParameterObject</span></span>
<span data-ttu-id="782f2-174">Das neue Richtlinienparameterobjekt für die Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="782f2-174">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="782f2-175">-Pre</span><span class="sxs-lookup"><span data-stu-id="782f2-175">-Pre</span></span>
<span data-ttu-id="782f2-176">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="782f2-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="782f2-177">-Scope</span><span class="sxs-lookup"><span data-stu-id="782f2-177">-Scope</span></span>
<span data-ttu-id="782f2-178">Gibt den Bereich an, auf den die Richtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="782f2-178">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="782f2-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="782f2-179">CommonParameters</span></span>
<span data-ttu-id="782f2-180">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="782f2-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="782f2-181">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="782f2-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="782f2-182">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="782f2-182">INPUTS</span></span>

### <span data-ttu-id="782f2-183">System.String</span><span class="sxs-lookup"><span data-stu-id="782f2-183">System.String</span></span>

### <span data-ttu-id="782f2-184">System.String[]</span><span class="sxs-lookup"><span data-stu-id="782f2-184">System.String[]</span></span>

## <span data-ttu-id="782f2-185">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="782f2-185">OUTPUTS</span></span>

### <span data-ttu-id="782f2-186">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="782f2-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="782f2-187">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="782f2-187">NOTES</span></span>

## <span data-ttu-id="782f2-188">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="782f2-188">RELATED LINKS</span></span>

[<span data-ttu-id="782f2-189">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="782f2-189">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="782f2-190">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="782f2-190">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="782f2-191">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="782f2-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


