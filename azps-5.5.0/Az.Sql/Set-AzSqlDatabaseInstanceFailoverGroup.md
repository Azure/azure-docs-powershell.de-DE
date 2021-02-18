---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/set-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: f8ac83b684718a6a2698fd1b304b85ffa1ae5d45
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100175129"
---
# <span data-ttu-id="4d617-101">Set-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4d617-101">Set-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="4d617-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d617-102">SYNOPSIS</span></span>
<span data-ttu-id="4d617-103">Ändert die Konfiguration einer Instanz failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="4d617-103">Modifies the configuration of an Instance Failover Group.</span></span>

## <span data-ttu-id="4d617-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4d617-104">SYNTAX</span></span>

### <span data-ttu-id="4d617-105">SetInstanceFailoverGroupDefaultSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="4d617-105">SetInstanceFailoverGroupDefaultSet (Default)</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-ResourceGroupName] <String> [-Location] <String> [-Name] <String>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d617-106">SetInstanceFailoverGroupByResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4d617-106">SetInstanceFailoverGroupByResourceIdSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-Location] <String> [-ResourceId] <String> [-FailoverPolicy <String>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d617-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span><span class="sxs-lookup"><span data-stu-id="4d617-107">SetInstanceFailoverGroupByAzureSqlInstanceFailoverGroupModelSet</span></span>
```
Set-AzSqlDatabaseInstanceFailoverGroup [-InputObject] <AzureSqlInstanceFailoverGroupModel>
 [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d617-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4d617-108">DESCRIPTION</span></span>
<span data-ttu-id="4d617-109">Mit diesem Befehl wird die Konfiguration einer Instanz failovergruppe geändert.</span><span class="sxs-lookup"><span data-stu-id="4d617-109">This command modifies the configuration of an Instance Failover Group.</span></span>

<span data-ttu-id="4d617-110">Der primäre Bereich der Instanz failover group sollte zum Ausführen des Befehls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d617-110">The Instance Failover Group's primary region should be used to execute the command.</span></span>

<span data-ttu-id="4d617-111">Während der Vorschau auf das Feature "Instanz-Failovergruppen" werden für den Parameter "-GracePeriodWithDataLossHours" nur Werte unterstützt, die größer oder gleich 1 Stunde sind.</span><span class="sxs-lookup"><span data-stu-id="4d617-111">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="4d617-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4d617-112">EXAMPLES</span></span>

### <span data-ttu-id="4d617-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4d617-113">Example 1</span></span>
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

<span data-ttu-id="4d617-114">Legt die Failoverrichtlinie einer Instanz failover group auf "Manual" fest, indem ein Piping in der Failovergruppe erfolgt.</span><span class="sxs-lookup"><span data-stu-id="4d617-114">Sets a Instance Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="4d617-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d617-115">PARAMETERS</span></span>

### <span data-ttu-id="4d617-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="4d617-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="4d617-117">Gibt an, ob Ausfälle auf dem sekundären Server ein automatisches Failover des schreibgeschützten Endpunkts auslösen sollen.</span><span class="sxs-lookup"><span data-stu-id="4d617-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="4d617-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d617-118">-DefaultProfile</span></span>
<span data-ttu-id="4d617-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4d617-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d617-120">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="4d617-120">-FailoverPolicy</span></span>
<span data-ttu-id="4d617-121">Die Failoverrichtlinie der Instanz failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="4d617-121">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="4d617-122">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="4d617-122">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="4d617-123">Intervall vor dem Starten des automatischen Failovers, wenn ein Ausfall auf dem primären Server auftritt und der Failover nicht ohne Datenverlust abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="4d617-123">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="4d617-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4d617-124">-InputObject</span></span>
<span data-ttu-id="4d617-125">Das zu festlegende Instanz-Failovergruppenobjekt</span><span class="sxs-lookup"><span data-stu-id="4d617-125">The Instance Failover Group object to set</span></span>

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

### <span data-ttu-id="4d617-126">-Location</span><span class="sxs-lookup"><span data-stu-id="4d617-126">-Location</span></span>
<span data-ttu-id="4d617-127">Der Name der lokalen Region, aus der die Instanz failovergruppe abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d617-127">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="4d617-128">-Name</span><span class="sxs-lookup"><span data-stu-id="4d617-128">-Name</span></span>
<span data-ttu-id="4d617-129">Der Name der Instanz failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="4d617-129">The name of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="4d617-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d617-130">-ResourceGroupName</span></span>
<span data-ttu-id="4d617-131">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4d617-131">The name of the resource group.</span></span>

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

### <span data-ttu-id="4d617-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4d617-132">-ResourceId</span></span>
<span data-ttu-id="4d617-133">Die Ressourcen-ID der zu festlegende Instanz failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="4d617-133">The Resource ID of the Instance Failover Group to set.</span></span>

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

### <span data-ttu-id="4d617-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4d617-134">-Confirm</span></span>
<span data-ttu-id="4d617-135">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4d617-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d617-136">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4d617-136">-WhatIf</span></span>
<span data-ttu-id="4d617-137">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4d617-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d617-138">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d617-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d617-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d617-139">CommonParameters</span></span>
<span data-ttu-id="4d617-140">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d617-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d617-141">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d617-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d617-142">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4d617-142">INPUTS</span></span>

### <span data-ttu-id="4d617-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="4d617-143">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>
<span data-ttu-id="4d617-144">System.String</span><span class="sxs-lookup"><span data-stu-id="4d617-144">System.String</span></span>

## <span data-ttu-id="4d617-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4d617-145">OUTPUTS</span></span>

### <span data-ttu-id="4d617-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="4d617-146">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="4d617-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4d617-147">NOTES</span></span>

## <span data-ttu-id="4d617-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4d617-148">RELATED LINKS</span></span>
