---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 8f6e161ad9ae2078da15dda659f1aea13929eec9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476697"
---
# <span data-ttu-id="de520-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="de520-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="de520-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="de520-102">SYNOPSIS</span></span>
<span data-ttu-id="de520-103">Testet das vorhanden sein einer Instanz der eingebetteten Kapazität von PowerBI.</span><span class="sxs-lookup"><span data-stu-id="de520-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de520-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="de520-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity 
    [-Name] <String> 
    [<CommonParameters>]
```

## <span data-ttu-id="de520-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de520-105">DESCRIPTION</span></span>
<span data-ttu-id="de520-106">Das Test-AzureRmPowerBIEmbeddedCapacity-Cmdlet testet das vorhanden sein einer Instanz der eingebetteten Kapazität von PowerBI</span><span class="sxs-lookup"><span data-stu-id="de520-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="de520-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de520-107">EXAMPLES</span></span>

### <span data-ttu-id="de520-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="de520-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="de520-109">Mit diesem Befehl wird getestet, ob eine Kapazität mit dem Namen testcapacity vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="de520-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="de520-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="de520-110">PARAMETERS</span></span>

### <span data-ttu-id="de520-111">-Name</span><span class="sxs-lookup"><span data-stu-id="de520-111">-Name</span></span>
<span data-ttu-id="de520-112">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="de520-112">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: String
Aliases: 

Required: True
Position: 0
Default value: None
Accept wildcard characters: False
```

### <span data-ttu-id="de520-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de520-113">CommonParameters</span></span>
<span data-ttu-id="de520-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de520-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de520-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de520-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de520-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="de520-116">INPUTS</span></span>

### <span data-ttu-id="de520-117">Keine</span><span class="sxs-lookup"><span data-stu-id="de520-117">None</span></span>
<span data-ttu-id="de520-118">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="de520-118">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="de520-119">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="de520-119">OUTPUTS</span></span>

### <span data-ttu-id="de520-120">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="de520-120">System.Boolean</span></span>

## <span data-ttu-id="de520-121">Notizen</span><span class="sxs-lookup"><span data-stu-id="de520-121">NOTES</span></span>

## <span data-ttu-id="de520-122">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="de520-122">RELATED LINKS</span></span>

[<span data-ttu-id="de520-123">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="de520-123">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="de520-124">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="de520-124">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
