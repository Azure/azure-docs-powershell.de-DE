---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 7e0d8e55b5a4ab3ab22081fde94bac10f4550730
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307851"
---
# <span data-ttu-id="35fca-101">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="35fca-101">Get-AzSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="35fca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="35fca-102">SYNOPSIS</span></span>
<span data-ttu-id="35fca-103">Hier erhalten Sie Empfehlungen für den Pool.</span><span class="sxs-lookup"><span data-stu-id="35fca-103">Gets elastic pool recommendations.</span></span>

## <span data-ttu-id="35fca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="35fca-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="35fca-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="35fca-105">DESCRIPTION</span></span>
<span data-ttu-id="35fca-106">Das **Cmdlet "Get-AzSqlElasticPoolRecommendation"** ruft Poolempfehlungen für einen Server ab.</span><span class="sxs-lookup"><span data-stu-id="35fca-106">The **Get-AzSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="35fca-107">Diese Empfehlungen enthalten die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="35fca-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="35fca-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="35fca-108">DatabaseCollection.</span></span> <span data-ttu-id="35fca-109">Sammlung von Datenbanknamen, die zum Pool gehören.</span><span class="sxs-lookup"><span data-stu-id="35fca-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="35fca-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="35fca-110">DatabaseDtuMin.</span></span> <span data-ttu-id="35fca-111">DTU (Data Transmission Unit) ist eine Garantie für Datenbanken im Pool.</span><span class="sxs-lookup"><span data-stu-id="35fca-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="35fca-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="35fca-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="35fca-113">DTU cap for databases in the pool.</span><span class="sxs-lookup"><span data-stu-id="35fca-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="35fca-114">Dtu.</span><span class="sxs-lookup"><span data-stu-id="35fca-114">Dtu.</span></span> <span data-ttu-id="35fca-115">DTU-Garantie für den Pool.</span><span class="sxs-lookup"><span data-stu-id="35fca-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="35fca-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="35fca-116">StorageMb.</span></span> <span data-ttu-id="35fca-117">Speicher in Megabyte für den Pool.</span><span class="sxs-lookup"><span data-stu-id="35fca-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="35fca-118">Edition.</span><span class="sxs-lookup"><span data-stu-id="35fca-118">Edition.</span></span> <span data-ttu-id="35fca-119">Edition für den Pool im Pool.</span><span class="sxs-lookup"><span data-stu-id="35fca-119">Edition for the elastic pool.</span></span> <span data-ttu-id="35fca-120">Die zulässigen Werte für diesen Parameter sind: Standard, Standard und Premium.</span><span class="sxs-lookup"><span data-stu-id="35fca-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="35fca-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="35fca-121">IncludeAllDatabases.</span></span> <span data-ttu-id="35fca-122">Gibt an, ob alle Datenbanken im Pool zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="35fca-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="35fca-123">Name.</span><span class="sxs-lookup"><span data-stu-id="35fca-123">Name.</span></span> <span data-ttu-id="35fca-124">Name des Poolpools.</span><span class="sxs-lookup"><span data-stu-id="35fca-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="35fca-125">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="35fca-125">EXAMPLES</span></span>

### <span data-ttu-id="35fca-126">Beispiel 1: Erhalten von Empfehlungen für einen Server</span><span class="sxs-lookup"><span data-stu-id="35fca-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="35fca-127">Dieser Befehl ruft die Empfehlungen des Poolpools für den Server mit dem Namen Server01 ab.</span><span class="sxs-lookup"><span data-stu-id="35fca-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="35fca-128">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="35fca-128">PARAMETERS</span></span>

### <span data-ttu-id="35fca-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35fca-129">-DefaultProfile</span></span>
<span data-ttu-id="35fca-130">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="35fca-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35fca-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35fca-131">-ResourceGroupName</span></span>
<span data-ttu-id="35fca-132">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="35fca-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="35fca-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="35fca-133">-ServerName</span></span>
<span data-ttu-id="35fca-134">Gibt den Namen des Servers an, für den dieses Cmdlet Empfehlungen erhält.</span><span class="sxs-lookup"><span data-stu-id="35fca-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="35fca-135">-Confirm</span><span class="sxs-lookup"><span data-stu-id="35fca-135">-Confirm</span></span>
<span data-ttu-id="35fca-136">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="35fca-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35fca-137">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="35fca-137">-WhatIf</span></span>
<span data-ttu-id="35fca-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="35fca-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="35fca-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="35fca-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35fca-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35fca-140">CommonParameters</span></span>
<span data-ttu-id="35fca-141">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35fca-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35fca-142">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="35fca-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35fca-143">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="35fca-143">INPUTS</span></span>

### <span data-ttu-id="35fca-144">System.String</span><span class="sxs-lookup"><span data-stu-id="35fca-144">System.String</span></span>

## <span data-ttu-id="35fca-145">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="35fca-145">OUTPUTS</span></span>

### <span data-ttu-id="35fca-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span><span class="sxs-lookup"><span data-stu-id="35fca-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="35fca-147">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="35fca-147">NOTES</span></span>

## <span data-ttu-id="35fca-148">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="35fca-148">RELATED LINKS</span></span>
