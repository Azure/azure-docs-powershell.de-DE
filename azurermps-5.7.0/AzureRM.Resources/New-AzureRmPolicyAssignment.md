---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: 364411d6b69c04d8b29c1c32e2809ec3c4789b09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500413"
---
# <span data-ttu-id="3e03a-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3e03a-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="3e03a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3e03a-102">SYNOPSIS</span></span>
<span data-ttu-id="3e03a-103">Erstellt eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="3e03a-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3e03a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3e03a-104">SYNTAX</span></span>

### <span data-ttu-id="3e03a-105">CreateWithoutParameters (Standard)</span><span class="sxs-lookup"><span data-stu-id="3e03a-105">CreateWithoutParameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3e03a-106">CreateWithPolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="3e03a-106">CreateWithPolicyParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3e03a-107">CreateWithPolicyParameterString</span><span class="sxs-lookup"><span data-stu-id="3e03a-107">CreateWithPolicyParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3e03a-108">CreateWithPolicySetParameterObject</span><span class="sxs-lookup"><span data-stu-id="3e03a-108">CreateWithPolicySetParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="3e03a-109">CreateWithPolicySetParameterString</span><span class="sxs-lookup"><span data-stu-id="3e03a-109">CreateWithPolicySetParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="3e03a-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e03a-110">DESCRIPTION</span></span>
<span data-ttu-id="3e03a-111">Das Cmdlet **New-AzureRmPolicyAssignment** erstellt eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="3e03a-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="3e03a-112">Geben Sie eine Richtlinie und einen Bereich an.</span><span class="sxs-lookup"><span data-stu-id="3e03a-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="3e03a-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3e03a-113">EXAMPLES</span></span>

### <span data-ttu-id="3e03a-114">Beispiel 1: Richtlinienzuweisung auf Ressourcengruppen Ebene</span><span class="sxs-lookup"><span data-stu-id="3e03a-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="3e03a-115">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzureRMResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="3e03a-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="3e03a-116">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="3e03a-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="3e03a-117">Der zweite Befehl ruft die Richtliniendefinition mit dem Namen VirtualMachinePolicy mithilfe des Get-AzureRmPolicyDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="3e03a-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="3e03a-118">Der Befehl speichert das Objekt in der $Policy Variablen.</span><span class="sxs-lookup"><span data-stu-id="3e03a-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="3e03a-119">Der endgültige Befehl weist die Richtlinie in $Policy auf der Ebene einer Ressourcengruppe zu.</span><span class="sxs-lookup"><span data-stu-id="3e03a-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="3e03a-120">Die **Resourcen** -Eigenschaft von $ResourceGroup identifiziert die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3e03a-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="3e03a-121">Beispiel 2: Richtlinienzuweisung auf Ressourcengruppen Ebene mit Richtlinienparameter Objekt</span><span class="sxs-lookup"><span data-stu-id="3e03a-121">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> $Locations = Get-AzureRmLocation | where displayname -like "*east*"
PS C:\> $AllowedLocations = @{"listOfAllowedLocations"=($Locations.location)}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="3e03a-122">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzureRMResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="3e03a-122">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="3e03a-123">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="3e03a-123">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="3e03a-124">Der zweite Befehl ruft die integrierte Richtliniendefinition für zulässige Speicherorte mithilfe des Get-AzureRmPolicyDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="3e03a-124">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="3e03a-125">Der Befehl speichert das Objekt in der $Policy Variablen.</span><span class="sxs-lookup"><span data-stu-id="3e03a-125">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="3e03a-126">Der dritte und der vierte Befehl erstellen ein Objekt, das alle Azure-Bereiche mit "Ost" im Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="3e03a-126">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="3e03a-127">Die Befehle Speichern dieses Objekt in der $AllowedLocations Variablen.</span><span class="sxs-lookup"><span data-stu-id="3e03a-127">The commands store that object in the $AllowedLocations variable.</span></span>

