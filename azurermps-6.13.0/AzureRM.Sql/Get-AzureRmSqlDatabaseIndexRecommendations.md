---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseindexrecommendations
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseIndexRecommendations.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseIndexRecommendations.md
ms.openlocfilehash: 9180b89e54f84d2b457de79c400b7d6aa8259d28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495634"
---
# <span data-ttu-id="ce894-101">Get-AzureRmSqlDatabaseIndexRecommendations</span><span class="sxs-lookup"><span data-stu-id="ce894-101">Get-AzureRmSqlDatabaseIndexRecommendations</span></span>

## <span data-ttu-id="ce894-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ce894-102">SYNOPSIS</span></span>
<span data-ttu-id="ce894-103">Ruft die empfohlenen Indexvorgänge für einen Server oder eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="ce894-103">Gets the recommended index operations for a server or database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce894-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ce894-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseIndexRecommendations -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce894-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce894-105">DESCRIPTION</span></span>
<span data-ttu-id="ce894-106">Das Cmdlet " **Get-AzureRmSqlDatabaseIndexRecommendations** " Ruft die empfohlenen Indexvorgänge für einen Azure SQL-Datenbankserver oder eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="ce894-106">The **Get-AzureRmSqlDatabaseIndexRecommendations** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="ce894-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ce894-107">EXAMPLES</span></span>

### <span data-ttu-id="ce894-108">Beispiel 1: Abrufen von Indexempfehlungen für alle Datenbanken auf dem Server</span><span class="sxs-lookup"><span data-stu-id="ce894-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="ce894-109">Dieser Befehl gibt Indexempfehlungen für alle Datenbanken auf dem Server Server01 zurück.</span><span class="sxs-lookup"><span data-stu-id="ce894-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="ce894-110">Beispiel 2: Abrufen von Indexempfehlungen für eine bestimmte Datenbank</span><span class="sxs-lookup"><span data-stu-id="ce894-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="ce894-111">Dieser Befehl gibt Indexempfehlungen für eine bestimmte Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="ce894-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="ce894-112">Beispiel 3: Abrufen einer einzelnen Indexempfehlung nach Name</span><span class="sxs-lookup"><span data-stu-id="ce894-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseIndexRecommendations -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="ce894-113">Dieser Befehl gibt eine Empfehlung für einen einzelnen Index nach Namen zurück.</span><span class="sxs-lookup"><span data-stu-id="ce894-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="ce894-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce894-114">PARAMETERS</span></span>

### <span data-ttu-id="ce894-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="ce894-115">-DatabaseName</span></span>
<span data-ttu-id="ce894-116">Gibt den Namen der Datenbank an, für die dieses Cmdlet Indexempfehlungen erhält.</span><span class="sxs-lookup"><span data-stu-id="ce894-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce894-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce894-117">-DefaultProfile</span></span>
<span data-ttu-id="ce894-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="ce894-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce894-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="ce894-119">-IndexRecommendationName</span></span>
<span data-ttu-id="ce894-120">Gibt den Namen der Indexempfehlung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="ce894-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce894-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce894-121">-ResourceGroupName</span></span>
<span data-ttu-id="ce894-122">Gibt den Namen der Ressourcengruppe an, für die der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="ce894-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="ce894-123">Dieses Cmdlet ruft Indexempfehlungen für eine von diesem Server gehostete Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="ce894-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="ce894-124">-Servername</span><span class="sxs-lookup"><span data-stu-id="ce894-124">-ServerName</span></span>
<span data-ttu-id="ce894-125">Gibt den Server an, der die Datenbank hostet, für die dieses Cmdlet Indexempfehlungen erhält.</span><span class="sxs-lookup"><span data-stu-id="ce894-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="ce894-126">-Tabellenname</span><span class="sxs-lookup"><span data-stu-id="ce894-126">-TableName</span></span>
<span data-ttu-id="ce894-127">Gibt den Namen einer Azure SQL-Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="ce894-127">Specifies the name of an Azure SQL table.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce894-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ce894-128">-Confirm</span></span>
<span data-ttu-id="ce894-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ce894-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce894-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce894-130">-WhatIf</span></span>
<span data-ttu-id="ce894-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ce894-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce894-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ce894-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce894-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce894-133">CommonParameters</span></span>
<span data-ttu-id="ce894-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce894-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce894-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce894-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce894-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ce894-136">INPUTS</span></span>

### <span data-ttu-id="ce894-137">System. String</span><span class="sxs-lookup"><span data-stu-id="ce894-137">System.String</span></span>

## <span data-ttu-id="ce894-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ce894-138">OUTPUTS</span></span>

### <span data-ttu-id="ce894-139">Microsoft. Azure. Commands. SQL. Model. IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ce894-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="ce894-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="ce894-140">NOTES</span></span>

## <span data-ttu-id="ce894-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ce894-141">RELATED LINKS</span></span>

[<span data-ttu-id="ce894-142">Anfang-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ce894-142">Start-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzureRmSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="ce894-143">Stopp-AzureRmSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="ce894-143">Stop-AzureRmSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzureRmSqlDatabaseExecuteIndexRecommendation.md)
