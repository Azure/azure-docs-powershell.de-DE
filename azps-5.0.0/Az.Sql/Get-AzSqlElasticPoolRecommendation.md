---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: A1E19A66-CD70-467E-8C59-1F88453905A4
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlelasticpoolrecommendation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlElasticPoolRecommendation.md
ms.openlocfilehash: 7e0d8e55b5a4ab3ab22081fde94bac10f4550730
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94296649"
---
# <span data-ttu-id="06768-101">Get-AzSqlElasticPoolRecommendation</span><span class="sxs-lookup"><span data-stu-id="06768-101">Get-AzSqlElasticPoolRecommendation</span></span>

## <span data-ttu-id="06768-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="06768-102">SYNOPSIS</span></span>
<span data-ttu-id="06768-103">Erhält Empfehlungen für elastische Pools.</span><span class="sxs-lookup"><span data-stu-id="06768-103">Gets elastic pool recommendations.</span></span>

## <span data-ttu-id="06768-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="06768-104">SYNTAX</span></span>

```
Get-AzSqlElasticPoolRecommendation [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06768-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="06768-105">DESCRIPTION</span></span>
<span data-ttu-id="06768-106">Das Cmdlet " **Get-AzSqlElasticPoolRecommendation** " erhält elastische Pool Empfehlungen für einen Server.</span><span class="sxs-lookup"><span data-stu-id="06768-106">The **Get-AzSqlElasticPoolRecommendation** cmdlet gets elastic pool recommendations for a server.</span></span>
<span data-ttu-id="06768-107">Diese Empfehlungen umfassen die folgenden Werte:</span><span class="sxs-lookup"><span data-stu-id="06768-107">These recommendations include the following values:</span></span>
- <span data-ttu-id="06768-108">DatabaseCollection.</span><span class="sxs-lookup"><span data-stu-id="06768-108">DatabaseCollection.</span></span> <span data-ttu-id="06768-109">Eine Sammlung von Datenbanknamen, die zum Pool gehören.</span><span class="sxs-lookup"><span data-stu-id="06768-109">Collection of database names that belong to the pool.</span></span> 
- <span data-ttu-id="06768-110">DatabaseDtuMin.</span><span class="sxs-lookup"><span data-stu-id="06768-110">DatabaseDtuMin.</span></span> <span data-ttu-id="06768-111">DTU-Garantie für Datenbanken im Elastic-Pool.</span><span class="sxs-lookup"><span data-stu-id="06768-111">Data Transmission Unit (DTU) guarantee for databases in the elastic pool.</span></span> 
 <span data-ttu-id="06768-112">-- DatabaseDtuMax.</span><span class="sxs-lookup"><span data-stu-id="06768-112">-- DatabaseDtuMax.</span></span> <span data-ttu-id="06768-113">DTU-Cap für Datenbanken im Elastic-Pool.</span><span class="sxs-lookup"><span data-stu-id="06768-113">DTU cap for databases in the elastic pool.</span></span> 
- <span data-ttu-id="06768-114">DTU.</span><span class="sxs-lookup"><span data-stu-id="06768-114">Dtu.</span></span> <span data-ttu-id="06768-115">DTU-Garantie für den elastischen Pool.</span><span class="sxs-lookup"><span data-stu-id="06768-115">DTU guarantee for the elastic pool.</span></span> 
- <span data-ttu-id="06768-116">StorageMb.</span><span class="sxs-lookup"><span data-stu-id="06768-116">StorageMb.</span></span> <span data-ttu-id="06768-117">Speicherplatz in Megabyte für den elastischen Pool</span><span class="sxs-lookup"><span data-stu-id="06768-117">Storage in megabytes for the elastic pool.</span></span> 
- <span data-ttu-id="06768-118">Edition.</span><span class="sxs-lookup"><span data-stu-id="06768-118">Edition.</span></span> <span data-ttu-id="06768-119">Edition für den elastischen Pool.</span><span class="sxs-lookup"><span data-stu-id="06768-119">Edition for the elastic pool.</span></span> <span data-ttu-id="06768-120">Die akzeptablen Werte für diesen Parameter sind: Basic, Standard und Premium.</span><span class="sxs-lookup"><span data-stu-id="06768-120">The acceptable values for this parameter are: Basic, Standard, and Premium.</span></span> 
- <span data-ttu-id="06768-121">IncludeAllDatabases.</span><span class="sxs-lookup"><span data-stu-id="06768-121">IncludeAllDatabases.</span></span> <span data-ttu-id="06768-122">Gibt an, ob alle Datenbanken im Elastic-Pool zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="06768-122">Indicates whether to all databases in the elastic pool are returned.</span></span> 
- <span data-ttu-id="06768-123">Namen.</span><span class="sxs-lookup"><span data-stu-id="06768-123">Name.</span></span> <span data-ttu-id="06768-124">Name des elastischen Pools.</span><span class="sxs-lookup"><span data-stu-id="06768-124">Name of the elastic pool.</span></span>

## <span data-ttu-id="06768-125">Beispiele</span><span class="sxs-lookup"><span data-stu-id="06768-125">EXAMPLES</span></span>

### <span data-ttu-id="06768-126">Beispiel 1: Abrufen von Empfehlungen für einen Server</span><span class="sxs-lookup"><span data-stu-id="06768-126">Example 1: Get recommendations for a server</span></span>
```
PS C:\>Get-AzSqlElasticPoolRecommendation -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="06768-127">Dieser Befehl ruft die Empfehlungen für den elastischen Pool für den Server mit dem Namen SERVER01 ab.</span><span class="sxs-lookup"><span data-stu-id="06768-127">This command gets the elastic pool recommendations for the server named Server01.</span></span>

