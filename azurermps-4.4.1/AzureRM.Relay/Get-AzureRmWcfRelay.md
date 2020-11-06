---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmWcfRelay.md
ms.openlocfilehash: 81463fc5202c9b5990e5d73d81c7bc2cbeadcca0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496934"
---
# <span data-ttu-id="73a0b-101">Get-AzureRmWcfRelay</span><span class="sxs-lookup"><span data-stu-id="73a0b-101">Get-AzureRmWcfRelay</span></span>

## <span data-ttu-id="73a0b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="73a0b-102">SYNOPSIS</span></span>
<span data-ttu-id="73a0b-103">Gibt eine Beschreibung für den angegebenen WcfRelay zurück.</span><span class="sxs-lookup"><span data-stu-id="73a0b-103">Returns a description for the specified WcfRelay.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73a0b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="73a0b-104">SYNTAX</span></span>

```
Get-AzureRmWcfRelay [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73a0b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73a0b-105">DESCRIPTION</span></span>
<span data-ttu-id="73a0b-106">Das Cmdlet " **Get-AzureRmWcfRelay** " gibt eine Beschreibung des angegebenen WcfRelay zurück.</span><span class="sxs-lookup"><span data-stu-id="73a0b-106">The **Get-AzureRmWcfRelay** cmdlet returns a description of the specified WcfRelay.</span></span>

## <span data-ttu-id="73a0b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73a0b-107">EXAMPLES</span></span>

### <span data-ttu-id="73a0b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="73a0b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmWcfRelay -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name TestWCFRelay1
```

<span data-ttu-id="73a0b-109">Gibt die Beschreibung des WcfRelay zurück.</span><span class="sxs-lookup"><span data-stu-id="73a0b-109">Returns the description of the WcfRelay.</span></span> 

## <span data-ttu-id="73a0b-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="73a0b-110">PARAMETERS</span></span>

### <span data-ttu-id="73a0b-111">-Namespace</span><span class="sxs-lookup"><span data-stu-id="73a0b-111">-Namespace</span></span>
<span data-ttu-id="73a0b-112">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="73a0b-112">Namespace Name.</span></span>

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

### <span data-ttu-id="73a0b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73a0b-113">-ResourceGroupName</span></span>
<span data-ttu-id="73a0b-114">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="73a0b-114">Resource Group Name.</span></span>

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

### <span data-ttu-id="73a0b-115">-Name</span><span class="sxs-lookup"><span data-stu-id="73a0b-115">-Name</span></span>
<span data-ttu-id="73a0b-116">WcfRelay-Name.</span><span class="sxs-lookup"><span data-stu-id="73a0b-116">WcfRelay Name.</span></span>

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

### <span data-ttu-id="73a0b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73a0b-117">-DefaultProfile</span></span>
<span data-ttu-id="73a0b-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="73a0b-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73a0b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73a0b-119">CommonParameters</span></span>
<span data-ttu-id="73a0b-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73a0b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73a0b-121">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73a0b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73a0b-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="73a0b-122">INPUTS</span></span>

### <span data-ttu-id="73a0b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="73a0b-123">-ResourceGroupName</span></span>
 <span data-ttu-id="73a0b-124">System. String</span><span class="sxs-lookup"><span data-stu-id="73a0b-124">System.String</span></span>
 

### <span data-ttu-id="73a0b-125">-Namespace</span><span class="sxs-lookup"><span data-stu-id="73a0b-125">-Namespace</span></span>
 <span data-ttu-id="73a0b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="73a0b-126">System.String</span></span>
 

### <span data-ttu-id="73a0b-127">-Name</span><span class="sxs-lookup"><span data-stu-id="73a0b-127">-Name</span></span>
 <span data-ttu-id="73a0b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="73a0b-128">System.String</span></span> 

## <span data-ttu-id="73a0b-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="73a0b-129">OUTPUTS</span></span>

### <span data-ttu-id="73a0b-130">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Relay. Models. WcfRelayAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="73a0b-130">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.WcfRelayAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="73a0b-131">Relaytype: NetTcp CreatedAt: 4/12/2017 2:23:08 am UpdatedAt: 4/12/2017 2:23:08 am ListenerCount: 0 RequiresClientAuthorization: true RequiresTransportSecurity: true IsDynamic: false UserMetadata: Benutzer-Meta-Daten-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1: TestWCFRelay1 Typ: Microsoft. Relay/WcfRelays</span><span class="sxs-lookup"><span data-stu-id="73a0b-131">RelayType                   : NetTcp CreatedAt                   : 4/12/2017 2:23:08 AM UpdatedAt                   : 4/12/2017 2:23:08 AM ListenerCount               : 0 RequiresClientAuthorization : True RequiresTransportSecurity   : True IsDynamic                   : False UserMetadata                : User Meta data Id                          : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/W cfRelays/TestWCFRelay1 Name                        : TestWCFRelay1 Type                        : Microsoft.Relay/WcfRelays</span></span>

## <span data-ttu-id="73a0b-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="73a0b-132">NOTES</span></span>

## <span data-ttu-id="73a0b-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="73a0b-133">RELATED LINKS</span></span>

