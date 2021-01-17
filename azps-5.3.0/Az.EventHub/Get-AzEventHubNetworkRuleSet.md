---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 773f21c189833bf8dd9817d224b83eaf29dd644e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98469863"
---
# <span data-ttu-id="ffe02-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="ffe02-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="ffe02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffe02-102">SYNOPSIS</span></span>
<span data-ttu-id="ffe02-103">Ruft die Details eines "Event Hubs NetworkruleSet"-Namespaces im aktuellen Abonnement von Azure ab.</span><span class="sxs-lookup"><span data-stu-id="ffe02-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="ffe02-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ffe02-104">SYNTAX</span></span>

### <span data-ttu-id="ffe02-105">NetworkRuleSetPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ffe02-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ffe02-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="ffe02-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ffe02-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ffe02-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ffe02-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ffe02-108">DESCRIPTION</span></span>
<span data-ttu-id="ffe02-109">Ruft die Details eines "Event Hubs NetworkruleSet"-Namespaces im aktuellen Abonnement von Azure ab.</span><span class="sxs-lookup"><span data-stu-id="ffe02-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="ffe02-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ffe02-110">EXAMPLES</span></span>

### <span data-ttu-id="ffe02-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ffe02-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="ffe02-112">Hier erhalten Sie die Details zu "Event Hubs NetworkruleSet" für den Namespace mithilfe von ResourceGroup- und Namespaceparametern.</span><span class="sxs-lookup"><span data-stu-id="ffe02-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="ffe02-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ffe02-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="ffe02-114">Erfahren Sie mehr über das Event Hubs NetworkruleSet des Namespace mit dem Namespace, der im aktuellen Abonnement enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ffe02-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="ffe02-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="ffe02-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="ffe02-116">Details zum Event Hubs NetworkruleSet des Namespace mithilfe der Ressourcen-ID eines anderen Namespaces</span><span class="sxs-lookup"><span data-stu-id="ffe02-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="ffe02-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffe02-117">PARAMETERS</span></span>

### <span data-ttu-id="ffe02-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffe02-118">-DefaultProfile</span></span>
<span data-ttu-id="ffe02-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ffe02-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffe02-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ffe02-120">-Namespace</span></span>
<span data-ttu-id="ffe02-121">Namespacename</span><span class="sxs-lookup"><span data-stu-id="ffe02-121">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet, NetworkRuleSetNamespacePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe02-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffe02-122">-ResourceGroupName</span></span>
<span data-ttu-id="ffe02-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="ffe02-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetPropertiesSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetNamespacePropertiesSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ffe02-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ffe02-124">-ResourceId</span></span>
<span data-ttu-id="ffe02-125">Namespaceressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="ffe02-125">Namespace Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: NetworkRuleSetResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ffe02-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffe02-126">CommonParameters</span></span>
<span data-ttu-id="ffe02-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ffe02-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ffe02-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ffe02-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffe02-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ffe02-129">INPUTS</span></span>

### <span data-ttu-id="ffe02-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ffe02-130">System.String</span></span>

## <span data-ttu-id="ffe02-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ffe02-131">OUTPUTS</span></span>

### <span data-ttu-id="ffe02-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="ffe02-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="ffe02-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ffe02-133">NOTES</span></span>

## <span data-ttu-id="ffe02-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ffe02-134">RELATED LINKS</span></span>