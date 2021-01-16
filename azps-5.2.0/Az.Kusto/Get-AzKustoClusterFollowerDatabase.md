---
external help file: ''
Module Name: Az.Kusto
online version: https://docs.microsoft.com/en-us/powershell/module/az.kusto/get-azkustoclusterfollowerdatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Kusto/help/Get-AzKustoClusterFollowerDatabase.md
ms.openlocfilehash: e35e0731fb14cf8ca45b6e56d3957d13ccb88398
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98293392"
---
# <span data-ttu-id="c0c6f-101">Get-AzKustoClusterFollowerDatabase</span><span class="sxs-lookup"><span data-stu-id="c0c6f-101">Get-AzKustoClusterFollowerDatabase</span></span>

## <span data-ttu-id="c0c6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0c6f-102">SYNOPSIS</span></span>
<span data-ttu-id="c0c6f-103">Gibt eine Liste von Datenbanken zurück, die sich im Besitz dieses Cluster befinden und auf die ein anderer Cluster folgt.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-103">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="c0c6f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0c6f-104">SYNTAX</span></span>

```
Get-AzKustoClusterFollowerDatabase -ClusterName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c0c6f-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0c6f-105">DESCRIPTION</span></span>
<span data-ttu-id="c0c6f-106">Gibt eine Liste von Datenbanken zurück, die sich im Besitz dieses Cluster befinden und auf die ein anderer Cluster folgt.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-106">Returns a list of databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="c0c6f-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c0c6f-107">EXAMPLES</span></span>

### <span data-ttu-id="c0c6f-108">Beispiel 1: Auflisten aller gefolgten Datenbanken</span><span class="sxs-lookup"><span data-stu-id="c0c6f-108">Example 1: List all followed databases</span></span>
```powershell
PS C:\>  Get-AzKustoClusterFollowerDatabase  -ResourceGroupName testrg -ClusterName testnewkustocluster

AttachedDatabaseConfigurationName ClusterResourceId                                                                                                                     DatabaseName
--------------------------------- -----------------                                                                                                                     ------------
myfollowerconfiguration             /subscriptions/xxxxxxxx-xxxxx-xxxx-xxxx-xxxxxxxxx/resourceGroups/testrg/providers/Microsoft.Kusto/Clusters/testnewkustoclusterf mykustodatabase
```

<span data-ttu-id="c0c6f-109">Der oben aufgeführte Befehl listet alle Datenbanken auf, die sich im Besitz dieses Cluster befinden und auf die ein anderer Cluster folgt.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-109">The above command lists all the databases that are owned by this cluster and were followed by another cluster.</span></span>

## <span data-ttu-id="c0c6f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0c6f-110">PARAMETERS</span></span>

### <span data-ttu-id="c0c6f-111">-ClusterName</span><span class="sxs-lookup"><span data-stu-id="c0c6f-111">-ClusterName</span></span>
<span data-ttu-id="c0c6f-112">Der Name des Kusto-Cluster.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-112">The name of the Kusto cluster.</span></span>

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

### <span data-ttu-id="c0c6f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0c6f-113">-DefaultProfile</span></span>
<span data-ttu-id="c0c6f-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0c6f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0c6f-115">-ResourceGroupName</span></span>
<span data-ttu-id="c0c6f-116">Der Name der Ressourcengruppe, die den Cluster "Kusto" enthält.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-116">The name of the resource group containing the Kusto cluster.</span></span>

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

### <span data-ttu-id="c0c6f-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c0c6f-117">-SubscriptionId</span></span>
<span data-ttu-id="c0c6f-118">Ruft Abonnementanmeldeinformationen ab, die das Microsoft Azure-Abonnement eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-118">Gets subscription credentials which uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="c0c6f-119">Die Abonnement-ID ist Teil des URI für jeden Dienstaufruf.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-119">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c0c6f-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0c6f-120">-Confirm</span></span>
<span data-ttu-id="c0c6f-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0c6f-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c0c6f-122">-WhatIf</span></span>
<span data-ttu-id="c0c6f-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0c6f-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0c6f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0c6f-125">CommonParameters</span></span>
<span data-ttu-id="c0c6f-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0c6f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0c6f-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0c6f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0c6f-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c0c6f-128">INPUTS</span></span>

## <span data-ttu-id="c0c6f-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c0c6f-129">OUTPUTS</span></span>

### <span data-ttu-id="c0c6f-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IFollowerDatabaseDefinition</span><span class="sxs-lookup"><span data-stu-id="c0c6f-130">Microsoft.Azure.PowerShell.Cmdlets.Kusto.Models.Api20200614.IFollowerDatabaseDefinition</span></span>

## <span data-ttu-id="c0c6f-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c0c6f-131">NOTES</span></span>

<span data-ttu-id="c0c6f-132">ALIASE</span><span class="sxs-lookup"><span data-stu-id="c0c6f-132">ALIASES</span></span>

## <span data-ttu-id="c0c6f-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c0c6f-133">RELATED LINKS</span></span>

