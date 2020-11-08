---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDeletedDatabaseBackup.md
ms.openlocfilehash: d534ddc9c076d0e7c2ea611d6fdb15ae22e84846
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93996220"
---
# <span data-ttu-id="162a4-101">Get-AzSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="162a4-101">Get-AzSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="162a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="162a4-102">SYNOPSIS</span></span>
<span data-ttu-id="162a4-103">Ruft eine gelöschte Datenbank ab, die Sie wiederherstellen können.</span><span class="sxs-lookup"><span data-stu-id="162a4-103">Gets a deleted database that you can restore.</span></span>

## <span data-ttu-id="162a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="162a4-104">SYNTAX</span></span>

```
Get-AzSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>] [[-DeletionDate] <DateTime>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="162a4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="162a4-105">DESCRIPTION</span></span>
<span data-ttu-id="162a4-106">Das Cmdlet " **Get-AzSqlDeletedDatabaseBackup** " Ruft eine angegebene gelöschte SQL-Datenbanksicherung ab, die Sie wiederherstellen können, oder alle gelöschten Sicherungen, die wiederhergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="162a4-106">The **Get-AzSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>
<span data-ttu-id="162a4-107">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="162a4-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="162a4-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="162a4-108">EXAMPLES</span></span>

### <span data-ttu-id="162a4-109">Beispiel 1: Abrufen aller gelöschten Datenbanksicherungen auf einem Server</span><span class="sxs-lookup"><span data-stu-id="162a4-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="162a4-110">Dieser Befehl ruft alle gelöschten Datenbanksicherungen auf einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="162a4-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="162a4-111">Beispiel 2: Abrufen einer angegebenen gelöschten Datenbanksicherung</span><span class="sxs-lookup"><span data-stu-id="162a4-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="162a4-112">Mit diesem Befehl wird die gelöschte Datenbanksicherung für ContosoDatabase abgerufen.</span><span class="sxs-lookup"><span data-stu-id="162a4-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="162a4-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="162a4-113">PARAMETERS</span></span>

### <span data-ttu-id="162a4-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="162a4-114">-DatabaseName</span></span>
<span data-ttu-id="162a4-115">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="162a4-115">Specifies the name of the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="162a4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="162a4-116">-DefaultProfile</span></span>
<span data-ttu-id="162a4-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="162a4-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="162a4-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="162a4-118">-DeletionDate</span></span>
<span data-ttu-id="162a4-119">Gibt das Datum als **DateTime** -Objekt an, in dem die Datenbank gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="162a4-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="162a4-120">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="162a4-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="162a4-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="162a4-121">-ResourceGroupName</span></span>
<span data-ttu-id="162a4-122">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="162a4-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="162a4-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="162a4-123">-ServerName</span></span>
<span data-ttu-id="162a4-124">Gibt den Namen des Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="162a4-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="162a4-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="162a4-125">-Confirm</span></span>
<span data-ttu-id="162a4-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="162a4-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="162a4-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="162a4-127">-WhatIf</span></span>
<span data-ttu-id="162a4-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="162a4-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="162a4-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="162a4-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="162a4-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="162a4-130">CommonParameters</span></span>
<span data-ttu-id="162a4-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="162a4-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="162a4-132">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="162a4-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="162a4-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="162a4-133">INPUTS</span></span>

### <span data-ttu-id="162a4-134">System. String</span><span class="sxs-lookup"><span data-stu-id="162a4-134">System.String</span></span>

### <span data-ttu-id="162a4-135">System. Nullable ' 1 [[System. DateTime, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="162a4-135">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="162a4-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="162a4-136">OUTPUTS</span></span>

### <span data-ttu-id="162a4-137">Microsoft. Azure. Commands. SQL. Backup. Model. AzureSqlDeletedDatabaseBackupModel</span><span class="sxs-lookup"><span data-stu-id="162a4-137">Microsoft.Azure.Commands.Sql.Backup.Model.AzureSqlDeletedDatabaseBackupModel</span></span>

## <span data-ttu-id="162a4-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="162a4-138">NOTES</span></span>

## <span data-ttu-id="162a4-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="162a4-139">RELATED LINKS</span></span>

[<span data-ttu-id="162a4-140">Get-AzSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="162a4-140">Get-AzSqlDatabase</span></span>](./Get-AzSqlDatabase.md)

[<span data-ttu-id="162a4-141">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="162a4-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
