---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 2b7b6755b15c5dcaf0442557eb32b563f0c1af6e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94004212"
---
# <span data-ttu-id="9a497-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9a497-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="9a497-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9a497-102">SYNOPSIS</span></span>
<span data-ttu-id="9a497-103">Entfernt eine private Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="9a497-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="9a497-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9a497-104">SYNTAX</span></span>

### <span data-ttu-id="9a497-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="9a497-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a497-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="9a497-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9a497-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a497-107">DESCRIPTION</span></span>
<span data-ttu-id="9a497-108">Das Cmdlet " **Remove-AzPrivateEndpointConnection** " entfernt eine private Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="9a497-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="9a497-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9a497-109">EXAMPLES</span></span>

### <span data-ttu-id="9a497-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="9a497-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="9a497-111">In diesem Beispiel wird eine private Endpunkt Verbindung mit dem Namen MyPrivateEndpointConnection1 entfernt</span><span class="sxs-lookup"><span data-stu-id="9a497-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="9a497-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a497-112">PARAMETERS</span></span>

### <span data-ttu-id="9a497-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a497-113">-AsJob</span></span>
<span data-ttu-id="9a497-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="9a497-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a497-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a497-115">-DefaultProfile</span></span>
<span data-ttu-id="9a497-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="9a497-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a497-117">-Force</span><span class="sxs-lookup"><span data-stu-id="9a497-117">-Force</span></span>
<span data-ttu-id="9a497-118">Keine Bestätigung anfordern, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="9a497-118">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="9a497-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9a497-119">-Name</span></span>
<span data-ttu-id="9a497-120">Der Name der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="9a497-120">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="9a497-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a497-121">-PassThru</span></span>
<span data-ttu-id="9a497-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="9a497-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9a497-123">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="9a497-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9a497-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="9a497-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="9a497-125">Der Ressourcentyp "privater Link".</span><span class="sxs-lookup"><span data-stu-id="9a497-125">The private link resource type.</span></span>

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

### <span data-ttu-id="9a497-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a497-126">-ResourceGroupName</span></span>
<span data-ttu-id="9a497-127">Der Ressourcengruppenname der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="9a497-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="9a497-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9a497-128">-ResourceId</span></span>
<span data-ttu-id="9a497-129">Die Azure Resource Manager-ID der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="9a497-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="9a497-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9a497-130">-ServiceName</span></span>
<span data-ttu-id="9a497-131">Der Name des Diensts, zu dem die private Endpunkt Verbindung gehört.</span><span class="sxs-lookup"><span data-stu-id="9a497-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="9a497-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9a497-132">-Confirm</span></span>
<span data-ttu-id="9a497-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9a497-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a497-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a497-134">-WhatIf</span></span>
<span data-ttu-id="9a497-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a497-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a497-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a497-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a497-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a497-137">CommonParameters</span></span>
<span data-ttu-id="9a497-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a497-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a497-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9a497-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a497-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9a497-140">INPUTS</span></span>

### <span data-ttu-id="9a497-141">System. String</span><span class="sxs-lookup"><span data-stu-id="9a497-141">System.String</span></span>

## <span data-ttu-id="9a497-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9a497-142">OUTPUTS</span></span>

### <span data-ttu-id="9a497-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9a497-143">System.Boolean</span></span>

## <span data-ttu-id="9a497-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="9a497-144">NOTES</span></span>

## <span data-ttu-id="9a497-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9a497-145">RELATED LINKS</span></span>

[<span data-ttu-id="9a497-146">Genehmigen – AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9a497-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9a497-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9a497-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9a497-148">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9a497-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="9a497-149">Satz-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="9a497-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
