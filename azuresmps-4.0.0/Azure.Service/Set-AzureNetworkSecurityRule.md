---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.Network.dll-Help.xml
ms.assetid: 125B6865-0022-4F88-BB0F-DDDDB2EDFF00
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2a1f1d033c3e8bae708310d12a1c4cb2b581bf80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006006"
---
# <span data-ttu-id="a5a6e-101">Set-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="a5a6e-101">Set-AzureNetworkSecurityRule</span></span>

## <span data-ttu-id="a5a6e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a5a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a6e-103">Fügt eine Netzwerk Sicherheitsregel in einer Netzwerksicherheitsgruppe hinzu oder ändert diese.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-103">Adds or modifies a network security rule in a network security group.</span></span>

## <span data-ttu-id="a5a6e-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5a6e-104">SYNTAX</span></span>

```
Set-AzureNetworkSecurityRule -Name <String> -Type <String> -Priority <Int32> -Action <String>
 -SourceAddressPrefix <String> -SourcePortRange <String> -DestinationAddressPrefix <String>
 -DestinationPortRange <String> -Protocol <String> -NetworkSecurityGroup <INetworkSecurityGroup>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="a5a6e-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a5a6e-105">DESCRIPTION</span></span>
<span data-ttu-id="a5a6e-106">Das Cmdlet " **Satz-AzureNetworkSecurityRule** " fügt eine Azure Network Security-Regel in einer Netzwerksicherheitsgruppe hinzu oder ändert diese.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-106">The **Set-AzureNetworkSecurityRule** cmdlet adds or modifies an Azure network security rule in a network security group.</span></span>

## <span data-ttu-id="a5a6e-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a5a6e-107">EXAMPLES</span></span>

## <span data-ttu-id="a5a6e-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="a5a6e-108">PARAMETERS</span></span>

### <span data-ttu-id="a5a6e-109">– Aktion</span><span class="sxs-lookup"><span data-stu-id="a5a6e-109">-Action</span></span>
<span data-ttu-id="a5a6e-110">Gibt die Aktion für eine Netzwerk Sicherheitsregel an.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-110">Specifies the action for a network security rule.</span></span>
<span data-ttu-id="a5a6e-111">Gültige Werte sind: allow und Deny.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-111">Valid values are: Allow and Deny.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-112">-DestinationAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a5a6e-112">-DestinationAddressPrefix</span></span>
<span data-ttu-id="a5a6e-113">Gibt die CIDR-Adresse (classlos InterDomain Routing) des Ziel-IP-Bereichs für die Netzwerk Sicherheitsregel an.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-113">Specifies the Classless Interdomain Routing (CIDR) address of the destination IP range for the network security rule.</span></span>
<span data-ttu-id="a5a6e-114">Ein Sternchen (\*) gibt eine beliebige IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-114">An asterisk (\*) specifies any IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-115">-DestinationPortRange</span><span class="sxs-lookup"><span data-stu-id="a5a6e-115">-DestinationPortRange</span></span>
<span data-ttu-id="a5a6e-116">Gibt einen Ziel Portbereich für die Netzwerk Sicherheitsregel an.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-116">Specifies a destination port range for the network security rule.</span></span>
<span data-ttu-id="a5a6e-117">Gültige Werte bestehen aus ganzen Zahlen von 0 bis 65535.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-117">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="a5a6e-118">Sie können einen einzelnen Wert angeben oder einen Bereich im Format LowerNumber-HigherNumber angeben.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-118">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="a5a6e-119">Ein Bindestrich trennt die beiden Werte.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-119">A hyphen separates the two values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="a5a6e-120">-Name</span></span>
<span data-ttu-id="a5a6e-121">Gibt den Namen für die Netzwerk Sicherheitsregel an, die von diesem Cmdlet hinzugefügt oder geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-121">Specifies the name for the network security rule that this cmdlet adds or modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-122">-NetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="a5a6e-122">-NetworkSecurityGroup</span></span>
<span data-ttu-id="a5a6e-123">Gibt die Netzwerksicherheitsgruppe an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-123">Specifies the network security group that this cmdlet modifies.</span></span>
<span data-ttu-id="a5a6e-124">Verwenden Sie das Get-AzureNetworkSecurityGroup-Cmdlet, um ein **INetworkSecurityGroup** -Objekt zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-124">To obtain an **INetworkSecurityGroup** object, use the Get-AzureNetworkSecurityGroup cmdlet.</span></span>

```yaml
Type: INetworkSecurityGroup
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-125">-Priorität</span><span class="sxs-lookup"><span data-stu-id="a5a6e-125">-Priority</span></span>
<span data-ttu-id="a5a6e-126">Gibt die Priorität für die Netzwerk Sicherheitsregel an.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-126">Specifies the priority for the network security rule.</span></span>
<span data-ttu-id="a5a6e-127">Gültige Werte sind: ganze Zahlen von 100 bis 4096.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-127">Valid values are: integers from 100 to 4096.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-128">-Profil</span><span class="sxs-lookup"><span data-stu-id="a5a6e-128">-Profile</span></span>
<span data-ttu-id="a5a6e-129">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-129">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="a5a6e-130">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-130">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-131">-Protokoll</span><span class="sxs-lookup"><span data-stu-id="a5a6e-131">-Protocol</span></span>
<span data-ttu-id="a5a6e-132">Gibt das Protokoll für die Netzwerk Sicherheitsregel an.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-132">Specifies the protocol for the network security rule.</span></span>
<span data-ttu-id="a5a6e-133">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="a5a6e-133">Valid values are:</span></span> 

