---
external help file: Microsoft.Azure.Commands.Dns.dll-Help.xml
Module Name: AzureRM.Dns
ms.assetid: B78F3E8B-C7D2-458C-AB23-06F584FE97E0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.dns/new-azurermdnszone
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Dns/Commands.Dns/help/New-AzureRmDnsZone.md
ms.openlocfilehash: 28fabce7590644c230643822c206515957839127
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662853"
---
# <span data-ttu-id="6ce21-101">New-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="6ce21-101">New-AzureRmDnsZone</span></span>

## <span data-ttu-id="6ce21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6ce21-102">SYNOPSIS</span></span>
<span data-ttu-id="6ce21-103">Erstellt eine neue DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="6ce21-103">Creates a new DNS zone.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6ce21-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6ce21-104">SYNTAX</span></span>

### <span data-ttu-id="6ce21-105">IDs (Standard)</span><span class="sxs-lookup"><span data-stu-id="6ce21-105">Ids (Default)</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-ResolutionVirtualNetworkId <System.Collections.Generic.List`1[System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ce21-106">Objekte</span><span class="sxs-lookup"><span data-stu-id="6ce21-106">Objects</span></span>
```
New-AzureRmDnsZone -Name <String> -ResourceGroupName <String> [-ZoneType <ZoneType>] [-Tag <Hashtable>]
 [-RegistrationVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-ResolutionVirtualNetwork <System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ce21-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6ce21-107">DESCRIPTION</span></span>
<span data-ttu-id="6ce21-108">Das Cmdlet **New-AzureRmDnsZone** erstellt eine neue DNS-Zone (Domain Name System) in der angegebenen Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="6ce21-108">The **New-AzureRmDnsZone** cmdlet creates a new Domain Name System (DNS) zone in the specified resource group.</span></span> <span data-ttu-id="6ce21-109">Sie müssen einen eindeutigen DNS-Zonennamen für den Parameter *Name* angeben, oder das Cmdlet gibt einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="6ce21-109">You must specify a unique DNS zone name for the *Name* parameter or the cmdlet will return an error.</span></span> <span data-ttu-id="6ce21-110">Verwenden Sie nach der Erstellung der Zone das New-AzureRmDnsRecordSet-Cmdlet, um Daten Satz Sätze in der Zone zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="6ce21-110">After the zone is created, use the New-AzureRmDnsRecordSet cmdlet to create record sets in the zone.</span></span>

<span data-ttu-id="6ce21-111">Sie können den Parameter *Confirm* und $ConfirmPreference Windows PowerShell-Variable verwenden, um zu steuern, ob das Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="6ce21-111">You can use the *Confirm* parameter and $ConfirmPreference Windows PowerShell variable to control whether the cmdlet prompts you for confirmation.</span></span>

## <span data-ttu-id="6ce21-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6ce21-112">EXAMPLES</span></span>

### <span data-ttu-id="6ce21-113">Beispiel 1: Erstellen einer DNS-Zone</span><span class="sxs-lookup"><span data-stu-id="6ce21-113">Example 1: Create a DNS zone</span></span>
```
PS C:\>$Zone = New-AzureRmDnsZone -Name "myzone.com" -ResourceGroupName "MyResourceGroup"
```

<span data-ttu-id="6ce21-114">Dieser Befehl erstellt eine neue DNS-Zone mit dem Namen MyZone.com in der angegebenen Ressourcengruppe und speichert Sie dann in der $Zone-Variablen.</span><span class="sxs-lookup"><span data-stu-id="6ce21-114">This command creates a new DNS zone named myzone.com in the specified resource group, and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="6ce21-115">Beispiel 2: Erstellen einer privaten DNS-Zone durch Angabe virtueller Netzwerk-IDs</span><span class="sxs-lookup"><span data-stu-id="6ce21-115">Example 2: Create a Private DNS zone by specifying virtual network IDs</span></span>
```
PS C:\>$ResVirtualNetworkId = "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/testresgroup/providers/Microsoft.Network/virtualNetworks/resvnet"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetworkId @($ResVirtualNetworkId)
```

<span data-ttu-id="6ce21-116">Mit diesem Befehl wird eine neue private DNS-Zone mit dem Namen myprivatezone.com in der angegebenen Ressourcengruppe mit einem zugehörigen Auflösungs-virtuellen Netzwerk (Angabe der ID) erstellt und dann in der $Zone-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6ce21-116">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (specifying its ID), and then stores it in the $Zone variable.</span></span>

### <span data-ttu-id="6ce21-117">Beispiel 3: Erstellen einer privaten DNS-Zone durch angeben virtueller Netzwerkobjekte</span><span class="sxs-lookup"><span data-stu-id="6ce21-117">Example 3: Create a Private DNS zone by specifying virtual network objects</span></span>
```
PS C:\>$ResVirtualNetwork = Get-AzureRmVirtualNetwork -Name "resvnet" -ResourceGroupName "testresgroup"
PS C:\>$Zone = New-AzureRmDnsZone -Name "myprivatezone.com" -ResourceGroupName "MyResourceGroup" -ZoneType Private -ResolutionVirtualNetwork @($ResVirtualNetwork)
```

<span data-ttu-id="6ce21-118">Mit diesem Befehl wird eine neue private DNS-Zone mit dem Namen myprivatezone.com in der angegebenen Ressourcengruppe mit einem virtuellen Netzwerk für die Auflösung erstellt (auf das durch $ResVirtualNetwork Variable verwiesen wird) und dann in der $Zone-Variablen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6ce21-118">This command creates a new Private DNS zone named myprivatezone.com in the specified resource group with an associated resolution virtual network (referred to by $ResVirtualNetwork variable), and then stores it in the $Zone variable.</span></span>

## <span data-ttu-id="6ce21-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="6ce21-119">PARAMETERS</span></span>

### <span data-ttu-id="6ce21-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ce21-120">-DefaultProfile</span></span>
<span data-ttu-id="6ce21-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6ce21-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6ce21-122">-Name</span><span class="sxs-lookup"><span data-stu-id="6ce21-122">-Name</span></span>
<span data-ttu-id="6ce21-123">Gibt den Namen der zu erstellende DNS-Zone an.</span><span class="sxs-lookup"><span data-stu-id="6ce21-123">Specifies the name of the DNS zone to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce21-124">-RegistrationVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ce21-124">-RegistrationVirtualNetwork</span></span>
<span data-ttu-id="6ce21-125">In der Liste der virtuellen Netzwerke, die die Hostnamen für virtuelle Maschinen registrieren, werden die Datensätze in dieser DNS-Zone nur für private Zonen zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="6ce21-125">The list of virtual networks that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce21-126">-RegistrationVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="6ce21-126">-RegistrationVirtualNetworkId</span></span>
<span data-ttu-id="6ce21-127">Die Liste der virtuellen Netzwerk-IDs, die Hostnamen für virtuelle Maschinen in dieser DNS-Zone registrieren, die nur für private Zonen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6ce21-127">The list of virtual network IDs that will register virtual machine hostnames records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce21-128">-ResolutionVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="6ce21-128">-ResolutionVirtualNetwork</span></span>
<span data-ttu-id="6ce21-129">Die Liste der virtuellen Netzwerke, in denen Datensätze in dieser DNS-Zone aufgelöst werden können, die nur für private Zonen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6ce21-129">The list of virtual networks able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Internal.Network.Common.IResourceReference]
Parameter Sets: Objects
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce21-130">-ResolutionVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="6ce21-130">-ResolutionVirtualNetworkId</span></span>
<span data-ttu-id="6ce21-131">Die Liste der virtuellen Netzwerk-IDs, mit denen Datensätze in dieser DNS-Zone aufgelöst werden können, die nur für private Zonen verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="6ce21-131">The list of virtual network IDs able to resolve records in this DNS zone, only available for private zones.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Ids
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce21-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ce21-132">-ResourceGroupName</span></span>
<span data-ttu-id="6ce21-133">Gibt die Ressourcengruppe an, in der die Zone erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="6ce21-133">Specifies the resource group in which to create the zone.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce21-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="6ce21-134">-Tag</span></span>
<span data-ttu-id="6ce21-135">Schlüssel-Wert-Paare in Form einer Hashtabelle</span><span class="sxs-lookup"><span data-stu-id="6ce21-135">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="6ce21-136">Zum Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6ce21-136">For example:</span></span>

<span data-ttu-id="6ce21-137">@ {KEY0 = "value0"; key1 = $NULL; key2 = "Value2"}</span><span class="sxs-lookup"><span data-stu-id="6ce21-137">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce21-138">-Zonetype</span><span class="sxs-lookup"><span data-stu-id="6ce21-138">-ZoneType</span></span>
<span data-ttu-id="6ce21-139">Der Typ der Zone, öffentlich oder privat.</span><span class="sxs-lookup"><span data-stu-id="6ce21-139">The type of the zone, Public or Private.</span></span> <span data-ttu-id="6ce21-140">Zonen ohne Typ oder mit einem öffentlichen Typ werden auf der öffentlichen DNS-Dienstebene zur Verwendung in der DNS-Hierarchie zur Verfügung gestellt.</span><span class="sxs-lookup"><span data-stu-id="6ce21-140">Zones without a type or with a type of Public are made available on the public DNS serving plane for use in the DNS hierarchy.</span></span> <span data-ttu-id="6ce21-141">Zonen mit einem privaten Typ werden nur aus dem Satz der zugeordneten virtuellen Netzwerke angezeigt (dieses Feature befindet sich in der Vorschau).</span><span class="sxs-lookup"><span data-stu-id="6ce21-141">Zones with a type of Private are only visible from with the set of associated virtual networks (this feature is in preview).</span></span> <span data-ttu-id="6ce21-142">Diese Eigenschaft kann für eine Zone nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6ce21-142">This property cannot be changed for a zone.</span></span>

```yaml
Type: ZoneType
Parameter Sets: (All)
Aliases:
Accepted values: Public, Private

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ce21-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6ce21-143">-Confirm</span></span>
<span data-ttu-id="6ce21-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6ce21-144">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce21-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ce21-145">-WhatIf</span></span>
<span data-ttu-id="6ce21-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ce21-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ce21-147">Das Cmdlet wird nicht ausgeführt. Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ce21-147">The cmdlet is not run.Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6ce21-148">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ce21-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ce21-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ce21-149">CommonParameters</span></span>
<span data-ttu-id="6ce21-150">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ce21-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ce21-151">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ce21-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ce21-152">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6ce21-152">INPUTS</span></span>

