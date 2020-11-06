---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermserviceendpointpolicydefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmServiceEndpointPolicyDefinition.md
ms.openlocfilehash: 3d406bf0dffb0ee250e1494fc05727d0a4c983ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503506"
---
# <span data-ttu-id="a8275-101">Remove-AzureRmServiceEndpointPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="a8275-101">Remove-AzureRmServiceEndpointPolicyDefinition</span></span>

## <span data-ttu-id="a8275-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a8275-102">SYNOPSIS</span></span>
<span data-ttu-id="a8275-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="a8275-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a8275-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8275-104">SYNTAX</span></span>

```
Remove-AzureRmServiceEndpointPolicyDefinition [-Name <String>] -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a8275-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8275-105">DESCRIPTION</span></span>
<span data-ttu-id="a8275-106">Das Cmdlet **Remove-AzureRmServiceEndpointPolicy** entfernt eine Dienstendpunkt Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="a8275-106">The **Remove-AzureRmServiceEndpointPolicy** cmdlet removes a service endpoint policy.</span></span>

## <span data-ttu-id="a8275-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a8275-107">EXAMPLES</span></span>

### <span data-ttu-id="a8275-108">Beispiel 1: entfernt eine Dienstendpunkt-Richtlinie mit dem Namen</span><span class="sxs-lookup"><span data-stu-id="a8275-108">Example 1: Removes a service endpoint policy using name</span></span>
```
Remove-AzureRmServiceEndpointPolicyDefinition -Name "PolicyDef1"
```

<span data-ttu-id="a8275-109">Dieser Befehl entfernt eine Dienstendpunkt Richtlinie mit dem Namen PolicyDef1</span><span class="sxs-lookup"><span data-stu-id="a8275-109">This command removes a service endpoint policy with name PolicyDef1</span></span>

## <span data-ttu-id="a8275-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="a8275-110">PARAMETERS</span></span>

### <span data-ttu-id="a8275-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8275-111">-DefaultProfile</span></span>
<span data-ttu-id="a8275-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a8275-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8275-113">-Name</span><span class="sxs-lookup"><span data-stu-id="a8275-113">-Name</span></span>
<span data-ttu-id="a8275-114">Der Name der Dienstendpunkt Definition</span><span class="sxs-lookup"><span data-stu-id="a8275-114">The name of the service endpoint definition</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a8275-115">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a8275-115">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="a8275-116">Die ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a8275-116">The ServiceEndpointPolicy</span></span>

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

### <span data-ttu-id="a8275-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8275-117">CommonParameters</span></span>
<span data-ttu-id="a8275-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8275-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a8275-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8275-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8275-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a8275-120">INPUTS</span></span>

### <span data-ttu-id="a8275-121">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a8275-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="a8275-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a8275-122">OUTPUTS</span></span>

### <span data-ttu-id="a8275-123">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="a8275-123">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="a8275-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="a8275-124">NOTES</span></span>

## <span data-ttu-id="a8275-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a8275-125">RELATED LINKS</span></span>
