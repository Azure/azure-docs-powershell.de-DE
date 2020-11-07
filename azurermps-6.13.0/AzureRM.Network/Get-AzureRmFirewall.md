---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 91D58F60-F22A-454A-B04C-E5AEF33E9D06
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmFirewall.md
ms.openlocfilehash: cdaa9689919d2e307434d888b435dad9d29e105e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664825"
---
# <span data-ttu-id="6cfe6-101">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="6cfe6-101">Get-AzureRmFirewall</span></span>

## <span data-ttu-id="6cfe6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6cfe6-102">SYNOPSIS</span></span>
<span data-ttu-id="6cfe6-103">Ruft eine Azure-Firewall ab.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-103">Gets a Azure Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6cfe6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cfe6-104">SYNTAX</span></span>

```
Get-AzureRmFirewall [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6cfe6-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cfe6-105">DESCRIPTION</span></span>
<span data-ttu-id="6cfe6-106">Das Cmdlet " **Get-AzureRmFirewall** " ruft mindestens eine Firewall in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-106">The **Get-AzureRmFirewall** cmdlet gets one or more Firewalls in a resource group.</span></span>

## <span data-ttu-id="6cfe6-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6cfe6-107">EXAMPLES</span></span>

### <span data-ttu-id="6cfe6-108">1: Abrufen aller Firewalls in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="6cfe6-108">1:  Retrieve all Firewalls in a resource group</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName
```

<span data-ttu-id="6cfe6-109">In diesem Beispiel werden alle Firewalls in der Ressourcengruppe "rgName" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-109">This example retrieves all Firewalls in resource group "rgName".</span></span>

### <span data-ttu-id="6cfe6-110">2: Abrufen einer Firewall nach Namen</span><span class="sxs-lookup"><span data-stu-id="6cfe6-110">2:  Retrieve a Firewall by name</span></span>
```
Get-AzureRmFirewall -ResourceGroupName rgName -Name azFw
```

<span data-ttu-id="6cfe6-111">In diesem Beispiel wird die Firewall mit dem Namen "azFw" in der Ressourcengruppe "rgName" abgerufen.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-111">This example retrieves Firewall named "azFw" in resource group "rgName".</span></span>

### <span data-ttu-id="6cfe6-112">3: Abrufen einer Firewall und anschließendes Hinzufügen einer Anwendungsregel Sammlung zur Firewall</span><span class="sxs-lookup"><span data-stu-id="6cfe6-112">3:  Retrieve a firewall and then add a application rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$appRule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$appRuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name "MyAppRuleCollection" -Priority 100 -Rule $appRule -ActionType "Allow"
$azFw.AddApplicationRuleCollection($appRuleCollection)
```

<span data-ttu-id="6cfe6-113">In diesem Beispiel wird eine Firewall abgerufen und dann der Firewall eine Anwendungsregel Sammlung hinzugefügt, indem die AddApplicationRuleCollection-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-113">This example retrieves a firewall, then adds a application rule collection to the firewall by calling method AddApplicationRuleCollection.</span></span>

### <span data-ttu-id="6cfe6-114">4: Abrufen einer Firewall und anschließendes Hinzufügen einer Netzwerkregel Sammlung zur Firewall</span><span class="sxs-lookup"><span data-stu-id="6cfe6-114">4:  Retrieve a firewall and then add a network rule collection to the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$netRule = New-AzureRmFirewallNetworkRule -Name "all-udp-traffic" -Description "Rule for all UDP traffic" -Protocol "Udp" -SourceAddress "*" -DestinationAddress "*" -DestinationPort "*"
$netRuleCollection = New-AzureRmFirewallNetworkRuleCollection -Name "MyNetworkRuleCollection" -Priority 100 -Rule $netRule -ActionType "Allow"
$azFw.AddNetworkRuleCollection($netRuleCollection)
```

<span data-ttu-id="6cfe6-115">In diesem Beispiel wird eine Firewall abgerufen und dann der Firewall eine Netzwerkregel Sammlung hinzugefügt, indem die AddNetworkRuleCollection-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-115">This example retrieves a firewall, then adds a network rule collection to the firewall by calling method AddNetworkRuleCollection.</span></span>

