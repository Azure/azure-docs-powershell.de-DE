---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: 283a7963d7dcf278f203385bd790bd19cadc9d7c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460644"
---
# <span data-ttu-id="98f51-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98f51-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="98f51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98f51-102">SYNOPSIS</span></span>
<span data-ttu-id="98f51-103">Entfernt eine Azure SQL-Datenbank-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="98f51-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="98f51-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98f51-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="98f51-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98f51-105">DESCRIPTION</span></span>
<span data-ttu-id="98f51-106">Mit diesem Befehl wird die Failovergruppe mit dem angegebenen Namen entfernt, und alle Datenbanken und Replikationsbeziehungen bleiben erhalten.</span><span class="sxs-lookup"><span data-stu-id="98f51-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="98f51-107">Die Registrierung des Listenerendpunkts wird im DNS aufgehoben.</span><span class="sxs-lookup"><span data-stu-id="98f51-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="98f51-108">Der primäre Server der Failovergruppe sollte zum Ausführen des Befehls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="98f51-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="98f51-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="98f51-109">EXAMPLES</span></span>

### <span data-ttu-id="98f51-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="98f51-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="98f51-111">Entfernen einer Failovergruppe</span><span class="sxs-lookup"><span data-stu-id="98f51-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="98f51-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="98f51-112">PARAMETERS</span></span>

### <span data-ttu-id="98f51-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f51-113">-DefaultProfile</span></span>
<span data-ttu-id="98f51-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="98f51-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="98f51-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="98f51-115">-FailoverGroupName</span></span>
<span data-ttu-id="98f51-116">Der Name der Azure SQL-Datenbank-Failovergruppe, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="98f51-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="98f51-117">-Force</span><span class="sxs-lookup"><span data-stu-id="98f51-117">-Force</span></span>
<span data-ttu-id="98f51-118">Bestätigungsmeldung zum Ausführen der Aktion überspringen</span><span class="sxs-lookup"><span data-stu-id="98f51-118">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="98f51-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98f51-119">-ResourceGroupName</span></span>
<span data-ttu-id="98f51-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="98f51-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="98f51-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="98f51-121">-ServerName</span></span>
<span data-ttu-id="98f51-122">Der Name des primären Azure SQL Datenbankservers der Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="98f51-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="98f51-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="98f51-123">-Confirm</span></span>
<span data-ttu-id="98f51-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="98f51-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98f51-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="98f51-125">-WhatIf</span></span>
<span data-ttu-id="98f51-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="98f51-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98f51-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="98f51-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98f51-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f51-128">CommonParameters</span></span>
<span data-ttu-id="98f51-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98f51-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f51-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="98f51-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f51-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="98f51-131">INPUTS</span></span>

### <span data-ttu-id="98f51-132">System.String</span><span class="sxs-lookup"><span data-stu-id="98f51-132">System.String</span></span>

## <span data-ttu-id="98f51-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="98f51-133">OUTPUTS</span></span>

### <span data-ttu-id="98f51-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="98f51-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="98f51-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="98f51-135">NOTES</span></span>

## <span data-ttu-id="98f51-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="98f51-136">RELATED LINKS</span></span>

[<span data-ttu-id="98f51-137">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98f51-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="98f51-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98f51-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="98f51-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98f51-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="98f51-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98f51-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="98f51-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98f51-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="98f51-142">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="98f51-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="98f51-143">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="98f51-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
