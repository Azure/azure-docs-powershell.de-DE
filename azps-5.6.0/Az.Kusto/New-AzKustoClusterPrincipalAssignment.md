---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 738f0d4b4033dd7cccdc0fbabe94d2dfde9779c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101922387"
---
# <span data-ttu-id="23493-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="23493-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="23493-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23493-102">SYNOPSIS</span></span>
<span data-ttu-id="23493-103">Erstellen Sie einen Kusto-ClusterprinzipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="23493-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="23493-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23493-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="23493-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23493-105">DESCRIPTION</span></span>
<span data-ttu-id="23493-106">Erstellen Sie einen Kusto-ClusterprinzipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="23493-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="23493-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="23493-107">EXAMPLES</span></span>

### <span data-ttu-id="23493-108">Beispiel 1: Erstellen einer Kusto-Clusterprinzipalzuweisung</span><span class="sxs-lookup"><span data-stu-id="23493-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="23493-109">Mit dem obigen Befehl wird ein Kusto-ClusterprinzipalAssignment erstellt.</span><span class="sxs-lookup"><span data-stu-id="23493-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="23493-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="23493-110">PARAMETERS</span></span>

### <span data-ttu-id="23493-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="23493-111">-AsJob</span></span>
<span data-ttu-id="23493-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="23493-112">Run the command as a job</span></span>

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

### <span data-ttu-id="23493-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="23493-113">-ClusterName</span></span>
<span data-ttu-id="23493-114">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="23493-114">The name of the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23493-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23493-115">-DefaultProfile</span></span>
<span data-ttu-id="23493-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23493-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23493-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="23493-117">-NoWait</span></span>
<span data-ttu-id="23493-118">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="23493-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="23493-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="23493-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="23493-120">Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="23493-120">The name of the Kusto principalAssignment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23493-121">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="23493-121">-PrincipalId</span></span>
<span data-ttu-id="23493-122">Die dem Clusterprinzipal zugewiesene Prinzipal-ID.</span><span class="sxs-lookup"><span data-stu-id="23493-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="23493-123">Dabei kann es sich um eine Benutzer-E-Mail, anwendungs-ID oder einen Sicherheitsgruppennamen geben.</span><span class="sxs-lookup"><span data-stu-id="23493-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="23493-124">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="23493-124">-PrincipalType</span></span>
<span data-ttu-id="23493-125">Prinzipaltyp.</span><span class="sxs-lookup"><span data-stu-id="23493-125">Principal type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.PrincipalType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23493-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23493-126">-ResourceGroupName</span></span>
<span data-ttu-id="23493-127">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="23493-127">The name of the resource group containing the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23493-128">-Rolle</span><span class="sxs-lookup"><span data-stu-id="23493-128">-Role</span></span>
<span data-ttu-id="23493-129">Clusterprinzipalrolle.</span><span class="sxs-lookup"><span data-stu-id="23493-129">Cluster principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.ClusterPrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23493-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23493-130">-SubscriptionId</span></span>
<span data-ttu-id="23493-131">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="23493-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="23493-132">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="23493-132">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23493-133">-TenantId</span><span class="sxs-lookup"><span data-stu-id="23493-133">-TenantId</span></span>
<span data-ttu-id="23493-134">Die Mandanten-ID des Prinzipal</span><span class="sxs-lookup"><span data-stu-id="23493-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="23493-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="23493-135">-Confirm</span></span>
<span data-ttu-id="23493-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="23493-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23493-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23493-137">-WhatIf</span></span>
<span data-ttu-id="23493-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="23493-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23493-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="23493-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23493-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23493-140">CommonParameters</span></span>
<span data-ttu-id="23493-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23493-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23493-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23493-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23493-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="23493-143">INPUTS</span></span>

## <span data-ttu-id="23493-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="23493-144">OUTPUTS</span></span>

### <span data-ttu-id="23493-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="23493-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="23493-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="23493-146">NOTES</span></span>

<span data-ttu-id="23493-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="23493-147">ALIASES</span></span>

## <span data-ttu-id="23493-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="23493-148">RELATED LINKS</span></span>

