---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationService
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationService.md
ms.openlocfilehash: c8e81cf727894adfa7378bbed996a1a476521148
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98304723"
---
# <span data-ttu-id="d4211-101">New-AzDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="d4211-101">New-AzDataMigrationService</span></span>

## <span data-ttu-id="d4211-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4211-102">SYNOPSIS</span></span>
<span data-ttu-id="d4211-103">Erstellt eine neue Instanz des Azure-Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="d4211-103">Creates a new instance of the Azure Database Migration Service.</span></span>

## <span data-ttu-id="d4211-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d4211-104">SYNTAX</span></span>

```
New-AzDataMigrationService -ResourceGroupName <String> -Name <String> -Location <String> -Sku <String>
 -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d4211-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d4211-105">DESCRIPTION</span></span>
<span data-ttu-id="d4211-106">Das New-AzDataMigrationService erstellt eine neue Instanz des Azure-Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="d4211-106">The New-AzDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="d4211-107">Dieses Cmdlet trägt den Namen der vorhandenen Azure-Ressourcengruppe, den eindeutigen Namen für die neue Instanz des zu erstellenden Azure-Datenbankmigrationsdiensts, die Region, in der die Instanz bereitgestellt wird, den Namen der DMS-Worker-SKU und den Namen des virtuellen Azure-Subnetzes, in dem sich der Dienst befinden soll.</span><span class="sxs-lookup"><span data-stu-id="d4211-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="d4211-108">Es gibt keinen Parameter für den Abonnementnamen, da erwartet wird, dass der Benutzer das Standardabonnement der Azure-Anmeldesitzung anknrichte oder Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription, um ein anderes Abonnement auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d4211-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzSubscription -SubscriptionName "MySubscription" | Select-AzSubscription to select another subscription.</span></span>

## <span data-ttu-id="d4211-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d4211-109">EXAMPLES</span></span>

### <span data-ttu-id="d4211-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d4211-110">Example 1</span></span>
```
PS C:\> New-AzDataMigrationService -ResourceGroupName myResourceGroup -Name TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="d4211-111">Das beispiel oben zeigt, wie Sie eine neue Instanz des Azure Database Migration Service namens TestService in der Region "USA, Mitte" erstellen.</span><span class="sxs-lookup"><span data-stu-id="d4211-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>

## <span data-ttu-id="d4211-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d4211-112">PARAMETERS</span></span>

### <span data-ttu-id="d4211-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4211-113">-DefaultProfile</span></span>
<span data-ttu-id="d4211-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d4211-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d4211-115">-Location</span><span class="sxs-lookup"><span data-stu-id="d4211-115">-Location</span></span>
<span data-ttu-id="d4211-116">Der Speicherort der zu erstellende Azure-Datenbankmigrationsdienstinstanz, der einer Azure-Region entspricht.</span><span class="sxs-lookup"><span data-stu-id="d4211-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

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

### <span data-ttu-id="d4211-117">-Name</span><span class="sxs-lookup"><span data-stu-id="d4211-117">-Name</span></span>
<span data-ttu-id="d4211-118">Name des Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="d4211-118">Database Migration Service Name.</span></span>

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

### <span data-ttu-id="d4211-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4211-119">-ResourceGroupName</span></span>
<span data-ttu-id="d4211-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d4211-120">The name of the resource group.</span></span>

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

### <span data-ttu-id="d4211-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="d4211-121">-Sku</span></span>
<span data-ttu-id="d4211-122">Die SKU für die Instanz des Azure-Datenbankmigrationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="d4211-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="d4211-123">Mögliche Werte sind derzeit Basic_1vCore.Basic_2vCores.GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="d4211-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

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

### <span data-ttu-id="d4211-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="d4211-124">-VirtualSubnetId</span></span>
<span data-ttu-id="d4211-125">Der Name des Subnetzes unter dem angegebenen virtuellen Netzwerk, das für die Instanz des Azure Database Migration Service verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d4211-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

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

### <span data-ttu-id="d4211-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d4211-126">-Confirm</span></span>
<span data-ttu-id="d4211-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d4211-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d4211-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d4211-128">-WhatIf</span></span>
<span data-ttu-id="d4211-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d4211-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d4211-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d4211-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d4211-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4211-131">CommonParameters</span></span>
<span data-ttu-id="d4211-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4211-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4211-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4211-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4211-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d4211-134">INPUTS</span></span>

### <span data-ttu-id="d4211-135">Keine</span><span class="sxs-lookup"><span data-stu-id="d4211-135">None</span></span>

## <span data-ttu-id="d4211-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d4211-136">OUTPUTS</span></span>

### <span data-ttu-id="d4211-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="d4211-137">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>

## <span data-ttu-id="d4211-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d4211-138">NOTES</span></span>

## <span data-ttu-id="d4211-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d4211-139">RELATED LINKS</span></span>
