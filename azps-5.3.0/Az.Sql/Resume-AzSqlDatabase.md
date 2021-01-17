---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: a31a77f4e0780b5100018962b3475a0dffa97d9f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376492"
---
# <span data-ttu-id="25e7c-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="25e7c-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="25e7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25e7c-102">SYNOPSIS</span></span>
<span data-ttu-id="25e7c-103">Setzt eine SQL Data Warehouse fort.</span><span class="sxs-lookup"><span data-stu-id="25e7c-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="25e7c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="25e7c-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25e7c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="25e7c-105">DESCRIPTION</span></span>
<span data-ttu-id="25e7c-106">Das **Cmdlet "Resume-AzSqlDatabase"** setzt eine Azure SQL Data Warehouse-Datenbank fort.</span><span class="sxs-lookup"><span data-stu-id="25e7c-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="25e7c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="25e7c-107">EXAMPLES</span></span>

### <span data-ttu-id="25e7c-108">Beispiel 1: Fortsetzen einer Azure SQL Data Warehouse-Datenbank</span><span class="sxs-lookup"><span data-stu-id="25e7c-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="25e7c-109">Mit diesem Befehl wird eine angehaltene Azure SQL Data Warehouse-Datenbank fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="25e7c-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="25e7c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25e7c-110">PARAMETERS</span></span>

### <span data-ttu-id="25e7c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25e7c-111">-AsJob</span></span>
<span data-ttu-id="25e7c-112">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="25e7c-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="25e7c-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="25e7c-113">-DatabaseName</span></span>
<span data-ttu-id="25e7c-114">Gibt den Namen der Datenbank an, die dieses Cmdlet fortsetzen soll.</span><span class="sxs-lookup"><span data-stu-id="25e7c-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="25e7c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25e7c-115">-DefaultProfile</span></span>
<span data-ttu-id="25e7c-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="25e7c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25e7c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25e7c-117">-ResourceGroupName</span></span>
<span data-ttu-id="25e7c-118">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="25e7c-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="25e7c-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="25e7c-119">-ServerName</span></span>
<span data-ttu-id="25e7c-120">Gibt den Namen des Servers an, der die Datenbank hostet, die von diesem Cmdlet fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="25e7c-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="25e7c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25e7c-121">-Confirm</span></span>
<span data-ttu-id="25e7c-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="25e7c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25e7c-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="25e7c-123">-WhatIf</span></span>
<span data-ttu-id="25e7c-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="25e7c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25e7c-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="25e7c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25e7c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25e7c-126">CommonParameters</span></span>
<span data-ttu-id="25e7c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25e7c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25e7c-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="25e7c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25e7c-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="25e7c-129">INPUTS</span></span>

### <span data-ttu-id="25e7c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="25e7c-130">System.String</span></span>

## <span data-ttu-id="25e7c-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="25e7c-131">OUTPUTS</span></span>

### <span data-ttu-id="25e7c-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="25e7c-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="25e7c-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="25e7c-133">NOTES</span></span>
* <span data-ttu-id="25e7c-134">Das **Cmdlet "Resume-AzSqlDatabase"** funktioniert nur in Azure SQL Data Warehouse-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="25e7c-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="25e7c-135">Dieser Vorgang wird für die Editionen Azure SQL Database Basic, Standard und Premium nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="25e7c-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="25e7c-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="25e7c-136">RELATED LINKS</span></span>

[<span data-ttu-id="25e7c-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="25e7c-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="25e7c-138">New-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="25e7c-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="25e7c-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="25e7c-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="25e7c-140">Set-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="25e7c-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="25e7c-141">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="25e7c-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="25e7c-142">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="25e7c-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


