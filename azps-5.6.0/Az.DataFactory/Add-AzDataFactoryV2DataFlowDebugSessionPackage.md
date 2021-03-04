---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/add-azdatafactoryv2dataflowdebugsessionpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
ms.openlocfilehash: 185f01f31f8cae62e51b7b28909f66fbf37884e2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101939624"
---
# <span data-ttu-id="8d853-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="8d853-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>

## <span data-ttu-id="8d853-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d853-102">SYNOPSIS</span></span>
<span data-ttu-id="8d853-103">Fügen Sie die Datenflussressource und deren Abhängigkeiten zu einer bestimmten Datenflussdebuggersitzung hinzu.</span><span class="sxs-lookup"><span data-stu-id="8d853-103">Add data flow resource and its dependencies into specific data flow debug session.</span></span>

## <span data-ttu-id="8d853-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8d853-104">SYNTAX</span></span>

### <span data-ttu-id="8d853-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="8d853-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8d853-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="8d853-106">ByFactoryObject</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8d853-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8d853-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8d853-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8d853-108">DESCRIPTION</span></span>
<span data-ttu-id="8d853-109">Mit diesem Befehl werden die Datenflussressource und deren Abhängigkeiten an die spezifische Debugsitzung anfügen Die PowerShell-Befehlssequenz für den Workflow für den Datenflussdebugger sollte wie die folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="8d853-109">This command attaches data flow resource and its dependencies to the specific debug session The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="8d853-110">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="8d853-110">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="8d853-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="8d853-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="8d853-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (wiederholen Sie diesen Schritt für verschiedene Befehle/Ziele, oder wiederholen Sie schritt 2-3, um die Paketdatei zu ändern)</span><span class="sxs-lookup"><span data-stu-id="8d853-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="8d853-113">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="8d853-113">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="8d853-114">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8d853-114">EXAMPLES</span></span>

### <span data-ttu-id="8d853-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8d853-115">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Add-AzDataFactoryV2DataFlowDebugSessionPackage -ResourceGroupName adf -DataFactoryName WikiADF -PackageFile "D:\dataflowps\addpackage.json" -SessionId 550effe4-93a3-485c-8525-eaf25259efbd
```

<span data-ttu-id="8d853-116">Hinzufügen eines Datenflusspakets zur Debugsitzung "550effe4-93a3-485c-8525-eaf25259efbd" der Daten factory "WikiADF".</span><span class="sxs-lookup"><span data-stu-id="8d853-116">Add data flow package into debug session "550effe4-93a3-485c-8525-eaf25259efbd" of "WikiADF" data factory.</span></span>
<span data-ttu-id="8d853-117">Die Pakcagedatei enthält die Debugressource für den Datenfluss, eine Liste der Datasetdebuggerressource, eine Liste der verknüpften Dienstdebuggerressource, Debugeinstellungen und Sitzungs-ID.</span><span class="sxs-lookup"><span data-stu-id="8d853-117">Pakcage file contains data flow debug resource, list of dataset debug resouce, list of linked service debug resource, debug setting and session ID.</span></span> <span data-ttu-id="8d853-118">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="8d853-118">For instance:</span></span>

<span data-ttu-id="8d853-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": " \\ ", "firstRowAsHeader": true, "quoteChar": " \" " }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https; AccountName=name; AccountKey=key; EndpointSuffix=core.windows.net" } } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span><span class="sxs-lookup"><span data-stu-id="8d853-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": "\\", "firstRowAsHeader": true, "quoteChar": "\"" }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https;AccountName=name;AccountKey=key;EndpointSuffix=core.windows.net" } } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span></span>

<span data-ttu-id="8d853-120">Der Parameter SessionID wird verwendet, um die vorhandene sessionId-Eigenschaft in der Paketdatei zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="8d853-120">SessionID parameter is used to replace the existing sessionId property in the package file.</span></span>

## <span data-ttu-id="8d853-121">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8d853-121">PARAMETERS</span></span>

### <span data-ttu-id="8d853-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="8d853-122">-DataFactory</span></span>
<span data-ttu-id="8d853-123">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="8d853-123">The data factory object.</span></span>

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

### <span data-ttu-id="8d853-124">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="8d853-124">-DataFactoryName</span></span>
<span data-ttu-id="8d853-125">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="8d853-125">The data factory name.</span></span>

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

### <span data-ttu-id="8d853-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d853-126">-DefaultProfile</span></span>
<span data-ttu-id="8d853-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8d853-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d853-128">-PackageFile</span><span class="sxs-lookup"><span data-stu-id="8d853-128">-PackageFile</span></span>
<span data-ttu-id="8d853-129">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="8d853-129">The JSON file path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: File

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8d853-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8d853-130">-PassThru</span></span>
<span data-ttu-id="8d853-131">Wenn angegeben wird, wird "true" geschrieben, wenn der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="8d853-131">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="8d853-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="8d853-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="8d853-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d853-133">-ResourceGroupName</span></span>
<span data-ttu-id="8d853-134">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8d853-134">The resource group name.</span></span>

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

### <span data-ttu-id="8d853-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8d853-135">-ResourceId</span></span>
<span data-ttu-id="8d853-136">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="8d853-136">The Azure resource ID.</span></span>

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

### <span data-ttu-id="8d853-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8d853-137">-Confirm</span></span>
<span data-ttu-id="8d853-138">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8d853-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d853-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d853-139">-WhatIf</span></span>
<span data-ttu-id="8d853-140">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8d853-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d853-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8d853-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d853-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d853-142">CommonParameters</span></span>
<span data-ttu-id="8d853-143">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d853-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d853-144">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8d853-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d853-145">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8d853-145">INPUTS</span></span>

### <span data-ttu-id="8d853-146">System.String</span><span class="sxs-lookup"><span data-stu-id="8d853-146">System.String</span></span>

### <span data-ttu-id="8d853-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="8d853-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="8d853-148">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8d853-148">OUTPUTS</span></span>

### <span data-ttu-id="8d853-149">System.Void</span><span class="sxs-lookup"><span data-stu-id="8d853-149">System.Void</span></span>

### <span data-ttu-id="8d853-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8d853-150">System.Boolean</span></span>

## <span data-ttu-id="8d853-151">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8d853-151">NOTES</span></span>
<span data-ttu-id="8d853-152">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="8d853-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="8d853-153">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8d853-153">RELATED LINKS</span></span>

[<span data-ttu-id="8d853-154">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="8d853-154">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="8d853-155">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="8d853-155">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="8d853-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="8d853-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="8d853-157">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="8d853-157">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
