---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/suspend-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
ms.openlocfilehash: a2bfaa0b6cd6d0731bceab7f05a59216e80bd135
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98458352"
---
# <span data-ttu-id="8e7b9-101">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8e7b9-101">Suspend-AzSqlDatabase</span></span>

## <span data-ttu-id="8e7b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8e7b9-102">SYNOPSIS</span></span>
<span data-ttu-id="8e7b9-103">Ein Daten-Warehouse-SQL wird angehalten.</span><span class="sxs-lookup"><span data-stu-id="8e7b9-103">Suspends a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="8e7b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8e7b9-104">SYNTAX</span></span>

```
Suspend-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e7b9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8e7b9-105">DESCRIPTION</span></span>
<span data-ttu-id="8e7b9-106">Das **Cmdlet "Suspend-AzSqlDatabase"** setzt eine Azure SQL Data Warehouse-Datenbank aus.</span><span class="sxs-lookup"><span data-stu-id="8e7b9-106">The **Suspend-AzSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="8e7b9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8e7b9-107">EXAMPLES</span></span>

### <span data-ttu-id="8e7b9-108">Beispiel 1: Anhalten einer Azure SQL Data Warehouse-Datenbank</span><span class="sxs-lookup"><span data-stu-id="8e7b9-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="8e7b9-109">Mit diesem Befehl wird eine aktive Azure SQL Data Warehouse-Datenbank angehalten.</span><span class="sxs-lookup"><span data-stu-id="8e7b9-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="8e7b9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8e7b9-110">PARAMETERS</span></span>

### <span data-ttu-id="8e7b9-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8e7b9-111">-AsJob</span></span>
<span data-ttu-id="8e7b9-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8e7b9-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8e7b9-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8e7b9-113">-DatabaseName</span></span>
<span data-ttu-id="8e7b9-114">Gibt den Namen der Datenbank an, die von diesem Cmdlet angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="8e7b9-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="8e7b9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e7b9-115">-DefaultProfile</span></span>
<span data-ttu-id="8e7b9-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="8e7b9-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e7b9-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8e7b9-117">-ResourceGroupName</span></span>
<span data-ttu-id="8e7b9-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="8e7b9-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="8e7b9-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="8e7b9-119">-ServerName</span></span>
<span data-ttu-id="8e7b9-120">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="8e7b9-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="8e7b9-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8e7b9-121">-Confirm</span></span>
<span data-ttu-id="8e7b9-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8e7b9-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e7b9-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="8e7b9-123">-WhatIf</span></span>
<span data-ttu-id="8e7b9-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8e7b9-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e7b9-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8e7b9-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e7b9-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e7b9-126">CommonParameters</span></span>
<span data-ttu-id="8e7b9-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e7b9-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e7b9-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8e7b9-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e7b9-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8e7b9-129">INPUTS</span></span>

### <span data-ttu-id="8e7b9-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8e7b9-130">System.String</span></span>

## <span data-ttu-id="8e7b9-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8e7b9-131">OUTPUTS</span></span>

### <span data-ttu-id="8e7b9-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8e7b9-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="8e7b9-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="8e7b9-133">NOTES</span></span>
* <span data-ttu-id="8e7b9-134">Das **Cmdlet "Suspend-AzSqlDatabase"** funktioniert nur in Azure SQL Data Warehouse-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="8e7b9-134">The **Suspend-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="8e7b9-135">Dieser Vorgang wird für die Editionen Azure SQL Database Basic, Standard und Premium nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8e7b9-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="8e7b9-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="8e7b9-136">RELATED LINKS</span></span>

[<span data-ttu-id="8e7b9-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8e7b9-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="8e7b9-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8e7b9-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="8e7b9-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8e7b9-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="8e7b9-140">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8e7b9-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="8e7b9-141">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8e7b9-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="8e7b9-142">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="8e7b9-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


