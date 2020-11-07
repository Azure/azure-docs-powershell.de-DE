---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: ecd5a8eafc70a88b4ebda17a83f2b40139f5463f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663121"
---
# <span data-ttu-id="4c7b5-101">Set-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4c7b5-101">Set-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="4c7b5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4c7b5-102">SYNOPSIS</span></span>
<span data-ttu-id="4c7b5-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="4c7b5-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4c7b5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c7b5-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c7b5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c7b5-105">DESCRIPTION</span></span>
<span data-ttu-id="4c7b5-106">Das Cmdlet " **festlegen-AzureRmServiceEndpointPolicy** " erstellt eine Dienstendpunkt Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="4c7b5-106">The **Set-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="4c7b5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c7b5-107">EXAMPLES</span></span>

### <span data-ttu-id="4c7b5-108">Beispiel 1: Festlegen einer Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="4c7b5-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="4c7b5-109">Mit diesem Befehl wird eine Dienstendpunkt Richtlinie mit dem Namen "Fischereipolitik1" aktualisiert, die durch das Objekt definiert ist $serviceEndpointPolicy der "resourcegroup1"-ResourceGroup angehören.</span><span class="sxs-lookup"><span data-stu-id="4c7b5-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="4c7b5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c7b5-110">PARAMETERS</span></span>

### <span data-ttu-id="4c7b5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c7b5-111">-DefaultProfile</span></span>
<span data-ttu-id="4c7b5-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4c7b5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4c7b5-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4c7b5-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="4c7b5-114">Die ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4c7b5-114">The ServiceEndpointPolicy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c7b5-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c7b5-115">CommonParameters</span></span>
<span data-ttu-id="4c7b5-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c7b5-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="4c7b5-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c7b5-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c7b5-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4c7b5-118">INPUTS</span></span>

### <span data-ttu-id="4c7b5-119">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4c7b5-119">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="4c7b5-120">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4c7b5-120">OUTPUTS</span></span>

### <span data-ttu-id="4c7b5-121">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="4c7b5-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="4c7b5-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="4c7b5-122">NOTES</span></span>

## <span data-ttu-id="4c7b5-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4c7b5-123">RELATED LINKS</span></span>
