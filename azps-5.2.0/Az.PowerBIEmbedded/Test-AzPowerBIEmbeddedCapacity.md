---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 73960bb3efbc3d1a55d9894943c2f92bcf931faa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363990"
---
# <span data-ttu-id="7a40c-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="7a40c-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="7a40c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a40c-102">SYNOPSIS</span></span>
<span data-ttu-id="7a40c-103">Überprüft, ob es eine Instanz von eingebetteter PowerBI-Kapazität gibt.</span><span class="sxs-lookup"><span data-stu-id="7a40c-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="7a40c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7a40c-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7a40c-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7a40c-105">DESCRIPTION</span></span>
<span data-ttu-id="7a40c-106">Das Test-AzPowerBIEmbeddedCapacity cmdlet testet das Vorhandensein einer Instanz der eingebetteten PowerBI-Kapazität.</span><span class="sxs-lookup"><span data-stu-id="7a40c-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="7a40c-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7a40c-107">EXAMPLES</span></span>

### <span data-ttu-id="7a40c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7a40c-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="7a40c-109">Dieser Befehl testet, ob eine Kapazität mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="7a40c-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="7a40c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a40c-110">PARAMETERS</span></span>

### <span data-ttu-id="7a40c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a40c-111">-DefaultProfile</span></span>
<span data-ttu-id="7a40c-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7a40c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a40c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="7a40c-113">-Name</span></span>
<span data-ttu-id="7a40c-114">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="7a40c-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="7a40c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a40c-115">CommonParameters</span></span>
<span data-ttu-id="7a40c-116">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a40c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a40c-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a40c-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a40c-118">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7a40c-118">INPUTS</span></span>

### <span data-ttu-id="7a40c-119">Keine</span><span class="sxs-lookup"><span data-stu-id="7a40c-119">None</span></span>

## <span data-ttu-id="7a40c-120">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7a40c-120">OUTPUTS</span></span>

### <span data-ttu-id="7a40c-121">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7a40c-121">System.Boolean</span></span>

## <span data-ttu-id="7a40c-122">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7a40c-122">NOTES</span></span>

## <span data-ttu-id="7a40c-123">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7a40c-123">RELATED LINKS</span></span>

[<span data-ttu-id="7a40c-124">Get-AzPowerBIEmbedded1</span><span class="sxs-lookup"><span data-stu-id="7a40c-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="7a40c-125">Remove-AzPowerBIEmbedded1</span><span class="sxs-lookup"><span data-stu-id="7a40c-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
