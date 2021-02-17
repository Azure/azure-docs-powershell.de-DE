---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/set-azsearchprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Set-AzSearchPrivateEndpointConnection.md
ms.openlocfilehash: eda4cb403381bd41f7be471b91b2cbba3a6d2ad3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172002"
---
# <span data-ttu-id="c0cb4-101">Set-AzSearchPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c0cb4-101">Set-AzSearchPrivateEndpointConnection</span></span>

## <span data-ttu-id="c0cb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0cb4-102">SYNOPSIS</span></span>
<span data-ttu-id="c0cb4-103">Aktualisieren Sie die Verbindung mit dem privaten Endpunkt mit dem Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="c0cb4-103">Update the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="c0cb4-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c0cb4-104">SYNTAX</span></span>

### <span data-ttu-id="c0cb4-105">ResourceNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="c0cb4-105">ResourceNameParameterSet (Default)</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0cb4-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0cb4-106">ParentObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -ParentObject <PSSearchService> [-Name] <String>
 -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0cb4-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0cb4-107">ResourceIdParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection [-ResourceId] <String> -Status <PSPrivateLinkServiceConnectionStatus>
 [-Description <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0cb4-108">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c0cb4-108">InputObjectParameterSet</span></span>
```
Set-AzSearchPrivateEndpointConnection -Status <PSPrivateLinkServiceConnectionStatus> [-Description <String>]
 -InputObject <PSPrivateEndpointConnection> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0cb4-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c0cb4-109">DESCRIPTION</span></span>
<span data-ttu-id="c0cb4-110">**Set-AzSearchPrivateEndpointConnection** aktualisiert die Verbindung des privaten Endpunkts mit dem Azure Cognitive Search-Dienst.</span><span class="sxs-lookup"><span data-stu-id="c0cb4-110">The **Set-AzSearchPrivateEndpointConnection** updates the private endpoint connection to the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="c0cb4-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c0cb4-111">EXAMPLES</span></span>

### <span data-ttu-id="c0cb4-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c0cb4-112">Example 1</span></span>
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

<span data-ttu-id="c0cb4-113">In diesem Beispiel wird der Status einer Privaten Endpunktverbindung des Azure Cognitive Search-Diensts so aktualisiert, dass er abgelehnt wird.</span><span class="sxs-lookup"><span data-stu-id="c0cb4-113">This example updates a private endpoint connection's status of the Azure Cognitive Search service to be "Rejected".</span></span>

## <span data-ttu-id="c0cb4-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0cb4-114">PARAMETERS</span></span>

### <span data-ttu-id="c0cb4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0cb4-115">-DefaultProfile</span></span>
<span data-ttu-id="c0cb4-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0cb4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0cb4-117">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0cb4-117">-Description</span></span>
<span data-ttu-id="c0cb4-118">Beschreibung der Privaten Endpunktverbindung</span><span class="sxs-lookup"><span data-stu-id="c0cb4-118">Private endpoint connection description</span></span>

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

### <span data-ttu-id="c0cb4-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0cb4-119">-InputObject</span></span>
<span data-ttu-id="c0cb4-120">Eingabeobjekt für private Endpunktverbindung</span><span class="sxs-lookup"><span data-stu-id="c0cb4-120">Private endpoint connection input object</span></span>

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

### <span data-ttu-id="c0cb4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c0cb4-121">-Name</span></span>
<span data-ttu-id="c0cb4-122">Name der privaten Endpunktverbindung von Azure Cognitive Search Service</span><span class="sxs-lookup"><span data-stu-id="c0cb4-122">Azure Cognitive Search Service private endpoint connection name</span></span>

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

### <span data-ttu-id="c0cb4-123">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c0cb4-123">-ParentObject</span></span>
<span data-ttu-id="c0cb4-124">Azure Cognitive Search Service Input Object.</span><span class="sxs-lookup"><span data-stu-id="c0cb4-124">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="c0cb4-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0cb4-125">-ResourceGroupName</span></span>
<span data-ttu-id="c0cb4-126">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c0cb4-126">Resource Group name.</span></span>

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

### <span data-ttu-id="c0cb4-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0cb4-127">-ResourceId</span></span>
<span data-ttu-id="c0cb4-128">Ressourcen-ID des privaten Linksdiensts</span><span class="sxs-lookup"><span data-stu-id="c0cb4-128">Private link service resource id</span></span>

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

### <span data-ttu-id="c0cb4-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c0cb4-129">-ServiceName</span></span>
<span data-ttu-id="c0cb4-130">Name des Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="c0cb4-130">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="c0cb4-131">-Status</span><span class="sxs-lookup"><span data-stu-id="c0cb4-131">-Status</span></span>
<span data-ttu-id="c0cb4-132">Dienstverbindungsstatus für private Verknüpfungen</span><span class="sxs-lookup"><span data-stu-id="c0cb4-132">Private link service connection status</span></span>

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

### <span data-ttu-id="c0cb4-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0cb4-133">-Confirm</span></span>
<span data-ttu-id="c0cb4-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c0cb4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0cb4-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c0cb4-135">-WhatIf</span></span>
<span data-ttu-id="c0cb4-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c0cb4-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0cb4-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0cb4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0cb4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0cb4-138">CommonParameters</span></span>
<span data-ttu-id="c0cb4-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0cb4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0cb4-140">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c0cb4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0cb4-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c0cb4-141">INPUTS</span></span>

### <span data-ttu-id="c0cb4-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c0cb4-142">System.String</span></span>

## <span data-ttu-id="c0cb4-143">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c0cb4-143">OUTPUTS</span></span>

### <span data-ttu-id="c0cb4-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="c0cb4-144">Microsoft.Azure.Commands.Management.Search.Models.PSPrivateEndpointConnection</span></span>

## <span data-ttu-id="c0cb4-145">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c0cb4-145">NOTES</span></span>

## <span data-ttu-id="c0cb4-146">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c0cb4-146">RELATED LINKS</span></span>

[<span data-ttu-id="c0cb4-147">Get-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="c0cb4-147">Get-AzSearchPrivateEndpointConnection.md</span></span>](./Get-AzSearchPrivateEndpointConnection.md)

[<span data-ttu-id="c0cb4-148">Remove-AzSearchPrivateEndpointConnection.md</span><span class="sxs-lookup"><span data-stu-id="c0cb4-148">Remove-AzSearchPrivateEndpointConnection.md</span></span>](./Remove-AzSearchPrivateEndpointConnection.md)
