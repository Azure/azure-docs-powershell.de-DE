---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 2b7b6755b15c5dcaf0442557eb32b563f0c1af6e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100172516"
---
# <span data-ttu-id="7c034-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7c034-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="7c034-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c034-102">SYNOPSIS</span></span>
<span data-ttu-id="7c034-103">Entfernt eine private Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="7c034-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="7c034-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="7c034-104">SYNTAX</span></span>

### <span data-ttu-id="7c034-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="7c034-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c034-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="7c034-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c034-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="7c034-107">DESCRIPTION</span></span>
<span data-ttu-id="7c034-108">Das **Cmdlet "Remove-AzPrivateEndpointConnection"** entfernt eine private Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="7c034-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="7c034-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="7c034-109">EXAMPLES</span></span>

### <span data-ttu-id="7c034-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="7c034-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="7c034-111">In diesem Beispiel wird eine private Endpunktverbindung namens "MyPrivateEndpointConnection1" entfernt.</span><span class="sxs-lookup"><span data-stu-id="7c034-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="7c034-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7c034-112">PARAMETERS</span></span>

### <span data-ttu-id="7c034-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7c034-113">-AsJob</span></span>
<span data-ttu-id="7c034-114">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="7c034-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7c034-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c034-115">-DefaultProfile</span></span>
<span data-ttu-id="7c034-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7c034-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7c034-117">-Force</span><span class="sxs-lookup"><span data-stu-id="7c034-117">-Force</span></span>
<span data-ttu-id="7c034-118">Bestätigen Sie nicht, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="7c034-118">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="7c034-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7c034-119">-Name</span></span>
<span data-ttu-id="7c034-120">Der Name der privaten Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="7c034-120">The name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c034-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7c034-121">-PassThru</span></span>
<span data-ttu-id="7c034-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7c034-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7c034-123">Standardmäßig generiert dieses Cmdlet keine Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="7c034-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7c034-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="7c034-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="7c034-125">Der Ressourcentyp für private Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="7c034-125">The private link resource type.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: False
Position: Named
Default value: 'Microsoft.Network/privateLinkServices'
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c034-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c034-126">-ResourceGroupName</span></span>
<span data-ttu-id="7c034-127">Der Ressourcengruppenname der privaten Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="7c034-127">The resource group name of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c034-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7c034-128">-ResourceId</span></span>
<span data-ttu-id="7c034-129">Die Azure-Ressourcen-Manager-ID der privaten Endpunktverbindung.</span><span class="sxs-lookup"><span data-stu-id="7c034-129">The Azure resource manager id of the private endpoint connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c034-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7c034-130">-ServiceName</span></span>
<span data-ttu-id="7c034-131">Der Name des Diensts, dem die private Endpunktverbindung angehört.</span><span class="sxs-lookup"><span data-stu-id="7c034-131">The name of service that the private endpoint connection belong to.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c034-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7c034-132">-Confirm</span></span>
<span data-ttu-id="7c034-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c034-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c034-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="7c034-134">-WhatIf</span></span>
<span data-ttu-id="7c034-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c034-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c034-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c034-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c034-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c034-137">CommonParameters</span></span>
<span data-ttu-id="7c034-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c034-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c034-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7c034-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c034-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="7c034-140">INPUTS</span></span>

### <span data-ttu-id="7c034-141">System.String</span><span class="sxs-lookup"><span data-stu-id="7c034-141">System.String</span></span>

## <span data-ttu-id="7c034-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="7c034-142">OUTPUTS</span></span>

### <span data-ttu-id="7c034-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7c034-143">System.Boolean</span></span>

## <span data-ttu-id="7c034-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="7c034-144">NOTES</span></span>

## <span data-ttu-id="7c034-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="7c034-145">RELATED LINKS</span></span>

[<span data-ttu-id="7c034-146">Approve-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7c034-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7c034-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7c034-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7c034-148">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7c034-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="7c034-149">Set-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="7c034-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
