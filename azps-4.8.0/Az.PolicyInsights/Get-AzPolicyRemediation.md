---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PolicyInsights.dll-Help.xml
Module Name: Az.PolicyInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.policyinsights/get-azpolicyremediation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PolicyInsights/PolicyInsights/help/Get-AzPolicyRemediation.md
ms.openlocfilehash: 44c12e08ca66c19cf3541f4abb200e1ba0663208
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174490"
---
# <span data-ttu-id="a7d24-101">Get-AzPolicyRemediation</span><span class="sxs-lookup"><span data-stu-id="a7d24-101">Get-AzPolicyRemediation</span></span>

## <span data-ttu-id="a7d24-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a7d24-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d24-103">Ruft Richtlinien Behebungen ab.</span><span class="sxs-lookup"><span data-stu-id="a7d24-103">Gets policy remediations.</span></span>

## <span data-ttu-id="a7d24-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7d24-104">SYNTAX</span></span>

### <span data-ttu-id="a7d24-105">SubscriptionScope (Standard)</span><span class="sxs-lookup"><span data-stu-id="a7d24-105">SubscriptionScope (Default)</span></span>
```
Get-AzPolicyRemediation [-Top <Int32>] [-Filter <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7d24-106">ByName</span><span class="sxs-lookup"><span data-stu-id="a7d24-106">ByName</span></span>
```
Get-AzPolicyRemediation -Name <String> [-Scope <String>] [-ManagementGroupName <String>]
 [-ResourceGroupName <String>] [-Top <Int32>] [-IncludeDetail] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a7d24-107">GenericScope</span><span class="sxs-lookup"><span data-stu-id="a7d24-107">GenericScope</span></span>
```
Get-AzPolicyRemediation -Scope <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7d24-108">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="a7d24-108">ManagementGroupScope</span></span>
```
Get-AzPolicyRemediation -ManagementGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7d24-109">ResourceGroupScope</span><span class="sxs-lookup"><span data-stu-id="a7d24-109">ResourceGroupScope</span></span>
```
Get-AzPolicyRemediation -ResourceGroupName <String> [-Top <Int32>] [-Filter <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a7d24-110">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a7d24-110">ByResourceId</span></span>
```
Get-AzPolicyRemediation -ResourceId <String> [-Top <Int32>] [-IncludeDetail]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a7d24-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a7d24-111">DESCRIPTION</span></span>
<span data-ttu-id="a7d24-112">Das Cmdlet " **Get-AzPolicyRemediation** " ruft alle Richtlinien Behebungen in einem Bereich oder einer bestimmten Behebung ab.</span><span class="sxs-lookup"><span data-stu-id="a7d24-112">The **Get-AzPolicyRemediation** cmdlet gets all policy remediations in a scope or a particular remediation.</span></span>

## <span data-ttu-id="a7d24-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a7d24-113">EXAMPLES</span></span>

### <span data-ttu-id="a7d24-114">Beispiel 1: Abrufen aller Richtlinien Behebungen im aktuellen Abonnement</span><span class="sxs-lookup"><span data-stu-id="a7d24-114">Example 1: Get all policy remediations in the current subscription</span></span>
```
PS C:\> Select-AzSubscription -Subscription "My Subscription"
PS C:\> Get-AzPolicyRemediation
```

<span data-ttu-id="a7d24-115">Dieser Befehl ruft alle Behebungen ab, die am oder unterhalb eines Abonnements mit dem Namen "mein Abonnement" erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="a7d24-115">This command gets all the remediations created at or underneath a subscription named 'My Subscription'.</span></span>

### <span data-ttu-id="a7d24-116">Beispiel 2: Abrufen einer bestimmten Richtlinien Behebung und der Bereitstellungsdetails</span><span class="sxs-lookup"><span data-stu-id="a7d24-116">Example 2: Get a specific policy remediation and the deployment details</span></span>
```
PS C:\> Get-AzPolicyRemediation -ResourceGroupName "myResourceGroup" -Name "remediation1" -IncludeDetail
```

<span data-ttu-id="a7d24-117">Dieser Befehl ruft die Behebung mit dem Namen "remediation1" aus der Ressourcengruppe "myresourcegroup" ab.</span><span class="sxs-lookup"><span data-stu-id="a7d24-117">This command gets the remediation named 'remediation1' from resource group 'myResourceGroup'.</span></span> <span data-ttu-id="a7d24-118">Die Details der Ressourcen, die wiederhergestellt werden, sind enthalten.</span><span class="sxs-lookup"><span data-stu-id="a7d24-118">The details of the resources being remediated will be included.</span></span>

