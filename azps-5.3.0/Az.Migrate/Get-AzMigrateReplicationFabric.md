---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 8230056069668765d3d27a9dd54538a310edf383
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98467591"
---
# <span data-ttu-id="3f5cc-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="3f5cc-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="3f5cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3f5cc-102">SYNOPSIS</span></span>
<span data-ttu-id="3f5cc-103">Ruft die Details eines Azure Site Recovery Fabric ab.</span><span class="sxs-lookup"><span data-stu-id="3f5cc-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="3f5cc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="3f5cc-104">SYNTAX</span></span>

### <span data-ttu-id="3f5cc-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="3f5cc-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="3f5cc-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="3f5cc-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="3f5cc-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3f5cc-107">DESCRIPTION</span></span>
<span data-ttu-id="3f5cc-108">Ruft die Details eines Azure Site Recovery Fabric ab.</span><span class="sxs-lookup"><span data-stu-id="3f5cc-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="3f5cc-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="3f5cc-109">EXAMPLES</span></span>

### <span data-ttu-id="3f5cc-110">Beispiel 1: Alle Ressourcen nach Ressourcengruppe und Tresorname erhalten</span><span class="sxs-lookup"><span data-stu-id="3f5cc-110">Example 1: Get all fabrics by resource group and vault name</span></span>
```powershell
PS C:\> PS Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault -FabricName AzMigratePWSHTc8d1replicationfabric

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="3f5cc-111">Alles in Ressourcengruppe und Tresor</span><span class="sxs-lookup"><span data-stu-id="3f5cc-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="3f5cc-112">Example 2: Get fabric by resource group, vault name and fabric name</span><span class="sxs-lookup"><span data-stu-id="3f5cc-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
```powershell
PS C:\> Get-AzMigrateReplicationFabric -ResourceGroupName azmigratepwshtestasr13072020 -ResourceName AzMigrateTestProjectPWSH02aarsvault

BcdrState                                 : Valid
CustomDetailInstanceType                  : VMwareV2
EncryptionDetailKekCertExpiryDate         :
EncryptionDetailKekCertThumbprint         :
EncryptionDetailKekState                  : None
FriendlyName                              : AzMigratePWSHTc8d1replicationfabric
Health                                    : Normal
HealthErrorDetail                         : {}
Id                                        : /Subscriptions/xxx-xxx-xxx/resourceGroups/azmigratepwshtestasr13072020/providers/Microsof
                                            t.RecoveryServices/vaults/AzMigrateTestProjectPWSH02aarsvault/replicationFabrics/AzMigratePWSHTc8d1replicationfabr
                                            ic
InternalIdentifier                        : 501ff8f2-c9d7-5bf4-87ff-d0b3fc98aeb5
Location                                  :
Name                                      : AzMigratePWSHTc8d1replicationfabric
RolloverEncryptionDetailKekCertExpiryDate :
RolloverEncryptionDetailKekCertThumbprint :
RolloverEncryptionDetailKekState          : None
Type                                      : Microsoft.RecoveryServices/vaults/replicationFabrics
```

<span data-ttu-id="3f5cc-113">Get a specific fabric</span><span class="sxs-lookup"><span data-stu-id="3f5cc-113">Get a specific fabric</span></span>

## <span data-ttu-id="3f5cc-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3f5cc-114">PARAMETERS</span></span>

### <span data-ttu-id="3f5cc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3f5cc-115">-DefaultProfile</span></span>
<span data-ttu-id="3f5cc-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3f5cc-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3f5cc-117">-FabricName</span><span class="sxs-lookup"><span data-stu-id="3f5cc-117">-FabricName</span></span>
<span data-ttu-id="3f5cc-118">Fabric name.</span><span class="sxs-lookup"><span data-stu-id="3f5cc-118">Fabric name.</span></span>

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

### <span data-ttu-id="3f5cc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3f5cc-119">-ResourceGroupName</span></span>
<span data-ttu-id="3f5cc-120">Der Name der Ressourcengruppe, in der sich der Tresor der Wiederherstellungsdienste befindet.</span><span class="sxs-lookup"><span data-stu-id="3f5cc-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="3f5cc-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="3f5cc-121">-ResourceName</span></span>
<span data-ttu-id="3f5cc-122">Der Name des Tresors der Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="3f5cc-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="3f5cc-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3f5cc-123">-SubscriptionId</span></span>
<span data-ttu-id="3f5cc-124">Die Abonnement-ID.</span><span class="sxs-lookup"><span data-stu-id="3f5cc-124">The subscription Id.</span></span>

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

### <span data-ttu-id="3f5cc-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f5cc-125">CommonParameters</span></span>
<span data-ttu-id="3f5cc-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f5cc-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f5cc-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3f5cc-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f5cc-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="3f5cc-128">INPUTS</span></span>

## <span data-ttu-id="3f5cc-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="3f5cc-129">OUTPUTS</span></span>

### <span data-ttu-id="3f5cc-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span><span class="sxs-lookup"><span data-stu-id="3f5cc-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="3f5cc-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="3f5cc-131">NOTES</span></span>

<span data-ttu-id="3f5cc-132">ALIASE</span><span class="sxs-lookup"><span data-stu-id="3f5cc-132">ALIASES</span></span>

## <span data-ttu-id="3f5cc-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="3f5cc-133">RELATED LINKS</span></span>

