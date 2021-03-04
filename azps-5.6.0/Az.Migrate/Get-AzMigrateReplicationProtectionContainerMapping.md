---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: 87fa8d8653d0409eb4b322e0ce21dbc9c8cfa668
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934035"
---
# <span data-ttu-id="969f6-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="969f6-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="969f6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="969f6-102">SYNOPSIS</span></span>
<span data-ttu-id="969f6-103">Ruft die Details einer Schutzcontainerzuordnung ab.</span><span class="sxs-lookup"><span data-stu-id="969f6-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="969f6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="969f6-104">SYNTAX</span></span>

### <span data-ttu-id="969f6-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="969f6-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="969f6-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="969f6-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="969f6-107">Liste</span><span class="sxs-lookup"><span data-stu-id="969f6-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="969f6-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="969f6-108">DESCRIPTION</span></span>
<span data-ttu-id="969f6-109">Ruft die Details einer Schutzcontainerzuordnung ab.</span><span class="sxs-lookup"><span data-stu-id="969f6-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="969f6-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="969f6-110">EXAMPLES</span></span>

### <span data-ttu-id="969f6-111">Beispiel 1: Erhalten einer bestimmten Zuordnung</span><span class="sxs-lookup"><span data-stu-id="969f6-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="969f6-112">Erhalten Sie ein Zuordnungsdetail.</span><span class="sxs-lookup"><span data-stu-id="969f6-112">Get a mapping detail.</span></span>

## <span data-ttu-id="969f6-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="969f6-113">PARAMETERS</span></span>

### <span data-ttu-id="969f6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="969f6-114">-DefaultProfile</span></span>
<span data-ttu-id="969f6-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="969f6-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="969f6-116">-FabricName</span><span class="sxs-lookup"><span data-stu-id="969f6-116">-FabricName</span></span>
<span data-ttu-id="969f6-117">Fabricname.</span><span class="sxs-lookup"><span data-stu-id="969f6-117">Fabric name.</span></span>

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

### <span data-ttu-id="969f6-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="969f6-118">-MappingName</span></span>
<span data-ttu-id="969f6-119">Name der Schutzcontainerzuordnung.</span><span class="sxs-lookup"><span data-stu-id="969f6-119">Protection Container mapping name.</span></span>

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

### <span data-ttu-id="969f6-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="969f6-120">-ProtectionContainerName</span></span>
<span data-ttu-id="969f6-121">Name des Schutzcontainers.</span><span class="sxs-lookup"><span data-stu-id="969f6-121">Protection container name.</span></span>

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

### <span data-ttu-id="969f6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="969f6-122">-ResourceGroupName</span></span>
<span data-ttu-id="969f6-123">Der Name der Ressourcengruppe, in der sich der Wiederherstellungsdiensttresor befindet.</span><span class="sxs-lookup"><span data-stu-id="969f6-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="969f6-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="969f6-124">-ResourceName</span></span>
<span data-ttu-id="969f6-125">Der Name des Wiederherstellungsdienste-Tresors.</span><span class="sxs-lookup"><span data-stu-id="969f6-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="969f6-126">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="969f6-126">-SubscriptionId</span></span>
<span data-ttu-id="969f6-127">Azure-Abonnement-ID, in der das Projekt migriert wurde.</span><span class="sxs-lookup"><span data-stu-id="969f6-127">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="969f6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="969f6-128">CommonParameters</span></span>
<span data-ttu-id="969f6-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="969f6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="969f6-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="969f6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="969f6-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="969f6-131">INPUTS</span></span>

## <span data-ttu-id="969f6-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="969f6-132">OUTPUTS</span></span>

### <span data-ttu-id="969f6-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="969f6-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="969f6-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="969f6-134">NOTES</span></span>

<span data-ttu-id="969f6-135">ALIASE</span><span class="sxs-lookup"><span data-stu-id="969f6-135">ALIASES</span></span>

## <span data-ttu-id="969f6-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="969f6-136">RELATED LINKS</span></span>

