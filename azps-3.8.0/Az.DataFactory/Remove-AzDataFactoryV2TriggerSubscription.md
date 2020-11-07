---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/remove-azdatafactoryv2triggersubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Remove-AzDataFactoryV2TriggerSubscription.md
ms.openlocfilehash: 89fb4591af19db46aa536ebd15f3746cf6691244
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847159"
---
# <span data-ttu-id="8d7bd-101">Remove-AzDataFactoryV2TriggerSubscription</span><span class="sxs-lookup"><span data-stu-id="8d7bd-101">Remove-AzDataFactoryV2TriggerSubscription</span></span>

## <span data-ttu-id="8d7bd-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8d7bd-102">SYNOPSIS</span></span>
<span data-ttu-id="8d7bd-103">Kündigen Sie den Ereignisauslöser für externe Dienstereignisse.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-103">Unsubscribe the event trigger to external service events.</span></span>

## <span data-ttu-id="8d7bd-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8d7bd-104">SYNTAX</span></span>

### <span data-ttu-id="8d7bd-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8d7bd-105">ByFactoryName (Default)</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-Name] <String> [-PassThru] [-Force] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d7bd-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8d7bd-106">ByInputObject</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-InputObject] <PSTrigger> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d7bd-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8d7bd-107">ByResourceId</span></span>
```
Remove-AzDataFactoryV2TriggerSubscription [-PassThru] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d7bd-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8d7bd-108">DESCRIPTION</span></span>
<span data-ttu-id="8d7bd-109">Mit diesem Befehl wird der Event-Trigger für die angegebenen externen Dienstereignisse aus dem Trigger-Definition.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-109">This command unsubscribes the event trigger to the specified external service events from the trigger defintion.</span></span>

## <span data-ttu-id="8d7bd-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8d7bd-110">EXAMPLES</span></span>

### <span data-ttu-id="8d7bd-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8d7bd-111">Example 1</span></span>
```
PS C:\> Remove-AzDataFactoryV2TriggerSubscription -ResourceGroupName ADF -DataFactoryName WikiADF -Name Trigger1
```

<span data-ttu-id="8d7bd-112">Mit diesem Befehl wird der BlobEnetTrigger1-Trigger für die angegebenen Ereignisse aus dem Trigger-Definition abgemeldet.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-112">This command will unsubscribe BlobEnetTrigger1 trigger to the specified events from the trigger defintion.</span></span>

## <span data-ttu-id="8d7bd-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="8d7bd-113">PARAMETERS</span></span>

### <span data-ttu-id="8d7bd-114">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="8d7bd-114">-DataFactoryName</span></span>
<span data-ttu-id="8d7bd-115">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-115">The data factory name.</span></span>

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

### <span data-ttu-id="8d7bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d7bd-116">-DefaultProfile</span></span>
<span data-ttu-id="8d7bd-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d7bd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8d7bd-118">-Force</span></span>
<span data-ttu-id="8d7bd-119">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-119">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="8d7bd-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8d7bd-120">-InputObject</span></span>
<span data-ttu-id="8d7bd-121">Das Trigger-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-121">The trigger object.</span></span>

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

### <span data-ttu-id="8d7bd-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8d7bd-122">-Name</span></span>
<span data-ttu-id="8d7bd-123">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-123">The trigger name.</span></span>

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

### <span data-ttu-id="8d7bd-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d7bd-124">-PassThru</span></span>
<span data-ttu-id="8d7bd-125">Wenn angegeben, gibt das Cmdlet beim erfolgreichen löschen true zurück.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-125">If specified, cmdlet will return return true on successful delete.</span></span>

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

### <span data-ttu-id="8d7bd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d7bd-126">-ResourceGroupName</span></span>
<span data-ttu-id="8d7bd-127">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-127">The resource group name.</span></span>

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

### <span data-ttu-id="8d7bd-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="8d7bd-128">-ResourceId</span></span>
<span data-ttu-id="8d7bd-129">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-129">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8d7bd-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8d7bd-130">-Confirm</span></span>
<span data-ttu-id="8d7bd-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d7bd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d7bd-132">-WhatIf</span></span>
<span data-ttu-id="8d7bd-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d7bd-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d7bd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d7bd-135">CommonParameters</span></span>
<span data-ttu-id="8d7bd-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d7bd-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8d7bd-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d7bd-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8d7bd-138">INPUTS</span></span>

### <span data-ttu-id="8d7bd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8d7bd-139">System.String</span></span>
<span data-ttu-id="8d7bd-140">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="8d7bd-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="8d7bd-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8d7bd-141">OUTPUTS</span></span>

### <span data-ttu-id="8d7bd-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTriggerSubscriptionStatus</span><span class="sxs-lookup"><span data-stu-id="8d7bd-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTriggerSubscriptionStatus</span></span>

## <span data-ttu-id="8d7bd-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="8d7bd-143">NOTES</span></span>

## <span data-ttu-id="8d7bd-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8d7bd-144">RELATED LINKS</span></span>

