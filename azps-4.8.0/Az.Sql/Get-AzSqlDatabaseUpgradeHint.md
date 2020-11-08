---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: D64FB139-04E2-47BC-86FB-EEEA23839F2F
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqldatabaseupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlDatabaseUpgradeHint.md
ms.openlocfilehash: b5f94aeb66749fa9bc89a89febb0bc5597241d58
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94010454"
---
# <span data-ttu-id="0799a-101">Get-AzSqlDatabaseUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="0799a-101">Get-AzSqlDatabaseUpgradeHint</span></span>

## <span data-ttu-id="0799a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0799a-102">SYNOPSIS</span></span>
<span data-ttu-id="0799a-103">Ruft Preisstufen Hinweise für eine Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="0799a-103">Gets pricing tier hints for a database.</span></span>

## <span data-ttu-id="0799a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0799a-104">SYNTAX</span></span>

```
Get-AzSqlDatabaseUpgradeHint [-ServerName] <String> [-DatabaseName <String>]
 [-ExcludeElasticPoolCandidates <Boolean>] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0799a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0799a-105">DESCRIPTION</span></span>
<span data-ttu-id="0799a-106">Das Cmdlet " **Get-AzSqlDatabaseUpgradeHint** " ruft Preisstufen Hinweise für das Upgrade einer Azure SQL-Datenbank ab.</span><span class="sxs-lookup"><span data-stu-id="0799a-106">The **Get-AzSqlDatabaseUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database.</span></span>
<span data-ttu-id="0799a-107">Datenbanken, die sich noch im Web-und Business-Preisniveau befinden, erhalten den Hinweis, dass Sie ein Upgrade auf die neuen Standard-, Standard-oder Premium-Preisstufen durchführen können.</span><span class="sxs-lookup"><span data-stu-id="0799a-107">Databases that are still in Web and Business pricing tiers get the hint to upgrade to the new Basic, Standard, or Premium pricing tiers.</span></span>
<span data-ttu-id="0799a-108">Dieses Cmdlet wird auch vom SQL Server Stretch-Datenbankdienst auf Azure unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0799a-108">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="0799a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0799a-109">EXAMPLES</span></span>

### <span data-ttu-id="0799a-110">Beispiel 1: Abrufen von Empfehlungen für alle Datenbanken auf einem Server</span><span class="sxs-lookup"><span data-stu-id="0799a-110">Example 1: Get recommendations for all databases on a server</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="0799a-111">Dieser Befehl gibt Aktualisierungshinweise für alle Datenbanken auf dem Server mit dem Namen "Server01" zurück.</span><span class="sxs-lookup"><span data-stu-id="0799a-111">This command returns upgrade hints for all databases on the server named Server01.</span></span>

### <span data-ttu-id="0799a-112">Beispiel 2: Abrufen von Empfehlungen für eine bestimmte Datenbank</span><span class="sxs-lookup"><span data-stu-id="0799a-112">Example 2: Get recommendations for specific database</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01"
```

<span data-ttu-id="0799a-113">Dieser Befehl gibt Aktualisierungshinweise für eine bestimmte Datenbank zurück.</span><span class="sxs-lookup"><span data-stu-id="0799a-113">This command returns upgrade hints for a specific database.</span></span>

