---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: 7d36860991d5b6b12fb23044cc607044fb87bfa6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947923"
---
# <span data-ttu-id="9fae4-101">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9fae4-101">New-AzDataMigrationService</span></span>

## <span data-ttu-id="9fae4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9fae4-102">SYNOPSIS</span></span>
<span data-ttu-id="9fae4-103">Erstellt eine neue Instanz des Azure Database Migration Service.</span><span class="sxs-lookup"><span data-stu-id="9fae4-103">Creates a new instance of the Azure Database Migration Service.</span></span>

## <span data-ttu-id="9fae4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9fae4-104">SYNTAX</span></span>

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9fae4-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9fae4-105">DESCRIPTION</span></span>
<span data-ttu-id="9fae4-106">Das New-AzDataMigrationService-Cmdlet erstellt eine neue Instanz des Azure-Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="9fae4-106">The New-AzDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="9fae4-107">Dieses Cmdlet trägt den Namen der vorhandenen Azure Resource Group, den eindeutigen Namen für die neue Instanz des zu erstellenden Azure-Datenbankmigrationsdiensts, die Region, in der die Instanz bereitgestellt wird, den Namen der DMS Worker-SKU und den Namen des virtuellen Azure-Subnetzes, in dem sich der Dienst befinden soll.</span><span class="sxs-lookup"><span data-stu-id="9fae4-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="9fae4-108">Es gibt keinen Parameter für den Abonnementnamen, da der Benutzer das Standardabonnement der Azure-Anmeldesitzung angeben oder Get-AzSubscription -SubscriptionName "MySubscription" ausführen | Select-AzSubscription, um ein anderes Abonnement auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="9fae4-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription to select another subscription.</span></span>

## <span data-ttu-id="9fae4-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9fae4-109">EXAMPLES</span></span>

### <span data-ttu-id="9fae4-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9fae4-110">Example 1</span></span>
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="9fae4-111">Das vorstehende Beispiel zeigt, wie Sie eine neue Instanz des Azure Database Migration Service namens TestService in der Region "Usa, Mitte" erstellen.</span><span class="sxs-lookup"><span data-stu-id="9fae4-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="9fae4-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="9fae4-112">PARAMETERS</span></span>

### <span data-ttu-id="9fae4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9fae4-113">-DefaultProfile</span></span>
<span data-ttu-id="9fae4-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9fae4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9fae4-115">-Location</span><span class="sxs-lookup"><span data-stu-id="9fae4-115">-Location</span></span>
<span data-ttu-id="9fae4-116">Der Speicherort der zu erstellende Azure-Datenbankmigrationsdienstinstanz, die einer Azure-Region entspricht.</span><span class="sxs-lookup"><span data-stu-id="9fae4-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fae4-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9fae4-117">-Name</span></span>
<span data-ttu-id="9fae4-118">Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="9fae4-118">Database Migration Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fae4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9fae4-119">-ResourceGroupName</span></span>
<span data-ttu-id="9fae4-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="9fae4-120">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fae4-121">-Sku</span><span class="sxs-lookup"><span data-stu-id="9fae4-121">-Sku</span></span>
<span data-ttu-id="9fae4-122">Die Sku für die Azure Database Migration Service-Instanz.</span><span class="sxs-lookup"><span data-stu-id="9fae4-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="9fae4-123">Mögliche Werte werden derzeit Basic_1vCore.Basic_2vCores.GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="9fae4-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fae4-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="9fae4-124">-VirtualSubnetId</span></span>
<span data-ttu-id="9fae4-125">Der Name des Subnetzes unter dem angegebenen virtuellen Netzwerk, das für die Azure Database Migration Service-Instanz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="9fae4-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fae4-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9fae4-126">-Confirm</span></span>
<span data-ttu-id="9fae4-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9fae4-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fae4-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9fae4-128">-WhatIf</span></span>
<span data-ttu-id="9fae4-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9fae4-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9fae4-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9fae4-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9fae4-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9fae4-131">CommonParameters</span></span>
<span data-ttu-id="9fae4-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9fae4-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9fae4-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9fae4-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9fae4-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9fae4-134">INPUTS</span></span>

### <span data-ttu-id="9fae4-135">Keine</span><span class="sxs-lookup"><span data-stu-id="9fae4-135">None</span></span>

## <span data-ttu-id="9fae4-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9fae4-136">OUTPUTS</span></span>

### <span data-ttu-id="9fae4-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="9fae4-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="9fae4-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="9fae4-138">NOTES</span></span>

## <span data-ttu-id="9fae4-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="9fae4-139">RELATED LINKS</span></span>
