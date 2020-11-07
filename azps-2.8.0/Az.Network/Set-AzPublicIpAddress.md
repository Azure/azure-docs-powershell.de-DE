---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: cc2ef6f016047bd20beba1671129a15c3dfa06f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823831"
---
# <span data-ttu-id="f9fc8-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f9fc8-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="f9fc8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f9fc8-102">SYNOPSIS</span></span>
<span data-ttu-id="f9fc8-103">Aktualisiert eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f9fc8-103">Updates a public IP address.</span></span>

## <span data-ttu-id="f9fc8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9fc8-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f9fc8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9fc8-105">DESCRIPTION</span></span>
<span data-ttu-id="f9fc8-106">Das Cmdlet " **Satz-AzPublicIpAddress** " aktualisiert eine öffentliche IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="f9fc8-106">The **Set-AzPublicIpAddress** cmdlet updates a public IP address.</span></span>

## <span data-ttu-id="f9fc8-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f9fc8-107">EXAMPLES</span></span>

### <span data-ttu-id="f9fc8-108">1: Ändern der Zuordnungsmethode einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="f9fc8-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Static"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="f9fc8-109">Erster Befehl ruft die Ressource für öffentliche IP-Adressen mit dem Namen $publicIPName in der Ressourcengruppe $rgName ab.</span><span class="sxs-lookup"><span data-stu-id="f9fc8-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="f9fc8-110">Der zweite Befehl legt die Zuordnungsmethode des öffentlichen IP-Adressen Objekts auf "static" fest.</span><span class="sxs-lookup"><span data-stu-id="f9fc8-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="f9fc8-111">Set-AzPublicIPAddress Befehl aktualisiert die Ressource für öffentliche IP-Adressen mit dem aktualisierten Objekt und ändert die Zuordnungsmethode auf "statisch".</span><span class="sxs-lookup"><span data-stu-id="f9fc8-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="f9fc8-112">Eine öffentliche IP-Adresse wird sofort zugeteilt.</span><span class="sxs-lookup"><span data-stu-id="f9fc8-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="f9fc8-113">2: Ändern der DNS-Domänen Beschriftung einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="f9fc8-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="f9fc8-114">Erster Befehl ruft die Ressource für öffentliche IP-Adressen mit dem Namen $publicIPName in der Ressourcengruppe $rgName ab.</span><span class="sxs-lookup"><span data-stu-id="f9fc8-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="f9fc8-115">Der zweite Befehl legt die DomainNameLabel-Eigenschaft auf das erforderliche DNS-Präfix fest.</span><span class="sxs-lookup"><span data-stu-id="f9fc8-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="f9fc8-116">Set-AzPublicIPAddress Befehl aktualisiert die Ressource für öffentliche IP-Adressen mit dem aktualisierten Objekt.</span><span class="sxs-lookup"><span data-stu-id="f9fc8-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="f9fc8-117">DomainNameLabel & FQDN werden wie erwartet geändert.</span><span class="sxs-lookup"><span data-stu-id="f9fc8-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="f9fc8-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9fc8-118">PARAMETERS</span></span>

### <span data-ttu-id="f9fc8-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f9fc8-119">-AsJob</span></span>
<span data-ttu-id="f9fc8-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="f9fc8-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f9fc8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9fc8-121">-DefaultProfile</span></span>
<span data-ttu-id="f9fc8-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f9fc8-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9fc8-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f9fc8-123">-PublicIpAddress</span></span>
<span data-ttu-id="f9fc8-124">Gibt ein öffentliches IP-Adressen Objekt an, das den Zustand darstellt, für den die öffentliche IP-Adresse festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f9fc8-124">Specifies a public IP address object representing the state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="f9fc8-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9fc8-125">CommonParameters</span></span>
<span data-ttu-id="f9fc8-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f9fc8-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9fc8-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9fc8-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9fc8-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f9fc8-128">INPUTS</span></span>

### <span data-ttu-id="f9fc8-129">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f9fc8-129">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="f9fc8-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f9fc8-130">OUTPUTS</span></span>

### <span data-ttu-id="f9fc8-131">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f9fc8-131">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="f9fc8-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="f9fc8-132">NOTES</span></span>

## <span data-ttu-id="f9fc8-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f9fc8-133">RELATED LINKS</span></span>

[<span data-ttu-id="f9fc8-134">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f9fc8-134">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="f9fc8-135">Neu – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f9fc8-135">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="f9fc8-136">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="f9fc8-136">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


