---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnSite.md
ms.openlocfilehash: ac0513b7d411c2c95864aa6f619e80d2373a3554
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93495866"
---
# <span data-ttu-id="3cf2c-101">Remove-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="3cf2c-101">Remove-AzureRmVpnSite</span></span>

## <span data-ttu-id="3cf2c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3cf2c-102">SYNOPSIS</span></span>
<span data-ttu-id="3cf2c-103">Entfernt eine Azure VpnSite-Ressource.</span><span class="sxs-lookup"><span data-stu-id="3cf2c-103">Removes an Azure VpnSite resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cf2c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3cf2c-104">SYNTAX</span></span>

### <span data-ttu-id="3cf2c-105">ByVpnSiteName (Standard)</span><span class="sxs-lookup"><span data-stu-id="3cf2c-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzureRmVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf2c-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="3cf2c-106">ByVpnSiteObject</span></span>
```
Remove-AzureRmVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cf2c-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="3cf2c-107">ByVpnSiteResourceId</span></span>
```
Remove-AzureRmVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cf2c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3cf2c-108">DESCRIPTION</span></span>
<span data-ttu-id="3cf2c-109">Entfernt eine Azure VpnSite-Ressource.</span><span class="sxs-lookup"><span data-stu-id="3cf2c-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="3cf2c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3cf2c-110">EXAMPLES</span></span>

### <span data-ttu-id="3cf2c-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="3cf2c-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="3cf2c-112">Das obige wird eine Ressourcengruppe erstellen, virtuelles WAN in West US in "testRG" Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="3cf2c-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="3cf2c-113">Anschließend wird ein VpnSite erstellt, um einen Kunden Zweig darzustellen und mit dem virtuellen WAN zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="3cf2c-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="3cf2c-114">Nachdem die Website erstellt wurde, wird Sie mit dem Befehl Remove-AzureRmVpnSite sofort entfernt.</span><span class="sxs-lookup"><span data-stu-id="3cf2c-114">Once the site is created, it is immediately removed using the Remove-AzureRmVpnSite command.</span></span>

### <span data-ttu-id="3cf2c-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="3cf2c-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzureRmVpnSite
```

<span data-ttu-id="3cf2c-116">Identisch mit Beispiel 1, aber hier erfolgt die Entfernung mithilfe der geleiteten Ausgabe von Get-AzureRmVpnSite.</span><span class="sxs-lookup"><span data-stu-id="3cf2c-116">Same as example 1 but here the removal happens using the piped output from Get-AzureRmVpnSite.</span></span>

## <span data-ttu-id="3cf2c-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="3cf2c-117">PARAMETERS</span></span>

### <span data-ttu-id="3cf2c-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cf2c-118">-DefaultProfile</span></span>
<span data-ttu-id="3cf2c-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3cf2c-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf2c-120">-Force</span><span class="sxs-lookup"><span data-stu-id="3cf2c-120">-Force</span></span>
<span data-ttu-id="3cf2c-121">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="3cf2c-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf2c-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3cf2c-122">-InputObject</span></span>
<span data-ttu-id="3cf2c-123">Das vpnSite-Objekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="3cf2c-123">The vpnSite object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObject
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3cf2c-124">-Name</span><span class="sxs-lookup"><span data-stu-id="3cf2c-124">-Name</span></span>
<span data-ttu-id="3cf2c-125">Der vpnSite-Name.</span><span class="sxs-lookup"><span data-stu-id="3cf2c-125">The vpnSite name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf2c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3cf2c-126">-PassThru</span></span>
<span data-ttu-id="3cf2c-127">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="3cf2c-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="3cf2c-128">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="3cf2c-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf2c-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cf2c-129">-ResourceGroupName</span></span>
<span data-ttu-id="3cf2c-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="3cf2c-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf2c-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="3cf2c-131">-ResourceId</span></span>
<span data-ttu-id="3cf2c-132">Die Azure-Ressourcen-ID für die vpnSite, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="3cf2c-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceId
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cf2c-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3cf2c-133">-Confirm</span></span>
<span data-ttu-id="3cf2c-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3cf2c-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf2c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cf2c-135">-WhatIf</span></span>
<span data-ttu-id="3cf2c-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3cf2c-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cf2c-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3cf2c-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cf2c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cf2c-138">CommonParameters</span></span>
<span data-ttu-id="3cf2c-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cf2c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cf2c-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cf2c-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cf2c-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3cf2c-141">INPUTS</span></span>

### <span data-ttu-id="3cf2c-142">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="3cf2c-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="3cf2c-143">System. String</span><span class="sxs-lookup"><span data-stu-id="3cf2c-143">System.String</span></span>

## <span data-ttu-id="3cf2c-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3cf2c-144">OUTPUTS</span></span>

### <span data-ttu-id="3cf2c-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3cf2c-145">System.Boolean</span></span>

## <span data-ttu-id="3cf2c-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="3cf2c-146">NOTES</span></span>

## <span data-ttu-id="3cf2c-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3cf2c-147">RELATED LINKS</span></span>
