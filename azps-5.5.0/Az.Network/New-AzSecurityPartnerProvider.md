---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 5af78bb1f915dec55f75749296340ca6d13a3b3d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100146849"
---
# <span data-ttu-id="fbaa3-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="fbaa3-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="fbaa3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbaa3-102">SYNOPSIS</span></span>
<span data-ttu-id="fbaa3-103">Erstellt einen Azure SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="fbaa3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="fbaa3-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fbaa3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="fbaa3-105">DESCRIPTION</span></span>
<span data-ttu-id="fbaa3-106">Das **Cmdlet "New-AzSecurityPartnerProvider"** erstellt einen Azure SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="fbaa3-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="fbaa3-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="fbaa3-107">EXAMPLES</span></span>

### <span data-ttu-id="fbaa3-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="fbaa3-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="fbaa3-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbaa3-109">PARAMETERS</span></span>

### <span data-ttu-id="fbaa3-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fbaa3-110">-AsJob</span></span>
<span data-ttu-id="fbaa3-111">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="fbaa3-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fbaa3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbaa3-112">-DefaultProfile</span></span>
<span data-ttu-id="fbaa3-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fbaa3-114">-Force</span><span class="sxs-lookup"><span data-stu-id="fbaa3-114">-Force</span></span>
<span data-ttu-id="fbaa3-115">Bestätigen Sie nicht, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="fbaa3-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="fbaa3-116">-Location</span><span class="sxs-lookup"><span data-stu-id="fbaa3-116">-Location</span></span>
<span data-ttu-id="fbaa3-117">aus.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-117">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbaa3-118">-Name</span><span class="sxs-lookup"><span data-stu-id="fbaa3-118">-Name</span></span>
<span data-ttu-id="fbaa3-119">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-119">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbaa3-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fbaa3-120">-ResourceGroupName</span></span>
<span data-ttu-id="fbaa3-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbaa3-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="fbaa3-122">-SecurityProviderName</span></span>
<span data-ttu-id="fbaa3-123">Der Name des Sicherheitsanbieters</span><span class="sxs-lookup"><span data-stu-id="fbaa3-123">The Security Provider name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ZScaler, IBoss, Checkpoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbaa3-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="fbaa3-124">-Tag</span></span>
<span data-ttu-id="fbaa3-125">Eine Hashtable, die Ressourcentags darstellt.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbaa3-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="fbaa3-126">-VirtualHub</span></span>
<span data-ttu-id="fbaa3-127">Die virtuelle Hub-ID, an die der Sicherheitspartneranbieter angefügt ist</span><span class="sxs-lookup"><span data-stu-id="fbaa3-127">The virtual hub Id that the security partner provider is attached to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fbaa3-128">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="fbaa3-128">-VirtualHubId</span></span>
<span data-ttu-id="fbaa3-129">Die ID des VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fbaa3-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="fbaa3-130">-VirtualHubName</span></span>
<span data-ttu-id="fbaa3-131">Die ID des VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="fbaa3-132">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fbaa3-132">-Confirm</span></span>
<span data-ttu-id="fbaa3-133">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fbaa3-134">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="fbaa3-134">-WhatIf</span></span>
<span data-ttu-id="fbaa3-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fbaa3-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fbaa3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbaa3-137">CommonParameters</span></span>
<span data-ttu-id="fbaa3-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbaa3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbaa3-139">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbaa3-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbaa3-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="fbaa3-140">INPUTS</span></span>

### <span data-ttu-id="fbaa3-141">System.String</span><span class="sxs-lookup"><span data-stu-id="fbaa3-141">System.String</span></span>

### <span data-ttu-id="fbaa3-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="fbaa3-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="fbaa3-143">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fbaa3-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fbaa3-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="fbaa3-144">OUTPUTS</span></span>

### <span data-ttu-id="fbaa3-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="fbaa3-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="fbaa3-146">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="fbaa3-146">NOTES</span></span>

## <span data-ttu-id="fbaa3-147">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="fbaa3-147">RELATED LINKS</span></span>
