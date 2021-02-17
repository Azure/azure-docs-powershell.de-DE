---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabasefailovergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseFailoverGroup.md
ms.openlocfilehash: a2c7192fc1ce2055b05a4f943a0c04560f1e714e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100164961"
---
# <span data-ttu-id="1a49e-101">Get-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1a49e-101">Get-AzSqlDatabaseFailoverGroup</span></span>

## <span data-ttu-id="1a49e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a49e-102">SYNOPSIS</span></span>
<span data-ttu-id="1a49e-103">Ruft Azure-SQL-SQL-Failovergruppen ab oder listet diese auf.</span><span class="sxs-lookup"><span data-stu-id="1a49e-103">Gets or lists Azure SQL Database Failover Groups.</span></span>

## <span data-ttu-id="1a49e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1a49e-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseFailoverGroup [-ServerName] <String> [[-FailoverGroupName] <String>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a49e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1a49e-105">DESCRIPTION</span></span>
<span data-ttu-id="1a49e-106">Ruft eine bestimmte Azure SQL A0 ab oder listet die Failovergruppen auf einem Server auf.</span><span class="sxs-lookup"><span data-stu-id="1a49e-106">Gets a specific Azure SQL Database Failover Group or lists the Failover Groups on a server.</span></span>
<span data-ttu-id="1a49e-107">Zum Ausführen des Befehls kann entweder ein Server in der Failovergruppe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a49e-107">Either server in the Failover Group may be used to execute the command.</span></span> <span data-ttu-id="1a49e-108">Die zurückgegebenen Werte geben den Zustand des angegebenen Servers in Bezug auf die Failovergruppe wieder.</span><span class="sxs-lookup"><span data-stu-id="1a49e-108">The returned values will reflect the state of the specified server with respect to the Failover Group.</span></span>

## <span data-ttu-id="1a49e-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1a49e-109">EXAMPLES</span></span>

### <span data-ttu-id="1a49e-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1a49e-110">Example 1</span></span>
```
PS C:\> $failoverGroups = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server
```

<span data-ttu-id="1a49e-111">Listet alle Failovergruppen auf einem Server auf.</span><span class="sxs-lookup"><span data-stu-id="1a49e-111">Lists all Failover Groups on a server.</span></span>

### <span data-ttu-id="1a49e-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="1a49e-112">Example 2</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg
```

<span data-ttu-id="1a49e-113">Sie können eine bestimmte Failovergruppe erhalten.</span><span class="sxs-lookup"><span data-stu-id="1a49e-113">Get a specific Failover Group.</span></span>

### <span data-ttu-id="1a49e-114">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="1a49e-114">Example 3</span></span>
```
PS C:\> $failoverGroup = Get-AzSqlDatabaseFailoverGroup -ResourceGroupName rg -ServerName server -FailoverGroupName fg*
```

<span data-ttu-id="1a49e-115">Holen Sie sich alle Failovergruppen auf einem Server, die mit "fg" beginnen.</span><span class="sxs-lookup"><span data-stu-id="1a49e-115">Get all failover groups in a server that start with "fg".</span></span>

## <span data-ttu-id="1a49e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a49e-116">PARAMETERS</span></span>

### <span data-ttu-id="1a49e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a49e-117">-DefaultProfile</span></span>
<span data-ttu-id="1a49e-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1a49e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a49e-119">-FailoverGroupName</span><span class="sxs-lookup"><span data-stu-id="1a49e-119">-FailoverGroupName</span></span>
<span data-ttu-id="1a49e-120">Der Name der Azure SQL-Datenbank-Failovergruppe, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a49e-120">The name of the Azure SQL Database Failover Group to retrieve.</span></span>

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

### <span data-ttu-id="1a49e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a49e-121">-ResourceGroupName</span></span>
<span data-ttu-id="1a49e-122">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1a49e-122">The name of the resource group.</span></span>

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

### <span data-ttu-id="1a49e-123">-ServerName</span><span class="sxs-lookup"><span data-stu-id="1a49e-123">-ServerName</span></span>
<span data-ttu-id="1a49e-124">Der Name des Azure SQL Datenbankservers, aus dem die Failovergruppe abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a49e-124">The name of the Azure SQL Database Server from which to retrieve the Failover Group.</span></span>

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

### <span data-ttu-id="1a49e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a49e-125">CommonParameters</span></span>
<span data-ttu-id="1a49e-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a49e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a49e-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a49e-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a49e-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1a49e-128">INPUTS</span></span>

### <span data-ttu-id="1a49e-129">System.String</span><span class="sxs-lookup"><span data-stu-id="1a49e-129">System.String</span></span>

## <span data-ttu-id="1a49e-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1a49e-130">OUTPUTS</span></span>

### <span data-ttu-id="1a49e-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span><span class="sxs-lookup"><span data-stu-id="1a49e-131">Microsoft.Azure.Commands.Sql.FailoverGroup.Model.AzureSqlFailoverGroupModel</span></span>

## <span data-ttu-id="1a49e-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1a49e-132">NOTES</span></span>

## <span data-ttu-id="1a49e-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1a49e-133">RELATED LINKS</span></span>

[<span data-ttu-id="1a49e-134">New-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1a49e-134">New-AzSqlDatabaseFailoverGroup</span></span>](./New-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1a49e-135">Set-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1a49e-135">Set-AzSqlDatabaseFailoverGroup</span></span>](./Set-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1a49e-136">Add-AzSqlDatabaseToFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1a49e-136">Add-AzSqlDatabaseToFailoverGroup</span></span>](./Add-AzSqlDatabaseToFailoverGroup.md)

[<span data-ttu-id="1a49e-137">Remove-AzSqlDatabaseFromFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1a49e-137">Remove-AzSqlDatabaseFromFailoverGroup</span></span>](./Remove-AzSqlDatabaseFromFailoverGroup.md)

[<span data-ttu-id="1a49e-138">Switch-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1a49e-138">Switch-AzSqlDatabaseFailoverGroup</span></span>](./Switch-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1a49e-139">Remove-AzSqlDatabaseFailoverGroup</span><span class="sxs-lookup"><span data-stu-id="1a49e-139">Remove-AzSqlDatabaseFailoverGroup</span></span>](./Remove-AzSqlDatabaseFailoverGroup.md)

[<span data-ttu-id="1a49e-140">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="1a49e-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
