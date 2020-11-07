---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
ms.openlocfilehash: 31ced8988574aed139830b5cdd8a26ac74ffcc5f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846896"
---
# <span data-ttu-id="4fe49-101">Get-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="4fe49-101">Get-AzRelayHybridConnection</span></span>

## <span data-ttu-id="4fe49-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4fe49-102">SYNOPSIS</span></span>
<span data-ttu-id="4fe49-103">Ruft eine Beschreibung für den angegebenen HybridConnection im Relay-Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="4fe49-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="4fe49-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4fe49-104">SYNTAX</span></span>

```
Get-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4fe49-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4fe49-105">DESCRIPTION</span></span>
<span data-ttu-id="4fe49-106">Das Cmdlet " **Get-AzRelayHybridConnection** " Ruft eine Beschreibung für das angegebene HybridConnection im Relay-Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="4fe49-106">The **Get-AzRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="4fe49-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4fe49-107">EXAMPLES</span></span>

### <span data-ttu-id="4fe49-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4fe49-108">Example 1</span></span>
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

<span data-ttu-id="4fe49-109">Gibt die Beschreibung des HybridConnection zurück.</span><span class="sxs-lookup"><span data-stu-id="4fe49-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="4fe49-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="4fe49-110">PARAMETERS</span></span>

### <span data-ttu-id="4fe49-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4fe49-111">-DefaultProfile</span></span>
<span data-ttu-id="4fe49-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4fe49-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4fe49-113">-Name</span><span class="sxs-lookup"><span data-stu-id="4fe49-113">-Name</span></span>
<span data-ttu-id="4fe49-114">HybridConnections-Name.</span><span class="sxs-lookup"><span data-stu-id="4fe49-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="4fe49-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4fe49-115">-Namespace</span></span>
<span data-ttu-id="4fe49-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="4fe49-116">Namespace Name.</span></span>

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

### <span data-ttu-id="4fe49-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4fe49-117">-ResourceGroupName</span></span>
<span data-ttu-id="4fe49-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4fe49-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="4fe49-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4fe49-119">CommonParameters</span></span>
<span data-ttu-id="4fe49-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4fe49-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4fe49-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4fe49-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4fe49-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4fe49-122">INPUTS</span></span>

### <span data-ttu-id="4fe49-123">System. String</span><span class="sxs-lookup"><span data-stu-id="4fe49-123">System.String</span></span>

## <span data-ttu-id="4fe49-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4fe49-124">OUTPUTS</span></span>

### <span data-ttu-id="4fe49-125">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="4fe49-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="4fe49-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="4fe49-126">NOTES</span></span>

## <span data-ttu-id="4fe49-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4fe49-127">RELATED LINKS</span></span>