### <span data-ttu-id="0799a-114">Beispiel 3: Abrufen einer Empfehlung für alle Datenbanken, die sich nicht in einem elastischen datenbankpool befinden</span><span class="sxs-lookup"><span data-stu-id="0799a-114">Example 3: Get recommendation for all databases that are not in an elastic database pool</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -ExcludeElasticPoolCandidates $True
```

<span data-ttu-id="0799a-115">Dieser Befehl gibt Aktualisierungshinweise für alle Datenbanken zurück, die sich nicht in einem elastischen datenbankpool befinden.</span><span class="sxs-lookup"><span data-stu-id="0799a-115">This command returns upgrade hints for all databases that are not in an elastic database pool.</span></span>

### <span data-ttu-id="0799a-116">Beispiel 4: Abrufen von Empfehlungen für alle Datenbanken auf einem Server mithilfe von Filtern</span><span class="sxs-lookup"><span data-stu-id="0799a-116">Example 4: Get recommendations for all databases on a server using filtering</span></span>
```
PS C:\> Get-AzSqlDatabaseUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database*"
```

<span data-ttu-id="0799a-117">Dieser Befehl gibt Aktualisierungshinweise für alle Datenbanken auf dem Server mit dem Namen "Server01" zurück, die mit "Datenbank" beginnen.</span><span class="sxs-lookup"><span data-stu-id="0799a-117">This command returns upgrade hints for all databases on the server named Server01 that start with "Database".</span></span>

## <span data-ttu-id="0799a-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="0799a-118">PARAMETERS</span></span>

### <span data-ttu-id="0799a-119">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="0799a-119">-DatabaseName</span></span>
<span data-ttu-id="0799a-120">Gibt den Namen der SQL-Datenbank an, für die dieses Cmdlet einen Upgrade-Hinweis erhält.</span><span class="sxs-lookup"><span data-stu-id="0799a-120">Specifies the name of the SQL database for which this cmdlet gets an upgrade hint.</span></span>
<span data-ttu-id="0799a-121">Wenn Sie keine Datenbank angeben, erhält dieses Cmdlet Hinweise für alle Datenbanken auf dem logischen Server.</span><span class="sxs-lookup"><span data-stu-id="0799a-121">If you do not specify a database, this cmdlet gets hints for all databases on the logical server.</span></span>

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

### <span data-ttu-id="0799a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0799a-122">-DefaultProfile</span></span>
<span data-ttu-id="0799a-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="0799a-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0799a-124">-ExcludeElasticPoolCandidates</span><span class="sxs-lookup"><span data-stu-id="0799a-124">-ExcludeElasticPoolCandidates</span></span>
<span data-ttu-id="0799a-125">Gibt an, ob Datenbanken in elastischen Daten Bank Pools von den zurückgegebenen Empfehlungen ausgeschlossen werden.</span><span class="sxs-lookup"><span data-stu-id="0799a-125">Indicates whether databases in elastic database pools are excluded from the returned recommendations.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0799a-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0799a-126">-ResourceGroupName</span></span>
<span data-ttu-id="0799a-127">Gibt den Namen der Ressourcengruppe an, der die Datenbank zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="0799a-127">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="0799a-128">-Servername</span><span class="sxs-lookup"><span data-stu-id="0799a-128">-ServerName</span></span>
<span data-ttu-id="0799a-129">Gibt den Namen des Servers an, der die Datenbank hostet, für die dieses Cmdlet einen Upgrade-Hinweis erhält.</span><span class="sxs-lookup"><span data-stu-id="0799a-129">Specifies the name of the server that hosts the database for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="0799a-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="0799a-130">-Confirm</span></span>
<span data-ttu-id="0799a-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="0799a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0799a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0799a-132">-WhatIf</span></span>
<span data-ttu-id="0799a-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0799a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0799a-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="0799a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0799a-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0799a-135">CommonParameters</span></span>
<span data-ttu-id="0799a-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0799a-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0799a-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0799a-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0799a-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0799a-138">INPUTS</span></span>

### <span data-ttu-id="0799a-139">System. String</span><span class="sxs-lookup"><span data-stu-id="0799a-139">System.String</span></span>

### <span data-ttu-id="0799a-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="0799a-140">System.Boolean</span></span>

## <span data-ttu-id="0799a-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0799a-141">OUTPUTS</span></span>

### <span data-ttu-id="0799a-142">Microsoft. Azure. Management. SQL. LegacySdk. Models. RecommendedDatabaseProperties</span><span class="sxs-lookup"><span data-stu-id="0799a-142">Microsoft.Azure.Management.Sql.LegacySdk.Models.RecommendedDatabaseProperties</span></span>

## <span data-ttu-id="0799a-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="0799a-143">NOTES</span></span>

## <span data-ttu-id="0799a-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0799a-144">RELATED LINKS</span></span>

[<span data-ttu-id="0799a-145">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="0799a-145">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="0799a-146">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="0799a-146">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)


