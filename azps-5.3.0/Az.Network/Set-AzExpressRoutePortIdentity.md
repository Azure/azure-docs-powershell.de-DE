---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressrouteportidentity
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRoutePortIdentity.md
ms.openlocfilehash: af04f3540aaf0ec90432c3b1262b45ef9ef1c2cd
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98472168"
---
# <span data-ttu-id="df8e1-101">Set-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="df8e1-101">Set-AzExpressRoutePortIdentity</span></span>

## <span data-ttu-id="df8e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df8e1-102">SYNOPSIS</span></span>
<span data-ttu-id="df8e1-103">Aktualisiert eine einem ExpressRoutePort zugewiesene Identität.</span><span class="sxs-lookup"><span data-stu-id="df8e1-103">Updates a identity assigned to an ExpressRoutePort.</span></span>

## <span data-ttu-id="df8e1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="df8e1-104">SYNTAX</span></span>

```
Set-AzExpressRoutePortIdentity -ExpressRoutePort <PSExpressRoutePort> -UserAssignedIdentityId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="df8e1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="df8e1-105">DESCRIPTION</span></span>
<span data-ttu-id="df8e1-106">Das **Cmdlet Set-AzExpressRoutePortIdentity** aktualisiert ein lokales Azure ExpressRoutePort-Objekt.</span><span class="sxs-lookup"><span data-stu-id="df8e1-106">The **Set-AzExpressRoutePortIdentity** cmdlet updates a local Azure ExpressRoutePort object.</span></span> <span data-ttu-id="df8e1-107">Verwenden **Sie Set-AzExpressRoutePort,** um es ExpressRoutePort zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="df8e1-107">Use **Set-AzExpressRoutePort** to assign it to ExpressRoutePort.</span></span>

## <span data-ttu-id="df8e1-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="df8e1-108">EXAMPLES</span></span>

### <span data-ttu-id="df8e1-109">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="df8e1-109">Example 1</span></span>
```powershell
PS C:\>$exrport = Get-AzExpressRoutePort -Name $portName -ResourceGroupName $rgName
PS C:\>$identity = New-AzUserAssignedIdentity -Name $identityName -ResourceGroupName $rgName -Location $location
PS C:\>$exrPortIdentity = Set-AzExpressRoutePortIdentity -UserAssignedIdentity $identity.Id -ExpressRoutePort $exrPort
PS C:\>$updatedExrPort = Set-AzExpressRoutePort -ExpressRoutePort $exrPort
```

## <span data-ttu-id="df8e1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="df8e1-110">PARAMETERS</span></span>

### <span data-ttu-id="df8e1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df8e1-111">-DefaultProfile</span></span>
<span data-ttu-id="df8e1-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="df8e1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df8e1-113">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="df8e1-113">-ExpressRoutePort</span></span>
<span data-ttu-id="df8e1-114">The ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="df8e1-114">The ExpressRoutePort</span></span>

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

### <span data-ttu-id="df8e1-115">-UserAssignedIdentityId</span><span class="sxs-lookup"><span data-stu-id="df8e1-115">-UserAssignedIdentityId</span></span>
<span data-ttu-id="df8e1-116">ResourceId der Benutzeridentität, die ExpressRoutePort zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="df8e1-116">ResourceId of the user assigned identity to be assigned to ExpressRoutePort.</span></span>

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

### <span data-ttu-id="df8e1-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="df8e1-117">-Confirm</span></span>
<span data-ttu-id="df8e1-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="df8e1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df8e1-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="df8e1-119">-WhatIf</span></span>
<span data-ttu-id="df8e1-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="df8e1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df8e1-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="df8e1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df8e1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df8e1-122">CommonParameters</span></span>
<span data-ttu-id="df8e1-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df8e1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df8e1-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df8e1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df8e1-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="df8e1-125">INPUTS</span></span>

### <span data-ttu-id="df8e1-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="df8e1-126">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="df8e1-127">System.String</span><span class="sxs-lookup"><span data-stu-id="df8e1-127">System.String</span></span>

## <span data-ttu-id="df8e1-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="df8e1-128">OUTPUTS</span></span>

### <span data-ttu-id="df8e1-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="df8e1-129">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="df8e1-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="df8e1-130">NOTES</span></span>

## <span data-ttu-id="df8e1-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="df8e1-131">RELATED LINKS</span></span>
[<span data-ttu-id="df8e1-132">Get-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="df8e1-132">Get-AzExpressRoutePortIdentity</span></span>](./Get-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="df8e1-133">New-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="df8e1-133">New-AzExpressRoutePortIdentity</span></span>](./New-AzExpressRoutePortIdentity.md)

[<span data-ttu-id="df8e1-134">Remove-AzExpressRoutePortIdentity</span><span class="sxs-lookup"><span data-stu-id="df8e1-134">Remove-AzExpressRoutePortIdentity</span></span>](./Remove-AzExpressRoutePortIdentity.md)
