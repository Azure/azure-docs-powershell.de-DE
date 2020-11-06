---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 62B9754D-5EBF-4BEE-B07A-3E508C918F03
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRMSqlDeletedDatabaseBackup.md
ms.openlocfilehash: 9ffccf1122ac9919758883100eacce7933f5fea7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481478"
---
# <span data-ttu-id="75cbc-101">Get-AzureRmSqlDeletedDatabaseBackup</span><span class="sxs-lookup"><span data-stu-id="75cbc-101">Get-AzureRmSqlDeletedDatabaseBackup</span></span>

## <span data-ttu-id="75cbc-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="75cbc-102">SYNOPSIS</span></span>
<span data-ttu-id="75cbc-103">Ruft eine gelöschte Datenbank ab, die Sie wiederherstellen können.</span><span class="sxs-lookup"><span data-stu-id="75cbc-103">Gets a deleted database that you can restore.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="75cbc-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="75cbc-104">SYNTAX</span></span>

```
Get-AzureRmSqlDeletedDatabaseBackup [-ServerName] <String> [[-DatabaseName] <String>]
 [[-DeletionDate] <DateTime>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="75cbc-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="75cbc-105">DESCRIPTION</span></span>
<span data-ttu-id="75cbc-106">Das Cmdlet " **Get-AzureRMSqlDeletedDatabaseBackup** " Ruft eine angegebene gelöschte SQL-Datenbanksicherung ab, die Sie wiederherstellen können, oder alle gelöschten Sicherungen, die wiederhergestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="75cbc-106">The **Get-AzureRMSqlDeletedDatabaseBackup** cmdlet gets a specified deleted SQL database backup that you can restore, or all deleted backups that you can restore.</span></span>

<span data-ttu-id="75cbc-107">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="75cbc-107">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="75cbc-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="75cbc-108">EXAMPLES</span></span>

### <span data-ttu-id="75cbc-109">Beispiel 1: Abrufen aller gelöschten Datenbanksicherungen auf einem Server</span><span class="sxs-lookup"><span data-stu-id="75cbc-109">Example 1: Get all deleted database backups on a server</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer"
```

<span data-ttu-id="75cbc-110">Dieser Befehl ruft alle gelöschten Datenbanksicherungen auf einem Server ab.</span><span class="sxs-lookup"><span data-stu-id="75cbc-110">This command gets all deleted database backups on a server.</span></span>

### <span data-ttu-id="75cbc-111">Beispiel 2: Abrufen einer angegebenen gelöschten Datenbanksicherung</span><span class="sxs-lookup"><span data-stu-id="75cbc-111">Example 2: Get a specified deleted database backup</span></span>
```
PS C:\>Get-AzureRMSqlDeletedDatabaseBackup -ResourceGroupName "ContosoResourceGroup" -ServerName "ContosoServer" -DatabaseName "ContosoDatabase"
```

<span data-ttu-id="75cbc-112">Mit diesem Befehl wird die gelöschte Datenbanksicherung für ContosoDatabase abgerufen.</span><span class="sxs-lookup"><span data-stu-id="75cbc-112">This command gets the deleted database backup for ContosoDatabase.</span></span>

## <span data-ttu-id="75cbc-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="75cbc-113">PARAMETERS</span></span>

### <span data-ttu-id="75cbc-114">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="75cbc-114">-DatabaseName</span></span>
<span data-ttu-id="75cbc-115">Gibt den Namen der Datenbank an.</span><span class="sxs-lookup"><span data-stu-id="75cbc-115">Specifies the name of the database.</span></span>

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

### <span data-ttu-id="75cbc-116">-DeletionDate</span><span class="sxs-lookup"><span data-stu-id="75cbc-116">-DeletionDate</span></span>
<span data-ttu-id="75cbc-117">Gibt das Datum als **DateTime** -Objekt an, in dem die Datenbank gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="75cbc-117">Specifies the date, as a **DateTime** object, that the database was deleted.</span></span>
<span data-ttu-id="75cbc-118">Verwenden Sie das Get-Date-Cmdlet, um ein **DateTime** -Objekt abzurufen.</span><span class="sxs-lookup"><span data-stu-id="75cbc-118">To get a **DateTime** object, use the Get-Date cmdlet.</span></span>

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

### <span data-ttu-id="75cbc-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="75cbc-119">-ResourceGroupName</span></span>
<span data-ttu-id="75cbc-120">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="75cbc-120">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="75cbc-121">-Servername</span><span class="sxs-lookup"><span data-stu-id="75cbc-121">-ServerName</span></span>
<span data-ttu-id="75cbc-122">Gibt den Namen des Datenbankservers an.</span><span class="sxs-lookup"><span data-stu-id="75cbc-122">Specifies the name of the database server.</span></span>

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

### <span data-ttu-id="75cbc-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="75cbc-123">-Confirm</span></span>
<span data-ttu-id="75cbc-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="75cbc-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="75cbc-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="75cbc-125">-WhatIf</span></span>
<span data-ttu-id="75cbc-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="75cbc-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="75cbc-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="75cbc-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="75cbc-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="75cbc-128">-DefaultProfile</span></span>
<span data-ttu-id="75cbc-129">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="75cbc-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="75cbc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="75cbc-130">CommonParameters</span></span>
<span data-ttu-id="75cbc-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="75cbc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="75cbc-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="75cbc-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="75cbc-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="75cbc-133">INPUTS</span></span>

## <span data-ttu-id="75cbc-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="75cbc-134">OUTPUTS</span></span>

## <span data-ttu-id="75cbc-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="75cbc-135">NOTES</span></span>

## <span data-ttu-id="75cbc-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="75cbc-136">RELATED LINKS</span></span>

[<span data-ttu-id="75cbc-137">Get-AzureRmSqlDatabase</span><span class="sxs-lookup"><span data-stu-id="75cbc-137">Get-AzureRmSqlDatabase</span></span>](./Get-AzureRmSqlDatabase.md)

[<span data-ttu-id="75cbc-138">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="75cbc-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
