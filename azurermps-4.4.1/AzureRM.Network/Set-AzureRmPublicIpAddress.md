---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
ms.openlocfilehash: 1460b4497909d56e2d10d03e33df71518c52b796
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662636"
---
# <span data-ttu-id="e0dc5-101">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e0dc5-101">Set-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="e0dc5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e0dc5-102">SYNOPSIS</span></span>
<span data-ttu-id="e0dc5-103">Legt den Zielstatus für eine öffentliche IP-Adresse fest.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-103">Sets the goal state for a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e0dc5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e0dc5-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e0dc5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e0dc5-105">DESCRIPTION</span></span>
<span data-ttu-id="e0dc5-106">Das Cmdlet " **Set-AzureRmPublicIpAddress** " legt den Zielstatus für eine öffentliche IP-Adresse fest.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-106">The **Set-AzureRmPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="e0dc5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e0dc5-107">EXAMPLES</span></span>

### <span data-ttu-id="e0dc5-108">1: Ändern der Zuordnungsmethode einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="e0dc5-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="e0dc5-109">Erster Befehl ruft die Ressource für öffentliche IP-Adressen mit dem Namen $publicIPName in der Ressourcengruppe $rgName ab.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="e0dc5-110">Der zweite Befehl legt die Zuordnungsmethode des öffentlichen IP-Adressen Objekts auf "static" fest.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="e0dc5-111">Set-AzureRmPublicIPAddress Befehl aktualisiert die Ressource für öffentliche IP-Adressen mit dem aktualisierten Objekt und ändert die Zuordnungsmethode auf "statisch".</span><span class="sxs-lookup"><span data-stu-id="e0dc5-111">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="e0dc5-112">Eine öffentliche IP-Adresse wird sofort zugeteilt.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="e0dc5-113">2: Ändern der DNS-Domänen Beschriftung einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="e0dc5-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="e0dc5-114">Erster Befehl ruft die Ressource für öffentliche IP-Adressen mit dem Namen $publicIPName in der Ressourcengruppe $rgName ab.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="e0dc5-115">Der zweite Befehl legt die DomainNameLabel-Eigenschaft auf das erforderliche DNS-Präfix fest.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="e0dc5-116">Set-AzureRmPublicIPAddress Befehl aktualisiert die Ressource für öffentliche IP-Adressen mit dem aktualisierten Objekt.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-116">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="e0dc5-117">DomainNameLabel & FQDN werden wie erwartet geändert.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="e0dc5-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="e0dc5-118">PARAMETERS</span></span>

### <span data-ttu-id="e0dc5-119">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e0dc5-119">-PublicIpAddress</span></span>
<span data-ttu-id="e0dc5-120">Gibt ein **PublicIpAddress** -Objekt an, das den Zielzustand darstellt, für den die öffentliche IP-Adresse festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-120">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="e0dc5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0dc5-121">-DefaultProfile</span></span>
<span data-ttu-id="e0dc5-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e0dc5-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0dc5-123">CommonParameters</span></span>
<span data-ttu-id="e0dc5-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0dc5-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e0dc5-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0dc5-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e0dc5-126">INPUTS</span></span>

### <span data-ttu-id="e0dc5-127">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e0dc5-127">PSPublicIpAddress</span></span>
<span data-ttu-id="e0dc5-128">Der Parameter "PublicIpAddress" akzeptiert den Wert vom Typ "PSPublicIpAddress" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="e0dc5-128">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="e0dc5-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e0dc5-129">OUTPUTS</span></span>

### <span data-ttu-id="e0dc5-130">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e0dc5-130">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="e0dc5-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="e0dc5-131">NOTES</span></span>

## <span data-ttu-id="e0dc5-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e0dc5-132">RELATED LINKS</span></span>

[<span data-ttu-id="e0dc5-133">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e0dc5-133">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="e0dc5-134">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e0dc5-134">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="e0dc5-135">Neu – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e0dc5-135">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="e0dc5-136">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="e0dc5-136">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)


