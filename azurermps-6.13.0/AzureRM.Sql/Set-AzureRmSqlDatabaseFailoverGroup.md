---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 98a6ceafed2c7c62301c63ff1c8b3028c46e1201
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480054"
---
# <span data-ttu-id="ec331-101">Set-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ec331-101">Set-AzureRmSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="ec331-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec331-102">SYNOPSIS</span></span>
<span data-ttu-id="ec331-103">Ändert die Konfiguration einer Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ec331-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec331-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec331-104">SYNTAX</span></span>

```
Set-AzureRmSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec331-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec331-105">DESCRIPTION</span></span>
<span data-ttu-id="ec331-106">Mit diesem Befehl wird die Konfiguration einer Azure SQL-Daten Bank Failover-Gruppe geändert.</span><span class="sxs-lookup"><span data-stu-id="ec331-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="ec331-107">Der primäre Server der failovergruppe sollte verwendet werden, um den Befehl auszuführen.</span><span class="sxs-lookup"><span data-stu-id="ec331-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="ec331-108">Verwenden Sie stattdessen "Add-AzureRmSqlDatabaseToFailoverGroup" und "Remove-AzureRmSqlDatabaseFromFailoverGroup", um den Satz von Datenbanken in der Gruppe zu steuern.</span><span class="sxs-lookup"><span data-stu-id="ec331-108">To control the set of databases in the group, use 'Add-AzureRmSqlDatabaseToFailoverGroup' and 'Remove-AzureRmSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="ec331-109">Während der Vorschau des Features "failovergruppen" werden nur Werte, die größer oder gleich 1 Stunde sind, für den "-GracePeriodWithDataLossHours"-Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec331-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="ec331-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec331-110">EXAMPLES</span></span>

### <span data-ttu-id="ec331-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ec331-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="ec331-112">Legt die Failover-Richtlinie einer failovergruppe auf "automatisch" fest.</span><span class="sxs-lookup"><span data-stu-id="ec331-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="ec331-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ec331-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzureRmSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzureRmSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="ec331-114">Legt die Failover-Richtlinie einer failovergruppe auf "manuell" durch Verrohrung in der Gruppe Failover fest.</span><span class="sxs-lookup"><span data-stu-id="ec331-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="ec331-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec331-115">PARAMETERS</span></span>

### <span data-ttu-id="ec331-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="ec331-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="ec331-117">Ob Ausfälle auf dem sekundären Server ein automatisches Failover des schreibgeschützten Endpunkts auslösen sollten.</span><span class="sxs-lookup"><span data-stu-id="ec331-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span> <span data-ttu-id="ec331-118">Dieses Feature wird noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ec331-118">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="ec331-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec331-119">-DefaultProfile</span></span>
<span data-ttu-id="ec331-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ec331-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec331-121">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="ec331-121">-FailoverGroupName</span></span>
<span data-ttu-id="ec331-122">Der Name der Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ec331-122">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="ec331-123">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="ec331-123">-FailoverPolicy</span></span>
<span data-ttu-id="ec331-124">Die Failover-Richtlinie der Azure SQL-Datenbankfailover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="ec331-124">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="ec331-125">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="ec331-125">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="ec331-126">Das Intervall vor dem automatischen Failover wird initiiert, wenn ein Ausfall auf dem primären Server auftritt.</span><span class="sxs-lookup"><span data-stu-id="ec331-126">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="ec331-127">Dies zeigt an, dass Azure SQL-Datenbank kein automatisches Failover initiiert, bevor der Kulanzzeitraum abläuft.</span><span class="sxs-lookup"><span data-stu-id="ec331-127">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="ec331-128">Bitte beachten Sie, dass der Failover-Vorgang mit der Option AllowDataLoss aufgrund der Art der asynchronen Synchronisierung zu Datenverlusten führen kann.</span><span class="sxs-lookup"><span data-stu-id="ec331-128">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

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

### <span data-ttu-id="ec331-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec331-129">-ResourceGroupName</span></span>
<span data-ttu-id="ec331-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ec331-130">The name of the resource group.</span></span>

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

### <span data-ttu-id="ec331-131">-Servername</span><span class="sxs-lookup"><span data-stu-id="ec331-131">-ServerName</span></span>
<span data-ttu-id="ec331-132">Der Name des primären Azure SQL-Datenbankservers der Gruppe "Failover".</span><span class="sxs-lookup"><span data-stu-id="ec331-132">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="ec331-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec331-133">CommonParameters</span></span>
<span data-ttu-id="ec331-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec331-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec331-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec331-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec331-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec331-136">INPUTS</span></span>

### <span data-ttu-id="ec331-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ec331-137">System.String</span></span>

## <span data-ttu-id="ec331-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec331-138">OUTPUTS</span></span>

### <span data-ttu-id="ec331-139">Microsoft. Azure. Commands. SQL. failovergroup. Model. AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="ec331-139">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="ec331-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec331-140">NOTES</span></span>

## <span data-ttu-id="ec331-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec331-141">RELATED LINKS</span></span>

[<span data-ttu-id="ec331-142">Neu – AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ec331-142">New-AzureRmSqlDatabaseFailoverGroup</span></span>](./New-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ec331-143">Get-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ec331-143">Get-AzureRmSqlDatabaseFailoverGroup</span></span>](./Get-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ec331-144">Add-AzureRmSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ec331-144">Add-AzureRmSqlDatabaseToFailoverGroup</span></span>](./Add-AzureRmSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="ec331-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ec331-145">Remove-AzureRmSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="ec331-146">Switch-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ec331-146">Switch-AzureRmSqlDatabaseFailoverGroup</span></span>](./Switch-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ec331-147">Remove-AzureRmSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="ec331-147">Remove-AzureRmSqlDatabaseFailoverGroup</span></span>](./Remove-AzureRmSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="ec331-148">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="ec331-148">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
