---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzPublicIpAddress.md
ms.openlocfilehash: 53d5e15e6354e359461e59728e0776b7d3ec99ea
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843587"
---
# <span data-ttu-id="6f5b0-101">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6f5b0-101">Set-AzPublicIpAddress</span></span>

## <span data-ttu-id="6f5b0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6f5b0-102">SYNOPSIS</span></span>
<span data-ttu-id="6f5b0-103">Legt den Zielstatus für eine öffentliche IP-Adresse fest.</span><span class="sxs-lookup"><span data-stu-id="6f5b0-103">Sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="6f5b0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f5b0-104">SYNTAX</span></span>

```
Set-AzPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6f5b0-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6f5b0-105">DESCRIPTION</span></span>
<span data-ttu-id="6f5b0-106">Das Cmdlet " **Set-AzPublicIpAddress** " legt den Zielstatus für eine öffentliche IP-Adresse fest.</span><span class="sxs-lookup"><span data-stu-id="6f5b0-106">The **Set-AzPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="6f5b0-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6f5b0-107">EXAMPLES</span></span>

### <span data-ttu-id="6f5b0-108">1: Ändern der Zuordnungsmethode einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="6f5b0-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="6f5b0-109">Erster Befehl ruft die Ressource für öffentliche IP-Adressen mit dem Namen $publicIPName in der Ressourcengruppe $rgName ab.</span><span class="sxs-lookup"><span data-stu-id="6f5b0-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="6f5b0-110">Der zweite Befehl legt die Zuordnungsmethode des öffentlichen IP-Adressen Objekts auf "static" fest.</span><span class="sxs-lookup"><span data-stu-id="6f5b0-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="6f5b0-111">Set-AzPublicIPAddress Befehl aktualisiert die Ressource für öffentliche IP-Adressen mit dem aktualisierten Objekt und ändert die Zuordnungsmethode auf "statisch".</span><span class="sxs-lookup"><span data-stu-id="6f5b0-111">Set-AzPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="6f5b0-112">Eine öffentliche IP-Adresse wird sofort zugeteilt.</span><span class="sxs-lookup"><span data-stu-id="6f5b0-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="6f5b0-113">2: Ändern der DNS-Domänen Beschriftung einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="6f5b0-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="6f5b0-114">Erster Befehl ruft die Ressource für öffentliche IP-Adressen mit dem Namen $publicIPName in der Ressourcengruppe $rgName ab.</span><span class="sxs-lookup"><span data-stu-id="6f5b0-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="6f5b0-115">Der zweite Befehl legt die DomainNameLabel-Eigenschaft auf das erforderliche DNS-Präfix fest.</span><span class="sxs-lookup"><span data-stu-id="6f5b0-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="6f5b0-116">Set-AzPublicIPAddress Befehl aktualisiert die Ressource für öffentliche IP-Adressen mit dem aktualisierten Objekt.</span><span class="sxs-lookup"><span data-stu-id="6f5b0-116">Set-AzPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="6f5b0-117">DomainNameLabel & FQDN werden wie erwartet geändert.</span><span class="sxs-lookup"><span data-stu-id="6f5b0-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="6f5b0-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f5b0-118">PARAMETERS</span></span>

### <span data-ttu-id="6f5b0-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6f5b0-119">-AsJob</span></span>
<span data-ttu-id="6f5b0-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="6f5b0-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6f5b0-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f5b0-121">-DefaultProfile</span></span>
<span data-ttu-id="6f5b0-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6f5b0-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6f5b0-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6f5b0-123">-PublicIpAddress</span></span>
<span data-ttu-id="6f5b0-124">Gibt ein **PublicIpAddress** -Objekt an, das den Zielzustand darstellt, für den die öffentliche IP-Adresse festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6f5b0-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

```yaml
Type: PSPublicIpAddress
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6f5b0-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f5b0-125">CommonParameters</span></span>
<span data-ttu-id="6f5b0-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6f5b0-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f5b0-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6f5b0-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f5b0-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6f5b0-128">INPUTS</span></span>

### <span data-ttu-id="6f5b0-129">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6f5b0-129">PSPublicIpAddress</span></span>
<span data-ttu-id="6f5b0-130">Der Parameter "PublicIpAddress" akzeptiert den Wert vom Typ "PSPublicIpAddress" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="6f5b0-130">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="6f5b0-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6f5b0-131">OUTPUTS</span></span>

### <span data-ttu-id="6f5b0-132">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6f5b0-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="6f5b0-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="6f5b0-133">NOTES</span></span>

## <span data-ttu-id="6f5b0-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6f5b0-134">RELATED LINKS</span></span>

[<span data-ttu-id="6f5b0-135">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6f5b0-135">Get-AzPublicIpAddress</span></span>](./Get-AzPublicIpAddress.md)

[<span data-ttu-id="6f5b0-136">Neu – AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6f5b0-136">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="6f5b0-137">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="6f5b0-137">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)


