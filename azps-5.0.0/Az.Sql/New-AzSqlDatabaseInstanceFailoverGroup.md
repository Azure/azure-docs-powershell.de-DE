---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/new-Azsqldatabaseinstancefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlDatabaseInstanceFailoverGroup.md
ms.openlocfilehash: 7a893099a81225f165fc6fc56c6ba3fd6cfaec3a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177190"
---
# <span data-ttu-id="4d80d-101">New-AzSqlDatabaseInstanceFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4d80d-101">New-AzSqlDatabaseInstanceFailoverGroup</span></span>

## <span data-ttu-id="4d80d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4d80d-102">SYNOPSIS</span></span>
<span data-ttu-id="4d80d-103">Mit diesem Befehl wird eine neue Azure SQL-Datenbankinstanz-Failover-Gruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="4d80d-103">This command creates a new Azure SQL Database Instance Failover Group.</span></span>

## <span data-ttu-id="4d80d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4d80d-104">SYNTAX</span></span>

```
New-AzSqlDatabaseInstanceFailoverGroup [-Name] <String> [-PartnerResourceGroupName <String>]
 -PartnerRegion <String> -PrimaryManagedInstanceName <String> -PartnerManagedInstanceName <String>
 [-PartnerSubscriptionId <String>] [-FailoverPolicy <String>] [-GracePeriodWithDataLossHours <Int32>]
 [-AllowReadOnlyFailoverToPrimary <String>] [-ResourceGroupName] <String> [-Location] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d80d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4d80d-105">DESCRIPTION</span></span>
<span data-ttu-id="4d80d-106">Erstellt eine neue Azure SQL-Datenbankinstanz-failovergruppe zwischen den angegebenen Bereichen mit dem bekannten verwalteten Instanzen Paar.</span><span class="sxs-lookup"><span data-stu-id="4d80d-106">Creates a new Azure SQL Database Instance Failover Group between the specified regions with the noted Managed Instance pair.</span></span>

<span data-ttu-id="4d80d-107">Zwei Azure SQL-Datenbank-TDS-Endpunkte werden unter Name. SqlDatabaseDnsSuffix (beispielsweise Name.Database.Windows.net) und Name. Secondary. SqlDatabaseDnsSuffix erstellt.</span><span class="sxs-lookup"><span data-stu-id="4d80d-107">Two Azure SQL Database TDS endpoints are created at Name.SqlDatabaseDnsSuffix (for example, Name.database.windows.net) and Name.secondary.SqlDatabaseDnsSuffix.</span></span> <span data-ttu-id="4d80d-108">Diese Endpunkte können verwendet werden, um eine Verbindung mit den primären und sekundären Regionen der failovergruppe herzustellen.</span><span class="sxs-lookup"><span data-stu-id="4d80d-108">These endpoints may be used to connect to the primary and secondary regions of the Failover Group, respectively.</span></span> <span data-ttu-id="4d80d-109">Wenn der primäre Bereich von einem Ausfall betroffen ist, wird das automatische Failover der Endpunkte und Datenbanken wie von der Failover-Richtlinie und dem Kulanzzeitraum der Instanz-failovergruppe diktiert ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="4d80d-109">If the primary region is affected by an outage, automatic failover of the endpoints and databases will be triggered as dictated by the Instance Failover Group's failover policy and grace period.</span></span>

<span data-ttu-id="4d80d-110">Während der Vorschau des Features "Instanzen-failovergruppen" werden nur Werte, die größer oder gleich 1 Stunde sind, für den "-GracePeriodWithDataLossHours"-Parameter unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4d80d-110">During preview of the Instance Failover Groups feature, only values greater than or equal to 1 hour are supported for the '-GracePeriodWithDataLossHours' parameter.</span></span>

## <span data-ttu-id="4d80d-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4d80d-111">EXAMPLES</span></span>

### <span data-ttu-id="4d80d-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4d80d-112">Example 1</span></span>
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

<span data-ttu-id="4d80d-113">Mit diesem Befehl wird eine neue Instanz-Failover-Gruppe mit der Failover-Richtlinie "automatisch" für das Paar für verwaltete Instanzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="4d80d-113">This command creates a new Instance Failover Group with failover policy 'Automatic' for the Managed Instance pair.</span></span>

### <span data-ttu-id="4d80d-114">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4d80d-114">Example 2</span></span>
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

<span data-ttu-id="4d80d-115">Mit diesem Befehl wird eine neue Instanz-Failover-Gruppe mit der Failover-Richtlinie "Manual" für das Paar für verwaltete Instanzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="4d80d-115">This command creates a new Instance Failover Group with failover policy 'Manual' for the Managed Instance pair.</span></span>

### <span data-ttu-id="4d80d-116">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="4d80d-116">Example 3</span></span>

<span data-ttu-id="4d80d-117">Mit diesem Befehl wird eine neue Azure SQL-Datenbankinstanz-Failover-Gruppe erstellt.</span><span class="sxs-lookup"><span data-stu-id="4d80d-117">This command creates a new Azure SQL Database Instance Failover Group.</span></span> <span data-ttu-id="4d80d-118">automatisch</span><span class="sxs-lookup"><span data-stu-id="4d80d-118">(autogenerated)</span></span>

```powershell
<!-- Aladdin Generated Example --> 
New-AzSqlDatabaseInstanceFailoverGroup -FailoverPolicy Automatic -GracePeriodWithDataLossHours 1 -Location location -Name fgName -PartnerManagedInstanceName $partnerManagedInstance.Name -PartnerRegion $partnerRegion -PartnerResourceGroupName rg2 -PrimaryManagedInstanceName $managedInstance.Name -ResourceGroupName rg
```

## <span data-ttu-id="4d80d-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d80d-119">PARAMETERS</span></span>

### <span data-ttu-id="4d80d-120">-AllowReadOnlyFailoverToPrimary</span><span class="sxs-lookup"><span data-stu-id="4d80d-120">-AllowReadOnlyFailoverToPrimary</span></span>
<span data-ttu-id="4d80d-121">Ob ein Ausfall auf dem sekundären Server ein automatisches Failover des schreibgeschützten Endpunkts auslösen soll.</span><span class="sxs-lookup"><span data-stu-id="4d80d-121">Whether an outage on the secondary server should trigger automatic failover of the read-only endpoint.</span></span>
<span data-ttu-id="4d80d-122">Dieses Feature wird noch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="4d80d-122">This feature is not yet supported.</span></span>

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

### <span data-ttu-id="4d80d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d80d-123">-DefaultProfile</span></span>
<span data-ttu-id="4d80d-124">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4d80d-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d80d-125">-FailoverPolicy</span><span class="sxs-lookup"><span data-stu-id="4d80d-125">-FailoverPolicy</span></span>
<span data-ttu-id="4d80d-126">Die Failover-Richtlinie der Instanz-Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4d80d-126">The failover policy of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="4d80d-127">-GracePeriodWithDataLossHours</span><span class="sxs-lookup"><span data-stu-id="4d80d-127">-GracePeriodWithDataLossHours</span></span>
<span data-ttu-id="4d80d-128">Das Intervall vor dem automatischen Failover wird initiiert, wenn ein Ausfall auf dem primären Server auftritt und ein Failover ohne Datenverlust nicht abgeschlossen werden kann.</span><span class="sxs-lookup"><span data-stu-id="4d80d-128">Interval before automatic failover is initiated if an outage occurs on the primary server and failover cannot be completed without data loss.</span></span>

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

### <span data-ttu-id="4d80d-129">-Standort</span><span class="sxs-lookup"><span data-stu-id="4d80d-129">-Location</span></span>
<span data-ttu-id="4d80d-130">Der Name des lokalen Bereichs, aus dem die Gruppe der Instanz-Failover abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d80d-130">The name of the Local Region from which to retrieve the Instance Failover Group.</span></span>

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

### <span data-ttu-id="4d80d-131">-Name</span><span class="sxs-lookup"><span data-stu-id="4d80d-131">-Name</span></span>
<span data-ttu-id="4d80d-132">Der Name der zu erstellende Azure SQL-Daten Bank Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4d80d-132">The name of the Azure SQL Database Failover Group to create.</span></span>

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

### <span data-ttu-id="4d80d-133">-PartnerManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="4d80d-133">-PartnerManagedInstanceName</span></span>
<span data-ttu-id="4d80d-134">Der Name der verwalteten Instanz in der Partnerregion, die der Instanz-failovergruppe hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d80d-134">The name of the Managed Instance in the partner region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="4d80d-135">-PartnerRegion</span><span class="sxs-lookup"><span data-stu-id="4d80d-135">-PartnerRegion</span></span>
<span data-ttu-id="4d80d-136">Der Name des Partnerbereichs der Instanz-Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4d80d-136">The name of the partner region of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="4d80d-137">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d80d-137">-PartnerResourceGroupName</span></span>
<span data-ttu-id="4d80d-138">Der Name der sekundären Ressourcengruppe der Instanz-Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4d80d-138">The name of the secondary resource group of the Instance Failover Group.</span></span>

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

### <span data-ttu-id="4d80d-139">-PartnerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="4d80d-139">-PartnerSubscriptionId</span></span>
<span data-ttu-id="4d80d-140">Die Abonnement-ID der sekundären verwalteten Instanz der Instanz-Failover-Gruppe.</span><span class="sxs-lookup"><span data-stu-id="4d80d-140">The subscription id of the secondary Managed Instance of the Instance Failover Group.</span></span> <span data-ttu-id="4d80d-141">Dieser Parameter wird nur für das Abonnement übergreifende Setup benötigt.</span><span class="sxs-lookup"><span data-stu-id="4d80d-141">This parameter is only needed for cross-subscription setup</span></span>

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

### <span data-ttu-id="4d80d-142">-PrimaryManagedInstanceName</span><span class="sxs-lookup"><span data-stu-id="4d80d-142">-PrimaryManagedInstanceName</span></span>
<span data-ttu-id="4d80d-143">Der Name der verwalteten Instanz in der lokalen Region, die der Instanz-failovergruppe hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d80d-143">The name of the Managed Instance in the local region to be added to the Instance Failover Group.</span></span>

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

### <span data-ttu-id="4d80d-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4d80d-144">-ResourceGroupName</span></span>
<span data-ttu-id="4d80d-145">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4d80d-145">The name of the resource group.</span></span>

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

### <span data-ttu-id="4d80d-146">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4d80d-146">-Confirm</span></span>
<span data-ttu-id="4d80d-147">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4d80d-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d80d-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d80d-148">-WhatIf</span></span>
<span data-ttu-id="4d80d-149">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4d80d-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d80d-150">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d80d-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d80d-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d80d-151">CommonParameters</span></span>
<span data-ttu-id="4d80d-152">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d80d-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d80d-153">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4d80d-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d80d-154">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4d80d-154">INPUTS</span></span>

### <span data-ttu-id="4d80d-155">System. String</span><span class="sxs-lookup"><span data-stu-id="4d80d-155">System.String</span></span>

## <span data-ttu-id="4d80d-156">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4d80d-156">OUTPUTS</span></span>

### <span data-ttu-id="4d80d-157">Microsoft. Azure. Commands. SQL. InstanceFailoverGroup. Model. AzureSqlInstanceFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="4d80d-157">Microsoft.Azure.Commands.Sql.InstanceFailoverGroup.Model.AzureSqlInstanceFailoverGroupModel</span></span>

## <span data-ttu-id="4d80d-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="4d80d-158">NOTES</span></span>

## <span data-ttu-id="4d80d-159">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4d80d-159">RELATED LINKS</span></span>
