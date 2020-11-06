---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
ms.openlocfilehash: 23affeb81159da5a9f1212f5190f927dc1689e44
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503154"
---
# <span data-ttu-id="e1d25-101">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e1d25-101">Suspend-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="e1d25-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e1d25-102">SYNOPSIS</span></span>
<span data-ttu-id="e1d25-103">Unterbricht eine SQL Data Warehouse-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e1d25-103">Suspends a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1d25-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e1d25-104">SYNTAX</span></span>

```
Suspend-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e1d25-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e1d25-105">DESCRIPTION</span></span>
<span data-ttu-id="e1d25-106">Das Cmdlet **Suspend-AzureRmSqlDatabase** unterbricht eine Azure SQL Data Warehouse-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="e1d25-106">The **Suspend-AzureRmSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="e1d25-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e1d25-107">EXAMPLES</span></span>

### <span data-ttu-id="e1d25-108">Beispiel 1: unterbricht eine Azure SQL Data Warehouse-Datenbank</span><span class="sxs-lookup"><span data-stu-id="e1d25-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="e1d25-109">Mit diesem Befehl wird eine Active Azure SQL Data Warehouse-Datenbank angehalten.</span><span class="sxs-lookup"><span data-stu-id="e1d25-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="e1d25-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="e1d25-110">PARAMETERS</span></span>

### <span data-ttu-id="e1d25-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="e1d25-111">-DatabaseName</span></span>
<span data-ttu-id="e1d25-112">Gibt den Namen der Datenbank an, die von diesem Cmdlet angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="e1d25-112">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="e1d25-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1d25-113">-ResourceGroupName</span></span>
<span data-ttu-id="e1d25-114">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="e1d25-114">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="e1d25-115">-Servername</span><span class="sxs-lookup"><span data-stu-id="e1d25-115">-ServerName</span></span>
<span data-ttu-id="e1d25-116">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="e1d25-116">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="e1d25-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="e1d25-117">-Confirm</span></span>
<span data-ttu-id="e1d25-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e1d25-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1d25-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1d25-119">-WhatIf</span></span>
<span data-ttu-id="e1d25-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e1d25-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1d25-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e1d25-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1d25-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1d25-122">-DefaultProfile</span></span>
<span data-ttu-id="e1d25-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e1d25-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1d25-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1d25-124">CommonParameters</span></span>
<span data-ttu-id="e1d25-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1d25-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1d25-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1d25-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1d25-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e1d25-127">INPUTS</span></span>

### <span data-ttu-id="e1d25-128">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e1d25-128">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="e1d25-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e1d25-129">OUTPUTS</span></span>

### <span data-ttu-id="e1d25-130">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="e1d25-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="e1d25-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="e1d25-131">NOTES</span></span>
* <span data-ttu-id="e1d25-132">Das Cmdlet **Suspend-AzureRmSqlDatabase** funktioniert nur in Azure SQL Data Warehouse-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="e1d25-132">The **Suspend-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="e1d25-133">Dieser Vorgang wird in Azure SQL-Datenbank Basic-, Standard-und Premium-Editionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e1d25-133">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="e1d25-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e1d25-134">RELATED LINKS</span></span>

[<span data-ttu-id="e1d25-135">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e1d25-135">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="e1d25-136">Neu – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e1d25-136">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="e1d25-137">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e1d25-137">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="e1d25-138">Lebenslauf-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e1d25-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="e1d25-139">Satz-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="e1d25-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="e1d25-140">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="e1d25-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


