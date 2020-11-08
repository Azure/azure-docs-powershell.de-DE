---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlinstancepoolusage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstancePoolUsage.md
ms.openlocfilehash: c2acc357e53a57060f7ba1ff3e19a5344ceee412
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174130"
---
# <span data-ttu-id="ccace-101">Get-AzSqlInstancePoolUsage</span><span class="sxs-lookup"><span data-stu-id="ccace-101">Get-AzSqlInstancePoolUsage</span></span>

## <span data-ttu-id="ccace-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ccace-102">SYNOPSIS</span></span>
<span data-ttu-id="ccace-103">Gibt Informationen zur Verwendung eines Azure-SQL-Instanzen Pools zurück.</span><span class="sxs-lookup"><span data-stu-id="ccace-103">Returns information about an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="ccace-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ccace-104">SYNTAX</span></span>

### <span data-ttu-id="ccace-105">InstancePoolUsageDefaultParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ccace-105">InstancePoolUsageDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceGroupName] <String> [-Name] <String> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccace-106">InstancePoolUsageParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccace-106">InstancePoolUsageParentObjectParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-InstancePool] <AzureSqlInstancePoolModel> [-ExpandChildren]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ccace-107">InstancePoolUsageResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ccace-107">InstancePoolUsageResourceIdParameterSet</span></span>
```
Get-AzSqlInstancePoolUsage [-ResourceId] <String> [-ExpandChildren] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ccace-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ccace-108">DESCRIPTION</span></span>
<span data-ttu-id="ccace-109">Das Cmdlet " **Get-AzSqlInstancePoolUsage** " gibt Informationen zurück, die von der Verwendung des Azure SQL-Instanzen Pools abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="ccace-109">The **Get-AzSqlInstancePoolUsage** cmdlet returns information an Azure SQL Instance pool's usage.</span></span>

## <span data-ttu-id="ccace-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ccace-110">EXAMPLES</span></span>

### <span data-ttu-id="ccace-111">Beispiel 1: Ruft die Verwendung eines Azure SQL-Instanzen Pools ab</span><span class="sxs-lookup"><span data-stu-id="ccace-111">Example 1 : Gets the usage of an Azure SQL Instance pool</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceGroupName resourcegroup01 -Name instancepool0

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="ccace-112">Ruft die Verwendung für den Azure SQL instance Pool instancepool0.</span><span class="sxs-lookup"><span data-stu-id="ccace-112">Gets the usage for the Azure SQL Instance pool instancepool0.</span></span>

### <span data-ttu-id="ccace-113">Beispiel 2: Ruft die Verwendung eines Azure SQL-Instanzen Pools unter Verwendung eines Instanzen Pool Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="ccace-113">Example 2: Gets the usage of an Azure SQL Instance pool using an instance pool object</span></span>
```powershell
PS C:\> $instancePool = Get-AzSqlInstancePool -ResourceGroupName resourcegroup01 -Name instancepool0
PS C:\> Get-AzSqlInstancePoolUsage -InstancePool $instancePool

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="ccace-114">Ruft die Verwendung für den Azure SQL instance Pool-instancepool0 mithilfe eines Instanzen Pool Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="ccace-114">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool object.</span></span>

### <span data-ttu-id="ccace-115">Beispiel 3: Ruft die Verwendung eines Azure SQL-Instanzen Pools unter Verwendung einer Ressourcen-ID des Instanzen Pools ab.</span><span class="sxs-lookup"><span data-stu-id="ccace-115">Example 3: Gets the usage of an Azure SQL Instance pool using an instance pool resource id</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceId "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancePool0"

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages
```

<span data-ttu-id="ccace-116">Ruft die Verwendung für den Azure SQL instance Pool-instancepool0 mithilfe eines Ressourcenbezeichners für einen Instanzen Pool ab.</span><span class="sxs-lookup"><span data-stu-id="ccace-116">Gets the usage for the Azure SQL Instance pool instancepool0 using an instance pool resource identifier.</span></span>

### <span data-ttu-id="ccace-117">Beispiel 3: Ruft die Verwendung eines Azure SQL-Instanzen Pools mit einer Aufschlüsselung der Verwendung von verwalteten Instanzen innerhalb des Pools ab.</span><span class="sxs-lookup"><span data-stu-id="ccace-117">Example 3: Gets the usage of an Azure SQL Instance pool with a breakdown of the managed instance usages within the pool.</span></span>
```powershell
PS C:\> Get-AzSqlInstancePoolUsage -ResourceGroupName resourcegroup01 -Name instancepool0 -ExpandChildren

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/vcore_utilization
CurrentValue   : 2
Limit          : 8
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/storage_utilization
CurrentValue   : 32
Limit          : 8192
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/resourcegroup01/providers/Microsoft.Sql/instancePools/instancepool0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/vcore_utilization
CurrentValue   :
Limit          : 2
RequestedLimit :
Unit           : VCores
Name           : VCore utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/storage_utilization
CurrentValue   :
Limit          : 32
RequestedLimit :
Unit           : Gigabytes
Name           : Storage utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages

