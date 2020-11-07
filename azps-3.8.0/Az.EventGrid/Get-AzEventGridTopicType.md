---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: 23392f77c9315cee2bf8b1b8369febbc2281c6ff
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846080"
---
# <span data-ttu-id="a66f6-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="a66f6-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="a66f6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a66f6-102">SYNOPSIS</span></span>
<span data-ttu-id="a66f6-103">Ruft die Details zu den vom Azure-Ereignis Raster unterstützten Thementypen ab.</span><span class="sxs-lookup"><span data-stu-id="a66f6-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="a66f6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a66f6-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a66f6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a66f6-105">DESCRIPTION</span></span>
<span data-ttu-id="a66f6-106">Ruft die Details der Thementypen ab, die vom Azure-Ereignis Raster unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a66f6-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="a66f6-107">Wenn der Name des Thementyps angegeben wird, werden Details zu diesem Thementyp zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a66f6-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="a66f6-108">Wenn der Name des Thementyps nicht angegeben ist, werden Details zu allen Thementypen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a66f6-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="a66f6-109">Wenn IncludeEventTypes angegeben wird, werden Informationen zu Ereignistypen, die von den einzelnen Thementypen unterstützt werden, in der Antwort berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="a66f6-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="a66f6-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a66f6-110">EXAMPLES</span></span>

### <span data-ttu-id="a66f6-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a66f6-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="a66f6-112">Ruft eine Liste der Thementypen ab.</span><span class="sxs-lookup"><span data-stu-id="a66f6-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="a66f6-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a66f6-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="a66f6-114">Ruft Informationen zum StorageAccounts-Thementyp ab.</span><span class="sxs-lookup"><span data-stu-id="a66f6-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="a66f6-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="a66f6-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="a66f6-116">Ruft Informationen zum StorageAccounts-Thementyp ab, einschließlich der Ereignistypen, die von StorageAccounts unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a66f6-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="a66f6-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="a66f6-117">PARAMETERS</span></span>

### <span data-ttu-id="a66f6-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a66f6-118">-DefaultProfile</span></span>
<span data-ttu-id="a66f6-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a66f6-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a66f6-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="a66f6-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="a66f6-121">Wenn angegeben, enthält die Antwort die Ereignistypen, die von einem Thementyp unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="a66f6-121">If specified, the response will include the event types supported by a topic type.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a66f6-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a66f6-122">-Name</span></span>
<span data-ttu-id="a66f6-123">EventGrid Topic Type Name.</span><span class="sxs-lookup"><span data-stu-id="a66f6-123">EventGrid Topic Type Name.</span></span>

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

### <span data-ttu-id="a66f6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a66f6-124">CommonParameters</span></span>
<span data-ttu-id="a66f6-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a66f6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a66f6-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a66f6-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a66f6-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a66f6-127">INPUTS</span></span>

### <span data-ttu-id="a66f6-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a66f6-128">System.String</span></span>

## <span data-ttu-id="a66f6-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a66f6-129">OUTPUTS</span></span>

### <span data-ttu-id="a66f6-130">Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="a66f6-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="a66f6-131">Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="a66f6-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="a66f6-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="a66f6-132">NOTES</span></span>

## <span data-ttu-id="a66f6-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a66f6-133">RELATED LINKS</span></span>
