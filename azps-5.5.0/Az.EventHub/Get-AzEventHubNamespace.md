---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNamespace.md
ms.openlocfilehash: ba2209f7b58951bdc52976fb3cbab10fa15da98a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147921"
---
# <span data-ttu-id="500bd-101">Get-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="500bd-101">Get-AzEventHubNamespace</span></span>

## <span data-ttu-id="500bd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="500bd-102">SYNOPSIS</span></span>
<span data-ttu-id="500bd-103">Ruft die Details eines Event Hubs-Namespaces ab, oder ruft eine Liste aller Ereignishubs-Namespaces im aktuellen Abonnement von Azure ab.</span><span class="sxs-lookup"><span data-stu-id="500bd-103">Gets the details of an Event Hubs namespace, or gets a list of all Event Hubs namespaces in the current Azure subscription.</span></span>

## <span data-ttu-id="500bd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="500bd-104">SYNTAX</span></span>

```
Get-AzEventHubNamespace [[-ResourceGroupName] <String>] [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="500bd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="500bd-105">DESCRIPTION</span></span>
<span data-ttu-id="500bd-106">Das Get-AzEventHubNamespace-Cmdlet ruft entweder die Details eines angegebenen Ereignishubs-Namespaces oder eine Liste aller Ereignishubs-Namespaces im aktuellen Abonnement von Azure ab.</span><span class="sxs-lookup"><span data-stu-id="500bd-106">The Get-AzEventHubNamespace cmdlet gets either the details of a specified Event Hubs namespace, or a list of all Event Hubs namespaces in the current Azure subscription.</span></span>
<span data-ttu-id="500bd-107">Wenn der Namespacename angegeben wird, werden die Details eines einzelnen Ereignishubs-Namespaces zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="500bd-107">If the namespace name is provided, the details of a single Event Hubs namespace is returned.</span></span>
<span data-ttu-id="500bd-108">Wenn der Namespacename nicht angegeben wird, wird eine Liste mit Namespaces zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="500bd-108">If the namespace name is not provided, a list of namespaces is returned.</span></span>

## <span data-ttu-id="500bd-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="500bd-109">EXAMPLES</span></span>

### <span data-ttu-id="500bd-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="500bd-110">Example 1</span></span>
```
PS C:\> Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="500bd-111">Ruft die Details des \` Namespaces "MyNamespaceName" \` in der Ressourcengruppe \` "MyResourceGroupName" \` ab.</span><span class="sxs-lookup"><span data-stu-id="500bd-111">Gets the details of namespace \`MyNamespaceName\` in the resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="500bd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="500bd-112">PARAMETERS</span></span>

### <span data-ttu-id="500bd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="500bd-113">-DefaultProfile</span></span>
<span data-ttu-id="500bd-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="500bd-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="500bd-115">-Name</span><span class="sxs-lookup"><span data-stu-id="500bd-115">-Name</span></span>
<span data-ttu-id="500bd-116">EventHub Namespacename</span><span class="sxs-lookup"><span data-stu-id="500bd-116">EventHub Namespace Name</span></span>

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

### <span data-ttu-id="500bd-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="500bd-117">-ResourceGroupName</span></span>
<span data-ttu-id="500bd-118">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="500bd-118">Resource Group Name</span></span>

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

### <span data-ttu-id="500bd-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="500bd-119">CommonParameters</span></span>
<span data-ttu-id="500bd-120">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="500bd-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="500bd-121">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="500bd-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="500bd-122">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="500bd-122">INPUTS</span></span>

### <span data-ttu-id="500bd-123">System.String</span><span class="sxs-lookup"><span data-stu-id="500bd-123">System.String</span></span>

## <span data-ttu-id="500bd-124">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="500bd-124">OUTPUTS</span></span>

### <span data-ttu-id="500bd-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="500bd-125">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="500bd-126">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="500bd-126">NOTES</span></span>

## <span data-ttu-id="500bd-127">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="500bd-127">RELATED LINKS</span></span>
