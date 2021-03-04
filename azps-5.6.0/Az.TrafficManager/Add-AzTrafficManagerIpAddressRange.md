---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: 84d994366c81b7adfc5fa0f7fdb34267ae8b6370
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101918035"
---
# <span data-ttu-id="8ec78-101">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="8ec78-101">Add-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="8ec78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ec78-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec78-103">Fügt einem lokalen Traffic Manager-Endpunktobjekt einen Adressbereich oder ein Subnetz hinzu.</span><span class="sxs-lookup"><span data-stu-id="8ec78-103">Adds an address range or subnet to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="8ec78-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="8ec78-104">SYNTAX</span></span>

```
Add-AzTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8ec78-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="8ec78-105">DESCRIPTION</span></span>
<span data-ttu-id="8ec78-106">Das **Add-AzTrafficManagerIpAddressRange-Cmdlet** fügt einem lokalen Azure Traffic Manager-Endpunktobjekt einen IP-Adressbereich hinzu.</span><span class="sxs-lookup"><span data-stu-id="8ec78-106">The **Add-AzTrafficManagerIpAddressRange** cmdlet adds an IP address range to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="8ec78-107">Sie können einen Endpunkt mithilfe der cmdlets New-AzTrafficManagerEndpoint oder Get-AzTrafficManagerEndpoint erhalten.</span><span class="sxs-lookup"><span data-stu-id="8ec78-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="8ec78-108">Dieses Cmdlet wird für das lokale Endpunktobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="8ec78-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="8ec78-109">Sie können Ihre Änderungen mithilfe des cmdlets "Set-AzTrafficManagerEndpoint" am Endpunkt für Traffic Manager festlegen.</span><span class="sxs-lookup"><span data-stu-id="8ec78-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="8ec78-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="8ec78-110">EXAMPLES</span></span>

### <span data-ttu-id="8ec78-111">Beispiel 1: Hinzufügen von IP-Adressbereichen zu einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="8ec78-111">Example 1: Add IP address ranges to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="8ec78-112">Mit dem ersten Befehl wird ein Azure Traffic Manager-Endpunkt mithilfe des **Cmdlets New-AzTrafficManagerEndpoint** erstellt.</span><span class="sxs-lookup"><span data-stu-id="8ec78-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="8ec78-113">Der Befehl speichert den lokalen Endpunkt in der $TrafficManagerEndpoint Variablen.</span><span class="sxs-lookup"><span data-stu-id="8ec78-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="8ec78-114">Mit dem zweiten Befehl wird der IP-Adressbereich 1.2.3.4 bis 5.6.7.8 dem endpunkt, der in der Datei gespeichert $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8ec78-114">The second command adds the IP address range 1.2.3.4 to 5.6.7.8 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="8ec78-115">Mit dem dritten Befehl wird der IP-Adressbereich 9.10.11.0 bis 9.10.11.255 dem endpunkt, der in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8ec78-115">The third command adds the IP address range 9.10.11.0 to 9.10.11.255 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="8ec78-116">Mit dem vierten Befehl wird überprüft, ob der Bereich der Größe des Bereichs entspricht, und fügt dann dem in $TrafficManagerEndpoint gespeicherten Endpunkt den IP-Adressbereich 12.13.14.0 bis 12.13.14.31 hinzu.</span><span class="sxs-lookup"><span data-stu-id="8ec78-116">The fourth command verifies that the scope matches the size of the range, then adds the IP address range 12.13.14.0 to 12.13.14.31 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="8ec78-117">Mit dem fünften Befehl wird der IP-Adressbereich 15.16.17.18 bis 15.16.17.18 dem endpunkt, der in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8ec78-117">The fifth command adds the IP address range 15.16.17.18 to 15.16.17.18 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="8ec78-118">Der letzte Befehl aktualisiert den Endpunkt in Traffic Manager so, dass er dem lokalen Wert in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="8ec78-118">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="8ec78-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="8ec78-119">PARAMETERS</span></span>

### <span data-ttu-id="8ec78-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec78-120">-DefaultProfile</span></span>
<span data-ttu-id="8ec78-121">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8ec78-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ec78-122">-Last</span><span class="sxs-lookup"><span data-stu-id="8ec78-122">-Last</span></span>
<span data-ttu-id="8ec78-123">Gibt die letzte IP-Adresse im bereich an, der hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ec78-123">Specifies the last IP address in the range to be added.</span></span>

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

### <span data-ttu-id="8ec78-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="8ec78-124">-Scope</span></span>
<span data-ttu-id="8ec78-125">Gibt den Bereich des zu hinzufügenden IP-Adressbereichs an.</span><span class="sxs-lookup"><span data-stu-id="8ec78-125">Specifies the scope of the IP address range to be added.</span></span>

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

### <span data-ttu-id="8ec78-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ec78-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="8ec78-127">Gibt ein lokales **TrafficManagerEndpoint-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="8ec78-127">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="8ec78-128">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="8ec78-128">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="8ec78-129">Um ein **TrafficManagerEndpoint-Objekt zu** erhalten, verwenden Sie das cmdlet Get-AzTrafficManagerEndpoint oder New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ec78-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="8ec78-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8ec78-130">-Confirm</span></span>
<span data-ttu-id="8ec78-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8ec78-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8ec78-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8ec78-132">-WhatIf</span></span>
<span data-ttu-id="8ec78-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8ec78-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8ec78-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8ec78-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8ec78-135">-First</span><span class="sxs-lookup"><span data-stu-id="8ec78-135">-First</span></span>
<span data-ttu-id="8ec78-136">Gibt die erste IP-Adresse im bereich an, der hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="8ec78-136">Specifies the first IP address in the range to be added.</span></span>

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

### <span data-ttu-id="8ec78-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec78-137">CommonParameters</span></span>
<span data-ttu-id="8ec78-138">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ec78-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec78-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ec78-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec78-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="8ec78-140">INPUTS</span></span>

### <span data-ttu-id="8ec78-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ec78-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="8ec78-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="8ec78-142">OUTPUTS</span></span>

### <span data-ttu-id="8ec78-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ec78-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="8ec78-144">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="8ec78-144">NOTES</span></span>

## <span data-ttu-id="8ec78-145">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="8ec78-145">RELATED LINKS</span></span>

[<span data-ttu-id="8ec78-146">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="8ec78-146">Remove-AzTrafficManagerIpAddressRange</span></span>](./Remove-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="8ec78-147">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ec78-147">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8ec78-148">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="8ec78-148">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="8ec78-149">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="8ec78-149">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
