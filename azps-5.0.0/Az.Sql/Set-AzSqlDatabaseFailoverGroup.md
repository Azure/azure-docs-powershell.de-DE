---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 8b78cfc7a2934b4670702562941ea0e00c2a70c8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179991"
---
# <span data-ttu-id="ded28-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ded28-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="ded28-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ded28-102">SYNOPSIS</span></span>
<span data-ttu-id="ded28-103">Ändert die Konfiguration einer Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ded28-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="ded28-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ded28-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ded28-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ded28-105">DESCRIPTION</span></span>
<span data-ttu-id="ded28-106">Mit diesem Befehl wird die Konfiguration einer Azure SQL-Daten Bank Failover-Gruppe geändert.</span><span class="sxs-lookup"><span data-stu-id="ded28-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="ded28-107">Der primäre Server der failovergruppe sollte verwendet werden, um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ded28-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="ded28-108">Verwenden Sie stattdessen "Add-AzSqlDatabaseToFailoverGroup" und "Remove-AzSqlDatabaseFromFailoverGroup", um den Satz von Datenbanken in der Gruppe zu steuern.</span><span class="sxs-lookup"><span data-stu-id="ded28-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="ded28-109">Während der Vorschau des Features "failovergruppen" werden nur Werte, die größer oder gleich 1 Stunde sind, für den "-GracePeriodWithDataLossHours"-Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ded28-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="ded28-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ded28-110">EXAMPLES</span></span>

### <span data-ttu-id="ded28-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ded28-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="ded28-112">Legt die Failover-Richtlinie einer failovergruppe auf "automatisch" fest.</span><span class="sxs-lookup"><span data-stu-id="ded28-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="ded28-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ded28-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="ded28-114">Legt die Failover-Richtlinie einer failovergruppe auf "manuell" durch Verrohrung in der Gruppe Failover fest.</span><span class="sxs-lookup"><span data-stu-id="ded28-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="ded28-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ded28-115">PARAMETERS</span></span>

### <span data-ttu-id="ded28-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="ded28-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="ded28-117">Ob Ausfälle auf dem sekundären Server ein automatisches Failover des schreibgeschützten Endpunkts auslösen sollten.</span><span class="sxs-lookup"><span data-stu-id="ded28-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="ded28-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ded28-118">-DefaultProfile</span></span>
<span data-ttu-id="ded28-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ded28-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ded28-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="ded28-120">-FailoverGroupName</span></span>
<span data-ttu-id="ded28-121">Der Name der Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ded28-121">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="ded28-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="ded28-122">-FailoverPolicy</span></span>
<span data-ttu-id="ded28-123">Die Failover-Richtlinie der Azure SQL-Datenbankfailover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ded28-123">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="ded28-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="ded28-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="ded28-125">Das Intervall vor dem automatischen Failover wird initiiert, wenn ein Ausfall auf dem primären Server auftritt.</span><span class="sxs-lookup"><span data-stu-id="ded28-125">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="ded28-126">Dies zeigt an, dass Azure SQL-Datenbank kein automatisches Failover initiiert, bevor der Kulanzzeitraum abläuft.</span><span class="sxs-lookup"><span data-stu-id="ded28-126">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="ded28-127">Bitte beachten Sie, dass der Failover-Vorgang mit der Option AllowDataLoss aufgrund der Art der asynchronen Synchronisierung zu Datenverlusten führen kann.</span><span class="sxs-lookup"><span data-stu-id="ded28-127">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

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

### <span data-ttu-id="ded28-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ded28-128">-ResourceGroupName</span></span>
<span data-ttu-id="ded28-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ded28-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="ded28-130">-Servername</span><span class="sxs-lookup"><span data-stu-id="ded28-130">-ServerName</span></span>
<span data-ttu-id="ded28-131">Der Name des primären Azure SQL-Datenbankservers der Gruppe "Failover".</span><span class="sxs-lookup"><span data-stu-id="ded28-131">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="ded28-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ded28-132">CommonParameters</span></span>
<span data-ttu-id="ded28-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ded28-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ded28-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ded28-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ded28-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ded28-135">INPUTS</span></span>

### <span data-ttu-id="ded28-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ded28-136">System.String</span></span>

## <span data-ttu-id="ded28-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ded28-137">OUTPUTS</span></span>

### <span data-ttu-id="ded28-138">Microsoft. Azure. Commands. SQL. failovergroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="ded28-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="ded28-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="ded28-139">NOTES</span></span>

## <span data-ttu-id="ded28-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ded28-140">RELATED LINKS</span></span>

[<span data-ttu-id="ded28-141">Neu – AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ded28-141">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ded28-142">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ded28-142">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ded28-143">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ded28-143">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="ded28-144">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ded28-144">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="ded28-145">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ded28-145">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ded28-146">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ded28-146">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ded28-147">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="ded28-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
