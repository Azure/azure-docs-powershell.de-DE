---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/add-azdatafactoryv2dataflowdebugsessionpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Add-AzDataFactoryV2DataFlowDebugSessionPackage.md
ms.openlocfilehash: fdf8d4fefef434e503c0fc21c3036577e56b56c9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651796"
---
# <span data-ttu-id="1fbfe-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="1fbfe-101">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>

## <span data-ttu-id="1fbfe-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1fbfe-102">SYNOPSIS</span></span>
<span data-ttu-id="1fbfe-103">Fügen Sie die Datenfluss Ressource und deren Abhängigkeiten in eine bestimmte Datenfluss-Debugsitzung ein.</span><span class="sxs-lookup"><span data-stu-id="1fbfe-103">Add data flow resource and its dependencies into specific data flow debug session.</span></span>

## <span data-ttu-id="1fbfe-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1fbfe-104">SYNTAX</span></span>

### <span data-ttu-id="1fbfe-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="1fbfe-105">ByFactoryName (Default)</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1fbfe-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="1fbfe-106">ByFactoryObject</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru]
 [-DataFactory] <PSDataFactory> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1fbfe-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="1fbfe-107">ByResourceId</span></span>
```
Add-AzDataFactoryV2DataFlowDebugSessionPackage [-PackageFile] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1fbfe-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1fbfe-108">DESCRIPTION</span></span>
<span data-ttu-id="1fbfe-109">Dieser Befehl fügt die Datenfluss Ressource und ihre Abhängigkeiten an die spezifische Debugsitzung an die PowerShell-Befehlssequenz für den Workflow für den Datenfluss-Debugvorgang sollte wie folgt lauten:</span><span class="sxs-lookup"><span data-stu-id="1fbfe-109">This command attaches data flow resource and its dependencies to the specific debug session The PowerShell command sequence for data flow debug workflow should be:</span></span>
1. <span data-ttu-id="1fbfe-110">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1fbfe-110">Start-AzDataFactoryV2DataFlowDebugSession</span></span>
1. <span data-ttu-id="1fbfe-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="1fbfe-111">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>
1. <span data-ttu-id="1fbfe-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (wiederholen Sie diesen Schritt für verschiedene Befehle/Ziele, oder wiederholen Sie Schritt 2-3, um die Paketdatei zu ändern)</span><span class="sxs-lookup"><span data-stu-id="1fbfe-112">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand (repeat this step for different commands/targets, or repeat step 2-3 in order to change the package file)</span></span>
1. <span data-ttu-id="1fbfe-113">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1fbfe-113">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="1fbfe-114">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1fbfe-114">EXAMPLES</span></span>

### <span data-ttu-id="1fbfe-115">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1fbfe-115">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Add-AzDataFactoryV2DataFlowDebugSessionPackage -ResourceGroupName adf -DataFactoryName WikiADF -PackageFile "D:\dataflowps\addpackage.json" -SessionId 550effe4-93a3-485c-8525-eaf25259efbd
```

<span data-ttu-id="1fbfe-116">Fügen Sie das Datenfluss Paket in die Debug-Sitzung "550effe4-93a3-485c-8525-eaf25259efbd" der Data Factory "WikiADF" ein.</span><span class="sxs-lookup"><span data-stu-id="1fbfe-116">Add data flow package into debug session "550effe4-93a3-485c-8525-eaf25259efbd" of "WikiADF" data factory.</span></span>
<span data-ttu-id="1fbfe-117">Pakcage-Datei enthält Datenfluss-Debug-Ressource, Liste der DataSet-Debug-Resouce, Liste der verknüpften Dienst-Debug-Ressource, Debug-Einstellung und Sitzungs-ID.</span><span class="sxs-lookup"><span data-stu-id="1fbfe-117">Pakcage file contains data flow debug resource, list of dataset debug resouce, list of linked service debug resource, debug setting and session ID.</span></span> <span data-ttu-id="1fbfe-118">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="1fbfe-118">For instance:</span></span>

