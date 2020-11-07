---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2trigger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2Trigger.md
ms.openlocfilehash: 17953aa02bf0242f358fd07b1173977db6318d05
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93665420"
---
# <span data-ttu-id="5cc7c-101">Set-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5cc7c-101">Set-AzureRmDataFactoryV2Trigger</span></span>

## <span data-ttu-id="5cc7c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5cc7c-102">SYNOPSIS</span></span>
<span data-ttu-id="5cc7c-103">Erstellt einen Trigger in einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="5cc7c-103">Creates a trigger in a data factory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5cc7c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5cc7c-104">SYNTAX</span></span>

### <span data-ttu-id="5cc7c-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="5cc7c-105">ByFactoryName (Default)</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-Name] <String> [-DefinitionFile] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5cc7c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5cc7c-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2Trigger [-DefinitionFile] <String> [-ResourceId] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5cc7c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cc7c-107">DESCRIPTION</span></span>
<span data-ttu-id="5cc7c-108">Das Cmdlet " **Satz-AzureRmDataFactoryV2Trigger** " erstellt einen Trigger in einer Data Factory.</span><span class="sxs-lookup"><span data-stu-id="5cc7c-108">The **Set-AzureRmDataFactoryV2Trigger** cmdlet creates a trigger in a data factory.</span></span> <span data-ttu-id="5cc7c-109">Wenn Sie einen Namen für einen bereits vorhandenen Trigger angeben, fordert das Cmdlet eine Bestätigung auf, bevor der Trigger ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="5cc7c-109">If you specify a name for a trigger that already exists, the cmdlet prompts for confirmation before replacing the trigger.</span></span> <span data-ttu-id="5cc7c-110">Wenn Sie den Parameter _Force_ angeben, ersetzt das Cmdlet den vorhandenen Trigger ohne Aufforderung zur Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="5cc7c-110">If you specify the _Force_ parameter, the cmdlet replaces the existing trigger without prompting for confirmation.</span></span> <span data-ttu-id="5cc7c-111">Trigger werden im Zustand "stopped" erstellt, was bedeutet, dass Sie nicht sofort mit dem Aufruf von Pipelines beginnen, auf die Sie verweisen.</span><span class="sxs-lookup"><span data-stu-id="5cc7c-111">Triggers are created in the 'Stopped' state, meaning that they don't immediately begin invoking pipelines that they reference.</span></span>

## <span data-ttu-id="5cc7c-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5cc7c-112">EXAMPLES</span></span>

### <span data-ttu-id="5cc7c-113">Beispiel 1: Erstellen eines Triggers</span><span class="sxs-lookup"><span data-stu-id="5cc7c-113">Example 1: Create a trigger</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2Trigger -ResourceGroupName "ADF" -DataFactoryName "WikiADF" -Name "ScheduledTrigger" -DefinitionFile ".\scheduledTrigger.json"

    TriggerName       : ScheduledTrigger
    ResourceGroupName : ADF
    DataFactoryName   : WikiADF
    Properties        : Microsoft.Azure.Management.DataFactory.Models.ScheduleTrigger
    RuntimeState      : Stopped
```

<span data-ttu-id="5cc7c-114">Erstellen Sie einen neuen Trigger mit dem Namen "ScheduledTrigger" in der Data Factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="5cc7c-114">Create a new trigger called "ScheduledTrigger" in the data factory "WikiADF".</span></span> <span data-ttu-id="5cc7c-115">Der Trigger wird im Zustand "stopped" erstellt, was bedeutet, dass er nicht sofort gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="5cc7c-115">The trigger is created in the 'Stopped' state, meaning that it doesn't immediately start.</span></span> <span data-ttu-id="5cc7c-116">Ein Trigger kann mit dem Cmdlet gestartet werden `Start-AzureRmDataFactoryV2Trigger` .</span><span class="sxs-lookup"><span data-stu-id="5cc7c-116">A trigger can be started using the `Start-AzureRmDataFactoryV2Trigger` cmdlet.</span></span>

## <span data-ttu-id="5cc7c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="5cc7c-117">PARAMETERS</span></span>

### <span data-ttu-id="5cc7c-118">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="5cc7c-118">-DataFactoryName</span></span>
<span data-ttu-id="5cc7c-119">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="5cc7c-119">The data factory name.</span></span>

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

### <span data-ttu-id="5cc7c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5cc7c-120">-DefaultProfile</span></span>
<span data-ttu-id="5cc7c-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5cc7c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cc7c-122">-Definitions-Nr.</span><span class="sxs-lookup"><span data-stu-id="5cc7c-122">-DefinitionFile</span></span>
<span data-ttu-id="5cc7c-123">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="5cc7c-123">The JSON file path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cc7c-124">-Force</span><span class="sxs-lookup"><span data-stu-id="5cc7c-124">-Force</span></span>
<span data-ttu-id="5cc7c-125">Führt das Cmdlet ohne Aufforderung zur Bestätigung aus.</span><span class="sxs-lookup"><span data-stu-id="5cc7c-125">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5cc7c-126">-Name</span><span class="sxs-lookup"><span data-stu-id="5cc7c-126">-Name</span></span>
<span data-ttu-id="5cc7c-127">Der Name des Triggers.</span><span class="sxs-lookup"><span data-stu-id="5cc7c-127">The trigger name.</span></span>

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

### <span data-ttu-id="5cc7c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5cc7c-128">-ResourceGroupName</span></span>
<span data-ttu-id="5cc7c-129">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5cc7c-129">The resource group name.</span></span>

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

### <span data-ttu-id="5cc7c-130">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5cc7c-130">-ResourceId</span></span>
<span data-ttu-id="5cc7c-131">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="5cc7c-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5cc7c-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5cc7c-132">-Confirm</span></span>
<span data-ttu-id="5cc7c-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5cc7c-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5cc7c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5cc7c-134">-WhatIf</span></span>
<span data-ttu-id="5cc7c-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird, das Cmdlet aber nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5cc7c-135">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5cc7c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cc7c-136">CommonParameters</span></span>
<span data-ttu-id="5cc7c-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cc7c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cc7c-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cc7c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cc7c-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5cc7c-139">INPUTS</span></span>

### <span data-ttu-id="5cc7c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="5cc7c-140">System.String</span></span>

## <span data-ttu-id="5cc7c-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5cc7c-141">OUTPUTS</span></span>

### <span data-ttu-id="5cc7c-142">Microsoft. Azure. Commands. DataFactoryV2. Models. PSTrigger</span><span class="sxs-lookup"><span data-stu-id="5cc7c-142">Microsoft.Azure.Commands.DataFactoryV2.Models.PSTrigger</span></span>

## <span data-ttu-id="5cc7c-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="5cc7c-143">NOTES</span></span>

## <span data-ttu-id="5cc7c-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5cc7c-144">RELATED LINKS</span></span>

[<span data-ttu-id="5cc7c-145">Get-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5cc7c-145">Get-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5cc7c-146">Anfang-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5cc7c-146">Start-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5cc7c-147">Stopp-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5cc7c-147">Stop-AzureRmDataFactoryV2Trigger</span></span>]()

[<span data-ttu-id="5cc7c-148">Remove-AzureRmDataFactoryV2Trigger</span><span class="sxs-lookup"><span data-stu-id="5cc7c-148">Remove-AzureRmDataFactoryV2Trigger</span></span>]()
