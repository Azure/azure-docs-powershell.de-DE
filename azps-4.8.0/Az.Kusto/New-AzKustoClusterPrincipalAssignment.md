---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoclusterprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoClusterPrincipalAssignment.md
ms.openlocfilehash: 8f2a0cd576c3fe7f184d3f016f6666aa8749b5c2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173754"
---
# <span data-ttu-id="333b7-101">New-AzKustoClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="333b7-101">New-AzKustoClusterPrincipalAssignment</span></span>

## <span data-ttu-id="333b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="333b7-102">SYNOPSIS</span></span>
<span data-ttu-id="333b7-103">Erstellen Sie ein Kusto-Cluster-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="333b7-103">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="333b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="333b7-104">SYNTAX</span></span>

```
New-AzKustoClusterPrincipalAssignment -ClusterName <String> -PrincipalAssignmentName <String>
 -ResourceGroupName <String> [-SubscriptionId <String>] [-PrincipalId <String>]
 [-PrincipalType <PrincipalType>] [-Role <ClusterPrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="333b7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="333b7-105">DESCRIPTION</span></span>
<span data-ttu-id="333b7-106">Erstellen Sie ein Kusto-Cluster-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="333b7-106">Create a Kusto cluster principalAssignment.</span></span>

## <span data-ttu-id="333b7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="333b7-107">EXAMPLES</span></span>

### <span data-ttu-id="333b7-108">Beispiel 1: Erstellen eines Kusto-Clusters principalAssignment</span><span class="sxs-lookup"><span data-stu-id="333b7-108">Example 1: Create a Kusto cluster principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoClusterPrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role AllDatabasesAdmin

Name                                Type
----                                ----
testnewkustocluster/kustoprincipal1 Microsoft.Kusto/Clusters/PrincipalAssignments
```

<span data-ttu-id="333b7-109">Der obige Befehl erstellt einen Kusto-Cluster principalAssignment</span><span class="sxs-lookup"><span data-stu-id="333b7-109">The above command creates a Kusto cluster principalAssignment</span></span>

## <span data-ttu-id="333b7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="333b7-110">PARAMETERS</span></span>

### <span data-ttu-id="333b7-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="333b7-111">-AsJob</span></span>
<span data-ttu-id="333b7-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="333b7-112">Run the command as a job</span></span>

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

### <span data-ttu-id="333b7-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="333b7-113">-ClusterName</span></span>
<span data-ttu-id="333b7-114">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="333b7-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="333b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="333b7-115">-DefaultProfile</span></span>
<span data-ttu-id="333b7-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="333b7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="333b7-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="333b7-117">-NoWait</span></span>
<span data-ttu-id="333b7-118">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="333b7-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="333b7-119">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="333b7-119">-PrincipalAssignmentName</span></span>
<span data-ttu-id="333b7-120">Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="333b7-120">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="333b7-121">-Prinzipal-Nr</span><span class="sxs-lookup"><span data-stu-id="333b7-121">-PrincipalId</span></span>
<span data-ttu-id="333b7-122">Die Prinzipal-ID, die dem Cluster Prinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="333b7-122">The principal ID assigned to the cluster principal.</span></span>
<span data-ttu-id="333b7-123">Hierbei kann es sich um eine Benutzer-e-Mail, eine Anwendungs-ID oder einen Sicherheitsgruppen Namen handeln.</span><span class="sxs-lookup"><span data-stu-id="333b7-123">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="333b7-124">-Principaltype</span><span class="sxs-lookup"><span data-stu-id="333b7-124">-PrincipalType</span></span>
<span data-ttu-id="333b7-125">Principal-Typ.</span><span class="sxs-lookup"><span data-stu-id="333b7-125">Principal type.</span></span>

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

### <span data-ttu-id="333b7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="333b7-126">-ResourceGroupName</span></span>
<span data-ttu-id="333b7-127">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="333b7-127">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="333b7-128">-Role</span><span class="sxs-lookup"><span data-stu-id="333b7-128">-Role</span></span>
<span data-ttu-id="333b7-129">Hauptrolle des Clusters.</span><span class="sxs-lookup"><span data-stu-id="333b7-129">Cluster principal role.</span></span>

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

### <span data-ttu-id="333b7-130">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="333b7-130">-SubscriptionId</span></span>
<span data-ttu-id="333b7-131">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="333b7-131">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="333b7-132">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="333b7-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="333b7-133">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="333b7-133">-TenantId</span></span>
<span data-ttu-id="333b7-134">Die Mandanten-ID des Prinzipals</span><span class="sxs-lookup"><span data-stu-id="333b7-134">The tenant id of the principal</span></span>

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

### <span data-ttu-id="333b7-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="333b7-135">-Confirm</span></span>
<span data-ttu-id="333b7-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="333b7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="333b7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="333b7-137">-WhatIf</span></span>
<span data-ttu-id="333b7-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="333b7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="333b7-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="333b7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="333b7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="333b7-140">CommonParameters</span></span>
<span data-ttu-id="333b7-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="333b7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="333b7-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="333b7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="333b7-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="333b7-143">INPUTS</span></span>

## <span data-ttu-id="333b7-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="333b7-144">OUTPUTS</span></span>

### <span data-ttu-id="333b7-145">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. IClusterPrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="333b7-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IClusterPrincipalAssignment</span></span>

## <span data-ttu-id="333b7-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="333b7-146">NOTES</span></span>

<span data-ttu-id="333b7-147">Aliase</span><span class="sxs-lookup"><span data-stu-id="333b7-147">ALIASES</span></span>

## <span data-ttu-id="333b7-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="333b7-148">RELATED LINKS</span></span>

