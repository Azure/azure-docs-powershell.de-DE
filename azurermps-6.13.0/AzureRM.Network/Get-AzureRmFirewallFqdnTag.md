---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 98CB62E1-0A18-4207-81FA-07CC60310896
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewallfqdntag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewallFqdnTag.md
ms.openlocfilehash: 33482ff6686409c62a2aeffbf616f62074b1984e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664824"
---
# <span data-ttu-id="19071-101">Get-AzureRmFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="19071-101">Get-AzureRmFirewallFqdnTag</span></span>

## <span data-ttu-id="19071-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="19071-102">SYNOPSIS</span></span>
<span data-ttu-id="19071-103">Ruft die verfügbaren Azure Firewall-FQDN-Tags ab.</span><span class="sxs-lookup"><span data-stu-id="19071-103">Gets the available Azure Firewall Fqdn Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19071-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="19071-104">SYNTAX</span></span>

```
Get-AzureRmFirewallFqdnTag [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19071-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="19071-105">DESCRIPTION</span></span>
<span data-ttu-id="19071-106">Das Cmdlet " **Get-AzureRmFirewallFqdnTag** " Ruft die Liste der FQDN-Tags ab, die für Azure Firewall-Anwendungsregeln verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="19071-106">The **Get-AzureRmFirewallFqdnTag** cmdlet gets the list of FQDN Tags which can be used for Azure Firewall Application Rules</span></span>

## <span data-ttu-id="19071-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="19071-107">EXAMPLES</span></span>

### <span data-ttu-id="19071-108">1: Abrufen aller verfügbaren FQDN-Tags</span><span class="sxs-lookup"><span data-stu-id="19071-108">1:  Retrieve all available FQDN Tags</span></span>
```
Get-AzureRmFirewallFqdnTag
```

<span data-ttu-id="19071-109">In diesem Beispiel werden alle verfügbaren FQDN-Tags abgerufen.</span><span class="sxs-lookup"><span data-stu-id="19071-109">This example retrieves all available FQDN Tags.</span></span>

### <span data-ttu-id="19071-110">2: Verwenden des ersten verfügbaren FQDN-Tags in einer Anwendungsregel</span><span class="sxs-lookup"><span data-stu-id="19071-110">2:  Use first available FQDN Tag in an Application Rule</span></span>
```
$fqdnTags = Get-AzureRmFirewallFqdnTag
New-AzureRmFirewallApplicationRule -Name AR -SourceAddress * -FqdnTag $fqdnTags[0].FqdnTagName
```

<span data-ttu-id="19071-111">In diesem Beispiel wird eine Firewall-Anwendungsregel mit dem ersten verfügbaren FQDN-Tag erstellt</span><span class="sxs-lookup"><span data-stu-id="19071-111">This example creates a Firewall Application Rule using the first available FQDN Tag</span></span>

## <span data-ttu-id="19071-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="19071-112">PARAMETERS</span></span>

### <span data-ttu-id="19071-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19071-113">-DefaultProfile</span></span>
<span data-ttu-id="19071-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="19071-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19071-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19071-115">CommonParameters</span></span>
<span data-ttu-id="19071-116">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19071-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19071-117">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19071-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19071-118">Eingaben</span><span class="sxs-lookup"><span data-stu-id="19071-118">INPUTS</span></span>

### <span data-ttu-id="19071-119">Keine</span><span class="sxs-lookup"><span data-stu-id="19071-119">None</span></span>
<span data-ttu-id="19071-120">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="19071-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="19071-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="19071-121">OUTPUTS</span></span>

### <span data-ttu-id="19071-122">Microsoft. Azure. Commands. Network. Models. PSAzureFirewallFqdnTag</span><span class="sxs-lookup"><span data-stu-id="19071-122">Microsoft.Azure.Commands.Network.Models.PSAzureFirewallFqdnTag</span></span>

## <span data-ttu-id="19071-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="19071-123">NOTES</span></span>

## <span data-ttu-id="19071-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="19071-124">RELATED LINKS</span></span>

[<span data-ttu-id="19071-125">Neu – AzureRmFirewallApplicationRule</span><span class="sxs-lookup"><span data-stu-id="19071-125">New-AzureRmFirewallApplicationRule</span></span>](./New-AzureRmFirewallApplicationRule.md)

[<span data-ttu-id="19071-126">Neu – AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="19071-126">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)
