---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnClientConfiguration.md
ms.openlocfilehash: 09c3862513b893003908b07992ae479656ba7ab1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505449"
---
# <span data-ttu-id="8a589-101">Get-AzureRmVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="8a589-101">Get-AzureRmVpnClientConfiguration</span></span>

## <span data-ttu-id="8a589-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8a589-102">SYNOPSIS</span></span>
<span data-ttu-id="8a589-103">Ermöglicht Benutzern das einfache Herunterladen des VPN-Profil Pakets, das mit der New-AzureRmVpnClientConfiguration-Unifiedgroup generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8a589-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzureRmVpnClientConfiguration commandlet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a589-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8a589-104">SYNTAX</span></span>

```
Get-AzureRmVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a589-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8a589-105">DESCRIPTION</span></span>
<span data-ttu-id="8a589-106">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="8a589-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="8a589-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8a589-107">EXAMPLES</span></span>

### <span data-ttu-id="8a589-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="8a589-108">Example 1</span></span>
```
PS C:\> New-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzureRmVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="8a589-109">Ruft die URL zum Herunterladen eines VpnClient-Profils ab, das zuvor mit dem Befehl New-AzureRMVpnClientConfiguration generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="8a589-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzureRMVpnClientConfiguration command.</span></span>

## <span data-ttu-id="8a589-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="8a589-110">PARAMETERS</span></span>

### <span data-ttu-id="8a589-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a589-111">-DefaultProfile</span></span>
<span data-ttu-id="8a589-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8a589-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="8a589-113">-Name</span><span class="sxs-lookup"><span data-stu-id="8a589-113">-Name</span></span>
<span data-ttu-id="8a589-114">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="8a589-114">The resource name.</span></span>

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

### <span data-ttu-id="8a589-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8a589-115">-ResourceGroupName</span></span>
<span data-ttu-id="8a589-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="8a589-116">The resource group name.</span></span>

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

### <span data-ttu-id="8a589-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8a589-117">-Confirm</span></span>
<span data-ttu-id="8a589-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8a589-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a589-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a589-119">-WhatIf</span></span>
<span data-ttu-id="8a589-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8a589-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8a589-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8a589-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a589-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a589-122">CommonParameters</span></span>
<span data-ttu-id="8a589-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a589-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a589-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a589-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a589-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8a589-125">INPUTS</span></span>

### <span data-ttu-id="8a589-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8a589-126">System.String</span></span>

## <span data-ttu-id="8a589-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8a589-127">OUTPUTS</span></span>

### <span data-ttu-id="8a589-128">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="8a589-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="8a589-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="8a589-129">NOTES</span></span>

## <span data-ttu-id="8a589-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8a589-130">RELATED LINKS</span></span>