## <span data-ttu-id="06768-128">Parameter</span><span class="sxs-lookup"><span data-stu-id="06768-128">PARAMETERS</span></span>

### <span data-ttu-id="06768-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06768-129">-DefaultProfile</span></span>
<span data-ttu-id="06768-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="06768-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="06768-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06768-131">-ResourceGroupName</span></span>
<span data-ttu-id="06768-132">Gibt den Namen der Ressourcengruppe an, der der Server zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="06768-132">Specifies name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="06768-133">-Servername</span><span class="sxs-lookup"><span data-stu-id="06768-133">-ServerName</span></span>
<span data-ttu-id="06768-134">Gibt den Namen des Servers an, für den dieses Cmdlet Empfehlungen erhält.</span><span class="sxs-lookup"><span data-stu-id="06768-134">Specifies the name of the server for which this cmdlet gets recommendations.</span></span>

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

### <span data-ttu-id="06768-135">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="06768-135">-Confirm</span></span>
<span data-ttu-id="06768-136">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="06768-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06768-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06768-137">-WhatIf</span></span>
<span data-ttu-id="06768-138">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="06768-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="06768-139">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="06768-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06768-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06768-140">CommonParameters</span></span>
<span data-ttu-id="06768-141">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06768-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06768-142">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="06768-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06768-143">Eingaben</span><span class="sxs-lookup"><span data-stu-id="06768-143">INPUTS</span></span>

### <span data-ttu-id="06768-144">System. String</span><span class="sxs-lookup"><span data-stu-id="06768-144">System.String</span></span>

## <span data-ttu-id="06768-145">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="06768-145">OUTPUTS</span></span>

### <span data-ttu-id="06768-146">Microsoft. Azure. Management. SQL. LegacySdk. Models. UpgradeRecommendedElasticPoolProperties</span><span class="sxs-lookup"><span data-stu-id="06768-146">Microsoft.Azure.Management.Sql.LegacySdk.Models.UpgradeRecommendedElasticPoolProperties</span></span>

## <span data-ttu-id="06768-147">Notizen</span><span class="sxs-lookup"><span data-stu-id="06768-147">NOTES</span></span>

## <span data-ttu-id="06768-148">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="06768-148">RELATED LINKS</span></span>
