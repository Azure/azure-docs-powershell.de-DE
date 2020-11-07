---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
ms.openlocfilehash: 6ae26d1d5061989ac93756812cf48494e9101978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663148"
---
# <span data-ttu-id="a573a-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="a573a-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="a573a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a573a-102">SYNOPSIS</span></span>
<span data-ttu-id="a573a-103">Ruft die Details eines einzelnen Ereignis Hubs ab oder ruft eine Liste der Ereignis Hubs ab.</span><span class="sxs-lookup"><span data-stu-id="a573a-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a573a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a573a-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>] [-MaxCount <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a573a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a573a-105">DESCRIPTION</span></span>
<span data-ttu-id="a573a-106">Das Get-AzureRmEventHub-Cmdlet gibt entweder die Details eines Event-Hubs oder eine Liste aller Event-Hubs im aktuellen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="a573a-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="a573a-107">Wenn der Name des Ereignis Hubs bereitgestellt wird, werden die Details eines einzelnen Ereignis Hubs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a573a-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="a573a-108">Wenn kein Ereignis-Hub-Name angegeben wird, wird eine Liste aller Ereignis Hubs im angegebenen Namespace zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a573a-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="a573a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a573a-109">EXAMPLES</span></span>

### <span data-ttu-id="a573a-110">Beispiel 1: angegebene EventHub</span><span class="sxs-lookup"><span data-stu-id="a573a-110">Example 1 - specified EventHub</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="a573a-111">Gibt die Details des Ereignis-Hub \` -MyEventHubName zurück \` .</span><span class="sxs-lookup"><span data-stu-id="a573a-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="a573a-112">Beispiel 2 – Liste der EventHub im angegebenen Namespace</span><span class="sxs-lookup"><span data-stu-id="a573a-112">Example 2 - List of EventHub in specified Namespace</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="a573a-113">Gibt eine Liste von Ereignis Hubs im Namespace \` mynamespacename zurück \` .</span><span class="sxs-lookup"><span data-stu-id="a573a-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="a573a-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="a573a-114">PARAMETERS</span></span>

### <span data-ttu-id="a573a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a573a-115">-DefaultProfile</span></span>
<span data-ttu-id="a573a-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a573a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a573a-117">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="a573a-117">-MaxCount</span></span>
<span data-ttu-id="a573a-118">Ermitteln Sie die maximale Anzahl der EventHubs, die zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a573a-118">Determine the maximum number of EventHubs to return.</span></span>

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

### <span data-ttu-id="a573a-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a573a-119">-Name</span></span>
<span data-ttu-id="a573a-120">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="a573a-120">EventHub Name</span></span>

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

### <span data-ttu-id="a573a-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a573a-121">-Namespace</span></span>
<span data-ttu-id="a573a-122">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="a573a-122">Namespace Name</span></span>

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

### <span data-ttu-id="a573a-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a573a-123">-ResourceGroupName</span></span>
<span data-ttu-id="a573a-124">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="a573a-124">Resource Group Name</span></span>

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

### <span data-ttu-id="a573a-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a573a-125">CommonParameters</span></span>
<span data-ttu-id="a573a-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a573a-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a573a-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a573a-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a573a-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a573a-128">INPUTS</span></span>

### <span data-ttu-id="a573a-129">System. String</span><span class="sxs-lookup"><span data-stu-id="a573a-129">System.String</span></span>

## <span data-ttu-id="a573a-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a573a-130">OUTPUTS</span></span>

### <span data-ttu-id="a573a-131">Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="a573a-131">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="a573a-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="a573a-132">NOTES</span></span>

## <span data-ttu-id="a573a-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a573a-133">RELATED LINKS</span></span>
