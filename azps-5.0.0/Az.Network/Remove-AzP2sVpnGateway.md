---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azp2svpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzP2sVpnGateway.md
ms.openlocfilehash: 704a8e0164361c338ac182eef3bf09758eec363b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303646"
---
# <span data-ttu-id="4c16c-101">Remove-AzP2sVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4c16c-101">Remove-AzP2sVpnGateway</span></span>

## <span data-ttu-id="4c16c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4c16c-102">SYNOPSIS</span></span>
<span data-ttu-id="4c16c-103">Entfernt eine vorhandene P2SVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="4c16c-103">Removes an existing P2SVpnGateway.</span></span>

## <span data-ttu-id="4c16c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4c16c-104">SYNTAX</span></span>

### <span data-ttu-id="4c16c-105">ByP2SVpnGatewayName (Standard)</span><span class="sxs-lookup"><span data-stu-id="4c16c-105">ByP2SVpnGatewayName (Default)</span></span>
```
Remove-AzP2sVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c16c-106">ByP2SVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="4c16c-106">ByP2SVpnGatewayObject</span></span>
```
Remove-AzP2sVpnGateway -InputObject <PSP2SVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c16c-107">ByP2SVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="4c16c-107">ByP2SVpnGatewayResourceId</span></span>
```
Remove-AzP2sVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c16c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c16c-108">DESCRIPTION</span></span>
<span data-ttu-id="4c16c-109">Mit dem Cmdlet **Remove-AzP2sVpnGateway** können Sie ein vorhandenes P2SVpnGateway unter VirtualHub entfernen.</span><span class="sxs-lookup"><span data-stu-id="4c16c-109">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span> <span data-ttu-id="4c16c-110">Alle Punkte für die Konnektivität der Website Clients können nach dem Entfernen von P2SVpnGateway nicht mehr ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4c16c-110">All the point to site clients connectivity will fail after P2SVpnGateway is removed.</span></span>

## <span data-ttu-id="4c16c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4c16c-111">EXAMPLES</span></span>

### <span data-ttu-id="4c16c-112">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4c16c-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzP2sVpnGateway -Name 683482ade8564515aed4b8448c9757ea-westus-gw-ResourceGroupName P2SCortexGATesting -Force -PassThru
```

<span data-ttu-id="4c16c-113">Mit dem Cmdlet **Remove-AzP2sVpnGateway** können Sie ein vorhandenes P2SVpnGateway unter VirtualHub entfernen.</span><span class="sxs-lookup"><span data-stu-id="4c16c-113">The **Remove-AzP2sVpnGateway** cmdlet enables you to remove an existing P2SVpnGateway under VirtualHub.</span></span>

## <span data-ttu-id="4c16c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="4c16c-114">PARAMETERS</span></span>

### <span data-ttu-id="4c16c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c16c-115">-DefaultProfile</span></span>
<span data-ttu-id="4c16c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="4c16c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c16c-117">-Force</span><span class="sxs-lookup"><span data-stu-id="4c16c-117">-Force</span></span>
<span data-ttu-id="4c16c-118">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="4c16c-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="4c16c-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4c16c-119">-InputObject</span></span>
<span data-ttu-id="4c16c-120">Das p2sVpnGateway-Objekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c16c-120">The p2sVpnGateway object to be deleted.</span></span>

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

### <span data-ttu-id="4c16c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4c16c-121">-Name</span></span>
<span data-ttu-id="4c16c-122">Der P2SVpnGateway-Name.</span><span class="sxs-lookup"><span data-stu-id="4c16c-122">The P2SVpnGateway name.</span></span>

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

### <span data-ttu-id="4c16c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c16c-123">-PassThru</span></span>
<span data-ttu-id="4c16c-124">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c16c-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="4c16c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c16c-125">-ResourceGroupName</span></span>
<span data-ttu-id="4c16c-126">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="4c16c-126">The resource group name.</span></span>

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

### <span data-ttu-id="4c16c-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="4c16c-127">-ResourceId</span></span>
<span data-ttu-id="4c16c-128">Die Azure-Ressourcen-ID für die p2sVpnGateway, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="4c16c-128">The Azure resource ID for the p2sVpnGateway to be deleted.</span></span>

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

### <span data-ttu-id="4c16c-129">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4c16c-129">-Confirm</span></span>
<span data-ttu-id="4c16c-130">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4c16c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c16c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c16c-131">-WhatIf</span></span>
<span data-ttu-id="4c16c-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c16c-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c16c-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4c16c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c16c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c16c-134">CommonParameters</span></span>
<span data-ttu-id="4c16c-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c16c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c16c-136">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c16c-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c16c-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4c16c-137">INPUTS</span></span>

### <span data-ttu-id="4c16c-138">Microsoft. Azure. Commands. Network. Models. PSP2SVpnGateway</span><span class="sxs-lookup"><span data-stu-id="4c16c-138">Microsoft.Azure.Commands.Network.Models.PSP2SVpnGateway</span></span>
<span data-ttu-id="4c16c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4c16c-139">System.String</span></span>

## <span data-ttu-id="4c16c-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4c16c-140">OUTPUTS</span></span>

### <span data-ttu-id="4c16c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="4c16c-141">System.Boolean</span></span>

## <span data-ttu-id="4c16c-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="4c16c-142">NOTES</span></span>

## <span data-ttu-id="4c16c-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4c16c-143">RELATED LINKS</span></span>