### <span data-ttu-id="6ce21-153">Keine</span><span class="sxs-lookup"><span data-stu-id="6ce21-153">None</span></span>
<span data-ttu-id="6ce21-154">Sie können keine Eingabe an dieses Cmdlet übergeben.</span><span class="sxs-lookup"><span data-stu-id="6ce21-154">You cannot pipe input to this cmdlet.</span></span>

## <span data-ttu-id="6ce21-155">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6ce21-155">OUTPUTS</span></span>

### <span data-ttu-id="6ce21-156">Microsoft. Azure. Commands. DNS. dnsZone</span><span class="sxs-lookup"><span data-stu-id="6ce21-156">Microsoft.Azure.Commands.Dns.DnsZone</span></span>
<span data-ttu-id="6ce21-157">Dieses Cmdlet gibt ein Microsoft. Azure. Commands. DNS. dnsZone-Objekt zurück, das die neue DNS-Zone darstellt.</span><span class="sxs-lookup"><span data-stu-id="6ce21-157">This cmdlet returns a Microsoft.Azure.Commands.Dns.DnsZone object that represents the new DNS zone.</span></span>

## <span data-ttu-id="6ce21-158">Notizen</span><span class="sxs-lookup"><span data-stu-id="6ce21-158">NOTES</span></span>
<span data-ttu-id="6ce21-159">Sie können den Parameter *Confirm* verwenden, um zu steuern, ob dieses Cmdlet Sie zur Bestätigung auffordert.</span><span class="sxs-lookup"><span data-stu-id="6ce21-159">You can use the *Confirm* parameter to control whether this cmdlet prompts you for confirmation.</span></span>
<span data-ttu-id="6ce21-160">Standardmäßig werden Sie vom Cmdlet zur Bestätigung aufgefordert, wenn die $ConfirmPreference Windows PowerShell-Variable einen Wert von Mittel oder niedriger aufweist.</span><span class="sxs-lookup"><span data-stu-id="6ce21-160">By default, the cmdlet prompts you for confirmation if the $ConfirmPreference Windows PowerShell variable has a value of Medium or lower.</span></span>

