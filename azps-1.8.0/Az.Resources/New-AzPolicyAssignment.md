---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 1b88fa6ea7a44d17843b72da162eec374e2c861f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93659595"
---
# <span data-ttu-id="1b0c3-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1b0c3-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="1b0c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1b0c3-102">SYNOPSIS</span></span>
<span data-ttu-id="1b0c3-103">Erstellt eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="1b0c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b0c3-104">SYNTAX</span></span>

### <span data-ttu-id="1b0c3-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="1b0c3-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b0c3-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b0c3-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b0c3-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b0c3-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b0c3-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b0c3-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b0c3-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="1b0c3-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b0c3-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b0c3-110">DESCRIPTION</span></span>
<span data-ttu-id="1b0c3-111">Das Cmdlet **New-AzPolicyAssignment** erstellt eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="1b0c3-112">Geben Sie eine Richtlinie und einen Bereich an.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="1b0c3-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1b0c3-113">EXAMPLES</span></span>

### <span data-ttu-id="1b0c3-114">Beispiel 1: Richtlinienzuweisung auf Ressourcengruppen Ebene</span><span class="sxs-lookup"><span data-stu-id="1b0c3-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="1b0c3-115">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab und speichert Sie in der Variablen $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1b0c3-116">Der zweite Befehl ruft die Richtliniendefinition mit dem Namen VirtualMachinePolicy mithilfe des Get-AzPolicyDefinition-Cmdlets ab und speichert Sie in der $Policy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="1b0c3-117">Der endgültige Befehl weist die Richtlinie in $Policy auf der Ebene der Ressourcengruppe zu, die von der Eigenschaft " **Resourcen** " von $ResourceGroup identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-117">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="1b0c3-118">Beispiel 2: Richtlinienzuweisung auf Ressourcengruppen Ebene mit Richtlinienparameter Objekt</span><span class="sxs-lookup"><span data-stu-id="1b0c3-118">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="1b0c3-119">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="1b0c3-120">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-120">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1b0c3-121">Der zweite Befehl ruft die integrierte Richtliniendefinition für zulässige Speicherorte mithilfe des Get-AzPolicyDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-121">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="1b0c3-122">Der Befehl speichert das Objekt in der $Policy Variablen.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-122">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="1b0c3-123">Der dritte und der vierte Befehl erstellen ein Objekt, das alle Azure-Bereiche mit "Ost" im Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-123">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="1b0c3-124">Die Befehle Speichern dieses Objekt in der $AllowedLocations Variablen.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-124">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="1b0c3-125">Der endgültige Befehl weist die Richtlinie in $Policy auf der Ebene einer Ressourcengruppe mithilfe des Richtlinienparameter Objekts in $AllowedLocations zu.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-125">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="1b0c3-126">Die **Resourcen** -Eigenschaft von $ResourceGroup identifiziert die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-126">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="1b0c3-127">Beispiel 3: Richtlinienzuweisung auf Ressourcengruppen Ebene mit Richtlinienparameter Datei</span><span class="sxs-lookup"><span data-stu-id="1b0c3-127">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="1b0c3-128">Erstellen Sie eine Datei mit dem Namen _AllowedLocations.js_ im lokalen Arbeitsverzeichnis mit folgendem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-128">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="1b0c3-129">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab und speichert Sie in der Variablen $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-129">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1b0c3-130">Der zweite Befehl ruft die integrierte Richtliniendefinition für zulässige Speicherorte mithilfe des Get-AzPolicyDefinition-Cmdlets ab und speichert Sie in der $Policy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-130">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="1b0c3-131">Der endgültige Befehl weist die Richtlinie in $Policy der Ressourcengruppe zu, die von der Eigenschaft " **Resourcen** " von $ResourceGroup mithilfe der Richtlinienparameter Datei AllowedLocations.jsauf aus dem lokalen Arbeitsverzeichnis festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-131">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="1b0c3-132">Beispiel 4: Richtlinienzuweisung mit einer verwalteten Identität</span><span class="sxs-lookup"><span data-stu-id="1b0c3-132">Example 4: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="1b0c3-133">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab und speichert Sie in der Variablen $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="1b0c3-134">Der zweite Befehl ruft die Richtliniendefinition mit dem Namen VirtualMachinePolicy mithilfe des Get-AzPolicyDefinition-Cmdlets ab und speichert Sie in der $Policy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-134">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="1b0c3-135">Der endgültige Befehl weist die Richtlinie in $Policy der Ressourcengruppe zu.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-135">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="1b0c3-136">Eine verwaltete Identität wird automatisch erstellt und der Richtlinien Aufgabe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-136">A managed identity is automatically created and assigned to the policy assignment.</span></span>

## <span data-ttu-id="1b0c3-137">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b0c3-137">PARAMETERS</span></span>

