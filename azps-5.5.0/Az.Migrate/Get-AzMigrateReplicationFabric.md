---
external help file: ''
Module Name: Az.Migrate
online version: https://docs.microsoft.com/en-us/powershell/module/az.migrate/get-azmigratereplicationfabric
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Migrate/help/Get-AzMigrateReplicationFabric.md
ms.openlocfilehash: 6872eb3da4f67969dcb6ec57a9e300677bd4611b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157417"
---
# <span data-ttu-id="b742d-101">Get-AzMigrateReplicationFabric</span><span class="sxs-lookup"><span data-stu-id="b742d-101">Get-AzMigrateReplicationFabric</span></span>

## <span data-ttu-id="b742d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b742d-102">SYNOPSIS</span></span>
<span data-ttu-id="b742d-103">Ruft die Details eines Azure Site Recovery Fabric ab.</span><span class="sxs-lookup"><span data-stu-id="b742d-103">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="b742d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b742d-104">SYNTAX</span></span>

### <span data-ttu-id="b742d-105">Liste (Standard)</span><span class="sxs-lookup"><span data-stu-id="b742d-105">List (Default)</span></span>
```
Get-AzMigrateReplicationFabric -ResourceGroupName <String> -ResourceName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="b742d-106">Erhalten</span><span class="sxs-lookup"><span data-stu-id="b742d-106">Get</span></span>
```
Get-AzMigrateReplicationFabric -FabricName <String> -ResourceGroupName <String> -ResourceName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="b742d-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b742d-107">DESCRIPTION</span></span>
<span data-ttu-id="b742d-108">Ruft die Details eines Azure Site Recovery Fabric ab.</span><span class="sxs-lookup"><span data-stu-id="b742d-108">Gets the details of an Azure Site Recovery fabric.</span></span>

## <span data-ttu-id="b742d-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b742d-109">EXAMPLES</span></span>

### <span data-ttu-id="b742d-110">Beispiel 1: Alle Ressourcen nach Ressourcengruppe und Tresornamen erhalten</span><span class="sxs-lookup"><span data-stu-id="b742d-110">Example 1: Get all fabrics by resource group and vault name</span></span>
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

<span data-ttu-id="b742d-111">Alles in Ressourcengruppe und Tresor</span><span class="sxs-lookup"><span data-stu-id="b742d-111">Get all fabrics in resource group and vault</span></span>

### <span data-ttu-id="b742d-112">Example 2: Get fabric by resource group, vault name and fabric name</span><span class="sxs-lookup"><span data-stu-id="b742d-112">Example 2: Get fabric by resource group, vault name and fabric name</span></span>
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

<span data-ttu-id="b742d-113">Get a specific fabric</span><span class="sxs-lookup"><span data-stu-id="b742d-113">Get a specific fabric</span></span>

## <span data-ttu-id="b742d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b742d-114">PARAMETERS</span></span>

### <span data-ttu-id="b742d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b742d-115">-DefaultProfile</span></span>
<span data-ttu-id="b742d-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b742d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b742d-117">-FabricName</span><span class="sxs-lookup"><span data-stu-id="b742d-117">-FabricName</span></span>
<span data-ttu-id="b742d-118">Fabric name.</span><span class="sxs-lookup"><span data-stu-id="b742d-118">Fabric name.</span></span>

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

### <span data-ttu-id="b742d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b742d-119">-ResourceGroupName</span></span>
<span data-ttu-id="b742d-120">Der Name der Ressourcengruppe, in der sich der Tresor der Wiederherstellungsdienste befindet.</span><span class="sxs-lookup"><span data-stu-id="b742d-120">The name of the resource group where the recovery services vault is present.</span></span>

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

### <span data-ttu-id="b742d-121">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="b742d-121">-ResourceName</span></span>
<span data-ttu-id="b742d-122">Der Name des Tresors der Wiederherstellungsdienste.</span><span class="sxs-lookup"><span data-stu-id="b742d-122">The name of the recovery services vault.</span></span>

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

### <span data-ttu-id="b742d-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="b742d-123">-SubscriptionId</span></span>
<span data-ttu-id="b742d-124">Azure-Abonnement-ID, in der das Projekt migriert wurde.</span><span class="sxs-lookup"><span data-stu-id="b742d-124">Azure Subscription Id in which migrate project was created.</span></span>

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

### <span data-ttu-id="b742d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b742d-125">CommonParameters</span></span>
<span data-ttu-id="b742d-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b742d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b742d-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b742d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b742d-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b742d-128">INPUTS</span></span>

## <span data-ttu-id="b742d-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b742d-129">OUTPUTS</span></span>

### <span data-ttu-id="b742d-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span><span class="sxs-lookup"><span data-stu-id="b742d-130">Microsoft.Azure.PowerShell.Cmdlets.Migrate.Models.Api20180110.IFabric</span></span>

## <span data-ttu-id="b742d-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b742d-131">NOTES</span></span>

<span data-ttu-id="b742d-132">ALIASE</span><span class="sxs-lookup"><span data-stu-id="b742d-132">ALIASES</span></span>

## <span data-ttu-id="b742d-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b742d-133">RELATED LINKS</span></span>

