---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/set-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 94f4448816bc7cf60272f602caafbf5be6f1a3f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940824"
---
# <span data-ttu-id="78869-101">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="78869-101">Set-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="78869-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78869-102">SYNOPSIS</span></span>
<span data-ttu-id="78869-103">Ändert die Konfiguration einer Azure SQL-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="78869-103">Modifies the configuration of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="78869-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78869-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String>
 [-FailoverPolicy <FailoverPolicy>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <AllowReadOnlyFailoverToPrimary>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78869-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78869-105">DESCRIPTION</span></span>
<span data-ttu-id="78869-106">Mit diesem Befehl wird die Konfiguration einer Azure SQL-Failovergruppe geändert.</span><span class="sxs-lookup"><span data-stu-id="78869-106">This command modifies the configuration of an Azure SQL Database Failover Group.</span></span>
<span data-ttu-id="78869-107">Der primäre Server der Failovergruppe sollte zum Ausführen des Befehls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78869-107">The Failover Group's primary server should be used to execute the command.</span></span>
<span data-ttu-id="78869-108">Um die Gruppe der Datenbanken in der Gruppe zu steuern, verwenden Sie stattdessen "Add-AzSqlDatabaseToFailoverGroup" und "Remove-AzSqlDatabaseFromFailoverGroup".</span><span class="sxs-lookup"><span data-stu-id="78869-108">To control the set of databases in the group, use 'Add-AzSqlDatabaseToFailoverGroup' and 'Remove-AzSqlDatabaseFromFailoverGroup' instead.</span></span>
<span data-ttu-id="78869-109">Während der Vorschau des Features Failovergruppen werden für den Parameter "-GracePeriodWithDataLossHours" nur Werte unterstützt, die größer als oder gleich 1 Stunde sind.</span><span class="sxs-lookup"><span data-stu-id="78869-109">During preview of the Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="78869-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="78869-110">EXAMPLES</span></span>

### <span data-ttu-id="78869-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="78869-111">Example 1</span></span>
```
PS C:\> $failoverGroup = Set-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1
```

<span data-ttu-id="78869-112">Legt die Failoverrichtlinie einer Failovergruppe auf "Automatisch" fest.</span><span class="sxs-lookup"><span data-stu-id="78869-112">Sets a Failover Group's failover policy to 'Automatic.'</span></span>

### <span data-ttu-id="78869-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="78869-113">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg | Set-AzSqlDatabaseFailoverGroup -FailoverPolicy Manual
```

<span data-ttu-id="78869-114">Legt die Failoverrichtlinie einer Failovergruppe durch Piping in der Failovergruppe auf "Manuell" fest.</span><span class="sxs-lookup"><span data-stu-id="78869-114">Sets a Failover Group's failover policy to 'Manual' by piping in the Failover Group.</span></span>

## <span data-ttu-id="78869-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="78869-115">PARAMETERS</span></span>

### <span data-ttu-id="78869-116">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="78869-116">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="78869-117">Gibt an, ob Ausfälle auf dem sekundären Server ein automatisches Failover des schreibgeschützten Endpunkts auslösen sollten.</span><span class="sxs-lookup"><span data-stu-id="78869-117">Whether outages on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>

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

### <span data-ttu-id="78869-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78869-118">-DefaultProfile</span></span>
<span data-ttu-id="78869-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="78869-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78869-120">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="78869-120">-FailoverGroupName</span></span>
<span data-ttu-id="78869-121">Der Name der Azure SQL-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="78869-121">The name of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="78869-122">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="78869-122">-FailoverPolicy</span></span>
<span data-ttu-id="78869-123">Die Failoverrichtlinie der Azure SQL Database Failover Group.</span><span class="sxs-lookup"><span data-stu-id="78869-123">The failover policy of the Azure SQL Database Failover Group.</span></span>

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

### <span data-ttu-id="78869-124">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="78869-124">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="78869-125">Intervall, bevor das automatische Failover initiiert wird, wenn ein Ausfall auf dem primären Server auftritt.</span><span class="sxs-lookup"><span data-stu-id="78869-125">Interval before automatic failover is initiated if an outage occurs on the primary server.</span></span> <span data-ttu-id="78869-126">Dies zeigt an, dass Azure SQL-Datenbank vor Ablauf der Nachfrist kein automatisches Failover initiiert.</span><span class="sxs-lookup"><span data-stu-id="78869-126">This indicates that Azure SQL Database will not initiate automatic failover before the grace period expires.</span></span> <span data-ttu-id="78869-127">Beachten Sie, dass ein Failovervorgang mit der Option AllowDataLoss aufgrund der asynchronen Synchronisierung zu Datenverlust führen kann.</span><span class="sxs-lookup"><span data-stu-id="78869-127">Please note that failover operation with AllowDataLoss option might cause data loss due to the nature of asynchronous synchronization.</span></span>

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

### <span data-ttu-id="78869-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78869-128">-ResourceGroupName</span></span>
<span data-ttu-id="78869-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="78869-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="78869-130">-Servername</span><span class="sxs-lookup"><span data-stu-id="78869-130">-ServerName</span></span>
<span data-ttu-id="78869-131">Der Name des primären Azure SQL Datenbankserver der Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="78869-131">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="78869-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78869-132">CommonParameters</span></span>
<span data-ttu-id="78869-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78869-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78869-134">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="78869-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78869-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="78869-135">INPUTS</span></span>

### <span data-ttu-id="78869-136">System.String</span><span class="sxs-lookup"><span data-stu-id="78869-136">System.String</span></span>

## <span data-ttu-id="78869-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="78869-137">OUTPUTS</span></span>

### <span data-ttu-id="78869-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="78869-138">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="78869-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="78869-139">NOTES</span></span>

## <span data-ttu-id="78869-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="78869-140">RELATED LINKS</span></span>

[<span data-ttu-id="78869-141">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="78869-141">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="78869-142">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="78869-142">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="78869-143">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="78869-143">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="78869-144">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="78869-144">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="78869-145">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="78869-145">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="78869-146">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="78869-146">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="78869-147">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="78869-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
