---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/set-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: d67108e935d4f3ef14522f792a06f975d98be803
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101928891"
---
# <span data-ttu-id="5bc49-101">Set-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5bc49-101">Set-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="5bc49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bc49-102">SYNOPSIS</span></span>
<span data-ttu-id="5bc49-103">Aktualisieren Sie die private Endpunktverbindung mit dem Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="5bc49-103">Update the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="5bc49-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5bc49-104">SYNTAX</span></span>

### <span data-ttu-id="5bc49-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="5bc49-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bc49-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bc49-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bc49-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bc49-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceId] <String> -Status <PSPrivateLinkServiceConnectionStatus>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5bc49-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5bc49-108">InputObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 -InputObject <PSPrivateEndpointConnection> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5bc49-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5bc49-109">DESCRIPTION</span></span>
<span data-ttu-id="5bc49-110">Die **Set-AzSearchPrivateEndpointConnection** aktualisiert die private Endpunktverbindung mit dem Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="5bc49-110">The **Set-AzSearchPrivateEndpointConnection** updates the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="5bc49-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5bc49-111">EXAMPLES</span></span>

### <span data-ttu-id="5bc49-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="5bc49-112">Example 1</span></span>
```powershell
PS C:\> Set-AzSearchPrivateEndpointConnection -ResourceGroupName arjagann -ServiceName arjagann-test-cuseuap -Name arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266 -Status Rejected  -Description "Rejected" | ConvertTo-Json

{
  "Name": "arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann/providers/Microsoft.Search/searchServices/arjagann-test-cuseuap/privateEndpointConnections/arjagann-test-cuseuap-pe.4c74dd7c-7016-42ac-827a-8d5d1378f266",
  "PrivateEndpoint": {
    "Id": "/subscriptions/a4337210-c6b0-4de4-907a-688f1c120d9a/resourceGroups/arjagann2/providers/Microsoft.Network/privateEndpoints/arjagann-test-cuseuap-pe"
  },
  "PrivateLinkServiceConnectionState": {
    "Status": 2,
    "Description": "Rejected",
    "ActionsRequired": "None"
  }
}
```

<span data-ttu-id="5bc49-113">In diesem Beispiel wird der Status einer privaten Endpunktverbindung des Azure Cognitive Search-Diensts auf "Abgelehnt" aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="5bc49-113">This example updates a private endpoint connection's status of the Azure Cognitive Search service to be "Rejected".</span></span>

## <span data-ttu-id="5bc49-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5bc49-114">PARAMETERS</span></span>

### <span data-ttu-id="5bc49-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5bc49-115">-DefaultProfile</span></span>
<span data-ttu-id="5bc49-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5bc49-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5bc49-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5bc49-117">-Description</span></span>
<span data-ttu-id="5bc49-118">Beschreibung der Privaten Endpunktverbindung</span><span class="sxs-lookup"><span data-stu-id="5bc49-118">Private endpoint connection description</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc49-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5bc49-119">-InputObject</span></span>
<span data-ttu-id="5bc49-120">Eingabeobjekt für private Endpunktverbindung</span><span class="sxs-lookup"><span data-stu-id="5bc49-120">Private endpoint connection input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc49-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5bc49-121">-Name</span></span>
<span data-ttu-id="5bc49-122">Name der privaten Azure Cognitive Search Service-Verbindung</span><span class="sxs-lookup"><span data-stu-id="5bc49-122">Azure Cognitive Search Service private endpoint connection name</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet, ParentObjectParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc49-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="5bc49-123">-ParentObject</span></span>
<span data-ttu-id="5bc49-124">Azure Cognitive Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="5bc49-124">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bc49-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bc49-125">-ResourceGroupName</span></span>
<span data-ttu-id="5bc49-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5bc49-126">Resource Group name.</span></span>

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

### <span data-ttu-id="5bc49-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5bc49-127">-ResourceId</span></span>
<span data-ttu-id="5bc49-128">Private Link Service Resource ID</span><span class="sxs-lookup"><span data-stu-id="5bc49-128">Private link service resource id</span></span>

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

### <span data-ttu-id="5bc49-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5bc49-129">-ServiceName</span></span>
<span data-ttu-id="5bc49-130">Name des Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="5bc49-130">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="5bc49-131">-Status</span><span class="sxs-lookup"><span data-stu-id="5bc49-131">-Status</span></span>
<span data-ttu-id="5bc49-132">Verbindungsstatus des privaten Linkdiensts</span><span class="sxs-lookup"><span data-stu-id="5bc49-132">Private link service connection status</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSPrivateLinkServiceConnectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Pending, Approved, Rejected, Disconnected

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bc49-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5bc49-133">-Confirm</span></span>
<span data-ttu-id="5bc49-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5bc49-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5bc49-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bc49-135">-WhatIf</span></span>
<span data-ttu-id="5bc49-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5bc49-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bc49-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5bc49-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5bc49-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bc49-138">CommonParameters</span></span>
<span data-ttu-id="5bc49-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5bc49-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bc49-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5bc49-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bc49-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5bc49-141">INPUTS</span></span>

### <span data-ttu-id="5bc49-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5bc49-142">System.String</span></span>

## <span data-ttu-id="5bc49-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5bc49-143">OUTPUTS</span></span>

### <span data-ttu-id="5bc49-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="5bc49-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="5bc49-145">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5bc49-145">NOTES</span></span>

## <span data-ttu-id="5bc49-146">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5bc49-146">RELATED LINKS</span></span>

[<span data-ttu-id="5bc49-147">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="5bc49-147">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="5bc49-148">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="5bc49-148">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)
