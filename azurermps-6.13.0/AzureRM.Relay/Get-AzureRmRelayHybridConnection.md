---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 468128f16c3a5ef7ef4b400694dbcc1c570f5488
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505285"
---
# <span data-ttu-id="65642-101">Get-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="65642-101">Get-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="65642-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="65642-102">SYNOPSIS</span></span>
<span data-ttu-id="65642-103">Ruft eine Beschreibung für den angegebenen HybridConnection im Relay-Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="65642-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65642-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="65642-104">SYNTAX</span></span>

```
Get-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65642-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="65642-105">DESCRIPTION</span></span>
<span data-ttu-id="65642-106">Das Cmdlet " **Get-AzureRmRelayHybridConnection** " Ruft eine Beschreibung für das angegebene HybridConnection im Relay-Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="65642-106">The **Get-AzureRmRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="65642-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="65642-107">EXAMPLES</span></span>

### <span data-ttu-id="65642-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="65642-108">Example 1</span></span>
```
PS C:\>Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection

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

<span data-ttu-id="65642-109">Gibt die Beschreibung des HybridConnection zurück.</span><span class="sxs-lookup"><span data-stu-id="65642-109">Returns the description of the HybridConnection.</span></span>

## <span data-ttu-id="65642-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="65642-110">PARAMETERS</span></span>

### <span data-ttu-id="65642-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65642-111">-DefaultProfile</span></span>
<span data-ttu-id="65642-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="65642-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="65642-113">-Name</span><span class="sxs-lookup"><span data-stu-id="65642-113">-Name</span></span>
<span data-ttu-id="65642-114">HybridConnections-Name.</span><span class="sxs-lookup"><span data-stu-id="65642-114">HybridConnections Name.</span></span>

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

### <span data-ttu-id="65642-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="65642-115">-Namespace</span></span>
<span data-ttu-id="65642-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="65642-116">Namespace Name.</span></span>

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

### <span data-ttu-id="65642-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65642-117">-ResourceGroupName</span></span>
<span data-ttu-id="65642-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="65642-118">Resource Group Name.</span></span>

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

### <span data-ttu-id="65642-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65642-119">CommonParameters</span></span>
<span data-ttu-id="65642-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65642-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="65642-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65642-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65642-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="65642-122">INPUTS</span></span>

### <span data-ttu-id="65642-123">System. String</span><span class="sxs-lookup"><span data-stu-id="65642-123">System.String</span></span>


## <span data-ttu-id="65642-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="65642-124">OUTPUTS</span></span>

### <span data-ttu-id="65642-125">Microsoft. Azure. Commands. Relay. Models. PSHybridConnectionAttibutes</span><span class="sxs-lookup"><span data-stu-id="65642-125">Microsoft.Azure.Commands.Relay.Models.PSHybridConnectionAttibutes</span></span>


## <span data-ttu-id="65642-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="65642-126">NOTES</span></span>

## <span data-ttu-id="65642-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="65642-127">RELATED LINKS</span></span>
