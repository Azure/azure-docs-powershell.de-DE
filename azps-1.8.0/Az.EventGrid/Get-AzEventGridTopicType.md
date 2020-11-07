---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: 950ac2da0d69a11a29d39059f267e9273b783499
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661078"
---
# <span data-ttu-id="7006a-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="7006a-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="7006a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7006a-102">SYNOPSIS</span></span>
<span data-ttu-id="7006a-103">Ruft die Details zu den vom Azure-Ereignis Raster unterstützten Thementypen ab.</span><span class="sxs-lookup"><span data-stu-id="7006a-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="7006a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7006a-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7006a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7006a-105">DESCRIPTION</span></span>
<span data-ttu-id="7006a-106">Ruft die Details der Thementypen ab, die vom Azure-Ereignis Raster unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7006a-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="7006a-107">Wenn der Name des Thementyps angegeben wird, werden Details zu diesem Thementyp zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7006a-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="7006a-108">Wenn der Name des Thementyps nicht angegeben ist, werden Details zu allen Thementypen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7006a-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="7006a-109">Wenn IncludeEventTypes angegeben wird, werden Informationen zu Ereignistypen, die von den einzelnen Thementypen unterstützt werden, in der Antwort berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="7006a-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="7006a-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7006a-110">EXAMPLES</span></span>

### <span data-ttu-id="7006a-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7006a-111">Example 1</span></span>
```
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="7006a-112">Ruft eine Liste der Thementypen ab.</span><span class="sxs-lookup"><span data-stu-id="7006a-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="7006a-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="7006a-113">Example 2</span></span>
```
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="7006a-114">Ruft Informationen zum StorageAccounts-Thementyp ab.</span><span class="sxs-lookup"><span data-stu-id="7006a-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="7006a-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="7006a-115">Example 3</span></span>
```
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="7006a-116">Ruft Informationen zum StorageAccounts-Thementyp ab, einschließlich der Ereignistypen, die von StorageAccounts unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7006a-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="7006a-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="7006a-117">PARAMETERS</span></span>

### <span data-ttu-id="7006a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7006a-118">-DefaultProfile</span></span>
<span data-ttu-id="7006a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7006a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7006a-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="7006a-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="7006a-121">Wenn angegeben, enthält die Antwort die Ereignistypen, die von einem Thementyp unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7006a-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="7006a-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7006a-122">-Name</span></span>
<span data-ttu-id="7006a-123">EventGrid Topic Type Name.</span><span class="sxs-lookup"><span data-stu-id="7006a-123">EventGrid Topic Type Name.</span></span>

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

### <span data-ttu-id="7006a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7006a-124">CommonParameters</span></span>
<span data-ttu-id="7006a-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7006a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7006a-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7006a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7006a-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7006a-127">INPUTS</span></span>

### <span data-ttu-id="7006a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="7006a-128">System.String</span></span>

## <span data-ttu-id="7006a-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7006a-129">OUTPUTS</span></span>

### <span data-ttu-id="7006a-130">Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="7006a-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="7006a-131">Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="7006a-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="7006a-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="7006a-132">NOTES</span></span>

## <span data-ttu-id="7006a-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7006a-133">RELATED LINKS</span></span>
