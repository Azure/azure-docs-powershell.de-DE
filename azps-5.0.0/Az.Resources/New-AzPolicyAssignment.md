---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 63efc580cf47274363f04750dc6a3f8da93b6665
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94300189"
---
# <span data-ttu-id="d11b9-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d11b9-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="d11b9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d11b9-102">SYNOPSIS</span></span>
<span data-ttu-id="d11b9-103">Erstellt eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="d11b9-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="d11b9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d11b9-104">SYNTAX</span></span>

### <span data-ttu-id="d11b9-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d11b9-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>]
 [-PolicySetDefinition <PsPolicySetDefinition>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d11b9-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d11b9-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d11b9-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d11b9-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d11b9-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="d11b9-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d11b9-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="d11b9-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d11b9-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d11b9-110">DESCRIPTION</span></span>
<span data-ttu-id="d11b9-111">Das Cmdlet **New-AzPolicyAssignment** erstellt eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="d11b9-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="d11b9-112">Geben Sie eine Richtlinie und einen Bereich an.</span><span class="sxs-lookup"><span data-stu-id="d11b9-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="d11b9-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d11b9-113">EXAMPLES</span></span>

### <span data-ttu-id="d11b9-114">Beispiel 1: Richtlinienzuweisung auf Abonnementebene</span><span class="sxs-lookup"><span data-stu-id="d11b9-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="d11b9-115">Der erste Befehl ruft mithilfe des Get-AzSubscription-Cmdlets ein Abonnement mit dem Namen Subscription01 ab und speichert es in der $Subscription-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d11b9-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="d11b9-116">Der zweite Befehl ruft die Richtliniendefinition mit dem Namen VirtualMachinePolicy mithilfe des Get-AzPolicyDefinition-Cmdlets ab und speichert Sie in der $Policy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d11b9-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="d11b9-117">Der endgültige Befehl weist die Richtlinie in $Policy auf der Ebene des Abonnements zu, das durch die Zeichenfolge des Abonnement Bereichs angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d11b9-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="d11b9-118">Beispiel 2: Richtlinienzuweisung auf Ressourcengruppen Ebene</span><span class="sxs-lookup"><span data-stu-id="d11b9-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="d11b9-119">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab und speichert Sie in der Variablen $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d11b9-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="d11b9-120">Der zweite Befehl ruft die Richtliniendefinition mit dem Namen VirtualMachinePolicy mithilfe des Get-AzPolicyDefinition-Cmdlets ab und speichert Sie in der $Policy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d11b9-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="d11b9-121">Der endgültige Befehl weist die Richtlinie in $Policy auf der Ebene der Ressourcengruppe zu, die von der Eigenschaft " **Resourcen** " von $ResourceGroup identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="d11b9-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="d11b9-122">Beispiel 3: Richtlinienzuweisung auf Ressourcengruppen Ebene mit Richtlinienparameter Objekt</span><span class="sxs-lookup"><span data-stu-id="d11b9-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="d11b9-123">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="d11b9-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="d11b9-124">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="d11b9-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="d11b9-125">Der zweite Befehl ruft die integrierte Richtliniendefinition für zulässige Speicherorte mithilfe des Get-AzPolicyDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="d11b9-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="d11b9-126">Der Befehl speichert das Objekt in der $Policy Variablen.</span><span class="sxs-lookup"><span data-stu-id="d11b9-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="d11b9-127">Der dritte und der vierte Befehl erstellen ein Objekt, das alle Azure-Bereiche mit "Ost" im Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="d11b9-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="d11b9-128">Die Befehle Speichern dieses Objekt in der $AllowedLocations Variablen.</span><span class="sxs-lookup"><span data-stu-id="d11b9-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="d11b9-129">Der endgültige Befehl weist die Richtlinie in $Policy auf der Ebene einer Ressourcengruppe mithilfe des Richtlinienparameter Objekts in $AllowedLocations zu.</span><span class="sxs-lookup"><span data-stu-id="d11b9-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="d11b9-130">Die **Resourcen** -Eigenschaft von $ResourceGroup identifiziert die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d11b9-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="d11b9-131">Beispiel 4: Richtlinienzuweisung auf Ressourcengruppen Ebene mit Richtlinienparameter Datei</span><span class="sxs-lookup"><span data-stu-id="d11b9-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="d11b9-132">Erstellen Sie eine Datei mit dem Namen _AllowedLocations.js_ im lokalen Arbeitsverzeichnis mit folgendem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="d11b9-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="d11b9-133">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab und speichert Sie in der Variablen $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d11b9-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="d11b9-134">Der zweite Befehl ruft die integrierte Richtliniendefinition für zulässige Speicherorte mithilfe des Get-AzPolicyDefinition-Cmdlets ab und speichert Sie in der $Policy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d11b9-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="d11b9-135">Der endgültige Befehl weist die Richtlinie in $Policy der Ressourcengruppe zu, die von der Eigenschaft " **Resourcen** " von $ResourceGroup mithilfe der Richtlinienparameter Datei AllowedLocations.jsauf aus dem lokalen Arbeitsverzeichnis festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="d11b9-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="d11b9-136">Beispiel 5: Richtlinienzuweisung mit einer verwalteten Identität</span><span class="sxs-lookup"><span data-stu-id="d11b9-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="d11b9-137">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab und speichert Sie in der Variablen $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d11b9-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="d11b9-138">Der zweite Befehl ruft die Richtliniendefinition mit dem Namen VirtualMachinePolicy mithilfe des Get-AzPolicyDefinition-Cmdlets ab und speichert Sie in der $Policy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d11b9-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="d11b9-139">Der endgültige Befehl weist die Richtlinie in $Policy der Ressourcengruppe zu.</span><span class="sxs-lookup"><span data-stu-id="d11b9-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="d11b9-140">Eine verwaltete Identität wird automatisch erstellt und der Richtlinien Aufgabe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="d11b9-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="d11b9-141">Beispiel 6: Richtlinienzuweisung mit einer Eigenschaft des Erzwingungsmodus</span><span class="sxs-lookup"><span data-stu-id="d11b9-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="d11b9-142">Der erste Befehl ruft mithilfe des Get-AzSubscription-Cmdlets ein Abonnement mit dem Namen Subscription01 ab und speichert es in der $Subscription-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d11b9-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="d11b9-143">Der zweite Befehl ruft die Richtliniendefinition mit dem Namen VirtualMachinePolicy mithilfe des Get-AzPolicyDefinition-Cmdlets ab und speichert Sie in der $Policy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="d11b9-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="d11b9-144">Der endgültige Befehl weist die Richtlinie in $Policy auf der Ebene des Abonnements zu, das durch die Zeichenfolge des Abonnement Bereichs angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d11b9-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="d11b9-145">Die Zuordnung wird mit einem EnforcementMode-Wert von _DoNotEnforce_ gesetzt, d. h., der Richtlinien Effekt wird während der Erstellung oder Aktualisierung der Ressource nicht erzwungen.</span><span class="sxs-lookup"><span data-stu-id="d11b9-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="d11b9-146">Parameter</span><span class="sxs-lookup"><span data-stu-id="d11b9-146">PARAMETERS</span></span>

### <span data-ttu-id="d11b9-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="d11b9-147">-ApiVersion</span></span>
<span data-ttu-id="d11b9-148">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="d11b9-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="d11b9-149">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="d11b9-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="d11b9-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="d11b9-150">-AssignIdentity</span></span>
<span data-ttu-id="d11b9-151">Generieren Sie eine Azure Active Directory-Identität für diese Richtlinienzuweisung, und weisen Sie diese zu.</span><span class="sxs-lookup"><span data-stu-id="d11b9-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="d11b9-152">Die Identität wird verwendet, wenn Bereitstellungen für "deployIfNotExists"-Richtlinien ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d11b9-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="d11b9-153">Beim Zuweisen einer Identität ist ein Speicherort erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d11b9-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="d11b9-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d11b9-154">-DefaultProfile</span></span>
<span data-ttu-id="d11b9-155">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d11b9-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d11b9-156">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d11b9-156">-Description</span></span>
<span data-ttu-id="d11b9-157">Die Beschreibung für die Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="d11b9-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="d11b9-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d11b9-158">-DisplayName</span></span>
<span data-ttu-id="d11b9-159">Gibt einen Anzeigenamen für die Richtlinienzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="d11b9-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="d11b9-160">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="d11b9-160">-EnforcementMode</span></span>
<span data-ttu-id="d11b9-161">Der Erzwingungsmodus für die Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="d11b9-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="d11b9-162">Gültige Werte sind derzeit Standard, DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="d11b9-162">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="d11b9-163">-Standort</span><span class="sxs-lookup"><span data-stu-id="d11b9-163">-Location</span></span>
<span data-ttu-id="d11b9-164">Der Speicherort der Ressourcen Identität der Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="d11b9-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="d11b9-165">Dies ist erforderlich, wenn der-AssignIdentity-Schalter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d11b9-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="d11b9-166">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="d11b9-166">-Metadata</span></span>
<span data-ttu-id="d11b9-167">Die Metadaten für die neue Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="d11b9-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="d11b9-168">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d11b9-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="d11b9-169">-Name</span><span class="sxs-lookup"><span data-stu-id="d11b9-169">-Name</span></span>
<span data-ttu-id="d11b9-170">Gibt einen Namen für die Richtlinienzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="d11b9-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="d11b9-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="d11b9-171">-NotScope</span></span>
<span data-ttu-id="d11b9-172">Die nicht-Bereiche für die Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="d11b9-172">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="d11b9-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d11b9-173">-PolicyDefinition</span></span>
<span data-ttu-id="d11b9-174">Gibt eine Richtlinie als **PsPolicyDefinition** -Objekt an, das die Richtlinienregel enthält.</span><span class="sxs-lookup"><span data-stu-id="d11b9-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="d11b9-175">-Policyparameter</span><span class="sxs-lookup"><span data-stu-id="d11b9-175">-PolicyParameter</span></span>
<span data-ttu-id="d11b9-176">Der Richtlinienparameter-Dateipfad oder die Richtlinienparameter-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="d11b9-176">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="d11b9-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="d11b9-177">-PolicyParameterObject</span></span>
<span data-ttu-id="d11b9-178">Das Richtlinienparameter-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d11b9-178">The policy parameter object.</span></span>

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

### <span data-ttu-id="d11b9-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="d11b9-179">-PolicySetDefinition</span></span>
<span data-ttu-id="d11b9-180">Das Richtliniensatz-Definitionsobjekt.</span><span class="sxs-lookup"><span data-stu-id="d11b9-180">The policy set definition object.</span></span>

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

### <span data-ttu-id="d11b9-181">-Pre</span><span class="sxs-lookup"><span data-stu-id="d11b9-181">-Pre</span></span>
<span data-ttu-id="d11b9-182">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="d11b9-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="d11b9-183">-Scope</span><span class="sxs-lookup"><span data-stu-id="d11b9-183">-Scope</span></span>
<span data-ttu-id="d11b9-184">Gibt den Bereich an, für den die Richtlinie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="d11b9-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="d11b9-185">Wenn Sie beispielsweise einer Ressourcengruppe eine Richtlinie zuweisen möchten, geben Sie Folgendes an: `/subscriptions/` Abonnement-ID- `/resourcegroups/` Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="d11b9-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="d11b9-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d11b9-186">CommonParameters</span></span>
<span data-ttu-id="d11b9-187">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d11b9-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d11b9-188">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d11b9-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d11b9-189">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d11b9-189">INPUTS</span></span>

### <span data-ttu-id="d11b9-190">System. String</span><span class="sxs-lookup"><span data-stu-id="d11b9-190">System.String</span></span>

### <span data-ttu-id="d11b9-191">System. String []</span><span class="sxs-lookup"><span data-stu-id="d11b9-191">System.String[]</span></span>

### <span data-ttu-id="d11b9-192">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d11b9-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d11b9-193">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d11b9-193">OUTPUTS</span></span>

### <span data-ttu-id="d11b9-194">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="d11b9-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="d11b9-195">Notizen</span><span class="sxs-lookup"><span data-stu-id="d11b9-195">NOTES</span></span>

## <span data-ttu-id="d11b9-196">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d11b9-196">RELATED LINKS</span></span>

[<span data-ttu-id="d11b9-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="d11b9-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="d11b9-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d11b9-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="d11b9-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d11b9-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="d11b9-200">Satz-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="d11b9-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


