---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
ms.openlocfilehash: 21bf1e235d9e6b2f6bb4d2017b69f607e559e46b
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459571"
---
# <span data-ttu-id="9d903-101">Get-AzRelayOperation</span><span class="sxs-lookup"><span data-stu-id="9d903-101">Get-AzRelayOperation</span></span>

## <span data-ttu-id="9d903-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d903-102">SYNOPSIS</span></span>
<span data-ttu-id="9d903-103">Liste unterstützter Relayvorgänge</span><span class="sxs-lookup"><span data-stu-id="9d903-103">List supported Relay Operations</span></span>

## <span data-ttu-id="9d903-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d903-104">SYNTAX</span></span>

```
Get-AzRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9d903-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d903-105">DESCRIPTION</span></span>
<span data-ttu-id="9d903-106">Das **Cmdlet "Get-AzRelayOperation"** listet die von Relay unterstützten Vorgänge auf.</span><span class="sxs-lookup"><span data-stu-id="9d903-106">The **Get-AzRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="9d903-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9d903-107">EXAMPLES</span></span>

### <span data-ttu-id="9d903-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9d903-108">Example 1</span></span>
```
PS C:\> Get-AzRelayOperation

Name                                                                            Display
----                                                                            -------
Microsoft.Relay/checkNamespaceAvailability/action                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/register/action                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/write                                                Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/read                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/Delete                                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/write                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/delete                            Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/authorizationRules/listkeys/action                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/write                              Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/read                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/Delete                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write           Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete          Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/write                                      Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/read                                       Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/Delete                                     Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete                  Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action         Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes
```

<span data-ttu-id="9d903-109">Von Listen relay unterstützte Vorgänge</span><span class="sxs-lookup"><span data-stu-id="9d903-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="9d903-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d903-110">PARAMETERS</span></span>

### <span data-ttu-id="9d903-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d903-111">-DefaultProfile</span></span>
<span data-ttu-id="9d903-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9d903-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9d903-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d903-113">CommonParameters</span></span>
<span data-ttu-id="9d903-114">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d903-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d903-115">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d903-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d903-116">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9d903-116">INPUTS</span></span>

### <span data-ttu-id="9d903-117">Keine</span><span class="sxs-lookup"><span data-stu-id="9d903-117">None</span></span>

## <span data-ttu-id="9d903-118">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9d903-118">OUTPUTS</span></span>

### <span data-ttu-id="9d903-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="9d903-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="9d903-120">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9d903-120">NOTES</span></span>

## <span data-ttu-id="9d903-121">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9d903-121">RELATED LINKS</span></span>
