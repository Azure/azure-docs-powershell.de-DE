---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
ms.openlocfilehash: 6afb01ef46ba4f9c627f20a1c49ab58c2a79f252
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98292522"
---
# <span data-ttu-id="12e4c-101">New-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="12e4c-101">New-AzEventGridDomainKey</span></span>

## <span data-ttu-id="12e4c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12e4c-102">SYNOPSIS</span></span>
<span data-ttu-id="12e4c-103">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid Domain erneut.</span><span class="sxs-lookup"><span data-stu-id="12e4c-103">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="12e4c-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="12e4c-104">SYNTAX</span></span>

### <span data-ttu-id="12e4c-105">DomainNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="12e4c-105">DomainNameParameterSet (Default)</span></span>
```
New-AzEventGridDomainKey [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12e4c-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="12e4c-106">DomainInputObjectParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainInputObject] <PSDomain>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12e4c-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="12e4c-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="12e4c-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="12e4c-108">DESCRIPTION</span></span>
<span data-ttu-id="12e4c-109">Generiert den freigegebenen Zugriffsschlüssel für eine Azure Event Grid Domain erneut.</span><span class="sxs-lookup"><span data-stu-id="12e4c-109">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="12e4c-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="12e4c-110">EXAMPLES</span></span>

### <span data-ttu-id="12e4c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="12e4c-111">Example 1</span></span>

<span data-ttu-id="12e4c-112">Erstellen Sie den Schlüssel erneut, der \' "key1'\" der "Event Grid \` domain1" \` in der Ressourcengruppe \` "MyResourceGroupName" \` entspricht.</span><span class="sxs-lookup"><span data-stu-id="12e4c-112">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -DomainName Domain1 -Name key1

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="12e4c-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="12e4c-113">Example 2</span></span>

<span data-ttu-id="12e4c-114">Erstellen Sie den Schlüssel erneut, der \' "key1'\" der "Event Grid \` domain1" \` in der Ressourcengruppe \` "MyResourceGroupName" \` entspricht.</span><span class="sxs-lookup"><span data-stu-id="12e4c-114">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | New-AzEventGridTopicKey -KeyName "key1"

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="12e4c-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="12e4c-115">Example 3</span></span>

<span data-ttu-id="12e4c-116">Erstellen Sie den Schlüssel erneut, der \' "key2'\" der "Event Grid domain1" in der Ressourcengruppe \` \` \` "MyResourceGroupName" entspricht, und verwenden Sie dabei die \` vollständige Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="12e4c-116">Regenerate the key corresponding to key \'key2'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using its full resource Id.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceId /subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1 -KeyName Key2

Key1                                         Key2
----                                         ----
<Old Value for Key1>                        <New Value for Key2>
```

## <span data-ttu-id="12e4c-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="12e4c-117">PARAMETERS</span></span>

### <span data-ttu-id="12e4c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12e4c-118">-DefaultProfile</span></span>
<span data-ttu-id="12e4c-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="12e4c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="12e4c-120">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="12e4c-120">-DomainInputObject</span></span>
<span data-ttu-id="12e4c-121">EventGrid Domain-Objekt.</span><span class="sxs-lookup"><span data-stu-id="12e4c-121">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="12e4c-122">-DomainName</span><span class="sxs-lookup"><span data-stu-id="12e4c-122">-DomainName</span></span>
<span data-ttu-id="12e4c-123">"EventGrid"-Domänenname.</span><span class="sxs-lookup"><span data-stu-id="12e4c-123">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: DomainNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12e4c-124">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="12e4c-124">-DomainResourceId</span></span>
<span data-ttu-id="12e4c-125">Ressourcenbezeichner, der die "Event Grid Domain" darstellt.</span><span class="sxs-lookup"><span data-stu-id="12e4c-125">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="12e4c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="12e4c-126">-Name</span></span>
<span data-ttu-id="12e4c-127">Der Name des Schlüssels, der erneut generiert werden muss</span><span class="sxs-lookup"><span data-stu-id="12e4c-127">The name of the key that needs to be regenerated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: KeyName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12e4c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12e4c-128">-ResourceGroupName</span></span>
<span data-ttu-id="12e4c-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="12e4c-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="12e4c-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="12e4c-130">-Confirm</span></span>
<span data-ttu-id="12e4c-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="12e4c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12e4c-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="12e4c-132">-WhatIf</span></span>
<span data-ttu-id="12e4c-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="12e4c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="12e4c-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="12e4c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12e4c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12e4c-135">CommonParameters</span></span>
<span data-ttu-id="12e4c-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12e4c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12e4c-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12e4c-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12e4c-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="12e4c-138">INPUTS</span></span>

### <span data-ttu-id="12e4c-139">System.String</span><span class="sxs-lookup"><span data-stu-id="12e4c-139">System.String</span></span>

### <span data-ttu-id="12e4c-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="12e4c-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="12e4c-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="12e4c-141">OUTPUTS</span></span>

### <span data-ttu-id="12e4c-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="12e4c-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="12e4c-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="12e4c-143">NOTES</span></span>

## <span data-ttu-id="12e4c-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="12e4c-144">RELATED LINKS</span></span>
