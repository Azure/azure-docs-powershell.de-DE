---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
ms.assetid: B831ABE6-348C-4DD6-9295-18D23A1FDF63
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8b71c522a8d4dc006428ca2a400160a0ce7ce68b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93850023"
---
# <span data-ttu-id="320e9-101">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="320e9-101">Get-AzureRmDnsZone</span></span>

## <span data-ttu-id="320e9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="320e9-102">SYNOPSIS</span></span>
<span data-ttu-id="320e9-103">Ruft eine DNS-Zone ab.</span><span class="sxs-lookup"><span data-stu-id="320e9-103">Gets a DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="320e9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="320e9-104">SYNTAX</span></span>

### <span data-ttu-id="320e9-105">Standard (Standard)</span><span class="sxs-lookup"><span data-stu-id="320e9-105">Default (Default)</span></span>
```
Get-AzureRmDnsZone [<CommonParameters>]
```

### <span data-ttu-id="320e9-106">ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="320e9-106">ResourceGroup</span></span>
```
Get-AzureRmDnsZone [-Name <String>] -ResourceGroupName <String> [<CommonParameters>]
```

## <span data-ttu-id="320e9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="320e9-107">DESCRIPTION</span></span>
<span data-ttu-id="320e9-108">Das Cmdlet " **Get-AzureRmDnsZone** " Ruft eine DNS-Zone (Domain Name System) aus der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="320e9-108">The **Get-AzureRmDnsZone** cmdlet gets a Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="320e9-109">Wenn Sie den Parameter *Name* angeben, wird ein einzelnes **dnsZone** -Objekt zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="320e9-109">If you specify the *Name* parameter, a single **DnsZone** object is returned.</span></span>
<span data-ttu-id="320e9-110">Wenn Sie den Parameter *Name* nicht angeben, wird ein Array zurückgegeben, das alle Zonen in der angegebenen Ressourcengruppe enthält.</span><span class="sxs-lookup"><span data-stu-id="320e9-110">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="320e9-111">Sie können das **dnsZone** -Objekt verwenden, um die Zone zu aktualisieren, beispielsweise können Sie **Recordset** -Objekte hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="320e9-111">You can use the **DnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="320e9-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="320e9-112">EXAMPLES</span></span>

### <span data-ttu-id="320e9-113">Beispiel 1: Abrufen einer Zone</span><span class="sxs-lookup"><span data-stu-id="320e9-113">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"
```

<span data-ttu-id="320e9-114">In diesem Beispiel wird die DNS-Zone mit dem Namen MyZone.com aus der angegebenen Ressourcengruppe abgerufen und dann in der $Zone-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="320e9-114">This example gets the DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="320e9-115">Beispiel 2: Abrufen aller Zonen in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="320e9-115">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="320e9-116">In diesem Beispiel werden alle DNS-Zonen in der angegebenen Ressourcengruppe abgerufen und dann in der $Zones-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="320e9-116">This example gets all of the DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="320e9-117">Beispiel 3: Abrufen aller Zonen in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="320e9-117">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzureRmDnsZone
```

<span data-ttu-id="320e9-118">In diesem Beispiel werden alle DNS-Zonen im aktuellen Azure-Abonnement abgerufen und dann in der $Zones-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="320e9-118">This example gets all of the DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="320e9-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="320e9-119">PARAMETERS</span></span>

### <span data-ttu-id="320e9-120">-Name</span><span class="sxs-lookup"><span data-stu-id="320e9-120">-Name</span></span>
<span data-ttu-id="320e9-121">Gibt den Namen der abzurufenden DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="320e9-121">Specifies the name of the DNS zone to get.</span></span>

<span data-ttu-id="320e9-122">Wenn Sie keinen Wert für den Parameter *Name* angeben, ruft dieses Cmdlet alle DNS-Zonen in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="320e9-122">If you do not specify a value for the *Name* parameter, this cmdlet gets all DNS zones in the specified resource group.</span></span>
<span data-ttu-id="320e9-123">Wenn Sie auch den *ResourceGroupName* -Parameter weglassen, ruft dieses Cmdlet alle DNS-Zonen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="320e9-123">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="320e9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="320e9-124">-ResourceGroupName</span></span>
<span data-ttu-id="320e9-125">Gibt den Namen der Ressourcengruppe an, die die DNS-Zone enthält, die abgerufen werden soll.</span><span class="sxs-lookup"><span data-stu-id="320e9-125">Specifies the name of the resource group that contains the DNS zone to get.</span></span>

<span data-ttu-id="320e9-126">Wenn Sie das *ResourceGroupName* nicht angeben, müssen Sie auch den Parameter *Name* weglassen.</span><span class="sxs-lookup"><span data-stu-id="320e9-126">If you do not specify the *ResourceGroupName* , then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="320e9-127">In diesem Fall ruft dieses Cmdlet alle DNS-Zonen im aktuellen Azure-Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="320e9-127">In this case, this cmdlet gets all DNS zones in the current Azure subscription.</span></span>

```yaml
Type: String
Parameter Sets: ResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="320e9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="320e9-128">CommonParameters</span></span>
<span data-ttu-id="320e9-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="320e9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="320e9-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="320e9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="320e9-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="320e9-131">INPUTS</span></span>

### <span data-ttu-id="320e9-132">Keine</span><span class="sxs-lookup"><span data-stu-id="320e9-132">None</span></span>
<span data-ttu-id="320e9-133">Mit diesem Cmdlet können Sie keine Pipe-Eingabe durchleiten.</span><span class="sxs-lookup"><span data-stu-id="320e9-133">This cmdlet does not allow you to pipe input.</span></span>

## <span data-ttu-id="320e9-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="320e9-134">OUTPUTS</span></span>

### <span data-ttu-id="320e9-135">Microsoft. Azure. Commands. DNS. dnsZone</span><span class="sxs-lookup"><span data-stu-id="320e9-135">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="320e9-136">Dieses Cmdlet gibt ein Objekt zurück, das die DNS-Zone darstellt.</span><span class="sxs-lookup"><span data-stu-id="320e9-136">This cmdlet returns an object that represents the DNS zone.</span></span>
<span data-ttu-id="320e9-137">Wenn der Zonen Name nicht angegeben wird, wird ein Array von Zone-Objekten zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="320e9-137">If the zone name is not specified, an array of zone objects is returned.</span></span>

## <span data-ttu-id="320e9-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="320e9-138">NOTES</span></span>

## <span data-ttu-id="320e9-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="320e9-139">RELATED LINKS</span></span>

[<span data-ttu-id="320e9-140">Neu – AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="320e9-140">New-AzureRmDnsZone</span></span>](./New-AzureRmDnsZone.md)

[<span data-ttu-id="320e9-141">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="320e9-141">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)

[<span data-ttu-id="320e9-142">Satz-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="320e9-142">Set-AzureRmDnsZone</span></span>](./Set-AzureRmDnsZone.md)
