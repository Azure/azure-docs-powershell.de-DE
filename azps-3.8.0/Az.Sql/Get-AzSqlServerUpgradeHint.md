---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerUpgradeHint.md
ms.openlocfilehash: 841de793c6e0c6d9213be262576dbd4f407fd947
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995480"
---
# <span data-ttu-id="776bb-101">Get-AzSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="776bb-101">Get-AzSqlServerUpgradeHint</span></span>

## <span data-ttu-id="776bb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="776bb-102">SYNOPSIS</span></span>
<span data-ttu-id="776bb-103">Ruft Informationen zu Preisstufen für das Upgrade eines Azure SQL-Datenbankservers ab.</span><span class="sxs-lookup"><span data-stu-id="776bb-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

## <span data-ttu-id="776bb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="776bb-104">SYNTAX</span></span>

```
Get-AzSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="776bb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="776bb-105">DESCRIPTION</span></span>
<span data-ttu-id="776bb-106">Das Cmdlet " **Get-AzSqlServerUpgradeHint** " ruft Preisstufen Hinweise für das Upgrade eines Azure SQL-Datenbankservers ab.</span><span class="sxs-lookup"><span data-stu-id="776bb-106">The **Get-AzSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="776bb-107">Hinweise enthalten möglicherweise den elastischen datenbankpool und eigenständige Daten Bank Hinweise.</span><span class="sxs-lookup"><span data-stu-id="776bb-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="776bb-108">Datenbanken, die sich noch im Web-und Business-Preisniveau befinden, erhalten einen Hinweis, wie Sie ein Upgrade auf die neuen Standard-, Standard-oder Premium-Preisstufen durchführen oder in den elastischen datenbankpool wechseln.</span><span class="sxs-lookup"><span data-stu-id="776bb-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="776bb-109">Dieses Cmdlet gibt Hinweise für alle auf dem angegebenen Server gehosteten Datenbanken zurück.</span><span class="sxs-lookup"><span data-stu-id="776bb-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="776bb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="776bb-110">EXAMPLES</span></span>

### <span data-ttu-id="776bb-111">Beispiel 1: Abrufen kombinierter Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="776bb-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="776bb-112">Dieser Befehl ruft kombinierte Empfehlungen für alle Datenbanken auf einem Server mit dem Namen "Server01" ab.</span><span class="sxs-lookup"><span data-stu-id="776bb-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="776bb-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="776bb-113">PARAMETERS</span></span>

### <span data-ttu-id="776bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="776bb-114">-DefaultProfile</span></span>
<span data-ttu-id="776bb-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="776bb-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="776bb-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="776bb-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="776bb-117">Gibt an, ob Datenbanken, die in elastischen Daten Bank Pools enthalten sind, zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="776bb-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="776bb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="776bb-118">-ResourceGroupName</span></span>
<span data-ttu-id="776bb-119">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="776bb-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="776bb-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="776bb-120">-ServerName</span></span>
<span data-ttu-id="776bb-121">Gibt den Namen des Servers an, für den dieses Cmdlet einen Upgrade-Hinweis erhält.</span><span class="sxs-lookup"><span data-stu-id="776bb-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="776bb-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="776bb-122">-Confirm</span></span>
<span data-ttu-id="776bb-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="776bb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="776bb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="776bb-124">-WhatIf</span></span>
<span data-ttu-id="776bb-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="776bb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="776bb-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="776bb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="776bb-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="776bb-127">CommonParameters</span></span>
<span data-ttu-id="776bb-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="776bb-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="776bb-129">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="776bb-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="776bb-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="776bb-130">INPUTS</span></span>

### <span data-ttu-id="776bb-131">System. String</span><span class="sxs-lookup"><span data-stu-id="776bb-131">System.String</span></span>

### <span data-ttu-id="776bb-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="776bb-132">System.Boolean</span></span>

## <span data-ttu-id="776bb-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="776bb-133">OUTPUTS</span></span>

### <span data-ttu-id="776bb-134">Microsoft. Azure. Commands. SQL. ServiceTierAdvisor. Model. UpgradeServerHint</span><span class="sxs-lookup"><span data-stu-id="776bb-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="776bb-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="776bb-135">NOTES</span></span>

## <span data-ttu-id="776bb-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="776bb-136">RELATED LINKS</span></span>

[<span data-ttu-id="776bb-137">Get-AzSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="776bb-137">Get-AzSqlDatabaseExpanded</span></span>](./Get-AzSqlDatabaseExpanded.md)

[<span data-ttu-id="776bb-138">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="776bb-138">Get-AzSqlElasticPoolRecommendation</span></span>](./Get-AzSqlElasticPoolRecommendation.md)

[<span data-ttu-id="776bb-139">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="776bb-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


