---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/switch-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Switch-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: d8eff694378f6145931a18a622f29bf88d99e1ef
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100163124"
---
# <span data-ttu-id="4993a-101">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4993a-101">Switch-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="4993a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4993a-102">SYNOPSIS</span></span>
<span data-ttu-id="4993a-103">Führt einen Failover eines Azure SQL A0 aus.</span><span class="sxs-lookup"><span data-stu-id="4993a-103">Executes a failover of an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="4993a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4993a-104">SYNTAX</span></span>

```
Switch-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>] [-AllowDataLoss]
 [-AsJob] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4993a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4993a-105">DESCRIPTION</span></span>
<span data-ttu-id="4993a-106">Mit diesem Befehl werden die Rollen der Server in einer Failovergruppe ausgetauscht, und alle sekundären Datenbanken werden in die primäre Rolle übertragen.</span><span class="sxs-lookup"><span data-stu-id="4993a-106">This command swaps the roles of the servers in a Failover Group and switches all secondary databases to the primary role.</span></span> <span data-ttu-id="4993a-107">Alle neuen TDS-Sitzungen werden nach der Aktualisierung des DNS-Clientcaches automatisch neu an den sekundären Server umgeroutet.</span><span class="sxs-lookup"><span data-stu-id="4993a-107">All new TDS sessions are automatically re-routed to the secondary server after the DNS client cache is refreshed.</span></span> <span data-ttu-id="4993a-108">Wenn der ursprüngliche primäre Server wieder online ist, wechseln alle früheren primären Datenbanken in die sekundäre Rolle.</span><span class="sxs-lookup"><span data-stu-id="4993a-108">When the original primary server is back online, all formerly primary databases in it will switch to the secondary role.</span></span>
<span data-ttu-id="4993a-109">Zum Ausführen dieses Befehls muss der sekundäre Server der Failovergruppe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4993a-109">The Failover Group's secondary server must be used to execute this command.</span></span>
<span data-ttu-id="4993a-110">Wenn der Parameter "AllowDataLoss" nicht angegeben ist, wartet dieser Befehl, bis beide Rollen gewechselt werden.</span><span class="sxs-lookup"><span data-stu-id="4993a-110">If the AllowDataLoss parameter is not specified, this command waits until both roles are switched.</span></span> <span data-ttu-id="4993a-111">Wenn der Parameter "AllowDataLoss" angegeben wird, wartet der Befehl nur, bis das neue Primäre seine Rolle annimmt.</span><span class="sxs-lookup"><span data-stu-id="4993a-111">If the AllowDataLoss parameter is specified, the command only waits until the new primary assumes its role.</span></span>

## <span data-ttu-id="4993a-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4993a-112">EXAMPLES</span></span>

### <span data-ttu-id="4993a-113">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4993a-113">Example 1</span></span>
```
C:\> Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg | Switch-AzSqlDatabaseFailoverGroup -AllowDataLoss
```

<span data-ttu-id="4993a-114">Führen Sie einen Failovervorgang aus, der Datenverlust durch Die Piping in der Failovergruppe ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="4993a-114">Issue a failover operation allowing data loss by piping in the Failover Group.</span></span>

### <span data-ttu-id="4993a-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="4993a-115">Example 2</span></span>
```
C:\> Switch-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName secondaryserver -FailoverGroupName fg
```

<span data-ttu-id="4993a-116">Führen Sie einen Best-Effort-Failovervorgang aus, der entweder erfolgreich ist, ohne dass Daten verloren gehen, oder fehlschlagen und ein Rollback durchführen.</span><span class="sxs-lookup"><span data-stu-id="4993a-116">Issue a best effort failover operation that will either succeed without losing data or fail and roll back.</span></span>

## <span data-ttu-id="4993a-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4993a-117">PARAMETERS</span></span>

### <span data-ttu-id="4993a-118">-AllowDataLoss</span><span class="sxs-lookup"><span data-stu-id="4993a-118">-AllowDataLoss</span></span>
<span data-ttu-id="4993a-119">Schließen Sie den Failover ab, auch wenn dies zu Datenverlust führen kann.</span><span class="sxs-lookup"><span data-stu-id="4993a-119">Complete the failover even if doing so may result in data loss.</span></span> <span data-ttu-id="4993a-120">Dadurch kann der Failover fortgesetzt werden, auch wenn eine primäre Datenbank nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="4993a-120">This will allow the failover to proceed even if a primary database is unavailable.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4993a-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4993a-121">-AsJob</span></span>
<span data-ttu-id="4993a-122">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="4993a-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4993a-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4993a-123">-DefaultProfile</span></span>
<span data-ttu-id="4993a-124">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4993a-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4993a-125">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="4993a-125">-FailoverGroupName</span></span>
<span data-ttu-id="4993a-126">Der Name der Azure SQL-Datenbank-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="4993a-126">The name of the Azure SQL Database Failover Group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4993a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4993a-127">-ResourceGroupName</span></span>
<span data-ttu-id="4993a-128">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4993a-128">The name of the resource group.</span></span>

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

### <span data-ttu-id="4993a-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4993a-129">-ServerName</span></span>
<span data-ttu-id="4993a-130">Der Name des sekundären Azure SQL Datenbankserver der Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="4993a-130">The name of the secondary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="4993a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4993a-131">-Confirm</span></span>
<span data-ttu-id="4993a-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4993a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4993a-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4993a-133">-WhatIf</span></span>
<span data-ttu-id="4993a-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4993a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4993a-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4993a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4993a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4993a-136">CommonParameters</span></span>
<span data-ttu-id="4993a-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4993a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4993a-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4993a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4993a-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4993a-139">INPUTS</span></span>

### <span data-ttu-id="4993a-140">System.String</span><span class="sxs-lookup"><span data-stu-id="4993a-140">System.String</span></span>

## <span data-ttu-id="4993a-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4993a-141">OUTPUTS</span></span>

### <span data-ttu-id="4993a-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="4993a-142">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="4993a-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4993a-143">NOTES</span></span>

## <span data-ttu-id="4993a-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4993a-144">RELATED LINKS</span></span>

[<span data-ttu-id="4993a-145">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4993a-145">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4993a-146">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4993a-146">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4993a-147">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4993a-147">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4993a-148">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4993a-148">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="4993a-149">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4993a-149">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="4993a-150">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="4993a-150">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="4993a-151">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="4993a-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