Id             : /subscriptions/2e7fe4bd-90c7-454e-8bb6-dc44649f27b2/resourceGroups/poolsPS/providers/Microsoft.Sql/instancePools/instancepool0/managedInstances/managedinstance0/usages/database_utilization
CurrentValue   : 0
Limit          : 100
RequestedLimit :
Unit           : Number Of Databases
Name           : Database utilization
Type           : Microsoft.Sql/instancePools/managedInstances/usages
```

<span data-ttu-id="ccace-118">Ruft die Verwendung für den Azure SQL instance Pool instancepool0 zusammen mit den Verwendungen der verwalteten Instanzen in instancepool0 ab.</span><span class="sxs-lookup"><span data-stu-id="ccace-118">Gets the usage for the Azure SQL Instance pool instancepool0 along with the usages of the managed instances within instancepool0.</span></span>

## <span data-ttu-id="ccace-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="ccace-119">PARAMETERS</span></span>

### <span data-ttu-id="ccace-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ccace-120">-DefaultProfile</span></span>
<span data-ttu-id="ccace-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ccace-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ccace-122">-ExpandChildren</span><span class="sxs-lookup"><span data-stu-id="ccace-122">-ExpandChildren</span></span>
<span data-ttu-id="ccace-123">Kennzeichnung, die angibt, ob die Verwendung dieses Instanzen Pools mit der Verwendung durch die Kinder erweitert werden soll.</span><span class="sxs-lookup"><span data-stu-id="ccace-123">Flag indicating whether to expand this instance pool's usage with its children's usage.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccace-124">-InstancePool</span><span class="sxs-lookup"><span data-stu-id="ccace-124">-InstancePool</span></span>
<span data-ttu-id="ccace-125">Das Pool Objekt der übergeordneten Instanz.</span><span class="sxs-lookup"><span data-stu-id="ccace-125">The parent instance pool object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel
Parameter Sets: InstancePoolUsageParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ccace-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ccace-126">-Name</span></span>
<span data-ttu-id="ccace-127">Der Name des Pool für verwaltete Instanzen.</span><span class="sxs-lookup"><span data-stu-id="ccace-127">The managed instance pool name.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageDefaultParameterSet
Aliases: InstancePoolName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccace-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ccace-128">-ResourceGroupName</span></span>
<span data-ttu-id="ccace-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ccace-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ccace-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ccace-130">-ResourceId</span></span>
<span data-ttu-id="ccace-131">Die übergeordnete Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ccace-131">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: InstancePoolUsageResourceIdParameterSet
Aliases: InstancePoolResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ccace-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccace-132">CommonParameters</span></span>
<span data-ttu-id="ccace-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccace-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccace-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ccace-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccace-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ccace-135">INPUTS</span></span>

### <span data-ttu-id="ccace-136">Microsoft.Azure.Commands.SQL.Instance_Pools. Model. AzureSqlInstancePoolModel</span><span class="sxs-lookup"><span data-stu-id="ccace-136">Microsoft.Azure.Commands.Sql.Instance_Pools.Model.AzureSqlInstancePoolModel</span></span>

### <span data-ttu-id="ccace-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ccace-137">System.String</span></span>

## <span data-ttu-id="ccace-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ccace-138">OUTPUTS</span></span>

### <span data-ttu-id="ccace-139">Microsoft. Azure. Commands. SQL. usages. Models. AzureSqlUsageModel</span><span class="sxs-lookup"><span data-stu-id="ccace-139">Microsoft.Azure.Commands.Sql.Usages.Models.AzureSqlUsageModel</span></span>

## <span data-ttu-id="ccace-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="ccace-140">NOTES</span></span>

## <span data-ttu-id="ccace-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ccace-141">RELATED LINKS</span></span>
