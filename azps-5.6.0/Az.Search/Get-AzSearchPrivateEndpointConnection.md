---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/get-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 0ed07bed894d31be68b8fd4b71605e94b19171ab
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101943505"
---
# <span data-ttu-id="f6214-101">Get-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f6214-101">Get-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="f6214-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6214-102">SYNOPSIS</span></span>
<span data-ttu-id="f6214-103">Ruft private Endpunktverbindung(n) mit dem Azure Cognitive Search-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="f6214-103">Gets private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="f6214-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f6214-104">SYNTAX</span></span>

### <span data-ttu-id="f6214-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="f6214-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6214-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6214-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6214-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6214-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6214-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f6214-108">DESCRIPTION</span></span>
<span data-ttu-id="f6214-109">Das **Get-AzSearchPrivateEndpointConnection-Cmdlet** ruft die privaten Endpunktverbindung(n) mit dem Azure Cognitive Search-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="f6214-109">The **Get-AzSearchPrivateEndpointConnection** cmdlet gets the private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="f6214-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f6214-110">EXAMPLES</span></span>

### <span data-ttu-id="f6214-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f6214-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap

Name                                                          Id
----                                                          --
arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266 /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="f6214-112">Das Beispiel ruft alle privaten Endpunktverbindungen mit dem Azure Cognitive Search-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="f6214-112">The example gets all the private endpoint connections to the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="f6214-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="f6214-113">Example 2</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266  | ConvertTo-Json

{
  "Name": "arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "PrivateEndpoint": {
    "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann2/providers/Microsoft.Network/privateEndpoints/arjagann-test-cuseuap-pe"
  },
  "PrivateLinkServiceConnectionState": {
    "Status": 1,
    "Description": "Auto-approved",
    "ActionsRequired": "None"
  }
}
```

<span data-ttu-id="f6214-114">Im Beispiel wird eine bestimmte private Endpunktverbindung nach Name (zur einfacheren Lesbarkeit in JSON konvertiert) zum Azure Cognitive Search-Dienst bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="f6214-114">The example gets a specific private endpoint connection by name (converted to JSON for ease of reading) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="f6214-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f6214-115">PARAMETERS</span></span>

### <span data-ttu-id="f6214-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6214-116">-DefaultProfile</span></span>
<span data-ttu-id="f6214-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f6214-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6214-118">-Name</span><span class="sxs-lookup"><span data-stu-id="f6214-118">-Name</span></span>
<span data-ttu-id="f6214-119">Name der privaten Azure Cognitive Search Service-Verbindung</span><span class="sxs-lookup"><span data-stu-id="f6214-119">Azure Cognitive Search Service private endpoint connection name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6214-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="f6214-120">-ParentObject</span></span>
<span data-ttu-id="f6214-121">Azure Cognitive Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="f6214-121">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6214-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6214-122">-ResourceGroupName</span></span>
<span data-ttu-id="f6214-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f6214-123">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6214-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f6214-124">-ResourceId</span></span>
<span data-ttu-id="f6214-125">Private Link Service Resource ID</span><span class="sxs-lookup"><span data-stu-id="f6214-125">Private link service resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f6214-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="f6214-126">-ServiceName</span></span>
<span data-ttu-id="f6214-127">Name des Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="f6214-127">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6214-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f6214-128">-Confirm</span></span>
<span data-ttu-id="f6214-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f6214-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6214-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6214-130">-WhatIf</span></span>
<span data-ttu-id="f6214-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6214-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6214-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f6214-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6214-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6214-133">CommonParameters</span></span>
<span data-ttu-id="f6214-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6214-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6214-135">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f6214-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6214-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f6214-136">INPUTS</span></span>

### <span data-ttu-id="f6214-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="f6214-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="f6214-138">System.String</span><span class="sxs-lookup"><span data-stu-id="f6214-138">System.String</span></span>

## <span data-ttu-id="f6214-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f6214-139">OUTPUTS</span></span>

### <span data-ttu-id="f6214-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="f6214-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="f6214-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f6214-141">NOTES</span></span>

## <span data-ttu-id="f6214-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f6214-142">RELATED LINKS</span></span>

[<span data-ttu-id="f6214-143">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="f6214-143">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="f6214-144">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="f6214-144">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)
