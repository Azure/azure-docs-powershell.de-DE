---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationprotectioncontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationProtectionContainer.md
ms.openlocfilehash: a89d762f0317075a0da94290ad964aeef133fdd5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94180273"
---
# <span data-ttu-id="7a270-101">Get-AzMigrateReplicationProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7a270-101">Get-AzMigrateReplicationProtectionContainer</span></span>

## <span data-ttu-id="7a270-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7a270-102">SYNOPSIS</span></span>
<span data-ttu-id="7a270-103">Ruft die Details eines Schutz Containers ab.</span><span class="sxs-lookup"><span data-stu-id="7a270-103">Gets the details of a protection container.</span></span>

## <span data-ttu-id="7a270-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a270-104">SYNTAX</span></span>

### <span data-ttu-id="7a270-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="7a270-105">List (Default)</span></span>
```
Get-AzMigrateReplicationProtectionContainer -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="7a270-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="7a270-106">Get</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ProtectionContainerName <String>
 -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a270-107">List1</span><span class="sxs-lookup"><span data-stu-id="7a270-107">List1</span></span>
```
Get-AzMigrateReplicationProtectionContainer -FabricName <String> -ResourceGroupName <String>
 -ResourceName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="7a270-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7a270-108">DESCRIPTION</span></span>
<span data-ttu-id="7a270-109">Ruft die Details eines Schutz Containers ab.</span><span class="sxs-lookup"><span data-stu-id="7a270-109">Gets the details of a protection container.</span></span>

## <span data-ttu-id="7a270-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7a270-110">EXAMPLES</span></span>

### <span data-ttu-id="7a270-111">Beispiel 1: Auflisten aller Schutzcontainer in Vault und Fabric</span><span class="sxs-lookup"><span data-stu-id="7a270-111">Example 1: List all protection containers in vault and fabric</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="7a270-112">Listet alle auf.</span><span class="sxs-lookup"><span data-stu-id="7a270-112">Lists all.</span></span>

### <span data-ttu-id="7a270-113">Beispiel 2: Abrufen eines bestimmten Containers</span><span class="sxs-lookup"><span data-stu-id="7a270-113">Example 2: Get a specific container</span></span>
```powershell
PS C:\> PS /src/Migrate [Az.Migrate]> Get-AzMigrateReplicationProtectionContainer -ResourceGroupName azmigratepwshtestasr13072020  -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric -ProtectionContainerName AzMigratePWSHTc8d1replicationcontainer

Location Name                                   Type
-------- ----                                   ----
         AzMigratePWSHTc8d1replicationcontainer Microsoft.RecoveryServices/vaults/replicationFabrics/replicationProtectionContainers
```

<span data-ttu-id="7a270-114">Ruft eine bestimmte ab.</span><span class="sxs-lookup"><span data-stu-id="7a270-114">Gets a specific one.</span></span>

## <span data-ttu-id="7a270-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a270-115">PARAMETERS</span></span>

### <span data-ttu-id="7a270-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a270-116">-DefaultProfile</span></span>
<span data-ttu-id="7a270-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7a270-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a270-118">-Fabricname</span><span class="sxs-lookup"><span data-stu-id="7a270-118">-FabricName</span></span>
<span data-ttu-id="7a270-119">Name des Stoffs.</span><span class="sxs-lookup"><span data-stu-id="7a270-119">Fabric name.</span></span>

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

### <span data-ttu-id="7a270-120">-ProtectionContainerName</span><span class="sxs-lookup"><span data-stu-id="7a270-120">-ProtectionContainerName</span></span>
<span data-ttu-id="7a270-121">Name des Schutz Containers.</span><span class="sxs-lookup"><span data-stu-id="7a270-121">Protection container name.</span></span>

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

### <span data-ttu-id="7a270-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a270-122">-ResourceGroupName</span></span>
<span data-ttu-id="7a270-123">Der Name der Ressourcengruppe, in der der Vault für Wiederherstellungsdienste vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7a270-123">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="7a270-124">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="7a270-124">-ResourceName</span></span>
<span data-ttu-id="7a270-125">Der Name des Speichers für Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="7a270-125">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="7a270-126">-Abonnement-Nr</span><span class="sxs-lookup"><span data-stu-id="7a270-126">-SubscriptionId</span></span>
<span data-ttu-id="7a270-127">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="7a270-127">The subscription Id.</span></span>

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

### <span data-ttu-id="7a270-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a270-128">CommonParameters</span></span>
<span data-ttu-id="7a270-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a270-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a270-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a270-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a270-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7a270-131">INPUTS</span></span>

## <span data-ttu-id="7a270-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7a270-132">OUTPUTS</span></span>

### <span data-ttu-id="7a270-133">Microsoft. Azure. PowerShell. Cmdlets. migrate. Models. Api20180110. IProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7a270-133">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IProtectionContainer</span></span>

## <span data-ttu-id="7a270-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="7a270-134">NOTES</span></span>

<span data-ttu-id="7a270-135">Aliase</span><span class="sxs-lookup"><span data-stu-id="7a270-135">ALIASES</span></span>

## <span data-ttu-id="7a270-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7a270-136">RELATED LINKS</span></span>