### <span data-ttu-id="6cfe6-116">5: Abrufen einer Firewall und anschließendes Abrufen einer APP-Regelsammlung nach Namen aus der Firewall</span><span class="sxs-lookup"><span data-stu-id="6cfe6-116">5:  Retrieve a firewall and then retrieve a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getAppRc=$azFw.GetApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="6cfe6-117">In diesem Beispiel wird eine Firewall abgerufen, und dann wird eine Regelsammlung nach Name aufgerufen, die für das GetApplicationRuleCollectionByName-Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-117">This example retrieves a firewall and then gets a rule collection by name, calling method GetApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="6cfe6-118">Der Name der Regelsammlung für Methoden-GetApplicationRuleCollectionByName ist keine Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-118">The rule collection name for method GetApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="6cfe6-119">6: Abrufen einer Firewall und Abrufen einer Netzwerkregel Sammlung nach Namen aus der Firewall</span><span class="sxs-lookup"><span data-stu-id="6cfe6-119">6:  Retrieve a firewall and then retrieve a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$getNetRc=$azFw.GetNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="6cfe6-120">In diesem Beispiel wird eine Firewall abgerufen, und dann wird eine Regelsammlung nach Name aufgerufen, die für das GetNetworkRuleCollectionByName-Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-120">This example retrieves a firewall and then gets a rule collection by name, calling method GetNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="6cfe6-121">Der Name der Regelsammlung für Methoden-GetNetworkRuleCollectionByName ist keine Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-121">The rule collection name for method GetNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="6cfe6-122">7: Rufen Sie eine Firewall ab, und entfernen Sie dann eine Anwendung Regelsammlung nach Namen aus der Firewall.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-122">7:  Retrieve a firewall and then remove a application rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveApplicationRuleCollectionByName("MyAppRuleCollection")
```

<span data-ttu-id="6cfe6-123">In diesem Beispiel wird eine Firewall abgerufen, und anschließend wird eine Regelsammlung nach Name aufgerufen, wobei die RemoveApplicationRuleCollectionByName-Methode für das Firewall-Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-123">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveApplicationRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="6cfe6-124">Der Name der Regelsammlung für Methoden-RemoveApplicationRuleCollectionByName ist keine Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-124">The rule collection name for method RemoveApplicationRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="6cfe6-125">8: Abrufen einer Firewall und Entfernen einer Netzwerkregel Sammlung nach Namen aus der Firewall</span><span class="sxs-lookup"><span data-stu-id="6cfe6-125">8:  Retrieve a firewall and then remove a network rule collection by name from the Firewall</span></span>
```
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.RemoveNetworkRuleCollectionByName("MyNetworkRuleCollection")
```

<span data-ttu-id="6cfe6-126">In diesem Beispiel wird eine Firewall abgerufen, und anschließend wird eine Regelsammlung nach Name aufgerufen, wobei die RemoveNetworkRuleCollectionByName-Methode für das Firewall-Objekt aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-126">This example retrieves a firewall and then removes a rule collection by name, calling method RemoveNetworkRuleCollectionByName on the firewall object.</span></span> <span data-ttu-id="6cfe6-127">Der Name der Regelsammlung für Methoden-RemoveNetworkRuleCollectionByName ist keine Unterscheidung nach Groß-/Kleinschreibung.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-127">The rule collection name for method RemoveNetworkRuleCollectionByName is case-insensitive.</span></span>

### <span data-ttu-id="6cfe6-128">9: Abrufen einer Firewall und Zuweisen der Firewall</span><span class="sxs-lookup"><span data-stu-id="6cfe6-128">9:  Retrieve a firewall and then allocate the firewall</span></span>
```
$vnet=Get-AzureRmVirtualNetwork -Name "vnet" -ResourceGroupName "rgName"
$publicIp=Get-AzureRmPublicIpAddress -Name "firewallpip" -ResourceGroupName "rgName"
$azFw=Get-AzureRmFirewall -Name "azFw" -ResourceGroupName "rgName"
$azFw.Allocate($vnet, $publicIp)
```

<span data-ttu-id="6cfe6-129">In diesem Beispiel wird eine Firewall abgerufen und die Zuweisung für die Firewall aufgerufen, um den Firewalldienst mithilfe der Konfiguration (Anwendung und Netzwerkregel Sammlungen) zu starten, die der Firewall zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-129">This example retrieves a firewall and calls Allocate on the firewall to start the firewall service using the configuration (application and network rule collections) associated with the firewall.</span></span>

## <span data-ttu-id="6cfe6-130">Parameter</span><span class="sxs-lookup"><span data-stu-id="6cfe6-130">PARAMETERS</span></span>

### <span data-ttu-id="6cfe6-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6cfe6-131">-DefaultProfile</span></span>
<span data-ttu-id="6cfe6-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6cfe6-133">-Name</span><span class="sxs-lookup"><span data-stu-id="6cfe6-133">-Name</span></span>
<span data-ttu-id="6cfe6-134">Gibt den Namen der Firewall an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-134">Specifies the name of the Firewall that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cfe6-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6cfe6-135">-ResourceGroupName</span></span>
<span data-ttu-id="6cfe6-136">Gibt den Namen der Ressourcengruppe an, zu der die Firewall gehört.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-136">Specifies the name of the resource group that Firewall belongs to.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6cfe6-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6cfe6-137">CommonParameters</span></span>
<span data-ttu-id="6cfe6-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6cfe6-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6cfe6-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6cfe6-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6cfe6-140">INPUTS</span></span>

### <span data-ttu-id="6cfe6-141">Keine</span><span class="sxs-lookup"><span data-stu-id="6cfe6-141">None</span></span>
<span data-ttu-id="6cfe6-142">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="6cfe6-142">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="6cfe6-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6cfe6-143">OUTPUTS</span></span>

### <span data-ttu-id="6cfe6-144">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="6cfe6-144">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="6cfe6-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="6cfe6-145">NOTES</span></span>

## <span data-ttu-id="6cfe6-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6cfe6-146">RELATED LINKS</span></span>

[<span data-ttu-id="6cfe6-147">Neu – AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="6cfe6-147">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="6cfe6-148">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="6cfe6-148">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)

[<span data-ttu-id="6cfe6-149">Satz-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="6cfe6-149">Set-AzureRmFirewall</span></span>](./Set-AzureRmFirewall.md)
