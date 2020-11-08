---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 9a1be7c45c507746ae3b8c97f883a61de0da78db
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166725"
---
# <span data-ttu-id="6f5a2-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f5a2-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="6f5a2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6f5a2-102">SYNOPSIS</span></span>
<span data-ttu-id="6f5a2-103">Fügt benutzerdefinierte Headerinformationen zu einem lokalen Traffic Manager-Endpunkt Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="6f5a2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f5a2-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6f5a2-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f5a2-105">DESCRIPTION</span></span>
<span data-ttu-id="6f5a2-106">Mit dem Cmdlet **Add-AzTrafficManagerCustomHeaderToEndpoint** werden benutzerdefinierte Headerinformationen zu einem lokalen Azure Traffic Manager-Endpunkt Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="6f5a2-107">Sie können einen Endpunkt mithilfe der Cmdlets New-AzTrafficManagerEndpoint oder Get-AzTrafficManagerEndpoint abrufen.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="6f5a2-108">Dieses Cmdlet funktioniert für das lokale Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="6f5a2-109">Übernehmen Sie Ihre Änderungen mithilfe des Set-AzTrafficManagerEndpoint-Cmdlets an den Endpunkt des Datenverkehrs-Managers.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="6f5a2-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f5a2-110">EXAMPLES</span></span>

### <span data-ttu-id="6f5a2-111">Beispiel 1: Hinzufügen von benutzerdefinierten Kopfzeileninformationen zu einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="6f5a2-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="6f5a2-112">Der erste Befehl erstellt einen Azure Traffic Manager-Endpunkt mithilfe des Cmdlets **New-AzTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="6f5a2-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="6f5a2-113">Der Befehl speichert den lokalen Endpunkt in der $TrafficManagerEndpoint-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="6f5a2-114">Der zweite Befehl fügt dem in $TrafficManagerEndpoint gespeicherten Endpunktbenutzer definierte Headerinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="6f5a2-115">Mit dem letzten Befehl wird der Endpunkt im Traffic Manager so aktualisiert, dass er dem lokalen Wert in $TrafficManagerEndpoint entspricht.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="6f5a2-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f5a2-116">PARAMETERS</span></span>

### <span data-ttu-id="6f5a2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f5a2-117">-DefaultProfile</span></span>
<span data-ttu-id="6f5a2-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6f5a2-119">-Name</span><span class="sxs-lookup"><span data-stu-id="6f5a2-119">-Name</span></span>
<span data-ttu-id="6f5a2-120">Gibt den Namen der benutzerdefinierten Headerinformationen an, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="6f5a2-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f5a2-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="6f5a2-122">Gibt ein lokales **TrafficManagerEndpoint** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="6f5a2-123">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="6f5a2-124">Verwenden Sie zum Abrufen eines **TrafficManagerEndpoint** -Objekts das Get-AzTrafficManagerEndpoint-oder New-AzTrafficManagerEndpoint-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="6f5a2-125">-Wert</span><span class="sxs-lookup"><span data-stu-id="6f5a2-125">-Value</span></span>
<span data-ttu-id="6f5a2-126">Gibt den Wert der benutzerdefinierten Headerinformationen an, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="6f5a2-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6f5a2-127">-Confirm</span></span>
<span data-ttu-id="6f5a2-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6f5a2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6f5a2-129">-WhatIf</span></span>
<span data-ttu-id="6f5a2-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6f5a2-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6f5a2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f5a2-132">CommonParameters</span></span>
<span data-ttu-id="6f5a2-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f5a2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f5a2-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f5a2-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f5a2-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6f5a2-135">INPUTS</span></span>

### <span data-ttu-id="6f5a2-136">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f5a2-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="6f5a2-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6f5a2-137">OUTPUTS</span></span>

### <span data-ttu-id="6f5a2-138">Microsoft. Azure. Commands. Trafficmanager. Models. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f5a2-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="6f5a2-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="6f5a2-139">NOTES</span></span>

## <span data-ttu-id="6f5a2-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6f5a2-140">RELATED LINKS</span></span>

[<span data-ttu-id="6f5a2-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f5a2-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="6f5a2-142">Neu – AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f5a2-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="6f5a2-143">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="6f5a2-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="6f5a2-144">Satz-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="6f5a2-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
