---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 71f4796e33ec512f9d0aa2eb27f78ba615eefef1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476465"
---
# <span data-ttu-id="7ef67-101">New-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7ef67-101">New-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="7ef67-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ef67-102">SYNOPSIS</span></span>
<span data-ttu-id="7ef67-103">Mit diesem Befehl wird eine neue Azure SQL-Daten Bank Failover-Gruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="7ef67-103">This command creates a new Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ef67-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ef67-104">SYNTAX</span></span>

```
New-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> -FailoverGroupName <String>
 [-PartnerResourceGroupName <String>] -PartnerServerName <String> [-FailoverPolicy <FailoverPolicy>]
 [-GracePeriodWithDataLossHours <Int32>] [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ef67-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ef67-105">DESCRIPTION</span></span>
<span data-ttu-id="7ef67-106">Erstellt eine neue Azure SQL-Daten Bank Failover-Gruppe für die angegebenen Server.</span><span class="sxs-lookup"><span data-stu-id="7ef67-106">Creates a new Azure SQL Database Failover Group for the specified servers.</span></span>

<span data-ttu-id="7ef67-107">Zwei Azure SQL-Datenbank-TDS-Endpunkte werden in FailoverGroupName. SqlDatabaseDnsSuffix (beispielsweise FailoverGroupName.Database.Windows.net) und FailoverGroupName. Secondary. SqlDatabaseDnsSuffix erstellt.</span><span class="sxs-lookup"><span data-stu-id="7ef67-107">Two Azure SQL Database TDS endpoints are created at FailoverGroupName.SqlDatabaseDnsSuffix (for example, FailoverGroupName.database.windows.net) and FailoverGroupName.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="7ef67-108">Diese Endpunkte können verwendet werden, um eine Verbindung mit den primären und sekundären Servern in der Gruppe Failover herzustellen.</span><span class="sxs-lookup"><span data-stu-id="7ef67-108">These endpoints may be used to connect to the primary and secondary servers in the Failover Group, respectively.</span></span> <span data-ttu-id="7ef67-109">Wenn der primäre Server von einem Ausfall betroffen ist, wird das automatische Failover der Endpunkte und Datenbanken wie von der Failover-Richtlinie und dem Kulanzzeitraum der failovergruppe diktiert ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="7ef67-109">If the primary server is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="7ef67-110">Neu erstellte Failovercluster enthalten keine Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="7ef67-110">Newly created Failover Groups do not contain any databases.</span></span> <span data-ttu-id="7ef67-111">Verwenden Sie die Cmdlets "Add-AzureRmSqlDatabaseToFailoverGroup" und "Remove-AzureRmSqlDatabaseFromFailoverGroup", um die Gruppe von Datenbanken in einer failovergruppe zu steuern.</span><span class="sxs-lookup"><span data-stu-id="7ef67-111">To control the set of databases in a Failover Group, use the 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' cmdlets.</span></span>

<span data-ttu-id="7ef67-112">Während der Vorschau des Features "failovergruppen" werden nur Werte, die größer oder gleich 1 Stunde sind, für den "-GracePeriodWithDataLossHours"-Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7ef67-112">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="7ef67-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ef67-113">EXAMPLES</span></span>

### <span data-ttu-id="7ef67-114">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7ef67-114">Example 1</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -PartnerServerName secondaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="7ef67-115">Mit diesem Befehl wird eine neue Failover-Gruppe mit der Failover-Richtlinie "automatisch" für zwei Server in der gleichen Ressourcengruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="7ef67-115">This command creates a new Failover Group with failover policy 'Automatic' for two servers in the same resource group.</span></span>

### <span data-ttu-id="7ef67-116">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7ef67-116">Example 2</span></span>
```
C:\> $failoverGroup = New-AzureRMSqlDatabaseFailoverGroup -ResourceGroupName rg1 -ServerName primaryserver -PartnerResourceGroupName rg2 -PartnerServerName secondaryserver1 -FailoverGroupName fg -FailoverPolicy Manual
```

<span data-ttu-id="7ef67-117">Mit diesem Befehl wird eine neue Failover-Gruppe mit der Failover-Richtlinie "Manual" für zwei Server in verschiedenen Ressourcengruppen erstellt.</span><span class="sxs-lookup"><span data-stu-id="7ef67-117">This command creates a new Failover Group with failover policy 'Manual' for two servers in different resource groups.</span></span>

## <span data-ttu-id="7ef67-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ef67-118">PARAMETERS</span></span>

### <span data-ttu-id="7ef67-119">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="7ef67-119">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="7ef67-120">Ob ein Ausfall auf dem sekundären Server ein automatisches Failover des schreibgeschützten Endpunkts auslösen soll.</span><span class="sxs-lookup"><span data-stu-id="7ef67-120">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="7ef67-121">Dieses Feature wird noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7ef67-121">This feature is not yet supported.</span></span>

```yaml
Type: AllowReadOnlyFailoverToPrimary
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ef67-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ef67-122">-DefaultProfile</span></span>
<span data-ttu-id="7ef67-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7ef67-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ef67-124">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="7ef67-124">-FailoverGroupName</span></span>
<span data-ttu-id="7ef67-125">Der Name der zu erstellende Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="7ef67-125">The name of the Azure SQL Database Failover Group to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ef67-126">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="7ef67-126">-FailoverPolicy</span></span>
<span data-ttu-id="7ef67-127">Die Failover-Richtlinie der Azure SQL-Datenbankfailover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="7ef67-127">The failover policy of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: FailoverPolicy
Parameter Sets: (All)
Aliases:
Accepted values: Automatic, Manual