- <span data-ttu-id="a5a6e-134">TCP</span><span class="sxs-lookup"><span data-stu-id="a5a6e-134">TCP</span></span> 
- <span data-ttu-id="a5a6e-135">UDP</span><span class="sxs-lookup"><span data-stu-id="a5a6e-135">UDP</span></span> 
- *

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-136">-SourceAddressPrefix</span><span class="sxs-lookup"><span data-stu-id="a5a6e-136">-SourceAddressPrefix</span></span>
<span data-ttu-id="a5a6e-137">Gibt die CIDR-Adresse des Quell-IP-Bereichs für die Netzwerk Sicherheitsregel an.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-137">Specifies the CIDR address of the source IP range for the network security rule.</span></span>
<span data-ttu-id="a5a6e-138">Ein Sternchen (\*) gibt eine beliebige IP-Adresse an.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-138">An asterisk (\*) specifies any IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-139">-SourcePortRange</span><span class="sxs-lookup"><span data-stu-id="a5a6e-139">-SourcePortRange</span></span>
<span data-ttu-id="a5a6e-140">Gibt einen Quellportbereich für die Netzwerk Sicherheitsregel an.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-140">Specifies a source port range for the network security rule.</span></span>
<span data-ttu-id="a5a6e-141">Gültige Werte bestehen aus ganzen Zahlen von 0 bis 65535.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-141">Valid values consist of integers from 0 to 65535.</span></span>
<span data-ttu-id="a5a6e-142">Sie können einen einzelnen Wert angeben oder einen Bereich im Format LowerNumber-HigherNumber angeben.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-142">You can specify an individual value, or specify a range in the format LowerNumber-HigherNumber.</span></span>
<span data-ttu-id="a5a6e-143">Ein Bindestrich trennt die beiden Werte.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-143">A hyphen separates the two values.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-144">-Typ</span><span class="sxs-lookup"><span data-stu-id="a5a6e-144">-Type</span></span>
<span data-ttu-id="a5a6e-145">Gibt den Verbindungstyp für die Netzwerk Sicherheitsregel an.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-145">Specifies the type of connection for the network security rule.</span></span>
<span data-ttu-id="a5a6e-146">Gültige Werte sind: ein-und ausgehende Daten.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-146">Valid values are: Inbound and Outbound.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5a6e-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a6e-147">CommonParameters</span></span>
<span data-ttu-id="a5a6e-148">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a6e-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a6e-149">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a6e-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a6e-150">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a5a6e-150">INPUTS</span></span>

## <span data-ttu-id="a5a6e-151">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a5a6e-151">OUTPUTS</span></span>

## <span data-ttu-id="a5a6e-152">Notizen</span><span class="sxs-lookup"><span data-stu-id="a5a6e-152">NOTES</span></span>

## <span data-ttu-id="a5a6e-153">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a5a6e-153">RELATED LINKS</span></span>

[<span data-ttu-id="a5a6e-154">Remove-AzureNetworkSecurityRule</span><span class="sxs-lookup"><span data-stu-id="a5a6e-154">Remove-AzureNetworkSecurityRule</span></span>](./Remove-AzureNetworkSecurityRule.md)


