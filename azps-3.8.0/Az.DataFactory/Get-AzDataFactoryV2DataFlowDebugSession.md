---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2dataflowdebugsession
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2DataFlowDebugSession.md
ms.openlocfilehash: 951f1b6a03c621e0dd8bc5d559eaf317cfd43a2c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93847304"
---
# <span data-ttu-id="f2097-101">Get-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f2097-101">Get-AzDataFactoryV2DataFlowDebugSession</span></span>

## <span data-ttu-id="f2097-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f2097-102">SYNOPSIS</span></span>
<span data-ttu-id="f2097-103">Abrufen aller aktiven Datenfluss-Debug-Sitzungen nach Azure Data Factory</span><span class="sxs-lookup"><span data-stu-id="f2097-103">Get all active data flow debug sessions by Azure Data Factory</span></span>

## <span data-ttu-id="f2097-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f2097-104">SYNTAX</span></span>

### <span data-ttu-id="f2097-105">ByFactoryName (Standard)</span><span class="sxs-lookup"><span data-stu-id="f2097-105">ByFactoryName (Default)</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f2097-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="f2097-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f2097-107">ByFactoryObject</span><span class="sxs-lookup"><span data-stu-id="f2097-107">ByFactoryObject</span></span>
```
Get-AzDataFactoryV2DataFlowDebugSession [-DataFactory] <PSDataFactory>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f2097-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f2097-108">DESCRIPTION</span></span>
<span data-ttu-id="f2097-109">Auflisten aller aktiven Datenfluss-Debug-Sitzungen nach Azure Data Factory mit Details</span><span class="sxs-lookup"><span data-stu-id="f2097-109">List all active data flow debug sessions by Azure Data Factory with details.</span></span>

## <span data-ttu-id="f2097-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f2097-110">EXAMPLES</span></span>

### <span data-ttu-id="f2097-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f2097-111">Example 1</span></span>
```powershell
PS C:\WINDOWS\system32> Get-AzDataFactoryV2DataFlowDebugSession -ResourceGroupName adf -DataFactoryName WikiADF

SessionId                            ComputeType CoreCount                         StartTime                  LastActivityTime TimeToLiveInMinutes IntegrationRuntimeName                                      DataFlowName
---------                            ----------- ---------                         ---------                  ---------------- ------------------- ----------------------                                      ------------
3c68dbd6-f9c3-4b5f-a200-2310258016a7     General         8 2019-10-04T18:19:58.5550364+00:00 2019-10-04T18:24:51.3680548+00:00                  60                        DebugSession-0a7e0d6e-f2b7-48cc-8cd8-618326f5662f
```

<span data-ttu-id="f2097-112">Rufen Sie alle aktiven Datenfluss-Debug-Sitzungen in Azure Data Factory "WikiADF" ab.</span><span class="sxs-lookup"><span data-stu-id="f2097-112">Get all active data flow debug sessions in Azure Data Factory "WikiADF".</span></span>

## <span data-ttu-id="f2097-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f2097-113">PARAMETERS</span></span>

### <span data-ttu-id="f2097-114">-DataFactory</span><span class="sxs-lookup"><span data-stu-id="f2097-114">-DataFactory</span></span>
<span data-ttu-id="f2097-115">Das Data Factory-Objekt.</span><span class="sxs-lookup"><span data-stu-id="f2097-115">The data factory object.</span></span>

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

### <span data-ttu-id="f2097-116">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="f2097-116">-DataFactoryName</span></span>
<span data-ttu-id="f2097-117">Der Name der Daten Factory.</span><span class="sxs-lookup"><span data-stu-id="f2097-117">The data factory name.</span></span>

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

### <span data-ttu-id="f2097-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2097-118">-DefaultProfile</span></span>
<span data-ttu-id="f2097-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f2097-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2097-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2097-120">-ResourceGroupName</span></span>
<span data-ttu-id="f2097-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f2097-121">The resource group name.</span></span>

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

### <span data-ttu-id="f2097-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f2097-122">-ResourceId</span></span>
<span data-ttu-id="f2097-123">Die Azure-Ressourcen-ID.</span><span class="sxs-lookup"><span data-stu-id="f2097-123">The Azure resource ID.</span></span>

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

### <span data-ttu-id="f2097-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2097-124">CommonParameters</span></span>
<span data-ttu-id="f2097-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2097-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2097-126">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f2097-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2097-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f2097-127">INPUTS</span></span>

### <span data-ttu-id="f2097-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f2097-128">System.String</span></span>

### <span data-ttu-id="f2097-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="f2097-129">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="f2097-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f2097-130">OUTPUTS</span></span>

### <span data-ttu-id="f2097-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span><span class="sxs-lookup"><span data-stu-id="f2097-131">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFlowDebugSessionInfo</span></span>

## <span data-ttu-id="f2097-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="f2097-132">NOTES</span></span>
<span data-ttu-id="f2097-133">Schlüsselwörter: Azure, azurerm, arm, Resource, Verwaltung, Manager, Daten, Factorys</span><span class="sxs-lookup"><span data-stu-id="f2097-133">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="f2097-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f2097-134">RELATED LINKS</span></span>

[<span data-ttu-id="f2097-135">Anfang-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f2097-135">Start-AzDataFactoryV2DataFlowDebugSession</span></span>](./Start-AzDataFactoryV2DataFlowDebugSession.md)

[<span data-ttu-id="f2097-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span><span class="sxs-lookup"><span data-stu-id="f2097-136">Add-AzDataFactoryV2DataFlowDebugSessionPackage</span></span>](./Add-AzDataFactoryV2DataFlowDebugSessionPackage.md)

[<span data-ttu-id="f2097-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span><span class="sxs-lookup"><span data-stu-id="f2097-137">Invoke-AzDataFactoryV2DataFlowDebugSessionCommand</span></span>](./Invoke-AzDataFactoryV2DataFlowDebugSessionCommand.md)

[<span data-ttu-id="f2097-138">Stopp-AzDataFactoryV2DataFlowDebugSession</span><span class="sxs-lookup"><span data-stu-id="f2097-138">Stop-AzDataFactoryV2DataFlowDebugSession</span></span>](./Stop-AzDataFactoryV2DataFlowDebugSession.md)