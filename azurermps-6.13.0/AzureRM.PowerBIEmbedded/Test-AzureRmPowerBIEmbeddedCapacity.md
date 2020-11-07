---
external help file: Microsoft.Azure.Commands.PowerBI.dll-Help.xml
Module Name: AzureRM.PowerBIEmbedded
ms.assetid: 5321FC62-3585-4493-A3D2-22CD82503CA7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.powerbiembedded/test-azurermpowerbiembeddedcapacity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/PowerBIEmbedded/Commands.PowerBI/help/Test-AzureRmPowerBIEmbeddedCapacity.md
ms.openlocfilehash: 306bb6e4e12adcb4a4eda65b2517ddf0648a81fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663116"
---
# <span data-ttu-id="a5a2c-101">Test-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a5a2c-101">Test-AzureRmPowerBIEmbeddedCapacity</span></span>

## <span data-ttu-id="a5a2c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5a2c-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a2c-103">Testet das vorhanden sein einer Instanz der eingebetteten Kapazität von PowerBI.</span><span class="sxs-lookup"><span data-stu-id="a5a2c-103">Tests the existence of an instance of PowerBI Embedded Capacity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5a2c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5a2c-104">SYNTAX</span></span>

```
Test-AzureRmPowerBIEmbeddedCapacity [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a5a2c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5a2c-105">DESCRIPTION</span></span>
<span data-ttu-id="a5a2c-106">Das Test-AzureRmPowerBIEmbeddedCapacity-Cmdlet testet das vorhanden sein einer Instanz der eingebetteten Kapazität von PowerBI</span><span class="sxs-lookup"><span data-stu-id="a5a2c-106">The Test-AzureRmPowerBIEmbeddedCapacity cmdlet tests the existence of an instance of PowerBI Embedded Capacity</span></span>

## <span data-ttu-id="a5a2c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5a2c-107">EXAMPLES</span></span>

### <span data-ttu-id="a5a2c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a5a2c-108">Example 1</span></span>
```
PS C:\> Test-AzureRmPowerBIEmbeddedCapacity -Name "testcapacity"
True
```

<span data-ttu-id="a5a2c-109">Mit diesem Befehl wird getestet, ob eine Kapazität mit dem Namen testcapacity vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="a5a2c-109">This command will test if there is a capacity named testcapacity</span></span>

## <span data-ttu-id="a5a2c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5a2c-110">PARAMETERS</span></span>

### <span data-ttu-id="a5a2c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a2c-111">-DefaultProfile</span></span>
<span data-ttu-id="a5a2c-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a5a2c-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a2c-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a5a2c-113">-Name</span></span>
<span data-ttu-id="a5a2c-114">Name der eingebetteten PowerBI-Kapazität</span><span class="sxs-lookup"><span data-stu-id="a5a2c-114">Name of the PowerBI Embedded Capacity</span></span>

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

### <span data-ttu-id="a5a2c-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a2c-115">CommonParameters</span></span>
<span data-ttu-id="a5a2c-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a2c-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a2c-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a2c-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a2c-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5a2c-118">INPUTS</span></span>

### <span data-ttu-id="a5a2c-119">Keine</span><span class="sxs-lookup"><span data-stu-id="a5a2c-119">None</span></span>

## <span data-ttu-id="a5a2c-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5a2c-120">OUTPUTS</span></span>

### <span data-ttu-id="a5a2c-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5a2c-121">System.Boolean</span></span>

## <span data-ttu-id="a5a2c-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5a2c-122">NOTES</span></span>

## <span data-ttu-id="a5a2c-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5a2c-123">RELATED LINKS</span></span>

[<span data-ttu-id="a5a2c-124">Get-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a5a2c-124">Get-AzureRmPowerBIEmbeddedCapacity</span></span>](./Get-AzureRmPowerBIEmbeddedCapacity.md)

[<span data-ttu-id="a5a2c-125">Remove-AzureRmPowerBIEmbeddedCapacity</span><span class="sxs-lookup"><span data-stu-id="a5a2c-125">Remove-AzureRmPowerBIEmbeddedCapacity</span></span>](./Remove-AzureRmPowerBIEmbeddedCapacity.md)
