---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azsecuritypartnerprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzSecurityPartnerProvider.md
ms.openlocfilehash: 5af78bb1f915dec55f75749296340ca6d13a3b3d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94301887"
---
# <span data-ttu-id="08e1c-101">New-AzSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="08e1c-101">New-AzSecurityPartnerProvider</span></span>

## <span data-ttu-id="08e1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="08e1c-102">SYNOPSIS</span></span>
<span data-ttu-id="08e1c-103">Erstellt eine Azure-SecurityPartnerProvider.</span><span class="sxs-lookup"><span data-stu-id="08e1c-103">Creates an Azure SecurityPartnerProvider.</span></span>

## <span data-ttu-id="08e1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="08e1c-104">SYNTAX</span></span>

```
New-AzSecurityPartnerProvider -Name <String> -ResourceGroupName <String> -Location <String>
 -SecurityProviderName <String> [-VirtualHub <PSVirtualHub>] [-VirtualHubId <String>]
 [-VirtualHubName <String>] [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="08e1c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="08e1c-105">DESCRIPTION</span></span>
<span data-ttu-id="08e1c-106">Das Cmdlet " **New-AzSecurityPartnerProvider** " erstellt ein Azure-SecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="08e1c-106">The **New-AzSecurityPartnerProvider** cmdlet creates an Azure SecurityPartnerProvider</span></span>

## <span data-ttu-id="08e1c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="08e1c-107">EXAMPLES</span></span>

### <span data-ttu-id="08e1c-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="08e1c-108">Example 1</span></span>
```powershell
 New-AzSecurityPartnerProvider -Name securityPartnerProviderName -ResourceGroupName rgname -Location 'West US' -SecurityProviderName 'ZScaler'
```

## <span data-ttu-id="08e1c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="08e1c-109">PARAMETERS</span></span>

### <span data-ttu-id="08e1c-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08e1c-110">-AsJob</span></span>
<span data-ttu-id="08e1c-111">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="08e1c-111">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08e1c-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e1c-112">-DefaultProfile</span></span>
<span data-ttu-id="08e1c-113">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="08e1c-113">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08e1c-114">-Force</span><span class="sxs-lookup"><span data-stu-id="08e1c-114">-Force</span></span>
<span data-ttu-id="08e1c-115">Keine Bestätigung anfordern, wenn Sie eine Ressource überschreiben möchten</span><span class="sxs-lookup"><span data-stu-id="08e1c-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08e1c-116">-Standort</span><span class="sxs-lookup"><span data-stu-id="08e1c-116">-Location</span></span>
<span data-ttu-id="08e1c-117">Lage.</span><span class="sxs-lookup"><span data-stu-id="08e1c-117">location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08e1c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="08e1c-118">-Name</span></span>
<span data-ttu-id="08e1c-119">Der Ressourcenname.</span><span class="sxs-lookup"><span data-stu-id="08e1c-119">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08e1c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08e1c-120">-ResourceGroupName</span></span>
<span data-ttu-id="08e1c-121">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="08e1c-121">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08e1c-122">-SecurityProviderName</span><span class="sxs-lookup"><span data-stu-id="08e1c-122">-SecurityProviderName</span></span>
<span data-ttu-id="08e1c-123">Name des Sicherheitsanbieters</span><span class="sxs-lookup"><span data-stu-id="08e1c-123">The Security Provider name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ZScaler, IBoss, Checkpoint

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08e1c-124">-Tag</span><span class="sxs-lookup"><span data-stu-id="08e1c-124">-Tag</span></span>
<span data-ttu-id="08e1c-125">Eine Hashtable, die Ressourcen Tags darstellt.</span><span class="sxs-lookup"><span data-stu-id="08e1c-125">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08e1c-126">-VirtualHub</span><span class="sxs-lookup"><span data-stu-id="08e1c-126">-VirtualHub</span></span>
<span data-ttu-id="08e1c-127">Die virtuelle Hub-ID, an die der Security-Partner-Anbieter angefügt ist</span><span class="sxs-lookup"><span data-stu-id="08e1c-127">The virtual hub Id that the security partner provider is attached to</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="08e1c-128">-VirtualHubId</span><span class="sxs-lookup"><span data-stu-id="08e1c-128">-VirtualHubId</span></span>
<span data-ttu-id="08e1c-129">Die ID des VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="08e1c-129">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="08e1c-130">-VirtualHubName</span><span class="sxs-lookup"><span data-stu-id="08e1c-130">-VirtualHubName</span></span>
<span data-ttu-id="08e1c-131">Die ID des VirtualHub, dem dieses VpnGateway zugeordnet werden muss.</span><span class="sxs-lookup"><span data-stu-id="08e1c-131">The Id of the VirtualHub this VpnGateway needs to be associated with.</span></span>

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

### <span data-ttu-id="08e1c-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="08e1c-132">-Confirm</span></span>
<span data-ttu-id="08e1c-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="08e1c-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08e1c-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08e1c-134">-WhatIf</span></span>
<span data-ttu-id="08e1c-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="08e1c-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08e1c-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="08e1c-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="08e1c-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e1c-137">CommonParameters</span></span>
<span data-ttu-id="08e1c-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08e1c-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e1c-139">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08e1c-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e1c-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="08e1c-140">INPUTS</span></span>

### <span data-ttu-id="08e1c-141">System. String</span><span class="sxs-lookup"><span data-stu-id="08e1c-141">System.String</span></span>

### <span data-ttu-id="08e1c-142">Microsoft. Azure. Commands. Network. Models. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="08e1c-142">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="08e1c-143">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="08e1c-143">System.Collections.Hashtable</span></span>

## <span data-ttu-id="08e1c-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="08e1c-144">OUTPUTS</span></span>

### <span data-ttu-id="08e1c-145">Microsoft. Azure. Commands. Network. Models. PSSecurityPartnerProvider</span><span class="sxs-lookup"><span data-stu-id="08e1c-145">Microsoft.Azure.Commands.Network.Models.PSSecurityPartnerProvider</span></span>

## <span data-ttu-id="08e1c-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="08e1c-146">NOTES</span></span>

## <span data-ttu-id="08e1c-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="08e1c-147">RELATED LINKS</span></span>
