---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 442a88c7fe64fd8913e86ba0ee6be013f226061e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846071"
---
# <span data-ttu-id="ec4d7-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="ec4d7-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="ec4d7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ec4d7-102">SYNOPSIS</span></span>
<span data-ttu-id="ec4d7-103">Erstellt eine neue Azure-Ereignis Raster Domäne.</span><span class="sxs-lookup"><span data-stu-id="ec4d7-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="ec4d7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ec4d7-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec4d7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ec4d7-105">DESCRIPTION</span></span>
<span data-ttu-id="ec4d7-106">Erstellt eine neue Azure-Ereignis Raster Domäne.</span><span class="sxs-lookup"><span data-stu-id="ec4d7-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="ec4d7-107">Nachdem die Domäne erstellt wurde, kann eine Anwendung Ereignisse für den Themen Endpunkt veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="ec4d7-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="ec4d7-108">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ec4d7-108">EXAMPLES</span></span>

### <span data-ttu-id="ec4d7-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ec4d7-109">Example 1</span></span>

<span data-ttu-id="ec4d7-110">Erstellt eine Ereignis Raster \` -Domänen domain1 \` im angegebenen geografischen Standort \` westus2 in der \` Ressourcengruppe \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ec4d7-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="ec4d7-111">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="ec4d7-111">Example 2</span></span>

<span data-ttu-id="ec4d7-112">Erstellt eine Ereignis Raster \` -Domänen domain1 am \` angegebenen geografischen Standort \` westus2 in der \` Ressourcengruppe \` MyResourceGroupName \` mit den angegebenen Tags "Department" und "Environment".</span><span class="sxs-lookup"><span data-stu-id="ec4d7-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Department, Finance], [Environment, Test]}
```

## <span data-ttu-id="ec4d7-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec4d7-113">PARAMETERS</span></span>

### <span data-ttu-id="ec4d7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec4d7-114">-DefaultProfile</span></span>
<span data-ttu-id="ec4d7-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ec4d7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec4d7-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="ec4d7-116">-Location</span></span>
<span data-ttu-id="ec4d7-117">Der Speicherort der Domäne.</span><span class="sxs-lookup"><span data-stu-id="ec4d7-117">The location of the domain.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec4d7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ec4d7-118">-Name</span></span>
<span data-ttu-id="ec4d7-119">EventGrid-Domänenname.</span><span class="sxs-lookup"><span data-stu-id="ec4d7-119">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec4d7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec4d7-120">-ResourceGroupName</span></span>
<span data-ttu-id="ec4d7-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ec4d7-121">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec4d7-122">-Tag</span><span class="sxs-lookup"><span data-stu-id="ec4d7-122">-Tag</span></span>
<span data-ttu-id="ec4d7-123">Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="ec4d7-123">Hashtable which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec4d7-124">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ec4d7-124">-Confirm</span></span>
<span data-ttu-id="ec4d7-125">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ec4d7-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4d7-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec4d7-126">-WhatIf</span></span>
<span data-ttu-id="ec4d7-127">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ec4d7-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec4d7-128">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ec4d7-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ec4d7-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec4d7-129">CommonParameters</span></span>
<span data-ttu-id="ec4d7-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec4d7-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec4d7-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec4d7-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec4d7-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ec4d7-132">INPUTS</span></span>

### <span data-ttu-id="ec4d7-133">System. String</span><span class="sxs-lookup"><span data-stu-id="ec4d7-133">System.String</span></span>

### <span data-ttu-id="ec4d7-134">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ec4d7-134">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ec4d7-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ec4d7-135">OUTPUTS</span></span>

### <span data-ttu-id="ec4d7-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="ec4d7-136">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="ec4d7-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="ec4d7-137">NOTES</span></span>

## <span data-ttu-id="ec4d7-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ec4d7-138">RELATED LINKS</span></span>
