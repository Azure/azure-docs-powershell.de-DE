---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: dcfc63c1dbf36cf7c592fe8fc7eb5afae09dc4e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101948499"
---
# <span data-ttu-id="0df18-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0df18-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="0df18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0df18-102">SYNOPSIS</span></span>
<span data-ttu-id="0df18-103">Ändert eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="0df18-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="0df18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="0df18-104">SYNTAX</span></span>

### <span data-ttu-id="0df18-105">NameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="0df18-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0df18-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0df18-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0df18-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0df18-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0df18-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0df18-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0df18-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0df18-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0df18-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="0df18-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0df18-111">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0df18-111">InputObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] -InputObject <PsPolicyAssignment> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0df18-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0df18-112">DESCRIPTION</span></span>
<span data-ttu-id="0df18-113">Das **Cmdlet Set-AzPolicyAssignment** ändert eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="0df18-113">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="0df18-114">Geben Sie eine Aufgabe nach ID oder nach Name und Bereich an.</span><span class="sxs-lookup"><span data-stu-id="0df18-114">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="0df18-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="0df18-115">EXAMPLES</span></span>

### <span data-ttu-id="0df18-116">Beispiel 1: Aktualisieren des Anzeigenamens</span><span class="sxs-lookup"><span data-stu-id="0df18-116">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="0df18-117">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 ab, indem er das cmdlet Get-AzResourceGroup verwendet.</span><span class="sxs-lookup"><span data-stu-id="0df18-117">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="0df18-118">Der Befehl speichert dieses Objekt in der $ResourceGroup-Variable.</span><span class="sxs-lookup"><span data-stu-id="0df18-118">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="0df18-119">Der zweite Befehl ruft die Richtlinienzuordnung mit dem Namen "PolicyAssignment" mithilfe des cmdlets Get-AzPolicyAssignment ab.</span><span class="sxs-lookup"><span data-stu-id="0df18-119">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="0df18-120">Der Befehl speichert dieses Objekt in der $PolicyAssignment-Variable.</span><span class="sxs-lookup"><span data-stu-id="0df18-120">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="0df18-121">Der letzte Befehl aktualisiert den Anzeigenamen für die Richtlinienzuordnung für die Ressourcengruppe, die durch die **ResourceId-Eigenschaft** des $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0df18-121">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="0df18-122">Beispiel 2: Hinzufügen einer verwalteten Identität zur Richtlinienzuordnung</span><span class="sxs-lookup"><span data-stu-id="0df18-122">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="0df18-123">Der erste Befehl ruft die Richtlinienzuordnung mit dem Namen "PolicyAssignment" aus dem aktuellen Abonnement ab, indem er das cmdlet Get-AzPolicyAssignment verwendet.</span><span class="sxs-lookup"><span data-stu-id="0df18-123">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="0df18-124">Der Befehl speichert dieses Objekt in der $PolicyAssignment-Variable.</span><span class="sxs-lookup"><span data-stu-id="0df18-124">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="0df18-125">Der letzte Befehl weist der Richtlinienzuordnung eine verwaltete Identität zu.</span><span class="sxs-lookup"><span data-stu-id="0df18-125">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="0df18-126">Beispiel 3: Aktualisieren von Richtlinienzuordnungsparametern mit neuem Richtlinienparameterobjekt</span><span class="sxs-lookup"><span data-stu-id="0df18-126">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="0df18-127">Mit dem ersten und zweiten Befehl wird ein -Objekt erstellt, das alle Azure-Regionen enthält, deren Namen mit "frankreich" oder "uk" beginnen.</span><span class="sxs-lookup"><span data-stu-id="0df18-127">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="0df18-128">Der zweite Befehl speichert dieses Objekt in der $AllowedLocations-Variable.</span><span class="sxs-lookup"><span data-stu-id="0df18-128">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="0df18-129">Der dritte Befehl ruft die Richtlinienzuordnung mit dem Namen "PolicyAssignment" ab Der Befehl speichert dieses Objekt in der $PolicyAssignment Variablen.</span><span class="sxs-lookup"><span data-stu-id="0df18-129">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="0df18-130">Der letzte Befehl aktualisiert die Parameterwerte für die Richtlinienzuordnung mit dem Namen "PolicyAssignment".</span><span class="sxs-lookup"><span data-stu-id="0df18-130">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="0df18-131">Beispiel 4: Aktualisieren von Richtlinienzuordnungsparametern mit richtlinienparameterdatei</span><span class="sxs-lookup"><span data-stu-id="0df18-131">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="0df18-132">Erstellen Sie eine Datei _namensAllowedLocations.jsim_ lokalen Arbeitsverzeichnis mit dem folgenden Inhalt.</span><span class="sxs-lookup"><span data-stu-id="0df18-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="0df18-133">Der Befehl aktualisiert die Richtlinienzuordnung mit dem Namen "PolicyAssignment" mithilfe der Richtlinienparameterdatei, AllowedLocations.jsaus dem lokalen Arbeitsverzeichnis aus.</span><span class="sxs-lookup"><span data-stu-id="0df18-133">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="0df18-134">Beispiel 5: Aktualisieren eines EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="0df18-134">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="0df18-135">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 ab, indem er das cmdlet Get-AzResourceGroup verwendet.</span><span class="sxs-lookup"><span data-stu-id="0df18-135">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="0df18-136">Der Befehl speichert dieses Objekt in der $ResourceGroup-Variable.</span><span class="sxs-lookup"><span data-stu-id="0df18-136">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="0df18-137">Der zweite Befehl ruft die Richtlinienzuordnung mit dem Namen "PolicyAssignment" mithilfe des cmdlets Get-AzPolicyAssignment ab.</span><span class="sxs-lookup"><span data-stu-id="0df18-137">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="0df18-138">Der Befehl speichert dieses Objekt in der $PolicyAssignment-Variable.</span><span class="sxs-lookup"><span data-stu-id="0df18-138">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="0df18-139">Der letzte Befehl aktualisiert die enforcementMode-Eigenschaft für die Richtlinienzuordnung für die Ressourcengruppe, die durch die **ResourceId-Eigenschaft** von $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="0df18-139">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="0df18-140">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="0df18-140">PARAMETERS</span></span>

