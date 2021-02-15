---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 89fb4591af19db46aa536ebd15f3746cf6691244
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174641"
---
# <span data-ttu-id="f8f5e-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="f8f5e-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="f8f5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8f5e-102">SYNOPSIS</span></span>
<span data-ttu-id="f8f5e-103">Kündigen des Auslösers des Ereignisses für externe Dienste</span><span class="sxs-lookup"><span data-stu-id="f8f5e-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="f8f5e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f8f5e-104">SYNTAX</span></span>

### <span data-ttu-id="f8f5e-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f8f5e-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f8f5e-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f8f5e-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f8f5e-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f8f5e-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8f5e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f8f5e-108">DESCRIPTION</span></span>
<span data-ttu-id="f8f5e-109">Dieser Befehl kündigen das Abonnement des Ereignistriggers für die angegebenen Ereignisse des externen Diensts aus der Triggerdefinierung.</span><span class="sxs-lookup"><span data-stu-id="f8f5e-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="f8f5e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f8f5e-110">EXAMPLES</span></span>

### <span data-ttu-id="f8f5e-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8f5e-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="f8f5e-112">Dieser Befehl kündigen den BlobEnetTrigger1-Trigger für die angegebenen Ereignisse der Triggerdefinierung.</span><span class="sxs-lookup"><span data-stu-id="f8f5e-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="f8f5e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f8f5e-113">PARAMETERS</span></span>

### <span data-ttu-id="f8f5e-114">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="f8f5e-114">-DataFactoryName</span></span>
<span data-ttu-id="f8f5e-115">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="f8f5e-115">The data factory name.</span></span>

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

### <span data-ttu-id="f8f5e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8f5e-116">-DefaultProfile</span></span>
<span data-ttu-id="f8f5e-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f8f5e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f8f5e-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f8f5e-118">-Force</span></span>
<span data-ttu-id="f8f5e-119">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="f8f5e-119">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f5e-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f8f5e-120">-InputObject</span></span>
<span data-ttu-id="f8f5e-121">Das Triggerobjekt.</span><span class="sxs-lookup"><span data-stu-id="f8f5e-121">The trigger object.</span></span>

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

### <span data-ttu-id="f8f5e-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f8f5e-122">-Name</span></span>
<span data-ttu-id="f8f5e-123">Der Auslösername.</span><span class="sxs-lookup"><span data-stu-id="f8f5e-123">The trigger name.</span></span>

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

### <span data-ttu-id="f8f5e-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f8f5e-124">-PassThru</span></span>
<span data-ttu-id="f8f5e-125">Wenn diese Angabe angegeben ist, gibt das Cmdlet beim erfolgreichen Löschen "true" zurück.</span><span class="sxs-lookup"><span data-stu-id="f8f5e-125">If specified, cmdlet will return return true on successful delete.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8f5e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8f5e-126">-ResourceGroupName</span></span>
<span data-ttu-id="f8f5e-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f8f5e-127">The resource group name.</span></span>

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

### <span data-ttu-id="f8f5e-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f8f5e-128">-ResourceId</span></span>
<span data-ttu-id="f8f5e-129">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f8f5e-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f8f5e-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f8f5e-130">-Confirm</span></span>
<span data-ttu-id="f8f5e-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8f5e-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8f5e-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="f8f5e-132">-WhatIf</span></span>
<span data-ttu-id="f8f5e-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8f5e-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f8f5e-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8f5e-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8f5e-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8f5e-135">CommonParameters</span></span>
<span data-ttu-id="f8f5e-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8f5e-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8f5e-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8f5e-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8f5e-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f8f5e-138">INPUTS</span></span>

### <span data-ttu-id="f8f5e-139">System.String</span><span class="sxs-lookup"><span data-stu-id="f8f5e-139">System.String</span></span>
<span data-ttu-id="f8f5e-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span><span class="sxs-lookup"><span data-stu-id="f8f5e-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="f8f5e-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f8f5e-141">OUTPUTS</span></span>

### <span data-ttu-id="f8f5e-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="f8f5e-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="f8f5e-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f8f5e-143">NOTES</span></span>

## <span data-ttu-id="f8f5e-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f8f5e-144">RELATED LINKS</span></span>

