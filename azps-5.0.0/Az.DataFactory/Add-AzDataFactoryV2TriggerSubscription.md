---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 6e38f98f9dd3ebfaa2ad4747016556aecd9998e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94298636"
---
# <span data-ttu-id="a1868-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="a1868-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="a1868-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a1868-102">SYNOPSIS</span></span>
<span data-ttu-id="a1868-103">Abonnieren Sie den Ereignisauslöser für externe Dienstereignisse.</span><span class="sxs-lookup"><span data-stu-id="a1868-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="a1868-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a1868-104">SYNTAX</span></span>

### <span data-ttu-id="a1868-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="a1868-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1868-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="a1868-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1868-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a1868-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1868-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a1868-108">DESCRIPTION</span></span>
<span data-ttu-id="a1868-109">Dieser Befehl abonniert den Ereignistrigger für die angegebenen externen Dienstereignisse aus dem Trigger-Definition.</span><span class="sxs-lookup"><span data-stu-id="a1868-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="a1868-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a1868-110">EXAMPLES</span></span>

### <span data-ttu-id="a1868-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a1868-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="a1868-112">Dieser Befehl abonniert BlobEnetTrigger1-Trigger für die angegebenen Ereignisse aus dem Trigger-Definition.</span><span class="sxs-lookup"><span data-stu-id="a1868-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="a1868-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="a1868-113">PARAMETERS</span></span>

### <span data-ttu-id="a1868-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="a1868-114">-DataFactoryName</span></span>
<span data-ttu-id="a1868-115">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="a1868-115">The data factory name.</span></span>

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

### <span data-ttu-id="a1868-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1868-116">-DefaultProfile</span></span>
<span data-ttu-id="a1868-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a1868-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a1868-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a1868-118">-InputObject</span></span>
<span data-ttu-id="a1868-119">Das Trigger-Objekt.</span><span class="sxs-lookup"><span data-stu-id="a1868-119">The trigger object.</span></span>

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

### <span data-ttu-id="a1868-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a1868-120">-Name</span></span>
<span data-ttu-id="a1868-121">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="a1868-121">The trigger name.</span></span>

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

### <span data-ttu-id="a1868-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1868-122">-ResourceGroupName</span></span>
<span data-ttu-id="a1868-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="a1868-123">The resource group name.</span></span>

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

### <span data-ttu-id="a1868-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a1868-124">-ResourceId</span></span>
<span data-ttu-id="a1868-125">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="a1868-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a1868-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a1868-126">-Confirm</span></span>
<span data-ttu-id="a1868-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a1868-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1868-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1868-128">-WhatIf</span></span>
<span data-ttu-id="a1868-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a1868-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1868-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a1868-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1868-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1868-131">CommonParameters</span></span>
<span data-ttu-id="a1868-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1868-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1868-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1868-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1868-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a1868-134">INPUTS</span></span>

### <span data-ttu-id="a1868-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a1868-135">System.String</span></span>
<span data-ttu-id="a1868-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="a1868-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="a1868-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a1868-137">OUTPUTS</span></span>

### <span data-ttu-id="a1868-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="a1868-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="a1868-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="a1868-139">NOTES</span></span>

## <span data-ttu-id="a1868-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a1868-140">RELATED LINKS</span></span>

