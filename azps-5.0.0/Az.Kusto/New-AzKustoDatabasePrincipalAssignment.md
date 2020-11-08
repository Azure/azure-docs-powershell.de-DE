---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabaseprincipalassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabasePrincipalAssignment.md
ms.openlocfilehash: 8bfcb3a96ee8db53a6a869a01441739ee9c503bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179197"
---
# <span data-ttu-id="d3390-101">New-AzKustoDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="d3390-101">New-AzKustoDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="d3390-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d3390-102">SYNOPSIS</span></span>
<span data-ttu-id="d3390-103">Erstellt eine Kusto-Clusterdatenbank-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d3390-103">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="d3390-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3390-104">SYNTAX</span></span>

```
New-AzKustoDatabasePrincipalAssignment -ClusterName <String> -DatabaseName <String>
 -PrincipalAssignmentName <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-PrincipalId <String>] [-PrincipalType <PrincipalType>] [-Role <DatabasePrincipalRole>] [-TenantId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d3390-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3390-105">DESCRIPTION</span></span>
<span data-ttu-id="d3390-106">Erstellt eine Kusto-Clusterdatenbank-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d3390-106">Creates a Kusto cluster database principalAssignment.</span></span>

## <span data-ttu-id="d3390-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3390-107">EXAMPLES</span></span>

### <span data-ttu-id="d3390-108">Beispiel 1: Erstellen einer Kusto-Clusterdatenbank principalAssignment</span><span class="sxs-lookup"><span data-stu-id="d3390-108">Example 1: Create a Kusto cluster database principalAssignment</span></span>
```powershell
PS C:\> New-AzKustoDatabasePrincipalAssignment -ResourceGroupName testrg -ClusterName testnewkustocluster -DatabaseName mykustodatabase -PrincipalAssignmentName kustoprincipal1 -PrincipalId "7e1cb39f-d2cb-4f0d-801a-c9ea1f376e96" -PrincipalType App -Role Admin

Name                                                Type
----                                                ----
testnewkustocluster/mykustodatabase/kustoprincipal1 Microsoft.Kusto/Clusters/Databases/PrincipalAssignments
```

<span data-ttu-id="d3390-109">Mit dem obigen Befehl wird eine Kusto-Clusterdatenbank erstellt principalAssignment</span><span class="sxs-lookup"><span data-stu-id="d3390-109">The above command creates a Kusto cluster database principalAssignment</span></span>

## <span data-ttu-id="d3390-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3390-110">PARAMETERS</span></span>

### <span data-ttu-id="d3390-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d3390-111">-AsJob</span></span>
<span data-ttu-id="d3390-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="d3390-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d3390-113">-Clustername</span><span class="sxs-lookup"><span data-stu-id="d3390-113">-ClusterName</span></span>
<span data-ttu-id="d3390-114">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="d3390-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="d3390-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d3390-115">-DatabaseName</span></span>
<span data-ttu-id="d3390-116">Der Name der Datenbank im Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="d3390-116">The name of the database in the Kusto cluster.</span></span>

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

### <span data-ttu-id="d3390-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3390-117">-DefaultProfile</span></span>
<span data-ttu-id="d3390-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d3390-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3390-119">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d3390-119">-NoWait</span></span>
<span data-ttu-id="d3390-120">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="d3390-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d3390-121">-PrincipalAssignmentName</span><span class="sxs-lookup"><span data-stu-id="d3390-121">-PrincipalAssignmentName</span></span>
<span data-ttu-id="d3390-122">Der Name des Kusto-principalAssignment.</span><span class="sxs-lookup"><span data-stu-id="d3390-122">The name of the Kusto principalAssignment.</span></span>

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

### <span data-ttu-id="d3390-123">-Prinzipal-Nr</span><span class="sxs-lookup"><span data-stu-id="d3390-123">-PrincipalId</span></span>
<span data-ttu-id="d3390-124">Die Prinzipal-ID, die dem Datenbankprinzipal zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d3390-124">The principal ID assigned to the database principal.</span></span>
<span data-ttu-id="d3390-125">Hierbei kann es sich um eine Benutzer-e-Mail, eine Anwendungs-ID oder einen Sicherheitsgruppen Namen handeln.</span><span class="sxs-lookup"><span data-stu-id="d3390-125">It can be a user email, application ID, or security group name.</span></span>

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

### <span data-ttu-id="d3390-126">-Principaltype</span><span class="sxs-lookup"><span data-stu-id="d3390-126">-PrincipalType</span></span>
<span data-ttu-id="d3390-127">Principal-Typ.</span><span class="sxs-lookup"><span data-stu-id="d3390-127">Principal type.</span></span>

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

### <span data-ttu-id="d3390-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3390-128">-ResourceGroupName</span></span>
<span data-ttu-id="d3390-129">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="d3390-129">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="d3390-130">-Role</span><span class="sxs-lookup"><span data-stu-id="d3390-130">-Role</span></span>
<span data-ttu-id="d3390-131">Datenbankprinzipal Rolle.</span><span class="sxs-lookup"><span data-stu-id="d3390-131">Database principal role.</span></span>

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

### <span data-ttu-id="d3390-132">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="d3390-132">-SubscriptionId</span></span>
<span data-ttu-id="d3390-133">Ruft Abonnement Anmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d3390-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d3390-134">Die Abonnement-ID ist Teil des URIs für jeden Dienst Anruf.</span><span class="sxs-lookup"><span data-stu-id="d3390-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d3390-135">-Mandanten-Nr</span><span class="sxs-lookup"><span data-stu-id="d3390-135">-TenantId</span></span>
<span data-ttu-id="d3390-136">Die Mandanten-ID des Prinzipals</span><span class="sxs-lookup"><span data-stu-id="d3390-136">The tenant id of the principal</span></span>

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

### <span data-ttu-id="d3390-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d3390-137">-Confirm</span></span>
<span data-ttu-id="d3390-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d3390-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3390-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3390-139">-WhatIf</span></span>
<span data-ttu-id="d3390-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3390-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3390-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3390-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3390-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3390-142">CommonParameters</span></span>
<span data-ttu-id="d3390-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3390-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3390-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d3390-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3390-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d3390-145">INPUTS</span></span>

## <span data-ttu-id="d3390-146">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d3390-146">OUTPUTS</span></span>

### <span data-ttu-id="d3390-147">Microsoft. Azure. PowerShell. Cmdlets. Kusto. Models. Api20200614. IDatabasePrincipalAssignment</span><span class="sxs-lookup"><span data-stu-id="d3390-147">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IDatabasePrincipalAssignment</span></span>

## <span data-ttu-id="d3390-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="d3390-148">NOTES</span></span>

<span data-ttu-id="d3390-149">Aliase</span><span class="sxs-lookup"><span data-stu-id="d3390-149">ALIASES</span></span>

## <span data-ttu-id="d3390-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d3390-150">RELATED LINKS</span></span>

