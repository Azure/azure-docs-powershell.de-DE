---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusNamespace.md
ms.openlocfilehash: 359ff0ce6de0c017d1ea2a65adc1d4573e45c17f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176753"
---
# <span data-ttu-id="81d4a-101">Get-AzServiceBusNamespace</span><span class="sxs-lookup"><span data-stu-id="81d4a-101">Get-AzServiceBusNamespace</span></span>

## <span data-ttu-id="81d4a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81d4a-102">SYNOPSIS</span></span>
<span data-ttu-id="81d4a-103">Ruft eine Beschreibung für den angegebenen ServiceBus-Namespace innerhalb der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="81d4a-103">Gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="81d4a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81d4a-104">SYNTAX</span></span>

```
Get-AzServiceBusNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="81d4a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81d4a-105">DESCRIPTION</span></span>
<span data-ttu-id="81d4a-106">Das Cmdlet " **Get-AzServiceBusNamespace** " Ruft eine Beschreibung für den angegebenen ServiceBus-Namespace innerhalb der Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="81d4a-106">The **Get-AzServiceBusNamespace** cmdlet gets a description for the specified Service Bus namespace within the resource group.</span></span>

## <span data-ttu-id="81d4a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81d4a-107">EXAMPLES</span></span>

### <span data-ttu-id="81d4a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="81d4a-108">Example 1</span></span>

```
PS C:\> Get-AzServiceBusNamespace -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1

Name               : SB-Example1
Id                 : /subscriptions/{subscription id}/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1
ResourceGroupName  : Default-ServiceBus-WestUS
Location           : West US
Tags               : {TesttingTags, TestingTagValue, TestTag, TestTagValue}
Sku                : Name : Premium , Tier : Premium
ProvisioningState  : Succeeded
CreatedAt          : 1/20/2017 1:40:01 AM
UpdatedAt          : 1/20/2017 1:40:24 AM
ServiceBusEndpoint : https://SB-Example1.servicebus.windows.net:443/
```

## <span data-ttu-id="81d4a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="81d4a-109">PARAMETERS</span></span>

### <span data-ttu-id="81d4a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81d4a-110">-DefaultProfile</span></span>
<span data-ttu-id="81d4a-111">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="81d4a-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="81d4a-112">-Name</span><span class="sxs-lookup"><span data-stu-id="81d4a-112">-Name</span></span>
<span data-ttu-id="81d4a-113">Namespace Name.</span><span class="sxs-lookup"><span data-stu-id="81d4a-113">Namespace Name.</span></span>

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

### <span data-ttu-id="81d4a-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="81d4a-114">-ResourceGroupName</span></span>
<span data-ttu-id="81d4a-115">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="81d4a-115">The name of the resource group</span></span>

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

### <span data-ttu-id="81d4a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81d4a-116">CommonParameters</span></span>
<span data-ttu-id="81d4a-117">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81d4a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81d4a-118">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81d4a-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81d4a-119">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81d4a-119">INPUTS</span></span>

### <span data-ttu-id="81d4a-120">System. String</span><span class="sxs-lookup"><span data-stu-id="81d4a-120">System.String</span></span>

## <span data-ttu-id="81d4a-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81d4a-121">OUTPUTS</span></span>

### <span data-ttu-id="81d4a-122">Microsoft. Azure. Commands. ServiceBus. Models. PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="81d4a-122">Microsoft.Azure.Commands.ServiceBus.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="81d4a-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="81d4a-123">NOTES</span></span>

## <span data-ttu-id="81d4a-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81d4a-124">RELATED LINKS</span></span>
