---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/get-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHub.md
ms.openlocfilehash: e87300af80c38fa0f7989836c992fd1baa53ba6d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93482954"
---
# <span data-ttu-id="5e18b-101">Get-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="5e18b-101">Get-AzureRmEventHub</span></span>

## <span data-ttu-id="5e18b-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e18b-102">SYNOPSIS</span></span>
<span data-ttu-id="5e18b-103">Ruft die Details eines einzelnen Ereignis Hubs ab oder ruft eine Liste der Ereignis Hubs ab.</span><span class="sxs-lookup"><span data-stu-id="5e18b-103">Gets the details of a single Event Hub, or gets a list of Event Hubs.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5e18b-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e18b-104">SYNTAX</span></span>

```
Get-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e18b-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e18b-105">DESCRIPTION</span></span>
<span data-ttu-id="5e18b-106">Das Get-AzureRmEventHub-Cmdlet gibt entweder die Details eines Event-Hubs oder eine Liste aller Event-Hubs im aktuellen Namespace zurück.</span><span class="sxs-lookup"><span data-stu-id="5e18b-106">The Get-AzureRmEventHub cmdlet returns either the details of an Event Hub, or a list of all Event Hubs in the current namespace.</span></span>
<span data-ttu-id="5e18b-107">Wenn der Name des Ereignis Hubs bereitgestellt wird, werden die Details eines einzelnen Ereignis Hubs zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5e18b-107">If the Event Hub name is provided, the details of a single Event Hub are returned.</span></span>
<span data-ttu-id="5e18b-108">Wenn kein Ereignis-Hub-Name angegeben wird, wird eine Liste aller Ereignis Hubs im angegebenen Namespace zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="5e18b-108">If an Event Hub name is not provided, a list of all Event Hubs in the specified namespace is returned.</span></span>

## <span data-ttu-id="5e18b-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e18b-109">EXAMPLES</span></span>

### <span data-ttu-id="5e18b-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5e18b-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="5e18b-111">Gibt die Details des Ereignis-Hub \` -MyEventHubName zurück \` .</span><span class="sxs-lookup"><span data-stu-id="5e18b-111">Returns the details of the Event Hub \`MyEventHubName\`.</span></span>

### <span data-ttu-id="5e18b-112">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="5e18b-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHub -ResourceGroup MyResourceGroupName -NamespaceName MyNamespaceName
```

<span data-ttu-id="5e18b-113">Gibt eine Liste von Ereignis Hubs im Namespace \` mynamespacename zurück \` .</span><span class="sxs-lookup"><span data-stu-id="5e18b-113">Returns a list of Event Hubs in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="5e18b-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e18b-114">PARAMETERS</span></span>

### <span data-ttu-id="5e18b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e18b-115">-DefaultProfile</span></span>
<span data-ttu-id="5e18b-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e18b-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e18b-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5e18b-117">-Name</span></span>
<span data-ttu-id="5e18b-118">EventHub Name</span><span class="sxs-lookup"><span data-stu-id="5e18b-118">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e18b-119">-Namespace</span><span class="sxs-lookup"><span data-stu-id="5e18b-119">-Namespace</span></span>
<span data-ttu-id="5e18b-120">Namespace Name</span><span class="sxs-lookup"><span data-stu-id="5e18b-120">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e18b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e18b-121">-ResourceGroupName</span></span>
<span data-ttu-id="5e18b-122">Ressourcengruppen Name</span><span class="sxs-lookup"><span data-stu-id="5e18b-122">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e18b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e18b-123">CommonParameters</span></span>
<span data-ttu-id="5e18b-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e18b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5e18b-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e18b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e18b-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e18b-126">INPUTS</span></span>

### <span data-ttu-id="5e18b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="5e18b-127">System.String</span></span>


## <span data-ttu-id="5e18b-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e18b-128">OUTPUTS</span></span>

### <span data-ttu-id="5e18b-129">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventHub. Models. PSEventHubAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.5.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="5e18b-129">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes, Microsoft.Azure.Commands.EventHub, Version=0.5.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>


## <span data-ttu-id="5e18b-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e18b-130">NOTES</span></span>

## <span data-ttu-id="5e18b-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e18b-131">RELATED LINKS</span></span>
