---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: d713675e3e73f32a4579d801a4dc1577cebd4cf0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458379"
---
# <span data-ttu-id="c48fb-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c48fb-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="c48fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c48fb-102">SYNOPSIS</span></span>
<span data-ttu-id="c48fb-103">Schaltet eine sekundäre Datenbank als primäre Datenbank um, um den Failover zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="c48fb-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="c48fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c48fb-104">SYNTAX</span></span>

### <span data-ttu-id="c48fb-105">NoOptionsSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c48fb-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c48fb-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="c48fb-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c48fb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c48fb-107">DESCRIPTION</span></span>
<span data-ttu-id="c48fb-108">Das **Cmdlet "Set-AzSqlDatabaseSecondary"** schaltet eine sekundäre Datenbank als primäre Datenbank um, um den Failover zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="c48fb-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="c48fb-109">Dieses Cmdlet ist als allgemeiner Konfigurationsbefehl konzipiert, ist aber derzeit auf das Initiieren des Failovers beschränkt.</span><span class="sxs-lookup"><span data-stu-id="c48fb-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="c48fb-110">Geben Sie den *Parameter "AllowDataLoss"* an, um einen Failover bei einem Ausfall zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="c48fb-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="c48fb-111">Sie müssen diesen Parameter nicht angeben, wenn Sie einen geplanten Vorgang wie einen Wiederherstellungsdrill ausführen.</span><span class="sxs-lookup"><span data-stu-id="c48fb-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="c48fb-112">Im zweiten Fall wird die sekundäre Datenbank vor dem Wechsel mit dem primären Datenbank synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="c48fb-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="c48fb-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c48fb-113">EXAMPLES</span></span>

### <span data-ttu-id="c48fb-114">Beispiel 1: Initiieren eines geplanten Failovers</span><span class="sxs-lookup"><span data-stu-id="c48fb-114">Example 1: Initiate a planned failover</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="c48fb-115">Beispiel 2: Initiieren eines erzwungenen Failovers (mit potenziellem Datenverlust)</span><span class="sxs-lookup"><span data-stu-id="c48fb-115">Example 2: Initiate a forced failover (with potential data loss)</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="c48fb-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c48fb-116">PARAMETERS</span></span>

### <span data-ttu-id="c48fb-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="c48fb-117">-AllowDataLoss</span></span>
<span data-ttu-id="c48fb-118">Gibt an, dass dieser Failovervorgang Datenverlust zulässt.</span><span class="sxs-lookup"><span data-stu-id="c48fb-118">Indicates that this failover operation permits data loss.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48fb-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c48fb-119">-AsJob</span></span>
<span data-ttu-id="c48fb-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="c48fb-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48fb-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="c48fb-121">-DatabaseName</span></span>
<span data-ttu-id="c48fb-122">Gibt den Namen des Azure SQL Database Secondary an.</span><span class="sxs-lookup"><span data-stu-id="c48fb-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="c48fb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c48fb-123">-DefaultProfile</span></span>
<span data-ttu-id="c48fb-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c48fb-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c48fb-125">-Failover</span><span class="sxs-lookup"><span data-stu-id="c48fb-125">-Failover</span></span>
<span data-ttu-id="c48fb-126">Gibt an, dass es sich bei diesem Vorgang um einen Failover handelt.</span><span class="sxs-lookup"><span data-stu-id="c48fb-126">Indicates that this operation is a failover.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByFailoverParams
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48fb-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c48fb-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="c48fb-128">Gibt den Namen der Ressourcengruppe an, der der Azure SQL zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c48fb-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c48fb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c48fb-129">-ResourceGroupName</span></span>
<span data-ttu-id="c48fb-130">Gibt den Namen der Ressourcengruppe an, der die Azure SQL Database Secondary zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c48fb-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="c48fb-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c48fb-131">-ServerName</span></span>
<span data-ttu-id="c48fb-132">Gibt den Namen des SQL Server an, das die sekundäre Azure SQL hostet.</span><span class="sxs-lookup"><span data-stu-id="c48fb-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="c48fb-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c48fb-133">-Confirm</span></span>
<span data-ttu-id="c48fb-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c48fb-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48fb-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c48fb-135">-WhatIf</span></span>
<span data-ttu-id="c48fb-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c48fb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c48fb-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c48fb-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c48fb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c48fb-138">CommonParameters</span></span>
<span data-ttu-id="c48fb-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c48fb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c48fb-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c48fb-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c48fb-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c48fb-141">INPUTS</span></span>

### <span data-ttu-id="c48fb-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c48fb-142">System.String</span></span>

## <span data-ttu-id="c48fb-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c48fb-143">OUTPUTS</span></span>

### <span data-ttu-id="c48fb-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="c48fb-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="c48fb-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c48fb-145">NOTES</span></span>

## <span data-ttu-id="c48fb-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c48fb-146">RELATED LINKS</span></span>

[<span data-ttu-id="c48fb-147">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c48fb-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="c48fb-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="c48fb-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="c48fb-149">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="c48fb-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
