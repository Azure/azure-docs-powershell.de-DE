---
external help file: Microsoft.Azure.PowerShell.Cmdlets.TrafficManager.dll-Help.xml
Module Name: Az.TrafficManager
ms.assetid: 25E3F297-1D91-4102-B4D3-1E7195A5D33E
online version: https://docs.microsoft.com/powershell/module/az.trafficmanager/add-aztrafficmanagercustomheadertoendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TrafficManager/TrafficManager/help/Add-AzTrafficManagerCustomHeaderToEndpoint.md
ms.openlocfilehash: 4a24953dd763c54cba7454bf9e46bb9373b0f450
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101936536"
---
# <span data-ttu-id="d0551-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0551-101">Add-AzTrafficManagerCustomHeaderToEndpoint</span></span>

## <span data-ttu-id="d0551-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0551-102">SYNOPSIS</span></span>
<span data-ttu-id="d0551-103">Fügt einem lokalen Traffic Manager-Endpunktobjekt benutzerdefinierte Headerinformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="d0551-103">Adds custom header information to a local Traffic Manager endpoint object.</span></span>

## <span data-ttu-id="d0551-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d0551-104">SYNTAX</span></span>

```
Add-AzTrafficManagerCustomHeaderToEndpoint -Name <String> -Value <String>
 -TrafficManagerEndpoint <TrafficManagerEndpoint> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0551-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d0551-105">DESCRIPTION</span></span>
<span data-ttu-id="d0551-106">Das **Add-AzTrafficManagerCustomHeaderToEndpoint-Cmdlet** fügt einem lokalen Azure Traffic Manager-Endpunktobjekt benutzerdefinierte Kopfzeileninformationen hinzu.</span><span class="sxs-lookup"><span data-stu-id="d0551-106">The **Add-AzTrafficManagerCustomHeaderToEndpoint** cmdlet adds custom header information to a local Azure Traffic Manager endpoint object.</span></span>
<span data-ttu-id="d0551-107">Sie können einen Endpunkt mithilfe der cmdlets New-AzTrafficManagerEndpoint oder Get-AzTrafficManagerEndpoint erhalten.</span><span class="sxs-lookup"><span data-stu-id="d0551-107">You can get an endpoint by using the New-AzTrafficManagerEndpoint or Get-AzTrafficManagerEndpoint cmdlets.</span></span>

<span data-ttu-id="d0551-108">Dieses Cmdlet wird für das lokale Endpunktobjekt verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0551-108">This cmdlet operates on the local endpoint object.</span></span>
<span data-ttu-id="d0551-109">Sie können Ihre Änderungen mithilfe des cmdlets "Set-AzTrafficManagerEndpoint" am Endpunkt für Traffic Manager festlegen.</span><span class="sxs-lookup"><span data-stu-id="d0551-109">Commit your changes to the endpoint for Traffic Manager by using the Set-AzTrafficManagerEndpoint cmdlet.</span></span>

## <span data-ttu-id="d0551-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d0551-110">EXAMPLES</span></span>

### <span data-ttu-id="d0551-111">Beispiel 1: Hinzufügen von benutzerdefinierten Kopfzeileninformationen zu einem Endpunkt</span><span class="sxs-lookup"><span data-stu-id="d0551-111">Example 1: Add custom header information to an endpoint</span></span>
```
PS C:\> $TrafficManagerEndpoint = New-AzTrafficManagerEndpoint -EndpointStatus Enabled -Name "contoso" -ProfileName "ContosoProfile" -ResourceGroupName "ResourceGroup11" -Type AzureEndpoints -Priority 1 -TargetResourceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/Default-Web-CentralUS/providers/Microsoft.Web/sites/contoso-web-app" -Weight 10
PS C:\> Add-AzTrafficManagerCustomHeaderToEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint -Name "host" -Value "www.contoso.com"
PS C:\> Set-AzTrafficManagerEndpoint -TrafficManagerEndpoint $TrafficManagerEndpoint
```

<span data-ttu-id="d0551-112">Mit dem ersten Befehl wird ein Azure Traffic Manager-Endpunkt mithilfe des **Cmdlets New-AzTrafficManagerEndpoint** erstellt.</span><span class="sxs-lookup"><span data-stu-id="d0551-112">The first command creates an Azure Traffic Manager endpoint by using the **New-AzTrafficManagerEndpoint** cmdlet.</span></span>
<span data-ttu-id="d0551-113">Der Befehl speichert den lokalen Endpunkt in der $TrafficManagerEndpoint Variablen.</span><span class="sxs-lookup"><span data-stu-id="d0551-113">The command stores the local endpoint in the $TrafficManagerEndpoint variable.</span></span>
<span data-ttu-id="d0551-114">Der zweite Befehl fügt dem endpunkt, der in der Datei gespeichert ist, benutzerdefinierte Kopfzeileninformationen $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d0551-114">The second command adds custom header information to the endpoint stored in $TrafficManagerEndpoint.</span></span>
<span data-ttu-id="d0551-115">Der letzte Befehl aktualisiert den Endpunkt in Traffic Manager so, dass er dem lokalen Wert in $TrafficManagerEndpoint.</span><span class="sxs-lookup"><span data-stu-id="d0551-115">The final command updates the endpoint in Traffic Manager to match the local value in $TrafficManagerEndpoint.</span></span>

## <span data-ttu-id="d0551-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d0551-116">PARAMETERS</span></span>

### <span data-ttu-id="d0551-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0551-117">-DefaultProfile</span></span>
<span data-ttu-id="d0551-118">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0551-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0551-119">-Name</span><span class="sxs-lookup"><span data-stu-id="d0551-119">-Name</span></span>
<span data-ttu-id="d0551-120">Gibt den Namen der benutzerdefinierten Kopfzeileninformationen an, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d0551-120">Specifies the name of the custom header information to be added.</span></span>

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

### <span data-ttu-id="d0551-121">-TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0551-121">-TrafficManagerEndpoint</span></span>
<span data-ttu-id="d0551-122">Gibt ein lokales **TrafficManagerEndpoint-Objekt** an.</span><span class="sxs-lookup"><span data-stu-id="d0551-122">Specifies a local **TrafficManagerEndpoint** object.</span></span>
<span data-ttu-id="d0551-123">Dieses Cmdlet ändert dieses lokale Objekt.</span><span class="sxs-lookup"><span data-stu-id="d0551-123">This cmdlet modifies this local object.</span></span>
<span data-ttu-id="d0551-124">Um ein **TrafficManagerEndpoint-Objekt zu** erhalten, verwenden Sie das cmdlet Get-AzTrafficManagerEndpoint oder New-AzTrafficManagerEndpoint cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0551-124">To obtain a **TrafficManagerEndpoint** object, use the Get-AzTrafficManagerEndpoint or New-AzTrafficManagerEndpoint cmdlet.</span></span>

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

### <span data-ttu-id="d0551-125">-Wert</span><span class="sxs-lookup"><span data-stu-id="d0551-125">-Value</span></span>
<span data-ttu-id="d0551-126">Gibt den Wert der benutzerdefinierten Kopfzeileninformationen an, die hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d0551-126">Specifies the value of the custom header information to be added.</span></span>

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

### <span data-ttu-id="d0551-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d0551-127">-Confirm</span></span>
<span data-ttu-id="d0551-128">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d0551-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0551-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0551-129">-WhatIf</span></span>
<span data-ttu-id="d0551-130">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d0551-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d0551-131">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d0551-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0551-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0551-132">CommonParameters</span></span>
<span data-ttu-id="d0551-133">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0551-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0551-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0551-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0551-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d0551-135">INPUTS</span></span>

### <span data-ttu-id="d0551-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0551-136">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="d0551-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d0551-137">OUTPUTS</span></span>

### <span data-ttu-id="d0551-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0551-138">Microsoft.Azure.Commands.TrafficManager.Models.TrafficManagerEndpoint</span></span>

## <span data-ttu-id="d0551-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d0551-139">NOTES</span></span>

## <span data-ttu-id="d0551-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d0551-140">RELATED LINKS</span></span>

[<span data-ttu-id="d0551-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0551-141">Remove-AzTrafficManagerCustomHeaderFromEndpoint</span></span>](./Remove-AzTrafficManagerCustomHeaderFromEndpoint.md)

[<span data-ttu-id="d0551-142">New-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0551-142">New-AzTrafficManagerEndpoint</span></span>](./New-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="d0551-143">Get-AzTrafficManagerProfile</span><span class="sxs-lookup"><span data-stu-id="d0551-143">Get-AzTrafficManagerProfile</span></span>](./Get-AzTrafficManagerEndpoint.md)

[<span data-ttu-id="d0551-144">Set-AzTrafficManagerEndpoint</span><span class="sxs-lookup"><span data-stu-id="d0551-144">Set-AzTrafficManagerEndpoint</span></span>](./Set-AzTrafficManagerEndpoint.md)
