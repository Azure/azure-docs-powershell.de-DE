---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
ms.openlocfilehash: 31ced8988574aed139830b5cdd8a26ac74ffcc5f
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357200"
---
# <span data-ttu-id="639d0-101">Get-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="639d0-101">Get-AzRelayHybridConnection</span></span>

## <span data-ttu-id="639d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="639d0-102">SYNOPSIS</span></span>
<span data-ttu-id="639d0-103">Ruft eine Beschreibung für die angegebene HybridVerbindung im Namespace "Relay" ab.</span><span class="sxs-lookup"><span data-stu-id="639d0-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="639d0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="639d0-104">SYNTAX</span></span>

```
Get-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="639d0-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="639d0-105">DESCRIPTION</span></span>
<span data-ttu-id="639d0-106">Das **Cmdlet "Get-AzRelayHybridConnection"** ruft eine Beschreibung für das angegebene HybridConnection im Namespace "Relay" ab.</span><span class="sxs-lookup"><span data-stu-id="639d0-106">The **Get-AzRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="639d0-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="639d0-107">EXAMPLES</span></span>

### <span data-ttu-id="639d0-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="639d0-108">Example 1</span></span>
```
PS C:\>Get-AzRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection

CreatedAt                   : 4/12/2017 3:17:02 AM
UpdatedAt                   : 4/12/2017 3:17:02 AM
ListenerCount               : 0
RequiresClientAuthorization : True
UserMetadata                : User Meta data
Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H
                              ybridConnections/TestHybridConnection
Name                        : TestHybridConnection
Type                        : Microsoft.Relay/HybridConnections
```

<span data-ttu-id="639d0-109">Gibt die Beschreibung des HybridVerbindens zurück.</span><span class="sxs-lookup"><span data-stu-id="639d0-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="639d0-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="639d0-110">PARAMETERS</span></span>

### <span data-ttu-id="639d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="639d0-111">-DefaultProfile</span></span>
<span data-ttu-id="639d0-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="639d0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="639d0-113">-Name</span><span class="sxs-lookup"><span data-stu-id="639d0-113">-Name</span></span>
<span data-ttu-id="639d0-114">HybridConnections-Name.</span><span class="sxs-lookup"><span data-stu-id="639d0-114">HybridConnections Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="639d0-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="639d0-115">-Namespace</span></span>
<span data-ttu-id="639d0-116">Namespacename.</span><span class="sxs-lookup"><span data-stu-id="639d0-116">Namespace Name.</span></span>

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

### <span data-ttu-id="639d0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="639d0-117">-ResourceGroupName</span></span>
<span data-ttu-id="639d0-118">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="639d0-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="639d0-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="639d0-119">CommonParameters</span></span>
<span data-ttu-id="639d0-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="639d0-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="639d0-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="639d0-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="639d0-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="639d0-122">INPUTS</span></span>

### <span data-ttu-id="639d0-123">System.String</span><span class="sxs-lookup"><span data-stu-id="639d0-123">System.String</span></span>

## <span data-ttu-id="639d0-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="639d0-124">OUTPUTS</span></span>

### <span data-ttu-id="639d0-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="639d0-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="639d0-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="639d0-126">NOTES</span></span>

## <span data-ttu-id="639d0-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="639d0-127">RELATED LINKS</span></span>
