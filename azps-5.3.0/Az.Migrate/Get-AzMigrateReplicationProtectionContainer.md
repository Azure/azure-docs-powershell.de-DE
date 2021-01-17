---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: a89d762f0317075a0da94290ad964aeef133fdd5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459064"
---
# <span data-ttu-id="4cfac-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4cfac-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="4cfac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4cfac-102">SYNOPSIS</span></span>
<span data-ttu-id="4cfac-103">Ruft die Details eines Schutzcontainers ab.</span><span class="sxs-lookup"><span data-stu-id="4cfac-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="4cfac-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4cfac-104">SYNTAX</span></span>

### <span data-ttu-id="4cfac-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="4cfac-105">List (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="4cfac-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="4cfac-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="4cfac-107">Liste1</span><span class="sxs-lookup"><span data-stu-id="4cfac-107">List1</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="4cfac-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4cfac-108">DESCRIPTION</span></span>
<span data-ttu-id="4cfac-109">Ruft die Details eines Schutzcontainers ab.</span><span class="sxs-lookup"><span data-stu-id="4cfac-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="4cfac-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4cfac-110">EXAMPLES</span></span>

### <span data-ttu-id="4cfac-111">Example 1: List all protection containers in vault and fabric</span><span class="sxs-lookup"><span data-stu-id="4cfac-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="4cfac-112">Listet alle auf.</span><span class="sxs-lookup"><span data-stu-id="4cfac-112">Lists all.</span></span>

### <span data-ttu-id="4cfac-113">Beispiel 2: Erhalten eines bestimmten Containers</span><span class="sxs-lookup"><span data-stu-id="4cfac-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="4cfac-114">Ruft einen bestimmten ab.</span><span class="sxs-lookup"><span data-stu-id="4cfac-114">Gets a specific one.</span></span>

## <span data-ttu-id="4cfac-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4cfac-115">PARAMETERS</span></span>

### <span data-ttu-id="4cfac-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4cfac-116">-DefaultProfile</span></span>
<span data-ttu-id="4cfac-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4cfac-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4cfac-118">-FabricName</span><span class="sxs-lookup"><span data-stu-id="4cfac-118">-FabricName</span></span>
<span data-ttu-id="4cfac-119">Fabric name.</span><span class="sxs-lookup"><span data-stu-id="4cfac-119">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List1
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cfac-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="4cfac-120">-ProtectionContainerName</span></span>
<span data-ttu-id="4cfac-121">Name des Schutzcontainers.</span><span class="sxs-lookup"><span data-stu-id="4cfac-121">Protection container name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4cfac-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4cfac-122">-ResourceGroupName</span></span>
<span data-ttu-id="4cfac-123">Der Name der Ressourcengruppe, in der sich der Tresor der Wiederherstellungsdienste befindet.</span><span class="sxs-lookup"><span data-stu-id="4cfac-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="4cfac-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="4cfac-124">-ResourceName</span></span>
<span data-ttu-id="4cfac-125">Der Name des Tresors der Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="4cfac-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="4cfac-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4cfac-126">-SubscriptionId</span></span>
<span data-ttu-id="4cfac-127">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="4cfac-127">The subscription Id.</span></span>

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

### <span data-ttu-id="4cfac-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4cfac-128">CommonParameters</span></span>
<span data-ttu-id="4cfac-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4cfac-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4cfac-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4cfac-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4cfac-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4cfac-131">INPUTS</span></span>

## <span data-ttu-id="4cfac-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4cfac-132">OUTPUTS</span></span>

### <span data-ttu-id="4cfac-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="4cfac-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="4cfac-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4cfac-134">NOTES</span></span>

<span data-ttu-id="4cfac-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="4cfac-135">ALIASES</span></span>

## <span data-ttu-id="4cfac-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4cfac-136">RELATED LINKS</span></span>

