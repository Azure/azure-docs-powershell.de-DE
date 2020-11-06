---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: BFEAE1F7-56E3-4EA9-B39A-ED09582C8A09
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverupgradehint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerUpgradeHint.md
ms.openlocfilehash: 597156e101a9d16eff36d05fae71b32e0033ad6f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495602"
---
# <span data-ttu-id="5aada-101">Get-AzureRmSqlServerUpgradeHint</span><span class="sxs-lookup"><span data-stu-id="5aada-101">Get-AzureRmSqlServerUpgradeHint</span></span>

## <span data-ttu-id="5aada-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5aada-102">SYNOPSIS</span></span>
<span data-ttu-id="5aada-103">Ruft Informationen zu Preisstufen für das Upgrade eines Azure SQL-Datenbankservers ab.</span><span class="sxs-lookup"><span data-stu-id="5aada-103">Gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5aada-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5aada-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerUpgradeHint [-ServerName] <String> [-ExcludeElasticPools <Boolean>]
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5aada-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5aada-105">DESCRIPTION</span></span>
<span data-ttu-id="5aada-106">Das Cmdlet " **Get-AzureRmSqlServerUpgradeHint** " ruft Preisstufen Hinweise für das Upgrade eines Azure SQL-Datenbankservers ab.</span><span class="sxs-lookup"><span data-stu-id="5aada-106">The **Get-AzureRmSqlServerUpgradeHint** cmdlet gets pricing tier hints for upgrading an Azure SQL Database server.</span></span>
<span data-ttu-id="5aada-107">Hinweise enthalten möglicherweise den elastischen datenbankpool und eigenständige Daten Bank Hinweise.</span><span class="sxs-lookup"><span data-stu-id="5aada-107">Hints may contain the elastic database pool and stand-alone database hints.</span></span>
<span data-ttu-id="5aada-108">Datenbanken, die sich noch im Web-und Business-Preisniveau befinden, erhalten einen Hinweis, wie Sie ein Upgrade auf die neuen Standard-, Standard-oder Premium-Preisstufen durchführen oder in den elastischen datenbankpool wechseln.</span><span class="sxs-lookup"><span data-stu-id="5aada-108">Databases that are still in Web and Business pricing tiers get a hint to upgrade to the new Basic, Standard, or Premium pricing tiers, or to go into the elastic database pool.</span></span>
<span data-ttu-id="5aada-109">Dieses Cmdlet gibt Hinweise für alle auf dem angegebenen Server gehosteten Datenbanken zurück.</span><span class="sxs-lookup"><span data-stu-id="5aada-109">This cmdlet returns hints for all databases hosted on the specified server.</span></span>

## <span data-ttu-id="5aada-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5aada-110">EXAMPLES</span></span>

### <span data-ttu-id="5aada-111">Beispiel 1: Abrufen kombinierter Empfehlungen</span><span class="sxs-lookup"><span data-stu-id="5aada-111">Example 1: Get combined recommendations</span></span>
```
PS C:\>Get-AzureRmSqlServerUpgradeHint -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ElasticPools Databases           
------------ ---------           
{}           {database01, database02}
```

<span data-ttu-id="5aada-112">Dieser Befehl ruft kombinierte Empfehlungen für alle Datenbanken auf einem Server mit dem Namen "Server01" ab.</span><span class="sxs-lookup"><span data-stu-id="5aada-112">This command gets combined recommendations for all the databases on a server named Server01.</span></span>

## <span data-ttu-id="5aada-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5aada-113">PARAMETERS</span></span>

### <span data-ttu-id="5aada-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5aada-114">-DefaultProfile</span></span>
<span data-ttu-id="5aada-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5aada-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5aada-116">-ExcludeElasticPools</span><span class="sxs-lookup"><span data-stu-id="5aada-116">-ExcludeElasticPools</span></span>
<span data-ttu-id="5aada-117">Gibt an, ob Datenbanken, die in elastischen Daten Bank Pools enthalten sind, zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5aada-117">Indicates whether databases that are included in elastic database pools should be returned.</span></span>

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

### <span data-ttu-id="5aada-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5aada-118">-ResourceGroupName</span></span>
<span data-ttu-id="5aada-119">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="5aada-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="5aada-120">-Servername</span><span class="sxs-lookup"><span data-stu-id="5aada-120">-ServerName</span></span>
<span data-ttu-id="5aada-121">Gibt den Namen des Servers an, für den dieses Cmdlet einen Upgrade-Hinweis erhält.</span><span class="sxs-lookup"><span data-stu-id="5aada-121">Specifies the name of the server for which this cmdlet gets an upgrade hint.</span></span>

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

### <span data-ttu-id="5aada-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5aada-122">-Confirm</span></span>
<span data-ttu-id="5aada-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5aada-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5aada-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5aada-124">-WhatIf</span></span>
<span data-ttu-id="5aada-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5aada-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5aada-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5aada-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5aada-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5aada-127">CommonParameters</span></span>
<span data-ttu-id="5aada-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5aada-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5aada-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5aada-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5aada-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5aada-130">INPUTS</span></span>

### <span data-ttu-id="5aada-131">System. String</span><span class="sxs-lookup"><span data-stu-id="5aada-131">System.String</span></span>

### <span data-ttu-id="5aada-132">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5aada-132">System.Boolean</span></span>

## <span data-ttu-id="5aada-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5aada-133">OUTPUTS</span></span>

### <span data-ttu-id="5aada-134">Microsoft. Azure. Commands. SQL. ServiceTierAdvisor. Model. UpgradeServerHint</span><span class="sxs-lookup"><span data-stu-id="5aada-134">Microsoft.Azure.Commands.Sql.ServiceTierAdvisor.Model.UpgradeServerHint</span></span>

## <span data-ttu-id="5aada-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="5aada-135">NOTES</span></span>

## <span data-ttu-id="5aada-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5aada-136">RELATED LINKS</span></span>

[<span data-ttu-id="5aada-137">Get-AzureRmSqlDatabaseExpanded</span><span class="sxs-lookup"><span data-stu-id="5aada-137">Get-AzureRmSqlDatabaseExpanded</span></span>](./Get-AzureRmSqlDatabaseExpanded.md)

[<span data-ttu-id="5aada-138">Get-AzureRmSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="5aada-138">Get-AzureRmSqlElasticPoolRecommendation</span></span>](./Get-AzureRmSqlElasticPoolRecommendation.md)

[<span data-ttu-id="5aada-139">SQL-Datenbank-Dokumentation</span><span class="sxs-lookup"><span data-stu-id="5aada-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


