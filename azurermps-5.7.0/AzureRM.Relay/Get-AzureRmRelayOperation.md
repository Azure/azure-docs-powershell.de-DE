---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayOperation.md
ms.openlocfilehash: 2ec1fc27912fce9c218793d711a989d1dac285df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93502502"
---
# <span data-ttu-id="2fb7e-101">Get-AzureRmRelayOperation</span><span class="sxs-lookup"><span data-stu-id="2fb7e-101">Get-AzureRmRelayOperation</span></span>

## <span data-ttu-id="2fb7e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2fb7e-102">SYNOPSIS</span></span>
<span data-ttu-id="2fb7e-103">Liste unterstützter Relay-Vorgänge</span><span class="sxs-lookup"><span data-stu-id="2fb7e-103">List supported Relay Operations</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fb7e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fb7e-104">SYNTAX</span></span>

```
Get-AzureRmRelayOperation [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2fb7e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2fb7e-105">DESCRIPTION</span></span>
<span data-ttu-id="2fb7e-106">Das Cmdlet " **Get-AzureRmRelayOperation** " listet die unterstützten Relay-Vorgänge auf.</span><span class="sxs-lookup"><span data-stu-id="2fb7e-106">The **Get-AzureRmRelayOperation** cmdlet Lists the Relay supported Operations.</span></span>

## <span data-ttu-id="2fb7e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2fb7e-107">EXAMPLES</span></span>

### <span data-ttu-id="2fb7e-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2fb7e-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayOperation
```

<span data-ttu-id="2fb7e-109">Listet Relay-unterstützte Vorgänge auf</span><span class="sxs-lookup"><span data-stu-id="2fb7e-109">Lists Relay supported operations</span></span>

## <span data-ttu-id="2fb7e-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fb7e-110">PARAMETERS</span></span>

### <span data-ttu-id="2fb7e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fb7e-111">-DefaultProfile</span></span>
<span data-ttu-id="2fb7e-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2fb7e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2fb7e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fb7e-113">CommonParameters</span></span>
<span data-ttu-id="2fb7e-114">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fb7e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fb7e-115">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fb7e-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fb7e-116">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2fb7e-116">INPUTS</span></span>

### <span data-ttu-id="2fb7e-117">Keine</span><span class="sxs-lookup"><span data-stu-id="2fb7e-117">None</span></span>

## <span data-ttu-id="2fb7e-118">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2fb7e-118">OUTPUTS</span></span>

### <span data-ttu-id="2fb7e-119">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Relay. Models. OperationAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="2fb7e-119">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.OperationAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="2fb7e-120">Namensanzeige</span><span class="sxs-lookup"><span data-stu-id="2fb7e-120">Name                                                                            Display</span></span>
----                                                                            -------
<span data-ttu-id="2fb7e-121">Microsoft.Relay/checkNamespaceAvailability/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/register/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/read Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/Delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/read Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/Delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/read Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/Delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes</span><span class="sxs-lookup"><span data-stu-id="2fb7e-121">Microsoft.Relay/checkNamespaceAvailability/action                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/register/action                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/write                                                Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/read                                                 Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/Delete                                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/write                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/delete                            Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/authorizationRules/listkeys/action                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/write                              Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/read                               Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/Delete                             Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/write           Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/delete          Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/HybridConnections/authorizationRules/listkeys/action Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/write                                      Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/read                                       Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/Delete                                     Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/write                   Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/delete                  Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes Microsoft.Relay/namespaces/WcfRelays/authorizationRules/listkeys/action         Microsoft.Azure.Commands.Relay.Models.OperationDisplayAttributes</span></span>

## <span data-ttu-id="2fb7e-122">Notizen</span><span class="sxs-lookup"><span data-stu-id="2fb7e-122">NOTES</span></span>

## <span data-ttu-id="2fb7e-123">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2fb7e-123">RELATED LINKS</span></span>

