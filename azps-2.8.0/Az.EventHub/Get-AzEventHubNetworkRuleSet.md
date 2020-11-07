---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubnetworkruleset
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubNetworkRuleSet.md
ms.openlocfilehash: cbac380f317025154f25c3c4dfe449832c864741
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651191"
---
# <span data-ttu-id="49d01-101">Get-AzEventHubNetworkRuleSet</span><span class="sxs-lookup"><span data-stu-id="49d01-101">Get-AzEventHubNetworkRuleSet</span></span>

## <span data-ttu-id="49d01-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="49d01-102">SYNOPSIS</span></span>
<span data-ttu-id="49d01-103">Ruft die Details eines Ereignis Hubs NetworkruleSet des Namespaces im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="49d01-103">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="49d01-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="49d01-104">SYNTAX</span></span>

### <span data-ttu-id="49d01-105">NetworkRuleSetPropertiesSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="49d01-105">NetworkRuleSetPropertiesSet (Default)</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceGroupName] <String> [-Namespace] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49d01-106">NetworkRuleSetNamespacePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="49d01-106">NetworkRuleSetNamespacePropertiesSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-Namespace] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49d01-107">NetworkRuleSetResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="49d01-107">NetworkRuleSetResourceIdParameterSet</span></span>
```
Get-AzEventHubNetworkRuleSet [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="49d01-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="49d01-108">DESCRIPTION</span></span>
<span data-ttu-id="49d01-109">Ruft die Details eines Ereignis Hubs NetworkruleSet des Namespaces im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="49d01-109">Gets the details of an Event Hubs NetworkruleSet of namespace in the current Azure subscription.</span></span>

## <span data-ttu-id="49d01-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="49d01-110">EXAMPLES</span></span>

### <span data-ttu-id="49d01-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="49d01-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceGroupName  v-ajnavtest -Namespace Eventhub-Namespace1-1375
```

<span data-ttu-id="49d01-112">Abrufen der Details von Ereignis Hubs NetworkruleSet des Namespaces mithilfe von ResourceGroup-und Namespace-Parametern</span><span class="sxs-lookup"><span data-stu-id="49d01-112">Get the details of Event Hubs NetworkruleSet of namespace using ResourceGroup and Namespace parameters.</span></span> 

### <span data-ttu-id="49d01-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="49d01-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -Namespace Eventhub-Namespace1-2389
```

<span data-ttu-id="49d01-114">Rufen Sie die Details der Ereignis Hubs NetworkruleSet des Namespaces mit Namespace ab, der im aktuellen Abonnement enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="49d01-114">Get the details of Event Hubs NetworkruleSet of namespace using  Namespace which is in the current subscription.</span></span>

### <span data-ttu-id="49d01-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="49d01-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventHubNetworkRuleSet -ResourceId /SubscriptionId/resourcegroups/ResourceGroup/providers/Microsoft.EventHub/namespaces/Eventhub-Namespace1-2389
```

<span data-ttu-id="49d01-116">Abrufen der Details von Ereignis Hubs NetworkruleSet des Namespaces mithilfe der Ressourcen-ID eines anderen Namespaces</span><span class="sxs-lookup"><span data-stu-id="49d01-116">Get the details of Event Hubs NetworkruleSet of namespace using Resource Id of other Namespace</span></span> 

## <span data-ttu-id="49d01-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="49d01-117">PARAMETERS</span></span>

### <span data-ttu-id="49d01-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49d01-118">-DefaultProfile</span></span>
<span data-ttu-id="49d01-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="49d01-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="49d01-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="49d01-120">-Namespace</span></span>
<span data-ttu-id="49d01-121">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="49d01-121">Namespace Name</span></span>

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

### <span data-ttu-id="49d01-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="49d01-122">-ResourceGroupName</span></span>
<span data-ttu-id="49d01-123">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="49d01-123">Resource Group Name</span></span>

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

### <span data-ttu-id="49d01-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="49d01-124">-ResourceId</span></span>
<span data-ttu-id="49d01-125">Namespace-Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="49d01-125">Namespace Resource Id</span></span>

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

### <span data-ttu-id="49d01-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49d01-126">CommonParameters</span></span>
<span data-ttu-id="49d01-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49d01-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="49d01-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="49d01-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49d01-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="49d01-129">INPUTS</span></span>

### <span data-ttu-id="49d01-130">System. String</span><span class="sxs-lookup"><span data-stu-id="49d01-130">System.String</span></span>

## <span data-ttu-id="49d01-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="49d01-131">OUTPUTS</span></span>

### <span data-ttu-id="49d01-132">Microsoft. Azure. Commands. EventHub. Models. PSNetworkRuleSetAttributes</span><span class="sxs-lookup"><span data-stu-id="49d01-132">Microsoft.Azure.Commands.EventHub.Models.PSNetworkRuleSetAttributes</span></span>

## <span data-ttu-id="49d01-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="49d01-133">NOTES</span></span>

## <span data-ttu-id="49d01-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="49d01-134">RELATED LINKS</span></span>