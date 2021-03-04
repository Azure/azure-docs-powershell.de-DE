---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 35acbbaeb4983def89711049fc3284a63611bbec
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930256"
---
# <span data-ttu-id="b9eca-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b9eca-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="b9eca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b9eca-102">SYNOPSIS</span></span>
<span data-ttu-id="b9eca-103">Alle aktiven Datenflussdebuggersitzungen von Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="b9eca-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="b9eca-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="b9eca-104">SYNTAX</span></span>

### <span data-ttu-id="b9eca-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="b9eca-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b9eca-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="b9eca-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b9eca-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="b9eca-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b9eca-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b9eca-108">DESCRIPTION</span></span>
<span data-ttu-id="b9eca-109">Listen Sie alle aktiven Datenflussdebuggersitzungen von Azure Data Factory mit Details auf.</span><span class="sxs-lookup"><span data-stu-id="b9eca-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="b9eca-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="b9eca-110">EXAMPLES</span></span>

### <span data-ttu-id="b9eca-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="b9eca-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="b9eca-112">Alle aktiven Datenflussdebuggersitzungen in Azure Data Factory "WikiADF" erhalten.</span><span class="sxs-lookup"><span data-stu-id="b9eca-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="b9eca-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="b9eca-113">PARAMETERS</span></span>

### <span data-ttu-id="b9eca-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="b9eca-114">-DataFactory</span></span>
<span data-ttu-id="b9eca-115">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="b9eca-115">The data factory object.</span></span>

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

### <span data-ttu-id="b9eca-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="b9eca-116">-DataFactoryName</span></span>
<span data-ttu-id="b9eca-117">Der Name der Datenfabrik.</span><span class="sxs-lookup"><span data-stu-id="b9eca-117">The data factory name.</span></span>

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

### <span data-ttu-id="b9eca-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9eca-118">-DefaultProfile</span></span>
<span data-ttu-id="b9eca-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b9eca-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b9eca-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b9eca-120">-ResourceGroupName</span></span>
<span data-ttu-id="b9eca-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="b9eca-121">The resource group name.</span></span>

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

### <span data-ttu-id="b9eca-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b9eca-122">-ResourceId</span></span>
<span data-ttu-id="b9eca-123">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="b9eca-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="b9eca-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9eca-124">CommonParameters</span></span>
<span data-ttu-id="b9eca-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9eca-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9eca-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b9eca-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9eca-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="b9eca-127">INPUTS</span></span>

### <span data-ttu-id="b9eca-128">System.String</span><span class="sxs-lookup"><span data-stu-id="b9eca-128">System.String</span></span>

### <span data-ttu-id="b9eca-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="b9eca-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="b9eca-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="b9eca-130">OUTPUTS</span></span>

### <span data-ttu-id="b9eca-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span><span class="sxs-lookup"><span data-stu-id="b9eca-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="b9eca-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="b9eca-132">NOTES</span></span>
<span data-ttu-id="b9eca-133">Schlüsselwörter: azure, azurerm, arm, resource, management, manager, data, factory</span><span class="sxs-lookup"><span data-stu-id="b9eca-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="b9eca-134">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="b9eca-134">RELATED LINKS</span></span>

[<span data-ttu-id="b9eca-135">Start-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b9eca-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="b9eca-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="b9eca-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="b9eca-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="b9eca-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="b9eca-138">Stop-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="b9eca-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)