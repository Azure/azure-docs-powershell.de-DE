---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldeleteddatabasebackup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
ms.openlocfilehash: 2358383cd7cfdbf547ae14476e788d6919baacd0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476533"
---
# <span data-ttu-id="8eb2d-101">Get-AzureRmSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="8eb2d-101">Get-AzureRmSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="8eb2d-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8eb2d-102">SYNOPSIS</span></span>
<span data-ttu-id="8eb2d-103">Ruft eine gelöschte Datenbank ab, die Sie wiederherstellen können.</span><span class="sxs-lookup"><span data-stu-id="8eb2d-103">Gets a deleted database that you can restore.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8eb2d-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8eb2d-104">SYNTAX</span></span>

```
Get-AzureRmSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>]
 [[-DeletionDate] <DateTime>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8eb2d-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8eb2d-105">DESCRIPTION</span></span>
<span data-ttu-id="8eb2d-106">Das Cmdlet " **Get-AzureRMSqlDeletedDatabaseBackup** " Ruft eine angegebene gelöschte SQL-Datenbanksicherung ab, die Sie wiederherstellen können, oder alle gelöschten Sicherungen, die wiederhergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="8eb2d-106">The **Get-AzureRMSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>

<span data-ttu-id="8eb2d-107">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8eb2d-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="8eb2d-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8eb2d-108">EXAMPLES</span></span>

### <span data-ttu-id="8eb2d-109">Beispiel 1: Abrufen aller gelöschten Datenbanksicherungen auf einem Server</span><span class="sxs-lookup"><span data-stu-id="8eb2d-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="8eb2d-110">Dieser Befehl ruft alle gelöschten Datenbanksicherungen auf einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="8eb2d-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="8eb2d-111">Beispiel 2: Abrufen einer angegebenen gelöschten Datenbanksicherung</span><span class="sxs-lookup"><span data-stu-id="8eb2d-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="8eb2d-112">Mit diesem Befehl wird die gelöschte Datenbanksicherung für ContosoDatabase abgerufen.</span><span class="sxs-lookup"><span data-stu-id="8eb2d-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="8eb2d-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8eb2d-113">PARAMETERS</span></span>

### <span data-ttu-id="8eb2d-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="8eb2d-114">-DatabaseName</span></span>
<span data-ttu-id="8eb2d-115">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="8eb2d-115">Specifies the name of the database.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eb2d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eb2d-116">-DefaultProfile</span></span>
<span data-ttu-id="8eb2d-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="8eb2d-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8eb2d-118">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="8eb2d-118">-DeletionDate</span></span>
<span data-ttu-id="8eb2d-119">Gibt das Datum als **DateTime** -Objekt an, in dem die Datenbank gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="8eb2d-119">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="8eb2d-120">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8eb2d-120">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8eb2d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8eb2d-121">-ResourceGroupName</span></span>
<span data-ttu-id="8eb2d-122">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="8eb2d-122">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="8eb2d-123">-Servername</span><span class="sxs-lookup"><span data-stu-id="8eb2d-123">-ServerName</span></span>
<span data-ttu-id="8eb2d-124">Gibt den Namen des Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="8eb2d-124">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="8eb2d-125">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8eb2d-125">-Confirm</span></span>
<span data-ttu-id="8eb2d-126">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8eb2d-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8eb2d-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eb2d-127">-WhatIf</span></span>
<span data-ttu-id="8eb2d-128">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8eb2d-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8eb2d-129">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8eb2d-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8eb2d-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eb2d-130">CommonParameters</span></span>
<span data-ttu-id="8eb2d-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eb2d-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eb2d-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eb2d-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eb2d-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8eb2d-133">INPUTS</span></span>

### <span data-ttu-id="8eb2d-134">Keine</span><span class="sxs-lookup"><span data-stu-id="8eb2d-134">None</span></span>
<span data-ttu-id="8eb2d-135">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="8eb2d-135">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8eb2d-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8eb2d-136">OUTPUTS</span></span>

## <span data-ttu-id="8eb2d-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="8eb2d-137">NOTES</span></span>

## <span data-ttu-id="8eb2d-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8eb2d-138">RELATED LINKS</span></span>

[<span data-ttu-id="8eb2d-139">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="8eb2d-139">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="8eb2d-140">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="8eb2d-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
