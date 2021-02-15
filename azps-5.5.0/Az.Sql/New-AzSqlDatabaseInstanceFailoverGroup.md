---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 99be70e225dd607c580c4571f4ae332e7badf33a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100158265"
---
# <span data-ttu-id="8138b-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="8138b-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="8138b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8138b-102">SYNOPSIS</span></span>
<span data-ttu-id="8138b-103">Dieser Befehl erstellt eine neue Azure SQL-Datenbankinstanz-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="8138b-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="8138b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8138b-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup [-Name] <String> [-PartnerResourceGroupName <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-PartnerSubscriptionId <String>] [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8138b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8138b-105">DESCRIPTION</span></span>
<span data-ttu-id="8138b-106">Erstellt eine neue Azure SQL Datenbankinstanz-Failovergruppe zwischen den angegebenen Regionen mit dem angegebenen Paar verwalteter Instanzen.</span><span class="sxs-lookup"><span data-stu-id="8138b-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="8138b-107">Zwei Azure SQL Database TDS-Endpunkte werden in Name.SqlDatabaseDnsSuffix (z. B. Name.database.windows.net) und Name.secondary.SqlDatabaseDnsSuffix erstellt.</span><span class="sxs-lookup"><span data-stu-id="8138b-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="8138b-108">Diese Endpunkte können verwendet werden, um eine Verbindung mit den primären bzw. sekundären Regionen der Failovergruppe herzustellen.</span><span class="sxs-lookup"><span data-stu-id="8138b-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="8138b-109">Wenn der primäre Bereich von einem Ausfall betroffen ist, wird das automatische Failover der Endpunkte und Datenbanken ausgelöst, wie es von der Failoverrichtlinie und dem Toleranzzeitraum der Instanz failovergruppe vorgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8138b-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="8138b-110">Während der Vorschau auf das Feature "Instanz-Failovergruppen" werden für den Parameter "-GracePeriodWithDataLossHours" nur Werte unterstützt, die größer oder gleich 1 Stunde sind.</span><span class="sxs-lookup"><span data-stu-id="8138b-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="8138b-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8138b-111">EXAMPLES</span></span>

### <span data-ttu-id="8138b-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8138b-112">Example 1</span></span>
```powershell
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
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

<span data-ttu-id="8138b-113">Mit diesem Befehl wird eine neue Instanz failovergruppe mit der Failoverrichtlinie 'Automatic' für das paar verwaltete Instanzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="8138b-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="8138b-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="8138b-114">Example 2</span></span>
```powershell
C:\> $failoverGroup = New-AzSqlDatabaseInstanceFailoverGroup -Name fgName -Location location -ResourceGroupName rg -PrimaryManagedInstanceName $managedInstance.Name -PartnerRegion $partnerRegion -PartnerManagedInstanceName $partnerManagedInstance.Name -FailoverPolicy Manual
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

<span data-ttu-id="8138b-115">Mit diesem Befehl wird eine neue Instanz failovergruppe mit der Failoverrichtlinie "Manual" für das Paar verwalteter Instanzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="8138b-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

### <span data-ttu-id="8138b-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="8138b-116">Example 3</span></span>

<span data-ttu-id="8138b-117">Dieser Befehl erstellt eine neue Azure SQL-Datenbankinstanz-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="8138b-117">This command creates a new Azure SQL Database Instance Failover Group.</span></span> <span data-ttu-id="8138b-118">(automatisch generiert)</span><span class="sxs-lookup"><span data-stu-id="8138b-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1 -Location location -Name fgName -PartnerManagedInstanceName $partnerManagedInstance.Name -PartnerRegion $partnerRegion -PartnerResourceGroupName rg2 -PrimaryManagedInstanceName $managedInstance.Name -ResourceGroupName rg
```

## <span data-ttu-id="8138b-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8138b-119">PARAMETERS</span></span>

### <span data-ttu-id="8138b-120">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="8138b-120">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="8138b-121">Gibt an, ob ein Ausfall auf dem sekundären Server ein automatisches Failover des schreibgeschützten Endpunkts auslösen soll.</span><span class="sxs-lookup"><span data-stu-id="8138b-121">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="8138b-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8138b-122">-DefaultProfile</span></span>
<span data-ttu-id="8138b-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8138b-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8138b-124">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="8138b-124">-FailoverPolicy</span></span>
<span data-ttu-id="8138b-125">Die Failoverrichtlinie der Instanz failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="8138b-125">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="8138b-126">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="8138b-126">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="8138b-127">Intervall vor dem Starten des automatischen Failovers, wenn ein Ausfall auf dem primären Server auftritt und der Failover nicht ohne Datenverlust abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="8138b-127">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="8138b-128">-Location</span><span class="sxs-lookup"><span data-stu-id="8138b-128">-Location</span></span>
<span data-ttu-id="8138b-129">Der Name der lokalen Region, aus der die Instanz failovergruppe abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="8138b-129">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8138b-130">-Name</span><span class="sxs-lookup"><span data-stu-id="8138b-130">-Name</span></span>
<span data-ttu-id="8138b-131">Der Name der Azure SQL-Datenbank-Failovergruppe, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8138b-131">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8138b-132">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="8138b-132">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="8138b-133">Der Name der verwalteten Instanz in der Partnerregion, die der Instanz failovergruppe hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8138b-133">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="8138b-134">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="8138b-134">-PartnerRegion</span></span>
<span data-ttu-id="8138b-135">Der Name der Partnerregion der Instanz-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="8138b-135">The name of the partner region of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="8138b-136">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8138b-136">-PartnerResourceGroupName</span></span>
<span data-ttu-id="8138b-137">Der Name der sekundären Ressourcengruppe der Instanz failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="8138b-137">The name of the secondary resource group of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="8138b-138">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8138b-138">-PartnerSubscriptionId</span></span>
<span data-ttu-id="8138b-139">Die Abonnement-ID der sekundären verwalteten Instanz der Instanz-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="8138b-139">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="8138b-140">Dieser Parameter ist nur für die Einrichtung über ein abonnementübergreifendes Abonnement erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8138b-140">This parameter is only needed for cross-subscription setup</span></span>

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

### <span data-ttu-id="8138b-141">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="8138b-141">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="8138b-142">Der Name der verwalteten Instanz in der lokalen Region, die der Instanz failovergruppe hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8138b-142">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="8138b-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8138b-143">-ResourceGroupName</span></span>
<span data-ttu-id="8138b-144">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8138b-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8138b-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8138b-145">-Confirm</span></span>
<span data-ttu-id="8138b-146">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8138b-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8138b-147">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8138b-147">-WhatIf</span></span>
<span data-ttu-id="8138b-148">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8138b-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8138b-149">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8138b-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8138b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8138b-150">CommonParameters</span></span>
<span data-ttu-id="8138b-151">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8138b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8138b-152">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8138b-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8138b-153">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8138b-153">INPUTS</span></span>

### <span data-ttu-id="8138b-154">System.String</span><span class="sxs-lookup"><span data-stu-id="8138b-154">System.String</span></span>

## <span data-ttu-id="8138b-155">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8138b-155">OUTPUTS</span></span>

### <span data-ttu-id="8138b-156">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="8138b-156">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="8138b-157">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8138b-157">NOTES</span></span>

## <span data-ttu-id="8138b-158">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8138b-158">RELATED LINKS</span></span>
