---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 73960bb3efbc3d1a55d9894943c2f92bcf931faa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995035"
---
# <span data-ttu-id="2388c-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2388c-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="2388c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2388c-102">SYNOPSIS</span></span>
<span data-ttu-id="2388c-103">Testet das vorhanden sein einer Instanz der eingebetteten Kapazität von PowerBI.</span><span class="sxs-lookup"><span data-stu-id="2388c-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="2388c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2388c-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2388c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2388c-105">DESCRIPTION</span></span>
<span data-ttu-id="2388c-106">Das Test-AzPowerBIEmbeddedCapacity-Cmdlet testet das vorhanden sein einer Instanz der eingebetteten Kapazität von PowerBI</span><span class="sxs-lookup"><span data-stu-id="2388c-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="2388c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2388c-107">EXAMPLES</span></span>

### <span data-ttu-id="2388c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2388c-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="2388c-109">Mit diesem Befehl wird getestet, ob eine Kapazität mit dem Namen testcapacity vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2388c-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="2388c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2388c-110">PARAMETERS</span></span>

### <span data-ttu-id="2388c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2388c-111">-DefaultProfile</span></span>
<span data-ttu-id="2388c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2388c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2388c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="2388c-113">-Name</span></span>
<span data-ttu-id="2388c-114">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="2388c-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="2388c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2388c-115">CommonParameters</span></span>
<span data-ttu-id="2388c-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2388c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2388c-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2388c-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2388c-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2388c-118">INPUTS</span></span>

### <span data-ttu-id="2388c-119">Keine</span><span class="sxs-lookup"><span data-stu-id="2388c-119">None</span></span>

## <span data-ttu-id="2388c-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2388c-120">OUTPUTS</span></span>

### <span data-ttu-id="2388c-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="2388c-121">System.Boolean</span></span>

## <span data-ttu-id="2388c-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="2388c-122">NOTES</span></span>

## <span data-ttu-id="2388c-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2388c-123">RELATED LINKS</span></span>

[<span data-ttu-id="2388c-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2388c-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="2388c-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="2388c-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
