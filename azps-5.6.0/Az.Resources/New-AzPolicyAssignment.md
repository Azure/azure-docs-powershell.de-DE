---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: d1e6b5b2b2e76c4ec807c27922f9ce577d94a7d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928936"
---
# <span data-ttu-id="627fb-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="627fb-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="627fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="627fb-102">SYNOPSIS</span></span>
<span data-ttu-id="627fb-103">Erstellt eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="627fb-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="627fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="627fb-104">SYNTAX</span></span>

### <span data-ttu-id="627fb-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="627fb-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>]
 [-PolicySetDefinition <PsPolicySetDefinition>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="627fb-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="627fb-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="627fb-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="627fb-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="627fb-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="627fb-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="627fb-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="627fb-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="627fb-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="627fb-110">DESCRIPTION</span></span>
<span data-ttu-id="627fb-111">Das **Cmdlet New-AzPolicyAssignment** erstellt eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="627fb-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="627fb-112">Geben Sie eine Richtlinie und einen Bereich an.</span><span class="sxs-lookup"><span data-stu-id="627fb-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="627fb-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="627fb-113">EXAMPLES</span></span>

### <span data-ttu-id="627fb-114">Beispiel 1: Richtlinienzuweisung auf Abonnementebene</span><span class="sxs-lookup"><span data-stu-id="627fb-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="627fb-115">Der erste Befehl ruft ein Abonnement mit dem Namen Abonnement01 mithilfe des cmdlets Get-AzSubscription ab und speichert es in der $Subscription Variablen.</span><span class="sxs-lookup"><span data-stu-id="627fb-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="627fb-116">Der zweite Befehl ruft die Richtliniendefinition virtualMachinePolicy ab, indem er das cmdlet Get-AzPolicyDefinition verwendet und in der $Policy speichert.</span><span class="sxs-lookup"><span data-stu-id="627fb-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="627fb-117">Der letzte Befehl weist die Richtlinie $Policy auf der Ebene des Abonnements zu, das durch die Zeichenfolge des Abonnementbereichs identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="627fb-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="627fb-118">Beispiel 2: Richtlinienzuordnung auf Ressourcengruppenebene</span><span class="sxs-lookup"><span data-stu-id="627fb-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="627fb-119">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 ab, indem er das cmdlet Get-AzResourceGroup verwendet und in der $ResourceGroup speichert.</span><span class="sxs-lookup"><span data-stu-id="627fb-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="627fb-120">Der zweite Befehl ruft die Richtliniendefinition virtualMachinePolicy ab, indem er das cmdlet Get-AzPolicyDefinition verwendet und in der $Policy speichert.</span><span class="sxs-lookup"><span data-stu-id="627fb-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="627fb-121">Der letzte Befehl weist die Richtlinie $Policy auf der Ebene der Ressourcengruppe zu, die durch die **ResourceId-Eigenschaft** von $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="627fb-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="627fb-122">Beispiel 3: Richtlinienzuordnung auf Ressourcengruppenebene mit Richtlinienparameterobjekt</span><span class="sxs-lookup"><span data-stu-id="627fb-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="627fb-123">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 ab, indem er das cmdlet Get-AzResourceGroup verwendet.</span><span class="sxs-lookup"><span data-stu-id="627fb-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="627fb-124">Der Befehl speichert dieses Objekt in der $ResourceGroup-Variable.</span><span class="sxs-lookup"><span data-stu-id="627fb-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="627fb-125">Der zweite Befehl ruft die integrierte Richtliniendefinition für zulässige Speicherorte mithilfe des cmdlets Get-AzPolicyDefinition ab.</span><span class="sxs-lookup"><span data-stu-id="627fb-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="627fb-126">Der Befehl speichert dieses Objekt in der $Policy-Variable.</span><span class="sxs-lookup"><span data-stu-id="627fb-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="627fb-127">Mit dem dritten und vierten Befehl wird ein -Objekt erstellt, das alle Azure-Regionen mit "Ost" im Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="627fb-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="627fb-128">Die Befehle speichern dieses Objekt in der $AllowedLocations Variablen.</span><span class="sxs-lookup"><span data-stu-id="627fb-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="627fb-129">Der letzte Befehl weist die Richtlinie $Policy auf der Ebene einer Ressourcengruppe zu, die das Richtlinienparameterobjekt in $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="627fb-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="627fb-130">Die **ResourceId-Eigenschaft** $ResourceGroup die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="627fb-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="627fb-131">Beispiel 4: Richtlinienzuordnung auf Ressourcengruppenebene mit Richtlinienparameterdatei</span><span class="sxs-lookup"><span data-stu-id="627fb-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="627fb-132">Erstellen Sie eine Datei _namensAllowedLocations.jsim_ lokalen Arbeitsverzeichnis mit dem folgenden Inhalt.</span><span class="sxs-lookup"><span data-stu-id="627fb-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="627fb-133">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 ab, indem er das cmdlet Get-AzResourceGroup verwendet und in der $ResourceGroup speichert.</span><span class="sxs-lookup"><span data-stu-id="627fb-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="627fb-134">Der zweite Befehl ruft die integrierte Richtliniendefinition für zulässige Speicherorte ab, indem er das cmdlet Get-AzPolicyDefinition verwendet und in der $Policy speichert.</span><span class="sxs-lookup"><span data-stu-id="627fb-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="627fb-135">Der letzte Befehl weist die Richtlinie in $Policy der Ressourcengruppe zu, die durch die **ResourceId-Eigenschaft** von $ResourceGroup mit der Richtlinienparameterdatei AllowedLocations.jsaus dem lokalen Arbeitsverzeichnis identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="627fb-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="627fb-136">Beispiel 5: Richtlinienzuordnung mit verwalteter Identität</span><span class="sxs-lookup"><span data-stu-id="627fb-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="627fb-137">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 ab, indem er das cmdlet Get-AzResourceGroup verwendet und in der $ResourceGroup speichert.</span><span class="sxs-lookup"><span data-stu-id="627fb-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="627fb-138">Der zweite Befehl ruft die Richtliniendefinition virtualMachinePolicy ab, indem er das cmdlet Get-AzPolicyDefinition verwendet und in der $Policy speichert.</span><span class="sxs-lookup"><span data-stu-id="627fb-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="627fb-139">Der letzte Befehl weist die Richtlinie in $Policy der Ressourcengruppe zu.</span><span class="sxs-lookup"><span data-stu-id="627fb-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="627fb-140">Eine verwaltete Identität wird automatisch erstellt und der Richtlinienzuordnung zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="627fb-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="627fb-141">Beispiel 6: Richtlinienzuordnung mit einer Erzwingungsmoduseigenschaft</span><span class="sxs-lookup"><span data-stu-id="627fb-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="627fb-142">Der erste Befehl ruft ein Abonnement mit dem Namen Abonnement01 mithilfe des cmdlets Get-AzSubscription ab und speichert es in der $Subscription Variablen.</span><span class="sxs-lookup"><span data-stu-id="627fb-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="627fb-143">Der zweite Befehl ruft die Richtliniendefinition virtualMachinePolicy ab, indem er das cmdlet Get-AzPolicyDefinition verwendet und in der $Policy speichert.</span><span class="sxs-lookup"><span data-stu-id="627fb-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="627fb-144">Der letzte Befehl weist die Richtlinie $Policy auf der Ebene des Abonnements zu, das durch die Zeichenfolge des Abonnementbereichs identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="627fb-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="627fb-145">Die Zuordnung wird mit dem EnforcementMode-Wert von _DoNotEnforce_ festgelegt, d. h., der Richtlinieneffekt wird während der Ressourcenerstellung oder -aktualisierung nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="627fb-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="627fb-146">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="627fb-146">PARAMETERS</span></span>

### <span data-ttu-id="627fb-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="627fb-147">-ApiVersion</span></span>
<span data-ttu-id="627fb-148">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="627fb-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="627fb-149">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="627fb-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="627fb-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="627fb-150">-AssignIdentity</span></span>
<span data-ttu-id="627fb-151">Generieren und Zuweisen einer Azure Active Directory-Identität für diese Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="627fb-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="627fb-152">Die Identität wird beim Ausführen von Bereitstellungen für "deployIfNotExists"-Richtlinien verwendet.</span><span class="sxs-lookup"><span data-stu-id="627fb-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="627fb-153">Der Speicherort ist erforderlich, wenn Eine Identität zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="627fb-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="627fb-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="627fb-154">-DefaultProfile</span></span>
<span data-ttu-id="627fb-155">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="627fb-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="627fb-156">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="627fb-156">-Description</span></span>
<span data-ttu-id="627fb-157">Beschreibung der Richtlinienzuordnung</span><span class="sxs-lookup"><span data-stu-id="627fb-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="627fb-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="627fb-158">-DisplayName</span></span>
<span data-ttu-id="627fb-159">Gibt einen Anzeigenamen für die Richtlinienzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="627fb-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="627fb-160">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="627fb-160">-EnforcementMode</span></span>
<span data-ttu-id="627fb-161">Der Erzwingungsmodus für die Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="627fb-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="627fb-162">Aktuell sind gültige Werte Standard, DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="627fb-162">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="627fb-163">-Location</span><span class="sxs-lookup"><span data-stu-id="627fb-163">-Location</span></span>
<span data-ttu-id="627fb-164">Der Speicherort der Ressourcenidentität der Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="627fb-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="627fb-165">Dies ist erforderlich, wenn der Schalter "-AssignIdentity" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="627fb-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="627fb-166">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="627fb-166">-Metadata</span></span>
<span data-ttu-id="627fb-167">Die Metadaten für die neue Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="627fb-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="627fb-168">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="627fb-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="627fb-169">-Name</span><span class="sxs-lookup"><span data-stu-id="627fb-169">-Name</span></span>
<span data-ttu-id="627fb-170">Gibt einen Namen für die Richtlinienzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="627fb-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="627fb-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="627fb-171">-NotScope</span></span>
<span data-ttu-id="627fb-172">Die Nichtbereiche für die Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="627fb-172">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="627fb-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="627fb-173">-PolicyDefinition</span></span>
<span data-ttu-id="627fb-174">Gibt eine Richtlinie als **PsPolicyDefinition-Objekt** an, das die Richtlinienregel enthält.</span><span class="sxs-lookup"><span data-stu-id="627fb-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="627fb-175">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="627fb-175">-PolicyParameter</span></span>
<span data-ttu-id="627fb-176">Der Richtlinienparameterdateipfad oder die Richtlinienparameterzeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="627fb-176">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="627fb-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="627fb-177">-PolicyParameterObject</span></span>
<span data-ttu-id="627fb-178">Das Richtlinienparameterobjekt.</span><span class="sxs-lookup"><span data-stu-id="627fb-178">The policy parameter object.</span></span>

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

### <span data-ttu-id="627fb-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="627fb-179">-PolicySetDefinition</span></span>
<span data-ttu-id="627fb-180">Das Richtliniensatzdefinitionsobjekt.</span><span class="sxs-lookup"><span data-stu-id="627fb-180">The policy set definition object.</span></span>

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

### <span data-ttu-id="627fb-181">-Pre</span><span class="sxs-lookup"><span data-stu-id="627fb-181">-Pre</span></span>
<span data-ttu-id="627fb-182">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="627fb-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="627fb-183">-Scope</span><span class="sxs-lookup"><span data-stu-id="627fb-183">-Scope</span></span>
<span data-ttu-id="627fb-184">Gibt den Bereich an, in dem die Richtlinie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="627fb-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="627fb-185">Wenn Sie beispielsweise einer Ressourcengruppe eine Richtlinie zuweisen möchten, geben Sie Folgendes an: Name der `/subscriptions/` Ressourcengruppe "Abonnement-ID". `/resourcegroups/`</span><span class="sxs-lookup"><span data-stu-id="627fb-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="627fb-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="627fb-186">CommonParameters</span></span>
<span data-ttu-id="627fb-187">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="627fb-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="627fb-188">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="627fb-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="627fb-189">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="627fb-189">INPUTS</span></span>

### <span data-ttu-id="627fb-190">System.String</span><span class="sxs-lookup"><span data-stu-id="627fb-190">System.String</span></span>

### <span data-ttu-id="627fb-191">System.String[]</span><span class="sxs-lookup"><span data-stu-id="627fb-191">System.String[]</span></span>

### <span data-ttu-id="627fb-192">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="627fb-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="627fb-193">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="627fb-193">OUTPUTS</span></span>

### <span data-ttu-id="627fb-194">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="627fb-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="627fb-195">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="627fb-195">NOTES</span></span>

## <span data-ttu-id="627fb-196">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="627fb-196">RELATED LINKS</span></span>

[<span data-ttu-id="627fb-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="627fb-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="627fb-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="627fb-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="627fb-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="627fb-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="627fb-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="627fb-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


