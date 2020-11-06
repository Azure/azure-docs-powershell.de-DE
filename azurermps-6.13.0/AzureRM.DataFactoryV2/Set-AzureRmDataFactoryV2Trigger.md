---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: dc4630359070e627a3c65c63f21c23f987cb9a31
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93496254"
---
# <span data-ttu-id="ed8ac-101">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ed8ac-101">Set-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="ed8ac-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ed8ac-102">SYNOPSIS</span></span>
<span data-ttu-id="ed8ac-103">Erstellt einen Trigger in einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-103">Creates a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed8ac-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed8ac-104">SYNTAX</span></span>

### <span data-ttu-id="ed8ac-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="ed8ac-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ed8ac-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ed8ac-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed8ac-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ed8ac-107">DESCRIPTION</span></span>
<span data-ttu-id="ed8ac-108">Das Cmdlet " **Satz-AzureRmDataFactoryV2Trigger** " erstellt einen Trigger in einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-108">The **Set-AzureRmDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="ed8ac-109">Wenn Sie einen Namen für einen bereits vorhandenen Trigger angeben, fordert das Cmdlet eine Bestätigung auf, bevor der Trigger ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="ed8ac-110">Wenn Sie den Parameter _Force_ angeben, ersetzt das Cmdlet den vorhandenen Trigger ohne Aufforderung zur Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="ed8ac-111">Trigger werden im Zustand "stopped" erstellt, was bedeutet, dass Sie nicht sofort mit dem Aufruf von Pipelines beginnen, auf die Sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="ed8ac-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ed8ac-112">EXAMPLES</span></span>

### <span data-ttu-id="ed8ac-113">Beispiel 1: Erstellen eines Triggers</span><span class="sxs-lookup"><span data-stu-id="ed8ac-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="ed8ac-114">Erstellen Sie einen neuen Trigger mit dem Namen "ScheduledTrigger" in der Data Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="ed8ac-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="ed8ac-115">Der Trigger wird im Zustand "stopped" erstellt, was bedeutet, dass er nicht sofort gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="ed8ac-116">Ein Trigger kann mit dem Cmdlet gestartet werden `Start-AzureRmDataFactoryV2Trigger` .</span><span class="sxs-lookup"><span data-stu-id="ed8ac-116">A trigger can be started using the `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="ed8ac-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed8ac-117">PARAMETERS</span></span>

### <span data-ttu-id="ed8ac-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="ed8ac-118">-DataFactoryName</span></span>
<span data-ttu-id="ed8ac-119">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-119">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ac-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed8ac-120">-DefaultProfile</span></span>
<span data-ttu-id="ed8ac-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ac-122">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-122">-DefinitionFile</span></span>
<span data-ttu-id="ed8ac-123">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-123">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ac-124">-Force</span><span class="sxs-lookup"><span data-stu-id="ed8ac-124">-Force</span></span>
<span data-ttu-id="ed8ac-125">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-125">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ac-126">-Name</span><span class="sxs-lookup"><span data-stu-id="ed8ac-126">-Name</span></span>
<span data-ttu-id="ed8ac-127">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-127">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases: TriggerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ac-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed8ac-128">-ResourceGroupName</span></span>
<span data-ttu-id="ed8ac-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ac-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="ed8ac-130">-ResourceId</span></span>
<span data-ttu-id="ed8ac-131">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed8ac-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="ed8ac-132">-Confirm</span></span>
<span data-ttu-id="ed8ac-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed8ac-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed8ac-134">-WhatIf</span></span>
<span data-ttu-id="ed8ac-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="ed8ac-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed8ac-136">CommonParameters</span></span>
<span data-ttu-id="ed8ac-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed8ac-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed8ac-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed8ac-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed8ac-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ed8ac-139">INPUTS</span></span>

### <span data-ttu-id="ed8ac-140">System. String</span><span class="sxs-lookup"><span data-stu-id="ed8ac-140">System.String</span></span>

## <span data-ttu-id="ed8ac-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ed8ac-141">OUTPUTS</span></span>

### <span data-ttu-id="ed8ac-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="ed8ac-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="ed8ac-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="ed8ac-143">NOTES</span></span>

## <span data-ttu-id="ed8ac-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ed8ac-144">RELATED LINKS</span></span>

[<span data-ttu-id="ed8ac-145">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ed8ac-145">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="ed8ac-146">Anfang-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ed8ac-146">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="ed8ac-147">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ed8ac-147">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="ed8ac-148">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="ed8ac-148">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
