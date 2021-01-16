---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Dns.dll-Help.xml
Module Name: Az.Dns
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: https://docs.microsoft.com/en-us/powershell/module/az.dns/get-azdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Dns/Dns/help/Get-AzDnsZone.md
ms.openlocfilehash: 68fff050564eff7014a7428556d3d4b2ce68f06d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98302384"
---
# <span data-ttu-id="f33e2-101">Get-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="f33e2-101">Get-AzDnsZone</span></span>

## <span data-ttu-id="f33e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f33e2-102">SYNOPSIS</span></span>
<span data-ttu-id="f33e2-103">Ruft eine DNS-Zone ab.</span><span class="sxs-lookup"><span data-stu-id="f33e2-103">Gets a DNS zone.</span></span>

## <span data-ttu-id="f33e2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f33e2-104">SYNTAX</span></span>

### <span data-ttu-id="f33e2-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="f33e2-105">Default (Default)</span></span>
```
Get-AzDnsZone [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f33e2-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f33e2-106">ResourceGroup</span></span>
```
Get-AzDnsZone [-Name <String>] -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f33e2-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f33e2-107">DESCRIPTION</span></span>
<span data-ttu-id="f33e2-108">Das **Get-AzDnsZone-Cmdlet** ruft eine Domain Name System (DNS)-Zone aus der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="f33e2-108">The **Get-AzDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="f33e2-109">Wenn Sie den Parameter *"Name"* angeben, wird ein einzelnes **"DnsZone"-Objekt** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f33e2-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="f33e2-110">Wenn Sie den Parameter *"Name" nicht angeben,* wird ein Array zurückgegeben, das alle Zonen in der angegebenen Ressourcengruppe enthält.</span><span class="sxs-lookup"><span data-stu-id="f33e2-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="f33e2-111">Sie können das **"DnsZone"-Objekt** verwenden, um die Zone zu aktualisieren, z. B. können Sie **"RecordSet"-Objekte** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f33e2-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="f33e2-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f33e2-112">EXAMPLES</span></span>

### <span data-ttu-id="f33e2-113">Beispiel 1: Zone erhalten</span><span class="sxs-lookup"><span data-stu-id="f33e2-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="f33e2-114">In diesem Beispiel wird die "myzone.com"-Zone mit dem Namen "myzone.com" aus der angegebenen Ressourcengruppe und dann in der variablen $Zone gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f33e2-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="f33e2-115">Beispiel 2: Alle Zonen in einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="f33e2-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="f33e2-116">Dieses Beispiel ruft alle DNS-Zonen in der angegebenen Ressourcengruppe ab und speichert sie dann in $Zones Variable.</span><span class="sxs-lookup"><span data-stu-id="f33e2-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="f33e2-117">Beispiel 3: Alle Zonen in einem Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="f33e2-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzDnsZone
```

<span data-ttu-id="f33e2-118">In diesem Beispiel werden alle DNS-Zonen im aktuellen Abonnement von Azure ab- und dann in der $Zones gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f33e2-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="f33e2-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f33e2-119">PARAMETERS</span></span>

### <span data-ttu-id="f33e2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f33e2-120">-DefaultProfile</span></span>
<span data-ttu-id="f33e2-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="f33e2-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f33e2-122">-Name</span><span class="sxs-lookup"><span data-stu-id="f33e2-122">-Name</span></span>
<span data-ttu-id="f33e2-123">Gibt den Namen der zu erhaltenden DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="f33e2-123">Specifies the name of the DNS zone to get.</span></span>
<span data-ttu-id="f33e2-124">Wenn Sie keinen Wert für den Parameter *"Name"* angeben, ruft dieses Cmdlet alle DNS-Zonen in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="f33e2-124">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="f33e2-125">Wenn Sie auch den Parameter *"ResourceGroupName"* weglassen, ruft dieses Cmdlet alle DNS-Zonen im aktuellen Abonnement von Azure ab.</span><span class="sxs-lookup"><span data-stu-id="f33e2-125">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f33e2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f33e2-126">-ResourceGroupName</span></span>
<span data-ttu-id="f33e2-127">Gibt den Namen der Ressourcengruppe an, die die zu erhaltende DNS-Zone enthält.</span><span class="sxs-lookup"><span data-stu-id="f33e2-127">Specifies the name of the resource group that contains the DNS zone to get.</span></span>
<span data-ttu-id="f33e2-128">Wenn Sie den *ResourceGroupName nicht* angeben, müssen Sie auch den Parameter *"Name"* weglassen.</span><span class="sxs-lookup"><span data-stu-id="f33e2-128">If you do not specify the *ResourceGroupName*, then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="f33e2-129">In diesem Fall ruft dieses Cmdlet alle DNS-Zonen im aktuellen Abonnement von Azure ab.</span><span class="sxs-lookup"><span data-stu-id="f33e2-129">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f33e2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f33e2-130">CommonParameters</span></span>
<span data-ttu-id="f33e2-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f33e2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f33e2-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f33e2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f33e2-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f33e2-133">INPUTS</span></span>

### <span data-ttu-id="f33e2-134">System.String</span><span class="sxs-lookup"><span data-stu-id="f33e2-134">System.String</span></span>

## <span data-ttu-id="f33e2-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f33e2-135">OUTPUTS</span></span>

### <span data-ttu-id="f33e2-136">Microsoft.Azure.Commands.Dns.DnsZone</span><span class="sxs-lookup"><span data-stu-id="f33e2-136">Microsoft.Azure.Commands.Dns.DnsZone</span></span>

## <span data-ttu-id="f33e2-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="f33e2-137">NOTES</span></span>

## <span data-ttu-id="f33e2-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="f33e2-138">RELATED LINKS</span></span>

[<span data-ttu-id="f33e2-139">New-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="f33e2-139">New-AzDnsZone</span></span>](./New-AzDnsZone.md)

[<span data-ttu-id="f33e2-140">Remove-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="f33e2-140">Remove-AzDnsZone</span></span>](./Remove-AzDnsZone.md)

[<span data-ttu-id="f33e2-141">Set-AzDnsZone</span><span class="sxs-lookup"><span data-stu-id="f33e2-141">Set-AzDnsZone</span></span>](./Set-AzDnsZone.md)
