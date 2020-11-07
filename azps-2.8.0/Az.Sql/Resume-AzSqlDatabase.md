---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/resume-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Resume-AzSqlDatabase.md
ms.openlocfilehash: c5f30388e1e3cb804aa0ef8d45e0afe34a1d2cec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93825352"
---
# <span data-ttu-id="26438-101">Resume-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="26438-101">Resume-AzSqlDatabase</span></span>

## <span data-ttu-id="26438-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="26438-102">SYNOPSIS</span></span>
<span data-ttu-id="26438-103">Setzt eine SQL Data Warehouse-Datenbank fort.</span><span class="sxs-lookup"><span data-stu-id="26438-103">Resumes a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="26438-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="26438-104">SYNTAX</span></span>

```
Resume-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26438-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="26438-105">DESCRIPTION</span></span>
<span data-ttu-id="26438-106">Mit dem Cmdlet **Resume-AzSqlDatabase** wird eine Azure SQL Data Warehouse-Datenbank fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="26438-106">The **Resume-AzSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="26438-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="26438-107">EXAMPLES</span></span>

### <span data-ttu-id="26438-108">Beispiel 1: Fortsetzen einer Azure SQL Data Warehouse-Datenbank</span><span class="sxs-lookup"><span data-stu-id="26438-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="26438-109">Mit diesem Befehl wird eine angehaltene Azure SQL Data Warehouse-Datenbank fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="26438-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="26438-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="26438-110">PARAMETERS</span></span>

### <span data-ttu-id="26438-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26438-111">-AsJob</span></span>
<span data-ttu-id="26438-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="26438-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26438-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="26438-113">-DatabaseName</span></span>
<span data-ttu-id="26438-114">Gibt den Namen der Datenbank an, die von diesem Cmdlet fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="26438-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="26438-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26438-115">-DefaultProfile</span></span>
<span data-ttu-id="26438-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="26438-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26438-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26438-117">-ResourceGroupName</span></span>
<span data-ttu-id="26438-118">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="26438-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="26438-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="26438-119">-ServerName</span></span>
<span data-ttu-id="26438-120">Gibt den Namen des Servers an, der die Datenbank hostet, die von diesem Cmdlet fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="26438-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="26438-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="26438-121">-Confirm</span></span>
<span data-ttu-id="26438-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="26438-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26438-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26438-123">-WhatIf</span></span>
<span data-ttu-id="26438-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="26438-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26438-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="26438-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26438-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26438-126">CommonParameters</span></span>
<span data-ttu-id="26438-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26438-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26438-128">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="26438-128">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26438-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="26438-129">INPUTS</span></span>

### <span data-ttu-id="26438-130">System. String</span><span class="sxs-lookup"><span data-stu-id="26438-130">System.String</span></span>

## <span data-ttu-id="26438-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="26438-131">OUTPUTS</span></span>

### <span data-ttu-id="26438-132">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="26438-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="26438-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="26438-133">NOTES</span></span>
* <span data-ttu-id="26438-134">Das Cmdlet **Resume-AzSqlDatabase** funktioniert nur in Azure SQL Data Warehouse-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="26438-134">The **Resume-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="26438-135">Dieser Vorgang wird in Azure SQL-Datenbank Basic-, Standard-und Premium-Editionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="26438-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="26438-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="26438-136">RELATED LINKS</span></span>

[<span data-ttu-id="26438-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="26438-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="26438-138">Neu – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="26438-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="26438-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="26438-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="26438-140">Satz-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="26438-140">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="26438-141">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="26438-141">Suspend-AzSqlDatabase</span></span>](./Suspend-AzSqlDatabase.md)

[<span data-ttu-id="26438-142">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="26438-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


