---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 80ab75e2361cf052e88377e9d7a393fb36627ae7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98386293"
---
# <span data-ttu-id="835db-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="835db-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="835db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="835db-102">SYNOPSIS</span></span>
<span data-ttu-id="835db-103">Erstellt eine PrincipalAssignment für die Kusto-Clusterdatenbank.</span><span class="sxs-lookup"><span data-stu-id="835db-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="835db-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="835db-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="835db-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="835db-105">DESCRIPTION</span></span>
<span data-ttu-id="835db-106">Erstellt eine PrincipalAssignment für die Kusto-Clusterdatenbank.</span><span class="sxs-lookup"><span data-stu-id="835db-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="835db-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="835db-107">EXAMPLES</span></span>

### <span data-ttu-id="835db-108">Beispiel 1: Erstellen einer PrincipalAssignment für eine Kusto-Clusterdatenbank</span><span class="sxs-lookup"><span data-stu-id="835db-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="835db-109">Mit dem oben angegebenen Befehl wird eine PrincipalAssignment für die Kusto-Clusterdatenbank erstellt.</span><span class="sxs-lookup"><span data-stu-id="835db-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="835db-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="835db-110">PARAMETERS</span></span>

### <span data-ttu-id="835db-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="835db-111">-AsJob</span></span>
<span data-ttu-id="835db-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="835db-112">Run the command as a job</span></span>

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

### <span data-ttu-id="835db-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="835db-113">-ClusterName</span></span>
<span data-ttu-id="835db-114">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="835db-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="835db-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="835db-115">-DatabaseName</span></span>
<span data-ttu-id="835db-116">Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="835db-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="835db-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="835db-117">-DefaultProfile</span></span>
<span data-ttu-id="835db-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="835db-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="835db-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="835db-119">-NoWait</span></span>
<span data-ttu-id="835db-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="835db-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="835db-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="835db-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="835db-122">Der Name der Kusto PrincipalAssignment.</span><span class="sxs-lookup"><span data-stu-id="835db-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="835db-123">-PrincipalId</span><span class="sxs-lookup"><span data-stu-id="835db-123">-PrincipalId</span></span>
<span data-ttu-id="835db-124">Die dem Datenbankprinzipal zugewiesene Prinzipal-ID.</span><span class="sxs-lookup"><span data-stu-id="835db-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="835db-125">Es kann sich um eine Benutzer-E-Mail, anwendungs-ID oder den Namen einer Sicherheitsgruppe geben.</span><span class="sxs-lookup"><span data-stu-id="835db-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="835db-126">-PrincipalType</span><span class="sxs-lookup"><span data-stu-id="835db-126">-PrincipalType</span></span>
<span data-ttu-id="835db-127">Prinzipaltyp.</span><span class="sxs-lookup"><span data-stu-id="835db-127">Principal type.</span></span>

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

### <span data-ttu-id="835db-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="835db-128">-ResourceGroupName</span></span>
<span data-ttu-id="835db-129">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="835db-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="835db-130">-Role</span><span class="sxs-lookup"><span data-stu-id="835db-130">-Role</span></span>
<span data-ttu-id="835db-131">Datenbankprinzipalrolle.</span><span class="sxs-lookup"><span data-stu-id="835db-131">Database principal role.</span></span>

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

### <span data-ttu-id="835db-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="835db-132">-SubscriptionId</span></span>
<span data-ttu-id="835db-133">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="835db-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="835db-134">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="835db-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="835db-135">-TenantId</span><span class="sxs-lookup"><span data-stu-id="835db-135">-TenantId</span></span>
<span data-ttu-id="835db-136">Die Mandanten-ID des Prinzipal</span><span class="sxs-lookup"><span data-stu-id="835db-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="835db-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="835db-137">-Confirm</span></span>
<span data-ttu-id="835db-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="835db-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="835db-139">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="835db-139">-WhatIf</span></span>
<span data-ttu-id="835db-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="835db-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="835db-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="835db-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="835db-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="835db-142">CommonParameters</span></span>
<span data-ttu-id="835db-143">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="835db-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="835db-144">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="835db-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="835db-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="835db-145">INPUTS</span></span>

## <span data-ttu-id="835db-146">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="835db-146">OUTPUTS</span></span>

### <span data-ttu-id="835db-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="835db-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="835db-148">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="835db-148">NOTES</span></span>

<span data-ttu-id="835db-149">ALIASE</span><span class="sxs-lookup"><span data-stu-id="835db-149">ALIASES</span></span>

## <span data-ttu-id="835db-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="835db-150">RELATED LINKS</span></span>

