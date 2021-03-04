---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: a20f2196b6052befb74cd74366c96bf262cdd325
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939323"
---
# <span data-ttu-id="753da-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="753da-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="753da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="753da-102">SYNOPSIS</span></span>
<span data-ttu-id="753da-103">Führt einen Failover einer Instanz-Failovergruppe aus.</span><span class="sxs-lookup"><span data-stu-id="753da-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="753da-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="753da-104">SYNTAX</span></span>

### <span data-ttu-id="753da-105">SwitchInstanceFailoverGroupDefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="753da-105">SwitchInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="753da-106">SwitchInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="753da-106">SwitchInstanceFailoverGroupByResourceIdSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="753da-107">SwitchInstanceFailoverGroupByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="753da-107">SwitchInstanceFailoverGroupByInputObjectSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="753da-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="753da-108">DESCRIPTION</span></span>
<span data-ttu-id="753da-109">Dieser Befehl tauscht die Rollen der verwalteten Instanzen in einer Instanz-Failovergruppe aus, indem er zum angegebenen sekundären Bereich wechselt, wodurch er zur neuen primären Region wird.</span><span class="sxs-lookup"><span data-stu-id="753da-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="753da-110">Alle neuen TDS-Sitzungen, die eine Verbindung mit dem primären Endpunkt herstellen, werden automatisch erneut an die neue primäre Region geleitet.</span><span class="sxs-lookup"><span data-stu-id="753da-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="753da-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="753da-111">EXAMPLES</span></span>

### <span data-ttu-id="753da-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="753da-112">Example 1</span></span>
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

<span data-ttu-id="753da-113">Führen Sie einen Failovervorgang aus, der Datenverlust durch Piping in der Instanz-Failover-Gruppe ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="753da-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="753da-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="753da-114">Example 2</span></span>
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

<span data-ttu-id="753da-115">Führen Sie einen Failovervorgang mit optimalem Aufwand aus, der entweder erfolgreich ist, ohne Daten zu verlieren, oder fehlschlagen und ein Rollback ausführen.</span><span class="sxs-lookup"><span data-stu-id="753da-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="753da-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="753da-116">PARAMETERS</span></span>

### <span data-ttu-id="753da-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="753da-117">-AllowDataLoss</span></span>
<span data-ttu-id="753da-118">Schließen Sie den Failover ab, auch wenn dies zu Datenverlust führen kann.</span><span class="sxs-lookup"><span data-stu-id="753da-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="753da-119">Dadurch kann der Failover fortgesetzt werden, auch wenn eine primäre Datenbank nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="753da-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="753da-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="753da-120">-DefaultProfile</span></span>
<span data-ttu-id="753da-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="753da-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="753da-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="753da-122">-InputObject</span></span>
<span data-ttu-id="753da-123">Das Instance Failover Group-Objekt zum Wechseln</span><span class="sxs-lookup"><span data-stu-id="753da-123">The Instance Failover Group object to switch</span></span>

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

### <span data-ttu-id="753da-124">-Location</span><span class="sxs-lookup"><span data-stu-id="753da-124">-Location</span></span>
<span data-ttu-id="753da-125">Der Name der lokalen Region, aus der die Instanz-Failovergruppe abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="753da-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="753da-126">-Name</span><span class="sxs-lookup"><span data-stu-id="753da-126">-Name</span></span>
<span data-ttu-id="753da-127">Der Name der Instanz-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="753da-127">The name of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="753da-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="753da-128">-ResourceGroupName</span></span>
<span data-ttu-id="753da-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="753da-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="753da-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="753da-130">-ResourceId</span></span>
<span data-ttu-id="753da-131">Die Ressourcen-ID der Zu wechselnde Instanz-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="753da-131">The Resource ID of the Instance Failover Group to switch.</span></span>

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

### <span data-ttu-id="753da-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="753da-132">-Confirm</span></span>
<span data-ttu-id="753da-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="753da-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="753da-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="753da-134">-WhatIf</span></span>
<span data-ttu-id="753da-135">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="753da-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="753da-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="753da-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="753da-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="753da-137">CommonParameters</span></span>
<span data-ttu-id="753da-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="753da-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="753da-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="753da-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="753da-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="753da-140">INPUTS</span></span>

### <span data-ttu-id="753da-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="753da-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="753da-142">System.String</span><span class="sxs-lookup"><span data-stu-id="753da-142">System.String</span></span>

## <span data-ttu-id="753da-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="753da-143">OUTPUTS</span></span>

### <span data-ttu-id="753da-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="753da-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="753da-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="753da-145">NOTES</span></span>

## <span data-ttu-id="753da-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="753da-146">RELATED LINKS</span></span>
