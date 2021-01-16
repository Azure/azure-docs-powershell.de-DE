---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactories.dll-Help.xml
Module Name: Az.DataFactory
ms.assetid: ECE1F469-E3C3-4294-A288-8BAE851E8599
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactory.md
ms.openlocfilehash: 11aaaa3bb17a35583655f231123b7f6e9dea9ab4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307528"
---
# <span data-ttu-id="16618-101">Get-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="16618-101">Get-AzDataFactory</span></span>

## <span data-ttu-id="16618-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16618-102">SYNOPSIS</span></span>
<span data-ttu-id="16618-103">Ruft Informationen zu Daten factorys ab.</span><span class="sxs-lookup"><span data-stu-id="16618-103">Gets information about Data Factories.</span></span>

## <span data-ttu-id="16618-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="16618-104">SYNTAX</span></span>

```
Get-AzDataFactory [[-Name] <String>] [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="16618-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="16618-105">DESCRIPTION</span></span>
<span data-ttu-id="16618-106">Das **Cmdlet "Get-AzDataFactory"** ruft Informationen zu Datenfactorys in einer Azure-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="16618-106">The **Get-AzDataFactory** cmdlet gets information about data factories in an Azure resource group.</span></span>
<span data-ttu-id="16618-107">Wenn Sie den Namen einer Daten factory angeben, ruft dieses Cmdlet Informationen zu dieser Daten factory ab.</span><span class="sxs-lookup"><span data-stu-id="16618-107">If you specify the name of a data factory, this cmdlet gets information about that data factory.</span></span>
<span data-ttu-id="16618-108">Wenn Sie keinen Namen angeben, ruft dieses Cmdlet Informationen zu allen Daten factorys in einer Azure-Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="16618-108">If you do not specify a name, this cmdlet gets information about all of the data factories in an Azure resource group.</span></span>

## <span data-ttu-id="16618-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="16618-109">EXAMPLES</span></span>

### <span data-ttu-id="16618-110">Beispiel 1: Alle Daten factorys erhalten</span><span class="sxs-lookup"><span data-stu-id="16618-110">Example 1: Get all data factories</span></span>
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

<span data-ttu-id="16618-111">Dieser Befehl zeigt Informationen zu allen Daten factorys im Azure-Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="16618-111">This command displays information about all data factories in the Azure subscription.</span></span>

### <span data-ttu-id="16618-112">Beispiel 2: Erhalten einer bestimmten Daten factory</span><span class="sxs-lookup"><span data-stu-id="16618-112">Example 2: Get a specific data factory</span></span>
```
PS C:\>$DataFactory = Get-AzDataFactory -ResourceGroupName "ADF" -Name "WikiADF"
DataFactoryName   : WikiADF
ResourceGroupName : ADF
Location          : westus
Tags              : {}
Properties        : Microsoft.WindowsAzure.Commands.Utilities.PSDataFactoryConfiguration
```

<span data-ttu-id="16618-113">Dieser Befehl zeigt Informationen über die Daten factory namens WikiADF im Abonnement für die Ressourcengruppe namens ADF an und speichert sie dann in der $DataFactory Variable.</span><span class="sxs-lookup"><span data-stu-id="16618-113">This command displays information about the data factory named WikiADF in the subscription for the resource group named ADF, and then stores it in the $DataFactory variable.</span></span>
<span data-ttu-id="16618-114">Geben Sie *den Parameter "DataFactory"* in nachfolgenden Cmdlets an, um die in der Datei gespeicherte $DataFactory.</span><span class="sxs-lookup"><span data-stu-id="16618-114">Specify the *DataFactory* parameter in subsequent cmdlets to use the data factory stored in $DataFactory.</span></span>

## <span data-ttu-id="16618-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="16618-115">PARAMETERS</span></span>

### <span data-ttu-id="16618-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16618-116">-DefaultProfile</span></span>
<span data-ttu-id="16618-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="16618-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16618-118">-Name</span><span class="sxs-lookup"><span data-stu-id="16618-118">-Name</span></span>
<span data-ttu-id="16618-119">Gibt den Namen der Daten factory an, über die Informationen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="16618-119">Specifies the name of the data factory about which to get information.</span></span>

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

### <span data-ttu-id="16618-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16618-120">-ResourceGroupName</span></span>
<span data-ttu-id="16618-121">Gibt den Namen einer Azure-Ressourcengruppe an.</span><span class="sxs-lookup"><span data-stu-id="16618-121">Specifies the name of an Azure resource group.</span></span>
<span data-ttu-id="16618-122">Dieses Cmdlet ruft Informationen zu Daten factorys ab, die zu der Gruppe gehören, die dieser Parameter angibt.</span><span class="sxs-lookup"><span data-stu-id="16618-122">This cmdlet gets information about data factories that belong to the group that this parameter specifies.</span></span>

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

### <span data-ttu-id="16618-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16618-123">CommonParameters</span></span>
<span data-ttu-id="16618-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16618-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16618-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16618-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16618-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="16618-126">INPUTS</span></span>

### <span data-ttu-id="16618-127">System.String</span><span class="sxs-lookup"><span data-stu-id="16618-127">System.String</span></span>

## <span data-ttu-id="16618-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="16618-128">OUTPUTS</span></span>

### <span data-ttu-id="16618-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="16618-129">Microsoft.Azure.Commands.DataFactories.Models.PSDataFactory</span></span>

## <span data-ttu-id="16618-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="16618-130">NOTES</span></span>
* <span data-ttu-id="16618-131">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="16618-131">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="16618-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="16618-132">RELATED LINKS</span></span>

[<span data-ttu-id="16618-133">New-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="16618-133">New-AzDataFactory</span></span>](./New-AzDataFactory.md)

[<span data-ttu-id="16618-134">Remove-AzDataFactory</span><span class="sxs-lookup"><span data-stu-id="16618-134">Remove-AzDataFactory</span></span>](./Remove-AzDataFactory.md)


