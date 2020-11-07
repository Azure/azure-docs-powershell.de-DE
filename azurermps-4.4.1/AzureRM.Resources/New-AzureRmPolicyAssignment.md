---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: fa43b462cf06b9e2cd58df5d6796c098e942fafc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663837"
---
# <span data-ttu-id="4318b-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4318b-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="4318b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4318b-102">SYNOPSIS</span></span>
<span data-ttu-id="4318b-103">Erstellt eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="4318b-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4318b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4318b-104">SYNTAX</span></span>

### <span data-ttu-id="4318b-105">Richtlinienzuweisung ohne Parameter (Standard)</span><span class="sxs-lookup"><span data-stu-id="4318b-105">Policy assignment without parameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4318b-106">Richtlinienzuweisung mit Parametern über das Richtlinienparameter Objekt</span><span class="sxs-lookup"><span data-stu-id="4318b-106">Policy assignment with parameters via policy parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4318b-107">Richtlinienzuweisung mit Parametern über die Richtlinienparameter Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4318b-107">Policy assignment with parameters via policy parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4318b-108">Richtlinienzuweisung mit Parametern über Richtliniensatz-Parameter Objekt</span><span class="sxs-lookup"><span data-stu-id="4318b-108">Policy assignment with parameters via policy set parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="4318b-109">Richtlinienzuweisung mit Parametern über Richtliniensatz-Parameterzeichenfolge</span><span class="sxs-lookup"><span data-stu-id="4318b-109">Policy assignment with parameters via policy set parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="4318b-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4318b-110">DESCRIPTION</span></span>
<span data-ttu-id="4318b-111">Das Cmdlet **New-AzureRmPolicyAssignment** erstellt eine Richtlinienzuordnung.</span><span class="sxs-lookup"><span data-stu-id="4318b-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="4318b-112">Geben Sie eine Richtlinie und einen Bereich an.</span><span class="sxs-lookup"><span data-stu-id="4318b-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="4318b-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4318b-113">EXAMPLES</span></span>

### <span data-ttu-id="4318b-114">Beispiel 1: Richtlinienzuweisung auf Ressourcengruppen Ebene</span><span class="sxs-lookup"><span data-stu-id="4318b-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="4318b-115">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen ResourceGroup11 mithilfe des Get-AzureRMResourceGroup-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="4318b-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="4318b-116">Der Befehl speichert das Objekt in der $ResourceGroup Variablen.</span><span class="sxs-lookup"><span data-stu-id="4318b-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="4318b-117">Der zweite Befehl ruft die Richtliniendefinition mit dem Namen VirtualMachinePolicy mithilfe des Get-AzureRmPolicyDefinition-Cmdlets ab.</span><span class="sxs-lookup"><span data-stu-id="4318b-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="4318b-118">Der Befehl speichert das Objekt in der $Policy Variablen.</span><span class="sxs-lookup"><span data-stu-id="4318b-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="4318b-119">Der endgültige Befehl weist die Richtlinie in $Policy auf der Ebene einer Ressourcengruppe zu.</span><span class="sxs-lookup"><span data-stu-id="4318b-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="4318b-120">Die **Resourcen** -Eigenschaft von $ResourceGroup identifiziert die Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4318b-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

## <span data-ttu-id="4318b-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="4318b-121">PARAMETERS</span></span>

### <span data-ttu-id="4318b-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4318b-122">-ApiVersion</span></span>
<span data-ttu-id="4318b-123">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="4318b-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="4318b-124">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="4318b-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="4318b-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4318b-125">-DisplayName</span></span>
<span data-ttu-id="4318b-126">Gibt einen Anzeigenamen für die Richtlinienzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="4318b-126">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="4318b-127">-Information</span><span class="sxs-lookup"><span data-stu-id="4318b-127">-InformationAction</span></span>
<span data-ttu-id="4318b-128">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="4318b-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4318b-129">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4318b-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4318b-130">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="4318b-130">Continue</span></span>
- <span data-ttu-id="4318b-131">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="4318b-131">Ignore</span></span>
- <span data-ttu-id="4318b-132">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="4318b-132">Inquire</span></span>
- <span data-ttu-id="4318b-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4318b-133">SilentlyContinue</span></span>
- <span data-ttu-id="4318b-134">Beenden</span><span class="sxs-lookup"><span data-stu-id="4318b-134">Stop</span></span>
- <span data-ttu-id="4318b-135">Anhalten</span><span class="sxs-lookup"><span data-stu-id="4318b-135">Suspend</span></span>

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

