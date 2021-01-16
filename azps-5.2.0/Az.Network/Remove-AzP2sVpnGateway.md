---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: 704a8e0164361c338ac182eef3bf09758eec363b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98291880"
---
# <span data-ttu-id="365cd-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="365cd-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="365cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="365cd-102">SYNOPSIS</span></span>
<span data-ttu-id="365cd-103">Entfernt ein vorhandenes P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="365cd-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="365cd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="365cd-104">SYNTAX</span></span>

### <span data-ttu-id="365cd-105">ByP2SVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="365cd-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="365cd-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="365cd-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="365cd-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="365cd-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="365cd-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="365cd-108">DESCRIPTION</span></span>
<span data-ttu-id="365cd-109">Mit **dem Cmdlet "Remove-AzP2sVpnGateway"** können Sie ein vorhandenes P2SVpnGateway unter VirtualHub entfernen.</span><span class="sxs-lookup"><span data-stu-id="365cd-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="365cd-110">Nach dem Entfernen von P2SVpnGateway kann keine Verbindung mehr zu den Websiteclients verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="365cd-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="365cd-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="365cd-111">EXAMPLES</span></span>

### <span data-ttu-id="365cd-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="365cd-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="365cd-113">Mit **dem Cmdlet "Remove-AzP2sVpnGateway"** können Sie ein vorhandenes P2SVpnGateway unter VirtualHub entfernen.</span><span class="sxs-lookup"><span data-stu-id="365cd-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="365cd-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="365cd-114">PARAMETERS</span></span>

### <span data-ttu-id="365cd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="365cd-115">-DefaultProfile</span></span>
<span data-ttu-id="365cd-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="365cd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365cd-117">-Force</span><span class="sxs-lookup"><span data-stu-id="365cd-117">-Force</span></span>
<span data-ttu-id="365cd-118">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="365cd-118">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365cd-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="365cd-119">-InputObject</span></span>
<span data-ttu-id="365cd-120">Das zu löschende p2sVpnGateway-Objekt.</span><span class="sxs-lookup"><span data-stu-id="365cd-120">The p2sVpnGateway object to be deleted.</span></span>

```yaml
Type: PSP2SVpnGateway
Parameter Sets: ByP2SVpnGatewayObject
Aliases: P2SVpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="365cd-121">-Name</span><span class="sxs-lookup"><span data-stu-id="365cd-121">-Name</span></span>
<span data-ttu-id="365cd-122">Der Name des P2SVpnGateways.</span><span class="sxs-lookup"><span data-stu-id="365cd-122">The P2SVpnGateway name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases: ResourceName, P2SVpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365cd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="365cd-123">-PassThru</span></span>
<span data-ttu-id="365cd-124">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="365cd-124">Returns an object representing the item on which this operation is being performed.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365cd-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="365cd-125">-ResourceGroupName</span></span>
<span data-ttu-id="365cd-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="365cd-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365cd-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="365cd-127">-ResourceId</span></span>
<span data-ttu-id="365cd-128">Die Azure-Ressourcen-ID für das zu löschende p2sVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="365cd-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByP2SVpnGatewayResourceId
Aliases: p2sVpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="365cd-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="365cd-129">-Confirm</span></span>
<span data-ttu-id="365cd-130">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="365cd-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365cd-131">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="365cd-131">-WhatIf</span></span>
<span data-ttu-id="365cd-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="365cd-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="365cd-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="365cd-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="365cd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="365cd-134">CommonParameters</span></span>
<span data-ttu-id="365cd-135">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="365cd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="365cd-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="365cd-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="365cd-137">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="365cd-137">INPUTS</span></span>

### <span data-ttu-id="365cd-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="365cd-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="365cd-139">System.String</span><span class="sxs-lookup"><span data-stu-id="365cd-139">System.String</span></span>

## <span data-ttu-id="365cd-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="365cd-140">OUTPUTS</span></span>

### <span data-ttu-id="365cd-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="365cd-141">System.Boolean</span></span>

## <span data-ttu-id="365cd-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="365cd-142">NOTES</span></span>

## <span data-ttu-id="365cd-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="365cd-143">RELATED LINKS</span></span>
