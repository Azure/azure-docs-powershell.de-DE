---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvpnserverconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnServerConfiguration.md
ms.openlocfilehash: f5451b2c3af331f0086f39f46028aff1d33bf002
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938019"
---
# <span data-ttu-id="747ae-101">Remove-AzVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="747ae-101">Remove-AzVpnServerConfiguration</span></span>

## <span data-ttu-id="747ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="747ae-102">SYNOPSIS</span></span>
<span data-ttu-id="747ae-103">Entfernt eine vorhandene VpnServerConfiguration.</span><span class="sxs-lookup"><span data-stu-id="747ae-103">Removes an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="747ae-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="747ae-104">SYNTAX</span></span>

### <span data-ttu-id="747ae-105">ByVpnServerConfigurationName (Standard)</span><span class="sxs-lookup"><span data-stu-id="747ae-105">ByVpnServerConfigurationName (Default)</span></span>
```
Remove-AzVpnServerConfiguration -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="747ae-106">ByVpnServerConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="747ae-106">ByVpnServerConfigurationObject</span></span>
```
Remove-AzVpnServerConfiguration -InputObject <PSVpnServerConfiguration> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="747ae-107">ByVpnServerConfigurationResourceId</span><span class="sxs-lookup"><span data-stu-id="747ae-107">ByVpnServerConfigurationResourceId</span></span>
```
Remove-AzVpnServerConfiguration -ResourceId <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="747ae-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="747ae-108">DESCRIPTION</span></span>
<span data-ttu-id="747ae-109">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="747ae-109">{{Fill in the Description}}</span></span>

## <span data-ttu-id="747ae-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="747ae-110">EXAMPLES</span></span>

### <span data-ttu-id="747ae-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="747ae-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzVpnServerConfiguration -Name "test1config" -ResourceGroupName "P2SCortexGATesting" -Force -PassThru
```

<span data-ttu-id="747ae-112">Mit dem obigen Befehl wird eine vorhandene VpnServerConfiguration entfernt.</span><span class="sxs-lookup"><span data-stu-id="747ae-112">The above command will remove an existing VpnServerConfiguration.</span></span>

## <span data-ttu-id="747ae-113">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="747ae-113">PARAMETERS</span></span>

### <span data-ttu-id="747ae-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="747ae-114">-DefaultProfile</span></span>
<span data-ttu-id="747ae-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="747ae-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="747ae-116">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="747ae-116">-Force</span></span>
<span data-ttu-id="747ae-117">Bitten Sie nicht um Bestätigung.</span><span class="sxs-lookup"><span data-stu-id="747ae-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="747ae-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="747ae-118">-InputObject</span></span>
<span data-ttu-id="747ae-119">Das zu löschende vpnServerConfiguration-Objekt.</span><span class="sxs-lookup"><span data-stu-id="747ae-119">The vpnServerConfiguration object to be deleted.</span></span>

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

### <span data-ttu-id="747ae-120">-Name</span><span class="sxs-lookup"><span data-stu-id="747ae-120">-Name</span></span>
<span data-ttu-id="747ae-121">Der VpnServerConfiguration-Name.</span><span class="sxs-lookup"><span data-stu-id="747ae-121">The vpnServerConfiguration name.</span></span>

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

### <span data-ttu-id="747ae-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="747ae-122">-PassThru</span></span>
<span data-ttu-id="747ae-123">Gibt ein Objekt zurück, das das Element darstellt, für das dieser Vorgang ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="747ae-123">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="747ae-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="747ae-124">-ResourceGroupName</span></span>
<span data-ttu-id="747ae-125">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="747ae-125">The resource group name.</span></span>

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

### <span data-ttu-id="747ae-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="747ae-126">-ResourceId</span></span>
<span data-ttu-id="747ae-127">Die Azure-Ressourcen-ID für die vpnServerConfiguration, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="747ae-127">The Azure resource ID for the vpnServerConfiguration to be deleted.</span></span>

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

### <span data-ttu-id="747ae-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="747ae-128">-Confirm</span></span>
<span data-ttu-id="747ae-129">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="747ae-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="747ae-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="747ae-130">-WhatIf</span></span>
<span data-ttu-id="747ae-131">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="747ae-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="747ae-132">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="747ae-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="747ae-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="747ae-133">CommonParameters</span></span>
<span data-ttu-id="747ae-134">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="747ae-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="747ae-135">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="747ae-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="747ae-136">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="747ae-136">INPUTS</span></span>

### <span data-ttu-id="747ae-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="747ae-137">Microsoft.Azure.Commands.Network.Models.PSVpnServerConfiguration</span></span>
<span data-ttu-id="747ae-138">System.String</span><span class="sxs-lookup"><span data-stu-id="747ae-138">System.String</span></span>

## <span data-ttu-id="747ae-139">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="747ae-139">OUTPUTS</span></span>

### <span data-ttu-id="747ae-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="747ae-140">System.Boolean</span></span>

## <span data-ttu-id="747ae-141">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="747ae-141">NOTES</span></span>

## <span data-ttu-id="747ae-142">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="747ae-142">RELATED LINKS</span></span>
