---
external help file: Microsoft.Azure.Commands.TrafficManager.dll-Help.xml
Module Name: AzureRM.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.trafficmanager/add-azurertmtrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/TrafficManager/Commands.TrafficManager2/help/Add-AzureRmTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: a00eb5977ad1a58b12ad3f326d36dba8d083d718
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664789"
---
# <span data-ttu-id="7b0af-101">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b0af-101">Add-AzureRmTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="7b0af-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7b0af-102">SYNOPSIS</span></span>
<span data-ttu-id="7b0af-103">Fügt benutzerdefinierte Headerinformationen zu einem lokalen Traffic Manager-Endpunkt Objekt hinzu.</span><span class="sxs-lookup"><span data-stu-id="7b0af-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7b0af-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7b0af-104">SYNTAX</span></span>

```
Add-AzureRmTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b0af-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7b0af-105">DESCRIPTION</span></span>
<span data-ttu-id="7b0af-106">Mit dem Cmdlet **Add-AzureRmTrafficManagerCustomHeaderToEndpoint** werden benutzerdefinierte Headerinformationen zu einem lokalen Azure Traffic Manager-Endpunkt Objekt hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7b0af-106">The **Add-AzureRmTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="7b0af-107">Sie können einen Endpunkt mithilfe der Cmdlets New-AzureRmTrafficManagerEndpoint oder Get-AzureRmTrafficManagerEndpoint abrufen.</span><span class="sxs-lookup"><span data-stu-id="7b0af-107">You can get an endpoint by using the New-AzureRmTrafficManagerEndpoint or Get-AzureRmTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="7b0af-108">Dieses Cmdlet funktioniert für das lokale Endpunkt Objekt.</span><span class="sxs-lookup"><span data-stu-id="7b0af-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="7b0af-109">Übernehmen Sie Ihre Änderungen mithilfe des Set-AzureRmTrafficManagerEndpoint-Cmdlets an den Endpunkt des Datenverkehrs-Managers.</span><span class="sxs-lookup"><span data-stu-id="7b0af-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="7b0af-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7b0af-110">EXAMPLES</span></span>

### <span data-ttu-id="7b0af-111">Beispiel 1: Hinzufügen von benutzerdefinierten Kopfzeileninformationen zu einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="7b0af-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzureRmTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzureRmTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzureRmTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="7b0af-112">Der erste Befehl erstellt einen Azure Traffic Manager-Endpunkt mithilfe des Cmdlets **New-AzureRmTrafficManagerEndpoint** .</span><span class="sxs-lookup"><span data-stu-id="7b0af-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzureRmTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="7b0af-113">Der Befehl speichert den lokalen Endpunkt in der $TrafficManagerEndpoint-Variablen.</span><span class="sxs-lookup"><span data-stu-id="7b0af-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="7b0af-114">Der zweite Befehl fügt dem in $TrafficManagerEndpoint gespeicherten Endpunktbenutzer definierte Headerinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="7b0af-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="7b0af-115">Mit dem letzten Befehl wird der Endpunkt im Traffic Manager so aktualisiert, dass er dem lokalen Wert in $TrafficManagerEndpoint entspricht.</span><span class="sxs-lookup"><span data-stu-id="7b0af-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="7b0af-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="7b0af-116">PARAMETERS</span></span>

### <span data-ttu-id="7b0af-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b0af-117">-DefaultProfile</span></span>
<span data-ttu-id="7b0af-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7b0af-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b0af-119">-Name</span><span class="sxs-lookup"><span data-stu-id="7b0af-119">-Name</span></span>
<span data-ttu-id="7b0af-120">Gibt den Namen der benutzerdefinierten Headerinformationen an, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7b0af-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="7b0af-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b0af-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="7b0af-122">Gibt ein lokales **TrafficManagerEndpoint** -Objekt an.</span><span class="sxs-lookup"><span data-stu-id="7b0af-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="7b0af-123">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="7b0af-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="7b0af-124">Verwenden Sie zum Abrufen eines **TrafficManagerEndpoint** -Objekts das Get-AzureRmTrafficManagerEndpoint-oder New-AzureRmTrafficManagerEndpoint-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b0af-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzureRmTrafficManagerEndpoint or New-AzureRmTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="7b0af-125">-Wert</span><span class="sxs-lookup"><span data-stu-id="7b0af-125">-Value</span></span>
<span data-ttu-id="7b0af-126">Gibt den Wert der benutzerdefinierten Headerinformationen an, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="7b0af-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="7b0af-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7b0af-127">-Confirm</span></span>
<span data-ttu-id="7b0af-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7b0af-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b0af-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b0af-129">-WhatIf</span></span>
<span data-ttu-id="7b0af-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b0af-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7b0af-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7b0af-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b0af-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b0af-132">CommonParameters</span></span>
<span data-ttu-id="7b0af-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b0af-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b0af-134">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7b0af-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b0af-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7b0af-135">INPUTS</span></span>

### <span data-ttu-id="7b0af-136">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b0af-136">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="7b0af-137">Dieses Cmdlet akzeptiert ein **TrafficManagerEndpoint** -Objekt für dieses Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7b0af-137">This cmdlet accepts a **TrafficManagerEndpoint** object to this cmdlet.</span></span>

## <span data-ttu-id="7b0af-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7b0af-138">OUTPUTS</span></span>

### <span data-ttu-id="7b0af-139">Microsoft. Azure. Commands. Network. TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b0af-139">Microsoft.Azure.Commands.Network.TrafficManagerEndpoint</span></span>
<span data-ttu-id="7b0af-140">Dieses Cmdlet gibt ein geändertes **TrafficManagerEndpoint** -Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="7b0af-140">This cmdlet returns a modified **TrafficManagerEndpoint** object.</span></span>

## <span data-ttu-id="7b0af-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="7b0af-141">NOTES</span></span>

## <span data-ttu-id="7b0af-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7b0af-142">RELATED LINKS</span></span>

[<span data-ttu-id="7b0af-143">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b0af-143">Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzureRmTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="7b0af-144">Neu – AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b0af-144">New-AzureRmTrafficManagerEndpoint</span></span>](./New-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="7b0af-145">Get-AzureRmTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="7b0af-145">Get-AzureRmTrafficManagerProfile</span></span>](./Get-AzureRmTrafficManagerEndpoint.md)

[<span data-ttu-id="7b0af-146">Satz-AzureRmTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="7b0af-146">Set-AzureRmTrafficManagerEndpoint</span></span>](./Set-AzureRmTrafficManagerEndpoint.md)
