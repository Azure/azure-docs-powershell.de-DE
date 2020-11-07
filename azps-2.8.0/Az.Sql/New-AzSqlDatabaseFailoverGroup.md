---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 43723efe8e04a7913ca84f08927afd4757102801
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93826023"
---
# <span data-ttu-id="79535-101">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="79535-101">New-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="79535-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="79535-102">SYNOPSIS</span></span>
<span data-ttu-id="79535-103">Mit diesem Befehl wird eine neue Azure SQL-Daten Bank Failover-Gruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="79535-103">This command creates a new Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="79535-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="79535-104">SYNTAX</span></span>

```
New-AzSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79535-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="79535-105">DESCRIPTION</span></span>
<span data-ttu-id="79535-106">Erstellt eine neue Azure SQL-Daten Bank Failover-Gruppe für die angegebenen Server.</span><span class="sxs-lookup"><span data-stu-id="79535-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>
<span data-ttu-id="79535-107">Zwei Azure SQL-Datenbank-TDS-Endpunkte werden in FailoverGroupName. SqlDatabaseDnsSuffix (beispielsweise FailoverGroupName.Database.Windows.net) und FailoverGroupName. Secondary. SqlDatabaseDnsSuffix erstellt.</span><span class="sxs-lookup"><span data-stu-id="79535-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="79535-108">Diese Endpunkte können verwendet werden, um eine Verbindung mit den primären und sekundären Servern in der Gruppe Failover herzustellen.</span><span class="sxs-lookup"><span data-stu-id="79535-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="79535-109">Wenn der primäre Server von einem Ausfall betroffen ist, wird das automatische Failover der Endpunkte und Datenbanken wie von der Failover-Richtlinie und dem Kulanzzeitraum der failovergruppe diktiert ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="79535-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>
<span data-ttu-id="79535-110">Neu erstellte Failovercluster enthalten keine Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="79535-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="79535-111">Verwenden Sie die Cmdlets "Add-AzSqlDatabaseToFailoverGroup" und "Remove-AzSqlDatabaseFromFailoverGroup", um die Gruppe von Datenbanken in einer failovergruppe zu steuern.</span><span class="sxs-lookup"><span data-stu-id="79535-111">To control the set of databases in a Failover Group, use the 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' cmdlets.</span></span>
<span data-ttu-id="79535-112">Nur Werte, die größer oder gleich 1 Stunde sind, werden für den "-GracePeriodWithDataLossHours"-Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="79535-112">Only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="79535-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="79535-113">EXAMPLES</span></span>

### <span data-ttu-id="79535-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="79535-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="79535-115">Mit diesem Befehl wird eine neue Failover-Gruppe mit der Failover-Richtlinie "automatisch" für zwei Server in der gleichen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="79535-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="79535-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="79535-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="79535-117">Mit diesem Befehl wird eine neue Failover-Gruppe mit der Failover-Richtlinie "Manual" für zwei Server in verschiedenen Ressourcengruppen erstellt.</span><span class="sxs-lookup"><span data-stu-id="79535-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="79535-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="79535-118">PARAMETERS</span></span>

### <span data-ttu-id="79535-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="79535-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="79535-120">Ob ein Ausfall auf dem sekundären Server ein automatisches Failover des schreibgeschützten Endpunkts auslösen soll.</span><span class="sxs-lookup"><span data-stu-id="79535-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="79535-121">Dieses Feature wird noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="79535-121">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="79535-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79535-122">-DefaultProfile</span></span>
<span data-ttu-id="79535-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="79535-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79535-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="79535-124">-FailoverGroupName</span></span>
<span data-ttu-id="79535-125">Der Name der zu erstellende Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="79535-125">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="79535-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="79535-126">-FailoverPolicy</span></span>
<span data-ttu-id="79535-127">Die Failover-Richtlinie der Azure SQL-Datenbankfailover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="79535-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="79535-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="79535-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="79535-129">Das Intervall vor dem automatischen Failover wird initiiert, wenn ein Ausfall auf dem primären Server auftritt und ein Failover ohne Datenverlust nicht abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="79535-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="79535-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79535-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="79535-131">Der Name der sekundären Ressourcengruppe der Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="79535-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="79535-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="79535-132">-PartnerServerName</span></span>
<span data-ttu-id="79535-133">Der Name des sekundären Servers der Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="79535-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="79535-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79535-134">-ResourceGroupName</span></span>
<span data-ttu-id="79535-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="79535-135">The name of the resource group.</span></span>

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

### <span data-ttu-id="79535-136">-Servername</span><span class="sxs-lookup"><span data-stu-id="79535-136">-ServerName</span></span>
<span data-ttu-id="79535-137">Der Name des primären Azure SQL-Datenbankservers der Gruppe "Failover".</span><span class="sxs-lookup"><span data-stu-id="79535-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="79535-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79535-138">CommonParameters</span></span>
<span data-ttu-id="79535-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79535-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79535-140">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79535-140">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79535-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="79535-141">INPUTS</span></span>

### <span data-ttu-id="79535-142">System. String</span><span class="sxs-lookup"><span data-stu-id="79535-142">System.String</span></span>

## <span data-ttu-id="79535-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="79535-143">OUTPUTS</span></span>

### <span data-ttu-id="79535-144">Microsoft. Azure. Commands. SQL. failovergroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="79535-144">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="79535-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="79535-145">NOTES</span></span>

## <span data-ttu-id="79535-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="79535-146">RELATED LINKS</span></span>

[<span data-ttu-id="79535-147">Satz-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="79535-147">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="79535-148">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="79535-148">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="79535-149">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="79535-149">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="79535-150">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="79535-150">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="79535-151">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="79535-151">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="79535-152">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="79535-152">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="79535-153">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="79535-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
