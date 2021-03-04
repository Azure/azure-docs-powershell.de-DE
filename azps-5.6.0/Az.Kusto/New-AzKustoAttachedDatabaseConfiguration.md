---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 6b540b82ed07e42a6789a2603299508c21c7c3aa
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934355"
---
# <span data-ttu-id="1b6ea-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b6ea-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="1b6ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b6ea-102">SYNOPSIS</span></span>
<span data-ttu-id="1b6ea-103">Erstellt oder aktualisiert eine angefügte Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b6ea-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="1b6ea-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b6ea-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1b6ea-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b6ea-105">DESCRIPTION</span></span>
<span data-ttu-id="1b6ea-106">Erstellt oder aktualisiert eine angefügte Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b6ea-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="1b6ea-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1b6ea-107">EXAMPLES</span></span>

### <span data-ttu-id="1b6ea-108">Beispiel 1: Erstellen einer neuen AttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b6ea-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="1b6ea-109">Mit dem obigen Befehl wird eine ReadOnly-Datenbank "mykustodatabase" im Cluster "testnewkustoclusterf" erstellt.</span><span class="sxs-lookup"><span data-stu-id="1b6ea-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="1b6ea-110">Sie folgt der Datenbank "mykustodatabase" aus dem Cluster "testnewkustocluster"</span><span class="sxs-lookup"><span data-stu-id="1b6ea-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="1b6ea-111">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1b6ea-111">PARAMETERS</span></span>

### <span data-ttu-id="1b6ea-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1b6ea-112">-AsJob</span></span>
<span data-ttu-id="1b6ea-113">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="1b6ea-113">Run the command as a job</span></span>

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

### <span data-ttu-id="1b6ea-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="1b6ea-114">-ClusterName</span></span>
<span data-ttu-id="1b6ea-115">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="1b6ea-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="1b6ea-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="1b6ea-116">-ClusterResourceId</span></span>
<span data-ttu-id="1b6ea-117">Die Ressourcen-ID des Clusters, in dem sich die Datenbanken befinden, die Sie anfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="1b6ea-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

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

### <span data-ttu-id="1b6ea-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="1b6ea-118">-DatabaseName</span></span>
<span data-ttu-id="1b6ea-119">Wenn Sie allen aktuellen und zukünftigen Datenbanken folgen möchten, verwenden Sie \* den Namen der Datenbank, die Sie anfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="1b6ea-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

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

### <span data-ttu-id="1b6ea-120">-DefaultPrincipalsModificationKind</span><span class="sxs-lookup"><span data-stu-id="1b6ea-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="1b6ea-121">Änderungs art der Standardprinzipale</span><span class="sxs-lookup"><span data-stu-id="1b6ea-121">The default principals modification kind</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Kusto.Support.DefaultPrincipalsModificationKind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6ea-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b6ea-122">-DefaultProfile</span></span>
<span data-ttu-id="1b6ea-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b6ea-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b6ea-124">-Location</span><span class="sxs-lookup"><span data-stu-id="1b6ea-124">-Location</span></span>
<span data-ttu-id="1b6ea-125">Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="1b6ea-125">Resource location.</span></span>

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

### <span data-ttu-id="1b6ea-126">-Name</span><span class="sxs-lookup"><span data-stu-id="1b6ea-126">-Name</span></span>
<span data-ttu-id="1b6ea-127">Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="1b6ea-127">The name of the attached database configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AttachedDatabaseConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b6ea-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1b6ea-128">-NoWait</span></span>
<span data-ttu-id="1b6ea-129">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="1b6ea-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1b6ea-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b6ea-130">-ResourceGroupName</span></span>
<span data-ttu-id="1b6ea-131">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="1b6ea-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="1b6ea-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1b6ea-132">-SubscriptionId</span></span>
<span data-ttu-id="1b6ea-133">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="1b6ea-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1b6ea-134">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="1b6ea-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="1b6ea-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1b6ea-135">-Confirm</span></span>
<span data-ttu-id="1b6ea-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1b6ea-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1b6ea-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1b6ea-137">-WhatIf</span></span>
<span data-ttu-id="1b6ea-138">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1b6ea-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1b6ea-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b6ea-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1b6ea-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b6ea-140">CommonParameters</span></span>
<span data-ttu-id="1b6ea-141">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b6ea-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b6ea-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1b6ea-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b6ea-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1b6ea-143">INPUTS</span></span>

## <span data-ttu-id="1b6ea-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1b6ea-144">OUTPUTS</span></span>

### <span data-ttu-id="1b6ea-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b6ea-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="1b6ea-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1b6ea-146">NOTES</span></span>

<span data-ttu-id="1b6ea-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="1b6ea-147">ALIASES</span></span>

## <span data-ttu-id="1b6ea-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1b6ea-148">RELATED LINKS</span></span>

