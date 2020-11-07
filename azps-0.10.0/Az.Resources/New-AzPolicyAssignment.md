---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 1b8a7bd3d0c9f73b551cf6eefcb2564918fde1fa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843344"
---
# <span data-ttu-id="68db2-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="68db2-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="68db2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="68db2-102">SYNOPSIS</span></span>
<span data-ttu-id="68db2-103">Erstellt eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="68db2-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="68db2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="68db2-104">SYNTAX</span></span>

### <span data-ttu-id="68db2-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="68db2-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="68db2-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68db2-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="68db2-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="68db2-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="68db2-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="68db2-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="68db2-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="68db2-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="68db2-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68db2-110">DESCRIPTION</span></span>
<span data-ttu-id="68db2-111">Das Cmdlet **New-AzPolicyAssignment** erstellt eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="68db2-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="68db2-112">Geben Sie eine Richtlinie und einen Bereich an.</span><span class="sxs-lookup"><span data-stu-id="68db2-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="68db2-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="68db2-113">EXAMPLES</span></span>

### <span data-ttu-id="68db2-114">Beispiel 1: Richtlinienzuweisung auf Ressourcengruppen Ebene</span><span class="sxs-lookup"><span data-stu-id="68db2-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="68db2-115">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab und speichert Sie in der Variablen $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="68db2-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="68db2-116">Der zweite Befehl ruft die Richtliniendefinition mit dem Namen VirtualMachinePolicy mithilfe des Get-AzPolicyDefinition-Cmdlets ab und speichert Sie in der $Policy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="68db2-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="68db2-117">Der endgültige Befehl weist die Richtlinie in $Policy auf der Ebene der Ressourcengruppe zu, die von der Eigenschaft " **Resourcen** " von $ResourceGroup identifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="68db2-117">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="68db2-118">Beispiel 2: Richtlinienzuweisung auf Ressourcengruppen Ebene mit Richtlinienparameter Objekt</span><span class="sxs-lookup"><span data-stu-id="68db2-118">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="68db2-119">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="68db2-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="68db2-120">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="68db2-120">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="68db2-121">Der zweite Befehl ruft die integrierte Richtliniendefinition für zulässige Speicherorte mithilfe des Get-AzPolicyDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="68db2-121">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="68db2-122">Der Befehl speichert das Objekt in der $Policy Variablen.</span><span class="sxs-lookup"><span data-stu-id="68db2-122">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="68db2-123">Der dritte und der vierte Befehl erstellen ein Objekt, das alle Azure-Bereiche mit "Ost" im Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="68db2-123">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="68db2-124">Die Befehle Speichern dieses Objekt in der $AllowedLocations Variablen.</span><span class="sxs-lookup"><span data-stu-id="68db2-124">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="68db2-125">Der endgültige Befehl weist die Richtlinie in $Policy auf der Ebene einer Ressourcengruppe mithilfe des Richtlinienparameter Objekts in $AllowedLocations zu.</span><span class="sxs-lookup"><span data-stu-id="68db2-125">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="68db2-126">Die **Resourcen** -Eigenschaft von $ResourceGroup identifiziert die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="68db2-126">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="68db2-127">Beispiel 3: Richtlinienzuweisung auf Ressourcengruppen Ebene mit Richtlinienparameter Datei</span><span class="sxs-lookup"><span data-stu-id="68db2-127">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="68db2-128">Erstellen Sie eine Datei mit dem Namen _AllowedLocations.js_ im lokalen Arbeitsverzeichnis mit folgendem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="68db2-128">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="68db2-129">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab und speichert Sie in der Variablen $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="68db2-129">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="68db2-130">Der zweite Befehl ruft die integrierte Richtliniendefinition für zulässige Speicherorte mithilfe des Get-AzPolicyDefinition-Cmdlets ab und speichert Sie in der $Policy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="68db2-130">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="68db2-131">Der endgültige Befehl weist die Richtlinie in $Policy der Ressourcengruppe zu, die von der Eigenschaft " **Resourcen** " von $ResourceGroup mithilfe der Richtlinienparameter Datei AllowedLocations.jsauf aus dem lokalen Arbeitsverzeichnis festgelegt wurde.</span><span class="sxs-lookup"><span data-stu-id="68db2-131">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="68db2-132">Beispiel 4: Richtlinienzuweisung mit einer verwalteten Identität</span><span class="sxs-lookup"><span data-stu-id="68db2-132">Example 4: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity 
```

<span data-ttu-id="68db2-133">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzResourceGroup-Cmdlets ab und speichert Sie in der Variablen $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="68db2-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="68db2-134">Der zweite Befehl ruft die Richtliniendefinition mit dem Namen VirtualMachinePolicy mithilfe des Get-AzPolicyDefinition-Cmdlets ab und speichert Sie in der $Policy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="68db2-134">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="68db2-135">Der endgültige Befehl weist die Richtlinie in $Policy der Ressourcengruppe zu.</span><span class="sxs-lookup"><span data-stu-id="68db2-135">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="68db2-136">Eine verwaltete Identität wird automatisch erstellt und der Richtlinien Aufgabe zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="68db2-136">A managed identity is automatically created and assigned to the policy assignment.</span></span>

## <span data-ttu-id="68db2-137">Parameter</span><span class="sxs-lookup"><span data-stu-id="68db2-137">PARAMETERS</span></span>

### <span data-ttu-id="68db2-138">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="68db2-138">-ApiVersion</span></span>
<span data-ttu-id="68db2-139">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="68db2-139">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="68db2-140">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="68db2-140">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="68db2-141">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="68db2-141">-AssignIdentity</span></span>
<span data-ttu-id="68db2-142">Generieren Sie eine Azure Active Directory-Identität für diese Richtlinienzuweisung, und weisen Sie diese zu.</span><span class="sxs-lookup"><span data-stu-id="68db2-142">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="68db2-143">Die Identität wird verwendet, wenn Bereitstellungen für "deployIfNotExists"-Richtlinien ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="68db2-143">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="68db2-144">Beim Zuweisen einer Identität ist ein Speicherort erforderlich.</span><span class="sxs-lookup"><span data-stu-id="68db2-144">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="68db2-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="68db2-145">-DefaultProfile</span></span>
<span data-ttu-id="68db2-146">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="68db2-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="68db2-147">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="68db2-147">-Description</span></span>
<span data-ttu-id="68db2-148">Die Beschreibung für die Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="68db2-148">The description for policy assignment</span></span>

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

### <span data-ttu-id="68db2-149">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="68db2-149">-DisplayName</span></span>
<span data-ttu-id="68db2-150">Gibt einen Anzeigenamen für die Richtlinienzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="68db2-150">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="68db2-151">-Information</span><span class="sxs-lookup"><span data-stu-id="68db2-151">-InformationAction</span></span>
<span data-ttu-id="68db2-152">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="68db2-152">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="68db2-153">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="68db2-153">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="68db2-154">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="68db2-154">Continue</span></span>
- <span data-ttu-id="68db2-155">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="68db2-155">Ignore</span></span>
- <span data-ttu-id="68db2-156">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="68db2-156">Inquire</span></span>
- <span data-ttu-id="68db2-157">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="68db2-157">SilentlyContinue</span></span>
- <span data-ttu-id="68db2-158">Beenden</span><span class="sxs-lookup"><span data-stu-id="68db2-158">Stop</span></span>
- <span data-ttu-id="68db2-159">Anhalten</span><span class="sxs-lookup"><span data-stu-id="68db2-159">Suspend</span></span>

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

### <span data-ttu-id="68db2-160">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="68db2-160">-InformationVariable</span></span>
<span data-ttu-id="68db2-161">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="68db2-161">Specifies an information variable.</span></span>

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

### <span data-ttu-id="68db2-162">-Standort</span><span class="sxs-lookup"><span data-stu-id="68db2-162">-Location</span></span>
<span data-ttu-id="68db2-163">Der Speicherort der Ressourcen Identität der Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="68db2-163">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="68db2-164">Dies ist erforderlich, wenn der-AssignIdentity-Schalter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="68db2-164">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="68db2-165">-Metadaten</span><span class="sxs-lookup"><span data-stu-id="68db2-165">-Metadata</span></span>
<span data-ttu-id="68db2-166">Die Metadaten für die neue Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="68db2-166">The metadata for the new policy assignment.</span></span> <span data-ttu-id="68db2-167">Dies kann entweder ein Pfad zu einem Dateinamen sein, der die Metadaten enthält, oder die Metadaten als Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="68db2-167">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="68db2-168">-Name</span><span class="sxs-lookup"><span data-stu-id="68db2-168">-Name</span></span>
<span data-ttu-id="68db2-169">Gibt einen Namen für die Richtlinienzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="68db2-169">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="68db2-170">-NotScope</span><span class="sxs-lookup"><span data-stu-id="68db2-170">-NotScope</span></span>
<span data-ttu-id="68db2-171">Die nicht-Bereiche für die Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="68db2-171">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="68db2-172">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="68db2-172">-PolicyDefinition</span></span>
<span data-ttu-id="68db2-173">Gibt eine Richtlinie als **PsPolicyDefinition** -Objekt an, das die Richtlinienregel enthält.</span><span class="sxs-lookup"><span data-stu-id="68db2-173">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="68db2-174">-Policyparameter</span><span class="sxs-lookup"><span data-stu-id="68db2-174">-PolicyParameter</span></span>
<span data-ttu-id="68db2-175">Der Richtlinienparameter-Dateipfad oder die Richtlinienparameter-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="68db2-175">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="68db2-176">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="68db2-176">-PolicyParameterObject</span></span>
<span data-ttu-id="68db2-177">Das Richtlinienparameter-Objekt.</span><span class="sxs-lookup"><span data-stu-id="68db2-177">The policy parameter object.</span></span>

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

### <span data-ttu-id="68db2-178">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="68db2-178">-PolicySetDefinition</span></span>
<span data-ttu-id="68db2-179">Das Richtliniensatz-Definitionsobjekt.</span><span class="sxs-lookup"><span data-stu-id="68db2-179">The policy set definition object.</span></span>

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

### <span data-ttu-id="68db2-180">-Pre</span><span class="sxs-lookup"><span data-stu-id="68db2-180">-Pre</span></span>
<span data-ttu-id="68db2-181">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="68db2-181">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="68db2-182">-Scope</span><span class="sxs-lookup"><span data-stu-id="68db2-182">-Scope</span></span>
<span data-ttu-id="68db2-183">Gibt den Bereich an, für den die Richtlinie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="68db2-183">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="68db2-184">Wenn Sie beispielsweise einer Ressourcengruppe eine Richtlinie zuweisen möchten, geben Sie Folgendes an: `/subscriptions/` Abonnement-ID- `/resourcegroups/` Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="68db2-184">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="68db2-185">-SKU</span><span class="sxs-lookup"><span data-stu-id="68db2-185">-Sku</span></span>
<span data-ttu-id="68db2-186">Eine Hashtabelle, die SKU-Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="68db2-186">A hash table which represents SKU properties.</span></span> <span data-ttu-id="68db2-187">Standardmäßig ist die ﻿kostenlose SKU mit den Werten: `@{Name = 'A0'; Tier = 'Free'}` .</span><span class="sxs-lookup"><span data-stu-id="68db2-187">Defaults to the Free SKU with the values: `@{Name = 'A0'; Tier = 'Free'}`.</span></span> <span data-ttu-id="68db2-188">Verwenden Sie die Werte:, um die Standard-SKU zu verwenden `@{Name = 'A1'; Tier = 'Standard'}` .</span><span class="sxs-lookup"><span data-stu-id="68db2-188">To use the Standard SKU, use the values: `@{Name = 'A1'; Tier = 'Standard'}`.</span></span>

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

### <span data-ttu-id="68db2-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68db2-189">CommonParameters</span></span>
<span data-ttu-id="68db2-190">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="68db2-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68db2-191">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68db2-191">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68db2-192">Eingaben</span><span class="sxs-lookup"><span data-stu-id="68db2-192">INPUTS</span></span>

## <span data-ttu-id="68db2-193">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="68db2-193">OUTPUTS</span></span>

## <span data-ttu-id="68db2-194">Notizen</span><span class="sxs-lookup"><span data-stu-id="68db2-194">NOTES</span></span>

## <span data-ttu-id="68db2-195">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="68db2-195">RELATED LINKS</span></span>

[<span data-ttu-id="68db2-196">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="68db2-196">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="68db2-197">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="68db2-197">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="68db2-198">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="68db2-198">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="68db2-199">Satz-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="68db2-199">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


