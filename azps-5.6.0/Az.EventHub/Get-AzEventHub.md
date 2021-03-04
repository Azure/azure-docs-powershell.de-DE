---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: d69e30ff993d2e07c7711d36d8e5ec889bc0f7c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101946568"
---
# <span data-ttu-id="f5051-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="f5051-101">Get-AzEventHub</span></span>

## <span data-ttu-id="f5051-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5051-102">SYNOPSIS</span></span>
<span data-ttu-id="f5051-103">Ruft die Details eines einzelnen Ereignishubs ab oder ruft eine Liste der Ereignishubs ab.</span><span class="sxs-lookup"><span data-stu-id="f5051-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="f5051-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f5051-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5051-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5051-105">DESCRIPTION</span></span>
<span data-ttu-id="f5051-106">Das Get-AzEventHub-Cmdlet gibt entweder die Details eines Ereignishubs oder eine Liste aller Ereignishubs im aktuellen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="f5051-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="f5051-107">Wenn der Name des Ereignishubs angegeben wird, werden die Details eines einzelnen Ereignishubs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f5051-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="f5051-108">Wenn kein Ereignishubname angegeben wird, wird eine Liste aller Ereignishubs im angegebenen Namespace zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f5051-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="f5051-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f5051-109">EXAMPLES</span></span>

### <span data-ttu-id="f5051-110">Beispiel 1: angegebenes EventHub</span><span class="sxs-lookup"><span data-stu-id="f5051-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="f5051-111">Gibt die Details des \` Ereignishubs MyEventHubName \` zurück.</span><span class="sxs-lookup"><span data-stu-id="f5051-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="f5051-112">Beispiel 2: Liste von EventHub im angegebenen Namespace</span><span class="sxs-lookup"><span data-stu-id="f5051-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="f5051-113">Gibt eine Liste der Ereignishubs im Namespace \` MyNamespaceName \` zurück.</span><span class="sxs-lookup"><span data-stu-id="f5051-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="f5051-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f5051-114">PARAMETERS</span></span>

### <span data-ttu-id="f5051-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5051-115">-DefaultProfile</span></span>
<span data-ttu-id="f5051-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f5051-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5051-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="f5051-117">-MaxCount</span></span>
<span data-ttu-id="f5051-118">Bestimmen Sie die maximale Anzahl von Zurücksennungsereignishubs.</span><span class="sxs-lookup"><span data-stu-id="f5051-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="f5051-119">-Name</span><span class="sxs-lookup"><span data-stu-id="f5051-119">-Name</span></span>
<span data-ttu-id="f5051-120">EventHub-Name</span><span class="sxs-lookup"><span data-stu-id="f5051-120">EventHub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5051-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f5051-121">-Namespace</span></span>
<span data-ttu-id="f5051-122">Namespacename</span><span class="sxs-lookup"><span data-stu-id="f5051-122">Namespace Name</span></span>

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

### <span data-ttu-id="f5051-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5051-123">-ResourceGroupName</span></span>
<span data-ttu-id="f5051-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="f5051-124">Resource Group Name</span></span>

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

### <span data-ttu-id="f5051-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5051-125">CommonParameters</span></span>
<span data-ttu-id="f5051-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5051-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5051-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5051-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5051-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f5051-128">INPUTS</span></span>

### <span data-ttu-id="f5051-129">System.String</span><span class="sxs-lookup"><span data-stu-id="f5051-129">System.String</span></span>

## <span data-ttu-id="f5051-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f5051-130">OUTPUTS</span></span>

### <span data-ttu-id="f5051-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="f5051-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="f5051-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f5051-132">NOTES</span></span>

## <span data-ttu-id="f5051-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f5051-133">RELATED LINKS</span></span>