Required: False
Position: Named
Default value: Automatic
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ef67-128">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="7ef67-128">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="7ef67-129">Das Intervall vor dem automatischen Failover wird initiiert, wenn ein Ausfall auf dem primären Server auftritt und ein Failover ohne Datenverlust nicht abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="7ef67-129">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ef67-130">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ef67-130">-PartnerResourceGroupName</span></span>
<span data-ttu-id="7ef67-131">Der Name der sekundären Ressourcengruppe der Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="7ef67-131">The name of the secondary resource group of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ef67-132">-PartnerServerName</span><span class="sxs-lookup"><span data-stu-id="7ef67-132">-PartnerServerName</span></span>
<span data-ttu-id="7ef67-133">Der Name des sekundären Servers der Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="7ef67-133">The name of the secondary server of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7ef67-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ef67-134">-ResourceGroupName</span></span>
<span data-ttu-id="7ef67-135">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="7ef67-135">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef67-136">-Servername</span><span class="sxs-lookup"><span data-stu-id="7ef67-136">-ServerName</span></span>
<span data-ttu-id="7ef67-137">Der Name des primären Azure SQL-Datenbankservers der Gruppe "Failover".</span><span class="sxs-lookup"><span data-stu-id="7ef67-137">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ef67-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ef67-138">CommonParameters</span></span>
<span data-ttu-id="7ef67-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ef67-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ef67-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ef67-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ef67-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ef67-141">INPUTS</span></span>

### <span data-ttu-id="7ef67-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7ef67-142">System.String</span></span>

## <span data-ttu-id="7ef67-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ef67-143">OUTPUTS</span></span>

### <span data-ttu-id="7ef67-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="7ef67-144">System.Object</span></span>

## <span data-ttu-id="7ef67-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ef67-145">NOTES</span></span>

## <span data-ttu-id="7ef67-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ef67-146">RELATED LINKS</span></span>

[<span data-ttu-id="7ef67-147">Satz-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7ef67-147">Set-AzureRmSqlDatabaseFailoverGroup</span></span>](./Set-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7ef67-148">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7ef67-148">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7ef67-149">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7ef67-149">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="7ef67-150">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7ef67-150">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="7ef67-151">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7ef67-151">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7ef67-152">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="7ef67-152">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="7ef67-153">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="7ef67-153">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
