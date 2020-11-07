---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/suspend-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Suspend-AzureRmSqlDatabase.md
ms.openlocfilehash: b4238ff85a35bcf6a48016a005af8a1f889332cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664149"
---
# <span data-ttu-id="97026-101">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="97026-101">Suspend-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="97026-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="97026-102">SYNOPSIS</span></span>
<span data-ttu-id="97026-103">Unterbricht eine SQL Data Warehouse-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="97026-103">Suspends a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="97026-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="97026-104">SYNTAX</span></span>

```
Suspend-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97026-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="97026-105">DESCRIPTION</span></span>
<span data-ttu-id="97026-106">Das Cmdlet **Suspend-AzureRmSqlDatabase** unterbricht eine Azure SQL Data Warehouse-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="97026-106">The **Suspend-AzureRmSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="97026-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="97026-107">EXAMPLES</span></span>

### <span data-ttu-id="97026-108">Beispiel 1: unterbricht eine Azure SQL Data Warehouse-Datenbank</span><span class="sxs-lookup"><span data-stu-id="97026-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="97026-109">Mit diesem Befehl wird eine Active Azure SQL Data Warehouse-Datenbank angehalten.</span><span class="sxs-lookup"><span data-stu-id="97026-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="97026-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="97026-110">PARAMETERS</span></span>

### <span data-ttu-id="97026-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="97026-111">-AsJob</span></span>
<span data-ttu-id="97026-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="97026-112">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97026-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="97026-113">-DatabaseName</span></span>
<span data-ttu-id="97026-114">Gibt den Namen der Datenbank an, die von diesem Cmdlet angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="97026-114">Specifies the name of the database that this cmdlet suspends.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97026-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97026-115">-DefaultProfile</span></span>
<span data-ttu-id="97026-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="97026-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97026-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="97026-117">-ResourceGroupName</span></span>
<span data-ttu-id="97026-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="97026-118">Specifies the name of the resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97026-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="97026-119">-ServerName</span></span>
<span data-ttu-id="97026-120">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="97026-120">Specifies the name of the server which hosts the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="97026-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="97026-121">-Confirm</span></span>
<span data-ttu-id="97026-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="97026-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97026-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97026-123">-WhatIf</span></span>
<span data-ttu-id="97026-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="97026-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97026-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="97026-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97026-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97026-126">CommonParameters</span></span>
<span data-ttu-id="97026-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="97026-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97026-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="97026-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97026-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="97026-129">INPUTS</span></span>

### <span data-ttu-id="97026-130">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="97026-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="97026-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="97026-131">OUTPUTS</span></span>

### <span data-ttu-id="97026-132">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="97026-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="97026-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="97026-133">NOTES</span></span>
* <span data-ttu-id="97026-134">Das Cmdlet **Suspend-AzureRmSqlDatabase** funktioniert nur in Azure SQL Data Warehouse-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="97026-134">The **Suspend-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="97026-135">Dieser Vorgang wird in Azure SQL-Datenbank Basic-, Standard-und Premium-Editionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="97026-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="97026-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="97026-136">RELATED LINKS</span></span>

[<span data-ttu-id="97026-137">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="97026-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="97026-138">Neu – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="97026-138">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="97026-139">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="97026-139">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="97026-140">Lebenslauf-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="97026-140">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="97026-141">Satz-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="97026-141">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="97026-142">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="97026-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


