---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/get-azwcfrelay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzWcfRelay.md
ms.openlocfilehash: e998bb09435abc787df78050ab25888d0e6651a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943805"
---
# <span data-ttu-id="c524b-101">Get-AzWcfRelay</span><span class="sxs-lookup"><span data-stu-id="c524b-101">Get-AzWcfRelay</span></span>

## <span data-ttu-id="c524b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c524b-102">SYNOPSIS</span></span>
<span data-ttu-id="c524b-103">Gibt eine Beschreibung für den angegebenen WcfRelay zurück.</span><span class="sxs-lookup"><span data-stu-id="c524b-103">Returns a description for the specified WcfRelay.</span></span>

## <span data-ttu-id="c524b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c524b-104">SYNTAX</span></span>

```
Get-AzWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c524b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c524b-105">DESCRIPTION</span></span>
<span data-ttu-id="c524b-106">Das **Get-AzWcfRelay-Cmdlet** gibt eine Beschreibung des angegebenen WcfRelays zurück.</span><span class="sxs-lookup"><span data-stu-id="c524b-106">The **Get-AzWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="c524b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c524b-107">EXAMPLES</span></span>

### <span data-ttu-id="c524b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c524b-108">Example 1</span></span>
```
PS C:\> Get-AzWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1

RelayType                   : NetTcp
CreatedAt                   : 4/12/2017 2:23:08 AM
UpdatedAt                   : 4/12/2017 2:23:08 AM
ListenerCount               : 0
RequiresClientAuthorization : True
RequiresTransportSecurity   : True
IsDynamic                   : False
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W
                              cfRelays/TestWCFRelay1
Name                        : TestWCFRelay1
Type                        : Microsoft.Relay/WcfRelays
```

<span data-ttu-id="c524b-109">Gibt die Beschreibung des WcfRelays zurück.</span><span class="sxs-lookup"><span data-stu-id="c524b-109">Returns the description of the WcfRelay.</span></span>

## <span data-ttu-id="c524b-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c524b-110">PARAMETERS</span></span>

### <span data-ttu-id="c524b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c524b-111">-DefaultProfile</span></span>
<span data-ttu-id="c524b-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c524b-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c524b-113">-Name</span><span class="sxs-lookup"><span data-stu-id="c524b-113">-Name</span></span>
<span data-ttu-id="c524b-114">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="c524b-114">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c524b-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c524b-115">-Namespace</span></span>
<span data-ttu-id="c524b-116">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="c524b-116">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c524b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c524b-117">-ResourceGroupName</span></span>
<span data-ttu-id="c524b-118">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="c524b-118">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c524b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c524b-119">CommonParameters</span></span>
<span data-ttu-id="c524b-120">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c524b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c524b-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c524b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c524b-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c524b-122">INPUTS</span></span>

### <span data-ttu-id="c524b-123">System.String</span><span class="sxs-lookup"><span data-stu-id="c524b-123">System.String</span></span>

## <span data-ttu-id="c524b-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c524b-124">OUTPUTS</span></span>

### <span data-ttu-id="c524b-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span><span class="sxs-lookup"><span data-stu-id="c524b-125">Microsoft.Azure.Commands.Relay.Models.PSWcfRelayAttributes</span></span>

## <span data-ttu-id="c524b-126">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c524b-126">NOTES</span></span>

## <span data-ttu-id="c524b-127">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c524b-127">RELATED LINKS</span></span>