### <span data-ttu-id="4318b-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4318b-136">-InformationVariable</span></span>
<span data-ttu-id="4318b-137">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="4318b-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="4318b-138">-Name</span><span class="sxs-lookup"><span data-stu-id="4318b-138">-Name</span></span>
<span data-ttu-id="4318b-139">Gibt einen Namen für die Richtlinienzuordnung an.</span><span class="sxs-lookup"><span data-stu-id="4318b-139">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="4318b-140">-NotScope</span><span class="sxs-lookup"><span data-stu-id="4318b-140">-NotScope</span></span>
<span data-ttu-id="4318b-141">Die nicht-Bereiche für die Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="4318b-141">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="4318b-142">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4318b-142">-PolicyDefinition</span></span>
<span data-ttu-id="4318b-143">Gibt eine Richtlinie als **PSObject** -Objekt an, das die Richtlinienregel enthält.</span><span class="sxs-lookup"><span data-stu-id="4318b-143">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4318b-144">-Policyparameter</span><span class="sxs-lookup"><span data-stu-id="4318b-144">-PolicyParameter</span></span>
<span data-ttu-id="4318b-145">Der Richtlinienparameter-Dateipfad oder die Richtlinienparameter-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="4318b-145">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: Policy assignment with parameters via policy parameter string, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4318b-146">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="4318b-146">-PolicyParameterObject</span></span>
<span data-ttu-id="4318b-147">Das Richtlinienparameter-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4318b-147">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy set parameter object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4318b-148">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="4318b-148">-PolicySetDefinition</span></span>
<span data-ttu-id="4318b-149">Das Richtliniensatz-Definitionsobjekt.</span><span class="sxs-lookup"><span data-stu-id="4318b-149">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4318b-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="4318b-150">-Pre</span></span>
<span data-ttu-id="4318b-151">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="4318b-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="4318b-152">-Scope</span><span class="sxs-lookup"><span data-stu-id="4318b-152">-Scope</span></span>
<span data-ttu-id="4318b-153">Gibt den Bereich an, für den die Richtlinie zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4318b-153">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="4318b-154">Wenn Sie beispielsweise einer Ressourcengruppe eine Richtlinie zuweisen möchten, geben Sie Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="4318b-154">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="4318b-155">`/subscriptions/`Name der Ressourcengruppe der Abonnement-ID `/resourcegroups/`</span><span class="sxs-lookup"><span data-stu-id="4318b-155">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="4318b-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4318b-156">-DefaultProfile</span></span>
<span data-ttu-id="4318b-157">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4318b-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4318b-158">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4318b-158">-Description</span></span>
<span data-ttu-id="4318b-159">Die Beschreibung für die Richtlinienzuweisung.</span><span class="sxs-lookup"><span data-stu-id="4318b-159">The description for policy assignment.</span></span>

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

### <span data-ttu-id="4318b-160">-SKU</span><span class="sxs-lookup"><span data-stu-id="4318b-160">-Sku</span></span>
<span data-ttu-id="4318b-161">Eine Hashtabelle, die SKU-Eigenschaften darstellt.</span><span class="sxs-lookup"><span data-stu-id="4318b-161">A hash table which represents sku properties.</span></span> <span data-ttu-id="4318b-162">Standardmäßig wird die SKU freigegeben: Name = a0, Tier = kostenlos</span><span class="sxs-lookup"><span data-stu-id="4318b-162">Defaults to Free Sku: Name = A0, Tier = Free</span></span>

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

### <span data-ttu-id="4318b-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4318b-163">CommonParameters</span></span>
<span data-ttu-id="4318b-164">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4318b-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4318b-165">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4318b-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4318b-166">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4318b-166">INPUTS</span></span>

## <span data-ttu-id="4318b-167">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4318b-167">OUTPUTS</span></span>

### <span data-ttu-id="4318b-168">System. Management. Automation. PSObject</span><span class="sxs-lookup"><span data-stu-id="4318b-168">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="4318b-169">Notizen</span><span class="sxs-lookup"><span data-stu-id="4318b-169">NOTES</span></span>

## <span data-ttu-id="4318b-170">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4318b-170">RELATED LINKS</span></span>

[<span data-ttu-id="4318b-171">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="4318b-171">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="4318b-172">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4318b-172">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="4318b-173">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4318b-173">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="4318b-174">Satz-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="4318b-174">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


