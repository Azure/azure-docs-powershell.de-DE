---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: 989b6aa91c0dabec1b72425f214c4097df374041
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480321"
---
# <span data-ttu-id="32eea-101">Get-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="32eea-101">Get-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="32eea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="32eea-102">SYNOPSIS</span></span>
<span data-ttu-id="32eea-103">{{Füllen Sie die Zusammenfassung aus}}</span><span class="sxs-lookup"><span data-stu-id="32eea-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="32eea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="32eea-104">SYNTAX</span></span>

```
Get-AzureRmServiceEndpointPolicy -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="32eea-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="32eea-105">DESCRIPTION</span></span>
<span data-ttu-id="32eea-106">Das Cmdlet " **Get-AzureRmServiceEndpointPolicy** " Ruft eine Dienstendpunkt Richtlinie ab.</span><span class="sxs-lookup"><span data-stu-id="32eea-106">The **Get-AzureRmServiceEndpointPolicy** cmdlet gets a service endpoint policy.</span></span>

## <span data-ttu-id="32eea-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="32eea-107">EXAMPLES</span></span>

### <span data-ttu-id="32eea-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="32eea-108">Example 1</span></span>
```
$policy = Get-AzureRmServiceEndpointPolicy -Name "ServiceEndpointPolicy1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="32eea-109">Dieser Befehl ruft die Dienstendpunkt Richtlinie mit dem Namen ServiceEndpointPolicy1 ab, die zur Ressourcengruppe mit dem Namen ResourceGroup01 gehört, und speichert Sie in der $Policy-Variablen.</span><span class="sxs-lookup"><span data-stu-id="32eea-109">This command gets the service endpoint policy named ServiceEndpointPolicy1 that belongs to the resource group named ResourceGroup01 and stores it in the $policy variable.</span></span>

### <span data-ttu-id="32eea-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="32eea-110">Example 2</span></span>
```
$policyList = Get-AzureRmServiceEndpointPolicy -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="32eea-111">Dieser Befehl ruft eine Liste aller Dienstendpunkt Richtlinien in der Ressourcengruppe mit dem Namen ResourceGroup01 ab und speichert Sie in der $policyList-Variablen.</span><span class="sxs-lookup"><span data-stu-id="32eea-111">This command gets a list of all the service endpoint policies in the resource group named ResourceGroup01 and stores it in the $policyList variable.</span></span>

## <span data-ttu-id="32eea-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="32eea-112">PARAMETERS</span></span>

### <span data-ttu-id="32eea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32eea-113">-DefaultProfile</span></span>
<span data-ttu-id="32eea-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="32eea-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="32eea-115">-Name</span><span class="sxs-lookup"><span data-stu-id="32eea-115">-Name</span></span>
<span data-ttu-id="32eea-116">Der Name der Dienstendpunkt Richtlinie</span><span class="sxs-lookup"><span data-stu-id="32eea-116">The name of the service endpoint policy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32eea-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32eea-117">-ResourceGroupName</span></span>
<span data-ttu-id="32eea-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="32eea-118">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32eea-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32eea-119">CommonParameters</span></span>
<span data-ttu-id="32eea-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32eea-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="32eea-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32eea-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32eea-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="32eea-122">INPUTS</span></span>

### <span data-ttu-id="32eea-123">System. String</span><span class="sxs-lookup"><span data-stu-id="32eea-123">System.String</span></span>


## <span data-ttu-id="32eea-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="32eea-124">OUTPUTS</span></span>

### <span data-ttu-id="32eea-125">Microsoft. Azure. Commands. Network. Models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="32eea-125">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="32eea-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="32eea-126">NOTES</span></span>

## <span data-ttu-id="32eea-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="32eea-127">RELATED LINKS</span></span>
