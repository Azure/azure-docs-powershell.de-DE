---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/stop-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Stop-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 63e78c0068d17986f845adaae9dbc5caf22b4b4d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847095"
---
# <span data-ttu-id="98cab-101">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="98cab-101">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="98cab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="98cab-102">SYNOPSIS</span></span>
<span data-ttu-id="98cab-103">Beendet eine Datenfluss-Debugsitzung in Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="98cab-103">Stops a data flow debug session in Azure Data Factory</span></span>

## <span data-ttu-id="98cab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="98cab-104">SYNTAX</span></span>

### <span data-ttu-id="98cab-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="98cab-105">ByFactoryName (Default)</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="98cab-106">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="98cab-106">ByFactoryObject</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98cab-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="98cab-107">ByResourceId</span></span>
```
Stop-AzDataFactoryV2DataFlowDebugSession [-SessionId] <String> [-PassThru] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98cab-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="98cab-108">DESCRIPTION</span></span>
<span data-ttu-id="98cab-109">Dieser Befehl beendet die Debug-Sitzung, wenn nicht, wird die Sitzung automatisch entsprechend der Uhrzeit für die Live-Einstellung der Debug-Sitzung deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="98cab-109">This command stops the debug session, if not then the session will be automatically turned off according to Time To Live setting of the debug session.</span></span>

## <span data-ttu-id="98cab-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="98cab-110">EXAMPLES</span></span>

### <span data-ttu-id="98cab-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="98cab-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Stop-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF -SessionId fd76cd0d-8b37-4dc0-a370-3f9d43ac686d

Confirm
Are you sure you want to stop data flow debug session 'fd76cd0d-8b37-4dc0-a370-3f9d43ac686d' in data factory 'WikiADF'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
```
<span data-ttu-id="98cab-112">Beendet eine Datenfluss-Debug-Sitzung "fd76cd0d-8b37-4DC0-A370-3f9d43ac686d" in Data Factory "WikiADF"</span><span class="sxs-lookup"><span data-stu-id="98cab-112">Stops a data flow debug session "fd76cd0d-8b37-4dc0-a370-3f9d43ac686d" in data factory "WikiADF"</span></span>

## <span data-ttu-id="98cab-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="98cab-113">PARAMETERS</span></span>

### <span data-ttu-id="98cab-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="98cab-114">-DataFactory</span></span>
<span data-ttu-id="98cab-115">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="98cab-115">The data factory object.</span></span>

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

### <span data-ttu-id="98cab-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="98cab-116">-DataFactoryName</span></span>
<span data-ttu-id="98cab-117">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="98cab-117">The data factory name.</span></span>

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

### <span data-ttu-id="98cab-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98cab-118">-DefaultProfile</span></span>
<span data-ttu-id="98cab-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="98cab-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="98cab-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98cab-120">-PassThru</span></span>
<span data-ttu-id="98cab-121">Wenn angegeben, wird true geschrieben, falls der Vorgang erfolgreich ist.</span><span class="sxs-lookup"><span data-stu-id="98cab-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="98cab-122">Dieser Parameter ist optional.</span><span class="sxs-lookup"><span data-stu-id="98cab-122">This parameter is optional.</span></span>

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

### <span data-ttu-id="98cab-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98cab-123">-ResourceGroupName</span></span>
<span data-ttu-id="98cab-124">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="98cab-124">The resource group name.</span></span>

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

### <span data-ttu-id="98cab-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="98cab-125">-ResourceId</span></span>
<span data-ttu-id="98cab-126">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="98cab-126">The Azure resource ID.</span></span>

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

### <span data-ttu-id="98cab-127">-SessionID</span><span class="sxs-lookup"><span data-stu-id="98cab-127">-SessionId</span></span>
<span data-ttu-id="98cab-128">Die Datenfluss-Debug-Sitzungs-ID.</span><span class="sxs-lookup"><span data-stu-id="98cab-128">The data flow debug session ID.</span></span>

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

### <span data-ttu-id="98cab-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="98cab-129">-Confirm</span></span>
<span data-ttu-id="98cab-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="98cab-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98cab-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98cab-131">-WhatIf</span></span>
<span data-ttu-id="98cab-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="98cab-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98cab-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="98cab-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98cab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98cab-134">CommonParameters</span></span>
<span data-ttu-id="98cab-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98cab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98cab-136">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98cab-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98cab-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="98cab-137">INPUTS</span></span>

### <span data-ttu-id="98cab-138">System. String</span><span class="sxs-lookup"><span data-stu-id="98cab-138">System.String</span></span>

### <span data-ttu-id="98cab-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="98cab-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="98cab-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="98cab-140">OUTPUTS</span></span>

### <span data-ttu-id="98cab-141">System. void</span><span class="sxs-lookup"><span data-stu-id="98cab-141">System.Void</span></span>

### <span data-ttu-id="98cab-142">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="98cab-142">System.Boolean</span></span>

## <span data-ttu-id="98cab-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="98cab-143">NOTES</span></span>
<span data-ttu-id="98cab-144">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="98cab-144">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="98cab-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="98cab-145">RELATED LINKS</span></span>

[<span data-ttu-id="98cab-146">Anfang-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="98cab-146">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="98cab-147">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="98cab-147">Get-AzDataFactoryV2DataFlowDebugSession</span></span>](./Get-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="98cab-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="98cab-148">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="98cab-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="98cab-149">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)