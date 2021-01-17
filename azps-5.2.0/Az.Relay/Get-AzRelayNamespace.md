---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelaynamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayNamespace.md
ms.openlocfilehash: ddbc0631b6ba6a3cb55d6e91ab951d44d644e85d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368079"
---
# <span data-ttu-id="af118-101">Get-AzRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="af118-101">Get-AzRelayNamespace</span></span>

## <span data-ttu-id="af118-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af118-102">SYNOPSIS</span></span>
<span data-ttu-id="af118-103">Ruft eine Beschreibung für den angegebenen Relay-Namespace innerhalb der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="af118-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="af118-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="af118-104">SYNTAX</span></span>

```
Get-AzRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="af118-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="af118-105">DESCRIPTION</span></span>
<span data-ttu-id="af118-106">Das **Cmdlet "Get-AzRelayNamespace"** ruft eine Beschreibung für den angegebenen Relay-Namespace innerhalb der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="af118-106">The **Get-AzRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="af118-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="af118-107">EXAMPLES</span></span>

### <span data-ttu-id="af118-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="af118-108">Example 1</span></span>
```
PS C:\> Get-AzRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1

ProvisioningState  : Succeeded
CreatedAt          : 4/12/2017 12:38:47 AM
UpdatedAt          : 4/12/2017 12:39:10 AM
ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/
MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1
Location           : West US
Tags               : {[tag1, Tag1Value]}
Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1
Name               : TestNameSpace-Relay1
Type               : Microsoft.Relay/namespaces
```

<span data-ttu-id="af118-109">Gibt eine Beschreibung des angegebenen Relay-Namespaces zurück.</span><span class="sxs-lookup"><span data-stu-id="af118-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="af118-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="af118-110">PARAMETERS</span></span>

### <span data-ttu-id="af118-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af118-111">-DefaultProfile</span></span>
<span data-ttu-id="af118-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="af118-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="af118-113">-Name</span><span class="sxs-lookup"><span data-stu-id="af118-113">-Name</span></span>
<span data-ttu-id="af118-114">Namespacename des Relays.</span><span class="sxs-lookup"><span data-stu-id="af118-114">Relay Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af118-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af118-115">-ResourceGroupName</span></span>
<span data-ttu-id="af118-116">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="af118-116">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="af118-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af118-117">CommonParameters</span></span>
<span data-ttu-id="af118-118">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af118-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af118-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af118-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af118-120">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="af118-120">INPUTS</span></span>

### <span data-ttu-id="af118-121">System.String</span><span class="sxs-lookup"><span data-stu-id="af118-121">System.String</span></span>

## <span data-ttu-id="af118-122">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="af118-122">OUTPUTS</span></span>

### <span data-ttu-id="af118-123">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="af118-123">Microsoft.Azure.Commands.Relay.Models.PSRelayNamespaceAttributes</span></span>

## <span data-ttu-id="af118-124">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="af118-124">NOTES</span></span>

## <span data-ttu-id="af118-125">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="af118-125">RELATED LINKS</span></span>
