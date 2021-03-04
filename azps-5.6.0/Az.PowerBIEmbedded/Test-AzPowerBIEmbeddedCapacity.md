---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 0b7d1f72b25da91e85a578a88eded7a511d6d1fd
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101941496"
---
# <span data-ttu-id="98f12-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="98f12-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="98f12-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98f12-102">SYNOPSIS</span></span>
<span data-ttu-id="98f12-103">Testet das Vorhandensein einer Instanz der eingebetteten PowerBI-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="98f12-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="98f12-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="98f12-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98f12-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98f12-105">DESCRIPTION</span></span>
<span data-ttu-id="98f12-106">Das Test-AzPowerBIEmbeddedCapacity-Cmdlet testet das Vorhandensein einer Instanz der eingebetteten PowerBI-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="98f12-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="98f12-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="98f12-107">EXAMPLES</span></span>

### <span data-ttu-id="98f12-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="98f12-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="98f12-109">Dieser Befehl testet, ob eine Kapazität namens "Testkapazität" vor ist.</span><span class="sxs-lookup"><span data-stu-id="98f12-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="98f12-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="98f12-110">PARAMETERS</span></span>

### <span data-ttu-id="98f12-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98f12-111">-DefaultProfile</span></span>
<span data-ttu-id="98f12-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="98f12-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98f12-113">-Name</span><span class="sxs-lookup"><span data-stu-id="98f12-113">-Name</span></span>
<span data-ttu-id="98f12-114">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="98f12-114">Name of the PowerBI Embedded Capacity</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98f12-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98f12-115">CommonParameters</span></span>
<span data-ttu-id="98f12-116">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98f12-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98f12-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98f12-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98f12-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="98f12-118">INPUTS</span></span>

### <span data-ttu-id="98f12-119">Keine</span><span class="sxs-lookup"><span data-stu-id="98f12-119">None</span></span>

## <span data-ttu-id="98f12-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="98f12-120">OUTPUTS</span></span>

### <span data-ttu-id="98f12-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="98f12-121">System.Boolean</span></span>

## <span data-ttu-id="98f12-122">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="98f12-122">NOTES</span></span>

## <span data-ttu-id="98f12-123">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="98f12-123">RELATED LINKS</span></span>

[<span data-ttu-id="98f12-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="98f12-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="98f12-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="98f12-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
