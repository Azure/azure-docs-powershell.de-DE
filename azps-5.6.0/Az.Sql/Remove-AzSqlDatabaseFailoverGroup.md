---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/remove-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: adc3bc9c8d367da6f031f8847cee7ce48b3f9b43
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101923307"
---
# <span data-ttu-id="54db6-101">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="54db6-101">Remove-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="54db6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54db6-102">SYNOPSIS</span></span>
<span data-ttu-id="54db6-103">Entfernt eine Azure SQL-Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="54db6-103">Removes an Azure SQL Database Failover Group.</span></span>

## <span data-ttu-id="54db6-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54db6-104">SYNTAX</span></span>

```
Remove-AzSqlDatabaseFailoverGroup [-ServerName] <String> [-FailoverGroupName] <String> [-Force]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="54db6-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54db6-105">DESCRIPTION</span></span>
<span data-ttu-id="54db6-106">Mit diesem Befehl wird die Failovergruppe mit dem angegebenen Namen entfernt, damit alle Datenbanken und Replikationsbeziehungen intakt bleiben.</span><span class="sxs-lookup"><span data-stu-id="54db6-106">This command removes the Failover Group with the specified name, leaving all databases and replication relationships intact.</span></span> <span data-ttu-id="54db6-107">Der Listenerendpunkt wird von DNS nicht registriert.</span><span class="sxs-lookup"><span data-stu-id="54db6-107">The listener endpoint will be unregistered from DNS.</span></span>
<span data-ttu-id="54db6-108">Der primäre Server der Failovergruppe sollte zum Ausführen des Befehls verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54db6-108">The Failover Group's primary server should be used to execute the command.</span></span>

## <span data-ttu-id="54db6-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54db6-109">EXAMPLES</span></span>

### <span data-ttu-id="54db6-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="54db6-110">Example 1</span></span>
```
PS C:\> Remove-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName primaryserver -FailoverGroupName fg
```

<span data-ttu-id="54db6-111">Entfernen sie eine Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="54db6-111">Remove a Failover Group.</span></span>

## <span data-ttu-id="54db6-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="54db6-112">PARAMETERS</span></span>

### <span data-ttu-id="54db6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54db6-113">-DefaultProfile</span></span>
<span data-ttu-id="54db6-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="54db6-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="54db6-115">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="54db6-115">-FailoverGroupName</span></span>
<span data-ttu-id="54db6-116">Der Name der Azure SQL-Failovergruppe, die entfernt werden soll.</span><span class="sxs-lookup"><span data-stu-id="54db6-116">The name of the Azure SQL Database Failover Group to remove.</span></span>

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

### <span data-ttu-id="54db6-117">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="54db6-117">-Force</span></span>
<span data-ttu-id="54db6-118">Bestätigungsmeldung überspringen, um die Aktion ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="54db6-118">Skip confirmation message for performing the action.</span></span>

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

### <span data-ttu-id="54db6-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="54db6-119">-ResourceGroupName</span></span>
<span data-ttu-id="54db6-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="54db6-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="54db6-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="54db6-121">-ServerName</span></span>
<span data-ttu-id="54db6-122">Der Name des primären Azure SQL Datenbankserver der Failovergruppe.</span><span class="sxs-lookup"><span data-stu-id="54db6-122">The name of the primary Azure SQL Database Server of the Failover Group.</span></span>

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

### <span data-ttu-id="54db6-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="54db6-123">-Confirm</span></span>
<span data-ttu-id="54db6-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="54db6-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="54db6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="54db6-125">-WhatIf</span></span>
<span data-ttu-id="54db6-126">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="54db6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="54db6-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54db6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="54db6-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54db6-128">CommonParameters</span></span>
<span data-ttu-id="54db6-129">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54db6-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54db6-130">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="54db6-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54db6-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54db6-131">INPUTS</span></span>

### <span data-ttu-id="54db6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="54db6-132">System.String</span></span>

## <span data-ttu-id="54db6-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54db6-133">OUTPUTS</span></span>

### <span data-ttu-id="54db6-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="54db6-134">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="54db6-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="54db6-135">NOTES</span></span>

## <span data-ttu-id="54db6-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="54db6-136">RELATED LINKS</span></span>

[<span data-ttu-id="54db6-137">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="54db6-137">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="54db6-138">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="54db6-138">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="54db6-139">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="54db6-139">Get-AzSqlDatabaseFailoverGroup</span></span>](./Get-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="54db6-140">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="54db6-140">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="54db6-141">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="54db6-141">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="54db6-142">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="54db6-142">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="54db6-143">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="54db6-143">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
