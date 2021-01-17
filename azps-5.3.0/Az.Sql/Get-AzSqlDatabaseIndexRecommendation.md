---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 10656EA5-EA5F-4394-951F-BC64BE3BF6F9
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseindexrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseIndexRecommendation.md
ms.openlocfilehash: 9dd14e1f8b61978575501700346157d7c22c0111
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98374966"
---
# <span data-ttu-id="4103a-101">Get-AzSqlDatabaseIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="4103a-101">Get-AzSqlDatabaseIndexRecommendation</span></span>

## <span data-ttu-id="4103a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4103a-102">SYNOPSIS</span></span>
<span data-ttu-id="4103a-103">Ruft die empfohlenen Indexvorgänge für einen Server oder eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="4103a-103">Gets the recommended index operations for a server or database.</span></span>

## <span data-ttu-id="4103a-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4103a-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseIndexRecommendation -ServerName <String> [-DatabaseName <String>] [-TableName <String>]
 [-IndexRecommendationName <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4103a-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4103a-105">DESCRIPTION</span></span>
<span data-ttu-id="4103a-106">Das **Cmdlet "Get-AzSqlDatabaseIndexRecommendation"** ruft die empfohlenen Indexvorgänge für einen Azure SQL Datenbankserver oder eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="4103a-106">The **Get-AzSqlDatabaseIndexRecommendation** cmdlet gets the recommended index operations for an Azure SQL Database server or database.</span></span>

## <span data-ttu-id="4103a-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4103a-107">EXAMPLES</span></span>

### <span data-ttu-id="4103a-108">Beispiel 1: Erhalten von Indexempfehlungen für alle Datenbanken auf dem Server</span><span class="sxs-lookup"><span data-stu-id="4103a-108">Example 1: Get index recommendations for all databases on server</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="4103a-109">Dieser Befehl gibt Indexempfehlungen für alle Datenbanken auf Serverserver01 zurück.</span><span class="sxs-lookup"><span data-stu-id="4103a-109">This command returns index recommendations for all databases on server server01.</span></span>

### <span data-ttu-id="4103a-110">Beispiel 2: Erhalten von Indexempfehlungen für eine bestimmte Datenbank</span><span class="sxs-lookup"><span data-stu-id="4103a-110">Example 2: Get index recommendations for a specific database</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="4103a-111">Dieser Befehl gibt Indexempfehlungen für eine bestimmte Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="4103a-111">This command returns index recommendations for specific database.</span></span>

### <span data-ttu-id="4103a-112">Beispiel 3: Erhalten einer einzelnen Indexempfehlung nach Name</span><span class="sxs-lookup"><span data-stu-id="4103a-112">Example 3: Get a single index recommendation by name</span></span>
```
PS C:\>Get-AzSqlDatabaseIndexRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01" -IndexRecommendationName "INDEX_NAME"
```

<span data-ttu-id="4103a-113">Dieser Befehl gibt eine Indexempfehlung nach Name zurück.</span><span class="sxs-lookup"><span data-stu-id="4103a-113">This command returns single index recommendation by name.</span></span>

## <span data-ttu-id="4103a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4103a-114">PARAMETERS</span></span>

### <span data-ttu-id="4103a-115">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="4103a-115">-DatabaseName</span></span>
<span data-ttu-id="4103a-116">Gibt den Namen der Datenbank an, für die dieses Cmdlet Indexempfehlungen erhält.</span><span class="sxs-lookup"><span data-stu-id="4103a-116">Specifies the name of the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="4103a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4103a-117">-DefaultProfile</span></span>
<span data-ttu-id="4103a-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4103a-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4103a-119">-IndexRecommendationName</span><span class="sxs-lookup"><span data-stu-id="4103a-119">-IndexRecommendationName</span></span>
<span data-ttu-id="4103a-120">Gibt den Namen der Indexempfehlung an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="4103a-120">Specifies the name of the index recommendation that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4103a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4103a-121">-ResourceGroupName</span></span>
<span data-ttu-id="4103a-122">Gibt den Namen der Ressourcengruppe an, der der Server zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="4103a-122">Specifies the name of the resource group that the server is assigned for.</span></span>
<span data-ttu-id="4103a-123">Dieses Cmdlet erhält Indexempfehlungen für eine Datenbank, die von diesem Server gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="4103a-123">This cmdlet gets index recommendations for a database hosted by this server.</span></span>

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

### <span data-ttu-id="4103a-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="4103a-124">-ServerName</span></span>
<span data-ttu-id="4103a-125">Gibt den Server an, der die Datenbank hostet, für die dieses Cmdlet Indexempfehlungen erhält.</span><span class="sxs-lookup"><span data-stu-id="4103a-125">Specifies the server that hosts the database for which this cmdlet gets index recommendations.</span></span>

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

### <span data-ttu-id="4103a-126">-TableName</span><span class="sxs-lookup"><span data-stu-id="4103a-126">-TableName</span></span>
<span data-ttu-id="4103a-127">Gibt den Namen einer Azure SQL an.</span><span class="sxs-lookup"><span data-stu-id="4103a-127">Specifies the name of an Azure SQL table.</span></span>

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

### <span data-ttu-id="4103a-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4103a-128">-Confirm</span></span>
<span data-ttu-id="4103a-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4103a-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4103a-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="4103a-130">-WhatIf</span></span>
<span data-ttu-id="4103a-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4103a-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4103a-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4103a-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4103a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4103a-133">CommonParameters</span></span>
<span data-ttu-id="4103a-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4103a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4103a-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4103a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4103a-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4103a-136">INPUTS</span></span>

### <span data-ttu-id="4103a-137">System.String</span><span class="sxs-lookup"><span data-stu-id="4103a-137">System.String</span></span>

## <span data-ttu-id="4103a-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4103a-138">OUTPUTS</span></span>

### <span data-ttu-id="4103a-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="4103a-139">Microsoft.Azure.Commands.Sql.Model.IndexRecommendation</span></span>

## <span data-ttu-id="4103a-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="4103a-140">NOTES</span></span>

## <span data-ttu-id="4103a-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="4103a-141">RELATED LINKS</span></span>

[<span data-ttu-id="4103a-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="4103a-142">Start-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Start-AzSqlDatabaseExecuteIndexRecommendation.md)

[<span data-ttu-id="4103a-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span><span class="sxs-lookup"><span data-stu-id="4103a-143">Stop-AzSqlDatabaseExecuteIndexRecommendation</span></span>](./Stop-AzSqlDatabaseExecuteIndexRecommendation.md)
