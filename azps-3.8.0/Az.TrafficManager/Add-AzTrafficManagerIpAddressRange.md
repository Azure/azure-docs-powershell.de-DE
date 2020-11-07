---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: 2cececec0610b813bf59a1ef8adac59e1fa8ddb2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93845368"
---
# <span data-ttu-id="145f3-101">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="145f3-101">Add-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="145f3-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="145f3-102">SYNOPSIS</span></span>
<span data-ttu-id="145f3-103">Fügt einen Adressbereich oder ein Subnetz zu einem Endpunkt Objekt des lokalen Datenverkehrs-Managers hinzu.</span><span class="sxs-lookup"><span data-stu-id="145f3-103">Adds an address range or subnet to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="145f3-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="145f3-104">SYNTAX</span></span>

```
Add-AzTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="145f3-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="145f3-105">DESCRIPTION</span></span>
<span data-ttu-id="145f3-106">Mit dem Cmdlet **Add-AzTrafficManagerIpAddressRange** wird ein IP-Adressbereich zu einem lokalen Azure Traffic Manager-Endpunkt Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="145f3-106">The **Add-AzTrafficManagerIpAddressRange** cmdlet adds an IP address range to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="145f3-107">Sie können einen Endpunkt mithilfe der Cmdlets New-AzTrafficManagerEndpoint oder Get-AzTrafficManagerEndpoint abrufen.</span><span class="sxs-lookup"><span data-stu-id="145f3-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="145f3-108">Dieses Cmdlet funktioniert für das lokale Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="145f3-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="145f3-109">Übernehmen Sie Ihre Änderungen mithilfe des Set-AzTrafficManagerEndpoint-Cmdlets an den Endpunkt des Datenverkehrs-Managers.</span><span class="sxs-lookup"><span data-stu-id="145f3-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="145f3-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="145f3-110">EXAMPLES</span></span>

### <span data-ttu-id="145f3-111">Beispiel 1: Hinzufügen von IP-Adressbereichen zu einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="145f3-111">Example 1: Add IP address ranges to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="145f3-112">Der erste Befehl erstellt einen Azure Traffic Manager-Endpunkt mithilfe des Cmdlets **New-AzTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="145f3-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="145f3-113">Der Befehl speichert den lokalen Endpunkt in der $TrafficManagerEndpoint-Variablen.</span><span class="sxs-lookup"><span data-stu-id="145f3-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="145f3-114">Der zweite Befehl fügt dem in $TrafficManagerEndpoint gespeicherten Endpunkt den IP-Adressbereich 1.2.3.4 zu 5.6.7.8 hinzu.</span><span class="sxs-lookup"><span data-stu-id="145f3-114">The second command adds the IP address range 1.2.3.4 to 5.6.7.8 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="145f3-115">Der dritte Befehl fügt dem in $TrafficManagerEndpoint gespeicherten Endpunkt den IP-Adressbereich 9.10.11.0 zu 9.10.11.255 hinzu.</span><span class="sxs-lookup"><span data-stu-id="145f3-115">The third command adds the IP address range 9.10.11.0 to 9.10.11.255 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="145f3-116">Der vierte Befehl überprüft, ob der Bereich der Größe des Bereichs entspricht, und fügt dann den IP-Adressbereich 12.13.14.0 zu 12.13.14.31 dem in $TrafficManagerEndpoint gespeicherten Endpunkt hinzu.</span><span class="sxs-lookup"><span data-stu-id="145f3-116">The fourth command verifies that the scope matches the size of the range, then adds the IP address range 12.13.14.0 to 12.13.14.31 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="145f3-117">Der fünfte Befehl fügt dem in $TrafficManagerEndpoint gespeicherten Endpunkt den IP-Adressbereich 15.16.17.18 zu 15.16.17.18 hinzu.</span><span class="sxs-lookup"><span data-stu-id="145f3-117">The fifth command adds the IP address range 15.16.17.18 to 15.16.17.18 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="145f3-118">Mit dem letzten Befehl wird der Endpunkt im Traffic Manager so aktualisiert, dass er dem lokalen Wert in $TrafficManagerEndpoint entspricht.</span><span class="sxs-lookup"><span data-stu-id="145f3-118">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="145f3-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="145f3-119">PARAMETERS</span></span>

### <span data-ttu-id="145f3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="145f3-120">-DefaultProfile</span></span>
<span data-ttu-id="145f3-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="145f3-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="145f3-122">-Letzte</span><span class="sxs-lookup"><span data-stu-id="145f3-122">-Last</span></span>
<span data-ttu-id="145f3-123">Gibt die letzte IP-Adresse im Bereich an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="145f3-123">Specifies the last IP address in the range to be added.</span></span>

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

### <span data-ttu-id="145f3-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="145f3-124">-Scope</span></span>
<span data-ttu-id="145f3-125">Gibt den Bereich des IP-Adressbereichs an, der hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="145f3-125">Specifies the scope of the IP address range to be added.</span></span>

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

### <span data-ttu-id="145f3-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="145f3-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="145f3-127">Gibt ein lokales **TrafficManagerEndpoint** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="145f3-127">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="145f3-128">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="145f3-128">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="145f3-129">Verwenden Sie zum Abrufen eines **TrafficManagerEndpoint** -Objekts das Get-AzTrafficManagerEndpoint-oder New-AzTrafficManagerEndpoint-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="145f3-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="145f3-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="145f3-130">-Confirm</span></span>
<span data-ttu-id="145f3-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="145f3-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="145f3-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="145f3-132">-WhatIf</span></span>
<span data-ttu-id="145f3-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="145f3-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="145f3-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="145f3-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="145f3-135">-First</span><span class="sxs-lookup"><span data-stu-id="145f3-135">-First</span></span>
<span data-ttu-id="145f3-136">Gibt die erste IP-Adresse im Bereich an, die hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="145f3-136">Specifies the first IP address in the range to be added.</span></span>

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

### <span data-ttu-id="145f3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="145f3-137">CommonParameters</span></span>
<span data-ttu-id="145f3-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="145f3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="145f3-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="145f3-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="145f3-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="145f3-140">INPUTS</span></span>

### <span data-ttu-id="145f3-141">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="145f3-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="145f3-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="145f3-142">OUTPUTS</span></span>

### <span data-ttu-id="145f3-143">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="145f3-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="145f3-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="145f3-144">NOTES</span></span>

## <span data-ttu-id="145f3-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="145f3-145">RELATED LINKS</span></span>

[<span data-ttu-id="145f3-146">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="145f3-146">Remove-AzTrafficManagerIpAddressRange</span></span>](./Remove-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="145f3-147">Neu – AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="145f3-147">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="145f3-148">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="145f3-148">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="145f3-149">Satz-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="145f3-149">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
