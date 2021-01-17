---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustodatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoDatabase.md
ms.openlocfilehash: fe976ed4e5d34e4b10fb8bba0a5e5397173417b8
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459111"
---
# <span data-ttu-id="60043-101">New-AzKustoDatabase</span><span class="sxs-lookup"><span data-stu-id="60043-101">New-AzKustoDatabase</span></span>

## <span data-ttu-id="60043-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60043-102">SYNOPSIS</span></span>
<span data-ttu-id="60043-103">Erstellt oder aktualisiert eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="60043-103">Creates or updates a database.</span></span>

## <span data-ttu-id="60043-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="60043-104">SYNTAX</span></span>

```
New-AzKustoDatabase -ClusterName <String> -Name <String> -ResourceGroupName <String> -Kind <Kind>
 [-SubscriptionId <String>] [-HotCachePeriod <TimeSpan>] [-Location <String>] [-SoftDeletePeriod <TimeSpan>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="60043-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60043-105">DESCRIPTION</span></span>
<span data-ttu-id="60043-106">Erstellt oder aktualisiert eine Datenbank.</span><span class="sxs-lookup"><span data-stu-id="60043-106">Creates or updates a database.</span></span>

## <span data-ttu-id="60043-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="60043-107">EXAMPLES</span></span>

### <span data-ttu-id="60043-108">Beispiel 1: Erstellen einer neuen "Kusto"-Datenbank nach Name</span><span class="sxs-lookup"><span data-stu-id="60043-108">Example 1: Create a new Kusto database by name</span></span>
```powershell
PS C:\> New-AzKustoDatabase -ResourceGroupName testrg -ClusterName testnewkustocluster -Name mykustodatabase -Kind ReadWrite -Location 'East US'

Kind      Location Name                                Type
----      -------- ----                                ----
ReadWrite East US  testnewkustocluster/mykustodatabase Microsoft.Kusto/Clusters/Databases
```

<span data-ttu-id="60043-109">Mit dem oben angegebenen Befehl wird eine neue "kusto"-Datenbank namens "mykustodatabase" im vorhandenen Cluster "testnewkustocluster" erstellt, der in der Ressourcengruppe "testrg" gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="60043-109">The above command creates a new Kusto database named "mykustodatabase" in the existing cluster "testnewkustocluster" found in the resource group "testrg".</span></span>

## <span data-ttu-id="60043-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="60043-110">PARAMETERS</span></span>

### <span data-ttu-id="60043-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60043-111">-AsJob</span></span>
<span data-ttu-id="60043-112">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="60043-112">Run the command as a job</span></span>

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

### <span data-ttu-id="60043-113">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="60043-113">-ClusterName</span></span>
<span data-ttu-id="60043-114">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="60043-114">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="60043-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60043-115">-DefaultProfile</span></span>
<span data-ttu-id="60043-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="60043-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="60043-117">-HotCachePeriod</span><span class="sxs-lookup"><span data-stu-id="60043-117">-HotCachePeriod</span></span>
<span data-ttu-id="60043-118">Die Zeit, zu der die Daten für schnelle Abfragen in TimeSpan im Cache gespeichert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="60043-118">The time the data should be kept in cache for fast queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60043-119">-Kind</span><span class="sxs-lookup"><span data-stu-id="60043-119">-Kind</span></span>
<span data-ttu-id="60043-120">Art der Datenbank</span><span class="sxs-lookup"><span data-stu-id="60043-120">Kind of the database</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60043-121">-Location</span><span class="sxs-lookup"><span data-stu-id="60043-121">-Location</span></span>
<span data-ttu-id="60043-122">Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="60043-122">Resource location.</span></span>

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

### <span data-ttu-id="60043-123">-Name</span><span class="sxs-lookup"><span data-stu-id="60043-123">-Name</span></span>
<span data-ttu-id="60043-124">Der Name der Datenbank im Cluster "Kusto".</span><span class="sxs-lookup"><span data-stu-id="60043-124">The name of the database in the Kusto cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DatabaseName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60043-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="60043-125">-NoWait</span></span>
<span data-ttu-id="60043-126">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="60043-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="60043-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60043-127">-ResourceGroupName</span></span>
<span data-ttu-id="60043-128">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="60043-128">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="60043-129">-SoftDeletePeriod</span><span class="sxs-lookup"><span data-stu-id="60043-129">-SoftDeletePeriod</span></span>
<span data-ttu-id="60043-130">Die Zeit, zu der die Daten gespeichert werden sollten, bevor sie für Abfragen in TimeSpan nicht mehr zugänglich sind.</span><span class="sxs-lookup"><span data-stu-id="60043-130">The time the data should be kept before it stops being accessible to queries in TimeSpan.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60043-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="60043-131">-SubscriptionId</span></span>
<span data-ttu-id="60043-132">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="60043-132">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="60043-133">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="60043-133">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="60043-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="60043-134">-Confirm</span></span>
<span data-ttu-id="60043-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="60043-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="60043-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="60043-136">-WhatIf</span></span>
<span data-ttu-id="60043-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="60043-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="60043-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="60043-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="60043-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60043-139">CommonParameters</span></span>
<span data-ttu-id="60043-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60043-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60043-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="60043-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60043-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="60043-142">INPUTS</span></span>

## <span data-ttu-id="60043-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="60043-143">OUTPUTS</span></span>

### <span data-ttu-id="60043-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span><span class="sxs-lookup"><span data-stu-id="60043-144">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IDatabase</span></span>

## <span data-ttu-id="60043-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="60043-145">NOTES</span></span>

<span data-ttu-id="60043-146">ALIASE</span><span class="sxs-lookup"><span data-stu-id="60043-146">ALIASES</span></span>

## <span data-ttu-id="60043-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="60043-147">RELATED LINKS</span></span>

