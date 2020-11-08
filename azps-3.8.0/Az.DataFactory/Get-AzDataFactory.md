---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: 11aaaa3bb17a35583655f231123b7f6e9dea9ab4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004308"
---
# <span data-ttu-id="986de-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="986de-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="986de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="986de-102">SYNOPSIS</span></span>
<span data-ttu-id="986de-103">Ruft Informationen zu Daten Factorys ab.</span><span class="sxs-lookup"><span data-stu-id="986de-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="986de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="986de-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="986de-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="986de-105">DESCRIPTION</span></span>
<span data-ttu-id="986de-106">Das Cmdlet " **Get-AzDataFactory** " Ruft Informationen zu Daten Factorys in einer Azure-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="986de-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="986de-107">Wenn Sie den Namen einer Data Factory angeben, ruft dieses Cmdlet Informationen zu dieser Data Factory ab.</span><span class="sxs-lookup"><span data-stu-id="986de-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="986de-108">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Daten Factorys in einer Azure-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="986de-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="986de-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="986de-109">EXAMPLES</span></span>

### <span data-ttu-id="986de-110">Beispiel 1: Abrufen aller Daten Factorys</span><span class="sxs-lookup"><span data-stu-id="986de-110">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="986de-111">Dieser Befehl zeigt Informationen zu allen Daten Fabriken im Azure-Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="986de-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="986de-112">Beispiel 2: Abrufen einer bestimmten Data Factory</span><span class="sxs-lookup"><span data-stu-id="986de-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="986de-113">Dieser Befehl zeigt Informationen zur Data Factory mit dem Namen WikiADF im Abonnement für die Ressourcengruppe "ADF" an und speichert Sie dann in der $datafactory-Variablen.</span><span class="sxs-lookup"><span data-stu-id="986de-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="986de-114">Geben Sie den Parameter *DataFactory* in nachfolgenden Cmdlets an, um die in $DataFactory gespeicherte Data Factory zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="986de-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="986de-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="986de-115">PARAMETERS</span></span>

### <span data-ttu-id="986de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="986de-116">-DefaultProfile</span></span>
<span data-ttu-id="986de-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="986de-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="986de-118">-Name</span><span class="sxs-lookup"><span data-stu-id="986de-118">-Name</span></span>
<span data-ttu-id="986de-119">Gibt den Namen der Data Factory an, über die Informationen abgerufen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="986de-119">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="986de-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="986de-120">-ResourceGroupName</span></span>
<span data-ttu-id="986de-121">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="986de-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="986de-122">Dieses Cmdlet ruft Informationen zu Daten Factorys ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="986de-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="986de-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="986de-123">CommonParameters</span></span>
<span data-ttu-id="986de-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="986de-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="986de-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="986de-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="986de-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="986de-126">INPUTS</span></span>

### <span data-ttu-id="986de-127">System. String</span><span class="sxs-lookup"><span data-stu-id="986de-127">System.String</span></span>

## <span data-ttu-id="986de-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="986de-128">OUTPUTS</span></span>

### <span data-ttu-id="986de-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="986de-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="986de-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="986de-130">NOTES</span></span>
* <span data-ttu-id="986de-131">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="986de-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="986de-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="986de-132">RELATED LINKS</span></span>

[<span data-ttu-id="986de-133">Neu – AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="986de-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="986de-134">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="986de-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


