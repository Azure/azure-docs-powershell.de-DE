---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: cabd2c86ed687b90b45e60b8078d89ad0a413c87
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849523"
---
# <span data-ttu-id="09bd5-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="09bd5-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="09bd5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09bd5-102">SYNOPSIS</span></span>
<span data-ttu-id="09bd5-103">Ruft Richtlinienzuweisungen ab.</span><span class="sxs-lookup"><span data-stu-id="09bd5-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09bd5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09bd5-104">SYNTAX</span></span>

### <span data-ttu-id="09bd5-105">DefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="09bd5-105">DefaultParameterSet (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="09bd5-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09bd5-106">NameParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="09bd5-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="09bd5-107">IncludeDescendentParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="09bd5-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09bd5-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="09bd5-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09bd5-109">DESCRIPTION</span></span>
<span data-ttu-id="09bd5-110">Das Cmdlet " **Get-AzureRmPolicyAssignment** " ruft alle Richtlinienzuweisungen oder bestimmte Aufgaben ab.</span><span class="sxs-lookup"><span data-stu-id="09bd5-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="09bd5-111">Identifizieren Sie eine Richtlinien Aufgabe, die nach Name und Bereich oder nach ID abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="09bd5-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="09bd5-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09bd5-112">EXAMPLES</span></span>

### <span data-ttu-id="09bd5-113">Beispiel 1: Abrufen aller Richtlinienzuweisungen</span><span class="sxs-lookup"><span data-stu-id="09bd5-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzureRmPolicyAssignment
```

<span data-ttu-id="09bd5-114">Mit diesem Befehl werden alle Richtlinienzuweisungen abgerufen.</span><span class="sxs-lookup"><span data-stu-id="09bd5-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="09bd5-115">Beispiel 2: Abrufen einer bestimmten Richtlinienzuweisung</span><span class="sxs-lookup"><span data-stu-id="09bd5-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="09bd5-116">Der erste Befehl ruft eine Ressourcengruppe mit dem Namen "ResourceGroup11" ab, indem der Get-AzureRMResourceGroup cmdletand in der $ResourceGroup-Variablen speichert.</span><span class="sxs-lookup"><span data-stu-id="09bd5-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdletand stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="09bd5-117">Der zweite Befehl ruft die Richtlinienzuweisung mit dem Namen "PolicyAssignment07" für den Bereich ab **, den die Eigenschaft "** Eigenschaften" von $ResourceGroup identifiziert.</span><span class="sxs-lookup"><span data-stu-id="09bd5-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="09bd5-118">Beispiel 3: Abrufen aller einer Verwaltungsgruppe zugewiesenen Richtlinienzuweisungen</span><span class="sxs-lookup"><span data-stu-id="09bd5-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzureRmPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="09bd5-119">Der erste Befehl gibt die ID der zu abfragenden Verwaltungsgruppe an.</span><span class="sxs-lookup"><span data-stu-id="09bd5-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="09bd5-120">Der zweite Befehl ruft alle Richtlinienzuweisungen ab, die der Verwaltungsgruppe mit der ID "mymanagegroup" zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="09bd5-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="09bd5-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="09bd5-121">PARAMETERS</span></span>

### <span data-ttu-id="09bd5-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="09bd5-122">-ApiVersion</span></span>
<span data-ttu-id="09bd5-123">Gibt die Version der zu verwendenden Ressourcenanbieter-API an.</span><span class="sxs-lookup"><span data-stu-id="09bd5-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="09bd5-124">Wenn Sie keine Version angeben, verwendet dieses Cmdlet die neueste verfügbare Version.</span><span class="sxs-lookup"><span data-stu-id="09bd5-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="09bd5-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09bd5-125">-DefaultProfile</span></span>
<span data-ttu-id="09bd5-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="09bd5-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="09bd5-127">-ID</span><span class="sxs-lookup"><span data-stu-id="09bd5-127">-Id</span></span>
<span data-ttu-id="09bd5-128">Gibt die vollqualifizierte Ressourcen-ID für die Richtlinienzuweisung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="09bd5-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09bd5-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="09bd5-129">-IncludeDescendent</span></span>
<span data-ttu-id="09bd5-130">Bewirkt, dass in der Liste der zurückgegebenen Richtlinienzuweisungen alle Aufgaben im Zusammenhang mit dem angegebenen Bereich eingeschlossen werden, einschließlich derer aus übergeordneten Bereichen und aus untergeordneten Bereichen.</span><span class="sxs-lookup"><span data-stu-id="09bd5-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IncludeDescendentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09bd5-131">-Information</span><span class="sxs-lookup"><span data-stu-id="09bd5-131">-InformationAction</span></span>
<span data-ttu-id="09bd5-132">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="09bd5-132">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="09bd5-133">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="09bd5-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="09bd5-134">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="09bd5-134">Continue</span></span>
- <span data-ttu-id="09bd5-135">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="09bd5-135">Ignore</span></span>
- <span data-ttu-id="09bd5-136">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="09bd5-136">Inquire</span></span>
- <span data-ttu-id="09bd5-137">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="09bd5-137">SilentlyContinue</span></span>
- <span data-ttu-id="09bd5-138">Beenden</span><span class="sxs-lookup"><span data-stu-id="09bd5-138">Stop</span></span>
- <span data-ttu-id="09bd5-139">Anhalten</span><span class="sxs-lookup"><span data-stu-id="09bd5-139">Suspend</span></span>

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

### <span data-ttu-id="09bd5-140">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="09bd5-140">-InformationVariable</span></span>
<span data-ttu-id="09bd5-141">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="09bd5-141">Specifies an information variable.</span></span>

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

### <span data-ttu-id="09bd5-142">-Name</span><span class="sxs-lookup"><span data-stu-id="09bd5-142">-Name</span></span>
<span data-ttu-id="09bd5-143">Gibt den Namen der Richtlinien Aufgabe an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="09bd5-143">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09bd5-144">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="09bd5-144">-PolicyDefinitionId</span></span>
<span data-ttu-id="09bd5-145">Gibt die ID der Richtliniendefinition für die Richtlinienzuweisungen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="09bd5-145">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09bd5-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="09bd5-146">-Pre</span></span>
<span data-ttu-id="09bd5-147">Gibt an, dass dieses Cmdlet Pre-Release-API-Versionen berücksichtigt, wenn es automatisch die zu verwendende Version bestimmt.</span><span class="sxs-lookup"><span data-stu-id="09bd5-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="09bd5-148">-Scope</span><span class="sxs-lookup"><span data-stu-id="09bd5-148">-Scope</span></span>
<span data-ttu-id="09bd5-149">Gibt den Bereich an, auf dem die Richtlinie für die Aufgabe angewendet wird, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="09bd5-149">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IncludeDescendentParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09bd5-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09bd5-150">CommonParameters</span></span>
<span data-ttu-id="09bd5-151">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09bd5-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09bd5-152">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09bd5-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09bd5-153">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09bd5-153">INPUTS</span></span>

## <span data-ttu-id="09bd5-154">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09bd5-154">OUTPUTS</span></span>

## <span data-ttu-id="09bd5-155">Notizen</span><span class="sxs-lookup"><span data-stu-id="09bd5-155">NOTES</span></span>

## <span data-ttu-id="09bd5-156">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09bd5-156">RELATED LINKS</span></span>

[<span data-ttu-id="09bd5-157">Neu – AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="09bd5-157">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="09bd5-158">Remove-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="09bd5-158">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="09bd5-159">Satz-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="09bd5-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


