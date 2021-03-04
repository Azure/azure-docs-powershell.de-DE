---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 9fd729a85babf1440516c52f0e7737f4c0d0d281
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101927960"
---
# <span data-ttu-id="69542-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="69542-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="69542-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69542-102">SYNOPSIS</span></span>
<span data-ttu-id="69542-103">Erstellt einen Kusto-ClusterdatenbankprinzipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="69542-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="69542-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="69542-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="69542-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="69542-105">DESCRIPTION</span></span>
<span data-ttu-id="69542-106">Erstellt einen Kusto-ClusterdatenbankprinzipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="69542-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="69542-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="69542-107">EXAMPLES</span></span>

### <span data-ttu-id="69542-108">Beispiel 1: Erstellen eines Kusto-ClusterdatenbankprinzipalAssignment</span><span class="sxs-lookup"><span data-stu-id="69542-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="69542-109">Mit dem obigen Befehl wird ein Kusto-ClusterdatenbankprinzipalAssignment erstellt.</span><span class="sxs-lookup"><span data-stu-id="69542-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="69542-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="69542-110">PARAMETERS</span></span>

### <span data-ttu-id="69542-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="69542-111">-AsJob</span></span>
<span data-ttu-id="69542-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="69542-112">Run the command as a job</span></span>

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

### <span data-ttu-id="69542-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="69542-113">-ClusterName</span></span>
<span data-ttu-id="69542-114">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="69542-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="69542-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="69542-115">-DatabaseName</span></span>
<span data-ttu-id="69542-116">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="69542-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="69542-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69542-117">-DefaultProfile</span></span>
<span data-ttu-id="69542-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="69542-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69542-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="69542-119">-NoWait</span></span>
<span data-ttu-id="69542-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="69542-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="69542-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="69542-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="69542-122">Der Name der Kusto principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="69542-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="69542-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="69542-123">-PrincipalId</span></span>
<span data-ttu-id="69542-124">Die dem Datenbankprinzipal zugewiesene Prinzipal-ID.</span><span class="sxs-lookup"><span data-stu-id="69542-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="69542-125">Dabei kann es sich um eine Benutzer-E-Mail, anwendungs-ID oder einen Sicherheitsgruppennamen geben.</span><span class="sxs-lookup"><span data-stu-id="69542-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="69542-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="69542-126">-PrincipalType</span></span>
<span data-ttu-id="69542-127">Prinzipaltyp.</span><span class="sxs-lookup"><span data-stu-id="69542-127">Principal type.</span></span>

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

### <span data-ttu-id="69542-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="69542-128">-ResourceGroupName</span></span>
<span data-ttu-id="69542-129">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="69542-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="69542-130">-Rolle</span><span class="sxs-lookup"><span data-stu-id="69542-130">-Role</span></span>
<span data-ttu-id="69542-131">Datenbankprinzipalrolle.</span><span class="sxs-lookup"><span data-stu-id="69542-131">Database principal role.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DatabasePrincipalRole
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="69542-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="69542-132">-SubscriptionId</span></span>
<span data-ttu-id="69542-133">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="69542-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="69542-134">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="69542-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="69542-135">-TenantId</span><span class="sxs-lookup"><span data-stu-id="69542-135">-TenantId</span></span>
<span data-ttu-id="69542-136">Die Mandanten-ID des Prinzipal</span><span class="sxs-lookup"><span data-stu-id="69542-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="69542-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="69542-137">-Confirm</span></span>
<span data-ttu-id="69542-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="69542-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="69542-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="69542-139">-WhatIf</span></span>
<span data-ttu-id="69542-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="69542-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="69542-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="69542-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="69542-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69542-142">CommonParameters</span></span>
<span data-ttu-id="69542-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="69542-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69542-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="69542-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69542-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="69542-145">INPUTS</span></span>

## <span data-ttu-id="69542-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="69542-146">OUTPUTS</span></span>

### <span data-ttu-id="69542-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="69542-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="69542-148">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="69542-148">NOTES</span></span>

<span data-ttu-id="69542-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="69542-149">ALIASES</span></span>

## <span data-ttu-id="69542-150">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="69542-150">RELATED LINKS</span></span>

