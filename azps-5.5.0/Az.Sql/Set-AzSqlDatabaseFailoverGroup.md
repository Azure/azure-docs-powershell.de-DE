---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 8b78cfc7a2934b4670702562941ea0e00c2a70c8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100173809"
---
# <span data-ttu-id="930fe-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="930fe-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="930fe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="930fe-102">SYNOPSIS</span></span>
<span data-ttu-id="930fe-103">Ändert die Konfiguration einer Azure SQL-Datenbank-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="930fe-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="930fe-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="930fe-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="930fe-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="930fe-105">DESCRIPTION</span></span>
<span data-ttu-id="930fe-106">Dieser Befehl ändert die Konfiguration einer Azure SQL-Datenbank-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="930fe-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="930fe-107">Der primäre Server der Failovergruppe sollte zum Ausführen des Befehls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="930fe-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="930fe-108">Verwenden Sie zum Steuern der Gruppe von Datenbanken in der Gruppe stattdessen "Add-AzSqlDatabaseToFailoverGroup" und "Remove-AzSqlDatabaseFromFailoverGroup".</span><span class="sxs-lookup"><span data-stu-id="930fe-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="930fe-109">Während der Vorschau des Features "Failovergruppen" werden für den Parameter "-GracePeriodWithDataLossHours" nur Werte unterstützt, die größer oder gleich 1 Stunde sind.</span><span class="sxs-lookup"><span data-stu-id="930fe-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="930fe-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="930fe-110">EXAMPLES</span></span>

### <span data-ttu-id="930fe-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="930fe-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="930fe-112">Legt die Failoverrichtlinie einer Failovergruppe auf "Automatisch" fest.</span><span class="sxs-lookup"><span data-stu-id="930fe-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="930fe-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="930fe-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="930fe-114">Legt die Failoverrichtlinie einer Failovergruppe auf "Manuell" fest, indem ein Piping in der Failovergruppe erfolgt.</span><span class="sxs-lookup"><span data-stu-id="930fe-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="930fe-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="930fe-115">PARAMETERS</span></span>

### <span data-ttu-id="930fe-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="930fe-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="930fe-117">Gibt an, ob Ausfälle auf dem sekundären Server ein automatisches Failover des schreibgeschützten Endpunkts auslösen sollen.</span><span class="sxs-lookup"><span data-stu-id="930fe-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="930fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="930fe-118">-DefaultProfile</span></span>
<span data-ttu-id="930fe-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="930fe-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="930fe-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="930fe-120">-FailoverGroupName</span></span>
<span data-ttu-id="930fe-121">Der Name der Azure SQL-Datenbank-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="930fe-121">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="930fe-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="930fe-122">-FailoverPolicy</span></span>
<span data-ttu-id="930fe-123">Die Failoverrichtlinie der Azure SQL-Datenbank-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="930fe-123">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="930fe-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="930fe-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="930fe-125">Intervall vor dem Beginn des automatischen Failovers, wenn ein Ausfall auf dem primären Server auftritt.</span><span class="sxs-lookup"><span data-stu-id="930fe-125">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="930fe-126">Dies weist darauf hin, SQL Azure-Datenbank vor Ablauf der Toleranzperiode keinen automatischen Failover initiiert.</span><span class="sxs-lookup"><span data-stu-id="930fe-126">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="930fe-127">Beachten Sie, dass ein Failovervorgang mit der Option "AllowDataLoss" aufgrund der Art der asynchronen Synchronisierung Datenverluste verursachen kann.</span><span class="sxs-lookup"><span data-stu-id="930fe-127">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

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

### <span data-ttu-id="930fe-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="930fe-128">-ResourceGroupName</span></span>
<span data-ttu-id="930fe-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="930fe-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="930fe-130">-ServerName</span><span class="sxs-lookup"><span data-stu-id="930fe-130">-ServerName</span></span>
<span data-ttu-id="930fe-131">Der Name des primären Azure SQL Datenbankservers der Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="930fe-131">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="930fe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="930fe-132">CommonParameters</span></span>
<span data-ttu-id="930fe-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="930fe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="930fe-134">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="930fe-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="930fe-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="930fe-135">INPUTS</span></span>

### <span data-ttu-id="930fe-136">System.String</span><span class="sxs-lookup"><span data-stu-id="930fe-136">System.String</span></span>

## <span data-ttu-id="930fe-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="930fe-137">OUTPUTS</span></span>

### <span data-ttu-id="930fe-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="930fe-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="930fe-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="930fe-139">NOTES</span></span>

## <span data-ttu-id="930fe-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="930fe-140">RELATED LINKS</span></span>

[<span data-ttu-id="930fe-141">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="930fe-141">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="930fe-142">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="930fe-142">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="930fe-143">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="930fe-143">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="930fe-144">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="930fe-144">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="930fe-145">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="930fe-145">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="930fe-146">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="930fe-146">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="930fe-147">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="930fe-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
