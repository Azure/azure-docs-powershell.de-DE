---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
ms.openlocfilehash: 44c12e08ca66c19cf3541f4abb200e1ba0663208
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302696"
---
# <span data-ttu-id="29914-101">Get-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="29914-101">Get-AzPolicyRemediation</span></span>

## <span data-ttu-id="29914-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="29914-102">SYNOPSIS</span></span>
<span data-ttu-id="29914-103">Ruft Richtlinienbehebungen ab.</span><span class="sxs-lookup"><span data-stu-id="29914-103">Gets policy remediations.</span></span>

## <span data-ttu-id="29914-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="29914-104">SYNTAX</span></span>

### <span data-ttu-id="29914-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="29914-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29914-106">ByName</span><span class="sxs-lookup"><span data-stu-id="29914-106">ByName</span></span>
```
Get-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="29914-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="29914-107">GenericScope</span></span>
```
Get-AzPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29914-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="29914-108">ManagementGroupScope</span></span>
```
Get-AzPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29914-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="29914-109">ResourceGroupScope</span></span>
```
Get-AzPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="29914-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="29914-110">ByResourceId</span></span>
```
Get-AzPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="29914-111">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="29914-111">DESCRIPTION</span></span>
<span data-ttu-id="29914-112">Das **Cmdlet "Get-AzPolicyRemediation"** ruft alle Richtlinienbehebungen in einem Bereich oder einer bestimmten Wartung ab.</span><span class="sxs-lookup"><span data-stu-id="29914-112">The **Get-AzPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="29914-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="29914-113">EXAMPLES</span></span>

### <span data-ttu-id="29914-114">Beispiel 1: Alle Richtlinienbehebungen im aktuellen Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="29914-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Get-AzPolicyRemediation
```

<span data-ttu-id="29914-115">Dieser Befehl ruft alle Korrekturen ab, die bei oder unter einem Abonnement mit dem Namen "Mein Abonnement" erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="29914-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="29914-116">Beispiel 2: Erhalten einer bestimmten Richtlinienbehebung und der Bereitstellungsdetails</span><span class="sxs-lookup"><span data-stu-id="29914-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="29914-117">Dieser Befehl ruft die Wartung mit dem Namen 'remediation1' aus der Ressourcengruppe 'myResourceGroup' ab.</span><span class="sxs-lookup"><span data-stu-id="29914-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="29914-118">Die Details der ressourcen, die behoben werden sollen, werden einbezogen.</span><span class="sxs-lookup"><span data-stu-id="29914-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="29914-119">Beispiel 3: Erhalten von 10 Richtlinienbehebungen in einer Verwaltungsgruppe mit optionalen Filtern</span><span class="sxs-lookup"><span data-stu-id="29914-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="29914-120">Dieser Befehl ruft maximal 10 Richtlinienbehebungen von einer Verwaltungsgruppe namens "mg1" ab.</span><span class="sxs-lookup"><span data-stu-id="29914-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="29914-121">Es werden nur Richtlinienbehebungen für die angegebene Richtlinienzuweisung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="29914-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="29914-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="29914-122">PARAMETERS</span></span>

### <span data-ttu-id="29914-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29914-123">-DefaultProfile</span></span>
<span data-ttu-id="29914-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="29914-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="29914-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="29914-125">-Filter</span></span>
<span data-ttu-id="29914-126">Filtern von Ausdrücken mithilfe der OData-Notation.</span><span class="sxs-lookup"><span data-stu-id="29914-126">Filter expression using OData notation.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, GenericScope, ManagementGroupScope, ResourceGroupScope
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29914-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="29914-127">-IncludeDetail</span></span>
<span data-ttu-id="29914-128">Fügen Sie Details zu den Bereitstellungen ein, die durch die Wartung erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="29914-128">Include details of the deployments created by the remediation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29914-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="29914-129">-ManagementGroupName</span></span>
<span data-ttu-id="29914-130">ID der Verwaltungsgruppe.</span><span class="sxs-lookup"><span data-stu-id="29914-130">Management group ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29914-131">-Name</span><span class="sxs-lookup"><span data-stu-id="29914-131">-Name</span></span>
<span data-ttu-id="29914-132">Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="29914-132">Resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29914-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29914-133">-ResourceGroupName</span></span>
<span data-ttu-id="29914-134">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="29914-134">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ResourceGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29914-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29914-135">-ResourceId</span></span>
<span data-ttu-id="29914-136">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="29914-136">Resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29914-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="29914-137">-Scope</span></span>
<span data-ttu-id="29914-138">Umfang der Ressource.</span><span class="sxs-lookup"><span data-stu-id="29914-138">Scope of the resource.</span></span> <span data-ttu-id="29914-139">Beispiel: '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span><span class="sxs-lookup"><span data-stu-id="29914-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GenericScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29914-140">-Top</span><span class="sxs-lookup"><span data-stu-id="29914-140">-Top</span></span>
<span data-ttu-id="29914-141">Maximale Anzahl der zurückzukehrende Datensätze.</span><span class="sxs-lookup"><span data-stu-id="29914-141">Maximum number of records to return.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="29914-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29914-142">CommonParameters</span></span>
<span data-ttu-id="29914-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29914-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29914-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="29914-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29914-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="29914-145">INPUTS</span></span>

### <span data-ttu-id="29914-146">System.String</span><span class="sxs-lookup"><span data-stu-id="29914-146">System.String</span></span>

## <span data-ttu-id="29914-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="29914-147">OUTPUTS</span></span>

### <span data-ttu-id="29914-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span><span class="sxs-lookup"><span data-stu-id="29914-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="29914-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="29914-149">NOTES</span></span>

## <span data-ttu-id="29914-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="29914-150">RELATED LINKS</span></span>
