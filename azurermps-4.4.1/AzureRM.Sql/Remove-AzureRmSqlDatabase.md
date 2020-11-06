---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B396388D-F91C-4BC9-A211-ABFF5DFC1693
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlDatabase.md
ms.openlocfilehash: 1660c92ef4bef4cd832bc60506f7ef24d8927313
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505594"
---
# <span data-ttu-id="d4808-101">Remove-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d4808-101">Remove-AzureRmSqlDatabase</span></span>

## <span data-ttu-id="d4808-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d4808-102">SYNOPSIS</span></span>
<span data-ttu-id="d4808-103">Entfernt eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d4808-103">Removes an Azure SQL database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4808-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4808-104">SYNTAX</span></span>

```
Remove-AzureRmSqlDatabase [-DatabaseName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d4808-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d4808-105">DESCRIPTION</span></span>
<span data-ttu-id="d4808-106">Das Cmdlet **Remove-AzureRmSqlDatabase** entfernt eine Azure SQL-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="d4808-106">The **Remove-AzureRmSqlDatabase** cmdlet removes an Azure SQL database.</span></span>

<span data-ttu-id="d4808-107">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d4808-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="d4808-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d4808-108">EXAMPLES</span></span>

### <span data-ttu-id="d4808-109">Beispiel 1: Entfernen einer Datenbank aus einem Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="d4808-109">Example 1: Remove a database from an Azure SQL server</span></span>
```
PS C:\>Remove-AzureRmSqlDatabase -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="d4808-110">Mit diesem Befehl wird die Datenbank namens database01 vom Server Server01 entfernt.</span><span class="sxs-lookup"><span data-stu-id="d4808-110">This command removes the database named Database01 from server Server01.</span></span>

## <span data-ttu-id="d4808-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4808-111">PARAMETERS</span></span>

### <span data-ttu-id="d4808-112">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="d4808-112">-DatabaseName</span></span>
<span data-ttu-id="d4808-113">Gibt den Namen der Datenbank an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="d4808-113">Specifies the name of the database that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4808-114">-Force</span><span class="sxs-lookup"><span data-stu-id="d4808-114">-Force</span></span>
<span data-ttu-id="d4808-115">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="d4808-115">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d4808-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4808-116">-ResourceGroupName</span></span>
<span data-ttu-id="d4808-117">Gibt den Namen der Azure-Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d4808-117">Specifies the name of the Azure resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="d4808-118">-Servername</span><span class="sxs-lookup"><span data-stu-id="d4808-118">-ServerName</span></span>
<span data-ttu-id="d4808-119">Gibt den Namen des Servers an, der die Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="d4808-119">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="d4808-120">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d4808-120">-Confirm</span></span>
<span data-ttu-id="d4808-121">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4808-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4808-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d4808-122">-WhatIf</span></span>
<span data-ttu-id="d4808-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4808-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d4808-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4808-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4808-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4808-125">-DefaultProfile</span></span>
<span data-ttu-id="d4808-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d4808-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4808-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4808-127">CommonParameters</span></span>
<span data-ttu-id="d4808-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4808-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4808-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4808-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4808-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d4808-130">INPUTS</span></span>

### <span data-ttu-id="d4808-131">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d4808-131">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="d4808-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d4808-132">OUTPUTS</span></span>

### <span data-ttu-id="d4808-133">Microsoft. Azure. Commands. SQL. Database. Model. AzureSqlDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="d4808-133">Microsoft.Azure.Commands.Sql.Database.Model.AzureSqlDatabaseModel</span></span>

## <span data-ttu-id="d4808-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="d4808-134">NOTES</span></span>

## <span data-ttu-id="d4808-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d4808-135">RELATED LINKS</span></span>

[<span data-ttu-id="d4808-136">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d4808-136">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="d4808-137">Neu – AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d4808-137">New-AzureRmSqlDatabase</span></span>](./New-AzureRmSqlDatabase.md)

[<span data-ttu-id="d4808-138">Lebenslauf-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d4808-138">Resume-AzureRmSqlDatabase</span></span>](./Resume-AzureRmSqlDatabase.md)

[<span data-ttu-id="d4808-139">Satz-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d4808-139">Set-AzureRmSqlDatabase</span></span>](./Set-AzureRmSqlDatabase.md)

[<span data-ttu-id="d4808-140">Suspend-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="d4808-140">Suspend-AzureRmSqlDatabase</span></span>](./Suspend-AzureRmSqlDatabase.md)

[<span data-ttu-id="d4808-141">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="d4808-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


