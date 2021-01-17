---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 6e38f98f9dd3ebfaa2ad4747016556aecd9998e9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472698"
---
# <span data-ttu-id="1c38e-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="1c38e-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="1c38e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1c38e-102">SYNOPSIS</span></span>
<span data-ttu-id="1c38e-103">Abonnieren Sie den Ereignistrigger für Externe Dienstereignisse.</span><span class="sxs-lookup"><span data-stu-id="1c38e-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="1c38e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1c38e-104">SYNTAX</span></span>

### <span data-ttu-id="1c38e-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1c38e-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1c38e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="1c38e-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1c38e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1c38e-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c38e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c38e-108">DESCRIPTION</span></span>
<span data-ttu-id="1c38e-109">Dieser Befehl abonniert den Ereignistrigger für die angegebenen Ereignisse des externen Diensts aus der Triggerdefinierung.</span><span class="sxs-lookup"><span data-stu-id="1c38e-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="1c38e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1c38e-110">EXAMPLES</span></span>

### <span data-ttu-id="1c38e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1c38e-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="1c38e-112">Dieser Befehl abonniert den BlobEnetTrigger1-Trigger für die angegebenen Ereignisse der Triggerdefinierung.</span><span class="sxs-lookup"><span data-stu-id="1c38e-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="1c38e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1c38e-113">PARAMETERS</span></span>

### <span data-ttu-id="1c38e-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="1c38e-114">-DataFactoryName</span></span>
<span data-ttu-id="1c38e-115">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="1c38e-115">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c38e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c38e-116">-DefaultProfile</span></span>
<span data-ttu-id="1c38e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1c38e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c38e-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1c38e-118">-InputObject</span></span>
<span data-ttu-id="1c38e-119">Das Triggerobjekt.</span><span class="sxs-lookup"><span data-stu-id="1c38e-119">The trigger object.</span></span>

```yaml
Type: PSTrigger
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1c38e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="1c38e-120">-Name</span></span>
<span data-ttu-id="1c38e-121">Der Auslösername.</span><span class="sxs-lookup"><span data-stu-id="1c38e-121">The trigger name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c38e-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c38e-122">-ResourceGroupName</span></span>
<span data-ttu-id="1c38e-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1c38e-123">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByFactoryName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c38e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1c38e-124">-ResourceId</span></span>
<span data-ttu-id="1c38e-125">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="1c38e-125">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1c38e-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1c38e-126">-Confirm</span></span>
<span data-ttu-id="1c38e-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c38e-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c38e-128">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="1c38e-128">-WhatIf</span></span>
<span data-ttu-id="1c38e-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1c38e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c38e-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1c38e-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1c38e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c38e-131">CommonParameters</span></span>
<span data-ttu-id="1c38e-132">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c38e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c38e-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1c38e-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c38e-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1c38e-134">INPUTS</span></span>

### <span data-ttu-id="1c38e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="1c38e-135">System.String</span></span>
<span data-ttu-id="1c38e-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="1c38e-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="1c38e-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1c38e-137">OUTPUTS</span></span>

### <span data-ttu-id="1c38e-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="1c38e-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="1c38e-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="1c38e-139">NOTES</span></span>

## <span data-ttu-id="1c38e-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="1c38e-140">RELATED LINKS</span></span>

