---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 2e6e044d888386b56d04ad48b7fbdaedadbd7497
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662400"
---
# <span data-ttu-id="ae6a4-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="ae6a4-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="ae6a4-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ae6a4-102">SYNOPSIS</span></span>
<span data-ttu-id="ae6a4-103">Ruft eine Beschreibung für den angegebenen ServiceBus-Namespace innerhalb der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae6a4-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ae6a4-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae6a4-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ae6a4-105">DESCRIPTION</span></span>
<span data-ttu-id="ae6a4-106">Das Cmdlet " **Get-AzureRmServiceBusNamespace** " Ruft eine Beschreibung für den angegebenen ServiceBus-Namespace innerhalb der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="ae6a4-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ae6a4-107">EXAMPLES</span></span>

### <span data-ttu-id="ae6a4-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ae6a4-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1
```

<span data-ttu-id="ae6a4-109">Gibt eine Beschreibung des angegebenen ServiceBus-Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-109">Returns a description of the specified Service Bus namespace.</span></span>

## <span data-ttu-id="ae6a4-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="ae6a4-110">PARAMETERS</span></span>

### <span data-ttu-id="ae6a4-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae6a4-111">-DefaultProfile</span></span>
<span data-ttu-id="ae6a4-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae6a4-113">-Name</span><span class="sxs-lookup"><span data-stu-id="ae6a4-113">-Name</span></span>
<span data-ttu-id="ae6a4-114">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-114">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6a4-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae6a4-115">-ResourceGroupName</span></span>
<span data-ttu-id="ae6a4-116">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="ae6a4-116">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae6a4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae6a4-117">CommonParameters</span></span>
<span data-ttu-id="ae6a4-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae6a4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae6a4-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae6a4-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae6a4-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ae6a4-120">INPUTS</span></span>

### <span data-ttu-id="ae6a4-121">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ae6a4-121">-ResourceGroup</span></span>
<span data-ttu-id="ae6a4-122">System. String</span><span class="sxs-lookup"><span data-stu-id="ae6a4-122">System.String</span></span>

### <span data-ttu-id="ae6a4-123">-Namespacename</span><span class="sxs-lookup"><span data-stu-id="ae6a4-123">-NamespaceName</span></span>
 <span data-ttu-id="ae6a4-124">System. String</span><span class="sxs-lookup"><span data-stu-id="ae6a4-124">System.String</span></span>

## <span data-ttu-id="ae6a4-125">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ae6a4-125">OUTPUTS</span></span>

### <span data-ttu-id="ae6a4-126">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. ServiceBus. Models. NamespaceAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="ae6a4-126">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.NamespaceAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="ae6a4-127">Name: SB-Example1-ID:/Subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/default-ServiceBus-WestUS/Providers/Microsoft.ServiceBus/Namespaces/SB-example1 Ort: US-amerikanische SKU: Name: Standard, Kapazität: 1, Stufe: Standard ProvisioningState: erfolgreicher Status: Active CreatedAt: 1/20/2017 1:40:01 am UpdatedAt: 1/20/2017 1:40:24 am ServiceBusEndpoint: https://SB-Example1.servicebus.windows.net:443/ aktiviert: wahr</span><span class="sxs-lookup"><span data-stu-id="ae6a4-127">Name               : SB-Example1 Id                 : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1 Location           : West US Sku                : Name : Standard , Capacity : 1 , Tier : Standard ProvisioningState  : Succeeded Status             : Active CreatedAt          : 1/20/2017 1:40:01 AM UpdatedAt          : 1/20/2017 1:40:24 AM ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/ Enabled            : True</span></span>

## <span data-ttu-id="ae6a4-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="ae6a4-128">NOTES</span></span>
## <span data-ttu-id="ae6a4-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae6a4-129">RELATED LINKS</span></span>

## <span data-ttu-id="ae6a4-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ae6a4-130">RELATED LINKS</span></span>

