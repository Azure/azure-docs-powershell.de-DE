---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: 5b53c9806fa541c28b7f318f464a26e9a88104e0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924872"
---
# <span data-ttu-id="e9fc4-101">Get-AzKustoClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="e9fc4-101">Get-AzKustoClusterFollowerDatabase</span></span>

## <span data-ttu-id="e9fc4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e9fc4-102">SYNOPSIS</span></span>
<span data-ttu-id="e9fc4-103">Gibt eine Liste der Datenbanken zurück, die sich im Besitz dieses Clusters befinden und auf die ein anderer Cluster gefolgt ist.</span><span class="sxs-lookup"><span data-stu-id="e9fc4-103">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="e9fc4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e9fc4-104">SYNTAX</span></span>

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e9fc4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e9fc4-105">DESCRIPTION</span></span>
<span data-ttu-id="e9fc4-106">Gibt eine Liste der Datenbanken zurück, die sich im Besitz dieses Clusters befinden und auf die ein anderer Cluster gefolgt ist.</span><span class="sxs-lookup"><span data-stu-id="e9fc4-106">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="e9fc4-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e9fc4-107">EXAMPLES</span></span>

### <span data-ttu-id="e9fc4-108">Beispiel 1: Auflisten aller gefolgten Datenbanken</span><span class="sxs-lookup"><span data-stu-id="e9fc4-108">Example 1: List all followed databases</span></span>
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

<span data-ttu-id="e9fc4-109">Der oben aufgeführte Befehl listet alle Datenbanken auf, die sich im Besitz dieses Clusters befinden und auf die ein anderer Cluster gefolgt ist.</span><span class="sxs-lookup"><span data-stu-id="e9fc4-109">The above command lists all the databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="e9fc4-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="e9fc4-110">PARAMETERS</span></span>

### <span data-ttu-id="e9fc4-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="e9fc4-111">-ClusterName</span></span>
<span data-ttu-id="e9fc4-112">Der Name des Kusto-Clusters.</span><span class="sxs-lookup"><span data-stu-id="e9fc4-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="e9fc4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9fc4-113">-DefaultProfile</span></span>
<span data-ttu-id="e9fc4-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e9fc4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e9fc4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9fc4-115">-ResourceGroupName</span></span>
<span data-ttu-id="e9fc4-116">Der Name der Ressourcengruppe, die den Kusto-Cluster enthält.</span><span class="sxs-lookup"><span data-stu-id="e9fc4-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="e9fc4-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e9fc4-117">-SubscriptionId</span></span>
<span data-ttu-id="e9fc4-118">Ruft Abonnementanmeldeinformationen ab, mit denen Microsoft Azure-Abonnement eindeutig identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e9fc4-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="e9fc4-119">Die Abonnement-ID ist Teil des URI für jeden Dienstanruf.</span><span class="sxs-lookup"><span data-stu-id="e9fc4-119">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e9fc4-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e9fc4-120">-Confirm</span></span>
<span data-ttu-id="e9fc4-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e9fc4-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9fc4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9fc4-122">-WhatIf</span></span>
<span data-ttu-id="e9fc4-123">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e9fc4-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9fc4-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e9fc4-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9fc4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9fc4-125">CommonParameters</span></span>
<span data-ttu-id="e9fc4-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9fc4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9fc4-127">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e9fc4-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9fc4-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e9fc4-128">INPUTS</span></span>

## <span data-ttu-id="e9fc4-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e9fc4-129">OUTPUTS</span></span>

### <span data-ttu-id="e9fc4-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IFollowerDatabaseDefinition</span><span class="sxs-lookup"><span data-stu-id="e9fc4-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200918.IFollowerDatabaseDefinition</span></span>

## <span data-ttu-id="e9fc4-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="e9fc4-131">NOTES</span></span>

<span data-ttu-id="e9fc4-132">ALIASE</span><span class="sxs-lookup"><span data-stu-id="e9fc4-132">ALIASES</span></span>

## <span data-ttu-id="e9fc4-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="e9fc4-133">RELATED LINKS</span></span>

