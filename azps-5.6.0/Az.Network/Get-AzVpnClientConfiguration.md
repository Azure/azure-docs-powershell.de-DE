---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: 03ed4fe9ad6e8b2e7c5af0b24e29c351a2b776f4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947827"
---
# <span data-ttu-id="797d5-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="797d5-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="797d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="797d5-102">SYNOPSIS</span></span>
<span data-ttu-id="797d5-103">Ermöglicht Benutzern das einfache Herunterladen des Vpn-Profilpakets, das mithilfe des New-AzVpnClientConfiguration generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="797d5-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="797d5-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="797d5-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="797d5-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="797d5-105">DESCRIPTION</span></span>
<span data-ttu-id="797d5-106">Die Get-AzVpnClientConfiguration gibt die URL zurück, aus der der VPN-Client heruntergeladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="797d5-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="797d5-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="797d5-107">EXAMPLES</span></span>

### <span data-ttu-id="797d5-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="797d5-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="797d5-109">Ruft die URL ab, um ein VpnClient-Profil herunterzuladen, das zuvor mithilfe des Befehls New-AzVpnClientConfiguration wurde.</span><span class="sxs-lookup"><span data-stu-id="797d5-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="797d5-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="797d5-110">PARAMETERS</span></span>

### <span data-ttu-id="797d5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="797d5-111">-DefaultProfile</span></span>
<span data-ttu-id="797d5-112">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="797d5-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="797d5-113">-Name</span><span class="sxs-lookup"><span data-stu-id="797d5-113">-Name</span></span>
<span data-ttu-id="797d5-114">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="797d5-114">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="797d5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="797d5-115">-ResourceGroupName</span></span>
<span data-ttu-id="797d5-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="797d5-116">The resource group name.</span></span>

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

### <span data-ttu-id="797d5-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="797d5-117">-Confirm</span></span>
<span data-ttu-id="797d5-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="797d5-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="797d5-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="797d5-119">-WhatIf</span></span>
<span data-ttu-id="797d5-120">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="797d5-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="797d5-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="797d5-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="797d5-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="797d5-122">CommonParameters</span></span>
<span data-ttu-id="797d5-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="797d5-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="797d5-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="797d5-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="797d5-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="797d5-125">INPUTS</span></span>

### <span data-ttu-id="797d5-126">System.String</span><span class="sxs-lookup"><span data-stu-id="797d5-126">System.String</span></span>

## <span data-ttu-id="797d5-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="797d5-127">OUTPUTS</span></span>

### <span data-ttu-id="797d5-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="797d5-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="797d5-129">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="797d5-129">NOTES</span></span>

## <span data-ttu-id="797d5-130">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="797d5-130">RELATED LINKS</span></span>

[<span data-ttu-id="797d5-131">New-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="797d5-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)