### <span data-ttu-id="0df18-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="0df18-141">-ApiVersion</span></span>
<span data-ttu-id="0df18-142">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="0df18-142">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="0df18-143">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="0df18-143">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="0df18-144">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="0df18-144">-AssignIdentity</span></span>
<span data-ttu-id="0df18-145">Generieren und Zuweisen einer Azure Active Directory-Identität für diese Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="0df18-145">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="0df18-146">Die Identität wird beim Ausführen von Bereitstellungen für "deployIfNotExists"-Richtlinien verwendet.</span><span class="sxs-lookup"><span data-stu-id="0df18-146">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="0df18-147">Der Speicherort ist erforderlich, wenn Eine Identität zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0df18-147">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="0df18-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0df18-148">-DefaultProfile</span></span>
<span data-ttu-id="0df18-149">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="0df18-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0df18-150">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0df18-150">-Description</span></span>
<span data-ttu-id="0df18-151">Beschreibung der Richtlinienzuordnung</span><span class="sxs-lookup"><span data-stu-id="0df18-151">The description for policy assignment</span></span>

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

### <span data-ttu-id="0df18-152">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0df18-152">-DisplayName</span></span>
<span data-ttu-id="0df18-153">Gibt einen neuen Anzeigenamen für die Richtlinienzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="0df18-153">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="0df18-154">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="0df18-154">-EnforcementMode</span></span>
<span data-ttu-id="0df18-155">Der Erzwingungsmodus für die Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="0df18-155">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="0df18-156">Aktuell sind gültige Werte Standard, DoNotEnforce.</span><span class="sxs-lookup"><span data-stu-id="0df18-156">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="0df18-157">-ID</span><span class="sxs-lookup"><span data-stu-id="0df18-157">-Id</span></span>
<span data-ttu-id="0df18-158">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuordnung an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0df18-158">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0df18-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0df18-159">-InputObject</span></span>
<span data-ttu-id="0df18-160">Das zu aktualisierende Richtlinienzuordnungsobjekt, das von einem anderen Cmdlet ausgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="0df18-160">The policy assignment object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="0df18-161">-Location</span><span class="sxs-lookup"><span data-stu-id="0df18-161">-Location</span></span>
<span data-ttu-id="0df18-162">Der Speicherort der Ressourcenidentität der Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="0df18-162">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="0df18-163">Dies ist erforderlich, wenn der Schalter "-AssignIdentity" verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0df18-163">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="0df18-164">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="0df18-164">-Metadata</span></span>
<span data-ttu-id="0df18-165">Die aktualisierten Metadaten für die Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="0df18-165">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="0df18-166">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="0df18-166">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="0df18-167">-Name</span><span class="sxs-lookup"><span data-stu-id="0df18-167">-Name</span></span>
<span data-ttu-id="0df18-168">Gibt den Namen der Richtlinienzuordnung an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="0df18-168">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="0df18-169">-NotScope</span><span class="sxs-lookup"><span data-stu-id="0df18-169">-NotScope</span></span>
<span data-ttu-id="0df18-170">Die Richtlinienzuordnung keine Bereiche.</span><span class="sxs-lookup"><span data-stu-id="0df18-170">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="0df18-171">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="0df18-171">-PolicyParameter</span></span>
<span data-ttu-id="0df18-172">Der neue Dateipfad oder die neue Zeichenfolge für die Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="0df18-172">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="0df18-173">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="0df18-173">-PolicyParameterObject</span></span>
<span data-ttu-id="0df18-174">Das neue Richtlinienparameterobjekt für die Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="0df18-174">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="0df18-175">-Pre</span><span class="sxs-lookup"><span data-stu-id="0df18-175">-Pre</span></span>
<span data-ttu-id="0df18-176">Gibt an, dass dieses Cmdlet Vorabversions-API-Versionen berücksichtigt, wenn automatisch bestimmt wird, welche Version verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="0df18-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="0df18-177">-Scope</span><span class="sxs-lookup"><span data-stu-id="0df18-177">-Scope</span></span>
<span data-ttu-id="0df18-178">Gibt den Bereich an, in dem die Richtlinie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="0df18-178">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="0df18-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0df18-179">CommonParameters</span></span>
<span data-ttu-id="0df18-180">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0df18-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0df18-181">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0df18-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0df18-182">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="0df18-182">INPUTS</span></span>

### <span data-ttu-id="0df18-183">System.String</span><span class="sxs-lookup"><span data-stu-id="0df18-183">System.String</span></span>

### <span data-ttu-id="0df18-184">System.String[]</span><span class="sxs-lookup"><span data-stu-id="0df18-184">System.String[]</span></span>

## <span data-ttu-id="0df18-185">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="0df18-185">OUTPUTS</span></span>

### <span data-ttu-id="0df18-186">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="0df18-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="0df18-187">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="0df18-187">NOTES</span></span>

## <span data-ttu-id="0df18-188">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="0df18-188">RELATED LINKS</span></span>

[<span data-ttu-id="0df18-189">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0df18-189">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="0df18-190">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0df18-190">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="0df18-191">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="0df18-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


