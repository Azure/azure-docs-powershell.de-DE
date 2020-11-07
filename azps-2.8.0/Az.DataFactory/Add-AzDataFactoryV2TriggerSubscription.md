---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: c99626e1323f10e98dcef1efc7ae622aab5f6b5a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651794"
---
# <span data-ttu-id="67eca-101">Add-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="67eca-101">Add-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="67eca-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="67eca-102">SYNOPSIS</span></span>
<span data-ttu-id="67eca-103">Abonnieren Sie den Ereignisauslöser für externe Dienstereignisse.</span><span class="sxs-lookup"><span data-stu-id="67eca-103">Subscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="67eca-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="67eca-104">SYNTAX</span></span>

### <span data-ttu-id="67eca-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="67eca-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="67eca-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="67eca-106">ByInputObject</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="67eca-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="67eca-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2TriggerSubscription [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67eca-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="67eca-108">DESCRIPTION</span></span>
<span data-ttu-id="67eca-109">Dieser Befehl abonniert den Ereignistrigger für die angegebenen externen Dienstereignisse aus dem Trigger-Definition.</span><span class="sxs-lookup"><span data-stu-id="67eca-109">This command subscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="67eca-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="67eca-110">EXAMPLES</span></span>

### <span data-ttu-id="67eca-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="67eca-111">Example 1</span></span>
```
PS C:\> Add-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1

TriggerName Status
----------- ------
Trigger1    Provisioning
```

<span data-ttu-id="67eca-112">Dieser Befehl abonniert BlobEnetTrigger1-Trigger für die angegebenen Ereignisse aus dem Trigger-Definition.</span><span class="sxs-lookup"><span data-stu-id="67eca-112">This command will subscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="67eca-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="67eca-113">PARAMETERS</span></span>

### <span data-ttu-id="67eca-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="67eca-114">-DataFactoryName</span></span>
<span data-ttu-id="67eca-115">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="67eca-115">The data factory name.</span></span>

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

### <span data-ttu-id="67eca-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67eca-116">-DefaultProfile</span></span>
<span data-ttu-id="67eca-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="67eca-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="67eca-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="67eca-118">-InputObject</span></span>
<span data-ttu-id="67eca-119">Das Trigger-Objekt.</span><span class="sxs-lookup"><span data-stu-id="67eca-119">The trigger object.</span></span>

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

### <span data-ttu-id="67eca-120">-Name</span><span class="sxs-lookup"><span data-stu-id="67eca-120">-Name</span></span>
<span data-ttu-id="67eca-121">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="67eca-121">The trigger name.</span></span>

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

### <span data-ttu-id="67eca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67eca-122">-ResourceGroupName</span></span>
<span data-ttu-id="67eca-123">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="67eca-123">The resource group name.</span></span>

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

### <span data-ttu-id="67eca-124">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="67eca-124">-ResourceId</span></span>
<span data-ttu-id="67eca-125">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="67eca-125">The Azure resource ID.</span></span>

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

### <span data-ttu-id="67eca-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="67eca-126">-Confirm</span></span>
<span data-ttu-id="67eca-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="67eca-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67eca-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67eca-128">-WhatIf</span></span>
<span data-ttu-id="67eca-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="67eca-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67eca-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="67eca-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67eca-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67eca-131">CommonParameters</span></span>
<span data-ttu-id="67eca-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67eca-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67eca-133">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67eca-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67eca-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="67eca-134">INPUTS</span></span>

### <span data-ttu-id="67eca-135">System. String</span><span class="sxs-lookup"><span data-stu-id="67eca-135">System.String</span></span>
<span data-ttu-id="67eca-136">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="67eca-136">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="67eca-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="67eca-137">OUTPUTS</span></span>

### <span data-ttu-id="67eca-138">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="67eca-138">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="67eca-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="67eca-139">NOTES</span></span>

## <span data-ttu-id="67eca-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="67eca-140">RELATED LINKS</span></span>

