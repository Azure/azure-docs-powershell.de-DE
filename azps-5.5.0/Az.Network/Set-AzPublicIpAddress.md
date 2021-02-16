---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100160585"
---
# <span data-ttu-id="54824-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="54824-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="54824-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="54824-102">SYNOPSIS</span></span>
<span data-ttu-id="54824-103">Aktualisiert eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="54824-103">Updates a public IP address.</span></span>

## <span data-ttu-id="54824-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="54824-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="54824-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="54824-105">DESCRIPTION</span></span>
<span data-ttu-id="54824-106">Das **Cmdlet "Set-AzPublicIpAddress"** aktualisiert eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="54824-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="54824-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="54824-107">EXAMPLES</span></span>

### <span data-ttu-id="54824-108">1: Ändern der Zuweisungsmethode einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="54824-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="54824-109">Der erste Befehl ruft die öffentliche IP-Adressressource mit $publicIPName in der Ressourcengruppe ab, $rgName.</span><span class="sxs-lookup"><span data-stu-id="54824-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="54824-110">Der zweite Befehl legt die Zuweisungsmethode des öffentlichen IP-Adressobjekts auf "Static" fest.</span><span class="sxs-lookup"><span data-stu-id="54824-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="54824-111">Set-AzPublicIPAddress Befehl aktualisiert die öffentliche IP-Adressressource mit dem aktualisierten Objekt und ändert die Zuordnungsmethode in "Statisch".</span><span class="sxs-lookup"><span data-stu-id="54824-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="54824-112">Eine öffentliche IP-Adresse wird sofort zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="54824-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="54824-113">2: Hinzufügen einer DNS-Domänenbezeichnung einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="54824-113">2: Add DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="54824-114">Der erste Befehl ruft die öffentliche IP-Adressressource mit $publicIPName in der Ressourcengruppe ab, $rgName.</span><span class="sxs-lookup"><span data-stu-id="54824-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="54824-115">Mit dem zweiten Befehl wird die Eigenschaft "DomainNameLabel" auf das erforderliche DNS-Präfix festgelegt.</span><span class="sxs-lookup"><span data-stu-id="54824-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="54824-116">Set-AzPublicIPAddress Befehl aktualisiert die öffentliche IP-Adressressource mit dem aktualisierten Objekt.</span><span class="sxs-lookup"><span data-stu-id="54824-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="54824-117">DomainNameLabel & Fqdn werden wie erwartet geändert.</span><span class="sxs-lookup"><span data-stu-id="54824-117">DomainNameLabel & Fqdn are modified as expected.</span></span>
    
### <span data-ttu-id="54824-118">3: Ändern der Bezeichnung einer öffentlichen IP-Adresse für die DNS-Domäne</span><span class="sxs-lookup"><span data-stu-id="54824-118">3: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="54824-119">Der erste Befehl ruft die öffentliche IP-Adressressource mit $publicIPName in der Ressourcengruppe ab, $rgName.</span><span class="sxs-lookup"><span data-stu-id="54824-119">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="54824-120">Mit dem zweiten Befehl wird die Eigenschaft "DomainNameLabel" auf das erforderliche DNS-Präfix festgelegt.</span><span class="sxs-lookup"><span data-stu-id="54824-120">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="54824-121">Set-AzPublicIPAddress Befehl aktualisiert die öffentliche IP-Adressressource mit dem aktualisierten Objekt.</span><span class="sxs-lookup"><span data-stu-id="54824-121">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="54824-122">DomainNameLabel & Fqdn werden wie erwartet geändert.</span><span class="sxs-lookup"><span data-stu-id="54824-122">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="54824-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="54824-123">PARAMETERS</span></span>

### <span data-ttu-id="54824-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="54824-124">-AsJob</span></span>
<span data-ttu-id="54824-125">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="54824-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="54824-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="54824-126">-DefaultProfile</span></span>
<span data-ttu-id="54824-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="54824-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="54824-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="54824-128">-PublicIpAddress</span></span>
<span data-ttu-id="54824-129">Gibt ein öffentliches IP-Adressobjekt an, das den Zustand darstellt, in dem die öffentliche IP-Adresse festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="54824-129">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="54824-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="54824-130">CommonParameters</span></span>
<span data-ttu-id="54824-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="54824-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="54824-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="54824-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="54824-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="54824-133">INPUTS</span></span>

### <span data-ttu-id="54824-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="54824-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="54824-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="54824-135">OUTPUTS</span></span>

### <span data-ttu-id="54824-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="54824-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="54824-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="54824-137">NOTES</span></span>

## <span data-ttu-id="54824-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="54824-138">RELATED LINKS</span></span>

[<span data-ttu-id="54824-139">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="54824-139">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="54824-140">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="54824-140">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="54824-141">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="54824-141">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