<span data-ttu-id="3e03a-128">Der endgültige Befehl weist die Richtlinie in $Policy auf der Ebene einer Ressourcengruppe mithilfe des Richtlinienparameter Objekts in $AllowedLocations zu.</span><span class="sxs-lookup"><span data-stu-id="3e03a-128">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="3e03a-129">Die **Resourcen** -Eigenschaft von $ResourceGroup identifiziert die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3e03a-129">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="3e03a-130">Beispiel 3: Richtlinienzuweisung auf Ressourcengruppen Ebene mit Richtlinienparameter Datei</span><span class="sxs-lookup"><span data-stu-id="3e03a-130">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="3e03a-131">Erstellen Sie eine Datei mit dem Namen _AllowedLocations.js_ im lokalen Arbeitsverzeichnis mit folgendem Inhalt.</span><span class="sxs-lookup"><span data-stu-id="3e03a-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>
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
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="3e03a-132">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzureRMResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="3e03a-132">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="3e03a-133">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="3e03a-133">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="3e03a-134">Der zweite Befehl ruft die integrierte Richtliniendefinition für zulässige Speicherorte mithilfe des Get-AzureRmPolicyDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="3e03a-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="3e03a-135">Der Befehl speichert das Objekt in der $Policy Variablen.</span><span class="sxs-lookup"><span data-stu-id="3e03a-135">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="3e03a-136">Der endgültige Befehl weist die Richtlinie in $Policy auf der Ebene einer Ressourcengruppe mithilfe der Richtlinienparameter Datei AllowedLocations.jsauf aus dem lokalen Arbeitsverzeichnis zu.</span><span class="sxs-lookup"><span data-stu-id="3e03a-136">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter file AllowedLocations.json from the local working directory.</span></span>
<span data-ttu-id="3e03a-137">Die **Resourcen** -Eigenschaft von $ResourceGroup identifiziert die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3e03a-137">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>


## <span data-ttu-id="3e03a-138">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e03a-138">PARAMETERS</span></span>

