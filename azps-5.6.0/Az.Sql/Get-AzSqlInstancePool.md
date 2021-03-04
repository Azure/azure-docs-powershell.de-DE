---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/get-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
ms.openlocfilehash: 524d9ff479355f511b9039e1ea64a8234e37e021
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943331"
---
# <span data-ttu-id="2a7ab-101">Get-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="2a7ab-101">Get-AzSqlInstancePool</span></span>

## <span data-ttu-id="2a7ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a7ab-102">SYNOPSIS</span></span>
<span data-ttu-id="2a7ab-103">Gibt Informationen zum Azure SQL-Instanzpool zurück.</span><span class="sxs-lookup"><span data-stu-id="2a7ab-103">Returns information about the Azure SQL Instance pool.</span></span>

## <span data-ttu-id="2a7ab-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="2a7ab-104">SYNTAX</span></span>

### <span data-ttu-id="2a7ab-105">ListBySubOrResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="2a7ab-105">ListBySubOrResourceGroupParameterSet (Default)</span></span>
```
Get-AzSqlInstancePool [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a7ab-106">ListByInstancePoolDefaultsParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a7ab-106">ListByInstancePoolDefaultsParameterSet</span></span>
```
Get-AzSqlInstancePool -ResourceGroupName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2a7ab-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="2a7ab-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2a7ab-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="2a7ab-108">DESCRIPTION</span></span>
<span data-ttu-id="2a7ab-109">Das **Get-AzSqlInstancePool-Cmdlet** gibt Informationen zu einem oder mehreren Azure SQL Instanzpool zurück.</span><span class="sxs-lookup"><span data-stu-id="2a7ab-109">The **Get-AzSqlInstancePool** cmdlet returns information about one or more Azure SQL Instance pool.</span></span>
<span data-ttu-id="2a7ab-110">Geben Sie den Namen eines Instanzpools an, um Informationen nur für diesen Instanzpool zu sehen.</span><span class="sxs-lookup"><span data-stu-id="2a7ab-110">Specify the name of an instance pool to see information for only that instance pool.</span></span>

## <span data-ttu-id="2a7ab-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="2a7ab-111">EXAMPLES</span></span>

### <span data-ttu-id="2a7ab-112">Beispiel 1: Alle Instanzpools für ein Kundenabonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="2a7ab-112">Example 1: Get all instance pools across a customer subscription</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded

ResourceGroupName : resourcegroup02
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Sql/instancePools/ps-instancepool-1
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup02/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="2a7ab-113">Dieser Befehl ruft Informationen zu allen Instanzpools innerhalb des Kundenabonnements ab.</span><span class="sxs-lookup"><span data-stu-id="2a7ab-113">This command gets information about all instance pools within the customer subscription.</span></span>

### <span data-ttu-id="2a7ab-114">Beispiel 2: Alle Instanzpools über eine Ressourcengruppe hinweg erhalten</span><span class="sxs-lookup"><span data-stu-id="2a7ab-114">Example 2: Get all instance pools across a resource group</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="2a7ab-115">Dieser Befehl ruft Informationen zu allen Instanzpools innerhalb der Ressourcengruppenressourcengruppe01 ab.</span><span class="sxs-lookup"><span data-stu-id="2a7ab-115">This command gets information about all instance pools within the resource group resourcegroup01.</span></span>

### <span data-ttu-id="2a7ab-116">Beispiel 3: Informationen zu einem Instanzpool erhalten</span><span class="sxs-lookup"><span data-stu-id="2a7ab-116">Example 3: Get information about an instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancePool0
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="2a7ab-117">Dieser Befehl ruft Informationen zur Instanzpoolinstanzpool0 ab.</span><span class="sxs-lookup"><span data-stu-id="2a7ab-117">This command gets information about the instance pool instancePool0.</span></span>

### <span data-ttu-id="2a7ab-118">Beispiel 4: Informationen zu einem Instanzpool mithilfe der Ressourcen-ID des Instanzpools</span><span class="sxs-lookup"><span data-stu-id="2a7ab-118">Example 4: Get information about an instance pool using instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePool -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"
ResourceGroupName : resourcegroup01
Type              : Microsoft.Sql/instancePools
Id                : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0
InstancePoolName  : instancePool0
SubnetId          : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Network/virtualNetworks/vnet_name/subnets/subnet_name
VCores            : 8
ComputeGeneration : Gen5
Edition           : GeneralPurpose
Tags              :
Sku               : Microsoft.Azure.Management.Sql.Models.Sku
Location          : canadacentral
LicenseType       : LicenseIncluded
```

<span data-ttu-id="2a7ab-119">Dieser Befehl ruft Informationen zum Instanzpool mit seinem Ressourcenbezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="2a7ab-119">This command gets information about the instance pool with its resource identifier.</span></span>

## <span data-ttu-id="2a7ab-120">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="2a7ab-120">PARAMETERS</span></span>

### <span data-ttu-id="2a7ab-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a7ab-121">-DefaultProfile</span></span>
<span data-ttu-id="2a7ab-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a7ab-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a7ab-123">-Name</span><span class="sxs-lookup"><span data-stu-id="2a7ab-123">-Name</span></span>
<span data-ttu-id="2a7ab-124">Der Name des Instanzpools.</span><span class="sxs-lookup"><span data-stu-id="2a7ab-124">The instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a7ab-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a7ab-125">-ResourceGroupName</span></span>
<span data-ttu-id="2a7ab-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2a7ab-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListBySubOrResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ListByInstancePoolDefaultsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2a7ab-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2a7ab-127">-ResourceId</span></span>
<span data-ttu-id="2a7ab-128">Der Ressourcenbezeichner des Instanzpools.</span><span class="sxs-lookup"><span data-stu-id="2a7ab-128">The instance pool resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: GetInstancePoolByInstancePoolResourceIdentifierParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a7ab-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a7ab-129">CommonParameters</span></span>
<span data-ttu-id="2a7ab-130">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a7ab-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a7ab-131">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a7ab-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a7ab-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="2a7ab-132">INPUTS</span></span>

### <span data-ttu-id="2a7ab-133">Keine</span><span class="sxs-lookup"><span data-stu-id="2a7ab-133">None</span></span>

## <span data-ttu-id="2a7ab-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="2a7ab-134">OUTPUTS</span></span>

### <span data-ttu-id="2a7ab-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="2a7ab-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

## <span data-ttu-id="2a7ab-136">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="2a7ab-136">NOTES</span></span>

## <span data-ttu-id="2a7ab-137">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="2a7ab-137">RELATED LINKS</span></span>
