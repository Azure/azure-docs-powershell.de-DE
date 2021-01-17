---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PrivateDns.dll-Help.xml
Module Name: Az.PrivateDns
online version: https://docs.microsoft.com/en-us/powershell/module/az.privatedns/get-azprivatednszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PrivateDns/PrivateDns/help/Get-AzPrivateDnsZone.md
ms.openlocfilehash: 3a909bcae464c70487ce4705bfaa43336776472b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98369745"
---
# <span data-ttu-id="e445e-101">Get-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="e445e-101">Get-AzPrivateDnsZone</span></span>

## <span data-ttu-id="e445e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e445e-102">SYNOPSIS</span></span>
<span data-ttu-id="e445e-103">Ruft eine private DNS-Zone ab.</span><span class="sxs-lookup"><span data-stu-id="e445e-103">Gets a Private DNS zone.</span></span>

## <span data-ttu-id="e445e-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e445e-104">SYNTAX</span></span>

```
Get-AzPrivateDnsZone [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e445e-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e445e-105">DESCRIPTION</span></span>
<span data-ttu-id="e445e-106">Das **Get-AzPrivateDnsZone-Cmdlet** ruft eine Zone des Privaten Domain Name Systems (DNS) aus der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e445e-106">The **Get-AzPrivateDnsZone** cmdlet gets a Private Domain Name System (DNS) zone from the specified resource group.</span></span>
<span data-ttu-id="e445e-107">Wenn Sie den Parameter *"Name"* angeben, wird ein **einzelnes "PrivateDnsZone"-Objekt** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e445e-107">If you specify the *Name* parameter, a single **PrivateDnsZone** object is returned.</span></span>
<span data-ttu-id="e445e-108">Wenn Sie den Parameter *"Name" nicht angeben,* wird ein Array zurückgegeben, das alle Zonen in der angegebenen Ressourcengruppe enthält.</span><span class="sxs-lookup"><span data-stu-id="e445e-108">If you do not specify the *Name* parameter, an array containing all of the zones in the specified resource group is returned.</span></span>
<span data-ttu-id="e445e-109">Sie können das **PrivateDnsZone-Objekt** verwenden, um die Zone zu aktualisieren, z. B. können Sie **"RecordSet"-Objekte** hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="e445e-109">You can use the **PrivateDnsZone** object to update the zone, for example you can add **RecordSet** objects to it.</span></span>

## <span data-ttu-id="e445e-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e445e-110">EXAMPLES</span></span>

### <span data-ttu-id="e445e-111">Beispiel 1: Zone erhalten</span><span class="sxs-lookup"><span data-stu-id="e445e-111">Example 1: Get a zone</span></span>
```
PS C:\> $Zone = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup" -Name "myzone.com"

This example gets the Private DNS zone named myzone.com from the specified resource group, and then stores it in the $Zone variable.
$Zone looks something like this: 

Name                          : myzone.com
ResourceId:                   : "/subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/PrivateZones/myzone.com"
ResourceGroupName             : MyResourceGroup
Location                      : 
Etag                          : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                          : {}
NumberOfRecordSets            : 1
MaxNumberOfRecordSets         : 5000
```

### <span data-ttu-id="e445e-112">Beispiel 2: Alle Zonen in einer Ressourcengruppe erhalten</span><span class="sxs-lookup"><span data-stu-id="e445e-112">Example 2: Get all of the zones in a resource group</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone -ResourceGroupName "MyResourceGroup"

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="e445e-113">Dieses Beispiel ruft alle privaten DNS-Zonen in der angegebenen Ressourcengruppe ab und speichert sie dann in $Zones Variable.</span><span class="sxs-lookup"><span data-stu-id="e445e-113">This example gets all of the Private DNS zones in the specified resource group, and then stores it in the $Zones variable.</span></span>

### <span data-ttu-id="e445e-114">Beispiel 3: Alle Zonen in einem Abonnement erhalten</span><span class="sxs-lookup"><span data-stu-id="e445e-114">Example 3: Get all of the zones in a subscription</span></span>
```
PS C:\> $Zones = Get-AzPrivateDnsZone

Name                  : zone1.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup1/providers/Micros
                        oft.Network/privateDnsZones/zone1.com
ResourceGroupName     : MyResourceGroup1
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000

