---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgridtopictype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridTopicType.md
ms.openlocfilehash: e2cd8cfeadf0c9574cbf39a642133109aa02ec39
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100161649"
---
# <span data-ttu-id="fa90b-101">Get-AzEventGridTopicType</span><span class="sxs-lookup"><span data-stu-id="fa90b-101">Get-AzEventGridTopicType</span></span>

## <span data-ttu-id="fa90b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa90b-102">SYNOPSIS</span></span>
<span data-ttu-id="fa90b-103">Ruft die Details zu den Thementypen ab, die von Azure Event Grid unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="fa90b-103">Gets the details about the topic types supported by Azure Event Grid.</span></span>

## <span data-ttu-id="fa90b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fa90b-104">SYNTAX</span></span>

```
Get-AzEventGridTopicType [-Name <String>] [-IncludeEventTypeData] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fa90b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fa90b-105">DESCRIPTION</span></span>
<span data-ttu-id="fa90b-106">Ruft die Details der Thementypen ab, die von Azure Event Grid unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="fa90b-106">Gets the details of topic types supported by Azure Event Grid.</span></span>
<span data-ttu-id="fa90b-107">Wenn ein Thementypname angegeben wird, werden Details zu diesem Thementyp zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fa90b-107">If a topic type name is specified, details about that topic type are returned.</span></span>
<span data-ttu-id="fa90b-108">Wenn kein Thementypname angegeben wird, werden Details zu allen Thementypen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="fa90b-108">If a topic type name is not specified, details about all topic types are returned.</span></span>
<span data-ttu-id="fa90b-109">Wenn IncludeEventTypes angegeben wird, werden Informationen zu den Ereignistypen, die von den einzelnen Thementypen unterstützt werden, in die Antwort eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="fa90b-109">If IncludeEventTypes is specified, information about event types supported by each topic type is included in the response.</span></span>

## <span data-ttu-id="fa90b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fa90b-110">EXAMPLES</span></span>

### <span data-ttu-id="fa90b-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fa90b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType
```

<span data-ttu-id="fa90b-112">Ruft eine Liste der Thementypen ab.</span><span class="sxs-lookup"><span data-stu-id="fa90b-112">Gets a list of the topic types.</span></span>

### <span data-ttu-id="fa90b-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="fa90b-113">Example 2</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts"
```

<span data-ttu-id="fa90b-114">Ruft Informationen zum Thematyp "StorageAccounts" ab.</span><span class="sxs-lookup"><span data-stu-id="fa90b-114">Gets information about the StorageAccounts topic type.</span></span>

### <span data-ttu-id="fa90b-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="fa90b-115">Example 3</span></span>
```powershell
PS C:\> Get-AzEventGridTopicType -Name "Microsoft.Storage.StorageAccounts" -IncludeEventTypeData
```

<span data-ttu-id="fa90b-116">Ruft Informationen zum Thematyp "StorageAccounts" ab, einschließlich der Ereignistypen, die von StorageAccounts unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="fa90b-116">Gets information about the StorageAccounts topic type, including the event types supported by StorageAccounts.</span></span>

## <span data-ttu-id="fa90b-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa90b-117">PARAMETERS</span></span>

### <span data-ttu-id="fa90b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa90b-118">-DefaultProfile</span></span>
<span data-ttu-id="fa90b-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fa90b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa90b-120">-IncludeEventTypeData</span><span class="sxs-lookup"><span data-stu-id="fa90b-120">-IncludeEventTypeData</span></span>
<span data-ttu-id="fa90b-121">Falls angegeben, enthält die Antwort die Ereignistypen, die von einem Thementyp unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="fa90b-121">If specified, the response will include the event types supported by a topic type.</span></span>

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

### <span data-ttu-id="fa90b-122">-Name</span><span class="sxs-lookup"><span data-stu-id="fa90b-122">-Name</span></span>
<span data-ttu-id="fa90b-123">Name des EventGrid-Thematyps.</span><span class="sxs-lookup"><span data-stu-id="fa90b-123">EventGrid Topic Type Name.</span></span>

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

### <span data-ttu-id="fa90b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa90b-124">CommonParameters</span></span>
<span data-ttu-id="fa90b-125">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa90b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa90b-126">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa90b-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa90b-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fa90b-127">INPUTS</span></span>

### <span data-ttu-id="fa90b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="fa90b-128">System.String</span></span>

## <span data-ttu-id="fa90b-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fa90b-129">OUTPUTS</span></span>

### <span data-ttu-id="fa90b-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span><span class="sxs-lookup"><span data-stu-id="fa90b-130">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfoListInstance</span></span>

### <span data-ttu-id="fa90b-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span><span class="sxs-lookup"><span data-stu-id="fa90b-131">Microsoft.Azure.Commands.EventGrid.Models.PSTopicTypeInfo</span></span>

## <span data-ttu-id="fa90b-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fa90b-132">NOTES</span></span>

## <span data-ttu-id="fa90b-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fa90b-133">RELATED LINKS</span></span>
