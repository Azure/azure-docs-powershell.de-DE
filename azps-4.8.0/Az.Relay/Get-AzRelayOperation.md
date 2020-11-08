---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayOperation.md
ms.openlocfilehash: 21bf1e235d9e6b2f6bb4d2017b69f607e559e46b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166146"
---
# <span data-ttu-id="f71ed-101">Get-AzRelayOperation</span><span class="sxs-lookup"><span data-stu-id="f71ed-101">Get-AzRelayOperation</span></span>

## <span data-ttu-id="f71ed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f71ed-102">SYNOPSIS</span></span>
<span data-ttu-id="f71ed-103">Liste unterstützter Relay-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="f71ed-103">List supported Relay Operations</span></span>

## <span data-ttu-id="f71ed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f71ed-104">SYNTAX</span></span>

```
Get-AzRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f71ed-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f71ed-105">DESCRIPTION</span></span>
<span data-ttu-id="f71ed-106">Das Cmdlet " **Get-AzRelayOperation** " listet die unterstützten Relay-Vorgänge auf.</span><span class="sxs-lookup"><span data-stu-id="f71ed-106">The **Get-AzRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="f71ed-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f71ed-107">EXAMPLES</span></span>

### <span data-ttu-id="f71ed-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f71ed-108">Example 1</span></span>
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

<span data-ttu-id="f71ed-109">Listet Relay-unterstützte Vorgänge auf</span><span class="sxs-lookup"><span data-stu-id="f71ed-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="f71ed-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f71ed-110">PARAMETERS</span></span>

### <span data-ttu-id="f71ed-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f71ed-111">-DefaultProfile</span></span>
<span data-ttu-id="f71ed-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f71ed-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f71ed-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f71ed-113">CommonParameters</span></span>
<span data-ttu-id="f71ed-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f71ed-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f71ed-115">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f71ed-115">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f71ed-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f71ed-116">INPUTS</span></span>

### <span data-ttu-id="f71ed-117">Keine</span><span class="sxs-lookup"><span data-stu-id="f71ed-117">None</span></span>

## <span data-ttu-id="f71ed-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f71ed-118">OUTPUTS</span></span>

### <span data-ttu-id="f71ed-119">Microsoft. Azure. Commands. Relay. Models. PSOperationAttributes</span><span class="sxs-lookup"><span data-stu-id="f71ed-119">Microsoft.Azure.Commands.Relay.Models.PSOperationAttributes</span></span>

## <span data-ttu-id="f71ed-120">Notizen</span><span class="sxs-lookup"><span data-stu-id="f71ed-120">NOTES</span></span>

## <span data-ttu-id="f71ed-121">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f71ed-121">RELATED LINKS</span></span>
