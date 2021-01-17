---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: 5d4fa487210b732e0121a01f7cc5fa392ebfb68c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98385145"
---
# <span data-ttu-id="c3753-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3753-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="c3753-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3753-102">SYNOPSIS</span></span>
<span data-ttu-id="c3753-103">Entfernt eine vorhandene VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c3753-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="c3753-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c3753-104">SYNTAX</span></span>

### <span data-ttu-id="c3753-105">ByVpnServerConfigurationName (Standard)</span><span class="sxs-lookup"><span data-stu-id="c3753-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3753-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="c3753-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3753-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="c3753-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3753-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c3753-108">DESCRIPTION</span></span>
<span data-ttu-id="c3753-109">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="c3753-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="c3753-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c3753-110">EXAMPLES</span></span>

### <span data-ttu-id="c3753-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="c3753-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="c3753-112">Mit dem oben angegebenen Befehl wird eine vorhandene VpnServerConfiguration entfernt.</span><span class="sxs-lookup"><span data-stu-id="c3753-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="c3753-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c3753-113">PARAMETERS</span></span>

### <span data-ttu-id="c3753-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3753-114">-DefaultProfile</span></span>
<span data-ttu-id="c3753-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3753-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c3753-116">-Force</span><span class="sxs-lookup"><span data-stu-id="c3753-116">-Force</span></span>
<span data-ttu-id="c3753-117">Fordern Sie keine Bestätigung an.</span><span class="sxs-lookup"><span data-stu-id="c3753-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="c3753-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c3753-118">-InputObject</span></span>
<span data-ttu-id="c3753-119">Das zu löschende vpnServerConfiguration-Objekt.</span><span class="sxs-lookup"><span data-stu-id="c3753-119">The vpnServerConfiguration object to be deleted.</span></span>

```yaml
Type: PSVpnServerConfiguration
Parameter Sets: ByVpnServerConfigurationObject
Aliases: VpnServerConfiguration

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c3753-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c3753-120">-Name</span></span>
<span data-ttu-id="c3753-121">Der Name der vpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c3753-121">The vpnServerConfiguration name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases: ResourceName, VpnServerConfigurationName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3753-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c3753-122">-PassThru</span></span>
<span data-ttu-id="c3753-123">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3753-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="c3753-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3753-124">-ResourceGroupName</span></span>
<span data-ttu-id="c3753-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="c3753-125">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3753-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c3753-126">-ResourceId</span></span>
<span data-ttu-id="c3753-127">Die Azure-Ressourcen-ID für die zu löschende vpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="c3753-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByVpnServerConfigurationResourceId
Aliases: VpnServerConfigurationId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c3753-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c3753-128">-Confirm</span></span>
<span data-ttu-id="c3753-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c3753-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3753-130">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c3753-130">-WhatIf</span></span>
<span data-ttu-id="c3753-131">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c3753-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c3753-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c3753-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3753-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3753-133">CommonParameters</span></span>
<span data-ttu-id="c3753-134">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3753-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3753-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3753-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3753-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c3753-136">INPUTS</span></span>

### <span data-ttu-id="c3753-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="c3753-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="c3753-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c3753-138">System.String</span></span>

## <span data-ttu-id="c3753-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c3753-139">OUTPUTS</span></span>

### <span data-ttu-id="c3753-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="c3753-140">System.Boolean</span></span>

## <span data-ttu-id="c3753-141">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c3753-141">NOTES</span></span>

## <span data-ttu-id="c3753-142">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c3753-142">RELATED LINKS</span></span>
