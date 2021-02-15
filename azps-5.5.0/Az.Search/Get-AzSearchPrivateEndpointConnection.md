---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: 3500cf71bb09bec4b204acc0bbf56f185f6ff647
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100174297"
---
# <span data-ttu-id="134e0-101">Get-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="134e0-101">Get-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="134e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="134e0-102">SYNOPSIS</span></span>
<span data-ttu-id="134e0-103">Ruft private Endpunkte mit dem Azure Cognitive Search-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="134e0-103">Gets private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="134e0-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="134e0-104">SYNTAX</span></span>

### <span data-ttu-id="134e0-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="134e0-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="134e0-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="134e0-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ParentObject] <PSSearchService> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="134e0-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="134e0-107">ResourceIdParameterSet</span></span>
```
Get-AzSearchPrivateEndpointConnection [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="134e0-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="134e0-108">DESCRIPTION</span></span>
<span data-ttu-id="134e0-109">Das **Cmdlet "Get-AzSearchPrivateEndpointConnection"** ruft die privaten Endpunktverbindung(en) mit dem Azure Cognitive Search-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="134e0-109">The **Get-AzSearchPrivateEndpointConnection** cmdlet gets the private endpoint connection(s) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="134e0-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="134e0-110">EXAMPLES</span></span>

### <span data-ttu-id="134e0-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="134e0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap

Name                                                          Id
----                                                          --
arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266 /subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266
```

<span data-ttu-id="134e0-112">Das Beispiel ruft alle privaten Endpunktverbindungen mit dem Azure Cognitive Search-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="134e0-112">The example gets all the private endpoint connections to the Azure Cognitive Search service.</span></span>

### <span data-ttu-id="134e0-113">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="134e0-113">Example 2</span></span>
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

<span data-ttu-id="134e0-114">Das Beispiel ruft eine bestimmte private Endpunktverbindung nach Name (zur leichteren Lesbarkeit in JSON konvertiert) zum Azure Cognitive Search-Dienst ab.</span><span class="sxs-lookup"><span data-stu-id="134e0-114">The example gets a specific private endpoint connection by name (converted to JSON for ease of reading) to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="134e0-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="134e0-115">PARAMETERS</span></span>

### <span data-ttu-id="134e0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="134e0-116">-DefaultProfile</span></span>
<span data-ttu-id="134e0-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="134e0-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="134e0-118">-Name</span><span class="sxs-lookup"><span data-stu-id="134e0-118">-Name</span></span>
<span data-ttu-id="134e0-119">Name der privaten Endpunktverbindung von Azure Cognitive Search Service</span><span class="sxs-lookup"><span data-stu-id="134e0-119">Azure Cognitive Search Service private endpoint connection name</span></span>

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

### <span data-ttu-id="134e0-120">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="134e0-120">-ParentObject</span></span>
<span data-ttu-id="134e0-121">Azure Cognitive Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="134e0-121">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="134e0-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="134e0-122">-ResourceGroupName</span></span>
<span data-ttu-id="134e0-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="134e0-123">Resource Group name.</span></span>

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

### <span data-ttu-id="134e0-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="134e0-124">-ResourceId</span></span>
<span data-ttu-id="134e0-125">Ressourcen-ID des privaten Linksdiensts</span><span class="sxs-lookup"><span data-stu-id="134e0-125">Private link service resource id</span></span>

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

### <span data-ttu-id="134e0-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="134e0-126">-ServiceName</span></span>
<span data-ttu-id="134e0-127">Name des Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="134e0-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="134e0-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="134e0-128">-Confirm</span></span>
<span data-ttu-id="134e0-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="134e0-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="134e0-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="134e0-130">-WhatIf</span></span>
<span data-ttu-id="134e0-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="134e0-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="134e0-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="134e0-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="134e0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="134e0-133">CommonParameters</span></span>
<span data-ttu-id="134e0-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="134e0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="134e0-135">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="134e0-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="134e0-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="134e0-136">INPUTS</span></span>

### <span data-ttu-id="134e0-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="134e0-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="134e0-138">System.String</span><span class="sxs-lookup"><span data-stu-id="134e0-138">System.String</span></span>

## <span data-ttu-id="134e0-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="134e0-139">OUTPUTS</span></span>

### <span data-ttu-id="134e0-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="134e0-140">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="134e0-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="134e0-141">NOTES</span></span>

## <span data-ttu-id="134e0-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="134e0-142">RELATED LINKS</span></span>

[<span data-ttu-id="134e0-143">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="134e0-143">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="134e0-144">Set-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="134e0-144">Set-AzSearchPrivateEndpointConnection.md</span></span>](./Set-AzSearchPrivateEndpointConnection.md)
