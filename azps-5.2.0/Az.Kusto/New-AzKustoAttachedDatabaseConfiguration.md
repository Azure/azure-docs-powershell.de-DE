---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/new-azkustoattacheddatabaseconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/New-AzKustoAttachedDatabaseConfiguration.md
ms.openlocfilehash: 26da7e8b0bf3ca24edd9f4abd52f0c27aabf49e8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356907"
---
# <span data-ttu-id="4e5f7-101">New-AzKustoAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e5f7-101">New-AzKustoAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="4e5f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e5f7-102">SYNOPSIS</span></span>
<span data-ttu-id="4e5f7-103">Erstellt oder aktualisiert eine angefügte Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4e5f7-103">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="4e5f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4e5f7-104">SYNTAX</span></span>

```
New-AzKustoAttachedDatabaseConfiguration -ClusterName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-ClusterResourceId <String>] [-DatabaseName <String>]
 [-DefaultPrincipalsModificationKind <DefaultPrincipalsModificationKind>] [-Location <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4e5f7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4e5f7-105">DESCRIPTION</span></span>
<span data-ttu-id="4e5f7-106">Erstellt oder aktualisiert eine angefügte Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4e5f7-106">Creates or updates an attached database configuration.</span></span>

## <span data-ttu-id="4e5f7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4e5f7-107">EXAMPLES</span></span>

### <span data-ttu-id="4e5f7-108">Beispiel 1: Erstellen einer neuen AttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e5f7-108">Example 1: Create a new AttachedDatabaseConfiguration</span></span>
```powershell
PS C:\> New-AzKustoAttachedDatabaseConfiguration -ResourceGroupName "testrg" -ClusterName "testnewkustoclusterf" -Name "myfollowerconfiguration" -Location "East US" -ClusterResourceId "/subscriptions/$subscriptionId/resourcegroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustocluster" -DatabaseName "mykustodatabase" -DefaultPrincipalsModificationKind "Union"

Name                                 Type                                                    Location
----                                 ----                                                    --------
testnewkustoclusterf/myfollowerconfiguration Microsoft.Kusto/Clusters/AttachedDatabaseConfigurations East US
```

<span data-ttu-id="4e5f7-109">Mit dem oben angegebenen Befehl wird eine ReadOnly-Datenbank "mykustodatabase" im Cluster "testnewkustoclusterf" erstellt.</span><span class="sxs-lookup"><span data-stu-id="4e5f7-109">The above command creates a ReadOnly database "mykustodatabase" in cluster "testnewkustoclusterf".</span></span>
<span data-ttu-id="4e5f7-110">Sie folgt der Datenbank "mykustodatabase" aus dem Cluster "testnewkustocluster".</span><span class="sxs-lookup"><span data-stu-id="4e5f7-110">It follows the database "mykustodatabase" from cluster "testnewkustocluster"</span></span>

## <span data-ttu-id="4e5f7-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4e5f7-111">PARAMETERS</span></span>

### <span data-ttu-id="4e5f7-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4e5f7-112">-AsJob</span></span>
<span data-ttu-id="4e5f7-113">Ausführen des Befehls als Auftrag</span><span class="sxs-lookup"><span data-stu-id="4e5f7-113">Run the command as a job</span></span>

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

### <span data-ttu-id="4e5f7-114">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="4e5f7-114">-ClusterName</span></span>
<span data-ttu-id="4e5f7-115">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="4e5f7-115">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="4e5f7-116">-ClusterResourceId</span><span class="sxs-lookup"><span data-stu-id="4e5f7-116">-ClusterResourceId</span></span>
<span data-ttu-id="4e5f7-117">Die Ressourcen-ID des Clusters, in dem sich die Datenbanken befinden, die Sie anfügen möchten.</span><span class="sxs-lookup"><span data-stu-id="4e5f7-117">The resource id of the cluster where the databases you would like to attach reside.</span></span>

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

### <span data-ttu-id="4e5f7-118">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4e5f7-118">-DatabaseName</span></span>
<span data-ttu-id="4e5f7-119">Der Name der Datenbank, die Sie anfügen möchten, verwenden Sie \*, wenn Sie allen aktuellen und zukünftigen Datenbanken folgen möchten.</span><span class="sxs-lookup"><span data-stu-id="4e5f7-119">The name of the database which you would like to attach, use \* if you want to follow all current and future databases.</span></span>

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

### <span data-ttu-id="4e5f7-120">-DefaultPrincipalsModificationKind</span><span class="sxs-lookup"><span data-stu-id="4e5f7-120">-DefaultPrincipalsModificationKind</span></span>
<span data-ttu-id="4e5f7-121">Änderungs art der Standardprinzipaleinstellungen</span><span class="sxs-lookup"><span data-stu-id="4e5f7-121">The default principals modification kind</span></span>

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

### <span data-ttu-id="4e5f7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e5f7-122">-DefaultProfile</span></span>
<span data-ttu-id="4e5f7-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4e5f7-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e5f7-124">-Location</span><span class="sxs-lookup"><span data-stu-id="4e5f7-124">-Location</span></span>
<span data-ttu-id="4e5f7-125">Ressourcenspeicherort.</span><span class="sxs-lookup"><span data-stu-id="4e5f7-125">Resource location.</span></span>

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

### <span data-ttu-id="4e5f7-126">-Name</span><span class="sxs-lookup"><span data-stu-id="4e5f7-126">-Name</span></span>
<span data-ttu-id="4e5f7-127">Der Name der angefügten Datenbankkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="4e5f7-127">The name of the attached database configuration.</span></span>

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

### <span data-ttu-id="4e5f7-128">-NoWait</span><span class="sxs-lookup"><span data-stu-id="4e5f7-128">-NoWait</span></span>
<span data-ttu-id="4e5f7-129">Asynchrones Ausführen des Befehls</span><span class="sxs-lookup"><span data-stu-id="4e5f7-129">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4e5f7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e5f7-130">-ResourceGroupName</span></span>
<span data-ttu-id="4e5f7-131">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="4e5f7-131">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="4e5f7-132">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4e5f7-132">-SubscriptionId</span></span>
<span data-ttu-id="4e5f7-133">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="4e5f7-133">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="4e5f7-134">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="4e5f7-134">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4e5f7-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4e5f7-135">-Confirm</span></span>
<span data-ttu-id="4e5f7-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4e5f7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e5f7-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4e5f7-137">-WhatIf</span></span>
<span data-ttu-id="4e5f7-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4e5f7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4e5f7-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4e5f7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e5f7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e5f7-140">CommonParameters</span></span>
<span data-ttu-id="4e5f7-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4e5f7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e5f7-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4e5f7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e5f7-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4e5f7-143">INPUTS</span></span>

## <span data-ttu-id="4e5f7-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4e5f7-144">OUTPUTS</span></span>

### <span data-ttu-id="4e5f7-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span><span class="sxs-lookup"><span data-stu-id="4e5f7-145">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IAttachedDatabaseConfiguration</span></span>

## <span data-ttu-id="4e5f7-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4e5f7-146">NOTES</span></span>

<span data-ttu-id="4e5f7-147">ALIASE</span><span class="sxs-lookup"><span data-stu-id="4e5f7-147">ALIASES</span></span>

## <span data-ttu-id="4e5f7-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4e5f7-148">RELATED LINKS</span></span>

