---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EC798838-1850-4E88-B17F-D2F00F2D4EE9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmPublicIpAddress.md
ms.openlocfilehash: df1c03551d520a833e8b974ae2a2b71fe442c4c4
ms.sourcegitcommit: e0947ba0606618a565d8a99fa0e4bef7d028d7e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "93665418"
---
# <span data-ttu-id="52a01-101">Set-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="52a01-101">Set-AzureRmPublicIpAddress</span></span>

## <span data-ttu-id="52a01-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="52a01-102">SYNOPSIS</span></span>
<span data-ttu-id="52a01-103">Legt den Zielstatus für eine öffentliche IP-Adresse fest.</span><span class="sxs-lookup"><span data-stu-id="52a01-103">Sets the goal state for a public IP address.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52a01-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="52a01-104">SYNTAX</span></span>

```
Set-AzureRmPublicIpAddress -PublicIpAddress <PSPublicIpAddress> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52a01-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="52a01-105">DESCRIPTION</span></span>
<span data-ttu-id="52a01-106">Das Cmdlet " **Set-AzureRmPublicIpAddress** " legt den Zielstatus für eine öffentliche IP-Adresse fest.</span><span class="sxs-lookup"><span data-stu-id="52a01-106">The **Set-AzureRmPublicIpAddress** cmdlet sets the goal state for a public IP address.</span></span>

## <span data-ttu-id="52a01-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="52a01-107">EXAMPLES</span></span>

### <span data-ttu-id="52a01-108">1: Ändern der Zuordnungsmethode einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="52a01-108">1: Change allocation method of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.PublicIpAllocationMethod = "Dynamic"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

 <span data-ttu-id="52a01-109">Erster Befehl ruft die Ressource für öffentliche IP-Adressen mit dem Namen $publicIPName in der Ressourcengruppe $rgName ab.</span><span class="sxs-lookup"><span data-stu-id="52a01-109">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="52a01-110">Der zweite Befehl legt die Zuordnungsmethode des öffentlichen IP-Adressen Objekts auf "static" fest.</span><span class="sxs-lookup"><span data-stu-id="52a01-110">Second command sets the allocation method of the public IP address object to "Static".</span></span>
<span data-ttu-id="52a01-111">Set-AzureRmPublicIPAddress Befehl aktualisiert die Ressource für öffentliche IP-Adressen mit dem aktualisierten Objekt und ändert die Zuordnungsmethode auf "statisch".</span><span class="sxs-lookup"><span data-stu-id="52a01-111">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object, and modifies the allocation method to 'Static'.</span></span> <span data-ttu-id="52a01-112">Eine öffentliche IP-Adresse wird sofort zugeteilt.</span><span class="sxs-lookup"><span data-stu-id="52a01-112">A public IP address gets allocated immediately.</span></span>

### <span data-ttu-id="52a01-113">2: Ändern der DNS-Domänen Beschriftung einer öffentlichen IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="52a01-113">2: Change DNS domain label of a public IP address</span></span>
```
PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName

PS C:\> $publicIp.DnsSettings.DomainNameLabel = "newdnsprefix"
    
PS C:\> Set-AzureRmPublicIpAddress -PublicIpAddress $publicIp

PS C:\> $publicIp = Get-AzureRmPublicIpAddress -Name $publicIpName -ResourceGroupName $rgName
```

<span data-ttu-id="52a01-114">Erster Befehl ruft die Ressource für öffentliche IP-Adressen mit dem Namen $publicIPName in der Ressourcengruppe $rgName ab.</span><span class="sxs-lookup"><span data-stu-id="52a01-114">First command gets the public IP address resource with name $publicIPName in the resource group $rgName.</span></span>
<span data-ttu-id="52a01-115">Der zweite Befehl legt die DomainNameLabel-Eigenschaft auf das erforderliche DNS-Präfix fest.</span><span class="sxs-lookup"><span data-stu-id="52a01-115">Second command sets the DomainNameLabel property to the required dns prefix.</span></span>
<span data-ttu-id="52a01-116">Set-AzureRmPublicIPAddress Befehl aktualisiert die Ressource für öffentliche IP-Adressen mit dem aktualisierten Objekt.</span><span class="sxs-lookup"><span data-stu-id="52a01-116">Set-AzureRmPublicIPAddress command updates the public IP address resource with the updated object.</span></span> <span data-ttu-id="52a01-117">DomainNameLabel & FQDN werden wie erwartet geändert.</span><span class="sxs-lookup"><span data-stu-id="52a01-117">DomainNameLabel & Fqdn are modified as expected.</span></span>

## <span data-ttu-id="52a01-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="52a01-118">PARAMETERS</span></span>

### <span data-ttu-id="52a01-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52a01-119">-AsJob</span></span>
<span data-ttu-id="52a01-120">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="52a01-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52a01-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52a01-121">-DefaultProfile</span></span>
<span data-ttu-id="52a01-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="52a01-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52a01-123">-PublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="52a01-123">-PublicIpAddress</span></span>
<span data-ttu-id="52a01-124">Gibt ein **PublicIpAddress** -Objekt an, das den Zielzustand darstellt, für den die öffentliche IP-Adresse festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="52a01-124">Specifies a **PublicIpAddress** object that represents the goal state to which the public IP address should be set.</span></span>

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

### <span data-ttu-id="52a01-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52a01-125">CommonParameters</span></span>
<span data-ttu-id="52a01-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52a01-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52a01-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52a01-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52a01-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="52a01-128">INPUTS</span></span>

### <span data-ttu-id="52a01-129">PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="52a01-129">PSPublicIpAddress</span></span>
<span data-ttu-id="52a01-130">Der Parameter "PublicIpAddress" akzeptiert den Wert vom Typ "PSPublicIpAddress" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="52a01-130">Parameter 'PublicIpAddress' accepts value of type 'PSPublicIpAddress' from the pipeline</span></span>

## <span data-ttu-id="52a01-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="52a01-131">OUTPUTS</span></span>

### <span data-ttu-id="52a01-132">Microsoft. Azure. Commands. Network. Models. PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="52a01-132">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="52a01-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="52a01-133">NOTES</span></span>

## <span data-ttu-id="52a01-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="52a01-134">RELATED LINKS</span></span>

[<span data-ttu-id="52a01-135">Get-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="52a01-135">Get-AzureRmPublicIpAddress</span></span>](./Get-AzureRmPublicIpAddress.md)

[<span data-ttu-id="52a01-136">Neu – AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="52a01-136">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="52a01-137">Remove-AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="52a01-137">Remove-AzureRmPublicIpAddress</span></span>](./Remove-AzureRmPublicIpAddress.md)


