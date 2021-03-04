---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: 3a715e0c4c2540a0905035afabc15ef46caa32bc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938760"
---
# <span data-ttu-id="f0c09-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="f0c09-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="f0c09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0c09-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c09-103">Ruft die Details zu den Thementypen ab, die von Azure Event Grid unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f0c09-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="f0c09-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f0c09-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f0c09-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f0c09-105">DESCRIPTION</span></span>
<span data-ttu-id="f0c09-106">Ruft die Details der von Azure Event Grid unterstützten Thementypen ab.</span><span class="sxs-lookup"><span data-stu-id="f0c09-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="f0c09-107">Wenn ein Thementypname angegeben wird, werden Details zu diesem Thementyp zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f0c09-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="f0c09-108">Wenn kein Thementypname angegeben wird, werden Details zu allen Thementypen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f0c09-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="f0c09-109">Wenn IncludeEventTypes angegeben wird, werden Informationen zu Ereignistypen, die von jedem Thementyp unterstützt werden, in die Antwort einbezogen.</span><span class="sxs-lookup"><span data-stu-id="f0c09-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="f0c09-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f0c09-110">EXAMPLES</span></span>

### <span data-ttu-id="f0c09-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f0c09-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="f0c09-112">Ruft eine Liste der Thementypen ab.</span><span class="sxs-lookup"><span data-stu-id="f0c09-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="f0c09-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f0c09-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="f0c09-114">Ruft Informationen zum Thematyp StorageAccounts ab.</span><span class="sxs-lookup"><span data-stu-id="f0c09-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="f0c09-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="f0c09-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="f0c09-116">Ruft Informationen zum Thematyp StorageAccounts ab, einschließlich der von StorageAccounts unterstützten Ereignistypen.</span><span class="sxs-lookup"><span data-stu-id="f0c09-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="f0c09-117">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f0c09-117">PARAMETERS</span></span>

### <span data-ttu-id="f0c09-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c09-118">-DefaultProfile</span></span>
<span data-ttu-id="f0c09-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f0c09-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f0c09-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="f0c09-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="f0c09-121">Wenn angegeben, enthält die Antwort die Ereignistypen, die von einem Thementyp unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f0c09-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="f0c09-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f0c09-122">-Name</span></span>
<span data-ttu-id="f0c09-123">Name des EventGrid-Thementyps.</span><span class="sxs-lookup"><span data-stu-id="f0c09-123">EventGrid Topic Type Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0c09-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c09-124">CommonParameters</span></span>
<span data-ttu-id="f0c09-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0c09-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c09-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0c09-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c09-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f0c09-127">INPUTS</span></span>

### <span data-ttu-id="f0c09-128">System.String</span><span class="sxs-lookup"><span data-stu-id="f0c09-128">System.String</span></span>

## <span data-ttu-id="f0c09-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f0c09-129">OUTPUTS</span></span>

### <span data-ttu-id="f0c09-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="f0c09-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="f0c09-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="f0c09-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="f0c09-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f0c09-132">NOTES</span></span>

## <span data-ttu-id="f0c09-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f0c09-133">RELATED LINKS</span></span>