### <span data-ttu-id="3e03a-139">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3e03a-139">-ApiVersion</span></span>
<span data-ttu-id="3e03a-140">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="3e03a-140">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3e03a-141">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="3e03a-141">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e03a-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e03a-142">-DefaultProfile</span></span>
<span data-ttu-id="3e03a-143">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3e03a-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e03a-144">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e03a-144">-Description</span></span>
<span data-ttu-id="3e03a-145">Die Beschreibung für die Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="3e03a-145">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e03a-146">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3e03a-146">-DisplayName</span></span>
<span data-ttu-id="3e03a-147">Gibt einen Anzeigenamen für die Richtlinienzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="3e03a-147">Specifies a display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e03a-148">-Information</span><span class="sxs-lookup"><span data-stu-id="3e03a-148">-InformationAction</span></span>
<span data-ttu-id="3e03a-149">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="3e03a-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3e03a-150">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3e03a-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3e03a-151">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="3e03a-151">Continue</span></span>
- <span data-ttu-id="3e03a-152">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="3e03a-152">Ignore</span></span>
- <span data-ttu-id="3e03a-153">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="3e03a-153">Inquire</span></span>
- <span data-ttu-id="3e03a-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3e03a-154">SilentlyContinue</span></span>
- <span data-ttu-id="3e03a-155">Beenden</span><span class="sxs-lookup"><span data-stu-id="3e03a-155">Stop</span></span>
- <span data-ttu-id="3e03a-156">Anhalten</span><span class="sxs-lookup"><span data-stu-id="3e03a-156">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e03a-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3e03a-157">-InformationVariable</span></span>
<span data-ttu-id="3e03a-158">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="3e03a-158">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e03a-159">-Name</span><span class="sxs-lookup"><span data-stu-id="3e03a-159">-Name</span></span>
<span data-ttu-id="3e03a-160">Gibt einen Namen für die Richtlinienzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="3e03a-160">Specifies a name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e03a-161">-NotScope</span><span class="sxs-lookup"><span data-stu-id="3e03a-161">-NotScope</span></span>
<span data-ttu-id="3e03a-162">Die nicht-Bereiche für die Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="3e03a-162">The not scopes for policy assignment.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e03a-163">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3e03a-163">-PolicyDefinition</span></span>
<span data-ttu-id="3e03a-164">Gibt eine Richtlinie als **PSObject** -Objekt an, das die Richtlinienregel enthält.</span><span class="sxs-lookup"><span data-stu-id="3e03a-164">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e03a-165">-Policyparameter</span><span class="sxs-lookup"><span data-stu-id="3e03a-165">-PolicyParameter</span></span>
<span data-ttu-id="3e03a-166">Der Richtlinienparameter-Dateipfad oder die Richtlinienparameter-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3e03a-166">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithPolicyParameterString, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e03a-167">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="3e03a-167">-PolicyParameterObject</span></span>
<span data-ttu-id="3e03a-168">Das Richtlinienparameter-Objekt.</span><span class="sxs-lookup"><span data-stu-id="3e03a-168">The policy parameter object.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicySetParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e03a-169">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="3e03a-169">-PolicySetDefinition</span></span>
<span data-ttu-id="3e03a-170">Das Richtliniensatz-Definitionsobjekt.</span><span class="sxs-lookup"><span data-stu-id="3e03a-170">The policy set definition object.</span></span>

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e03a-171">-Pre</span><span class="sxs-lookup"><span data-stu-id="3e03a-171">-Pre</span></span>
<span data-ttu-id="3e03a-172">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="3e03a-172">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3e03a-173">-Scope</span><span class="sxs-lookup"><span data-stu-id="3e03a-173">-Scope</span></span>
<span data-ttu-id="3e03a-174">Gibt den Bereich an, für den die Richtlinie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e03a-174">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="3e03a-175">Wenn Sie beispielsweise einer Ressourcengruppe eine Richtlinie zuweisen möchten, geben Sie Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="3e03a-175">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="3e03a-176">`/subscriptions/`Name der Ressourcengruppe der Abonnement-ID `/resourcegroups/`</span><span class="sxs-lookup"><span data-stu-id="3e03a-176">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e03a-177">-SKU</span><span class="sxs-lookup"><span data-stu-id="3e03a-177">-Sku</span></span>
<span data-ttu-id="3e03a-178">Eine Hashtabelle, die SKU-Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="3e03a-178">A hash table which represents sku properties.</span></span> <span data-ttu-id="3e03a-179">Standardmäßig wird die SKU freigegeben: Name = a0, Tier = Fre</span><span class="sxs-lookup"><span data-stu-id="3e03a-179">Defaults to Free Sku: Name = A0, Tier = Fre</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3e03a-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e03a-180">CommonParameters</span></span>
<span data-ttu-id="3e03a-181">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e03a-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e03a-182">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3e03a-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e03a-183">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3e03a-183">INPUTS</span></span>

### <span data-ttu-id="3e03a-184">Keine</span><span class="sxs-lookup"><span data-stu-id="3e03a-184">None</span></span>
<span data-ttu-id="3e03a-185">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="3e03a-185">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3e03a-186">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3e03a-186">OUTPUTS</span></span>

### <span data-ttu-id="3e03a-187">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="3e03a-187">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3e03a-188">Notizen</span><span class="sxs-lookup"><span data-stu-id="3e03a-188">NOTES</span></span>

## <span data-ttu-id="3e03a-189">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3e03a-189">RELATED LINKS</span></span>

[<span data-ttu-id="3e03a-190">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="3e03a-190">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="3e03a-191">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3e03a-191">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="3e03a-192">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3e03a-192">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="3e03a-193">Satz-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3e03a-193">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


