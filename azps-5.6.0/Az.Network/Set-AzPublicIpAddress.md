---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 33712b9813d6c23ed72097597d94a22bf7644992
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938560"
---
# <span data-ttu-id="afbcd-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="afbcd-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="afbcd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="afbcd-102">SYNOPSIS</span></span>
<span data-ttu-id="afbcd-103">Aktualisiert eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="afbcd-103">Updates a public IP address.</span></span>

## <span data-ttu-id="afbcd-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="afbcd-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="afbcd-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afbcd-105">DESCRIPTION</span></span>
<span data-ttu-id="afbcd-106">Das **Cmdlet Set-AzPublicIpAddress** aktualisiert eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="afbcd-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="afbcd-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="afbcd-107">EXAMPLES</span></span>

### <span data-ttu-id="afbcd-108">1: Ändern der Zuordnungsmethode einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="afbcd-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="afbcd-109">Der erste Befehl ruft die öffentliche IP-Adressressource mit $publicIPName in der Ressourcengruppe $rgName.</span><span class="sxs-lookup"><span data-stu-id="afbcd-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="afbcd-110">Der zweite Befehl legt die Zuordnungsmethode des öffentlichen IP-Adressobjekts auf "Statisch" fest.</span><span class="sxs-lookup"><span data-stu-id="afbcd-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="afbcd-111">Set-AzPublicIPAddress Befehl aktualisiert die öffentliche IP-Adressressource mit dem aktualisierten Objekt und ändert die Zuordnungsmethode in "Statisch".</span><span class="sxs-lookup"><span data-stu-id="afbcd-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="afbcd-112">Eine öffentliche IP-Adresse wird sofort zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="afbcd-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="afbcd-113">2: Hinzufügen einer DNS-Domänenbezeichnung einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="afbcd-113">2: Add DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="afbcd-114">Der erste Befehl ruft die öffentliche IP-Adressressource mit $publicIPName in der Ressourcengruppe $rgName.</span><span class="sxs-lookup"><span data-stu-id="afbcd-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="afbcd-115">Der zweite Befehl legt die DomainNameLabel-Eigenschaft auf das erforderliche DNS-Präfix fest.</span><span class="sxs-lookup"><span data-stu-id="afbcd-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="afbcd-116">Set-AzPublicIPAddress Befehl aktualisiert die öffentliche IP-Adressressource mit dem aktualisierten Objekt.</span><span class="sxs-lookup"><span data-stu-id="afbcd-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="afbcd-117">DomainNameLabel & Fqdn werden wie erwartet geändert.</span><span class="sxs-lookup"><span data-stu-id="afbcd-117">DomainNameLabel & Fqdn are modified as expected.</span></span>
    
### <span data-ttu-id="afbcd-118">3: Ändern der DNS-Domänenbezeichnung einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="afbcd-118">3: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="afbcd-119">Der erste Befehl ruft die öffentliche IP-Adressressource mit $publicIPName in der Ressourcengruppe $rgName.</span><span class="sxs-lookup"><span data-stu-id="afbcd-119">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="afbcd-120">Der zweite Befehl legt die DomainNameLabel-Eigenschaft auf das erforderliche DNS-Präfix fest.</span><span class="sxs-lookup"><span data-stu-id="afbcd-120">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="afbcd-121">Set-AzPublicIPAddress Befehl aktualisiert die öffentliche IP-Adressressource mit dem aktualisierten Objekt.</span><span class="sxs-lookup"><span data-stu-id="afbcd-121">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="afbcd-122">DomainNameLabel & Fqdn werden wie erwartet geändert.</span><span class="sxs-lookup"><span data-stu-id="afbcd-122">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="afbcd-123">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="afbcd-123">PARAMETERS</span></span>

### <span data-ttu-id="afbcd-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="afbcd-124">-AsJob</span></span>
<span data-ttu-id="afbcd-125">Ausführen des Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="afbcd-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="afbcd-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="afbcd-126">-DefaultProfile</span></span>
<span data-ttu-id="afbcd-127">Die Anmeldeinformationen, das Konto, der Mandant und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="afbcd-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="afbcd-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="afbcd-128">-PublicIpAddress</span></span>
<span data-ttu-id="afbcd-129">Gibt ein öffentliches IP-Adressobjekt an, das den Zustand darstellt, auf den die öffentliche IP-Adresse festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="afbcd-129">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="afbcd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="afbcd-130">CommonParameters</span></span>
<span data-ttu-id="afbcd-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="afbcd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="afbcd-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="afbcd-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="afbcd-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="afbcd-133">INPUTS</span></span>

### <span data-ttu-id="afbcd-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="afbcd-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="afbcd-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="afbcd-135">OUTPUTS</span></span>

### <span data-ttu-id="afbcd-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="afbcd-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="afbcd-137">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="afbcd-137">NOTES</span></span>

## <span data-ttu-id="afbcd-138">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="afbcd-138">RELATED LINKS</span></span>

[<span data-ttu-id="afbcd-139">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="afbcd-139">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="afbcd-140">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="afbcd-140">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="afbcd-141">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="afbcd-141">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


