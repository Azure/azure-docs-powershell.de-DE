---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayhybridconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayHybridConnection.md
ms.openlocfilehash: 08a20958975d78a945e3e73729d5841f6dda6811
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500434"
---
# <span data-ttu-id="3a367-101">Get-AzureRmRelayHybridConnection</span><span class="sxs-lookup"><span data-stu-id="3a367-101">Get-AzureRmRelayHybridConnection</span></span>

## <span data-ttu-id="3a367-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3a367-102">SYNOPSIS</span></span>
<span data-ttu-id="3a367-103">Ruft eine Beschreibung für den angegebenen HybridConnection im Relay-Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="3a367-103">Gets a description for the specified HybridConnection within the Relay namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3a367-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a367-104">SYNTAX</span></span>

```
Get-AzureRmRelayHybridConnection [-ResourceGroupName] <String> [-Namespace] <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3a367-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3a367-105">DESCRIPTION</span></span>
<span data-ttu-id="3a367-106">Das Cmdlet " **Get-AzureRmRelayHybridConnection** " Ruft eine Beschreibung für das angegebene HybridConnection im Relay-Namespace ab.</span><span class="sxs-lookup"><span data-stu-id="3a367-106">The **Get-AzureRmRelayHybridConnection** cmdlet gets a description for the specified HybridConnection within the Relay namespace.</span></span>

## <span data-ttu-id="3a367-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3a367-107">EXAMPLES</span></span>

### <span data-ttu-id="3a367-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3a367-108">Example 1</span></span>
```
PS C:\>Get-AzureRmRelayHybridConnection -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestHybridConnection
```

<span data-ttu-id="3a367-109">Gibt die Beschreibung des HybridConnection zurück.</span><span class="sxs-lookup"><span data-stu-id="3a367-109">Returns the description of the HybridConnection.</span></span> 

## <span data-ttu-id="3a367-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a367-110">PARAMETERS</span></span>

### <span data-ttu-id="3a367-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a367-111">-DefaultProfile</span></span>
<span data-ttu-id="3a367-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3a367-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3a367-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3a367-113">-Name</span></span>
<span data-ttu-id="3a367-114">HybridConnections-Name.</span><span class="sxs-lookup"><span data-stu-id="3a367-114">HybridConnections Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a367-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3a367-115">-Namespace</span></span>
<span data-ttu-id="3a367-116">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="3a367-116">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a367-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a367-117">-ResourceGroupName</span></span>
<span data-ttu-id="3a367-118">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3a367-118">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a367-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a367-119">CommonParameters</span></span>
<span data-ttu-id="3a367-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a367-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a367-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a367-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a367-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3a367-122">INPUTS</span></span>

### <span data-ttu-id="3a367-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a367-123">-ResourceGroupName</span></span>
    System.String

### <span data-ttu-id="3a367-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3a367-124">-Namespace</span></span>
    System.String

### <span data-ttu-id="3a367-125">-Name</span><span class="sxs-lookup"><span data-stu-id="3a367-125">-Name</span></span>
    System.String

## <span data-ttu-id="3a367-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3a367-126">OUTPUTS</span></span>

### <span data-ttu-id="3a367-127">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Relay. Models. HybridConnectionAttibutes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="3a367-127">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.HybridConnectionAttibutes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="3a367-128">CreatedAt: 4/12/2017 3:17:02 am UpdatedAt: 4/12/2017 3:17:02 am ListenerCount: 0 RequiresClientAuthorization: true UserMetadata: Benutzer-Meta-Daten-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name: TestHybridConnection-Typ: Microsoft. Relay/HybridConnections</span><span class="sxs-lookup"><span data-stu-id="3a367-128">CreatedAt                   : 4/12/2017 3:17:02 AM UpdatedAt                   : 4/12/2017 3:17:02 AM ListenerCount               : 0 RequiresClientAuthorization : True UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/H ybridConnections/TestHybridConnection Name                        : TestHybridConnection Type                        : Microsoft.Relay/HybridConnections</span></span>

## <span data-ttu-id="3a367-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="3a367-129">NOTES</span></span>

## <span data-ttu-id="3a367-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3a367-130">RELATED LINKS</span></span>

