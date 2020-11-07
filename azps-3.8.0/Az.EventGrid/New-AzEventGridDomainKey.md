---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomainkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomainKey.md
ms.openlocfilehash: fe86115ec5b82570a8498db10efeb7b7b24dd9c4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93846064"
---
# <span data-ttu-id="267c3-101">New-AzEventGridDomainKey</span><span class="sxs-lookup"><span data-stu-id="267c3-101">New-AzEventGridDomainKey</span></span>

## <span data-ttu-id="267c3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="267c3-102">SYNOPSIS</span></span>
<span data-ttu-id="267c3-103">Generiert die freigegebene Zugriffstaste für eine Azure-Ereignis Raster Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="267c3-103">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="267c3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="267c3-104">SYNTAX</span></span>

### <span data-ttu-id="267c3-105">DomainNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="267c3-105">DomainNameParameterSet (Default)</span></span>
```
New-AzEventGridDomainKey [-ResourceGroupName] <String> [-DomainName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="267c3-106">DomainInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="267c3-106">DomainInputObjectParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainInputObject] <PSDomain>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="267c3-107">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="267c3-107">ResourceIdEventSubscriptionParameterSet</span></span>
```
New-AzEventGridDomainKey [-Name] <String> [-DomainResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="267c3-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="267c3-108">DESCRIPTION</span></span>
<span data-ttu-id="267c3-109">Generiert die freigegebene Zugriffstaste für eine Azure-Ereignis Raster Domäne erneut.</span><span class="sxs-lookup"><span data-stu-id="267c3-109">Regenerates the shared access key for an Azure Event Grid Domain.</span></span>

## <span data-ttu-id="267c3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="267c3-110">EXAMPLES</span></span>

### <span data-ttu-id="267c3-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="267c3-111">Example 1</span></span>

<span data-ttu-id="267c3-112">Regenerieren Sie den Schlüssel, der dem Schlüssel \' key1 ' \ of Event Grid Domain \` domain1 \` in der Ressourcengruppe \` MyResourceGroupName entspricht \` .</span><span class="sxs-lookup"><span data-stu-id="267c3-112">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceGroup MyResourceGroupName -DomainName Domain1 -Name key1

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="267c3-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="267c3-113">Example 2</span></span>

<span data-ttu-id="267c3-114">Regenerieren Sie den Schlüssel, der dem Schlüssel \' key1 ' \ of Event Grid Domain \` domain1 \` in der Ressourcengruppe \` MyResourceGroupName entspricht \` .</span><span class="sxs-lookup"><span data-stu-id="267c3-114">Regenerate the key corresponding to key \'key1'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> Get-AzEventGridDomain -ResourceGroup MyResourceGroupName -Name Domain1 | New-AzEventGridTopicKey -KeyName "key1"

Key1                                         Key2
----                                         ----
<New Value for Key1>                        <Old Value for Key2>
```

### <span data-ttu-id="267c3-115">Beispiel 3</span><span class="sxs-lookup"><span data-stu-id="267c3-115">Example 3</span></span>

<span data-ttu-id="267c3-116">Regenerieren Sie den Schlüssel, der dem Schlüssel \' key2 ' \ of Event Grid Domain \` domain1 \` in der Ressourcengruppe \` MyResourceGroupName \` unter Verwendung der vollständigen Ressourcen-ID entspricht.</span><span class="sxs-lookup"><span data-stu-id="267c3-116">Regenerate the key corresponding to key \'key2'\ of Event Grid domain \`Domain1\` in resource group \`MyResourceGroupName\` using its full resource Id.</span></span>

```powershell
PS C:\> New-AzEventGridDomainKey -ResourceId /subscriptions/$subscriptionId/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/Domain1 -KeyName Key2

Key1                                         Key2
----                                         ----
<Old Value for Key1>                        <New Value for Key2>
```

## <span data-ttu-id="267c3-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="267c3-117">PARAMETERS</span></span>

### <span data-ttu-id="267c3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="267c3-118">-DefaultProfile</span></span>
<span data-ttu-id="267c3-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="267c3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="267c3-120">-DomainInputObject</span><span class="sxs-lookup"><span data-stu-id="267c3-120">-DomainInputObject</span></span>
<span data-ttu-id="267c3-121">EventGrid-Domänenobjekt.</span><span class="sxs-lookup"><span data-stu-id="267c3-121">EventGrid Domain object.</span></span>

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

### <span data-ttu-id="267c3-122">-Domänenname</span><span class="sxs-lookup"><span data-stu-id="267c3-122">-DomainName</span></span>
<span data-ttu-id="267c3-123">EventGrid-Domänenname.</span><span class="sxs-lookup"><span data-stu-id="267c3-123">EventGrid domain name.</span></span>

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

### <span data-ttu-id="267c3-124">-DomainResourceId</span><span class="sxs-lookup"><span data-stu-id="267c3-124">-DomainResourceId</span></span>
<span data-ttu-id="267c3-125">Der Ressourcenbezeichner, der die Ereignis Raster Domäne darstellt.</span><span class="sxs-lookup"><span data-stu-id="267c3-125">Resource Identifier representing the Event Grid Domain.</span></span>

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

### <span data-ttu-id="267c3-126">-Name</span><span class="sxs-lookup"><span data-stu-id="267c3-126">-Name</span></span>
<span data-ttu-id="267c3-127">Der Name des Schlüssels, der neu generiert werden muss</span><span class="sxs-lookup"><span data-stu-id="267c3-127">The name of the key that needs to be regenerated</span></span>

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

### <span data-ttu-id="267c3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="267c3-128">-ResourceGroupName</span></span>
<span data-ttu-id="267c3-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="267c3-129">The name of the resource group.</span></span>

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

### <span data-ttu-id="267c3-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="267c3-130">-Confirm</span></span>
<span data-ttu-id="267c3-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="267c3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="267c3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="267c3-132">-WhatIf</span></span>
<span data-ttu-id="267c3-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="267c3-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="267c3-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="267c3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="267c3-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="267c3-135">CommonParameters</span></span>
<span data-ttu-id="267c3-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="267c3-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="267c3-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="267c3-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="267c3-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="267c3-138">INPUTS</span></span>

### <span data-ttu-id="267c3-139">System. String</span><span class="sxs-lookup"><span data-stu-id="267c3-139">System.String</span></span>

### <span data-ttu-id="267c3-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="267c3-140">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="267c3-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="267c3-141">OUTPUTS</span></span>

### <span data-ttu-id="267c3-142">Microsoft. Azure. Management. EventGrid. Models. DomainSharedAccessKeys</span><span class="sxs-lookup"><span data-stu-id="267c3-142">Microsoft.Azure.Management.EventGrid.Models.DomainSharedAccessKeys</span></span>

## <span data-ttu-id="267c3-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="267c3-143">NOTES</span></span>

## <span data-ttu-id="267c3-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="267c3-144">RELATED LINKS</span></span>
