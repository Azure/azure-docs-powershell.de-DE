---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusNamespace.md
ms.openlocfilehash: 37d142947c09c211c947f3bd80455a812f96844f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482049"
---
# <span data-ttu-id="de34b-101">Get-AzureRmServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="de34b-101">Get-AzureRmServiceBusNamespace</span></span>

## <span data-ttu-id="de34b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="de34b-102">SYNOPSIS</span></span>
<span data-ttu-id="de34b-103">Ruft eine Beschreibung für den angegebenen ServiceBus-Namespace innerhalb der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="de34b-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="de34b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="de34b-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="de34b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="de34b-105">DESCRIPTION</span></span>
<span data-ttu-id="de34b-106">Das Cmdlet " **Get-AzureRmServiceBusNamespace** " Ruft eine Beschreibung für den angegebenen ServiceBus-Namespace innerhalb der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="de34b-106">The **Get-AzureRmServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="de34b-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="de34b-107">EXAMPLES</span></span>

### <span data-ttu-id="de34b-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="de34b-108">Example 1</span></span>

```
PS C:\> Get-AzureRmServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroup      : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

## <span data-ttu-id="de34b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="de34b-109">PARAMETERS</span></span>

### <span data-ttu-id="de34b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de34b-110">-DefaultProfile</span></span>
<span data-ttu-id="de34b-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="de34b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="de34b-112">-Name</span><span class="sxs-lookup"><span data-stu-id="de34b-112">-Name</span></span>
<span data-ttu-id="de34b-113">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="de34b-113">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de34b-114">-ResourceGroupName</span></span>
<span data-ttu-id="de34b-115">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="de34b-115">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="de34b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de34b-116">CommonParameters</span></span>
<span data-ttu-id="de34b-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de34b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de34b-118">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de34b-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de34b-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="de34b-119">INPUTS</span></span>

### <span data-ttu-id="de34b-120">System. String</span><span class="sxs-lookup"><span data-stu-id="de34b-120">System.String</span></span>

## <span data-ttu-id="de34b-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="de34b-121">OUTPUTS</span></span>

### <span data-ttu-id="de34b-122">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="de34b-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="de34b-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="de34b-123">NOTES</span></span>

## <span data-ttu-id="de34b-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="de34b-124">RELATED LINKS</span></span>
