---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 80ab75e2361cf052e88377e9d7a393fb36627ae7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100170430"
---
# <span data-ttu-id="fbbdc-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="fbbdc-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="fbbdc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbbdc-102">SYNOPSIS</span></span>
<span data-ttu-id="fbbdc-103">Erstellt eine PrincipalAssignment für die Kusto-Clusterdatenbank.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="fbbdc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbbdc-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fbbdc-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbbdc-105">DESCRIPTION</span></span>
<span data-ttu-id="fbbdc-106">Erstellt eine PrincipalAssignment für die Kusto-Clusterdatenbank.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="fbbdc-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fbbdc-107">EXAMPLES</span></span>

### <span data-ttu-id="fbbdc-108">Beispiel 1: Erstellen einer PrincipalAssignment für eine Kusto-Clusterdatenbank</span><span class="sxs-lookup"><span data-stu-id="fbbdc-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="fbbdc-109">Mit dem oben angegebenen Befehl wird eine PrincipalAssignment für die Kusto-Clusterdatenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="fbbdc-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbbdc-110">PARAMETERS</span></span>

### <span data-ttu-id="fbbdc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbbdc-111">-AsJob</span></span>
<span data-ttu-id="fbbdc-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="fbbdc-112">Run the command as a job</span></span>

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

### <span data-ttu-id="fbbdc-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="fbbdc-113">-ClusterName</span></span>
<span data-ttu-id="fbbdc-114">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="fbbdc-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="fbbdc-115">-DatabaseName</span></span>
<span data-ttu-id="fbbdc-116">Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="fbbdc-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="fbbdc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbbdc-117">-DefaultProfile</span></span>
<span data-ttu-id="fbbdc-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbbdc-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fbbdc-119">-NoWait</span></span>
<span data-ttu-id="fbbdc-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="fbbdc-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fbbdc-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="fbbdc-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="fbbdc-122">Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="fbbdc-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="fbbdc-123">-PrincipalId</span></span>
<span data-ttu-id="fbbdc-124">Die dem Datenbankprinzipal zugewiesene Prinzipal-ID.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="fbbdc-125">Es kann sich um eine E-Mail-Adresse, anwendungs-ID oder einen Namen für eine Sicherheitsgruppe geben.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="fbbdc-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="fbbdc-126">-PrincipalType</span></span>
<span data-ttu-id="fbbdc-127">Prinzipaltyp.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-127">Principal type.</span></span>

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

### <span data-ttu-id="fbbdc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbbdc-128">-ResourceGroupName</span></span>
<span data-ttu-id="fbbdc-129">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="fbbdc-130">-Role</span><span class="sxs-lookup"><span data-stu-id="fbbdc-130">-Role</span></span>
<span data-ttu-id="fbbdc-131">Datenbankprinzipalrolle.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-131">Database principal role.</span></span>

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

### <span data-ttu-id="fbbdc-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fbbdc-132">-SubscriptionId</span></span>
<span data-ttu-id="fbbdc-133">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="fbbdc-134">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fbbdc-135">-TenantId</span><span class="sxs-lookup"><span data-stu-id="fbbdc-135">-TenantId</span></span>
<span data-ttu-id="fbbdc-136">Die Mandanten-ID des Prinzipal</span><span class="sxs-lookup"><span data-stu-id="fbbdc-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="fbbdc-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbbdc-137">-Confirm</span></span>
<span data-ttu-id="fbbdc-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbbdc-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fbbdc-139">-WhatIf</span></span>
<span data-ttu-id="fbbdc-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbbdc-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbbdc-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbbdc-142">CommonParameters</span></span>
<span data-ttu-id="fbbdc-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbbdc-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbbdc-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbbdc-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbbdc-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fbbdc-145">INPUTS</span></span>

## <span data-ttu-id="fbbdc-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fbbdc-146">OUTPUTS</span></span>

### <span data-ttu-id="fbbdc-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="fbbdc-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="fbbdc-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fbbdc-148">NOTES</span></span>

<span data-ttu-id="fbbdc-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="fbbdc-149">ALIASES</span></span>

## <span data-ttu-id="fbbdc-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fbbdc-150">RELATED LINKS</span></span>

