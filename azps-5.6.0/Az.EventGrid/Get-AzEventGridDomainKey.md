---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: a211e3857cd81a5dd057795fb9e2956d60cbae17
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101934971"
---
# <span data-ttu-id="f3609-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="f3609-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="f3609-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3609-102">SYNOPSIS</span></span>
<span data-ttu-id="f3609-103">Ruft die freigegebenen Zugriffstasten ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3609-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="f3609-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f3609-104">SYNTAX</span></span>

### <span data-ttu-id="f3609-105">DomainNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f3609-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3609-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3609-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f3609-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3609-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3609-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f3609-108">DESCRIPTION</span></span>
<span data-ttu-id="f3609-109">Ruft die freigegebenen Zugriffstasten ab, die zum Veröffentlichen von Ereignissen in einer Event Grid-Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3609-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="f3609-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f3609-110">EXAMPLES</span></span>

### <span data-ttu-id="f3609-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f3609-111">Example 1</span></span>

<span data-ttu-id="f3609-112">Ruft die freigegebenen Zugriffstasten der Ereignisrasterdomäne \` Domäne1 \` in der Ressourcengruppe \` MyResourceGroupName \` ab.</span><span class="sxs-lookup"><span data-stu-id="f3609-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="f3609-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f3609-113">Example 2</span></span>

<span data-ttu-id="f3609-114">Ruft die freigegebenen Zugriffstasten der Ereignisrasterdomäne \` Domäne1 \` in der Ressourcengruppe \` MyResourceGroupName \` ab.</span><span class="sxs-lookup"><span data-stu-id="f3609-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="f3609-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f3609-115">PARAMETERS</span></span>

### <span data-ttu-id="f3609-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3609-116">-DefaultProfile</span></span>
<span data-ttu-id="f3609-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3609-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3609-118">-DomainObject</span><span class="sxs-lookup"><span data-stu-id="f3609-118">-DomainObject</span></span>
<span data-ttu-id="f3609-119">EventGrid Domain-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f3609-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="f3609-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="f3609-120">-DomainResourceId</span></span>
<span data-ttu-id="f3609-121">Ressourcenbezeichner, der die Ereignisrasterdomäne darstellt.</span><span class="sxs-lookup"><span data-stu-id="f3609-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="f3609-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f3609-122">-Name</span></span>
<span data-ttu-id="f3609-123">Name der EventGrid-Domäne.</span><span class="sxs-lookup"><span data-stu-id="f3609-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="f3609-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3609-124">-ResourceGroupName</span></span>
<span data-ttu-id="f3609-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f3609-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="f3609-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3609-126">CommonParameters</span></span>
<span data-ttu-id="f3609-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3609-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3609-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f3609-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3609-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f3609-129">INPUTS</span></span>

### <span data-ttu-id="f3609-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f3609-130">System.String</span></span>

### <span data-ttu-id="f3609-131">Microsoft.Azure.Commands.EventGrid.Models.PSDOmain</span><span class="sxs-lookup"><span data-stu-id="f3609-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="f3609-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f3609-132">OUTPUTS</span></span>

### <span data-ttu-id="f3609-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="f3609-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="f3609-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f3609-134">NOTES</span></span>

## <span data-ttu-id="f3609-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f3609-135">RELATED LINKS</span></span>
