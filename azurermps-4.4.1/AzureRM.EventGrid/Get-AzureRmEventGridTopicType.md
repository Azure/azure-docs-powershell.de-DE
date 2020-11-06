---
external help file: Microsoft.Azure.Commands.EventGrid.dll-Help.xml
Module Name: AzureRM.EventGrid
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventGrid/Commands.EventGrid/help/Get-AzureRmEventGridTopicType.md
ms.openlocfilehash: 621fb15d3a83b7c704e5828d6541ad9d4404875c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93501866"
---
# <span data-ttu-id="952b7-101">Get-AzureRmEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="952b7-101">Get-AzureRmEventGridTopicType</span></span>

## <span data-ttu-id="952b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="952b7-102">SYNOPSIS</span></span>
<span data-ttu-id="952b7-103">Ruft die Details zu den vom Azure-Ereignis Raster unterstützten Thementypen ab.</span><span class="sxs-lookup"><span data-stu-id="952b7-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="952b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="952b7-104">SYNTAX</span></span>

```
Get-AzureRmEventGridTopicType [[-Name] <String>] [-IncludeEventTypeData]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="952b7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="952b7-105">DESCRIPTION</span></span>
<span data-ttu-id="952b7-106">Ruft die Details der Thementypen ab, die vom Azure-Ereignis Raster unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="952b7-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="952b7-107">Wenn der Name des Thementyps angegeben wird, werden Details zu diesem Thementyp zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="952b7-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="952b7-108">Wenn der Name des Thementyps nicht angegeben ist, werden Details zu allen Thementypen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="952b7-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="952b7-109">Wenn IncludeEventTypes angegeben wird, werden Informationen zu Ereignistypen, die von den einzelnen Thementypen unterstützt werden, in der Antwort berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="952b7-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="952b7-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="952b7-110">EXAMPLES</span></span>

### <span data-ttu-id="952b7-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="952b7-111">Example 1</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType
```

<span data-ttu-id="952b7-112">Ruft eine Liste der Thementypen ab.</span><span class="sxs-lookup"><span data-stu-id="952b7-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="952b7-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="952b7-113">Example 2</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="952b7-114">Ruft Informationen zum StorageAccounts-Thementyp ab.</span><span class="sxs-lookup"><span data-stu-id="952b7-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="952b7-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="952b7-115">Example 3</span></span>
```
PS C:\> Get-AzureRmEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="952b7-116">Ruft Informationen zum StorageAccounts-Thementyp ab, einschließlich der Ereignistypen, die von StorageAccounts unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="952b7-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="952b7-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="952b7-117">PARAMETERS</span></span>

### <span data-ttu-id="952b7-118">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="952b7-118">-IncludeEventTypeData</span></span>
<span data-ttu-id="952b7-119">Wenn angegeben, enthält die Antwort die Ereignistypen, die von einem Thementyp unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="952b7-119">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="952b7-120">-Name</span><span class="sxs-lookup"><span data-stu-id="952b7-120">-Name</span></span>
<span data-ttu-id="952b7-121">EventGrid Topic Type Name.</span><span class="sxs-lookup"><span data-stu-id="952b7-121">EventGrid Topic Type Name.</span></span>

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

### <span data-ttu-id="952b7-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="952b7-122">-DefaultProfile</span></span>
<span data-ttu-id="952b7-123">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="952b7-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="952b7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="952b7-124">CommonParameters</span></span>
<span data-ttu-id="952b7-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="952b7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="952b7-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="952b7-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="952b7-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="952b7-127">INPUTS</span></span>

### <span data-ttu-id="952b7-128">System. String</span><span class="sxs-lookup"><span data-stu-id="952b7-128">System.String</span></span>
<span data-ttu-id="952b7-129">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="952b7-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="952b7-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="952b7-130">OUTPUTS</span></span>

### <span data-ttu-id="952b7-131">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfoListInstance, Microsoft. Azure. Commands. EventGrid, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="952b7-131">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance, Microsoft.Azure.Commands.EventGrid, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="952b7-132">Microsoft. Azure. Commands. EventGrid. Models. PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="952b7-132">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="952b7-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="952b7-133">NOTES</span></span>

## <span data-ttu-id="952b7-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="952b7-134">RELATED LINKS</span></span>

