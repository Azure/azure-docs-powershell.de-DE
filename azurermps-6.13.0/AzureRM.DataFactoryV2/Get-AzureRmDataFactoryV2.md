---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2.md
ms.openlocfilehash: be781e1679a5338cbc80312bbcfed01aa087a1b0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502969"
---
# <span data-ttu-id="725fb-101">Get-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="725fb-101">Get-AzureRmDataFactoryV2</span></span>

## <span data-ttu-id="725fb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="725fb-102">SYNOPSIS</span></span>
<span data-ttu-id="725fb-103">Ruft Informationen zu Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="725fb-103">Gets information about Data Factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="725fb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="725fb-104">SYNTAX</span></span>

### <span data-ttu-id="725fb-105">BySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="725fb-105">BySubscriptionId (Default)</span></span>
```
Get-AzureRmDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="725fb-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="725fb-106">ByFactoryName</span></span>
```
Get-AzureRmDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="725fb-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="725fb-107">DESCRIPTION</span></span>
<span data-ttu-id="725fb-108">Das Get-AzureRmDataFactoryV2-Cmdlet ruft Informationen zu Daten Factorys in einer Azure-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="725fb-108">The Get-AzureRmDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="725fb-109">Wenn Sie den Namen einer Data Factory angeben, ruft dieses Cmdlet Informationen zu dieser Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="725fb-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="725fb-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Daten Factorys in einer Azure-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="725fb-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="725fb-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="725fb-111">EXAMPLES</span></span>

### <span data-ttu-id="725fb-112">Beispiel 1: Abrufen aller Daten Factorys</span><span class="sxs-lookup"><span data-stu-id="725fb-112">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded

    DataFactoryName   : WikiADF2
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf2
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          :
    ProvisioningState : Succeeded
```

<span data-ttu-id="725fb-113">Zeigt Informationen zu allen Daten Fabriken im Azure-Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="725fb-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="725fb-114">Beispiel 2: Abrufen einer bestimmten Data Factory</span><span class="sxs-lookup"><span data-stu-id="725fb-114">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzureRmDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
```

<span data-ttu-id="725fb-115">Dieser Befehl zeigt Informationen zur Data Factory mit dem Namen WikiADF im Abonnement für die Ressourcengruppe "ADF" an und speichert Sie dann in der $datafactory-Variablen.</span><span class="sxs-lookup"><span data-stu-id="725fb-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="725fb-116">Geben Sie den Parameter DataFactory in nachfolgenden Cmdlets an, um die in $DataFactory gespeicherte Data Factory zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="725fb-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="725fb-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="725fb-117">PARAMETERS</span></span>

### <span data-ttu-id="725fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="725fb-118">-DefaultProfile</span></span>
<span data-ttu-id="725fb-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="725fb-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="725fb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="725fb-120">-Name</span></span>
<span data-ttu-id="725fb-121">Gibt den Namen der Data Factory an, über die Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="725fb-121">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: DataFactoryName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="725fb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="725fb-122">-ResourceGroupName</span></span>
<span data-ttu-id="725fb-123">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="725fb-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="725fb-124">Dieses Cmdlet ruft Informationen zu Daten Factorys ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="725fb-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="725fb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="725fb-125">CommonParameters</span></span>
<span data-ttu-id="725fb-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="725fb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="725fb-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="725fb-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="725fb-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="725fb-128">INPUTS</span></span>

### <span data-ttu-id="725fb-129">System. String</span><span class="sxs-lookup"><span data-stu-id="725fb-129">System.String</span></span>

## <span data-ttu-id="725fb-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="725fb-130">OUTPUTS</span></span>

### <span data-ttu-id="725fb-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="725fb-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="725fb-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="725fb-132">NOTES</span></span>
<span data-ttu-id="725fb-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="725fb-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="725fb-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="725fb-134">RELATED LINKS</span></span>

[<span data-ttu-id="725fb-135">Satz-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="725fb-135">Set-AzureRmDataFactoryV2</span></span>]()

[<span data-ttu-id="725fb-136">Remove-AzureRmDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="725fb-136">Remove-AzureRmDataFactoryV2</span></span>]()