<span data-ttu-id="6ce21-161">Wenn Sie *bestätigen* oder *bestätigen: $true* angeben, werden Sie von diesem Cmdlet zur Bestätigung aufgefordert, bevor es ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6ce21-161">If you specify *Confirm* or *Confirm:$True* , this cmdlet prompts you for confirmation before it runs.</span></span>
<span data-ttu-id="6ce21-162">Wenn Sie *Confirm: $false* angeben, werden Sie vom Cmdlet nicht zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="6ce21-162">If you specify *Confirm:$False* , the cmdlet does not prompt you for confirmation.</span></span>

## <span data-ttu-id="6ce21-163">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6ce21-163">RELATED LINKS</span></span>

[<span data-ttu-id="6ce21-164">Get-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="6ce21-164">Get-AzureRmDnsZone</span></span>](./Get-AzureRmDnsZone.md)

[<span data-ttu-id="6ce21-165">Neu – AzureRmDnsRecordSet</span><span class="sxs-lookup"><span data-stu-id="6ce21-165">New-AzureRmDnsRecordSet</span></span>](./New-AzureRmDnsRecordSet.md)

[<span data-ttu-id="6ce21-166">Remove-AzureRmDnsZone</span><span class="sxs-lookup"><span data-stu-id="6ce21-166">Remove-AzureRmDnsZone</span></span>](./Remove-AzureRmDnsZone.md)