<span data-ttu-id="1fbfe-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": " \\ ", "firstRowAsHeader": true, "quoteChar": " \" " }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https; Kontoname = Name; AccountKey = Schlüssel; EndpointSuffix = Core. Windows. net "}}}]," debugSettings ": {" sourceSettings ": [{" SourceName ":" Source1 ";" rowLimit ": 1000}]}," sessionId ":" 4f988caf-e765-47d2-82cd-430334a6b135 "}</span><span class="sxs-lookup"><span data-stu-id="1fbfe-119">{ "dataFlow": { "name": "dataflow5", "properties": { "type": "MappingDataFlow", "typeProperties": { "sources": [ { "dataset": { "referenceName": "DelimitedTextInput", "type": "DatasetReference" }, "name": "source1", "typeProperties": {} } ], "sinks": [], "transformations": [], "script": "\n\nsource(output(\n\t\tResourceAgencyNum as string,\n\t\tPublicName as string\n\t),\n\tallowSchemaDrift: true,\n\tvalidateSchema: false) ~> source1" } } }, "datasets": [ { "name": "DelimitedTextInput", "properties": { "linkedServiceName": { "referenceName": "AzureBlobStorage1", "type": "LinkedServiceReference" }, "annotations": [], "type": "DelimitedText", "typeProperties": { "location": { "type": "AzureBlobStorageLocation", "container": "20192019" }, "columnDelimiter": ",", "escapeChar": "\\", "firstRowAsHeader": true, "quoteChar": "\"" }, "schema": [ { "name": "ResourceAgencyNum", "type": "String" }, { "name": "PublicName", "type": "String" } ] }, "type": "Microsoft.DataFactory/factories/datasets" } ], "linkedServices": [ { "name": "AzureBlobStorage1", "type": "Microsoft.DataFactory/factories/linkedservices", "properties": { "annotations": [], "type": "AzureBlobStorage", "typeProperties": { "connectionString": "DefaultEndpointsProtocol=https;AccountName=name;AccountKey=key;EndpointSuffix=core.windows.net" } } } ], "debugSettings": { "sourceSettings": [ { "sourceName": "source1", "rowLimit": 1000 } ] }, "sessionId": "4f988caf-e765-47d2-82cd-430334a6b135" }</span></span>

<span data-ttu-id="1fbfe-120">SessionID-Parameter wird verwendet, um die vorhandene SessionID-Eigenschaft in der Paketdatei zu ersetzen.</span><span class="sxs-lookup"><span data-stu-id="1fbfe-120">SessionID parameter is used to replace the existing sessionId property in the package file.</span></span>

## <span data-ttu-id="1fbfe-121">Parameter</span><span class="sxs-lookup"><span data-stu-id="1fbfe-121">PARAMETERS</span></span>

### <span data-ttu-id="1fbfe-122">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="1fbfe-122">-DataFactory</span></span>
<span data-ttu-id="1fbfe-123">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="1fbfe-123">The data factory object.</span></span>

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

### <span data-ttu-id="1fbfe-124">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="1fbfe-124">-DataFactoryName</span></span>
<span data-ttu-id="1fbfe-125">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="1fbfe-125">The data factory name.</span></span>

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

### <span data-ttu-id="1fbfe-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1fbfe-126">-DefaultProfile</span></span>
<span data-ttu-id="1fbfe-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1fbfe-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1fbfe-128">-Packagedatei</span><span class="sxs-lookup"><span data-stu-id="1fbfe-128">-PackageFile</span></span>
<span data-ttu-id="1fbfe-129">Der JSON-Dateipfad.</span><span class="sxs-lookup"><span data-stu-id="1fbfe-129">The JSON file path.</span></span>

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

### <span data-ttu-id="1fbfe-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1fbfe-130">-PassThru</span></span>
<span data-ttu-id="1fbfe-131">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="1fbfe-131">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="1fbfe-132">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="1fbfe-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="1fbfe-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fbfe-133">-ResourceGroupName</span></span>
<span data-ttu-id="1fbfe-134">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1fbfe-134">The resource group name.</span></span>

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

### <span data-ttu-id="1fbfe-135">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1fbfe-135">-ResourceId</span></span>
<span data-ttu-id="1fbfe-136">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="1fbfe-136">The Azure resource ID.</span></span>

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

### <span data-ttu-id="1fbfe-137">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1fbfe-137">-Confirm</span></span>
<span data-ttu-id="1fbfe-138">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1fbfe-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1fbfe-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1fbfe-139">-WhatIf</span></span>
<span data-ttu-id="1fbfe-140">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1fbfe-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1fbfe-141">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1fbfe-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1fbfe-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fbfe-142">CommonParameters</span></span>
<span data-ttu-id="1fbfe-143">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1fbfe-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fbfe-144">Weitere Informationen finden Sie unter [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1fbfe-144">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fbfe-145">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1fbfe-145">INPUTS</span></span>

### <span data-ttu-id="1fbfe-146">System. String</span><span class="sxs-lookup"><span data-stu-id="1fbfe-146">System.String</span></span>

### <span data-ttu-id="1fbfe-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="1fbfe-147">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="1fbfe-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1fbfe-148">OUTPUTS</span></span>

### <span data-ttu-id="1fbfe-149">System. void</span><span class="sxs-lookup"><span data-stu-id="1fbfe-149">System.Void</span></span>

### <span data-ttu-id="1fbfe-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1fbfe-150">System.Boolean</span></span>

## <span data-ttu-id="1fbfe-151">Notizen</span><span class="sxs-lookup"><span data-stu-id="1fbfe-151">NOTES</span></span>
<span data-ttu-id="1fbfe-152">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="1fbfe-152">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="1fbfe-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1fbfe-153">RELATED LINKS</span></span>

[<span data-ttu-id="1fbfe-154">Anfang-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1fbfe-154">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="1fbfe-155">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1fbfe-155">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="1fbfe-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="1fbfe-156">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="1fbfe-157">Stopp-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="1fbfe-157">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)
