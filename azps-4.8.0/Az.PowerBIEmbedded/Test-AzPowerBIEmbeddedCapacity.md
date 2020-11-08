---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBI.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/test-azpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Test-AzPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 73960bb3efbc3d1a55d9894943c2f92bcf931faa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009601"
---
# <span data-ttu-id="cce74-101">Test-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="cce74-101">Test-AzPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="cce74-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cce74-102">SYNOPSIS</span></span>
<span data-ttu-id="cce74-103">Testet das vorhanden sein einer Instanz der eingebetteten Kapazität von PowerBI.</span><span class="sxs-lookup"><span data-stu-id="cce74-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

## <span data-ttu-id="cce74-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cce74-104">SYNTAX</span></span>

```
Test-AzPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cce74-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cce74-105">DESCRIPTION</span></span>
<span data-ttu-id="cce74-106">Das Test-AzPowerBIEmbeddedCapacity-Cmdlet testet das vorhanden sein einer Instanz der eingebetteten Kapazität von PowerBI</span><span class="sxs-lookup"><span data-stu-id="cce74-106">The Test-AzPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="cce74-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cce74-107">EXAMPLES</span></span>

### <span data-ttu-id="cce74-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="cce74-108">Example 1</span></span>
```
PS C:\> Test-AzPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="cce74-109">Mit diesem Befehl wird getestet, ob eine Kapazität mit dem Namen testcapacity vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="cce74-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="cce74-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cce74-110">PARAMETERS</span></span>

### <span data-ttu-id="cce74-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cce74-111">-DefaultProfile</span></span>
<span data-ttu-id="cce74-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cce74-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cce74-113">-Name</span><span class="sxs-lookup"><span data-stu-id="cce74-113">-Name</span></span>
<span data-ttu-id="cce74-114">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="cce74-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="cce74-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cce74-115">CommonParameters</span></span>
<span data-ttu-id="cce74-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cce74-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cce74-117">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cce74-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cce74-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cce74-118">INPUTS</span></span>

### <span data-ttu-id="cce74-119">Keine</span><span class="sxs-lookup"><span data-stu-id="cce74-119">None</span></span>

## <span data-ttu-id="cce74-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cce74-120">OUTPUTS</span></span>

### <span data-ttu-id="cce74-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="cce74-121">System.Boolean</span></span>

## <span data-ttu-id="cce74-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="cce74-122">NOTES</span></span>

## <span data-ttu-id="cce74-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cce74-123">RELATED LINKS</span></span>

[<span data-ttu-id="cce74-124">Get-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="cce74-124">Get-AzPowerBIEmbeddedCapacity</span></span>](./Get-AzPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="cce74-125">Remove-AzPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="cce74-125">Remove-AzPowerBIEmbeddedCapacity</span></span>](./Remove-AzPowerBIEmbeddedCapacity.md)
