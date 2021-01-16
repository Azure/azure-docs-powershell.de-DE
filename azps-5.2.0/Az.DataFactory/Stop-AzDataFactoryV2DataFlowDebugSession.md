---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 63e78c0068d17986f845adaae9dbc5caf22b4b4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98307819"
---
# <span data-ttu-id="d3e66-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="d3e66-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="d3e66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3e66-102">SYNOPSIS</span></span>
<span data-ttu-id="d3e66-103">Beendet eine Datenflussdebuggersitzung in Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="d3e66-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="d3e66-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d3e66-104">SYNTAX</span></span>

### <span data-ttu-id="d3e66-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="d3e66-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d3e66-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="d3e66-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d3e66-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e66-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3e66-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d3e66-108">DESCRIPTION</span></span>
<span data-ttu-id="d3e66-109">Dieser Befehl beendet die Debugsitzung, andern falls nicht, wird die Sitzung automatisch entsprechend der Time To Live-Einstellung der Debugsitzung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d3e66-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="d3e66-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d3e66-110">EXAMPLES</span></span>

### <span data-ttu-id="d3e66-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d3e66-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="d3e66-112">Beendet die Datenflussdebuggersitzung "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in der Daten factory "WikiADF"</span><span class="sxs-lookup"><span data-stu-id="d3e66-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="d3e66-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3e66-113">PARAMETERS</span></span>

### <span data-ttu-id="d3e66-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="d3e66-114">-DataFactory</span></span>
<span data-ttu-id="d3e66-115">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="d3e66-115">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByFactoryObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e66-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="d3e66-116">-DataFactoryName</span></span>
<span data-ttu-id="d3e66-117">Der Name der Daten factory.</span><span class="sxs-lookup"><span data-stu-id="d3e66-117">The data factory name.</span></span>

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

### <span data-ttu-id="d3e66-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3e66-118">-DefaultProfile</span></span>
<span data-ttu-id="d3e66-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d3e66-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3e66-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d3e66-120">-PassThru</span></span>
<span data-ttu-id="d3e66-121">Wenn angegeben, wird "true" für den Fall geschrieben, dass der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="d3e66-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="d3e66-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="d3e66-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="d3e66-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3e66-123">-ResourceGroupName</span></span>
<span data-ttu-id="d3e66-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="d3e66-124">The resource group name.</span></span>

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

### <span data-ttu-id="d3e66-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3e66-125">-ResourceId</span></span>
<span data-ttu-id="d3e66-126">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="d3e66-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="d3e66-127">-SessionId</span><span class="sxs-lookup"><span data-stu-id="d3e66-127">-SessionId</span></span>
<span data-ttu-id="d3e66-128">Die Sitzungs-ID des Datenflussdebuggers.</span><span class="sxs-lookup"><span data-stu-id="d3e66-128">The data flow debug session ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3e66-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="d3e66-129">-Confirm</span></span>
<span data-ttu-id="d3e66-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d3e66-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3e66-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="d3e66-131">-WhatIf</span></span>
<span data-ttu-id="d3e66-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3e66-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d3e66-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3e66-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3e66-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3e66-134">CommonParameters</span></span>
<span data-ttu-id="d3e66-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3e66-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3e66-136">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3e66-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3e66-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d3e66-137">INPUTS</span></span>

### <span data-ttu-id="d3e66-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d3e66-138">System.String</span></span>

### <span data-ttu-id="d3e66-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="d3e66-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="d3e66-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d3e66-140">OUTPUTS</span></span>

### <span data-ttu-id="d3e66-141">System.Void</span><span class="sxs-lookup"><span data-stu-id="d3e66-141">System.Void</span></span>

### <span data-ttu-id="d3e66-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d3e66-142">System.Boolean</span></span>

## <span data-ttu-id="d3e66-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="d3e66-143">NOTES</span></span>
<span data-ttu-id="d3e66-144">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factorys</span><span class="sxs-lookup"><span data-stu-id="d3e66-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="d3e66-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="d3e66-145">RELATED LINKS</span></span>

[<span data-ttu-id="d3e66-146">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="d3e66-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="d3e66-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="d3e66-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="d3e66-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="d3e66-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="d3e66-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="d3e66-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)