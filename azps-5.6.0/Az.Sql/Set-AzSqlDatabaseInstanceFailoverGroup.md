---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 3031878e30307cd5ff733de6177bc3c65c61a5bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101926280"
---
# <span data-ttu-id="c2e8d-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="c2e8d-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="c2e8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2e8d-102">SYNOPSIS</span></span>
<span data-ttu-id="c2e8d-103">Ändert die Konfiguration einer Instanz-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="c2e8d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2e8d-104">SYNTAX</span></span>

### <span data-ttu-id="c2e8d-105">SetInstanceFailoverGroupDefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c2e8d-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2e8d-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="c2e8d-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2e8d-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="c2e8d-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2e8d-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2e8d-108">DESCRIPTION</span></span>
<span data-ttu-id="c2e8d-109">Mit diesem Befehl wird die Konfiguration einer Instanz-Failovergruppe geändert.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="c2e8d-110">Der primäre Bereich der Instanz-Failovergruppe sollte zum Ausführen des Befehls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="c2e8d-111">Während der Vorschau des Features Instanz-Failovergruppen werden für den Parameter "-GracePeriodWithDataLossHours" nur Werte unterstützt, die größer oder gleich 1 Stunde sind.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="c2e8d-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c2e8d-112">EXAMPLES</span></span>

### <span data-ttu-id="c2e8d-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c2e8d-113">Example 1</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseInstanceFailoverGroup -ResourceGroupName rg -Location location -Name fg | Set-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Manual
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
ReadWriteFailoverPolicy               : Manual
FailoverWithDataLossGracePeriodHours  : 
ReadOnlyFailoverPolicy                : Disabled
Id                                    : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/rg/providers/Microsoft.Sql/locations/eastus/instanceFailoverGroups/fg
```

<span data-ttu-id="c2e8d-114">Legt die Failoverrichtlinie einer Instanz-Failovergruppe durch Piping in der Failovergruppe auf "Manuell" fest.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="c2e8d-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c2e8d-115">PARAMETERS</span></span>

### <span data-ttu-id="c2e8d-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="c2e8d-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="c2e8d-117">Gibt an, ob Ausfälle auf dem sekundären Server ein automatisches Failover des schreibgeschützten Endpunkts auslösen sollten.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e8d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2e8d-118">-DefaultProfile</span></span>
<span data-ttu-id="c2e8d-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2e8d-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="c2e8d-120">-FailoverPolicy</span></span>
<span data-ttu-id="c2e8d-121">Die Failoverrichtlinie der Instanz-Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-121">The failover policy of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e8d-122">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="c2e8d-122">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="c2e8d-123">Intervall vor dem Starten des automatischen Failovers, wenn ein Ausfall auf dem primären Server auftritt und der Failover ohne Datenverlust nicht abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-123">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e8d-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c2e8d-124">-InputObject</span></span>
<span data-ttu-id="c2e8d-125">Das zu setzende Instanz-Failover-Gruppenobjekt</span><span class="sxs-lookup"><span data-stu-id="c2e8d-125">The Instance Failover Group object to set</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel
Parameter Sets: SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c2e8d-126">-Location</span><span class="sxs-lookup"><span data-stu-id="c2e8d-126">-Location</span></span>
<span data-ttu-id="c2e8d-127">Der Name der lokalen Region, aus der die Instanz-Failovergruppe abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet, SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e8d-128">-Name</span><span class="sxs-lookup"><span data-stu-id="c2e8d-128">-Name</span></span>
<span data-ttu-id="c2e8d-129">Der Name der Instanz-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-129">The name of the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e8d-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2e8d-130">-ResourceGroupName</span></span>
<span data-ttu-id="c2e8d-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-131">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupDefaultSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c2e8d-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2e8d-132">-ResourceId</span></span>
<span data-ttu-id="c2e8d-133">Die Ressourcen-ID der zu setzende Instanz-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-133">The Resource ID of the Instance Failover Group to set.</span></span>

```yaml
Type: System.String
Parameter Sets: SetInstanceFailoverGroupByResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c2e8d-134">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c2e8d-134">-Confirm</span></span>
<span data-ttu-id="c2e8d-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2e8d-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2e8d-136">-WhatIf</span></span>
<span data-ttu-id="c2e8d-137">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2e8d-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2e8d-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2e8d-139">CommonParameters</span></span>
<span data-ttu-id="c2e8d-140">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2e8d-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2e8d-141">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c2e8d-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2e8d-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c2e8d-142">INPUTS</span></span>

### <span data-ttu-id="c2e8d-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c2e8d-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="c2e8d-144">System.String</span><span class="sxs-lookup"><span data-stu-id="c2e8d-144">System.String</span></span>

## <span data-ttu-id="c2e8d-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c2e8d-145">OUTPUTS</span></span>

### <span data-ttu-id="c2e8d-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="c2e8d-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="c2e8d-147">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c2e8d-147">NOTES</span></span>

## <span data-ttu-id="c2e8d-148">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c2e8d-148">RELATED LINKS</span></span>
