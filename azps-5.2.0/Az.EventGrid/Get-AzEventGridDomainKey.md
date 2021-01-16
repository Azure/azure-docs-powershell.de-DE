---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: c080a5132d5ed31828fbf7a35385432d3c91a923
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302296"
---
# <span data-ttu-id="ba8a8-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="ba8a8-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="ba8a8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba8a8-102">SYNOPSIS</span></span>
<span data-ttu-id="ba8a8-103">Ruft die freigegebenen Zugriffstasten ab, die zum Veröffentlichen von Ereignissen in einer Ereignisrasterdomäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba8a8-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="ba8a8-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ba8a8-104">SYNTAX</span></span>

### <span data-ttu-id="ba8a8-105">DomainNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="ba8a8-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ba8a8-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba8a8-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ba8a8-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="ba8a8-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ba8a8-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ba8a8-108">DESCRIPTION</span></span>
<span data-ttu-id="ba8a8-109">Ruft die freigegebenen Zugriffstasten ab, die zum Veröffentlichen von Ereignissen in einer Ereignisrasterdomäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba8a8-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="ba8a8-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ba8a8-110">EXAMPLES</span></span>

### <span data-ttu-id="ba8a8-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ba8a8-111">Example 1</span></span>

<span data-ttu-id="ba8a8-112">Ruft die freigegebenen Zugriffstasten der Ereignisrasterdomäne \` "Domäne1" \` in der Ressourcengruppe \` "MyResourceGroupName" \` ab.</span><span class="sxs-lookup"><span data-stu-id="ba8a8-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="ba8a8-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ba8a8-113">Example 2</span></span>

<span data-ttu-id="ba8a8-114">Ruft die freigegebenen Zugriffstasten der Ereignisrasterdomäne \` "Domäne1" \` in der Ressourcengruppe \` "MyResourceGroupName" \` ab.</span><span class="sxs-lookup"><span data-stu-id="ba8a8-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="ba8a8-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba8a8-115">PARAMETERS</span></span>

### <span data-ttu-id="ba8a8-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba8a8-116">-DefaultProfile</span></span>
<span data-ttu-id="ba8a8-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ba8a8-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba8a8-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="ba8a8-118">-DomainObject</span></span>
<span data-ttu-id="ba8a8-119">EventGrid Domain-Objekt.</span><span class="sxs-lookup"><span data-stu-id="ba8a8-119">EventGrid Domain object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSDomain
Parameter Sets: DomainInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8a8-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="ba8a8-120">-DomainResourceId</span></span>
<span data-ttu-id="ba8a8-121">Ressourcenbezeichner, der die "Event Grid Domain" darstellt.</span><span class="sxs-lookup"><span data-stu-id="ba8a8-121">Resource Identifier representing the Event Grid Domain.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8a8-122">-Name</span><span class="sxs-lookup"><span data-stu-id="ba8a8-122">-Name</span></span>
<span data-ttu-id="ba8a8-123">Name der EventGrid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="ba8a8-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8a8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ba8a8-124">-ResourceGroupName</span></span>
<span data-ttu-id="ba8a8-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ba8a8-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ba8a8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba8a8-126">CommonParameters</span></span>
<span data-ttu-id="ba8a8-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba8a8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba8a8-128">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba8a8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba8a8-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ba8a8-129">INPUTS</span></span>

### <span data-ttu-id="ba8a8-130">System.String</span><span class="sxs-lookup"><span data-stu-id="ba8a8-130">System.String</span></span>

### <span data-ttu-id="ba8a8-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="ba8a8-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="ba8a8-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ba8a8-132">OUTPUTS</span></span>

### <span data-ttu-id="ba8a8-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="ba8a8-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="ba8a8-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ba8a8-134">NOTES</span></span>

## <span data-ttu-id="ba8a8-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ba8a8-135">RELATED LINKS</span></span>
