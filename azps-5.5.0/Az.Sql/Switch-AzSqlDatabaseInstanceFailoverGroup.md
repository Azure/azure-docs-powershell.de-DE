---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 9f82c8a50cba86fed394d55692d03eeec2ef97ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158204"
---
# <span data-ttu-id="37b43-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="37b43-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="37b43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37b43-102">SYNOPSIS</span></span>
<span data-ttu-id="37b43-103">Führt einen Failover einer Instanz failovergruppe aus.</span><span class="sxs-lookup"><span data-stu-id="37b43-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="37b43-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="37b43-104">SYNTAX</span></span>

### <span data-ttu-id="37b43-105">SwitchInstanceFailoverGroupDefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="37b43-105">SwitchInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37b43-106">SwitchInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="37b43-106">SwitchInstanceFailoverGroupByResourceIdSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37b43-107">SwitchInstanceFailoverGroupByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="37b43-107">SwitchInstanceFailoverGroupByInputObjectSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37b43-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="37b43-108">DESCRIPTION</span></span>
<span data-ttu-id="37b43-109">Dieser Befehl tauscht die Rollen der verwalteten Instanzen in einer Instanz failovergruppe aus, indem ein Failover zum angegebenen sekundären Bereich fehlt, wodurch er zur neuen primären Region wird.</span><span class="sxs-lookup"><span data-stu-id="37b43-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="37b43-110">Alle neuen TDS-Sitzungen, die mit dem primären Endpunkt verbunden sind, werden automatisch an die neue primäre Region umgeroutet.</span><span class="sxs-lookup"><span data-stu-id="37b43-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="37b43-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="37b43-111">EXAMPLES</span></span>

### <span data-ttu-id="37b43-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="37b43-112">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup -AllowDataLoss
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="37b43-113">Führen Sie einen Failovervorgang aus, der Datenverlust ermöglicht, indem sie in die Instanz failovergruppe pipiert.</span><span class="sxs-lookup"><span data-stu-id="37b43-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="37b43-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="37b43-114">Example 2</span></span>
```
C:\> Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Switch-AzSqlDatabaseInstanceFailoverGroup
Output:
ResourceGroupName                     : rg
Location                              : East US
Name                                  : fg
PartnerResourceGroupName              : rg
PartnerRegion                         : West US
PrimaryManagedInstanceName            : managedInstance1
PartnerManagedInstanceName            : managedInstance2
ReplicationRole                       : Primary
ReplicationState                      : CATCH_UP
ReadWriteFailoverPolicy               : Automatic
FailoverWithDataLossGracePeriodHours  : 1
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="37b43-115">Führen Sie einen Best-Effort-Failovervorgang aus, der entweder erfolgreich ist, ohne dass Daten verloren gehen, oder fehlschlagen und ein Rollback durchführen.</span><span class="sxs-lookup"><span data-stu-id="37b43-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="37b43-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="37b43-116">PARAMETERS</span></span>

### <span data-ttu-id="37b43-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="37b43-117">-AllowDataLoss</span></span>
<span data-ttu-id="37b43-118">Schließen Sie den Failover ab, auch wenn dies zu Datenverlust führen kann.</span><span class="sxs-lookup"><span data-stu-id="37b43-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="37b43-119">Dadurch kann der Failover fortgesetzt werden, auch wenn eine primäre Datenbank nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="37b43-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="37b43-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b43-120">-DefaultProfile</span></span>
<span data-ttu-id="37b43-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37b43-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37b43-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="37b43-122">-InputObject</span></span>
<span data-ttu-id="37b43-123">Das zu wechselnde Instanz-Failovergruppenobjekt</span><span class="sxs-lookup"><span data-stu-id="37b43-123">The Instance Failover Group object to switch</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SwitchInstanceFailoverGroupByInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37b43-124">-Location</span><span class="sxs-lookup"><span data-stu-id="37b43-124">-Location</span></span>
<span data-ttu-id="37b43-125">Der Name der lokalen Region, aus der die Instanz failovergruppe abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="37b43-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet, SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b43-126">-Name</span><span class="sxs-lookup"><span data-stu-id="37b43-126">-Name</span></span>
<span data-ttu-id="37b43-127">Der Name der Instanz failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="37b43-127">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b43-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37b43-128">-ResourceGroupName</span></span>
<span data-ttu-id="37b43-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="37b43-129">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b43-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37b43-130">-ResourceId</span></span>
<span data-ttu-id="37b43-131">Die Ressourcen-ID der zu wechselnde Instanz failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="37b43-131">The Resource ID of the Instance Failover Group to switch.</span></span>

```yaml
Type: System.String
Parameter Sets: SwitchInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37b43-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="37b43-132">-Confirm</span></span>
<span data-ttu-id="37b43-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37b43-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b43-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="37b43-134">-WhatIf</span></span>
<span data-ttu-id="37b43-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37b43-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37b43-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37b43-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b43-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b43-137">CommonParameters</span></span>
<span data-ttu-id="37b43-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37b43-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b43-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="37b43-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b43-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="37b43-140">INPUTS</span></span>

### <span data-ttu-id="37b43-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="37b43-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="37b43-142">System.String</span><span class="sxs-lookup"><span data-stu-id="37b43-142">System.String</span></span>

## <span data-ttu-id="37b43-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="37b43-143">OUTPUTS</span></span>

### <span data-ttu-id="37b43-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="37b43-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="37b43-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="37b43-145">NOTES</span></span>

## <span data-ttu-id="37b43-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="37b43-146">RELATED LINKS</span></span>
