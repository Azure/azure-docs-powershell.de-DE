---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: c1164f7c4875d6cdd00ca13236c1d8e6d4b07cb3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368988"
---
# <span data-ttu-id="d4d90-101">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d4d90-101">New-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="d4d90-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4d90-102">SYNOPSIS</span></span>
<span data-ttu-id="d4d90-103">Mit diesem Befehl wird eine neue Azure SQL A0 erstellt.</span><span class="sxs-lookup"><span data-stu-id="d4d90-103">This command creates a new Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="d4d90-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4d90-104">SYNTAX</span></span>

```
New-AzSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d4d90-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4d90-105">DESCRIPTION</span></span>
<span data-ttu-id="d4d90-106">Erstellt eine neue Azure SQL-Datenbank-Failovergruppe für die angegebenen Server.</span><span class="sxs-lookup"><span data-stu-id="d4d90-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>
<span data-ttu-id="d4d90-107">Zwei Azure SQL Database TDS-Endpunkte werden unter FailoverGroupName.SqlDatabaseDnsSuffix (z. B. FailoverGroupName.database.windows.net) und FailoverGroupName.secondary.SqlDatabaseDnsSuffix erstellt.</span><span class="sxs-lookup"><span data-stu-id="d4d90-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="d4d90-108">Diese Endpunkte können verwendet werden, um eine Verbindung mit den primären bzw. sekundären Servern in der Failovergruppe herzustellen.</span><span class="sxs-lookup"><span data-stu-id="d4d90-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="d4d90-109">Wenn der primäre Server von einem Ausfall betroffen ist, wird das automatische Failover der Endpunkte und Datenbanken ausgelöst, wie es von der Failoverrichtlinie und dem Toleranzzeitraum der Failovergruppe vorgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d4d90-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>
<span data-ttu-id="d4d90-110">Neu erstellte Failovergruppen enthalten keine Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="d4d90-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="d4d90-111">Zum Steuern der Gruppe von Datenbanken in einer Failovergruppe verwenden Sie die Cmdlets "Add-AzSqlDatabaseToFailoverGroup" und "Remove-AzSqlDatabaseFromFailoverGroup".</span><span class="sxs-lookup"><span data-stu-id="d4d90-111">To control the set of databases in a Failover Group, use the 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' cmdlets.</span></span>
<span data-ttu-id="d4d90-112">Für den Parameter "-GracePeriodWithDataLossHours" werden nur Werte unterstützt, die größer gleich 1 Stunde sind.</span><span class="sxs-lookup"><span data-stu-id="d4d90-112">Only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="d4d90-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d4d90-113">EXAMPLES</span></span>

### <span data-ttu-id="d4d90-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d4d90-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="d4d90-115">Mit diesem Befehl wird eine neue Failovergruppe mit der Failoverrichtlinie "Automatic" für zwei Server in derselben Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="d4d90-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="d4d90-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d4d90-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="d4d90-117">Mit diesem Befehl wird eine neue Failovergruppe mit der Failoverrichtlinie "Manual" für zwei Server in verschiedenen Ressourcengruppen erstellt.</span><span class="sxs-lookup"><span data-stu-id="d4d90-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="d4d90-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4d90-118">PARAMETERS</span></span>

### <span data-ttu-id="d4d90-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="d4d90-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="d4d90-120">Gibt an, ob ein Ausfall auf dem sekundären Server ein automatisches Failover des schreibgeschützten Endpunkts auslösen soll.</span><span class="sxs-lookup"><span data-stu-id="d4d90-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="d4d90-121">Dieses Feature wird noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4d90-121">This feature is not yet supported.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d90-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4d90-122">-DefaultProfile</span></span>
<span data-ttu-id="d4d90-123">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d4d90-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d4d90-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="d4d90-124">-FailoverGroupName</span></span>
<span data-ttu-id="d4d90-125">Der Name der Azure SQL-Datenbank-Failovergruppe, die erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4d90-125">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="d4d90-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="d4d90-126">-FailoverPolicy</span></span>
<span data-ttu-id="d4d90-127">Die Failoverrichtlinie der Azure SQL-Datenbank-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="d4d90-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.FailoverGroup.Model.FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d90-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="d4d90-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="d4d90-129">Intervall vor dem Starten des automatischen Failovers, wenn ein Ausfall auf dem primären Server auftritt und der Failover nicht ohne Datenverlust abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="d4d90-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4d90-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4d90-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="d4d90-131">Der Name der sekundären Ressourcengruppe der Azure SQL-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="d4d90-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="d4d90-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="d4d90-132">-PartnerServerName</span></span>
<span data-ttu-id="d4d90-133">Der Name des sekundären Servers der Azure SQL-Datenbank-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="d4d90-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="d4d90-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4d90-134">-ResourceGroupName</span></span>
<span data-ttu-id="d4d90-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d4d90-135">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4d90-136">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d4d90-136">-ServerName</span></span>
<span data-ttu-id="d4d90-137">Der Name des primären Azure SQL Datenbankservers der Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="d4d90-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4d90-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4d90-138">CommonParameters</span></span>
<span data-ttu-id="d4d90-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4d90-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4d90-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d4d90-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4d90-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d4d90-141">INPUTS</span></span>

### <span data-ttu-id="d4d90-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d4d90-142">System.String</span></span>

## <span data-ttu-id="d4d90-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d4d90-143">OUTPUTS</span></span>

### <span data-ttu-id="d4d90-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="d4d90-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="d4d90-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d4d90-145">NOTES</span></span>

## <span data-ttu-id="d4d90-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d4d90-146">RELATED LINKS</span></span>

[<span data-ttu-id="d4d90-147">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d4d90-147">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d4d90-148">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d4d90-148">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d4d90-149">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d4d90-149">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="d4d90-150">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d4d90-150">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="d4d90-151">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d4d90-151">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d4d90-152">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="d4d90-152">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="d4d90-153">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="d4d90-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
