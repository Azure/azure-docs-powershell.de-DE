---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/en-us/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 9a1be7c45c507746ae3b8c97f883a61de0da78db
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98367154"
---
# <span data-ttu-id="e3ca9-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3ca9-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="e3ca9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3ca9-102">SYNOPSIS</span></span>
<span data-ttu-id="e3ca9-103">Fügt einem lokalen Endpunktobjekt von Traffic Manager benutzerdefinierte Headerinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="e3ca9-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="e3ca9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e3ca9-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e3ca9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e3ca9-105">DESCRIPTION</span></span>
<span data-ttu-id="e3ca9-106">Das **Cmdlet "Add-AzTrafficManagerCustomHeaderToEndpoint"** fügt einem lokalen Azure Traffic Manager-Endpunktobjekt benutzerdefinierte Headerinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="e3ca9-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="e3ca9-107">Sie können einen Endpunkt mithilfe der cmdlets New-AzTrafficManagerEndpoint oder Get-AzTrafficManagerEndpoint erhalten.</span><span class="sxs-lookup"><span data-stu-id="e3ca9-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="e3ca9-108">Dieses Cmdlet wird für das lokale Endpunktobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="e3ca9-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="e3ca9-109">Sie können Ihre Änderungen am Endpunkt für Verkehrs-Manager mithilfe des cmdlets Set-AzTrafficManagerEndpoint festlegen.</span><span class="sxs-lookup"><span data-stu-id="e3ca9-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="e3ca9-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e3ca9-110">EXAMPLES</span></span>

### <span data-ttu-id="e3ca9-111">Beispiel 1: Hinzufügen von benutzerdefinierten Kopfzeileninformationen zu einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="e3ca9-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="e3ca9-112">Der erste Befehl erstellt einen Azure Traffic Manager-Endpunkt mithilfe des **Cmdlets "New-AzTrafficManagerEndpoint".**</span><span class="sxs-lookup"><span data-stu-id="e3ca9-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="e3ca9-113">Der Befehl speichert den lokalen Endpunkt in der $TrafficManagerEndpoint Variable.</span><span class="sxs-lookup"><span data-stu-id="e3ca9-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="e3ca9-114">Mit dem zweiten Befehl werden dem in der Datei gespeicherten Endpunkt benutzerdefinierte Kopfzeileninformationen $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e3ca9-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="e3ca9-115">Der letzte Befehl aktualisiert den Endpunkt im Verkehrs-Manager so, dass er dem lokalen Wert in der $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e3ca9-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="e3ca9-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e3ca9-116">PARAMETERS</span></span>

### <span data-ttu-id="e3ca9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3ca9-117">-DefaultProfile</span></span>
<span data-ttu-id="e3ca9-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="e3ca9-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e3ca9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e3ca9-119">-Name</span></span>
<span data-ttu-id="e3ca9-120">Gibt den Namen der benutzerdefinierten Kopfzeileninformationen an, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e3ca9-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="e3ca9-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3ca9-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="e3ca9-122">Gibt ein lokales **TrafficManagerEndpoint-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="e3ca9-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="e3ca9-123">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="e3ca9-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="e3ca9-124">Verwenden Sie zum **Abrufen eines TrafficManagerEndpoint-Objekts** das cmdlet Get-AzTrafficManagerEndpoint New-AzTrafficManagerEndpoint TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="e3ca9-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="e3ca9-125">-Value</span><span class="sxs-lookup"><span data-stu-id="e3ca9-125">-Value</span></span>
<span data-ttu-id="e3ca9-126">Gibt den Wert der benutzerdefinierten Kopfzeileninformationen an, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="e3ca9-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="e3ca9-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e3ca9-127">-Confirm</span></span>
<span data-ttu-id="e3ca9-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="e3ca9-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3ca9-129">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="e3ca9-129">-WhatIf</span></span>
<span data-ttu-id="e3ca9-130">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="e3ca9-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e3ca9-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="e3ca9-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3ca9-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3ca9-132">CommonParameters</span></span>
<span data-ttu-id="e3ca9-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3ca9-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3ca9-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3ca9-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3ca9-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e3ca9-135">INPUTS</span></span>

### <span data-ttu-id="e3ca9-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3ca9-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="e3ca9-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e3ca9-137">OUTPUTS</span></span>

### <span data-ttu-id="e3ca9-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3ca9-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="e3ca9-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e3ca9-139">NOTES</span></span>

## <span data-ttu-id="e3ca9-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e3ca9-140">RELATED LINKS</span></span>

[<span data-ttu-id="e3ca9-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3ca9-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="e3ca9-142">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3ca9-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="e3ca9-143">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="e3ca9-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="e3ca9-144">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="e3ca9-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