Name                  : zone2.com
ResourceId            : /subscriptions/xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup2/providers/Micros
                        oft.Network/privateDnsZones/zone2.com
ResourceGroupName     : MyResourceGroup2
Location              :
Etag                  : xxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Tags                  :
NumberOfRecordSets    : 1
MaxNumberOfRecordSets : 5000
```

<span data-ttu-id="e445e-115">Dieses Beispiel ruft alle privaten DNS-Zonen im aktuellen Abonnement von Azure ab und speichert sie dann in $Zones Variable.</span><span class="sxs-lookup"><span data-stu-id="e445e-115">This example gets all of the Private DNS zones in the current Azure subscription, and then stores them in the $Zones variable.</span></span>

## <span data-ttu-id="e445e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e445e-116">PARAMETERS</span></span>

### <span data-ttu-id="e445e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e445e-117">-DefaultProfile</span></span>
<span data-ttu-id="e445e-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e445e-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e445e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="e445e-119">-Name</span></span>
<span data-ttu-id="e445e-120">Gibt den Namen der privaten DNS-Zone an, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="e445e-120">Specifies the name of the Private DNS zone to get.</span></span>
<span data-ttu-id="e445e-121">Wenn Sie keinen Wert für den Parameter *"Name"* angeben, ruft dieses Cmdlet alle privaten DNS-Zonen in der angegebenen Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="e445e-121">If you do not specify a value for the *Name* parameter, this cmdlet gets all Private DNS zones in the specified resource group.</span></span>
<span data-ttu-id="e445e-122">Wenn Sie auch den Parameter *"ResourceGroupName"* weglassen, ruft dieses Cmdlet alle privaten DNS-Zonen im aktuellen Abonnement von Azure ab.</span><span class="sxs-lookup"><span data-stu-id="e445e-122">If you also omit the *ResourceGroupName* parameter, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="e445e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e445e-123">-ResourceGroupName</span></span>
<span data-ttu-id="e445e-124">Gibt den Namen der Ressourcengruppe an, die die private DNS-Zone enthält, die sie erhalten soll.</span><span class="sxs-lookup"><span data-stu-id="e445e-124">Specifies the name of the resource group that contains the Private DNS zone to get.</span></span>
<span data-ttu-id="e445e-125">Wenn Sie den *ResourceGroupName nicht* angeben, müssen Sie auch den Parameter *"Name"* weglassen.</span><span class="sxs-lookup"><span data-stu-id="e445e-125">If you do not specify the *ResourceGroupName*, then you must also omit the *Name* parameter.</span></span>
<span data-ttu-id="e445e-126">In diesem Fall ruft dieses Cmdlet alle privaten DNS-Zonen im aktuellen Abonnement von Azure ab.</span><span class="sxs-lookup"><span data-stu-id="e445e-126">In this case, this cmdlet gets all Private DNS zones in the current Azure subscription.</span></span>

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

### <span data-ttu-id="e445e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e445e-127">CommonParameters</span></span>
<span data-ttu-id="e445e-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e445e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e445e-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e445e-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e445e-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e445e-130">INPUTS</span></span>

### <span data-ttu-id="e445e-131">Keine</span><span class="sxs-lookup"><span data-stu-id="e445e-131">None</span></span>

## <span data-ttu-id="e445e-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e445e-132">OUTPUTS</span></span>

### <span data-ttu-id="e445e-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="e445e-133">Microsoft.Azure.Commands.PrivateDns.Models.PSPrivateDnsZone</span></span>

## <span data-ttu-id="e445e-134">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e445e-134">NOTES</span></span>

## <span data-ttu-id="e445e-135">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e445e-135">RELATED LINKS</span></span>

[<span data-ttu-id="e445e-136">New-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="e445e-136">New-AzPrivateDnsZone</span></span>](./New-AzPrivateDnsZone.md)

[<span data-ttu-id="e445e-137">Remove-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="e445e-137">Remove-AzPrivateDnsZone</span></span>](./Remove-AzPrivateDnsZone.md)

[<span data-ttu-id="e445e-138">Set-AzPrivateDnsZone</span><span class="sxs-lookup"><span data-stu-id="e445e-138">Set-AzPrivateDnsZone</span></span>](./Set-AzPrivateDnsZone.md)