### <span data-ttu-id="1b0c3-138">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="1b0c3-138">-ApiVersion</span></span>
<span data-ttu-id="1b0c3-139">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-139">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="1b0c3-140">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-140">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="1b0c3-141">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="1b0c3-141">-AssignIdentity</span></span>
<span data-ttu-id="1b0c3-142">Generieren Sie eine Azure Active Directory-Identität für diese Richtlinienzuweisung, und weisen Sie diese zu.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-142">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="1b0c3-143">Die Identität wird verwendet, wenn Bereitstellungen für "deployIfNotExists"-Richtlinien ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-143">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="1b0c3-144">Beim Zuweisen einer Identität ist ein Speicherort erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-144">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="1b0c3-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b0c3-145">-DefaultProfile</span></span>
<span data-ttu-id="1b0c3-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1b0c3-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1b0c3-147">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1b0c3-147">-Description</span></span>
<span data-ttu-id="1b0c3-148">Die Beschreibung für die Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="1b0c3-148">The description for policy assignment</span></span>

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

### <span data-ttu-id="1b0c3-149">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="1b0c3-149">-DisplayName</span></span>
<span data-ttu-id="1b0c3-150">Gibt einen Anzeigenamen für die Richtlinienzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-150">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="1b0c3-151">-Standort</span><span class="sxs-lookup"><span data-stu-id="1b0c3-151">-Location</span></span>
<span data-ttu-id="1b0c3-152">Der Speicherort der Ressourcen Identität der Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-152">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="1b0c3-153">Dies ist erforderlich, wenn der-AssignIdentity-Schalter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-153">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="1b0c3-154">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="1b0c3-154">-Metadata</span></span>
<span data-ttu-id="1b0c3-155">Die Metadaten für die neue Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-155">The metadata for the new policy assignment.</span></span> <span data-ttu-id="1b0c3-156">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-156">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="1b0c3-157">-Name</span><span class="sxs-lookup"><span data-stu-id="1b0c3-157">-Name</span></span>
<span data-ttu-id="1b0c3-158">Gibt einen Namen für die Richtlinienzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-158">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="1b0c3-159">-NotScope</span><span class="sxs-lookup"><span data-stu-id="1b0c3-159">-NotScope</span></span>
<span data-ttu-id="1b0c3-160">Die nicht-Bereiche für die Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-160">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="1b0c3-161">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1b0c3-161">-PolicyDefinition</span></span>
<span data-ttu-id="1b0c3-162">Gibt eine Richtlinie als **PsPolicyDefinition** -Objekt an, das die Richtlinienregel enthält.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-162">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="1b0c3-163">-Policyparameter</span><span class="sxs-lookup"><span data-stu-id="1b0c3-163">-PolicyParameter</span></span>
<span data-ttu-id="1b0c3-164">Der Richtlinienparameter-Dateipfad oder die Richtlinienparameter-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-164">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="1b0c3-165">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="1b0c3-165">-PolicyParameterObject</span></span>
<span data-ttu-id="1b0c3-166">Das Richtlinienparameter-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-166">The policy parameter object.</span></span>

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

### <span data-ttu-id="1b0c3-167">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="1b0c3-167">-PolicySetDefinition</span></span>
<span data-ttu-id="1b0c3-168">Das Richtliniensatz-Definitionsobjekt.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-168">The policy set definition object.</span></span>

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

### <span data-ttu-id="1b0c3-169">-Pre</span><span class="sxs-lookup"><span data-stu-id="1b0c3-169">-Pre</span></span>
<span data-ttu-id="1b0c3-170">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-170">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="1b0c3-171">-Scope</span><span class="sxs-lookup"><span data-stu-id="1b0c3-171">-Scope</span></span>
<span data-ttu-id="1b0c3-172">Gibt den Bereich an, für den die Richtlinie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-172">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="1b0c3-173">Wenn Sie beispielsweise einer Ressourcengruppe eine Richtlinie zuweisen möchten, geben Sie Folgendes an: `/subscriptions/` Abonnement-ID- `/resourcegroups/` Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="1b0c3-173">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="1b0c3-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b0c3-174">CommonParameters</span></span>
<span data-ttu-id="1b0c3-175">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b0c3-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b0c3-176">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b0c3-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b0c3-177">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1b0c3-177">INPUTS</span></span>

### <span data-ttu-id="1b0c3-178">System. String</span><span class="sxs-lookup"><span data-stu-id="1b0c3-178">System.String</span></span>

### <span data-ttu-id="1b0c3-179">System. String []</span><span class="sxs-lookup"><span data-stu-id="1b0c3-179">System.String[]</span></span>

### <span data-ttu-id="1b0c3-180">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1b0c3-180">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1b0c3-181">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1b0c3-181">OUTPUTS</span></span>

### <span data-ttu-id="1b0c3-182">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="1b0c3-182">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="1b0c3-183">Notizen</span><span class="sxs-lookup"><span data-stu-id="1b0c3-183">NOTES</span></span>

## <span data-ttu-id="1b0c3-184">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1b0c3-184">RELATED LINKS</span></span>

[<span data-ttu-id="1b0c3-185">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="1b0c3-185">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="1b0c3-186">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1b0c3-186">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="1b0c3-187">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1b0c3-187">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="1b0c3-188">Satz-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="1b0c3-188">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


