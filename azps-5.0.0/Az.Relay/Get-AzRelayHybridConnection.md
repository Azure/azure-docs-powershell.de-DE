---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/get-azrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Get-AzRelayHybridConnection.md
ms.openlocfilehash: 31ced8988574aed139830b5cdd8a26ac74ffcc5f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94302629"
---
# <span data-ttu-id="dd53a-101">Get-AzRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="dd53a-101">Get-AzRelayHybridConnection</span></span>

## <span data-ttu-id="dd53a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dd53a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd53a-103">Ruft eine Beschreibung für den angegebenen HybridConnection im Relay-Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="dd53a-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="dd53a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dd53a-104">SYNTAX</span></span>

```
Get-AzRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd53a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd53a-105">DESCRIPTION</span></span>
<span data-ttu-id="dd53a-106">Das Cmdlet " **Get-AzRelayHybridConnection** " Ruft eine Beschreibung für das angegebene HybridConnection im Relay-Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="dd53a-106">The **Get-AzRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="dd53a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dd53a-107">EXAMPLES</span></span>

### <span data-ttu-id="dd53a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dd53a-108">Example 1</span></span>
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

<span data-ttu-id="dd53a-109">Gibt die Beschreibung des HybridConnection zurück.</span><span class="sxs-lookup"><span data-stu-id="dd53a-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="dd53a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dd53a-110">PARAMETERS</span></span>

### <span data-ttu-id="dd53a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd53a-111">-DefaultProfile</span></span>
<span data-ttu-id="dd53a-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dd53a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd53a-113">-Name</span><span class="sxs-lookup"><span data-stu-id="dd53a-113">-Name</span></span>
<span data-ttu-id="dd53a-114">HybridConnections-Name.</span><span class="sxs-lookup"><span data-stu-id="dd53a-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="dd53a-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dd53a-115">-Namespace</span></span>
<span data-ttu-id="dd53a-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="dd53a-116">Namespace Name.</span></span>

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

### <span data-ttu-id="dd53a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd53a-117">-ResourceGroupName</span></span>
<span data-ttu-id="dd53a-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dd53a-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="dd53a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd53a-119">CommonParameters</span></span>
<span data-ttu-id="dd53a-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd53a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd53a-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd53a-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd53a-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dd53a-122">INPUTS</span></span>

### <span data-ttu-id="dd53a-123">System. String</span><span class="sxs-lookup"><span data-stu-id="dd53a-123">System.String</span></span>

## <span data-ttu-id="dd53a-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dd53a-124">OUTPUTS</span></span>

### <span data-ttu-id="dd53a-125">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttributes</span><span class="sxs-lookup"><span data-stu-id="dd53a-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttributes</span></span>

## <span data-ttu-id="dd53a-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="dd53a-126">NOTES</span></span>

## <span data-ttu-id="dd53a-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dd53a-127">RELATED LINKS</span></span>
