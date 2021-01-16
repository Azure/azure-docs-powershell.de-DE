---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: F9703508-DD4D-4D25-A7CA-7E3432B5DCA9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasesecondary
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseSecondary.md
ms.openlocfilehash: d713675e3e73f32a4579d801a4dc1577cebd4cf0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307616"
---
# <span data-ttu-id="d0e16-101">Set-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d0e16-101">Set-AzSqlDatabaseSecondary</span></span>

## <span data-ttu-id="d0e16-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0e16-102">SYNOPSIS</span></span>
<span data-ttu-id="d0e16-103">Schaltet eine sekundäre Datenbank als primäre Datenbank um, um den Failover zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="d0e16-103">Switches a secondary database to be primary in order to initiate failover.</span></span>

## <span data-ttu-id="d0e16-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0e16-104">SYNTAX</span></span>

### <span data-ttu-id="d0e16-105">NoOptionsSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d0e16-105">NoOptionsSet (Default)</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-AsJob]
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0e16-106">ByFailoverParams</span><span class="sxs-lookup"><span data-stu-id="d0e16-106">ByFailoverParams</span></span>
```
Set-AzSqlDatabaseSecondary [-DatabaseName] <String> -PartnerResourceGroupName <String> [-Failover]
 [-AllowDataLoss] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0e16-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0e16-107">DESCRIPTION</span></span>
<span data-ttu-id="d0e16-108">Das **Cmdlet "Set-AzSqlDatabaseSecondary"** schaltet eine sekundäre Datenbank als primäre Datenbank um, um den Failover zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="d0e16-108">The **Set-AzSqlDatabaseSecondary** cmdlet switches a secondary database to be primary in order to initiate failover.</span></span>
<span data-ttu-id="d0e16-109">Dieses Cmdlet ist als allgemeiner Konfigurationsbefehl konzipiert, ist aber derzeit auf das Initiieren des Failovers beschränkt.</span><span class="sxs-lookup"><span data-stu-id="d0e16-109">This cmdlet is designed as a general configuration command, but is currently limited to initiating failover.</span></span>
<span data-ttu-id="d0e16-110">Geben Sie den *Parameter "AllowDataLoss"* an, um einen Failover bei einem Ausfall zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="d0e16-110">Specify the *AllowDataLoss* parameter to initiate a force failover during an outage.</span></span>
<span data-ttu-id="d0e16-111">Sie müssen diesen Parameter nicht angeben, wenn Sie einen geplanten Vorgang wie einen Wiederherstellungsdrill ausführen.</span><span class="sxs-lookup"><span data-stu-id="d0e16-111">You do not have to specify this parameter when you perform a planned operation, such as recovery drill.</span></span>
<span data-ttu-id="d0e16-112">Im zweiten Fall wird die sekundäre Datenbank mit dem primären Datenbank synchronisiert, bevor sie gewechselt wird.</span><span class="sxs-lookup"><span data-stu-id="d0e16-112">In the latter case, the secondary database is synchronized with the primary before it is switched.</span></span>

## <span data-ttu-id="d0e16-113">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d0e16-113">EXAMPLES</span></span>

### <span data-ttu-id="d0e16-114">Beispiel 1: Initiieren eines geplanten Failovers</span><span class="sxs-lookup"><span data-stu-id="d0e16-114">Example 1: Initiate a planned failover</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover
```

### <span data-ttu-id="d0e16-115">Beispiel 2: Initiieren eines erzwungenen Failovers (mit potenziellem Datenverlust)</span><span class="sxs-lookup"><span data-stu-id="d0e16-115">Example 2: Initiate a forced failover (with potential data loss)</span></span>
```powershell
$database = Get-AzSqlDatabase -DatabaseName $databaseName -ResourceGroupName $secondaryResourceGroupName -ServerName $secondaryServerName
$database | Set-AzSqlDatabaseSecondary -PartnerResourceGroupName $primaryResourceGroupName -Failover -AllowDataLoss
```

## <span data-ttu-id="d0e16-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0e16-116">PARAMETERS</span></span>

