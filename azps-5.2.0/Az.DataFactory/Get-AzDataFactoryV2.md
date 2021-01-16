---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2.md
ms.openlocfilehash: fac2e899984f9d626f6c7342043166649327a0f4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307448"
---
# <span data-ttu-id="a1788-101">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a1788-101">Get-AzDataFactoryV2</span></span>

## <span data-ttu-id="a1788-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1788-102">SYNOPSIS</span></span>
<span data-ttu-id="a1788-103">Ruft Informationen zu Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="a1788-103">Gets information about Data Factory.</span></span>

## <span data-ttu-id="a1788-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a1788-104">SYNTAX</span></span>

### <span data-ttu-id="a1788-105">BySubscriptionId (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1788-105">BySubscriptionId (Default)</span></span>
```
Get-AzDataFactoryV2 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a1788-106">ByFactoryName</span><span class="sxs-lookup"><span data-stu-id="a1788-106">ByFactoryName</span></span>
```
Get-AzDataFactoryV2 [-ResourceGroupName] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a1788-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a1788-107">DESCRIPTION</span></span>
<span data-ttu-id="a1788-108">Das Get-AzDataFactoryV2 Cmdlet ruft Informationen zu Daten factorys in einer Azure-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="a1788-108">The Get-AzDataFactoryV2 cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="a1788-109">Wenn Sie den Namen einer Daten factory angeben, ruft dieses Cmdlet Informationen zu dieser Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="a1788-109">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="a1788-110">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Daten factorys in einer Azure-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="a1788-110">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="a1788-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a1788-111">EXAMPLES</span></span>

### <span data-ttu-id="a1788-112">Beispiel 1: Alle Daten factorys erhalten</span><span class="sxs-lookup"><span data-stu-id="a1788-112">Example 1: Get all data factories</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF"

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

<span data-ttu-id="a1788-113">Zeigt Informationen zu allen Daten factorys im Abonnement von Azure an.</span><span class="sxs-lookup"><span data-stu-id="a1788-113">Displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="a1788-114">Beispiel 2: Erhalten einer bestimmten Daten factory</span><span class="sxs-lookup"><span data-stu-id="a1788-114">Example 2: Get a specific data factory</span></span>
```
PS C:\> $DataFactory = Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataF
                        actory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
```

<span data-ttu-id="a1788-115">Dieser Befehl zeigt Informationen über die Daten factory namens WikiADF im Abonnement für die Ressourcengruppe namens ADF an und speichert sie dann in der $DataFactory Variable.</span><span class="sxs-lookup"><span data-stu-id="a1788-115">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="a1788-116">Geben Sie den Parameter "DataFactory" in nachfolgenden Cmdlets an, um die in der Datei gespeicherte $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="a1788-116">Specify the DataFactory parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="a1788-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1788-117">PARAMETERS</span></span>

### <span data-ttu-id="a1788-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1788-118">-DefaultProfile</span></span>
<span data-ttu-id="a1788-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a1788-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1788-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a1788-120">-Name</span></span>
<span data-ttu-id="a1788-121">Gibt den Namen der Daten factory an, über die Informationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a1788-121">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="a1788-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1788-122">-ResourceGroupName</span></span>
<span data-ttu-id="a1788-123">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="a1788-123">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="a1788-124">Dieses Cmdlet ruft Informationen zu Daten factorys ab, die zu der von diesem Parameter angegebenen Gruppe gehören.</span><span class="sxs-lookup"><span data-stu-id="a1788-124">This cmdlet gets information about data factories that belong to the group this parameter specifies.</span></span>

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

### <span data-ttu-id="a1788-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1788-125">CommonParameters</span></span>
<span data-ttu-id="a1788-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1788-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1788-127">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1788-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1788-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a1788-128">INPUTS</span></span>

### <span data-ttu-id="a1788-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a1788-129">System.String</span></span>

## <span data-ttu-id="a1788-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a1788-130">OUTPUTS</span></span>

### <span data-ttu-id="a1788-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="a1788-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="a1788-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="a1788-132">NOTES</span></span>
<span data-ttu-id="a1788-133">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="a1788-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="a1788-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="a1788-134">RELATED LINKS</span></span>

[<span data-ttu-id="a1788-135">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a1788-135">Set-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="a1788-136">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="a1788-136">Remove-AzDataFactoryV2</span></span>]()

