---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: ba73b61d34e0f6422defb9e9d6f84c22945ec124
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94009125"
---
# <span data-ttu-id="f8bba-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8bba-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="f8bba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f8bba-102">SYNOPSIS</span></span>
<span data-ttu-id="f8bba-103">Ermöglicht Benutzern das einfache Herunterladen des VPN-Profil Pakets, das mit der New-AzVpnClientConfiguration-Unifiedgroup generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f8bba-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="f8bba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f8bba-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f8bba-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f8bba-105">DESCRIPTION</span></span>
<span data-ttu-id="f8bba-106">Die Get-AzVpnClientConfiguration gibt die URL zurück, von der aus der VPN-Client heruntergeladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="f8bba-106">The Get-AzVpnClientConfiguration returns the URL where the VPN client can be downloaded from.</span></span>

## <span data-ttu-id="f8bba-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f8bba-107">EXAMPLES</span></span>

### <span data-ttu-id="f8bba-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="f8bba-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="f8bba-109">Ruft die URL zum Herunterladen eines VpnClient-Profils ab, das zuvor mit dem Befehl New-AzVpnClientConfiguration generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f8bba-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="f8bba-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="f8bba-110">PARAMETERS</span></span>

### <span data-ttu-id="f8bba-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8bba-111">-DefaultProfile</span></span>
<span data-ttu-id="f8bba-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f8bba-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8bba-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f8bba-113">-Name</span></span>
<span data-ttu-id="f8bba-114">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="f8bba-114">The resource name.</span></span>

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

### <span data-ttu-id="f8bba-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f8bba-115">-ResourceGroupName</span></span>
<span data-ttu-id="f8bba-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="f8bba-116">The resource group name.</span></span>

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

### <span data-ttu-id="f8bba-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f8bba-117">-Confirm</span></span>
<span data-ttu-id="f8bba-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f8bba-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f8bba-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f8bba-119">-WhatIf</span></span>
<span data-ttu-id="f8bba-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f8bba-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f8bba-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f8bba-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f8bba-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8bba-122">CommonParameters</span></span>
<span data-ttu-id="f8bba-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f8bba-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8bba-124">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f8bba-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8bba-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f8bba-125">INPUTS</span></span>

### <span data-ttu-id="f8bba-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f8bba-126">System.String</span></span>

## <span data-ttu-id="f8bba-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f8bba-127">OUTPUTS</span></span>

### <span data-ttu-id="f8bba-128">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="f8bba-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="f8bba-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="f8bba-129">NOTES</span></span>

## <span data-ttu-id="f8bba-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f8bba-130">RELATED LINKS</span></span>

[<span data-ttu-id="f8bba-131">Neu – AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="f8bba-131">New-AzVpnClientConfiguration</span></span>](./New-AzVpnClientConfiguration.md)
