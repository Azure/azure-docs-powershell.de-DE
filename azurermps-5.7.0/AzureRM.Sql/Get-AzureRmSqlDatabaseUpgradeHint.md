---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseUpgradeHint.md
ms.openlocfilehash: c1be1a730c9e93778f9632477234d375813708dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480865"
---
# <span data-ttu-id="67a66-101">Get-AzureRmSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="67a66-101">Get-AzureRmSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="67a66-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67a66-102">SYNOPSIS</span></span>
<span data-ttu-id="67a66-103">Ruft Preisstufen Hinweise für eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="67a66-103">Gets pricing tier hints for a database.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67a66-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67a66-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67a66-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67a66-105">DESCRIPTION</span></span>
<span data-ttu-id="67a66-106">Das Cmdlet " **Get-AzureRmSqlDatabaseUpgradeHint** " ruft Preisstufen Hinweise für das Upgrade einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="67a66-106">The **Get-AzureRmSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="67a66-107">Datenbanken, die sich noch im Web-und Business-Preisniveau befinden, erhalten den Hinweis, dass Sie ein Upgrade auf die neuen Standard-, Standard-oder Premium-Preisstufen durchführen können.</span><span class="sxs-lookup"><span data-stu-id="67a66-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>

<span data-ttu-id="67a66-108">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="67a66-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="67a66-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67a66-109">EXAMPLES</span></span>

### <span data-ttu-id="67a66-110">Beispiel 1: Abrufen von Empfehlungen für alle Datenbanken auf einem Server</span><span class="sxs-lookup"><span data-stu-id="67a66-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="67a66-111">Dieser Befehl gibt Aktualisierungshinweise für alle Datenbanken auf dem Server mit dem Namen "Server01" zurück.</span><span class="sxs-lookup"><span data-stu-id="67a66-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="67a66-112">Beispiel 2: Abrufen von Empfehlungen für eine bestimmte Datenbank</span><span class="sxs-lookup"><span data-stu-id="67a66-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="67a66-113">Dieser Befehl gibt Aktualisierungshinweise für eine bestimmte Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="67a66-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="67a66-114">Beispiel 3: Abrufen einer Empfehlung für alle Datenbanken, die sich nicht in einem elastischen datenbankpool befinden</span><span class="sxs-lookup"><span data-stu-id="67a66-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\>Get-AzureRmSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="67a66-115">Dieser Befehl gibt Aktualisierungshinweise für alle Datenbanken zurück, die sich nicht in einem elastischen datenbankpool befinden.</span><span class="sxs-lookup"><span data-stu-id="67a66-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

## <span data-ttu-id="67a66-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="67a66-116">PARAMETERS</span></span>

### <span data-ttu-id="67a66-117">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="67a66-117">-DatabaseName</span></span>
<span data-ttu-id="67a66-118">Gibt den Namen der SQL-Datenbank an, für die dieses Cmdlet einen Upgrade-Hinweis erhält.</span><span class="sxs-lookup"><span data-stu-id="67a66-118">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="67a66-119">Wenn Sie keine Datenbank angeben, erhält dieses Cmdlet Hinweise für alle Datenbanken auf dem logischen Server.</span><span class="sxs-lookup"><span data-stu-id="67a66-119">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67a66-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67a66-120">-DefaultProfile</span></span>
<span data-ttu-id="67a66-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="67a66-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67a66-122">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="67a66-122">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="67a66-123">Gibt an, ob Datenbanken in elastischen Daten Bank Pools von den zurückgegebenen Empfehlungen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="67a66-123">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67a66-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67a66-124">-ResourceGroupName</span></span>
<span data-ttu-id="67a66-125">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="67a66-125">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="67a66-126">-Servername</span><span class="sxs-lookup"><span data-stu-id="67a66-126">-ServerName</span></span>
<span data-ttu-id="67a66-127">Gibt den Namen des Servers an, der die Datenbank hostet, für die dieses Cmdlet einen Upgrade-Hinweis erhält.</span><span class="sxs-lookup"><span data-stu-id="67a66-127">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="67a66-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="67a66-128">-Confirm</span></span>
<span data-ttu-id="67a66-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="67a66-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67a66-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67a66-130">-WhatIf</span></span>
<span data-ttu-id="67a66-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67a66-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67a66-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67a66-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67a66-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67a66-133">CommonParameters</span></span>
<span data-ttu-id="67a66-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67a66-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67a66-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67a66-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67a66-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67a66-136">INPUTS</span></span>

### <span data-ttu-id="67a66-137">Keine</span><span class="sxs-lookup"><span data-stu-id="67a66-137">None</span></span>
<span data-ttu-id="67a66-138">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="67a66-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="67a66-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67a66-139">OUTPUTS</span></span>

## <span data-ttu-id="67a66-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="67a66-140">NOTES</span></span>

## <span data-ttu-id="67a66-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67a66-141">RELATED LINKS</span></span>

[<span data-ttu-id="67a66-142">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="67a66-142">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="67a66-143">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="67a66-143">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)


