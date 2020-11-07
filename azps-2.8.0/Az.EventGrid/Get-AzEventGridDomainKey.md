---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/get-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Get-AzEventGridDomainKey.md
ms.openlocfilehash: 4d72be4f7ddbe6cd5884269c724c7505cc05fffc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651242"
---
# <span data-ttu-id="bec4c-101">Get-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="bec4c-101">Get-AzEventGridDomainKey</span></span>

## <span data-ttu-id="bec4c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bec4c-102">SYNOPSIS</span></span>
<span data-ttu-id="bec4c-103">Ruft die freigegebenen Zugriffstasten ab, die zum Veröffentlichen von Ereignissen in einer Ereignis Raster Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bec4c-103">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="bec4c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bec4c-104">SYNTAX</span></span>

### <span data-ttu-id="bec4c-105">DomainNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bec4c-105">DomainNameParameterSet (Default)</span></span>
```
Get-AzEventGridDomainKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bec4c-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bec4c-106">DomainInputObjectParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainObject] <PSDomain> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="bec4c-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="bec4c-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
Get-AzEventGridDomainKey [-DomainResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bec4c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bec4c-108">DESCRIPTION</span></span>
<span data-ttu-id="bec4c-109">Ruft die freigegebenen Zugriffstasten ab, die zum Veröffentlichen von Ereignissen in einer Ereignis Raster Domäne verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bec4c-109">Gets the shared access keys used to publish events to an Event Grid domain.</span></span>

## <span data-ttu-id="bec4c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bec4c-110">EXAMPLES</span></span>

### <span data-ttu-id="bec4c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="bec4c-111">Example 1</span></span>

<span data-ttu-id="bec4c-112">Ruft die freigegebenen Zugriffstasten des Ereignis Rasters \` domain1 \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="bec4c-112">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -Name Domain1

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

### <span data-ttu-id="bec4c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="bec4c-113">Example 2</span></span>

<span data-ttu-id="bec4c-114">Ruft die freigegebenen Zugriffstasten des Ereignis Rasters \` domain1 \` in der Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="bec4c-114">Gets the shared access keys of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | Get-AzEventGridDomainKey

Key1                                         Key2
----                                         ----
<Key1 value>                                <Key 2 value>
```

## <span data-ttu-id="bec4c-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="bec4c-115">PARAMETERS</span></span>

### <span data-ttu-id="bec4c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bec4c-116">-DefaultProfile</span></span>
<span data-ttu-id="bec4c-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="bec4c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bec4c-118">-Domainobject</span><span class="sxs-lookup"><span data-stu-id="bec4c-118">-DomainObject</span></span>
<span data-ttu-id="bec4c-119">EventGrid-Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="bec4c-119">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="bec4c-120">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="bec4c-120">-DomainResourceId</span></span>
<span data-ttu-id="bec4c-121">Der Ressourcenbezeichner, der die Ereignis Raster Domäne darstellt.</span><span class="sxs-lookup"><span data-stu-id="bec4c-121">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="bec4c-122">-Name</span><span class="sxs-lookup"><span data-stu-id="bec4c-122">-Name</span></span>
<span data-ttu-id="bec4c-123">EventGrid-Domänenname.</span><span class="sxs-lookup"><span data-stu-id="bec4c-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec4c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bec4c-124">-ResourceGroupName</span></span>
<span data-ttu-id="bec4c-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="bec4c-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bec4c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bec4c-126">CommonParameters</span></span>
<span data-ttu-id="bec4c-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bec4c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bec4c-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bec4c-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bec4c-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bec4c-129">INPUTS</span></span>

### <span data-ttu-id="bec4c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="bec4c-130">System.String</span></span>

### <span data-ttu-id="bec4c-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="bec4c-131">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="bec4c-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bec4c-132">OUTPUTS</span></span>

### <span data-ttu-id="bec4c-133">Microsoft. Azure. Management. EventGrid. Models. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="bec4c-133">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="bec4c-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="bec4c-134">NOTES</span></span>

## <span data-ttu-id="bec4c-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bec4c-135">RELATED LINKS</span></span>
