---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/get-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Get-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 16873efe9ba51eb71821fe7149c5abb1f316c4eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662457"
---
# <span data-ttu-id="0345f-101">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="0345f-101">Get-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="0345f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0345f-102">SYNOPSIS</span></span>
<span data-ttu-id="0345f-103">Ruft die Details einer eingebetteten PowerBI-Kapazität ab.</span><span class="sxs-lookup"><span data-stu-id="0345f-103">Gets the details of a PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0345f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0345f-104">SYNTAX</span></span>

```
Get-AzureRmPowerBIEmbeddedCapacity [[-ResourceGroupName] <String>] 
    [<CommonParameters>]

Get-AzureRmPowerBIEmbeddedCapacity [-ResourceGroupName] <String> [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="0345f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0345f-105">DESCRIPTION</span></span>
<span data-ttu-id="0345f-106">Das Get-AzureRmPowerBIEmbeddedCapacity-Cmdlet ruft die Details einer eingebetteten PowerBI-Kapazität ab.</span><span class="sxs-lookup"><span data-stu-id="0345f-106">The Get-AzureRmPowerBIEmbeddedCapacity cmdlet gets the details of a PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="0345f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0345f-107">EXAMPLES</span></span>

### <span data-ttu-id="0345f-108">Beispiel 1: Abrufen von Ressourcengruppenkapazitäten</span><span class="sxs-lookup"><span data-stu-id="0345f-108">Example 1: Get resource group capacities</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/mycapacity
ResourceGroup          : testRG
Name                   : mycapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A4
Tier                   : PBIE_Azure
Tag                    : {}
```

<span data-ttu-id="0345f-109">Dieser Befehl ruft alle Azure PowerBI eingebettete Kapazität in der Ressourcengruppe mit dem Namen testRG</span><span class="sxs-lookup"><span data-stu-id="0345f-109">This command gets all Azure PowerBI Embedded Capacity in the resource group named testRG</span></span>

### <span data-ttu-id="0345f-110">Beispiel 2: Abrufen einer Kapazität</span><span class="sxs-lookup"><span data-stu-id="0345f-110">Example 2: Get a capacity</span></span>
```
PS C:\>Get-AzureRmPowerBIEmbeddedCapacity -ResourceGroupName "testRG" -Name "testcapacity"
Type                   : Microsoft.PowerBIDedicated/capacities
Id                     : /subscriptions/78e47976-.../resourceGroups/testRG/providers/Microsoft.PowerBIDedicated/capacities/testcapacity
ResourceGroup          : testRG
Name                   : testcapacity
Location               : West Central US
State                  : Succeeded
Administrator          : {admin@microsoft.com}
Sku                    : A1
Tier                   : PBIE_Azure
Tag                    : {}

```

<span data-ttu-id="0345f-111">Dieser Befehl ruft die eingebettete Azure PowerBI-Kapazität mit dem Namen testcapacity in der Ressourcengruppe mit dem Namen testRG.</span><span class="sxs-lookup"><span data-stu-id="0345f-111">This command gets the Azure PowerBI Embedded Capacity named testcapacity in the resource group named testRG.</span></span>

## <span data-ttu-id="0345f-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0345f-112">PARAMETERS</span></span>

### <span data-ttu-id="0345f-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0345f-113">-ResourceGroupName</span></span>
<span data-ttu-id="0345f-114">Name der Azure-Ressourcengruppe, zu der die Kapazität gehört</span><span class="sxs-lookup"><span data-stu-id="0345f-114">Name of the Azure resource group to which the capacity belongs</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroup, ByCapacity
Aliases: 

Required: False
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="0345f-115">-Name</span><span class="sxs-lookup"><span data-stu-id="0345f-115">-Name</span></span>
<span data-ttu-id="0345f-116">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="0345f-116">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Parameter Sets: ByCapacity
Aliases: 

Required: True
Position: 1
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="0345f-117">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="0345f-117">-ResourceId</span></span>
<span data-ttu-id="0345f-118">Azure-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="0345f-118">Azure resource ID</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0345f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0345f-119">CommonParameters</span></span>
<span data-ttu-id="0345f-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0345f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0345f-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0345f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0345f-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0345f-122">INPUTS</span></span>

### <span data-ttu-id="0345f-123">Keine</span><span class="sxs-lookup"><span data-stu-id="0345f-123">None</span></span>
<span data-ttu-id="0345f-124">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="0345f-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0345f-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0345f-125">OUTPUTS</span></span>

### <span data-ttu-id="0345f-126">Liste<Microsoft. Azure. Commands. PowerBI. Models. PSPowerBIEmbeddedCapacity></span><span class="sxs-lookup"><span data-stu-id="0345f-126">List<Microsoft.Azure.Commands.PowerBI.Models.PSPowerBIEmbeddedCapacity></span></span>

## <span data-ttu-id="0345f-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="0345f-127">NOTES</span></span>

## <span data-ttu-id="0345f-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0345f-128">RELATED LINKS</span></span>

[<span data-ttu-id="0345f-129">Neu – AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="0345f-129">New-AzureRmPowerBIEmbeddedCapacity </span></span>](./New-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="0345f-130">Remove-AzureRmPowerBIEmbeddedCapacity </span><span class="sxs-lookup"><span data-stu-id="0345f-130">Remove-AzureRmPowerBIEmbeddedCapacity </span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