### <span data-ttu-id="a7d24-119">Beispiel 3: Abrufen von 10 Richtlinien Behebungen in einer Verwaltungsgruppe mit optionalen Filtern</span><span class="sxs-lookup"><span data-stu-id="a7d24-119">Example 3: Get 10 policy remediations in a management group with optional filters</span></span>
```
PS C:\> Get-AzPolicyRemediation -ManagementGroupName "mg1" -Top 10 -Filter "PolicyAssignmentId eq '/providers/Microsoft.Management/managementGroups/mg1/providers/Microsoft.Authorization/policyAssignments/pa1'"
```

<span data-ttu-id="a7d24-120">Dieser Befehl erhält maximal 10 Richtlinien Behebungen von einer Verwaltungsgruppe mit dem Namen "mg1".</span><span class="sxs-lookup"><span data-stu-id="a7d24-120">This command gets a max of 10 policy remediations from a management group named 'mg1'.</span></span> <span data-ttu-id="a7d24-121">Es werden nur Richtlinien Behebungen für die angegebene Richtlinienzuweisung abgerufen.</span><span class="sxs-lookup"><span data-stu-id="a7d24-121">Only policy remediations for the given policy assignment will be retrieved.</span></span>

## <span data-ttu-id="a7d24-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7d24-122">PARAMETERS</span></span>

### <span data-ttu-id="a7d24-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d24-123">-DefaultProfile</span></span>
<span data-ttu-id="a7d24-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a7d24-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7d24-125">-Filter</span><span class="sxs-lookup"><span data-stu-id="a7d24-125">-Filter</span></span>
<span data-ttu-id="a7d24-126">Filter Ausdruck mit OData-Notation</span><span class="sxs-lookup"><span data-stu-id="a7d24-126">Filter expression using OData notation.</span></span>

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

### <span data-ttu-id="a7d24-127">-IncludeDetail</span><span class="sxs-lookup"><span data-stu-id="a7d24-127">-IncludeDetail</span></span>
<span data-ttu-id="a7d24-128">Fügen Sie Details zu den von der Behebung erstellten Bereitstellungen ein.</span><span class="sxs-lookup"><span data-stu-id="a7d24-128">Include details of the deployments created by the remediation.</span></span>

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

### <span data-ttu-id="a7d24-129">-ManagementGroupName</span><span class="sxs-lookup"><span data-stu-id="a7d24-129">-ManagementGroupName</span></span>
<span data-ttu-id="a7d24-130">Verwaltungsgruppen-ID.</span><span class="sxs-lookup"><span data-stu-id="a7d24-130">Management group ID.</span></span>

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

### <span data-ttu-id="a7d24-131">-Name</span><span class="sxs-lookup"><span data-stu-id="a7d24-131">-Name</span></span>
<span data-ttu-id="a7d24-132">Ressourcenname</span><span class="sxs-lookup"><span data-stu-id="a7d24-132">Resource name.</span></span>

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

### <span data-ttu-id="a7d24-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7d24-133">-ResourceGroupName</span></span>
<span data-ttu-id="a7d24-134">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a7d24-134">Resource group name.</span></span>

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

### <span data-ttu-id="a7d24-135">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a7d24-135">-ResourceId</span></span>
<span data-ttu-id="a7d24-136">Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a7d24-136">Resource ID.</span></span>

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

### <span data-ttu-id="a7d24-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="a7d24-137">-Scope</span></span>
<span data-ttu-id="a7d24-138">Der Bereich der Ressource.</span><span class="sxs-lookup"><span data-stu-id="a7d24-138">Scope of the resource.</span></span> <span data-ttu-id="a7d24-139">Beispiel: "/Subscriptions/{SubscriptionId}/resourceGroups/{rgName}".</span><span class="sxs-lookup"><span data-stu-id="a7d24-139">For example, '/subscriptions/{subscriptionId}/resourceGroups/{rgName}'.</span></span>

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

### <span data-ttu-id="a7d24-140">-Top</span><span class="sxs-lookup"><span data-stu-id="a7d24-140">-Top</span></span>
<span data-ttu-id="a7d24-141">Die maximale Anzahl von Datensätzen, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a7d24-141">Maximum number of records to return.</span></span>

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

### <span data-ttu-id="a7d24-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d24-142">CommonParameters</span></span>
<span data-ttu-id="a7d24-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7d24-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d24-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a7d24-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d24-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a7d24-145">INPUTS</span></span>

### <span data-ttu-id="a7d24-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a7d24-146">System.String</span></span>

## <span data-ttu-id="a7d24-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a7d24-147">OUTPUTS</span></span>

### <span data-ttu-id="a7d24-148">Microsoft. Azure. Commands. PolicyInsights. Models. Remediation. PSRemediation</span><span class="sxs-lookup"><span data-stu-id="a7d24-148">Microsoft.Azure.Commands.PolicyInsights.Models.Remediation.PSRemediation</span></span>

## <span data-ttu-id="a7d24-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="a7d24-149">NOTES</span></span>

## <span data-ttu-id="a7d24-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a7d24-150">RELATED LINKS</span></span>
