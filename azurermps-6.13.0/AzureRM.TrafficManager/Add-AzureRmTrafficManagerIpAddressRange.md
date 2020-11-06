---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurermtrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerIpAddressRange.md
ms.openlocfilehash: 213e959ecfec178644246f56be11e5b7306ef07f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93477605"
---
# <span data-ttu-id="73fd2-101">Add-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="73fd2-101">Add-AzureRmTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="73fd2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="73fd2-102">SYNOPSIS</span></span>
<span data-ttu-id="73fd2-103">Fügt einen Adressbereich oder ein Subnetz zu einem Endpunkt Objekt des lokalen Datenverkehrs-Managers hinzu.</span><span class="sxs-lookup"><span data-stu-id="73fd2-103">Adds an address range or subnet to a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="73fd2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="73fd2-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="73fd2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73fd2-105">DESCRIPTION</span></span>
<span data-ttu-id="73fd2-106">Mit dem Cmdlet **Add-AzureRmTrafficManagerIpAddressRange** wird ein IP-Adressbereich zu einem lokalen Azure Traffic Manager-Endpunkt Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="73fd2-106">The **Add-AzureRmTrafficManagerIpAddressRange** cmdlet adds an IP address range to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="73fd2-107">Sie können einen Endpunkt mithilfe der Cmdlets New-AzureRmTrafficManagerEndpoint oder Get-AzureRmTrafficManagerEndpoint abrufen.</span><span class="sxs-lookup"><span data-stu-id="73fd2-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="73fd2-108">Dieses Cmdlet funktioniert für das lokale Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="73fd2-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="73fd2-109">Übernehmen Sie Ihre Änderungen mithilfe des Set-AzureRmTrafficManagerEndpoint-Cmdlets an den Endpunkt des Datenverkehrs-Managers.</span><span class="sxs-lookup"><span data-stu-id="73fd2-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="73fd2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="73fd2-110">EXAMPLES</span></span>

### <span data-ttu-id="73fd2-111">Beispiel 1: Hinzufügen von IP-Adressbereichen zu einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="73fd2-111">Example 1: Add IP address ranges to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzureRmTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="73fd2-112">Der erste Befehl erstellt einen Azure Traffic Manager-Endpunkt mithilfe des Cmdlets **New-AzureRmTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="73fd2-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="73fd2-113">Der Befehl speichert den lokalen Endpunkt in der $TrafficManagerEndpoint-Variablen.</span><span class="sxs-lookup"><span data-stu-id="73fd2-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="73fd2-114">Der zweite Befehl fügt dem in $TrafficManagerEndpoint gespeicherten Endpunkt den IP-Adressbereich 1.2.3.4 zu 5.6.7.8 hinzu.</span><span class="sxs-lookup"><span data-stu-id="73fd2-114">The second command adds the IP address range 1.2.3.4 to 5.6.7.8 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="73fd2-115">Der dritte Befehl fügt dem in $TrafficManagerEndpoint gespeicherten Endpunkt den IP-Adressbereich 9.10.11.0 zu 9.10.11.255 hinzu.</span><span class="sxs-lookup"><span data-stu-id="73fd2-115">The third command adds the IP address range 9.10.11.0 to 9.10.11.255 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="73fd2-116">Der vierte Befehl überprüft, ob der Bereich der Größe des Bereichs entspricht, und fügt dann den IP-Adressbereich 12.13.14.0 zu 12.13.14.31 dem in $TrafficManagerEndpoint gespeicherten Endpunkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="73fd2-116">The fourth command verifies that the scope matches the size of the range, then adds the IP address range 12.13.14.0 to 12.13.14.31 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="73fd2-117">Der fünfte Befehl fügt dem in $TrafficManagerEndpoint gespeicherten Endpunkt den IP-Adressbereich 15.16.17.18 zu 15.16.17.18 hinzu.</span><span class="sxs-lookup"><span data-stu-id="73fd2-117">The fifth command adds the IP address range 15.16.17.18 to 15.16.17.18 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="73fd2-118">Mit dem letzten Befehl wird der Endpunkt im Traffic Manager so aktualisiert, dass er dem lokalen Wert in $TrafficManagerEndpoint entspricht.</span><span class="sxs-lookup"><span data-stu-id="73fd2-118">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="73fd2-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="73fd2-119">PARAMETERS</span></span>

### <span data-ttu-id="73fd2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73fd2-120">-DefaultProfile</span></span>
<span data-ttu-id="73fd2-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="73fd2-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73fd2-122">-Letzte</span><span class="sxs-lookup"><span data-stu-id="73fd2-122">-Last</span></span>
<span data-ttu-id="73fd2-123">Gibt die letzte IP-Adresse im Bereich an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="73fd2-123">Specifies the last IP address in the range to be added.</span></span>

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

### <span data-ttu-id="73fd2-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="73fd2-124">-Scope</span></span>
<span data-ttu-id="73fd2-125">Gibt den Bereich des IP-Adressbereichs an, der hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="73fd2-125">Specifies the scope of the IP address range to be added.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73fd2-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="73fd2-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="73fd2-127">Gibt ein lokales **TrafficManagerEndpoint** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="73fd2-127">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="73fd2-128">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="73fd2-128">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="73fd2-129">Verwenden Sie zum Abrufen eines **TrafficManagerEndpoint** -Objekts das Get-AzureRmTrafficManagerEndpoint-oder New-AzureRmTrafficManagerEndpoint-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73fd2-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="73fd2-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="73fd2-130">-Confirm</span></span>
<span data-ttu-id="73fd2-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="73fd2-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="73fd2-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="73fd2-132">-WhatIf</span></span>
<span data-ttu-id="73fd2-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="73fd2-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="73fd2-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="73fd2-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="73fd2-135">-First</span><span class="sxs-lookup"><span data-stu-id="73fd2-135">-First</span></span>
<span data-ttu-id="73fd2-136">Gibt die erste IP-Adresse im Bereich an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="73fd2-136">Specifies the first IP address in the range to be added.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73fd2-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73fd2-137">CommonParameters</span></span>
<span data-ttu-id="73fd2-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="73fd2-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73fd2-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73fd2-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73fd2-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="73fd2-140">INPUTS</span></span>

### <span data-ttu-id="73fd2-141">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="73fd2-141">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="73fd2-142">Dieses Cmdlet akzeptiert ein **TrafficManagerEndpoint** -Objekt für dieses Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="73fd2-142">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="73fd2-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="73fd2-143">OUTPUTS</span></span>

### <span data-ttu-id="73fd2-144">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="73fd2-144">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="73fd2-145">Dieses Cmdlet gibt ein geändertes **TrafficManagerEndpoint** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="73fd2-145">This cmdlet returns a modified **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="73fd2-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="73fd2-146">NOTES</span></span>

## <span data-ttu-id="73fd2-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="73fd2-147">RELATED LINKS</span></span>

[<span data-ttu-id="73fd2-148">Remove-AzureRmTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="73fd2-148">Remove-AzureRmTrafficManagerIpAddressRange</span></span>](./Remove-AzureRmTrafficManagerIpAddressRange.md)

[<span data-ttu-id="73fd2-149">Neu – AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="73fd2-149">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="73fd2-150">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="73fd2-150">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="73fd2-151">Satz-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="73fd2-151">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
