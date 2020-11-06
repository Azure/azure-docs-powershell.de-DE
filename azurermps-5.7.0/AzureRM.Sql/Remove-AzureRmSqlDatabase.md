---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqldatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
ms.openlocfilehash: 3da5093decdaea29d1a225db5c683d2f23f7115f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498705"
---
# <span data-ttu-id="37cc4-101">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="37cc4-101">Remove-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="37cc4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37cc4-102">SYNOPSIS</span></span>
<span data-ttu-id="37cc4-103">Entfernt eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="37cc4-103">Removes an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="37cc4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37cc4-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="37cc4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37cc4-105">DESCRIPTION</span></span>
<span data-ttu-id="37cc4-106">Das Cmdlet **Remove-AzureRmSqlDatabase** entfernt eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="37cc4-106">The **Remove-AzureRmSqlDatabase** cmdlet removes an Azure SQL database.</span></span>

<span data-ttu-id="37cc4-107">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="37cc4-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="37cc4-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37cc4-108">EXAMPLES</span></span>

### <span data-ttu-id="37cc4-109">Beispiel 1: Entfernen einer Datenbank aus einem Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="37cc4-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="37cc4-110">Mit diesem Befehl wird die Datenbank namens database01 vom Server Server01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="37cc4-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="37cc4-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="37cc4-111">PARAMETERS</span></span>

### <span data-ttu-id="37cc4-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="37cc4-112">-DatabaseName</span></span>
<span data-ttu-id="37cc4-113">Gibt den Namen der Datenbank an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="37cc4-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37cc4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37cc4-114">-DefaultProfile</span></span>
<span data-ttu-id="37cc4-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="37cc4-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="37cc4-116">-Force</span><span class="sxs-lookup"><span data-stu-id="37cc4-116">-Force</span></span>
<span data-ttu-id="37cc4-117">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="37cc4-117">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="37cc4-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37cc4-118">-ResourceGroupName</span></span>
<span data-ttu-id="37cc4-119">Gibt den Namen der Azure-Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="37cc4-119">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="37cc4-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="37cc4-120">-ServerName</span></span>
<span data-ttu-id="37cc4-121">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="37cc4-121">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="37cc4-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="37cc4-122">-Confirm</span></span>
<span data-ttu-id="37cc4-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="37cc4-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37cc4-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37cc4-124">-WhatIf</span></span>
<span data-ttu-id="37cc4-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="37cc4-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37cc4-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="37cc4-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37cc4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37cc4-127">CommonParameters</span></span>
<span data-ttu-id="37cc4-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37cc4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37cc4-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37cc4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37cc4-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37cc4-130">INPUTS</span></span>

### <span data-ttu-id="37cc4-131">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="37cc4-131">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="37cc4-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37cc4-132">OUTPUTS</span></span>

### <span data-ttu-id="37cc4-133">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="37cc4-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="37cc4-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="37cc4-134">NOTES</span></span>

## <span data-ttu-id="37cc4-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37cc4-135">RELATED LINKS</span></span>

[<span data-ttu-id="37cc4-136">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="37cc4-136">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="37cc4-137">Neu – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="37cc4-137">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="37cc4-138">Lebenslauf-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="37cc4-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="37cc4-139">Satz-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="37cc4-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="37cc4-140">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="37cc4-140">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="37cc4-141">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="37cc4-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


