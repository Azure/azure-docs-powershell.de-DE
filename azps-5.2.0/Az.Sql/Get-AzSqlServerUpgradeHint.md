---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
ms.openlocfilehash: 841de793c6e0c6d9213be262576dbd4f407fd947
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302136"
---
# <span data-ttu-id="78c46-101">Get-AzSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="78c46-101">Get-AzSqlServerUpgradeHint</span></span>

## <span data-ttu-id="78c46-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78c46-102">SYNOPSIS</span></span>
<span data-ttu-id="78c46-103">Ruft Preisstufenhinweise für das Upgrade eines Azure SQL Datenbankservers ab.</span><span class="sxs-lookup"><span data-stu-id="78c46-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

## <span data-ttu-id="78c46-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="78c46-104">SYNTAX</span></span>

```
Get-AzSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="78c46-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="78c46-105">DESCRIPTION</span></span>
<span data-ttu-id="78c46-106">Das **Cmdlet "Get-AzSqlServerUpgradeHint"** ruft Preisstufenhinweise für das Upgrade eines Azure SQL Datenbankservers ab.</span><span class="sxs-lookup"><span data-stu-id="78c46-106">The **Get-AzSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="78c46-107">Hinweise können den Datenbankpool der Datenbank und eigenständige Datenbankhinweise enthalten.</span><span class="sxs-lookup"><span data-stu-id="78c46-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="78c46-108">Datenbanken, die sich noch auf den Preisstufen "Web" und "Business" befinden, erhalten einen Hinweis auf ein Upgrade auf die neuen Preisstufen "Basic", "Standard" oder "Premium" oder zum Wechseln in den Kalkulationsdatenbankpool.</span><span class="sxs-lookup"><span data-stu-id="78c46-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="78c46-109">Dieses Cmdlet gibt Hinweise für alle Datenbanken zurück, die auf dem angegebenen Server gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="78c46-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="78c46-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="78c46-110">EXAMPLES</span></span>

### <span data-ttu-id="78c46-111">Beispiel 1: Kombinierte Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="78c46-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="78c46-112">Dieser Befehl ruft kombinierte Empfehlungen für alle Datenbanken auf einem Server mit dem Namen Server01 ab.</span><span class="sxs-lookup"><span data-stu-id="78c46-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="78c46-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="78c46-113">PARAMETERS</span></span>

### <span data-ttu-id="78c46-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78c46-114">-DefaultProfile</span></span>
<span data-ttu-id="78c46-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="78c46-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78c46-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="78c46-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="78c46-117">Gibt an, ob Datenbanken, die in Datenbankdatenbankpools enthalten sind, zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="78c46-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="78c46-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78c46-118">-ResourceGroupName</span></span>
<span data-ttu-id="78c46-119">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="78c46-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="78c46-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="78c46-120">-ServerName</span></span>
<span data-ttu-id="78c46-121">Gibt den Namen des Servers an, für den dieses Cmdlet einen Upgradehinweis erhält.</span><span class="sxs-lookup"><span data-stu-id="78c46-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="78c46-122">-Confirm</span><span class="sxs-lookup"><span data-stu-id="78c46-122">-Confirm</span></span>
<span data-ttu-id="78c46-123">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="78c46-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78c46-124">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="78c46-124">-WhatIf</span></span>
<span data-ttu-id="78c46-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="78c46-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78c46-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="78c46-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78c46-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78c46-127">CommonParameters</span></span>
<span data-ttu-id="78c46-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="78c46-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78c46-129">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="78c46-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78c46-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="78c46-130">INPUTS</span></span>

### <span data-ttu-id="78c46-131">System.String</span><span class="sxs-lookup"><span data-stu-id="78c46-131">System.String</span></span>

### <span data-ttu-id="78c46-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="78c46-132">System.Boolean</span></span>

## <span data-ttu-id="78c46-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="78c46-133">OUTPUTS</span></span>

### <span data-ttu-id="78c46-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span><span class="sxs-lookup"><span data-stu-id="78c46-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="78c46-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="78c46-135">NOTES</span></span>

## <span data-ttu-id="78c46-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="78c46-136">RELATED LINKS</span></span>

[<span data-ttu-id="78c46-137">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="78c46-137">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="78c46-138">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="78c46-138">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

[<span data-ttu-id="78c46-139">SQL Datenbankdokumentation</span><span class="sxs-lookup"><span data-stu-id="78c46-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


