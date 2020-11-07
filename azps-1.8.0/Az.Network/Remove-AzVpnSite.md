---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
ms.openlocfilehash: 0215a05db7e18dad9aeb26476d7076bdc556b021
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93660289"
---
# <span data-ttu-id="896de-101">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="896de-101">Remove-AzVpnSite</span></span>

## <span data-ttu-id="896de-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="896de-102">SYNOPSIS</span></span>
<span data-ttu-id="896de-103">Entfernt eine Azure VpnSite-Ressource.</span><span class="sxs-lookup"><span data-stu-id="896de-103">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="896de-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="896de-104">SYNTAX</span></span>

### <span data-ttu-id="896de-105">ByVpnSiteName (Standard)</span><span class="sxs-lookup"><span data-stu-id="896de-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="896de-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="896de-106">ByVpnSiteObject</span></span>
```
Remove-AzVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="896de-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="896de-107">ByVpnSiteResourceId</span></span>
```
Remove-AzVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="896de-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="896de-108">DESCRIPTION</span></span>
<span data-ttu-id="896de-109">Entfernt eine Azure VpnSite-Ressource.</span><span class="sxs-lookup"><span data-stu-id="896de-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="896de-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="896de-110">EXAMPLES</span></span>

### <span data-ttu-id="896de-111">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="896de-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="896de-112">Das obige wird eine Ressourcengruppe erstellen, virtuelles WAN in West US in "testRG" Ressourcengruppe in Azure.</span><span class="sxs-lookup"><span data-stu-id="896de-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="896de-113">Anschließend wird ein VpnSite erstellt, um einen Kunden Zweig darzustellen und mit dem virtuellen WAN zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="896de-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="896de-114">Nachdem die Website erstellt wurde, wird Sie mit dem Befehl Remove-AzVpnSite sofort entfernt.</span><span class="sxs-lookup"><span data-stu-id="896de-114">Once the site is created, it is immediately removed using the Remove-AzVpnSite command.</span></span>

### <span data-ttu-id="896de-115">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="896de-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzVpnSite
```

<span data-ttu-id="896de-116">Identisch mit Beispiel 1, aber hier erfolgt die Entfernung mithilfe der geleiteten Ausgabe von Get-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="896de-116">Same as example 1 but here the removal happens using the piped output from Get-AzVpnSite.</span></span>

## <span data-ttu-id="896de-117">Parameter</span><span class="sxs-lookup"><span data-stu-id="896de-117">PARAMETERS</span></span>

### <span data-ttu-id="896de-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="896de-118">-DefaultProfile</span></span>
<span data-ttu-id="896de-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="896de-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="896de-120">-Force</span><span class="sxs-lookup"><span data-stu-id="896de-120">-Force</span></span>
<span data-ttu-id="896de-121">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="896de-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="896de-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="896de-122">-InputObject</span></span>
<span data-ttu-id="896de-123">Das vpnSite-Objekt, das gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="896de-123">The vpnSite object to be deleted.</span></span>

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

### <span data-ttu-id="896de-124">-Name</span><span class="sxs-lookup"><span data-stu-id="896de-124">-Name</span></span>
<span data-ttu-id="896de-125">Der vpnSite-Name.</span><span class="sxs-lookup"><span data-stu-id="896de-125">The vpnSite name.</span></span>

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

### <span data-ttu-id="896de-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="896de-126">-PassThru</span></span>
<span data-ttu-id="896de-127">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="896de-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="896de-128">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="896de-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="896de-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="896de-129">-ResourceGroupName</span></span>
<span data-ttu-id="896de-130">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="896de-130">The resource group name.</span></span>

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

### <span data-ttu-id="896de-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="896de-131">-ResourceId</span></span>
<span data-ttu-id="896de-132">Die Azure-Ressourcen-ID für die vpnSite, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="896de-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

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

### <span data-ttu-id="896de-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="896de-133">-Confirm</span></span>
<span data-ttu-id="896de-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="896de-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="896de-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="896de-135">-WhatIf</span></span>
<span data-ttu-id="896de-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="896de-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="896de-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="896de-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="896de-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="896de-138">CommonParameters</span></span>
<span data-ttu-id="896de-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="896de-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="896de-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="896de-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="896de-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="896de-141">INPUTS</span></span>

### <span data-ttu-id="896de-142">Microsoft. Azure. Commands. Network. Models. PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="896de-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="896de-143">System. String</span><span class="sxs-lookup"><span data-stu-id="896de-143">System.String</span></span>

## <span data-ttu-id="896de-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="896de-144">OUTPUTS</span></span>

### <span data-ttu-id="896de-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="896de-145">System.Boolean</span></span>

## <span data-ttu-id="896de-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="896de-146">NOTES</span></span>

## <span data-ttu-id="896de-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="896de-147">RELATED LINKS</span></span>

[<span data-ttu-id="896de-148">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="896de-148">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="896de-149">Neu – AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="896de-149">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="896de-150">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="896de-150">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
