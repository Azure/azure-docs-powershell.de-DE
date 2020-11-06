---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 40E56EC1-3327-4DFF-8262-E2EEBB5E4447
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermfirewall
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmFirewall.md
ms.openlocfilehash: 8f2c2560ac8ca0787a8a0eb8d37fb5242f4a915e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476030"
---
# <span data-ttu-id="8eb73-101">Set-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="8eb73-101">Set-AzureRmFirewall</span></span>

## <span data-ttu-id="8eb73-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="8eb73-102">SYNOPSIS</span></span>
<span data-ttu-id="8eb73-103">Speichert eine geänderte Firewall.</span><span class="sxs-lookup"><span data-stu-id="8eb73-103">Saves a modified Firewall.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8eb73-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="8eb73-104">SYNTAX</span></span>

```
Set-AzureRmFirewall -AzureFirewall <PSAzureFirewall> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8eb73-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8eb73-105">DESCRIPTION</span></span>
<span data-ttu-id="8eb73-106">Das Cmdlet " **Satz-AzureRmFirewall** " aktualisiert eine Azure-Firewall.</span><span class="sxs-lookup"><span data-stu-id="8eb73-106">The **Set-AzureRmFirewall** cmdlet updates an Azure Firewall.</span></span>

## <span data-ttu-id="8eb73-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="8eb73-107">EXAMPLES</span></span>

### <span data-ttu-id="8eb73-108">1: Aktualisieren der Priorität einer Firewall-Anwendungsregel Sammlung</span><span class="sxs-lookup"><span data-stu-id="8eb73-108">1:  Update priority of a Firewall application rule collection</span></span>
```
$azFw = Get-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg"
$ruleCollection = $azFw.GetApplicationRuleCollectionByName("ruleCollectionName")
$ruleCollection.Priority = 101
Set-AzureRmFirewall -Firewall $azFw
```

<span data-ttu-id="8eb73-109">In diesem Beispiel wird die Priorität einer vorhandenen Regelsammlung einer Azure-Firewall aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="8eb73-109">This example updates the priority of an existing rule collection of an Azure Firewall.</span></span>
<span data-ttu-id="8eb73-110">Wenn die Azure Firewall "AzureFirewall" in der Ressourcengruppe "RG" eine Anwendungsregel Sammlung mit dem Namen "ruleCollectionName" enthält, werden die oben aufgeführten Befehle die Priorität dieser Regelsammlung ändern und anschließend die Azure-Firewall aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="8eb73-110">Assuming Azure Firewall "AzureFirewall" in resource group "rg" contains an application rule collection named "ruleCollectionName", the commands above will change the priority of that rule collection and update the Azure Firewall afterwards.</span></span> <span data-ttu-id="8eb73-111">Ohne den Befehl Set-AzureRmFirewall werden alle Vorgänge, die für das lokale $azFw Objekt ausgeführt werden, nicht auf dem Server widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="8eb73-111">Without the Set-AzureRmFirewall command, all operations performed on the local $azFw object are not reflected on the server.</span></span>

### <span data-ttu-id="8eb73-112">2: Erstellen einer Azure Firewall und späteres Einrichten einer Anwendungsregel Sammlung</span><span class="sxs-lookup"><span data-stu-id="8eb73-112">2:  Create a Azure Firewall and set an application rule collection later</span></span>
```
$azFw = New-AzureRmFirewall -Name "AzureFirewall" -ResourceGroupName "rg" -VirtualNetworkName "vnet-name" -PublicIpName "pip-name"

$rule = New-AzureRmFirewallApplicationRule -Name R1 -Protocol "http:80","https:443" -TargetFqdn "*google.com", "*microsoft.com" -SourceAddress "10.0.0.0"
$RuleCollection = New-AzureRmFirewallApplicationRuleCollection -Name RC1 -Priority 100 -Rule $rule -ActionType "Allow"
$azFw.ApplicationRuleCollections = $RuleCollection