### <span data-ttu-id="d0e16-117">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="d0e16-117">-AllowDataLoss</span></span>
<span data-ttu-id="d0e16-118">Gibt an, dass dieser Failovervorgang Datenverlust zulässt.</span><span class="sxs-lookup"><span data-stu-id="d0e16-118">Indicates that this failover operation permits data loss.</span></span>

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

### <span data-ttu-id="d0e16-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d0e16-119">-AsJob</span></span>
<span data-ttu-id="d0e16-120">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="d0e16-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d0e16-121">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d0e16-121">-DatabaseName</span></span>
<span data-ttu-id="d0e16-122">Gibt den Namen des Azure SQL Database Secondary an.</span><span class="sxs-lookup"><span data-stu-id="d0e16-122">Specifies the name of the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="d0e16-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0e16-123">-DefaultProfile</span></span>
<span data-ttu-id="d0e16-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d0e16-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d0e16-125">-Failover</span><span class="sxs-lookup"><span data-stu-id="d0e16-125">-Failover</span></span>
<span data-ttu-id="d0e16-126">Gibt an, dass es sich bei diesem Vorgang um einen Failover handelt.</span><span class="sxs-lookup"><span data-stu-id="d0e16-126">Indicates that this operation is a failover.</span></span>

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

### <span data-ttu-id="d0e16-127">-PartnerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0e16-127">-PartnerResourceGroupName</span></span>
<span data-ttu-id="d0e16-128">Gibt den Namen der Ressourcengruppe an, der der Azure SQL zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d0e16-128">Specifies the name of the resource group to which the partner Azure SQL Database is assigned.</span></span>

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

### <span data-ttu-id="d0e16-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d0e16-129">-ResourceGroupName</span></span>
<span data-ttu-id="d0e16-130">Gibt den Namen der Ressourcengruppe an, der die Azure SQL Database Secondary zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d0e16-130">Specifies the name of the resource group to which the Azure SQL Database Secondary is assigned.</span></span>

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

### <span data-ttu-id="d0e16-131">-ServerName</span><span class="sxs-lookup"><span data-stu-id="d0e16-131">-ServerName</span></span>
<span data-ttu-id="d0e16-132">Gibt den Namen des SQL Server an, das die sekundäre Azure SQL hostet.</span><span class="sxs-lookup"><span data-stu-id="d0e16-132">Specifies the name of the SQL Server that hosts the Azure SQL Database Secondary.</span></span>

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

### <span data-ttu-id="d0e16-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d0e16-133">-Confirm</span></span>
<span data-ttu-id="d0e16-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d0e16-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0e16-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d0e16-135">-WhatIf</span></span>
<span data-ttu-id="d0e16-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0e16-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0e16-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d0e16-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0e16-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0e16-138">CommonParameters</span></span>
<span data-ttu-id="d0e16-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0e16-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0e16-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0e16-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0e16-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d0e16-141">INPUTS</span></span>

### <span data-ttu-id="d0e16-142">System.String</span><span class="sxs-lookup"><span data-stu-id="d0e16-142">System.String</span></span>

## <span data-ttu-id="d0e16-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d0e16-143">OUTPUTS</span></span>

### <span data-ttu-id="d0e16-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span><span class="sxs-lookup"><span data-stu-id="d0e16-144">Microsoft.Azure.Commands.Sql.Replication.Model.AzureReplicationLinkModel</span></span>

## <span data-ttu-id="d0e16-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d0e16-145">NOTES</span></span>

## <span data-ttu-id="d0e16-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d0e16-146">RELATED LINKS</span></span>

[<span data-ttu-id="d0e16-147">New-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d0e16-147">New-AzSqlDatabaseSecondary</span></span>](./New-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="d0e16-148">Remove-AzSqlDatabaseSecondary</span><span class="sxs-lookup"><span data-stu-id="d0e16-148">Remove-AzSqlDatabaseSecondary</span></span>](./Remove-AzSqlDatabaseSecondary.md)

[<span data-ttu-id="d0e16-149">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="d0e16-149">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
