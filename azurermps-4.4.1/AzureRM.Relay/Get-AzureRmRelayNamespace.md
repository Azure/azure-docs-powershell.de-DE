---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM.Relay
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayNamespace.md
ms.openlocfilehash: 5f1e8037e4a9faef508c2ffd62ff00aca4387cb9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481649"
---
# <span data-ttu-id="d1005-101">Get-AzureRmRelayNamespace</span><span class="sxs-lookup"><span data-stu-id="d1005-101">Get-AzureRmRelayNamespace</span></span>

## <span data-ttu-id="d1005-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d1005-102">SYNOPSIS</span></span>
<span data-ttu-id="d1005-103">Ruft eine Beschreibung für den angegebenen Relay-Namespace innerhalb der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="d1005-103">Gets a description for the specified Relay namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1005-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d1005-104">SYNTAX</span></span>

```
Get-AzureRmRelayNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d1005-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d1005-105">DESCRIPTION</span></span>
<span data-ttu-id="d1005-106">Das Cmdlet " **Get-AzureRmRelayNamespace** " Ruft eine Beschreibung für den angegebenen Relay-Namespace innerhalb der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="d1005-106">The **Get-AzureRmRelayNamespace** cmdlet gets a description for the specified Relay namespace within the resource group.</span></span>

## <span data-ttu-id="d1005-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d1005-107">EXAMPLES</span></span>

### <span data-ttu-id="d1005-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d1005-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRelayNamespace -ResourceGroupName Default-ServiceBus-WestUS -Name TestNameSpace-Relay1
```

<span data-ttu-id="d1005-109">Gibt eine Beschreibung des angegebenen Relay-Namespaces zurück.</span><span class="sxs-lookup"><span data-stu-id="d1005-109">Returns a description of the specified Relay namespace.</span></span>

## <span data-ttu-id="d1005-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d1005-110">PARAMETERS</span></span>

### <span data-ttu-id="d1005-111">-Name</span><span class="sxs-lookup"><span data-stu-id="d1005-111">-Name</span></span>
<span data-ttu-id="d1005-112">Name des Relay-Namespaces.</span><span class="sxs-lookup"><span data-stu-id="d1005-112">Relay Namespace Name.</span></span>

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

### <span data-ttu-id="d1005-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1005-113">-ResourceGroupName</span></span>
<span data-ttu-id="d1005-114">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d1005-114">Resource Group Name.</span></span>

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

### <span data-ttu-id="d1005-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1005-115">-DefaultProfile</span></span>
<span data-ttu-id="d1005-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d1005-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d1005-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1005-117">CommonParameters</span></span>
<span data-ttu-id="d1005-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1005-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1005-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1005-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1005-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d1005-120">INPUTS</span></span>

### <span data-ttu-id="d1005-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1005-121">-ResourceGroupName</span></span>
<span data-ttu-id="d1005-122">System. String</span><span class="sxs-lookup"><span data-stu-id="d1005-122">System.String</span></span>

### <span data-ttu-id="d1005-123">-Name</span><span class="sxs-lookup"><span data-stu-id="d1005-123">-Name</span></span>
 <span data-ttu-id="d1005-124">System. String</span><span class="sxs-lookup"><span data-stu-id="d1005-124">System.String</span></span>

## <span data-ttu-id="d1005-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d1005-125">OUTPUTS</span></span>

### <span data-ttu-id="d1005-126">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Relay. Models. RelayNamespaceAttributes, Microsoft. Azure. Commands. Relay, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d1005-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.RelayNamespaceAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="d1005-127">ProvisioningState: erfolgreich CreatedAt: 4/12/2017 12:38:47 am UpdatedAt: 4/12/2017 12:39:10 am ServiceBusEndpoint: https://TestNameSpace-Relay1.servicebus.windows.net:443/ Metric: 854d368f-1828-428f-8f3c-f2affa9b2f7d: testnamespace-relay1 Ort: West US Tags: {[Tag1, Tag1Value]} ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.Relay/Namespaces/TestNameSpace-Relay1 Name: TestNameSpace-Relay1 Typ: Microsoft. Relay/Namespaces</span><span class="sxs-lookup"><span data-stu-id="d1005-127">ProvisioningState  : Succeeded CreatedAt          : 4/12/2017 12:38:47 AM UpdatedAt          : 4/12/2017 12:39:10 AM ServiceBusEndpoint : https://TestNameSpace-Relay1.servicebus.windows.net:443/ MetricId           : 854d368f-1828-428f-8f3c-f2affa9b2f7d:testnamespace-relay1 Location           : West US Tags               : {[tag1, Tag1Value]} Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1 Name               : TestNameSpace-Relay1 Type               : Microsoft.Relay/namespaces</span></span>

## <span data-ttu-id="d1005-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="d1005-128">NOTES</span></span>

## <span data-ttu-id="d1005-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d1005-129">RELATED LINKS</span></span>

