---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D341
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagerIpAddressRange
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerIpAddressRange.md
ms.openlocfilehash: 2cececec0610b813bf59a1ef8adac59e1fa8ddb2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98360574"
---
# <span data-ttu-id="c2aaf-101">Add-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="c2aaf-101">Add-AzTrafficManagerIpAddressRange</span></span>

## <span data-ttu-id="c2aaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2aaf-102">SYNOPSIS</span></span>
<span data-ttu-id="c2aaf-103">Fügt einen Adressbereich oder ein Subnetz zu einem lokalen Endpunktobjekt für den Datenverkehrs-Manager hinzu.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-103">Adds an address range or subnet to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="c2aaf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c2aaf-104">SYNTAX</span></span>

```
Add-AzTrafficManagerIpAddressRange -First <String> [-Last <String>] [-Scope <Int32>]
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2aaf-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c2aaf-105">DESCRIPTION</span></span>
<span data-ttu-id="c2aaf-106">Das **Cmdlet "Add-AzTrafficManagerIpAddressRange"** fügt einem lokalen Azure Traffic Manager-Endpunktobjekt einen IP-Adressbereich hinzu.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-106">The **Add-AzTrafficManagerIpAddressRange** cmdlet adds an IP address range to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="c2aaf-107">Sie können einen Endpunkt mithilfe der cmdlets New-AzTrafficManagerEndpoint oder Get-AzTrafficManagerEndpoint erhalten.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="c2aaf-108">Dieses Cmdlet wird für das lokale Endpunktobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="c2aaf-109">Sie können Ihre Änderungen am Endpunkt für Verkehrs-Manager mithilfe des cmdlets Set-AzTrafficManagerEndpoint festlegen.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="c2aaf-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c2aaf-110">EXAMPLES</span></span>

### <span data-ttu-id="c2aaf-111">Beispiel 1: Hinzufügen von IP-Adressbereichen zu einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="c2aaf-111">Example 1: Add IP address ranges to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "1.2.3.4" -Last "5.6.7.8"
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "9.10.11.0" -Scope 24
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "12.13.14.0" -Last "12.13.14.31" -Scope 27
PS C:\> Add-AzTrafficManagerIpAddressRange -TrafficManagerEndpoint $TrafficManagerEndpoint -First "15.16.17.18"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="c2aaf-112">Der erste Befehl erstellt einen Azure Traffic Manager-Endpunkt mithilfe des **Cmdlets "New-AzTrafficManagerEndpoint".**</span><span class="sxs-lookup"><span data-stu-id="c2aaf-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="c2aaf-113">Der Befehl speichert den lokalen Endpunkt in der $TrafficManagerEndpoint Variable.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="c2aaf-114">Mit dem zweiten Befehl wird der IN-IP-Adressbereich 1.2.3.4 bis 5.6.7.8 dem in der Datei gespeicherten Endpunkt $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-114">The second command adds the IP address range 1.2.3.4 to 5.6.7.8 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="c2aaf-115">Mit dem dritten Befehl wird der IN-IP-Adressbereich 9.10.11.0 bis 9.10.11.255 dem in der Datei $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-115">The third command adds the IP address range 9.10.11.0 to 9.10.11.255 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="c2aaf-116">Der vierte Befehl überprüft, ob der Bereich der Größe des Bereichs entspricht, und fügt dann den in der Datei "$TrafficManagerEndpoint" gespeicherten Endpunkt den IP-Adressbereich 12.13.14.0 bis 12.13.14.31 hinzu.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-116">The fourth command verifies that the scope matches the size of the range, then adds the IP address range 12.13.14.0 to 12.13.14.31 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="c2aaf-117">Mit dem fünften Befehl wird der IP-Adressbereich 15.16.17.18 bis 15.16.17.18 dem in der Datei gespeicherten Endpunkt $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-117">The fifth command adds the IP address range 15.16.17.18 to 15.16.17.18 to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="c2aaf-118">Der letzte Befehl aktualisiert den Endpunkt im Verkehrs-Manager so, dass er dem lokalen Wert in der $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-118">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="c2aaf-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c2aaf-119">PARAMETERS</span></span>

### <span data-ttu-id="c2aaf-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2aaf-120">-DefaultProfile</span></span>
<span data-ttu-id="c2aaf-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2aaf-122">-Last</span><span class="sxs-lookup"><span data-stu-id="c2aaf-122">-Last</span></span>
<span data-ttu-id="c2aaf-123">Gibt die letzte IP-Adresse in dem Bereich an, der hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-123">Specifies the last IP address in the range to be added.</span></span>

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

### <span data-ttu-id="c2aaf-124">-Scope</span><span class="sxs-lookup"><span data-stu-id="c2aaf-124">-Scope</span></span>
<span data-ttu-id="c2aaf-125">Gibt den Bereich des zu hinzufügenden IP-Adressbereichs an.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-125">Specifies the scope of the IP address range to be added.</span></span>

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

### <span data-ttu-id="c2aaf-126">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c2aaf-126">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="c2aaf-127">Gibt ein lokales **TrafficManagerEndpoint-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-127">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="c2aaf-128">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-128">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="c2aaf-129">Verwenden Sie zum **Abrufen eines TrafficManagerEndpoint-Objekts** das cmdlet Get-AzTrafficManagerEndpoint New-AzTrafficManagerEndpoint TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-129">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="c2aaf-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c2aaf-130">-Confirm</span></span>
<span data-ttu-id="c2aaf-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2aaf-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c2aaf-132">-WhatIf</span></span>
<span data-ttu-id="c2aaf-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c2aaf-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2aaf-135">-First</span><span class="sxs-lookup"><span data-stu-id="c2aaf-135">-First</span></span>
<span data-ttu-id="c2aaf-136">Gibt die erste IP-Adresse in dem bereich an, der hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-136">Specifies the first IP address in the range to be added.</span></span>

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

### <span data-ttu-id="c2aaf-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2aaf-137">CommonParameters</span></span>
<span data-ttu-id="c2aaf-138">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2aaf-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2aaf-139">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2aaf-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2aaf-140">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c2aaf-140">INPUTS</span></span>

### <span data-ttu-id="c2aaf-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c2aaf-141">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="c2aaf-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c2aaf-142">OUTPUTS</span></span>

### <span data-ttu-id="c2aaf-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c2aaf-143">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="c2aaf-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c2aaf-144">NOTES</span></span>

## <span data-ttu-id="c2aaf-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c2aaf-145">RELATED LINKS</span></span>

[<span data-ttu-id="c2aaf-146">Remove-AzTrafficManagerIpAddressRange</span><span class="sxs-lookup"><span data-stu-id="c2aaf-146">Remove-AzTrafficManagerIpAddressRange</span></span>](./Remove-AzTrafficManagerIpAddressRange.md)

[<span data-ttu-id="c2aaf-147">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c2aaf-147">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="c2aaf-148">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="c2aaf-148">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="c2aaf-149">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c2aaf-149">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
