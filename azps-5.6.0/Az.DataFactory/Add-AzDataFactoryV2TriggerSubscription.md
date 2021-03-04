---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: c74eb60e698cff0d95a4361235c9282f1405dce0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939619"
---
# <span data-ttu-id="ac076-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="ac076-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="ac076-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac076-102">SYNOPSIS</span></span>
<span data-ttu-id="ac076-103">Abonnieren Sie den Ereignistrigger für externe Dienstereignisse.</span><span class="sxs-lookup"><span data-stu-id="ac076-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="ac076-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ac076-104">SYNTAX</span></span>

### <span data-ttu-id="ac076-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ac076-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ac076-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ac076-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ac076-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ac076-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ac076-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ac076-108">DESCRIPTION</span></span>
<span data-ttu-id="ac076-109">Dieser Befehl abonniert den Ereignistrigger für die angegebenen externen Dienstereignisse aus der Triggerdefintion.</span><span class="sxs-lookup"><span data-stu-id="ac076-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="ac076-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ac076-110">EXAMPLES</span></span>

### <span data-ttu-id="ac076-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="ac076-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="ac076-112">Dieser Befehl abonniert blobEnetTrigger1-Trigger für die angegebenen Ereignisse aus der Triggerdefintion.</span><span class="sxs-lookup"><span data-stu-id="ac076-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="ac076-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="ac076-113">PARAMETERS</span></span>

### <span data-ttu-id="ac076-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="ac076-114">-DataFactoryName</span></span>
<span data-ttu-id="ac076-115">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="ac076-115">The data factory name.</span></span>

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

### <span data-ttu-id="ac076-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac076-116">-DefaultProfile</span></span>
<span data-ttu-id="ac076-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ac076-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ac076-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ac076-118">-InputObject</span></span>
<span data-ttu-id="ac076-119">Das Triggerobjekt.</span><span class="sxs-lookup"><span data-stu-id="ac076-119">The trigger object.</span></span>

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

### <span data-ttu-id="ac076-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ac076-120">-Name</span></span>
<span data-ttu-id="ac076-121">Der Triggername.</span><span class="sxs-lookup"><span data-stu-id="ac076-121">The trigger name.</span></span>

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

### <span data-ttu-id="ac076-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac076-122">-ResourceGroupName</span></span>
<span data-ttu-id="ac076-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ac076-123">The resource group name.</span></span>

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

### <span data-ttu-id="ac076-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ac076-124">-ResourceId</span></span>
<span data-ttu-id="ac076-125">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ac076-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="ac076-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ac076-126">-Confirm</span></span>
<span data-ttu-id="ac076-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ac076-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ac076-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ac076-128">-WhatIf</span></span>
<span data-ttu-id="ac076-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ac076-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ac076-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ac076-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ac076-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac076-131">CommonParameters</span></span>
<span data-ttu-id="ac076-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac076-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac076-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac076-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac076-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ac076-134">INPUTS</span></span>

### <span data-ttu-id="ac076-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ac076-135">System.String</span></span>
<span data-ttu-id="ac076-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="ac076-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="ac076-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ac076-137">OUTPUTS</span></span>

### <span data-ttu-id="ac076-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="ac076-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="ac076-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="ac076-139">NOTES</span></span>

## <span data-ttu-id="ac076-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="ac076-140">RELATED LINKS</span></span>

