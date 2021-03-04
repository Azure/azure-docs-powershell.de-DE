---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: 7fa9cb54a6790a473be419dd934927ed26783d11
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101921219"
---
# <span data-ttu-id="d314f-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="d314f-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="d314f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d314f-102">SYNOPSIS</span></span>
<span data-ttu-id="d314f-103">Ruft die Details eines Event Hubs NetworkruleSet des Namespaces im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="d314f-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="d314f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d314f-104">SYNTAX</span></span>

### <span data-ttu-id="d314f-105">NetworkRuleSetPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="d314f-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d314f-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="d314f-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d314f-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d314f-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d314f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d314f-108">DESCRIPTION</span></span>
<span data-ttu-id="d314f-109">Ruft die Details eines Event Hubs NetworkruleSet des Namespaces im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="d314f-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="d314f-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d314f-110">EXAMPLES</span></span>

### <span data-ttu-id="d314f-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d314f-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="d314f-112">Hier erhalten Sie die Details zu Event Hubs NetworkruleSet des Namespaces mithilfe von ResourceGroup- und Namespaceparametern.</span><span class="sxs-lookup"><span data-stu-id="d314f-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="d314f-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d314f-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="d314f-114">Hier erhalten Sie die Details zu Event Hubs NetworkruleSet von Namespace mit Namespace, der sich im aktuellen Abonnement befindet.</span><span class="sxs-lookup"><span data-stu-id="d314f-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="d314f-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="d314f-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="d314f-116">Details zu Event Hubs NetworkruleSet of namespace using Resource ID of other Namespace</span><span class="sxs-lookup"><span data-stu-id="d314f-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="d314f-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d314f-117">PARAMETERS</span></span>

### <span data-ttu-id="d314f-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d314f-118">-DefaultProfile</span></span>
<span data-ttu-id="d314f-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d314f-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d314f-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="d314f-120">-Namespace</span></span>
<span data-ttu-id="d314f-121">Namespacename</span><span class="sxs-lookup"><span data-stu-id="d314f-121">Namespace Name</span></span>

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

### <span data-ttu-id="d314f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d314f-122">-ResourceGroupName</span></span>
<span data-ttu-id="d314f-123">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="d314f-123">Resource Group Name</span></span>

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

### <span data-ttu-id="d314f-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d314f-124">-ResourceId</span></span>
<span data-ttu-id="d314f-125">Namespaceressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="d314f-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="d314f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d314f-126">CommonParameters</span></span>
<span data-ttu-id="d314f-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d314f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="d314f-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d314f-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d314f-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d314f-129">INPUTS</span></span>

### <span data-ttu-id="d314f-130">System.String</span><span class="sxs-lookup"><span data-stu-id="d314f-130">System.String</span></span>

## <span data-ttu-id="d314f-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d314f-131">OUTPUTS</span></span>

### <span data-ttu-id="d314f-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="d314f-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="d314f-133">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d314f-133">NOTES</span></span>

## <span data-ttu-id="d314f-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d314f-134">RELATED LINKS</span></span>