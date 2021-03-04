---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: 6292c2fd19ff61e347291d3aba7e9840799e3b93
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101930896"
---
# <span data-ttu-id="4a080-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4a080-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="4a080-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a080-102">SYNOPSIS</span></span>
<span data-ttu-id="4a080-103">Aktualisiert eine identität, die einem ExpressRoutePort zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="4a080-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="4a080-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="4a080-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a080-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a080-105">DESCRIPTION</span></span>
<span data-ttu-id="4a080-106">Das **Cmdlet Set-AzExpressRoutePortIdentity** aktualisiert ein lokales Azure ExpressRoutePort-Objekt.</span><span class="sxs-lookup"><span data-stu-id="4a080-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="4a080-107">Verwenden **Sie Set-AzExpressRoutePort,** um ihn ExpressRoutePort zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="4a080-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="4a080-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="4a080-108">EXAMPLES</span></span>

### <span data-ttu-id="4a080-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="4a080-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="4a080-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="4a080-110">PARAMETERS</span></span>

### <span data-ttu-id="4a080-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a080-111">-DefaultProfile</span></span>
<span data-ttu-id="4a080-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="4a080-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4a080-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4a080-113">-ExpressRoutePort</span></span>
<span data-ttu-id="4a080-114">Der ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4a080-114">The ExpressRoutePort</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4a080-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="4a080-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="4a080-116">ResourceId des Benutzers, dem die Identität zugewiesen wurde, die ExpressRoutePort zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="4a080-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: UserAssignedIdentity

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4a080-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4a080-117">-Confirm</span></span>
<span data-ttu-id="4a080-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4a080-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4a080-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4a080-119">-WhatIf</span></span>
<span data-ttu-id="4a080-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4a080-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4a080-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4a080-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4a080-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a080-122">CommonParameters</span></span>
<span data-ttu-id="4a080-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4a080-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a080-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a080-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a080-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="4a080-125">INPUTS</span></span>

### <span data-ttu-id="4a080-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4a080-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="4a080-127">System.String</span><span class="sxs-lookup"><span data-stu-id="4a080-127">System.String</span></span>

## <span data-ttu-id="4a080-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="4a080-128">OUTPUTS</span></span>

### <span data-ttu-id="4a080-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="4a080-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="4a080-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="4a080-130">NOTES</span></span>

## <span data-ttu-id="4a080-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="4a080-131">RELATED LINKS</span></span>
[<span data-ttu-id="4a080-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4a080-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="4a080-133">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4a080-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="4a080-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="4a080-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