$azFw | Set-AzureRmFirewall
```

<span data-ttu-id="8eb73-113">In diesem Beispiel wird zunächst eine Firewall ohne Anwendungsregel Sammlungen erstellt.</span><span class="sxs-lookup"><span data-stu-id="8eb73-113">In this example, a Firewall is created first without any application rule collections.</span></span> <span data-ttu-id="8eb73-114">Anschließend werden eine Anwendungsregel und eine Anwendungsregel Sammlung erstellt, und das firewallobjekt wird im Arbeitsspeicher geändert, ohne dass sich dies auf die reale Konfiguration in der Cloud auswirkt.</span><span class="sxs-lookup"><span data-stu-id="8eb73-114">Afterwards a Application Rule and Application Rule Collection are created, then the Firewall object is modified in memory, without affecting the real configuration in cloud.</span></span> <span data-ttu-id="8eb73-115">Damit Änderungen in der Cloud wiedergegeben werden, müssen Set-AzureRmFirewall aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8eb73-115">For changes to be reflected in cloud, Set-AzureRmFirewall must be called.</span></span>

## <span data-ttu-id="8eb73-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="8eb73-116">PARAMETERS</span></span>

### <span data-ttu-id="8eb73-117">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8eb73-117">-AsJob</span></span>
<span data-ttu-id="8eb73-118">Ausführen eines Cmdlets im Hintergrund</span><span class="sxs-lookup"><span data-stu-id="8eb73-118">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8eb73-119">-AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="8eb73-119">-AzureFirewall</span></span>
<span data-ttu-id="8eb73-120">Die AzureFirewall</span><span class="sxs-lookup"><span data-stu-id="8eb73-120">The AzureFirewall</span></span>

```yaml
Type: PSAzureFirewall
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8eb73-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8eb73-121">-DefaultProfile</span></span>
<span data-ttu-id="8eb73-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="8eb73-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8eb73-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="8eb73-123">-Confirm</span></span>
<span data-ttu-id="8eb73-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="8eb73-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb73-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8eb73-125">-WhatIf</span></span>
<span data-ttu-id="8eb73-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8eb73-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8eb73-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8eb73-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8eb73-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8eb73-128">CommonParameters</span></span>
<span data-ttu-id="8eb73-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8eb73-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8eb73-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8eb73-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8eb73-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="8eb73-131">INPUTS</span></span>

### <span data-ttu-id="8eb73-132">PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="8eb73-132">PSAzureFirewall</span></span>
<span data-ttu-id="8eb73-133">Der Parameter "AzureFirewall" akzeptiert den Wert vom Typ "PSAzureFirewall" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="8eb73-133">Parameter 'AzureFirewall' accepts value of type 'PSAzureFirewall' from the pipeline</span></span>

## <span data-ttu-id="8eb73-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="8eb73-134">OUTPUTS</span></span>

### <span data-ttu-id="8eb73-135">Microsoft. Azure. Commands. Network. Models. PSAzureFirewall</span><span class="sxs-lookup"><span data-stu-id="8eb73-135">Microsoft.Azure.Commands.Network.Models.PSAzureFirewall</span></span>

## <span data-ttu-id="8eb73-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="8eb73-136">NOTES</span></span>

## <span data-ttu-id="8eb73-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="8eb73-137">RELATED LINKS</span></span>

[<span data-ttu-id="8eb73-138">Get-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="8eb73-138">Get-AzureRmFirewall</span></span>](./Get-AzureRmFirewall.md)

[<span data-ttu-id="8eb73-139">Neu – AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="8eb73-139">New-AzureRmFirewall</span></span>](./New-AzureRmFirewall.md)

[<span data-ttu-id="8eb73-140">Remove-AzureRmFirewall</span><span class="sxs-lookup"><span data-stu-id="8eb73-140">Remove-AzureRmFirewall</span></span>](./Remove-AzureRmFirewall.md)
