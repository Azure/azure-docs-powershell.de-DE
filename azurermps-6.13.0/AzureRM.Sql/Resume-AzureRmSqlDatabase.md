---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/resume-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
ms.openlocfilehash: 5681b046afb6682809d9b2dc744784514c2aefa6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93497245"
---
# <span data-ttu-id="9abb5-101">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9abb5-101">Resume-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="9abb5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9abb5-102">SYNOPSIS</span></span>
<span data-ttu-id="9abb5-103">Setzt eine SQL Data Warehouse-Datenbank fort.</span><span class="sxs-lookup"><span data-stu-id="9abb5-103">Resumes a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9abb5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9abb5-104">SYNTAX</span></span>

```
Resume-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9abb5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9abb5-105">DESCRIPTION</span></span>
<span data-ttu-id="9abb5-106">Mit dem Cmdlet **Resume-AzureRmSqlDatabase** wird eine Azure SQL Data Warehouse-Datenbank fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="9abb5-106">The **Resume-AzureRmSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="9abb5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9abb5-107">EXAMPLES</span></span>

### <span data-ttu-id="9abb5-108">Beispiel 1: Fortsetzen einer Azure SQL Data Warehouse-Datenbank</span><span class="sxs-lookup"><span data-stu-id="9abb5-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="9abb5-109">Mit diesem Befehl wird eine angehaltene Azure SQL Data Warehouse-Datenbank fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="9abb5-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="9abb5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9abb5-110">PARAMETERS</span></span>

### <span data-ttu-id="9abb5-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9abb5-111">-AsJob</span></span>
<span data-ttu-id="9abb5-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9abb5-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9abb5-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="9abb5-113">-DatabaseName</span></span>
<span data-ttu-id="9abb5-114">Gibt den Namen der Datenbank an, die von diesem Cmdlet fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="9abb5-114">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="9abb5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9abb5-115">-DefaultProfile</span></span>
<span data-ttu-id="9abb5-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9abb5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9abb5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9abb5-117">-ResourceGroupName</span></span>
<span data-ttu-id="9abb5-118">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="9abb5-118">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="9abb5-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="9abb5-119">-ServerName</span></span>
<span data-ttu-id="9abb5-120">Gibt den Namen des Servers an, der die Datenbank hostet, die von diesem Cmdlet fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="9abb5-120">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="9abb5-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9abb5-121">-Confirm</span></span>
<span data-ttu-id="9abb5-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9abb5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9abb5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9abb5-123">-WhatIf</span></span>
<span data-ttu-id="9abb5-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9abb5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9abb5-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9abb5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9abb5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9abb5-126">CommonParameters</span></span>
<span data-ttu-id="9abb5-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9abb5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9abb5-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9abb5-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9abb5-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9abb5-129">INPUTS</span></span>

### <span data-ttu-id="9abb5-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9abb5-130">System.String</span></span>

## <span data-ttu-id="9abb5-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9abb5-131">OUTPUTS</span></span>

### <span data-ttu-id="9abb5-132">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="9abb5-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="9abb5-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="9abb5-133">NOTES</span></span>
* <span data-ttu-id="9abb5-134">Das Cmdlet **Resume-AzureRmSqlDatabase** funktioniert nur in Azure SQL Data Warehouse-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="9abb5-134">The **Resume-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="9abb5-135">Dieser Vorgang wird in Azure SQL-Datenbank Basic-, Standard-und Premium-Editionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9abb5-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="9abb5-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9abb5-136">RELATED LINKS</span></span>

[<span data-ttu-id="9abb5-137">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9abb5-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="9abb5-138">Neu – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9abb5-138">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="9abb5-139">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9abb5-139">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="9abb5-140">Satz-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9abb5-140">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="9abb5-141">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="9abb5-141">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="9abb5-142">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="9abb5-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


