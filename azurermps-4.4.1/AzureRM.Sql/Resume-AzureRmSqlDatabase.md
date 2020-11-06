---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 84CF049A-D293-4FEB-8608-179146EADE41
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Resume-AzureRmSqlDatabase.md
ms.openlocfilehash: f3554aa2e7f4970b3fa1752077a25e02d631abbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505573"
---
# <span data-ttu-id="88227-101">Resume-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="88227-101">Resume-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="88227-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="88227-102">SYNOPSIS</span></span>
<span data-ttu-id="88227-103">Setzt eine SQL Data Warehouse-Datenbank fort.</span><span class="sxs-lookup"><span data-stu-id="88227-103">Resumes a SQL Data Warehouse database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88227-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="88227-104">SYNTAX</span></span>

```
Resume-AzureRmSqlDatabase [-ServerName] <String> -DatabaseName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88227-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88227-105">DESCRIPTION</span></span>
<span data-ttu-id="88227-106">Mit dem Cmdlet **Resume-AzureRmSqlDatabase** wird eine Azure SQL Data Warehouse-Datenbank fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="88227-106">The **Resume-AzureRmSqlDatabase** cmdlet resumes an Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="88227-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88227-107">EXAMPLES</span></span>

### <span data-ttu-id="88227-108">Beispiel 1: Fortsetzen einer Azure SQL Data Warehouse-Datenbank</span><span class="sxs-lookup"><span data-stu-id="88227-108">Example 1: Resumes an Azure SQL Data Warehouse database</span></span>
```
PS C:\>Resume-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="88227-109">Mit diesem Befehl wird eine angehaltene Azure SQL Data Warehouse-Datenbank fortgesetzt.</span><span class="sxs-lookup"><span data-stu-id="88227-109">This command resumes a suspended Azure SQL Data Warehouse database.</span></span>

## <span data-ttu-id="88227-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="88227-110">PARAMETERS</span></span>

### <span data-ttu-id="88227-111">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="88227-111">-DatabaseName</span></span>
<span data-ttu-id="88227-112">Gibt den Namen der Datenbank an, die von diesem Cmdlet fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="88227-112">Specifies the name of the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="88227-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88227-113">-ResourceGroupName</span></span>
<span data-ttu-id="88227-114">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="88227-114">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="88227-115">-Servername</span><span class="sxs-lookup"><span data-stu-id="88227-115">-ServerName</span></span>
<span data-ttu-id="88227-116">Gibt den Namen des Servers an, der die Datenbank hostet, die von diesem Cmdlet fortgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="88227-116">Specifies the name of the server that hosts the database that this cmdlet resumes.</span></span>

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

### <span data-ttu-id="88227-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="88227-117">-Confirm</span></span>
<span data-ttu-id="88227-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="88227-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88227-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88227-119">-WhatIf</span></span>
<span data-ttu-id="88227-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="88227-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88227-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="88227-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88227-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88227-122">-DefaultProfile</span></span>
<span data-ttu-id="88227-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="88227-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88227-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88227-124">CommonParameters</span></span>
<span data-ttu-id="88227-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88227-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88227-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88227-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88227-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="88227-127">INPUTS</span></span>

### <span data-ttu-id="88227-128">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="88227-128">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="88227-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="88227-129">OUTPUTS</span></span>

### <span data-ttu-id="88227-130">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="88227-130">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="88227-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="88227-131">NOTES</span></span>
* <span data-ttu-id="88227-132">Das Cmdlet **Resume-AzureRmSqlDatabase** funktioniert nur in Azure SQL Data Warehouse-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="88227-132">The **Resume-AzureRmSqlDatabase** cmdlet works only on Azure SQL Data Warehouse databases.</span></span> <span data-ttu-id="88227-133">Dieser Vorgang wird in Azure SQL-Datenbank Basic-, Standard-und Premium-Editionen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="88227-133">This operation is not supported on Azure SQL Database Basic, Standard and Premium editions.</span></span>

## <span data-ttu-id="88227-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="88227-134">RELATED LINKS</span></span>

[<span data-ttu-id="88227-135">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="88227-135">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="88227-136">Neu – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="88227-136">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="88227-137">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="88227-137">Remove-AzureRmSqlDatabase</span></span>](./Remove-AzureRmSqlDatabase.md)

[<span data-ttu-id="88227-138">Satz-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="88227-138">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="88227-139">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="88227-139">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="88227-140">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="88227-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


