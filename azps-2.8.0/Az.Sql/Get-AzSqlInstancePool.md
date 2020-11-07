---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancepool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePool.md
ms.openlocfilehash: 8d2d1333a10290c3a321b22cf33b527738d7ecb1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825543"
---
# <span data-ttu-id="5ebc0-101">Get-AzSqlInstancePool</span><span class="sxs-lookup"><span data-stu-id="5ebc0-101">Get-AzSqlInstancePool</span></span>

## <span data-ttu-id="5ebc0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5ebc0-102">SYNOPSIS</span></span>
<span data-ttu-id="5ebc0-103">Gibt Informationen zum Azure SQL-Instanzen Pool zurück.</span><span class="sxs-lookup"><span data-stu-id="5ebc0-103">Returns information about the Azure SQL Instance pool.</span></span>

## <span data-ttu-id="5ebc0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ebc0-104">SYNTAX</span></span>

### <span data-ttu-id="5ebc0-105">ListBySubOrResourceGroupParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5ebc0-105">ListBySubOrResourceGroupParameterSet (Default)</span></span>
```
Get-AzSqlInstancePool [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ebc0-106">ListByInstancePoolDefaultsParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ebc0-106">ListByInstancePoolDefaultsParameterSet</span></span>
```
Get-AzSqlInstancePool -ResourceGroupName <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ebc0-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ebc0-107">GetInstancePoolByInstancePoolResourceIdentifierParameterSet</span></span>
```
Get-AzSqlInstancePool [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ebc0-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5ebc0-108">DESCRIPTION</span></span>
<span data-ttu-id="5ebc0-109">Das Cmdlet " **Get-AzSqlInstancePool** " gibt Informationen zu einem oder mehreren Azure SQL-Instanzen Pools zurück.</span><span class="sxs-lookup"><span data-stu-id="5ebc0-109">The **Get-AzSqlInstancePool** cmdlet returns information about one or more Azure SQL Instance pool.</span></span>
<span data-ttu-id="5ebc0-110">Geben Sie den Namen eines Instanzen Pools an, um Informationen nur für diesen Instanzen Pool anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="5ebc0-110">Specify the name of an instance pool to see information for only that instance pool.</span></span>

## <span data-ttu-id="5ebc0-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5ebc0-111">EXAMPLES</span></span>

### <span data-ttu-id="5ebc0-112">Beispiel 1: Abrufen aller Instanzen Pools in einem Kundenabonnement</span><span class="sxs-lookup"><span data-stu-id="5ebc0-112">Example 1: Get all instance pools across a customer subscription</span></span>
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

<span data-ttu-id="5ebc0-113">Dieser Befehl ruft Informationen zu allen Instanzen Pools innerhalb des Kunden Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="5ebc0-113">This command gets information about all instance pools within the customer subscription.</span></span>

### <span data-ttu-id="5ebc0-114">Beispiel 2: Abrufen aller Instanzen Pools in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="5ebc0-114">Example 2: Get all instance pools across a resource group</span></span>
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

<span data-ttu-id="5ebc0-115">Dieser Befehl ruft Informationen zu allen Instanzen Pools innerhalb der Ressourcengruppe resourcegroup01.</span><span class="sxs-lookup"><span data-stu-id="5ebc0-115">This command gets information about all instance pools within the resource group resourcegroup01.</span></span>

### <span data-ttu-id="5ebc0-116">Beispiel 3: Abrufen von Informationen zu einem Instanzen Pool</span><span class="sxs-lookup"><span data-stu-id="5ebc0-116">Example 3: Get information about an instance pool</span></span>
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

<span data-ttu-id="5ebc0-117">Dieser Befehl ruft Informationen über den Instanz Pool instancePool0.</span><span class="sxs-lookup"><span data-stu-id="5ebc0-117">This command gets information about the instance pool instancePool0.</span></span>

### <span data-ttu-id="5ebc0-118">Beispiel 4: Abrufen von Informationen zu einem Instanzen Pool mithilfe der Ressourcen-ID des Instanzen Pools</span><span class="sxs-lookup"><span data-stu-id="5ebc0-118">Example 4: Get information about an instance pool using instance pool resource id</span></span>
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

<span data-ttu-id="5ebc0-119">Dieser Befehl ruft Informationen zum Instanzen Pool mit dem zugehörigen Ressourcenbezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="5ebc0-119">This command gets information about the instance pool with its resource identifier.</span></span>

## <span data-ttu-id="5ebc0-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ebc0-120">PARAMETERS</span></span>

### <span data-ttu-id="5ebc0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ebc0-121">-DefaultProfile</span></span>
<span data-ttu-id="5ebc0-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5ebc0-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ebc0-123">-Name</span><span class="sxs-lookup"><span data-stu-id="5ebc0-123">-Name</span></span>
<span data-ttu-id="5ebc0-124">Der Name des Instanz Pools.</span><span class="sxs-lookup"><span data-stu-id="5ebc0-124">The instance pool name.</span></span>

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

### <span data-ttu-id="5ebc0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ebc0-125">-ResourceGroupName</span></span>
<span data-ttu-id="5ebc0-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5ebc0-126">The resource group name.</span></span>

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

### <span data-ttu-id="5ebc0-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5ebc0-127">-ResourceId</span></span>
<span data-ttu-id="5ebc0-128">Der Ressourcenbezeichner des Instanz Pools.</span><span class="sxs-lookup"><span data-stu-id="5ebc0-128">The instance pool resource identifier.</span></span>

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

### <span data-ttu-id="5ebc0-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ebc0-129">CommonParameters</span></span>
<span data-ttu-id="5ebc0-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ebc0-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ebc0-131">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5ebc0-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ebc0-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5ebc0-132">INPUTS</span></span>

### <span data-ttu-id="5ebc0-133">Keine</span><span class="sxs-lookup"><span data-stu-id="5ebc0-133">None</span></span>

## <span data-ttu-id="5ebc0-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5ebc0-134">OUTPUTS</span></span>

### <span data-ttu-id="5ebc0-135">Microsoft.Azure.Commands.SQL.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="5ebc0-135">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

## <span data-ttu-id="5ebc0-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="5ebc0-136">NOTES</span></span>

## <span data-ttu-id="5ebc0-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5ebc0-137">RELATED LINKS</span></span>
