---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azprivateendpointconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzPrivateEndpointConnection.md
ms.openlocfilehash: 2b7b6755b15c5dcaf0442557eb32b563f0c1af6e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166247"
---
# <span data-ttu-id="a3485-101">Remove-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a3485-101">Remove-AzPrivateEndpointConnection</span></span>

## <span data-ttu-id="a3485-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a3485-102">SYNOPSIS</span></span>
<span data-ttu-id="a3485-103">Entfernt eine private Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="a3485-103">Removes a private endpoint connection.</span></span>

## <span data-ttu-id="a3485-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a3485-104">SYNTAX</span></span>

### <span data-ttu-id="a3485-105">ByResourceId (Standard)</span><span class="sxs-lookup"><span data-stu-id="a3485-105">ByResourceId (Default)</span></span>
```
Remove-AzPrivateEndpointConnection -ResourceId <String>
 [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a3485-106">ByResource</span><span class="sxs-lookup"><span data-stu-id="a3485-106">ByResource</span></span>
```
Remove-AzPrivateEndpointConnection -Name <String> -ServiceName <String> -ResourceGroupName <String>
 [-PrivateLinkResourceType <String>] [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a3485-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a3485-107">DESCRIPTION</span></span>
<span data-ttu-id="a3485-108">Das Cmdlet " **Remove-AzPrivateEndpointConnection** " entfernt eine private Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="a3485-108">The **Remove-AzPrivateEndpointConnection** cmdlet removes a private endpoint connection.</span></span>

## <span data-ttu-id="a3485-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a3485-109">EXAMPLES</span></span>

### <span data-ttu-id="a3485-110">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a3485-110">Example 1</span></span>
```
Remove-AzPrivateEndpointConnection -Name MyPrivateEndpointConnection1 -ResourceGroupName TestResourceGroup -ServiceName MyPrivateLinkServiceName
```

<span data-ttu-id="a3485-111">In diesem Beispiel wird eine private Endpunkt Verbindung mit dem Namen MyPrivateEndpointConnection1 entfernt</span><span class="sxs-lookup"><span data-stu-id="a3485-111">This example remove a private endpoint connection named MyPrivateEndpointConnection1</span></span>

## <span data-ttu-id="a3485-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3485-112">PARAMETERS</span></span>

### <span data-ttu-id="a3485-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a3485-113">-AsJob</span></span>
<span data-ttu-id="a3485-114">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="a3485-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a3485-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3485-115">-DefaultProfile</span></span>
<span data-ttu-id="a3485-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="a3485-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3485-117">-Force</span><span class="sxs-lookup"><span data-stu-id="a3485-117">-Force</span></span>
<span data-ttu-id="a3485-118">Keine Bestätigung anfordern, wenn Sie eine Ressource löschen möchten</span><span class="sxs-lookup"><span data-stu-id="a3485-118">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="a3485-119">-Name</span><span class="sxs-lookup"><span data-stu-id="a3485-119">-Name</span></span>
<span data-ttu-id="a3485-120">Der Name der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="a3485-120">The name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="a3485-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a3485-121">-PassThru</span></span>
<span data-ttu-id="a3485-122">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="a3485-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a3485-123">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="a3485-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a3485-124">-PrivateLinkResourceType</span><span class="sxs-lookup"><span data-stu-id="a3485-124">-PrivateLinkResourceType</span></span>
<span data-ttu-id="a3485-125">Der Ressourcentyp "privater Link".</span><span class="sxs-lookup"><span data-stu-id="a3485-125">The private link resource type.</span></span>

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

### <span data-ttu-id="a3485-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a3485-126">-ResourceGroupName</span></span>
<span data-ttu-id="a3485-127">Der Ressourcengruppenname der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="a3485-127">The resource group name of the private endpoint connection.</span></span>

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

### <span data-ttu-id="a3485-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="a3485-128">-ResourceId</span></span>
<span data-ttu-id="a3485-129">Die Azure Resource Manager-ID der privaten Endpunkt Verbindung.</span><span class="sxs-lookup"><span data-stu-id="a3485-129">The Azure resource manager id of the private endpoint connection.</span></span>

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

### <span data-ttu-id="a3485-130">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a3485-130">-ServiceName</span></span>
<span data-ttu-id="a3485-131">Der Name des Diensts, zu dem die private Endpunkt Verbindung gehört.</span><span class="sxs-lookup"><span data-stu-id="a3485-131">The name of service that the private endpoint connection belong to.</span></span>

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

### <span data-ttu-id="a3485-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a3485-132">-Confirm</span></span>
<span data-ttu-id="a3485-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a3485-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a3485-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a3485-134">-WhatIf</span></span>
<span data-ttu-id="a3485-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a3485-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a3485-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a3485-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a3485-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3485-137">CommonParameters</span></span>
<span data-ttu-id="a3485-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a3485-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3485-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a3485-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3485-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a3485-140">INPUTS</span></span>

### <span data-ttu-id="a3485-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a3485-141">System.String</span></span>

## <span data-ttu-id="a3485-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a3485-142">OUTPUTS</span></span>

### <span data-ttu-id="a3485-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a3485-143">System.Boolean</span></span>

## <span data-ttu-id="a3485-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="a3485-144">NOTES</span></span>

## <span data-ttu-id="a3485-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a3485-145">RELATED LINKS</span></span>

[<span data-ttu-id="a3485-146">Genehmigen – AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a3485-146">Approve-AzPrivateEndpointConnection</span></span>](./Approve-AzPrivateEndpointConnection.md)

[<span data-ttu-id="a3485-147">Deny-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a3485-147">Deny-AzPrivateEndpointConnection</span></span>](./Deny-AzPrivateEndpointConnection.md)

[<span data-ttu-id="a3485-148">Get-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a3485-148">Get-AzPrivateEndpointConnection</span></span>](./Get-AzPrivateEndpointConnection.md)

[<span data-ttu-id="a3485-149">Satz-AzPrivateEndpointConnection</span><span class="sxs-lookup"><span data-stu-id="a3485-149">Set-AzPrivateEndpointConnection</span></span>](./Set-AzPrivateEndpointConnection.md)
