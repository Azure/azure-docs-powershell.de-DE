---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationService.md
ms.openlocfilehash: 46455cbf411228f008bdc15c27f78715ccea0e89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664663"
---
# <span data-ttu-id="88142-101">New-AzureRmDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="88142-101">New-AzureRmDataMigrationService</span></span>

## <span data-ttu-id="88142-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="88142-102">SYNOPSIS</span></span>
<span data-ttu-id="88142-103">Erstellt eine neue Instanz des Azure-Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="88142-103">Creates a new instance of the Azure Database Migration Service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88142-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="88142-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationService -ResourceGroupName <String> -ServiceName <String> -Location <String>
 -Sku <String> -VirtualSubnetId <String> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="88142-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88142-105">DESCRIPTION</span></span>
<span data-ttu-id="88142-106">Das New-AzureRmDataMigrationService-Cmdlet erstellt eine neue Instanz des Azure-Daten Bank Migrations Diensts.</span><span class="sxs-lookup"><span data-stu-id="88142-106">The New-AzureRmDataMigrationService cmdlet creates a new instance of the Azure Database Migration Service.</span></span> <span data-ttu-id="88142-107">Dieses Cmdlet übernimmt den Namen der vorhandenen Azure-Ressourcengruppe, den eindeutigen Namen für die neue Instanz des zu erstellenden Azure-Daten Bank Migrations Diensts, den Bereich, in dem die Instanz bereitgestellt wird, den Namen der DMS-Worker-SKU sowie den Namen des virtuellen Azure-Subnets, in dem sich der Dienst befinden soll.</span><span class="sxs-lookup"><span data-stu-id="88142-107">This cmdlet takes in name of existing Azure Resource Group, the unique name for the new instance of the Azure Database Migration Service to be created, the region in which the instance is provisioned, the name of the DMS Worker SKU, and the name of the Azure Virtual Subnet on which the service is to reside.</span></span> <span data-ttu-id="88142-108">Es gibt keinen Parameter für den Abonnement Namen, da erwartet wird, dass der Benutzer das Standardabonnement der Azure-Anmeldesitzung angibt oder Get-AzureRmSubscription-Abonnementname "mysubscription" ausführt | Select-AzureRmSubscription, um ein anderes Abonnement auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="88142-108">There is no parameter for subscription name, because it is expected for the user to specify the default subscription of the Azure login session or execute Get-AzureRmSubscription –SubscriptionName "MySubscription" | Select-AzureRmSubscription to select another subscription.</span></span>

## <span data-ttu-id="88142-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="88142-109">EXAMPLES</span></span>

### <span data-ttu-id="88142-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="88142-110">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationService -ResourceGroupName myResourceGroup -ServiceName TestService -Location "Central US" -Sku Basic_2vCores -VirtualSubnetId $virtualSubNetId
```

<span data-ttu-id="88142-111">Das obige Beispiel zeigt, wie Sie eine neue Instanz des Azure Database Migration Service mit dem Namen Test Service in der Region Central US erstellen.</span><span class="sxs-lookup"><span data-stu-id="88142-111">The above example shows how to create a new instance of the Azure Database Migration Service named TestService in Central US region.</span></span>


## <span data-ttu-id="88142-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="88142-112">PARAMETERS</span></span>

### <span data-ttu-id="88142-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88142-113">-DefaultProfile</span></span>
<span data-ttu-id="88142-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="88142-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88142-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="88142-115">-Location</span></span>
<span data-ttu-id="88142-116">Der Speicherort der zu erstellenden Azure Database Migration Service-Instanz, die einem Azure-Bereich entspricht.</span><span class="sxs-lookup"><span data-stu-id="88142-116">The location of the Azure Database Migration Service instance to be created, which corresponds to an Azure region.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88142-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88142-117">-ResourceGroupName</span></span>
<span data-ttu-id="88142-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="88142-118">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88142-119">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="88142-119">-ServiceName</span></span>
<span data-ttu-id="88142-120">Der Name der Azure-Datenbank-Migrationsdienst Instanz.</span><span class="sxs-lookup"><span data-stu-id="88142-120">The name of the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88142-121">-SKU</span><span class="sxs-lookup"><span data-stu-id="88142-121">-Sku</span></span>
<span data-ttu-id="88142-122">Die SKU für die Azure Database Migration Service-Instanz.</span><span class="sxs-lookup"><span data-stu-id="88142-122">The sku for the Azure Database Migration Service instance.</span></span> <span data-ttu-id="88142-123">Mögliche Werte sind derzeit Basic_1vCore, Basic_2vCores, GeneralPurpose_4vCores</span><span class="sxs-lookup"><span data-stu-id="88142-123">Possible values currently are Basic_1vCore,Basic_2vCores,GeneralPurpose_4vCores</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88142-124">-VirtualSubnetId</span><span class="sxs-lookup"><span data-stu-id="88142-124">-VirtualSubnetId</span></span>
<span data-ttu-id="88142-125">Der Name des Subnetzes unter dem angegebenen virtuellen Netzwerk, das für die Azure-Datenbank-Migrationsdienst Instanz verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="88142-125">The name of the subnet under the specified virtual network to use for the Azure Database Migration Service instance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```




## <span data-ttu-id="88142-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="88142-126">OUTPUTS</span></span>

### <span data-ttu-id="88142-127">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span><span class="sxs-lookup"><span data-stu-id="88142-127">Microsoft.Azure.Commands.DataMigration.Models.PSDataMigrationService</span></span>


## <span data-ttu-id="88142-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="88142-128">NOTES</span></span>

## <span data-ttu-id="88142-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="88142-129">RELATED LINKS</span></span>

