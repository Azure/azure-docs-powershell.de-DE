---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2A3B7343-9AA0-4505-AEDE-31C0C5B98694
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutecrossconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteCrossConnection.md
ms.openlocfilehash: 649ae6233f312dab4f18263bb65c4a9cd43b2aee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174273"
---
# <span data-ttu-id="76552-101">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="76552-101">Set-AzExpressRouteCrossConnection</span></span>

## <span data-ttu-id="76552-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="76552-102">SYNOPSIS</span></span>
<span data-ttu-id="76552-103">Ändert eine Express Route-Querverbindung.</span><span class="sxs-lookup"><span data-stu-id="76552-103">Modifies an ExpressRoute cross connection.</span></span>

## <span data-ttu-id="76552-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="76552-104">SYNTAX</span></span>

### <span data-ttu-id="76552-105">ModifyByCircuitReference</span><span class="sxs-lookup"><span data-stu-id="76552-105">ModifyByCircuitReference</span></span>
```
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection <PSExpressRouteCrossConnection> [-AsJob]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76552-106">ModifyByParameterValues</span><span class="sxs-lookup"><span data-stu-id="76552-106">ModifyByParameterValues</span></span>
```
Set-AzExpressRouteCrossConnection -ResourceGroupName <String> -Name <String>
 [-ServiceProviderProvisioningState <String>] [-ServiceProviderNotes <String>]
 [-Peerings <PSExpressRouteCrossConnectionPeering[]>] [-AsJob] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76552-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="76552-107">DESCRIPTION</span></span>
<span data-ttu-id="76552-108">Das Cmdlet " **Satz-AzExpressRouteCrossConnection** " speichert die geänderte Express Route-Querverbindung zu Azure.</span><span class="sxs-lookup"><span data-stu-id="76552-108">The **Set-AzExpressRouteCrossConnection** cmdlet saves the modified ExpressRoute cross connection to Azure.</span></span>

## <span data-ttu-id="76552-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="76552-109">EXAMPLES</span></span>

### <span data-ttu-id="76552-110">Beispiel 1: Ändern des Dienstanbieter Bereitstellungsstatus einer Express Route-Querverbindung</span><span class="sxs-lookup"><span data-stu-id="76552-110">Example 1: Change the Service Provider Provisioning State of an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
$cc.ServiceProviderProvisioningState = 'Provisioned'
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="76552-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="76552-111">PARAMETERS</span></span>

### <span data-ttu-id="76552-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76552-112">-AsJob</span></span>
<span data-ttu-id="76552-113">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="76552-113">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76552-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76552-114">-DefaultProfile</span></span>
<span data-ttu-id="76552-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="76552-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76552-116">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="76552-116">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="76552-117">Gibt das **ExpressRouteCrossConnection** -Objekt an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="76552-117">Specifies the **ExpressRouteCrossConnection** object that this cmdlet modifies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: ModifyByCircuitReference
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76552-118">-Force</span><span class="sxs-lookup"><span data-stu-id="76552-118">-Force</span></span>
<span data-ttu-id="76552-119">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="76552-119">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76552-120">-Name</span><span class="sxs-lookup"><span data-stu-id="76552-120">-Name</span></span>
<span data-ttu-id="76552-121">Der Name der Express-Route-Kreuzverbindung.</span><span class="sxs-lookup"><span data-stu-id="76552-121">The name of express route cross connection.</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76552-122">-Peering</span><span class="sxs-lookup"><span data-stu-id="76552-122">-Peerings</span></span>
<span data-ttu-id="76552-123">Die Liste der Peerings für die Kreuzverbindung</span><span class="sxs-lookup"><span data-stu-id="76552-123">The list of peerings for the cross connection</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnectionPeering[]
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76552-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76552-124">-ResourceGroupName</span></span>
<span data-ttu-id="76552-125">Die ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="76552-125">The ExpressRouteCrossConnection</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76552-126">-ServiceProviderNotes</span><span class="sxs-lookup"><span data-stu-id="76552-126">-ServiceProviderNotes</span></span>
<span data-ttu-id="76552-127">Hinweise des Dienstanbieters</span><span class="sxs-lookup"><span data-stu-id="76552-127">The service provider notes</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76552-128">-ServiceProviderProvisioningState</span><span class="sxs-lookup"><span data-stu-id="76552-128">-ServiceProviderProvisioningState</span></span>
<span data-ttu-id="76552-129">Der Bereitstellungsstatus des Dienstanbieters, der festzulegen ist</span><span class="sxs-lookup"><span data-stu-id="76552-129">The service provider provisioning state to be set</span></span>

```yaml
Type: System.String
Parameter Sets: ModifyByParameterValues
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76552-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="76552-130">-Confirm</span></span>
<span data-ttu-id="76552-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="76552-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76552-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76552-132">-WhatIf</span></span>
<span data-ttu-id="76552-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76552-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76552-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="76552-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76552-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76552-135">CommonParameters</span></span>
<span data-ttu-id="76552-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76552-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76552-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76552-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76552-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="76552-138">INPUTS</span></span>

### <span data-ttu-id="76552-139">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="76552-139">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="76552-140">Der Parameter "ExpressRouteCrossConnection" akzeptiert den Wert vom Typ "PSExpressRouteCrossConnection" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="76552-140">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="76552-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="76552-141">OUTPUTS</span></span>

### <span data-ttu-id="76552-142">Microsoft. Azure. Commands. Network. Models. PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="76552-142">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="76552-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="76552-143">NOTES</span></span>

## <span data-ttu-id="76552-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="76552-144">RELATED LINKS</span></span>

[<span data-ttu-id="76552-145">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="76552-145">Get-AzExpressRouteCrossConnection</span></span>](./Get-AzExpressRouteCrossConnection.md)
