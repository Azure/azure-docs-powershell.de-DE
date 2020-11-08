---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainermapping
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainerMapping.md
ms.openlocfilehash: e321691106d892c703a56bd94c3fe84ab7d9fe38
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180270"
---
# <span data-ttu-id="b3c50-101">Get-AzMigrateReplicationProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b3c50-101">Get-AzMigrateReplicationProtectionContainerMapping</span></span>

## <span data-ttu-id="b3c50-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b3c50-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c50-103">Ruft die Details einer Schutzcontainer Zuordnung ab.</span><span class="sxs-lookup"><span data-stu-id="b3c50-103">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="b3c50-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3c50-104">SYNTAX</span></span>

### <span data-ttu-id="b3c50-105">List1 (Standard)</span><span class="sxs-lookup"><span data-stu-id="b3c50-105">List1 (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b3c50-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="b3c50-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -MappingName <String>
 -ProtectionContainerName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b3c50-107">Liste</span><span class="sxs-lookup"><span data-stu-id="b3c50-107">List</span></span>
```
Get-AzMigrateReplicationProtectionContainerMapping -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="b3c50-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3c50-108">DESCRIPTION</span></span>
<span data-ttu-id="b3c50-109">Ruft die Details einer Schutzcontainer Zuordnung ab.</span><span class="sxs-lookup"><span data-stu-id="b3c50-109">Gets the details of a protection container mapping.</span></span>

## <span data-ttu-id="b3c50-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3c50-110">EXAMPLES</span></span>

### <span data-ttu-id="b3c50-111">Beispiel 1: Abrufen einer bestimmten Zuordnung</span><span class="sxs-lookup"><span data-stu-id="b3c50-111">Example 1: Get a specific mapping</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationProtectionContainerMapping -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer -MappingName "containermapping"

Location Name             Type
-------- ----             ----
         containermapping Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers/replicationProtectionContainerMappings
```

<span data-ttu-id="b3c50-112">Abrufen eines Zuordnungsdetails</span><span class="sxs-lookup"><span data-stu-id="b3c50-112">Get a mapping detail.</span></span>

## <span data-ttu-id="b3c50-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3c50-113">PARAMETERS</span></span>

### <span data-ttu-id="b3c50-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c50-114">-DefaultProfile</span></span>
<span data-ttu-id="b3c50-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b3c50-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3c50-116">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="b3c50-116">-FabricName</span></span>
<span data-ttu-id="b3c50-117">Name des Stoffs.</span><span class="sxs-lookup"><span data-stu-id="b3c50-117">Fabric name.</span></span>

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

### <span data-ttu-id="b3c50-118">-MappingName</span><span class="sxs-lookup"><span data-stu-id="b3c50-118">-MappingName</span></span>
<span data-ttu-id="b3c50-119">Name des Schutz Container-Mappings</span><span class="sxs-lookup"><span data-stu-id="b3c50-119">Protection Container mapping name.</span></span>

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

### <span data-ttu-id="b3c50-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="b3c50-120">-ProtectionContainerName</span></span>
<span data-ttu-id="b3c50-121">Name des Schutz Containers.</span><span class="sxs-lookup"><span data-stu-id="b3c50-121">Protection container name.</span></span>

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

### <span data-ttu-id="b3c50-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3c50-122">-ResourceGroupName</span></span>
<span data-ttu-id="b3c50-123">Der Name der Ressourcengruppe, in der der Vault für Wiederherstellungsdienste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="b3c50-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="b3c50-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b3c50-124">-ResourceName</span></span>
<span data-ttu-id="b3c50-125">Der Name des Speichers für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="b3c50-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="b3c50-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="b3c50-126">-SubscriptionId</span></span>
<span data-ttu-id="b3c50-127">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="b3c50-127">The subscription Id.</span></span>

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

### <span data-ttu-id="b3c50-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c50-128">CommonParameters</span></span>
<span data-ttu-id="b3c50-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3c50-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c50-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3c50-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c50-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b3c50-131">INPUTS</span></span>

## <span data-ttu-id="b3c50-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b3c50-132">OUTPUTS</span></span>

### <span data-ttu-id="b3c50-133">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IProtectionContainerMapping</span><span class="sxs-lookup"><span data-stu-id="b3c50-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainerMapping</span></span>

## <span data-ttu-id="b3c50-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="b3c50-134">NOTES</span></span>

<span data-ttu-id="b3c50-135">Aliase</span><span class="sxs-lookup"><span data-stu-id="b3c50-135">ALIASES</span></span>

## <span data-ttu-id="b3c50-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b3c50-136">RELATED LINKS</span></span>

