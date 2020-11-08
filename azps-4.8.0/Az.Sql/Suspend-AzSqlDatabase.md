---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 7302D785-9DD0-4CC0-93C9-9A6EA60591CF
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/suspend-azsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Suspend-AzSqlDatabase.md
ms.openlocfilehash: a2bfaa0b6cd6d0731bceab7f05a59216e80bd135
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166819"
---
# <span data-ttu-id="8f50d-101">Suspend-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8f50d-101">Suspend-AzSqlDatabase</span></span>

## <span data-ttu-id="8f50d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8f50d-102">SYNOPSIS</span></span>
<span data-ttu-id="8f50d-103">Unterbricht eine SQL Data Warehouse-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8f50d-103">Suspends a SQL Data Warehouse database.</span></span>

## <span data-ttu-id="8f50d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8f50d-104">SYNTAX</span></span>

```
Suspend-AzSqlDatabase [-ServerName] <String> -DatabaseName <String> [-AsJob] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f50d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8f50d-105">DESCRIPTION</span></span>
<span data-ttu-id="8f50d-106">Das Cmdlet **Suspend-AzSqlDatabase** unterbricht eine Azure SQL Data Warehouse-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="8f50d-106">The **Suspend-AzSqlDatabase** cmdlet suspends an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="8f50d-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8f50d-107">EXAMPLES</span></span>

### <span data-ttu-id="8f50d-108">Beispiel 1: unterbricht eine Azure SQL Data Warehouse-Datenbank</span><span class="sxs-lookup"><span data-stu-id="8f50d-108">Example 1: Suspends an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Suspend-AzSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="8f50d-109">Mit diesem Befehl wird eine Active Azure SQL Data Warehouse-Datenbank angehalten.</span><span class="sxs-lookup"><span data-stu-id="8f50d-109">This command suspends an active Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="8f50d-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8f50d-110">PARAMETERS</span></span>

### <span data-ttu-id="8f50d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f50d-111">-AsJob</span></span>
<span data-ttu-id="8f50d-112">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8f50d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8f50d-113">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8f50d-113">-DatabaseName</span></span>
<span data-ttu-id="8f50d-114">Gibt den Namen der Datenbank an, die von diesem Cmdlet angehalten wird.</span><span class="sxs-lookup"><span data-stu-id="8f50d-114">Specifies the name of the database that this cmdlet suspends.</span></span>

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

### <span data-ttu-id="8f50d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f50d-115">-DefaultProfile</span></span>
<span data-ttu-id="8f50d-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8f50d-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8f50d-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f50d-117">-ResourceGroupName</span></span>
<span data-ttu-id="8f50d-118">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="8f50d-118">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="8f50d-119">-Servername</span><span class="sxs-lookup"><span data-stu-id="8f50d-119">-ServerName</span></span>
<span data-ttu-id="8f50d-120">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="8f50d-120">Specifies the name of the server which hosts the database.</span></span>

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

### <span data-ttu-id="8f50d-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8f50d-121">-Confirm</span></span>
<span data-ttu-id="8f50d-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8f50d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f50d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f50d-123">-WhatIf</span></span>
<span data-ttu-id="8f50d-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8f50d-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f50d-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8f50d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f50d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f50d-126">CommonParameters</span></span>
<span data-ttu-id="8f50d-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f50d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f50d-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f50d-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f50d-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8f50d-129">INPUTS</span></span>

### <span data-ttu-id="8f50d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="8f50d-130">System.String</span></span>

## <span data-ttu-id="8f50d-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8f50d-131">OUTPUTS</span></span>

### <span data-ttu-id="8f50d-132">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="8f50d-132">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="8f50d-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="8f50d-133">NOTES</span></span>
* <span data-ttu-id="8f50d-134">Das Cmdlet **Suspend-AzSqlDatabase** funktioniert nur in Azure SQL Data Warehouse-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="8f50d-134">The **Suspend-AzSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="8f50d-135">Dieser Vorgang wird in Azure SQL-Datenbank Basic-, Standard-und Premium-Editionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8f50d-135">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="8f50d-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8f50d-136">RELATED LINKS</span></span>

[<span data-ttu-id="8f50d-137">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8f50d-137">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="8f50d-138">Neu – AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8f50d-138">New-AzSqlDatabase</span></span>](./New-AzSqlDatabase.md)

[<span data-ttu-id="8f50d-139">Remove-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8f50d-139">Remove-AzSqlDatabase</span></span>](./Remove-AzSqlDatabase.md)

[<span data-ttu-id="8f50d-140">Lebenslauf-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8f50d-140">Resume-AzSqlDatabase</span></span>](./Resume-AzSqlDatabase.md)

[<span data-ttu-id="8f50d-141">Satz-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8f50d-141">Set-AzSqlDatabase</span></span>](./Set-AzSqlDatabase.md)

[<span data-ttu-id="8f50d-142">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="8f50d-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


