---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: f4899d55919f8b3c08b36babc448f1594f4ac4c8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003941"
---
# <span data-ttu-id="3d18f-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="3d18f-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="3d18f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3d18f-102">SYNOPSIS</span></span>
<span data-ttu-id="3d18f-103">Erstellt eine neue Regel für ein bestimmtes Abonnement des Themas.</span><span class="sxs-lookup"><span data-stu-id="3d18f-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="3d18f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3d18f-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3d18f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3d18f-105">DESCRIPTION</span></span>
<span data-ttu-id="3d18f-106">Das Cmdlet " **Get-AzServiceBusRule** " Ruft die Beschreibung der angegebenen Regel im angegebenen Abonnement des Themas ab.</span><span class="sxs-lookup"><span data-stu-id="3d18f-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="3d18f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3d18f-107">EXAMPLES</span></span>

### <span data-ttu-id="3d18f-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3d18f-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="3d18f-109">Gibt die angegebene Regelbeschreibung für ein angegebenes Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="3d18f-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="3d18f-110">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3d18f-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="3d18f-111">Gibt eine Liste der Regelbeschreibungen für ein angegebenes Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="3d18f-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="3d18f-112">Standardmäßig wird die 100-Regel zurückgegeben, wenn mehr als 100-Regel zurückgegeben werden soll, verwenden Sie bitte-MaxCount-Parameter.</span><span class="sxs-lookup"><span data-stu-id="3d18f-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="3d18f-113">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="3d18f-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="3d18f-114">Gibt eine Liste der ersten 150-Regelbeschreibungen für ein angegebenes Abonnement zurück.</span><span class="sxs-lookup"><span data-stu-id="3d18f-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="3d18f-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="3d18f-115">PARAMETERS</span></span>

### <span data-ttu-id="3d18f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d18f-116">-DefaultProfile</span></span>
<span data-ttu-id="3d18f-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3d18f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d18f-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="3d18f-118">-MaxCount</span></span>
<span data-ttu-id="3d18f-119">Ermitteln Sie die maximale Anzahl von Regeln, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="3d18f-119">Determine the maximum number of Rules to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d18f-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3d18f-120">-Name</span></span>
<span data-ttu-id="3d18f-121">Regelname</span><span class="sxs-lookup"><span data-stu-id="3d18f-121">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d18f-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="3d18f-122">-Namespace</span></span>
<span data-ttu-id="3d18f-123">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="3d18f-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d18f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d18f-124">-ResourceGroupName</span></span>
<span data-ttu-id="3d18f-125">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="3d18f-125">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d18f-126">-Abonnement</span><span class="sxs-lookup"><span data-stu-id="3d18f-126">-Subscription</span></span>
<span data-ttu-id="3d18f-127">Name des Abonnements</span><span class="sxs-lookup"><span data-stu-id="3d18f-127">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3d18f-128">-Topic</span><span class="sxs-lookup"><span data-stu-id="3d18f-128">-Topic</span></span>
<span data-ttu-id="3d18f-129">Name des Themas</span><span class="sxs-lookup"><span data-stu-id="3d18f-129">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3d18f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d18f-130">CommonParameters</span></span>
<span data-ttu-id="3d18f-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d18f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d18f-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d18f-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d18f-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3d18f-133">INPUTS</span></span>

### <span data-ttu-id="3d18f-134">System. String</span><span class="sxs-lookup"><span data-stu-id="3d18f-134">System.String</span></span>

## <span data-ttu-id="3d18f-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3d18f-135">OUTPUTS</span></span>

### <span data-ttu-id="3d18f-136">Microsoft. Azure. Commands. ServiceBus. Models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="3d18f-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="3d18f-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="3d18f-137">NOTES</span></span>

## <span data-ttu-id="3d18f-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3d18f-138">RELATED LINKS</span></span>
