---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: ff47851c998cb88bec7106e8aba6d47d16069321
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101931195"
---
# <span data-ttu-id="ac6fa-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="ac6fa-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="ac6fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac6fa-102">SYNOPSIS</span></span>
<span data-ttu-id="ac6fa-103">Ruft Informationen zu Data Factorys ab.</span><span class="sxs-lookup"><span data-stu-id="ac6fa-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="ac6fa-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac6fa-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac6fa-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac6fa-105">DESCRIPTION</span></span>
<span data-ttu-id="ac6fa-106">Das **Get-AzDataFactory-Cmdlet** ruft Informationen zu Datenfabriken in einer Azure-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="ac6fa-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="ac6fa-107">Wenn Sie den Namen einer Daten factory angeben, ruft dieses Cmdlet Informationen zu dieser Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="ac6fa-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="ac6fa-108">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Datenfabriken in einer Azure-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="ac6fa-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="ac6fa-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ac6fa-109">EXAMPLES</span></span>

### <span data-ttu-id="ac6fa-110">Beispiel 1: Alle Datenfabriken erhalten</span><span class="sxs-lookup"><span data-stu-id="ac6fa-110">Example 1: Get all data factories</span></span>
```
PS C:\>Get-AzDataFactory -ResourceGroupName "ADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : WestUS
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration

DataFactoryName   : WikiADF2
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="ac6fa-111">Mit diesem Befehl werden Informationen zu allen Datenfabriken im Azure-Abonnement angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ac6fa-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="ac6fa-112">Beispiel 2: Erhalten einer bestimmten Daten factory</span><span class="sxs-lookup"><span data-stu-id="ac6fa-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="ac6fa-113">Dieser Befehl zeigt Informationen zur Daten factory namens WikiADF im Abonnement für die Ressourcengruppe mit dem Namen ADF an und speichert sie dann in der $DataFactory Variablen.</span><span class="sxs-lookup"><span data-stu-id="ac6fa-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="ac6fa-114">Geben Sie *den Parameter DataFactory* in nachfolgenden Cmdlets an, um die in der Datei gespeicherte $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="ac6fa-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="ac6fa-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ac6fa-115">PARAMETERS</span></span>

### <span data-ttu-id="ac6fa-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac6fa-116">-DefaultProfile</span></span>
<span data-ttu-id="ac6fa-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ac6fa-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ac6fa-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ac6fa-118">-Name</span></span>
<span data-ttu-id="ac6fa-119">Gibt den Namen der Daten factory an, über die Informationen zu erhalten sind.</span><span class="sxs-lookup"><span data-stu-id="ac6fa-119">Specifies the name of the data factory about which to get information.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac6fa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac6fa-120">-ResourceGroupName</span></span>
<span data-ttu-id="ac6fa-121">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="ac6fa-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="ac6fa-122">Dieses Cmdlet ruft Informationen zu Datenfabriken ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="ac6fa-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="ac6fa-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac6fa-123">CommonParameters</span></span>
<span data-ttu-id="ac6fa-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac6fa-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac6fa-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac6fa-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac6fa-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ac6fa-126">INPUTS</span></span>

### <span data-ttu-id="ac6fa-127">System.String</span><span class="sxs-lookup"><span data-stu-id="ac6fa-127">System.String</span></span>

## <span data-ttu-id="ac6fa-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ac6fa-128">OUTPUTS</span></span>

### <span data-ttu-id="ac6fa-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="ac6fa-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="ac6fa-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ac6fa-130">NOTES</span></span>
* <span data-ttu-id="ac6fa-131">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="ac6fa-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="ac6fa-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ac6fa-132">RELATED LINKS</span></span>

[<span data-ttu-id="ac6fa-133">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="ac6fa-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="ac6fa-134">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="ac6fa-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


