---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: 7a1cec73706d1ed799966bc3d97da06867139c33
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934043"
---
# <span data-ttu-id="23b3d-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="23b3d-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="23b3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="23b3d-103">Ruft die Details eines Schutzcontainers ab.</span><span class="sxs-lookup"><span data-stu-id="23b3d-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="23b3d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="23b3d-104">SYNTAX</span></span>

### <span data-ttu-id="23b3d-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="23b3d-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="23b3d-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="23b3d-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="23b3d-107">Liste</span><span class="sxs-lookup"><span data-stu-id="23b3d-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="23b3d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="23b3d-108">DESCRIPTION</span></span>
<span data-ttu-id="23b3d-109">Ruft die Details eines Schutzcontainers ab.</span><span class="sxs-lookup"><span data-stu-id="23b3d-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="23b3d-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="23b3d-110">EXAMPLES</span></span>

### <span data-ttu-id="23b3d-111">Beispiel 1: Auflisten aller Schutzcontainer in Tresor und Fabric</span><span class="sxs-lookup"><span data-stu-id="23b3d-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="23b3d-112">Listet alle auf.</span><span class="sxs-lookup"><span data-stu-id="23b3d-112">Lists all.</span></span>

### <span data-ttu-id="23b3d-113">Beispiel 2: Einen bestimmten Container erhalten</span><span class="sxs-lookup"><span data-stu-id="23b3d-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="23b3d-114">Ruft eine bestimmte ab.</span><span class="sxs-lookup"><span data-stu-id="23b3d-114">Gets a specific one.</span></span>

## <span data-ttu-id="23b3d-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="23b3d-115">PARAMETERS</span></span>

### <span data-ttu-id="23b3d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23b3d-116">-DefaultProfile</span></span>
<span data-ttu-id="23b3d-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23b3d-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="23b3d-118">-FabricName</span><span class="sxs-lookup"><span data-stu-id="23b3d-118">-FabricName</span></span>
<span data-ttu-id="23b3d-119">Fabricname.</span><span class="sxs-lookup"><span data-stu-id="23b3d-119">Fabric name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23b3d-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="23b3d-120">-ProtectionContainerName</span></span>
<span data-ttu-id="23b3d-121">Name des Schutzcontainers.</span><span class="sxs-lookup"><span data-stu-id="23b3d-121">Protection container name.</span></span>

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

### <span data-ttu-id="23b3d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23b3d-122">-ResourceGroupName</span></span>
<span data-ttu-id="23b3d-123">Der Name der Ressourcengruppe, in der sich der Wiederherstellungsdiensttresor befindet.</span><span class="sxs-lookup"><span data-stu-id="23b3d-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="23b3d-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="23b3d-124">-ResourceName</span></span>
<span data-ttu-id="23b3d-125">Der Name des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="23b3d-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="23b3d-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="23b3d-126">-SubscriptionId</span></span>
<span data-ttu-id="23b3d-127">Azure-Abonnement-ID, in der das Projekt migriert wurde.</span><span class="sxs-lookup"><span data-stu-id="23b3d-127">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="23b3d-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23b3d-128">CommonParameters</span></span>
<span data-ttu-id="23b3d-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23b3d-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23b3d-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23b3d-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23b3d-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="23b3d-131">INPUTS</span></span>

## <span data-ttu-id="23b3d-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="23b3d-132">OUTPUTS</span></span>

### <span data-ttu-id="23b3d-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="23b3d-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="23b3d-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="23b3d-134">NOTES</span></span>

<span data-ttu-id="23b3d-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="23b3d-135">ALIASES</span></span>

## <span data-ttu-id="23b3d-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="23b3d-136">RELATED LINKS</span></span>

