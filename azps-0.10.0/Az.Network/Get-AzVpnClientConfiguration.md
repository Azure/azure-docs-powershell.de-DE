---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnclientconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzVpnClientConfiguration.md
ms.openlocfilehash: 63b044c4a9736aca72e9713cd8ec5833e7b056ab
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93841484"
---
# <span data-ttu-id="2c5b7-101">Get-AzVpnClientConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c5b7-101">Get-AzVpnClientConfiguration</span></span>

## <span data-ttu-id="2c5b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2c5b7-102">SYNOPSIS</span></span>
<span data-ttu-id="2c5b7-103">Ermöglicht Benutzern das einfache Herunterladen des VPN-Profil Pakets, das mit der New-AzVpnClientConfiguration-Unifiedgroup generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2c5b7-103">Allows users to easily download the Vpn Profile package that was generated using the New-AzVpnClientConfiguration commandlet.</span></span>

## <span data-ttu-id="2c5b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2c5b7-104">SYNTAX</span></span>

```
Get-AzVpnClientConfiguration [-Name <String>] -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c5b7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2c5b7-105">DESCRIPTION</span></span>
<span data-ttu-id="2c5b7-106">{{Fill in the Description}}</span><span class="sxs-lookup"><span data-stu-id="2c5b7-106">{{Fill in the Description}}</span></span>

## <span data-ttu-id="2c5b7-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2c5b7-107">EXAMPLES</span></span>

### <span data-ttu-id="2c5b7-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="2c5b7-108">Example 1</span></span>
```
PS C:\> New-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup" -AuthenticationMethod "EAPTLS" -RadiusRootCert "C:\Users\Test\Desktop\VpnProfileRadiusCert.cer"

PS C:\> Get-AzVpnClientConfiguration -VirtualNetworkGatewayName "ContosoVirtualNetworkGateway" -ResourceGroupName "ContosoResourceGroup"
```

<span data-ttu-id="2c5b7-109">Ruft die URL zum Herunterladen eines VpnClient-Profils ab, das zuvor mit dem Befehl New-AzVpnClientConfiguration generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="2c5b7-109">Gets the URL to download a VpnClient profile that has been previously generated using the New-AzVpnClientConfiguration command.</span></span>

## <span data-ttu-id="2c5b7-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2c5b7-110">PARAMETERS</span></span>

### <span data-ttu-id="2c5b7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c5b7-111">-DefaultProfile</span></span>
<span data-ttu-id="2c5b7-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2c5b7-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
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

### <span data-ttu-id="2c5b7-113">-Name</span><span class="sxs-lookup"><span data-stu-id="2c5b7-113">-Name</span></span>
<span data-ttu-id="2c5b7-114">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="2c5b7-114">The resource name.</span></span>

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

### <span data-ttu-id="2c5b7-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c5b7-115">-ResourceGroupName</span></span>
<span data-ttu-id="2c5b7-116">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="2c5b7-116">The resource group name.</span></span>

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

### <span data-ttu-id="2c5b7-117">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2c5b7-117">-Confirm</span></span>
<span data-ttu-id="2c5b7-118">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2c5b7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c5b7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c5b7-119">-WhatIf</span></span>
<span data-ttu-id="2c5b7-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2c5b7-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c5b7-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2c5b7-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c5b7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c5b7-122">CommonParameters</span></span>
<span data-ttu-id="2c5b7-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c5b7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c5b7-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c5b7-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c5b7-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2c5b7-125">INPUTS</span></span>

### <span data-ttu-id="2c5b7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="2c5b7-126">System.String</span></span>

## <span data-ttu-id="2c5b7-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2c5b7-127">OUTPUTS</span></span>

### <span data-ttu-id="2c5b7-128">Microsoft. Azure. Commands. Network. Models. PSVpnProfile</span><span class="sxs-lookup"><span data-stu-id="2c5b7-128">Microsoft.Azure.Commands.Network.Models.PSVpnProfile</span></span>

## <span data-ttu-id="2c5b7-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="2c5b7-129">NOTES</span></span>

## <span data-ttu-id="2c5b7-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2c5b7-130">RELATED LINKS</span></span>

