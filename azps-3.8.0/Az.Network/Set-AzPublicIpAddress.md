---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 4cb7d3a48d1783e834b9ecdd53d86969b4e1e6cb
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94003293"
---
# <span data-ttu-id="571ed-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="571ed-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="571ed-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="571ed-102">SYNOPSIS</span></span>
<span data-ttu-id="571ed-103">Aktualisiert eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="571ed-103">Updates a public IP address.</span></span>

## <span data-ttu-id="571ed-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="571ed-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="571ed-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="571ed-105">DESCRIPTION</span></span>
<span data-ttu-id="571ed-106">Das Cmdlet " **Satz-AzPublicIpAddress** " aktualisiert eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="571ed-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="571ed-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="571ed-107">EXAMPLES</span></span>

### <span data-ttu-id="571ed-108">1: Ändern der Zuordnungsmethode einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="571ed-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="571ed-109">Erster Befehl ruft die Ressource für öffentliche IP-Adressen mit dem Namen $publicIPName in der Ressourcengruppe $rgName ab.</span><span class="sxs-lookup"><span data-stu-id="571ed-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="571ed-110">Der zweite Befehl legt die Zuordnungsmethode des öffentlichen IP-Adressen Objekts auf "static" fest.</span><span class="sxs-lookup"><span data-stu-id="571ed-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="571ed-111">Set-AzPublicIPAddress Befehl aktualisiert die Ressource für öffentliche IP-Adressen mit dem aktualisierten Objekt und ändert die Zuordnungsmethode auf "statisch".</span><span class="sxs-lookup"><span data-stu-id="571ed-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="571ed-112">Eine öffentliche IP-Adresse wird sofort zugeteilt.</span><span class="sxs-lookup"><span data-stu-id="571ed-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="571ed-113">2: Hinzufügen einer DNS-Domänen Beschriftung einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="571ed-113">2: Add DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings = @{"DomainNameLabel" = "newdnsprefix"}
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="571ed-114">Erster Befehl ruft die Ressource für öffentliche IP-Adressen mit dem Namen $publicIPName in der Ressourcengruppe $rgName ab.</span><span class="sxs-lookup"><span data-stu-id="571ed-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="571ed-115">Der zweite Befehl legt die DomainNameLabel-Eigenschaft auf das erforderliche DNS-Präfix fest.</span><span class="sxs-lookup"><span data-stu-id="571ed-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="571ed-116">Set-AzPublicIPAddress Befehl aktualisiert die Ressource für öffentliche IP-Adressen mit dem aktualisierten Objekt.</span><span class="sxs-lookup"><span data-stu-id="571ed-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="571ed-117">DomainNameLabel & FQDN werden wie erwartet geändert.</span><span class="sxs-lookup"><span data-stu-id="571ed-117">DomainNameLabel & Fqdn are modified as expected.</span></span>
    
### <span data-ttu-id="571ed-118">3: Ändern der DNS-Domänen Beschriftung einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="571ed-118">3: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="571ed-119">Erster Befehl ruft die Ressource für öffentliche IP-Adressen mit dem Namen $publicIPName in der Ressourcengruppe $rgName ab.</span><span class="sxs-lookup"><span data-stu-id="571ed-119">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="571ed-120">Der zweite Befehl legt die DomainNameLabel-Eigenschaft auf das erforderliche DNS-Präfix fest.</span><span class="sxs-lookup"><span data-stu-id="571ed-120">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="571ed-121">Set-AzPublicIPAddress Befehl aktualisiert die Ressource für öffentliche IP-Adressen mit dem aktualisierten Objekt.</span><span class="sxs-lookup"><span data-stu-id="571ed-121">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="571ed-122">DomainNameLabel & FQDN werden wie erwartet geändert.</span><span class="sxs-lookup"><span data-stu-id="571ed-122">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="571ed-123">Parameter</span><span class="sxs-lookup"><span data-stu-id="571ed-123">PARAMETERS</span></span>

### <span data-ttu-id="571ed-124">-AsJob</span><span class="sxs-lookup"><span data-stu-id="571ed-124">-AsJob</span></span>
<span data-ttu-id="571ed-125">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="571ed-125">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="571ed-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="571ed-126">-DefaultProfile</span></span>
<span data-ttu-id="571ed-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="571ed-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="571ed-128">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="571ed-128">-PublicIpAddress</span></span>
<span data-ttu-id="571ed-129">Gibt ein öffentliches IP-Adressen Objekt an, das den Zustand darstellt, für den die öffentliche IP-Adresse festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="571ed-129">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="571ed-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="571ed-130">CommonParameters</span></span>
<span data-ttu-id="571ed-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="571ed-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="571ed-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="571ed-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="571ed-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="571ed-133">INPUTS</span></span>

### <span data-ttu-id="571ed-134">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="571ed-134">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="571ed-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="571ed-135">OUTPUTS</span></span>

### <span data-ttu-id="571ed-136">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="571ed-136">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="571ed-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="571ed-137">NOTES</span></span>

## <span data-ttu-id="571ed-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="571ed-138">RELATED LINKS</span></span>

[<span data-ttu-id="571ed-139">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="571ed-139">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="571ed-140">Neu – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="571ed-140">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="571ed-141">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="571ed-141">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


