---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHub.md
ms.openlocfilehash: ca2afaec702e27b4c20201cbd69984ec3827ded2
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98376702"
---
# <span data-ttu-id="b7aba-101">Get-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="b7aba-101">Get-AzEventHub</span></span>

## <span data-ttu-id="b7aba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7aba-102">SYNOPSIS</span></span>
<span data-ttu-id="b7aba-103">Ruft die Details eines einzelnen Ereignishubs ab oder ruft eine Liste der Ereignishubs ab.</span><span class="sxs-lookup"><span data-stu-id="b7aba-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

## <span data-ttu-id="b7aba-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b7aba-104">SYNTAX</span></span>

```
Get-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7aba-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b7aba-105">DESCRIPTION</span></span>
<span data-ttu-id="b7aba-106">Das Get-AzEventHub-Cmdlet gibt entweder die Details eines Ereignishubs oder eine Liste aller Ereignishubs im aktuellen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="b7aba-106">The Get-AzEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="b7aba-107">Wenn der Name des Ereignishubs angegeben wird, werden die Details eines einzelnen Ereignishubs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b7aba-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="b7aba-108">Wenn kein Ereignishubname angegeben wird, wird eine Liste aller Ereignishubs im angegebenen Namespace zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b7aba-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="b7aba-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b7aba-109">EXAMPLES</span></span>

### <span data-ttu-id="b7aba-110">Beispiel 1: Angegebenes EventHub</span><span class="sxs-lookup"><span data-stu-id="b7aba-110">Example 1: specified EventHub</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="b7aba-111">Gibt die Details des \` Ereignishubs "MyEventHubName" \` zurück.</span><span class="sxs-lookup"><span data-stu-id="b7aba-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="b7aba-112">Beispiel 2: Liste von EventHub im angegebenen Namespace</span><span class="sxs-lookup"><span data-stu-id="b7aba-112">Example 2: List of EventHub in specified Namespace</span></span>
```powershell
PS C:\> Get-AzEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="b7aba-113">Gibt eine Liste der Ereignishubs im Namespace \` "MyNamespaceName" \` zurück.</span><span class="sxs-lookup"><span data-stu-id="b7aba-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="b7aba-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7aba-114">PARAMETERS</span></span>

### <span data-ttu-id="b7aba-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7aba-115">-DefaultProfile</span></span>
<span data-ttu-id="b7aba-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b7aba-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7aba-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="b7aba-117">-MaxCount</span></span>
<span data-ttu-id="b7aba-118">Ermitteln Sie die maximale Anzahl von EventHubs, die zurückgeben werden.</span><span class="sxs-lookup"><span data-stu-id="b7aba-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="b7aba-119">-Name</span><span class="sxs-lookup"><span data-stu-id="b7aba-119">-Name</span></span>
<span data-ttu-id="b7aba-120">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="b7aba-120">EventHub Name</span></span>

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

### <span data-ttu-id="b7aba-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="b7aba-121">-Namespace</span></span>
<span data-ttu-id="b7aba-122">Namespacename</span><span class="sxs-lookup"><span data-stu-id="b7aba-122">Namespace Name</span></span>

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

### <span data-ttu-id="b7aba-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7aba-123">-ResourceGroupName</span></span>
<span data-ttu-id="b7aba-124">Ressourcengruppenname</span><span class="sxs-lookup"><span data-stu-id="b7aba-124">Resource Group Name</span></span>

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

### <span data-ttu-id="b7aba-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7aba-125">CommonParameters</span></span>
<span data-ttu-id="b7aba-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7aba-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7aba-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7aba-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7aba-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b7aba-128">INPUTS</span></span>

### <span data-ttu-id="b7aba-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b7aba-129">System.String</span></span>

## <span data-ttu-id="b7aba-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b7aba-130">OUTPUTS</span></span>

### <span data-ttu-id="b7aba-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="b7aba-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="b7aba-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="b7aba-132">NOTES</span></span>

## <span data-ttu-id="b7aba-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="b7aba-133">RELATED LINKS</span></span>
