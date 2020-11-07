---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientconfiguration
schema: 2.0.0
ms.openlocfilehash: 4d6e95534cdadd694fa2ed87d43d3f7387ec9b20
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848771"
---
# <span data-ttu-id="2df26-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="2df26-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="2df26-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2df26-102">SYNOPSIS</span></span>
<span data-ttu-id="2df26-103">Ermöglicht Benutzern das einfache Herunterladen des VPN-Profil Pakets, das mit der New-AzureRmVpnClientConfiguration-Unifiedgroup generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2df26-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2df26-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2df26-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2df26-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2df26-105">DESCRIPTION</span></span>
<span data-ttu-id="2df26-106">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="2df26-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="2df26-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2df26-107">EXAMPLES</span></span>

### <span data-ttu-id="2df26-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2df26-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="2df26-109">Ruft die URL zum Herunterladen eines VpnClient-Profils ab, das zuvor mit dem Befehl New-AzureRMVpnClientConfiguration generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2df26-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="2df26-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2df26-110">PARAMETERS</span></span>

### <span data-ttu-id="2df26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2df26-111">-DefaultProfile</span></span>
<span data-ttu-id="2df26-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2df26-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2df26-113">-Name</span><span class="sxs-lookup"><span data-stu-id="2df26-113">-Name</span></span>
<span data-ttu-id="2df26-114">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="2df26-114">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2df26-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2df26-115">-ResourceGroupName</span></span>
<span data-ttu-id="2df26-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2df26-116">The resource group name.</span></span>

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

### <span data-ttu-id="2df26-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2df26-117">-Confirm</span></span>
<span data-ttu-id="2df26-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2df26-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2df26-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2df26-119">-WhatIf</span></span>
<span data-ttu-id="2df26-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2df26-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2df26-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2df26-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2df26-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2df26-122">CommonParameters</span></span>
<span data-ttu-id="2df26-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2df26-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2df26-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2df26-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2df26-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2df26-125">INPUTS</span></span>

### <span data-ttu-id="2df26-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2df26-126">System.String</span></span>

## <span data-ttu-id="2df26-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2df26-127">OUTPUTS</span></span>

### <span data-ttu-id="2df26-128">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="2df26-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="2df26-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="2df26-129">NOTES</span></span>

## <span data-ttu-id="2df26-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2df26-130">RELATED LINKS</span></span>

