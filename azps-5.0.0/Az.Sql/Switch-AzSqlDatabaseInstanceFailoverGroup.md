---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/switch-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 9f82c8a50cba86fed394d55692d03eeec2ef97ef
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94178990"
---
# <span data-ttu-id="102fc-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="102fc-101">Switch-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="102fc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="102fc-102">SYNOPSIS</span></span>
<span data-ttu-id="102fc-103">Führt ein Failover einer Instanz-failovergruppe aus.</span><span class="sxs-lookup"><span data-stu-id="102fc-103">Executes a failover of an Instance Failover Group.</span></span>

## <span data-ttu-id="102fc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="102fc-104">SYNTAX</span></span>

### <span data-ttu-id="102fc-105">SwitchInstanceFailoverGroupDefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="102fc-105">SwitchInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-AllowDataLoss] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="102fc-106">SwitchInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="102fc-106">SwitchInstanceFailoverGroupByResourceIdSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="102fc-107">SwitchInstanceFailoverGroupByInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="102fc-107">SwitchInstanceFailoverGroupByInputObjectSet</span></span>
```
Switch-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel> [-AllowDataLoss]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="102fc-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="102fc-108">DESCRIPTION</span></span>
<span data-ttu-id="102fc-109">Dieser Befehl vertauscht die Rollen der verwalteten Instanzen in einer Instanz-failovergruppe durch einen Failover auf den angegebenen sekundären Bereich, wodurch dieser zum neuen primären Bereich wird.</span><span class="sxs-lookup"><span data-stu-id="102fc-109">This command swaps the roles of the managed instances in a Instance Failover Group by failing over to the specified secondary region, making it the new primary region.</span></span> <span data-ttu-id="102fc-110">Alle neuen TDS-Sitzungen, die eine Verbindung mit dem primären Endpunkt herstellen, werden automatisch an den neuen primären Bereich weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="102fc-110">All new TDS sessions connecting to the primary endpoint are automatically re-routed to the new primary region.</span></span> 

## <span data-ttu-id="102fc-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="102fc-111">EXAMPLES</span></span>

### <span data-ttu-id="102fc-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="102fc-112">Example 1</span></span>
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

<span data-ttu-id="102fc-113">Führen Sie einen Failover-Vorgang aus, der den Datenverlust durch Verrohrung in der Gruppe "Instanzen Failover" ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="102fc-113">Issue a failover operation allowing data loss by piping in the Instance Failover Group.</span></span>

### <span data-ttu-id="102fc-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="102fc-114">Example 2</span></span>
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

<span data-ttu-id="102fc-115">Führen Sie einen bestmöglichen Failover-Vorgang aus, der entweder erfolgreich ist, ohne Daten zu verlieren oder einen Fehler zu verursachen und zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="102fc-115">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="102fc-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="102fc-116">PARAMETERS</span></span>

### <span data-ttu-id="102fc-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="102fc-117">-AllowDataLoss</span></span>
<span data-ttu-id="102fc-118">Führen Sie das Failover durch, auch wenn dies zu einem Datenverlust führen kann.</span><span class="sxs-lookup"><span data-stu-id="102fc-118">Complete the failover even if doing so may result in data loss.</span></span>
<span data-ttu-id="102fc-119">Auf diese Weise kann das Failover fortgesetzt werden, selbst wenn eine primäre Datenbank nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="102fc-119">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

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

### <span data-ttu-id="102fc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="102fc-120">-DefaultProfile</span></span>
<span data-ttu-id="102fc-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="102fc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="102fc-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="102fc-122">-InputObject</span></span>
<span data-ttu-id="102fc-123">Das zu ändernde Instanzen-Failover-Gruppenobjekt</span><span class="sxs-lookup"><span data-stu-id="102fc-123">The Instance Failover Group object to switch</span></span>

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

### <span data-ttu-id="102fc-124">-Standort</span><span class="sxs-lookup"><span data-stu-id="102fc-124">-Location</span></span>
<span data-ttu-id="102fc-125">Der Name des lokalen Bereichs, aus dem die Gruppe der Instanz-Failover abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="102fc-125">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="102fc-126">-Name</span><span class="sxs-lookup"><span data-stu-id="102fc-126">-Name</span></span>
<span data-ttu-id="102fc-127">Der Name der Instanz-Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="102fc-127">The name of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="102fc-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="102fc-128">-ResourceGroupName</span></span>
<span data-ttu-id="102fc-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="102fc-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="102fc-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="102fc-130">-ResourceId</span></span>
<span data-ttu-id="102fc-131">Die Ressourcen-ID der zu wechselnden Instanzen-failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="102fc-131">The Resource ID of the Instance Failover Group to switch.</span></span>

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

### <span data-ttu-id="102fc-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="102fc-132">-Confirm</span></span>
<span data-ttu-id="102fc-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="102fc-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="102fc-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="102fc-134">-WhatIf</span></span>
<span data-ttu-id="102fc-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="102fc-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="102fc-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="102fc-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="102fc-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="102fc-137">CommonParameters</span></span>
<span data-ttu-id="102fc-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="102fc-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="102fc-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="102fc-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="102fc-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="102fc-140">INPUTS</span></span>

### <span data-ttu-id="102fc-141">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="102fc-141">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="102fc-142">System. String</span><span class="sxs-lookup"><span data-stu-id="102fc-142">System.String</span></span>

## <span data-ttu-id="102fc-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="102fc-143">OUTPUTS</span></span>

### <span data-ttu-id="102fc-144">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="102fc-144">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="102fc-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="102fc-145">NOTES</span></span>

## <span data-ttu-id="102fc-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="102fc-146">RELATED LINKS</span></span>
