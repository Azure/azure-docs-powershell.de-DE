---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/suspend-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
ms.openlocfilehash: 7a5ecbb21af23b31b321ef1568c2eb953a548cf1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658932"
---
# <span data-ttu-id="a0439-101">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0439-101">Suspend-AzSqlDatabase</span></span>

## <span data-ttu-id="a0439-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a0439-102">SYNOPSIS</span></span>
<span data-ttu-id="a0439-103">Unterbricht eine SQL Data Warehouse-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a0439-103">Suspends a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="a0439-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a0439-104">SYNTAX</span></span>

```
Suspend-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0439-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a0439-105">DESCRIPTION</span></span>
<span data-ttu-id="a0439-106">Das Cmdlet **Suspend-AzSqlDatabase** unterbricht eine Azure SQL Data Warehouse-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="a0439-106">The **Suspend-AzSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="a0439-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a0439-107">EXAMPLES</span></span>

### <span data-ttu-id="a0439-108">Beispiel 1: unterbricht eine Azure SQL Data Warehouse-Datenbank</span><span class="sxs-lookup"><span data-stu-id="a0439-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="a0439-109">Mit diesem Befehl wird eine Active Azure SQL Data Warehouse-Datenbank angehalten.</span><span class="sxs-lookup"><span data-stu-id="a0439-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="a0439-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a0439-110">PARAMETERS</span></span>

### <span data-ttu-id="a0439-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a0439-111">-AsJob</span></span>
<span data-ttu-id="a0439-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a0439-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a0439-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="a0439-113">-DatabaseName</span></span>
<span data-ttu-id="a0439-114">Gibt den Namen der Datenbank an, die von diesem Cmdlet angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="a0439-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="a0439-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0439-115">-DefaultProfile</span></span>
<span data-ttu-id="a0439-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a0439-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0439-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0439-117">-ResourceGroupName</span></span>
<span data-ttu-id="a0439-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="a0439-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="a0439-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="a0439-119">-ServerName</span></span>
<span data-ttu-id="a0439-120">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="a0439-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="a0439-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a0439-121">-Confirm</span></span>
<span data-ttu-id="a0439-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a0439-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0439-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0439-123">-WhatIf</span></span>
<span data-ttu-id="a0439-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a0439-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0439-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a0439-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0439-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0439-126">CommonParameters</span></span>
<span data-ttu-id="a0439-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0439-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0439-128">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a0439-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0439-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a0439-129">INPUTS</span></span>

### <span data-ttu-id="a0439-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a0439-130">System.String</span></span>

## <span data-ttu-id="a0439-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a0439-131">OUTPUTS</span></span>

### <span data-ttu-id="a0439-132">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a0439-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="a0439-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="a0439-133">NOTES</span></span>
* <span data-ttu-id="a0439-134">Das Cmdlet **Suspend-AzSqlDatabase** funktioniert nur in Azure SQL Data Warehouse-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="a0439-134">The **Suspend-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="a0439-135">Dieser Vorgang wird in Azure SQL-Datenbank Basic-, Standard-und Premium-Editionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a0439-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="a0439-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a0439-136">RELATED LINKS</span></span>

[<span data-ttu-id="a0439-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0439-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="a0439-138">Neu – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0439-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="a0439-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0439-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="a0439-140">Lebenslauf-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0439-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="a0439-141">Satz-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="a0439-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="a0439-142">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="a0439-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


